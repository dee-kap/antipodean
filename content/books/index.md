---
layout: layouts/base.njk
---

# Books

Reading books is one of my favourite pass times. I like to read all kinds of books including Non-Fiction, History, Science, Biographies, Finance, Classics.

First book I ever read was Dracula by Bram Stoker and that got me hooked on reading.

These are some of the books I have in my library. I have given a star rating to the books I have read, the others either I have not read or would like to read again.

<!-- <div style="font-size:18px">
    <a href="/books/2024">2024</a>
    /
    <a href="/books/2023">2023</a>
</div> -->

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