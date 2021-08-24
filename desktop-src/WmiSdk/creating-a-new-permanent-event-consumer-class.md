---
description: Einer der ersten Schritte beim Erstellen eines permanenten Ereignisverbraucher ist das Erstellen der WMI-Klasse, die den Ereignisverbraucher beschreibt. Insbesondere definiert die permanente Ereignisverbraucherklasse die Parameter der Aktion, die vom physischen Consumer implementiert wird.
ms.assetid: a5b6d0b9-8df1-47e3-bb3b-cc69db6d9c0e
ms.tgt_platform: multiple
title: Erstellen einer neuen permanenten Ereignisverbraucherklasse
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f86f9e8ea4339eb76bdc77087780fcfa9be09f47c92a154c5f89109d90337b41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464280"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a>Erstellen einer neuen permanenten Ereignisverbraucherklasse

Einer der ersten Schritte beim Erstellen eines permanenten Ereignisverbraucher ist das Erstellen der WMI-Klasse, die den Ereignisverbraucher beschreibt. Insbesondere definiert die permanente Ereignisverbraucherklasse die Parameter der Aktion, die vom physischen Consumer implementiert wird.

Im folgenden Verfahren wird beschrieben, wie eine permanente Ereignisverbraucherklasse erstellt wird.

**So erstellen Sie eine permanente Ereignisverbraucherklasse**

1.  Leiten Sie eine Klasse von der [**\_ \_ EventConsumer-Systemklasse**](--eventconsumer.md) ab.
2.  Implementieren Sie alle Parameter, die zum Verarbeiten einer Ereignisbenachrichtigung erforderlich sind.

Das folgende Beispiel zeigt die Syntax, die zum Erstellen der SMTPConsumerEvent-Klasse verwendet wird. Sie können dies als Beispiel für die Erstellung Ihrer neuen Klasse verwenden. Die [**SMTPEventConsumer-Klasse**](smtpeventconsumer.md) sendet mithilfe von Simple Mail Transfer Protocol (SMTP) jedes Mal eine E-Mail-Nachricht, wenn ein Ereignis an sie übermittelt wird. Diese Klasse wird in smtpcons.mof definiert.

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

Sie sollten Instanzen Ihrer permanenten Ereignisverbraucherklasse erstellen können, um eine oder mehrere Möglichkeiten zum Senden von Ereignissen an Ihren physischen Consumer zu beschreiben. Weitere Informationen finden Sie unter [Erstellen eines logischen Consumers.](creating-a-logical-consumer.md)

 

 



