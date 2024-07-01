# Справочник Vue 3

https://ru.vuejs.org/guide/introduction.html

## Создание приложения

```
import { createApp } from 'vue'
// импорт корневого компонента App из однофайлового компонента
import App from './App.vue'

const app = createApp(App)
```

В функицию createApp обязательно должен быть передан корневой компонент,
который содержит в себе другие компоненты.

`<div id="app"></div>`

`app.mount('#app')`

Экземпляр приложения не будет ничего отрисовывать, пока не вызвать его метод .mount().

```
app.config.errorHandler = (err) => {
  /* обработка ошибки */
}
```

Экземпляр приложения предоставляет объект .config.

## Синтаксис шаблонов

### Текстовые интерполяции
​
`<span>Сообщение: {{ msg }}</span>`

### Сырой HTML
​
`<p>Директива v-html: <span v-html="rawHtml"></span></p>`

### Атрибуты

`<div v-bind:id="dynamicId"></div>`

`<div :id="dynamicId"></div>`

```
<!-- так же, как :id="id" -->
<div :id></div>

<!-- это также работает -->
<div v-bind:id></div>
```

### Булевы атрибуты

`<button :disabled="isButtonDisabled">Кнопка</button>`

Атрибут disabled будет добавляться, когда значение isButtonDisabled истинно. 
Он также будет добавляться, если значением будет пустая строка, для сохранения консистентности с <button disabled="">. 
При использовании других ложных значений атрибут будет опущен.