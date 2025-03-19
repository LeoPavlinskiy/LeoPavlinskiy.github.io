# Personal Website Template

This repository contains a personal website template with a clean, modern design inspired by Apple UI Guidelines. The website is fully configurable through embedded JavaScript configuration.

## Features

- Light and dark themes
- Responsive design
- Configurable sections (About, Resume, Teaching, Activities, Publications)
- Easy to customize content
- No server-side code required

## Getting Started

1. Clone this repository
2. Open `index.html` (light theme) or `index-dark.html` (dark theme) in your browser
3. Customize the content by editing the configuration in the HTML file

## Content Configuration

The website content is configured through a JavaScript object in the HTML file. You can edit this object to customize your website.

### Site Configuration

```javascript
"site": {
  "title": "Your Name",
  "theme": "light", // or "dark"
  "favicon": "./assets/images/logo.ico"
}
```

### Personal Information

```javascript
"personal": {
  "name": "Your Name",
  "title": "Your Title",
  "avatar": "./assets/images/my-avatar.png",
  "contacts": [
    {
      "type": "email",
      "icon": "mail-outline",
      "title": "Email",
      "value": "your.email@example.com",
      "link": "mailto:your.email@example.com"
    },
    // Add more contacts here
  ],
  "social": [
    {
      "icon": "logo-linkedin",
      "link": "https://www.linkedin.com/in/your-profile/"
    },
    // Add more social links here
  ]
}
```

### Sections

The website supports the following sections:

#### About

```javascript
"about": {
  "enabled": true, // Set to false to disable this section
  "title": "About",
  "content": [
    "First paragraph of your bio.",
    "Second paragraph of your bio.",
    // Add more paragraphs here
  ]
}
```

#### Resume

```javascript
"resume": {
  "enabled": true, // Set to false to disable this section
  "title": "Resume",
  "education": [
    {
      "title": "University Name",
      "period": "City, Year — Year",
      "description": "Degree and other details"
    },
    // Add more education items here
  ],
  "experience": [
    {
      "title": "Job Title, Company",
      "period": "Month Year — Month Year",
      "items": [
        "Responsibility or achievement 1",
        "Responsibility or achievement 2",
        // Add more items here
      ]
    },
    // Add more experience items here
  ]
}
```

#### Teaching

```javascript
"teaching": {
  "enabled": true, // Set to false to disable this section
  "title": "Teaching",
  "courses": [
    {
      "title": "Course Name",
      "period": "Institution, Year — Year",
      "description": "Course description"
    },
    // Add more courses here
  ]
}
```

#### Activities

```javascript
"activities": {
  "enabled": true, // Set to false to disable this section
  "title": "Activities",
  "conferences": [
    {
      "title": "Conference Name",
      "period": "Years",
      "description": "Your role or contribution"
    },
    // Add more conferences here
  ],
  "workshops": [
    {
      "title": "Workshop Name",
      "period": "Year",
      "description": "Your role or contribution"
    },
    // Add more workshops here
  ]
}
```

#### Publications

```javascript
"publications": {
  "enabled": true, // Set to false to disable this section
  "title": "Publications",
  "webArticles": [
    {
      "title": "Article Title",
      "category": "Category",
      "date": "YYYY-MM-DD",
      "displayDate": "Month DD, YYYY",
      "description": "Brief description",
      "link": "https://example.com/article"
    },
    // Add more web articles here
  ],
  "researchPapers": [
    {
      "authors": "Author 1, Author 2, ...",
      "title": "Paper Title",
      "publication": "Conference or Journal, Year"
    },
    // Add more research papers here
  ]
}
```

## Customizing Icons

