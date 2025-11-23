---
layout: default
date: 2025-10-22
keywords: ""
image: ""
---

<div>
    <div class="container mx-auto" style="w-75">
        <div class="row responsive-padding">
           <div class="col-12 col-md-3 mb-5">
                {% include social-links.html %}
            </div>
            <div class="col-12 col-md-9 d-flex flex-column align-items-center align-items-md-end text-center text-md-end">
                <img src="/assets/images/main.jpg"
                        style="height:600px"
                        class="figure-img img-fluid rounded-5 shadow mb-3"
                        alt="{{ page.title }}"/>
                <div class="me-3 text-end">
                    <span class="fs-4">Я, Оксана Коновалова — клинический психолог,<br/><small class="text-body-secondary">доказательные протоколы КПТ и ДБТ</small></span>
                </div>
            </div>
        </div>

        <div class="row responsive-padding">
           <div class="col-12 col-md-3 mb-5">
                <span class="display-7">
                    Обо мне
                </span>
            </div>
            <div class="col-12 col-md-9">
                <div class="mx-3 fs-5">
                    <p>Работаю с 2012 года и использую доказательные методы психотерапии, признанные ведущими международными организациями — APA (Американская психологическая ассоциация), NICE (Национальный институт здравоохранения Великобритании) и Всемирной организацией здравоохранения (WHO).</p>
                    <p>Протоколы работы прошли десятки клинических исследований — измеримо, безопасно и без магического мышления. </p>
                </div>
            </div>
        </div>

        <div class="row responsive-padding">
             <div class="col-12 col-md-3 mb-5">
                <span class="display-7">
                    С чем я работаю
                </span>
            </div>
            <div class="col-12 col-md-9">
                <div class="ms-3">
                    {% assign services = site.data.services.list %}
                    {% for service in services %}
                        <div class="row align-items-center mb-5">
                            <div class="col-auto d-flex align-items-center">
                                <img 
                                  src="{{ service.url }}"
                                  width="110" height="110"
                                  class="figure-img img-fluid rounded-5 shadow"
                                />
                            </div>
                            <div class="col d-flex align-items-center">
                                <div>
                                    <p class="fw-bold fs-5 mb-1">{{ service.name }}</p>
                                    <p class="fs-6 fw-light">{{ service.description }}</p>
                                </div>
                            </div>
                        </div>
                    {% endfor %}
                </div>
            </div>
        </div>


        <div class="row responsive-padding">
            <div class="col-12 col-md-3 mb-5">
                <span class="display-7">
                    Как проходит работа
                </span>
            </div>
            <div class="col-12 col-md-9">
                <div class="mx-3 fs-5">
                    <p>Онлайн, 1 раз в неделю, продолжительность 55 минут. Между встречами — поддержка и упражнения, чтобы результат закреплялся в реальной жизни.</p>
                </div>
            </div>
        </div>


        <div class="row responsive-padding">
            <div class="col-12 col-md-3 mb-5">
                <span class="display-7">
                    Образование
                </span>
            </div>
            <div class="col-12 col-md-9">
                <div class="mx-3">
                    {% assign educations = site.data.education.list %}
                    {% for education in educations %}
                        <div class="row">
                            <p class="fw-bold fs-5 mb-0">{{ education.name }}</p>
                            <p class="fs-6 fw-light">{{ education.institute }}</p>
                        </div>
                        <hr style="margin: 10px 0">
                    {% endfor %}
                </div>
            </div>
        </div>


        <div class="row responsive-padding">
            <div class="col-12 col-md-3 mb-5">
                <span class="display-7">
                    Отзывы
                </span>
            </div>
            <div class="col-12 col-md-9">
                <div class="ms-3">
                    <div class="video-scroll-wrapper w-100">
                        {% assign feedbacks = site.data.feedbacks.list %}
                        {% for feedback in feedbacks %}

                            <a class="video-card text-decoration-none"
                                data-bs-toggle="modal"
                                data-bs-target="#feedbackModal-{{ forloop.index0 }}"
                                style="cursor:pointer;">
                            
                                <img src="{{ feedback.image }}" class="w-100 rounded-4 shadow" />
                            
                                <p class="mt-2 mb-1 text-black fs-6 fw-light">
                                    {{ feedback.name }}
                                </p>
                            </a>

                            <div class="modal fade" id="feedbackModal-{{ forloop.index0 }}" tabindex="-1" aria-hidden="true">
                                <div class="modal-dialog modal-dialog-centered modal-xl">
                                    <div class="modal-content bg-dark rounded-4">
                                        <div class="modal-body p-1">
                                            <div>
                                                {% include video-block.html item=feedback %}
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        {% endfor %}
                    </div>
                </div>
            </div>
        </div>


        <div class="row responsive-padding">
            <div class="col-12 col-md-3">
                <span class="display-7">
                    Стоимость
                </span>
            </div>
            <div class="col-12 col-md-9">
                <div class="row row-cols-1 row-cols-md-2 g-4 mt-4">
                    {% assign offers = site.data.offers.list %}
                    {% for offer in offers %}
                        <div class="col">
                            <a href="https://t.me/{{ site.data.contacts.telegram }}" target="_blank" class="text-decoration-none">
                                <div class="card card-clean h-100 rounded-4 p-3">
                                    <div class="row text-center">
                                        <div class="mt-3">
                                            <img 
                                              src="{{ offer.pic }}?random={{offer.name}}"
                                              width="150" height="150"
                                              class="figure-img img-fluid rounded-5 shadow"
                                            />
                                        </div>
                                    </div>
                                    <div class="row text-center mt-2">
                                        <span class="fs-4 fw-bold">{{ offer.name }}</span>
                                    </div>
                                    <div class="row text-center mt-2">
                                        <p class="fs-5 fw-light">
                                            {{ offer.description }}
                                        </p>
                                    </div>
                                    <div class="row text-center mt-2 mx-1 text-center">
                                        <div class="offer-price offer-price-color-{{ forloop.index0 }}">
                                            <p class="fs-4 fw-bold mt-3">{{ offer.price }}</p>
                                        </div>
                                    </div>
                                    <div class="row text-center mt-2 mb-4">
                                        {% assign results = offer.results %}
                                        {% for result in results %}
                                            <div class="d-flex align-items-center mt-2">
                                                <svg width="50" height="50" class="me-2 d-block" style="flex-shrink: 0">
                                                    <use xlink:href="#icon-mark"></use>
                                                </svg>
                                            
                                                <span class="fs-5 text-start">{{ result }}</span>
                                            </div>
                                        {% endfor %}
                                    </div>
                                    <div class="row text-center mt-auto mb-3 mx-1">
                                        <span class="btn btn-dark w-100 py-3 fs-5">Записаться</span>
                                    </div>
                                </div>
                            </a>
                        </div>
                    {% endfor %}
                </div>
            </div>
        </div>

        {% include footer.html %}
    </div>
</div>
