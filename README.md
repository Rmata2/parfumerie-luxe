import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { ShoppingCart } from "lucide-react";

const perfumes = [
  {
    id: 1,
    name: "Élégance Noire", 
    image: "https://images.unsplash.com/photo-1604200218755-6f83a0b820bd",
    price: "€38.99",
    link: "https://fr.aliexpress.com/item/1005001234567890.html"
  },
  {
    id: 2,
    name: "Mystic Oud",
    image: "https://images.unsplash.com/photo-1603810475800-671fe2156be8",
    price: "€45.49",
    link: "https://fr.aliexpress.com/item/1005000987654321.html"
  },
  {
    id: 3,
    name: "Saphir Royale",
    image: "https://images.unsplash.com/photo-1596887130684-a1d6826e1ecb",
    price: "€51.99",
    link: "https://fr.aliexpress.com/item/1005001122334455.html"
  },
  {
    id: 4,
    name: "Velours Nuit",
    image: "https://images.unsplash.com/photo-1623776058974-58044c49fd51",
    price: "€36.39",
    link: "https://fr.aliexpress.com/item/1005002233445566.html"
  },
  {
    id: 5,
    name: "Ambre Suprême",
    image: "https://images.unsplash.com/photo-1622448782658-b08d20e1df4a",
    price: "€58.49",
    link: "https://fr.aliexpress.com/item/1005003344556677.html"
  }
];

export default function PerfumeStore() {
  return (
    <div className="p-10 bg-gradient-to-r from-gray-900 via-gray-800 to-gray-900 min-h-screen text-white font-serif">
      <h1 className="text-5xl font-extrabold text-center mb-10 tracking-wide">Boutique de Parfums de Luxe</h1>
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        {perfumes.map((perfume) => (
          <Card key={perfume.id} className="p-6 shadow-2xl bg-gray-800 rounded-2xl border border-gray-700">
            <img src={perfume.image} alt={perfume.name} className="w-full h-60 object-cover rounded-lg" />
            <CardContent className="mt-6 text-center">
              <h2 className="text-3xl font-bold text-white italic">{perfume.name}</h2>
              <p className="text-xl text-gray-300 font-light tracking-wider">{perfume.price}</p>
              <Button className="mt-6 bg-gold-500 hover:bg-gold-600 text-black font-semibold py-3 px-5 rounded-lg flex items-center gap-2 uppercase tracking-wide" asChild>
                <a href={perfume.link} target="_blank" rel="noopener noreferrer">
                  <ShoppingCart size={18} /> Acheter
                </a>
              </Button>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}
