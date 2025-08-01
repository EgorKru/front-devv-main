# src/features/tasks/api

Здесь размещаются хуки и функции для работы с задачами через REST API WorkTech.

## Структура
- **use-get-tasks.ts** — получение всех задач активного проекта.
- **use-create-task.ts** — создание новой задачи.
- **use-update-task.ts** — обновление задачи.
- **...** — другие хуки для работы с комментариями, статусами, связями задач и т.д.

## Как работает
- Каждый хук инкапсулирует вызов определённого эндпоинта WorkTech API.
- Все хуки используют централизованный API-клиент (`rpc.ts`) для авторизации, обработки токенов и ошибок.
- Возвращают данные, статус загрузки, ошибки и функции для вызова (например, `mutate` для создания/обновления).

## Пример использования

```tsx
import { useGetTasks } from './use-get-tasks';

const { data: tasks, isLoading, error } = useGetTasks();

if (isLoading) return <Loader />;
if (error) return <ErrorMessage />;

return <TaskList tasks={tasks} />;
```

> Все функции используют централизованный API-клиент (rpc.ts) для запросов к серверу. 