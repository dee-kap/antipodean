---
layout: layouts/base.njk
---

# Books

Reading books is one of my favourite pass times. I feel blessed that I picked up this habit during my high school days and it has stayed with me since then.

<div style="font-size:18px">
    <a href="/books/2024">2024</a>
    /
    <a href="/books/2023">2023</a>
</div>

<div class="books-list">
  {%- for book in books -%}
    <div class="book" style="background-image: url('/images/covers/{{ book.image }}')">
      <div class="book-title">
        {{ book.displayTitle or book.title }}
        <div class="book-rating">
        {%- set rating = book.rating | int -%}
        {%- for i in range(1, 6) -%}
            <span class="star {% if i <= rating %}filled{% endif %}">★</span>
          {%- endfor %}
        </div>
      </div>
    </div>
  {%- endfor %}
</div>