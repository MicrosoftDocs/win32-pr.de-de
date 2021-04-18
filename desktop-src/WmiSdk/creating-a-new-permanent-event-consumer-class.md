---
description: Einer der ersten Schritte bei der Erstellung eines permanenten Ereignisconsumers ist das Erstellen der WMI-Klasse, die den Ereignisconsumer beschreibt. Die permanente ereignisconsumerklasse definiert die Parameter der vom physischen Consumer implementierten Aktion.
ms.assetid: a5b6d0b9-8df1-47e3-bb3b-cc69db6d9c0e
ms.tgt_platform: multiple
title: Erstellen einer neuen permanenten ereignisconsumerklasse
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f8ae8e1e83abcf3b340398d45aefde4c7141e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354630"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a>Erstellen einer neuen permanenten ereignisconsumerklasse

Einer der ersten Schritte bei der Erstellung eines permanenten Ereignisconsumers ist das Erstellen der WMI-Klasse, die den Ereignisconsumer beschreibt. Die permanente ereignisconsumerklasse definiert die Parameter der vom physischen Consumer implementierten Aktion.

Im folgenden Verfahren wird beschrieben, wie eine permanente ereignisconsumerklasse erstellt wird.

**So erstellen Sie eine permanente ereignisconsumerklasse**

1.  Leiten Sie eine Klasse von der [**\_ \_ eventconsumer**](--eventconsumer.md) -System Klasse ab.
2.  Implementieren Sie alle Parameter, die für die Verarbeitung einer Ereignis Benachrichtigung erforderlich sind.

Das folgende Beispiel zeigt die Syntax, die zum Erstellen der smtpconsumerevent-Klasse verwendet wird. Dies können Sie als Beispiel für die Erstellung der neuen Klasse verwenden. Die Klasse [**smtpeer-Consumer**](smtpeventconsumer.md) sendet eine e-Mail-Nachricht mit Simple Mail Transfer Protocol (SMTP), wenn ein Ereignis an Sie übermittelt wird. Diese Klasse ist in "smtpcons. mof" definiert.

``` syntax
class SMTPEventConsumer : __EventConsumer
{
  [key] string Name;
  [not_null] string SMTPServer;
  [Template] string Subject;
  [Template] string FromLine;
  [Template] string ReplyToLine;
  [Template] string Message;
  [Template] string ToLine;
  [Template] string CcLine;
  [Template] string BccLine;
  string HeaderFields[];
};
```

Sie sollten in der Lage sein, Instanzen ihrer permanenten ereignisconsumerklasse zu erstellen, um eine oder mehrere Methoden zum Senden von Ereignissen an Ihren physischen Consumer zu beschreiben. Weitere Informationen finden Sie unter [Erstellen eines logischen](creating-a-logical-consumer.md)Consumers.

 

 



