# Work-Task Frontend

Фронтенд для таск-трекера Work-Task на базе Next.js 14, TypeScript и REST API.

## 🚀 Быстрый старт

```bash
# Установить зависимости
npm install

# Запустить dev-сервер
npm run dev

# Сборка для продакшена
npm run build
npm start
```

## 📁 Структура проекта

- `src/app/` — роутинг, layout, страницы (Next.js App Router)
- `src/components/` — переиспользуемые UI-компоненты (группировка по смыслу)
- `src/features/` — бизнес-логика по доменам: auth, projects, tasks
- `src/lib/` — API-клиенты, типы, утилиты
- `src/hooks/` — кастомные React-хуки
- `public/` — статические файлы (иконки, лого)

## 🧩 Основные технологии

- **Next.js 14** — SSR/SSG, App Router
- **TypeScript** — строгая типизация
- **React Query** — кэширование и работа с API
- **Tailwind CSS** — стилизация
- **Radix UI** — базовые UI-примитивы

## 🛠️ Основные команды

- `npm run dev` — запуск в режиме разработки
- `npm run build` — сборка
- `npm start` — запуск production-сервера
- `npm run lint` — проверка кода

## 📝 Документация

- [Next.js Docs](https://nextjs.org/docs)
- [React Query](https://tanstack.com/query/latest)
- [Tailwind CSS](https://tailwindcss.com/docs)
- [Radix UI](https://www.radix-ui.com/docs/primitives/overview/introduction)

## 💡 Советы по разработке

- Все бизнес-фичи — в `src/features/`, UI-атомы — в `src/components/ui/`
- Для новых API-эндпоинтов — добавляйте хуки в `features/*/api/`
- Используйте кэширование React Query для мгновенного UX
- Не храните бизнес-логику в UI-компонентах

---

**Автор:** @krutakov
