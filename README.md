import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { useState } from "react";
import { motion } from "framer-motion";

export default function SalesMentorship() {
  const [email, setEmail] = useState("");

  return (
    <div className="min-h-screen bg-gray-100 p-6 flex flex-col items-center">
      <motion.h1 
        className="text-4xl font-bold mb-4 text-center" 
        initial={{ opacity: 0, y: -20 }} 
        animate={{ opacity: 1, y: 0 }}
      >
        Наставничество по продажам для предпринимателей
      </motion.h1>
      <motion.p 
        className="text-lg text-gray-600 text-center max-w-2xl mb-6"
        initial={{ opacity: 0, y: 20 }} 
        animate={{ opacity: 1, y: 0 }}
      >
        Помогаю выстроить систему продаж, чтобы ваш бизнес зарабатывал больше и работал предсказуемо.
      </motion.p>
      <Card className="max-w-3xl w-full p-6 shadow-xl rounded-2xl bg-white">
        <CardContent className="space-y-6">
          <h2 className="text-2xl font-semibold text-center">Что входит в программу:</h2>
          <ul className="list-disc list-inside space-y-2 text-gray-700">
            <li>Разработка структуры отдела продаж</li>
            <li>Настройка скриптов и обработка возражений</li>
            <li>Контроль, отчёты и мотивация сотрудников</li>
            <li>Личное сопровождение и разбор кейсов</li>
          </ul>
          <div className="text-center mt-4">
            <p className="text-lg font-medium">Готовы увеличить продажи?</p>
            <div className="mt-4 flex flex-col sm:flex-row items-center gap-4">
              <Input 
                type="email" 
                placeholder="Ваш email" 
                value={email} 
                onChange={(e) => setEmail(e.target.value)}
                className="flex-1 p-3 border rounded-lg"
              />
              <Button className="bg-blue-600 text-white px-6 py-3 rounded-lg">Записаться</Button>
            </div>
          </div>
        </CardContent>
      </Card>
    </div>
  );
}
