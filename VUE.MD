# Справочник Vue 3

https://ru.vuejs.org/guide/introduction.html

## Создание приложения

`
import { createApp } from 'vue'
// импорт корневого компонента App из однофайлового компонента
import App from './App.vue'

const app = createApp(App)
`

В функицию createApp обязательно должен быть передан корневой компонент,
который содержит в себе другие компоненты.

`<div id="app"></div>`
`app.mount('#app')`

Экземпляр приложения не будет ничего отрисовывать, пока не вызвать его метод .mount().

`
app.config.errorHandler = (err) => {
  /* обработка ошибки */
}
`

Экземпляр приложения предоставляет объект .config.

## Синтаксис шаблонов