The website uses [Ionicons](https://ionicons.com/) for icons. You can browse the available icons on their website and use the icon name in your configuration.

## Customizing Styles

You can customize the styles by editing the CSS in the HTML file or by modifying the `assets/css/apple-style.css` file.

## System Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Basic knowledge of HTML and JavaScript for customization
- Git (optional, for version control)

## Installation

### Local Development

1. Clone this repository:
```bash
git clone https://github.com/yourusername/personal-website.git
cd personal-website
```

2. Install a local server (optional, but recommended):
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx http-server
```

3. Open `http://localhost:8000` in your browser

### GitHub Pages Deployment

1. Fork this repository
2. Go to repository Settings > Pages
3. Select 'main' branch as source
4. Your site will be available at `https://yourusername.github.io/repository-name`

## Customization Examples

### Adding a New Section

1. Add configuration to your HTML file:
```javascript
"newSection": {
  "enabled": true,
  "title": "New Section",
  "items": [
    {
      "title": "Item Title",
      "description": "Item description"
    }
  ]
}
```

2. Add the section to the HTML structure:
```html
<section class="new-section" data-page="new-section">
  <div class="section-title-wrapper">
    <h3 class="h3 section-title">New Section</h3>
  </div>
  <div class="section-content">
    <!-- Your content here -->
  </div>
</section>
```

### Customizing Colors

Edit the CSS variables in `assets/css/apple-style.css`:

```css
:root {
  --primary-color: #your-color;
  --secondary-color: #your-color;
}
```

## Screenshots

![Light Theme](./assets/images/screenshots/light-theme.png)
![Dark Theme](./assets/images/screenshots/dark-theme.png)
![Mobile View](./assets/images/screenshots/mobile-view.png)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Design inspired by Apple UI Guidelines
- Icons by [Ionicons](https://ionicons.com/)
- Fonts by Google Fonts

---

# Шаблон персонального сайта

Этот репозиторий содержит шаблон персонального сайта с чистым, современным дизайном, вдохновленным руководствами по дизайну Apple. Сайт полностью настраивается через встроенную JavaScript-конфигурацию.

## Особенности

- Светлая и темная темы
- Адаптивный дизайн
- Настраиваемые разделы (О себе, Резюме, Преподавание, Деятельность, Публикации)
- Простая настройка содержимого
- Не требуется серверный код

## Начало работы

1. Клонируйте этот репозиторий
2. Откройте `index.html` (светлая тема) или `index-dark.html` (темная тема) в вашем браузере
3. Настройте содержимое, отредактировав конфигурацию в HTML-файле

## Настройка содержимого

Содержимое сайта настраивается через JavaScript-объект в HTML-файле. Вы можете редактировать этот объект для настройки вашего сайта.

### Настройка сайта

```javascript
"site": {
  "title": "Ваше имя",
  "theme": "light", // или "dark"
  "favicon": "./assets/images/logo.ico"
}
```

### Личная информация

```javascript
"personal": {
  "name": "Ваше имя",
  "title": "Ваша должность",
  "avatar": "./assets/images/my-avatar.png",
  "contacts": [
    {
      "type": "email",
      "icon": "mail-outline",
      "title": "Email",
      "value": "your.email@example.com",
      "link": "mailto:your.email@example.com"
    },
    // Добавьте больше контактов здесь
  ],
  "social": [
    {
      "icon": "logo-linkedin",
      "link": "https://www.linkedin.com/in/your-profile/"
    },
    // Добавьте больше социальных ссылок здесь
  ]
}
```

### Разделы

Сайт поддерживает следующие разделы:

#### О себе

```javascript
"about": {
  "enabled": true, // Установите false, чтобы отключить этот раздел
  "title": "О себе",
  "content": [
    "Первый абзац вашей биографии.",
    "Второй абзац вашей биографии.",
    // Добавьте больше абзацев здесь
  ]
}
```

#### Резюме

```javascript
"resume": {
  "enabled": true, // Установите false, чтобы отключить этот раздел
  "title": "Резюме",
  "education": [
    {
      "title": "Название университета",
      "period": "Город, Год — Год",
      "description": "Степень и другие детали"
    },
    // Добавьте больше пунктов образования здесь
  ],
  "experience": [
    {
      "title": "Должность, Компания",
      "period": "Месяц Год — Месяц Год",
      "items": [
        "Обязанность или достижение 1",
        "Обязанность или достижение 2",
        // Добавьте больше пунктов здесь
      ]
    },
    // Добавьте больше пунктов опыта работы здесь
  ]
}
```

#### Преподавание

```javascript
"teaching": {
  "enabled": true, // Установите false, чтобы отключить этот раздел
  "title": "Преподавание",
  "courses": [
    {
      "title": "Название курса",
      "period": "Учреждение, Год — Год",
      "description": "Описание курса"
    },
    // Добавьте больше курсов здесь
  ]
}
```

#### Деятельность

```javascript
"activities": {
  "enabled": true, // Установите false, чтобы отключить этот раздел
  "title": "Деятельность",
  "conferences": [
    {
      "title": "Название конференции",
      "period": "Годы",
      "description": "Ваша роль или вклад"
    },
    // Добавьте больше конференций здесь
  ],
  "workshops": [
    {
      "title": "Название воркшопа",
      "period": "Год",
      "description": "Ваша роль или вклад"
    },
    // Добавьте больше воркшопов здесь
  ]
}
```

#### Публикации

```javascript
"publications": {
  "enabled": true, // Установите false, чтобы отключить этот раздел
  "title": "Публикации",
  "webArticles": [
    {
      "title": "Заголовок статьи",
      "category": "Категория",
      "date": "ГГГГ-ММ-ДД",
      "displayDate": "Месяц ДД, ГГГГ",
      "description": "Краткое описание",
      "link": "https://example.com/article"
    },
    // Добавьте больше веб-статей здесь
  ],
  "researchPapers": [
    {
      "authors": "Автор 1, Автор 2, ...",
      "title": "Название статьи",
      "publication": "Конференция или журнал, Год"
    },
    // Добавьте больше научных статей здесь
  ]
}
```

## Настройка иконок

Сайт использует [Ionicons](https://ionicons.com/) для иконок. Вы можете просмотреть доступные иконки на их сайте и использовать имя иконки в вашей конфигурации.

## Настройка стилей

Вы можете настроить стили, отредактировав CSS в HTML-файле или изменив файл `assets/css/apple-style.css`. 