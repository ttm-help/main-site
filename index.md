---
layout: default
date: 2025-10-22
keywords: ""
image: ""
---

<div style="padding-top: 150px">
    <div class="container mx-auto" style="w-75">
        <div class="row">
            <div class="col-auto" style="min-width: 400px;">
                {% include social-links.html %}
            </div>
            <div class="col d-flex flex-column align-items-end text-end">
                <img src="/assets/images/main.jpg"
                        style="height:300px"
                        class="figure-img img-fluid rounded-5 shadow"
                        alt="{{ page.title }}"/>
                <h2>Я Оксана Коновалова — Психолог,<br/><small class="text-body-secondary">специализирующийся на трихотилломании</small></h2>
            </div>
        </div>

        <div class="row mt-5">
            <div class="col-auto" style="min-width: 400px;">
                Обо мне
            </div>
            <div class="col">
                <p>Работаю с 2012 года и использую доказательные методы психотерапии, признанные ведущими международными организациями — APA (Американская психологическая ассоциация), NICE (Национальный институт здравоохранения Великобритании) и Всемирной организацией здравоохранения (WHO).</p>
                <p>Протоколы работы прошли десятки клинических исследований — измеримо, безопасно и без магического мышления. </p>
            </div>
        </div>

        <div class="row mt-5">
             <div class="col-auto" style="min-width: 400px;">
                С чем я работаю
            </div>
            <div class="col">
                {% assign services = site.data.services.list %}
                {% for service in services %}
                    <div class="row align-items-center">
                        <div class="col-auto d-flex align-items-center">
                            <img 
                              src="{{ service.url }}"
                              width="110" height="110"
                              class="figure-img img-fluid rounded-5 shadow"
                            />
                            </div>
                            <div class="col d-flex align-items-center">
                            <div>
                              <span class="fw-bold">{{ service.name }}</span> <br/>
                              <span>{{ service.description }}</span>
                            </div>
                        </div>
                    </div>
                {% endfor %}
            </div>
        </div>


        <div class="row mt-5">
            <div class="col-auto" style="min-width: 400px;">
                Как проходит работа
            </div>
            <div class="col">
                <p>Онлайн, 1 раз в неделю, продолжительность 55 минут. Между встречами — поддержка и упражнения, чтобы результат закреплялся в реальной жизни.</p>
            </div>
        </div>


        <div class="row mt-5">
            <div class="col-auto" style="min-width: 400px;">
                Образование
            </div>
            <div class="col">
                {% assign educations = site.data.education.list %}
                {% for education in educations %}
                    <div class="row">
                        <span class="fw-bold">{{ education.name }}</span><br/>
                        <span>{{ education.institute }}</span>
                    </div>
                    <hr style="margin: 20px 0">
                {% endfor %}
            </div>
        </div>


        <div class="row mt-5">
            <div class="col-auto" style="min-width: 400px;">
                Отзывы
            </div>
            <div class="col d-flex">
                <div class="video-scroll-wrapper w-100">
                    {% assign feedbacks = site.data.feedbacks.list %}
                    {% for feedback in feedbacks %}
                        <div class="video-card">
                            <img src="{{ feedback.url }}">
                            <p class="fw-bold mt-2 mb-1">{{ feedback.name }}</p>
                        </div>
                    {% endfor %}
                </div>
            </div>
        </div>


        <div class="row mt-5">
            <div class="col-auto" style="min-width: 400px;">
                Стоимость
            </div>
            <div class="col">
                <div class="row row-cols-1 row-cols-md-4 g-4 mt-4">
                    {% assign offers = site.data.offers.list %}
                    {% for offer in offers %}
                        <div class="col">
                            <div class="card card-clean h-100 rounded-4 p-3">
                                <p class="fw-bold">{{ offer.name }}</p>
                                <p class="mt-2">
                                    {{ offer.description }}
                                </p>
                                <p class="fs-4 fw-bold mt-3">{{ offer.price }}</p>
                                <a href="#" class="btn btn-dark w-100 mt-2 mb-3">Записаться</a>
                            </div>
                        </div>
                    {% endfor %}
                </div>
            </div>
        </div>


        {% include footer.html %}
    </div>
</div>
