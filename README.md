import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

const products = [
  {
    id: 1,
    name: "Gray & Black Cap",
    image: "/images/merch/gray-and-black-cap.jpg",
    description: "Sleek and stylish gray & black cap for drift fans.",
  },
  {
    id: 2,
    name: "Gray Flat Cap",
    image: "/images/merch/gray-flat-cap.jpg",
    description: "Classic gray flat cap to complete your fit.",
  },
  {
    id: 3,
    name: "Pink Flat Cap",
    image: "/images/merch/pink-flat-cap.jpg",
    description: "Bold pink flat cap for the sideways enthusiast.",
  },
];

export default function HomePage() {
  return (
    <main
      className="min-h-screen text-white p-6 bg-cover bg-center"
      style={{ backgroundImage: "url('/images/background.jpg')" }}
    >
      <section className="max-w-4xl mx-auto text-center">
        <img
          src="/images/header-banner.png"
          alt="Sideways Sensation Banner"
          className="w-full rounded-xl shadow-lg mb-4"
        />
        <h2 className="text-lg text-pink-400 underline mb-6">
          www.sidewayssensation.co.za
        </h2>
      </section>

      <section className="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-6 mt-10">
        {products.map((item) => (
          <Card key={item.id} className="bg-zinc-900 bg-opacity-90 rounded-2xl shadow-md">
            <CardContent className="p-6">
              <img
                src={item.image}
                alt={item.name}
                className="w-full object-cover rounded-xl mb-4"
              />
              <h2 className="text-2xl font-semibold mb-2">{item.name}</h2>
            </CardContent>
          </Card>
        ))}
      </section>

      <section className="max-w-xl mx-auto mt-12 bg-black bg-opacity-70 p-6 rounded-2xl text-center">
        <p className="text-white text-lg mb-6">
          Away to build a drift community in South Africa, a sideways style. This would help with the projects soon to come in my YouTube channel. Show so Flex, stay sideways!
        </p>
        <div className="flex justify-center gap-4 mb-4">
          <Button className="bg-pink-500 hover:bg-pink-600 text-white px-6 py-2 rounded-xl">
            Shop Now!
          </Button>
          <Button className="border border-white text-white px-6 py-2 rounded-xl">
            See More!
          </Button>
        </div>
        <p className="text-sm text-zinc-400">@sidewayssensation</p>
      </section>
    </main>
  );
}
