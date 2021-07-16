# Viento portfolio REST API

1. Get list a portfolio
2. Get portfolio by ID

## Get list a portfolio

* Method 
``` GET ```
* Respons body
```
{
    content: [
        {
            id: int,
            image: Str,
            name_ru: Str,
            name_uz: Str,
            name_en: Str,
        },
        ....
    ],
    pagination:{
        page: Current page,
        last_page: Last page,
        per_page: Count current page
    }
}
```

## Get portfolio by ID

* Method 
``` GET ```
* Request parameters
``` 
Portfolio ID
```
* Respons body
```
{
    id: int,
    image: Str,
    name_ru: Str,
    name_uz: Str,
    name_en: Str,
    website_url: Str,
    benefits:[
        {
            name_ru: Str,
            name_uz: Str,
            name_en: Str,
            desc_ru: Str,
            desc_uz: Str,
            desc_en: Str,
        }
    ],
    images:[
        'url.images/original.jpg',
        ...
    ],
    content_title: Str,
    content_desc: Str,
    made_for_project:{
        title: 'Сайт, Брендинг, SMM' //это пример
        list: [
            'Концепция',
            'Анимация',
            'Опыт пользователя (UX)',
            'Мобильная версия',
            'Дизайн','Интерфейс (UI)',
            'Программирование'
        ]
    },
    main_images: Str,
    next_portfolio: {
        id: int,
        name_ru: Str,
        name_uz: Str,
        name_en: Str,
        name_image: Str,
    }
}
```
