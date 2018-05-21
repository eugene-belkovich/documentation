 1. [Introduction](#intro)
 1. [Components](#components)
 1. [Modules](#modules)
 1. [Event model](#events)
 1. [Usages](#usages)

----------
# <a name="intro"></a> Introduction
 Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

----------
# <a name="components"></a> Components

 - [Widget](#widget)
 - [Service](#service)
 - [Repository](#repository)
 
 ### <a name="widget"></a> Widget
 Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. 
 
 ### <a name="service"></a> Service
  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
  
 ### <a name="repository"></a> Repository
  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

----------
# <a name="modules"></a> Modules

 - [Bus](#bus)
 - [Dom](#dom)
 - [Api](#api)
 - [Template](#template)

 ### <a name="bus"></a> Bus
 Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. 

 ### <a name="dom"></a> Dom
  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
  
 ### <a name="api"></a> Api
  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
  
 ### <a name="template"></a> Template
  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

----------
# <a name="events"></a> Event model

Изменения в приложении проиходит посредством pub/sub (событийной) модели. Есть при типа событий: Event, Document, Command. У каджого типа свое назначение и правило к именованиию.

Event types:

 - [Event](#event)
 - [Document](#document)
 - [Command](#Command)
 
 ### <a name="event"></a> Event
 ##### Naming
 ``'event.<domain>.<verb>'``
 
 Domain - предметная область.
 
 Verb - действие которое будет сделано. Используется глагол в прошедшем времени
 
 Например:
  ``'event.invite.opened'`` - событие означающее что invite был открыт

 
 ##### Target

Используется для измения состояния приложения, например после изменения состояния виджетов или результат выполнения алгоритма. Источник событий никогда не должен ожидать на них какой-либо реакции.
Часто используется после Command, чтобы изменить состояние приложения.

  
 ### <a name="document"></a> Document
 ##### Naming
  ``'document.<domain>.<adjective or noun>'``
  
  Domain - предметная область.
  
  Adjective or noun - используется прилагательное или существительное для констатирования состояния сущности которая передается. действие которое будет сделано. Используется глагол в прошедшем времени
  
  Например:
   ``'document.dialogs.streams`` - событие которое просто передает все streams из dialogs
 
  
  ##### Target
 
Сообщения использующиеся только для передачи состояния системы. 
 
 ### <a name="command"></a> Command
 ##### Naming
 ``'command.<domain>.<verb>'``
 
 Domain - предметная область.
 
 Verb - действие которое нужно сделать. Используется глагол в настоящем времени
 
 Например:
  ``'command.events.send'''`` - событие означающее что events были посланы

 
 ##### Target

Используется для внутрисистемных действий, которые вызваны или слушаются из вне или самой системой. Например получение или посылка данных по api, кодирование параметров запроса.


----------
# <a name="usages"></a> Usages

