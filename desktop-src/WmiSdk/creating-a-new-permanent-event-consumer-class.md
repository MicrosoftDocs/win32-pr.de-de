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
# <a name="creating-a-new-permanent-event-consumer-class"></a><span data-ttu-id="77417-104">Erstellen einer neuen permanenten ereignisconsumerklasse</span><span class="sxs-lookup"><span data-stu-id="77417-104">Creating a New Permanent Event Consumer Class</span></span>

<span data-ttu-id="77417-105">Einer der ersten Schritte bei der Erstellung eines permanenten Ereignisconsumers ist das Erstellen der WMI-Klasse, die den Ereignisconsumer beschreibt.</span><span class="sxs-lookup"><span data-stu-id="77417-105">One of the first steps in creating a permanent event consumer is to create the WMI class that describes the event consumer.</span></span> <span data-ttu-id="77417-106">Die permanente ereignisconsumerklasse definiert die Parameter der vom physischen Consumer implementierten Aktion.</span><span class="sxs-lookup"><span data-stu-id="77417-106">Specifically, the permanent event consumer class defines the parameters of the action implemented by the physical consumer.</span></span>

<span data-ttu-id="77417-107">Im folgenden Verfahren wird beschrieben, wie eine permanente ereignisconsumerklasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="77417-107">The following procedure describes how to create a permanent event consumer class.</span></span>

<span data-ttu-id="77417-108">**So erstellen Sie eine permanente ereignisconsumerklasse**</span><span class="sxs-lookup"><span data-stu-id="77417-108">**To create a permanent event consumer class**</span></span>

1.  <span data-ttu-id="77417-109">Leiten Sie eine Klasse von der [**\_ \_ eventconsumer**](--eventconsumer.md) -System Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="77417-109">Derive a class from the [**\_\_EventConsumer**](--eventconsumer.md) system class.</span></span>
2.  <span data-ttu-id="77417-110">Implementieren Sie alle Parameter, die für die Verarbeitung einer Ereignis Benachrichtigung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="77417-110">Implement any parameters necessary to process an event notification.</span></span>

<span data-ttu-id="77417-111">Das folgende Beispiel zeigt die Syntax, die zum Erstellen der smtpconsumerevent-Klasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="77417-111">The following example shows the syntax used to create the SMTPConsumerEvent class.</span></span> <span data-ttu-id="77417-112">Dies können Sie als Beispiel für die Erstellung der neuen Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="77417-112">You can use this as an example for creating your new class.</span></span> <span data-ttu-id="77417-113">Die Klasse [**smtpeer-Consumer**](smtpeventconsumer.md) sendet eine e-Mail-Nachricht mit Simple Mail Transfer Protocol (SMTP), wenn ein Ereignis an Sie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="77417-113">The [**SMTPEventConsumer**](smtpeventconsumer.md) class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="77417-114">Diese Klasse ist in "smtpcons. mof" definiert.</span><span class="sxs-lookup"><span data-stu-id="77417-114">This class is defined in smtpcons.mof.</span></span>

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

<span data-ttu-id="77417-115">Sie sollten in der Lage sein, Instanzen ihrer permanenten ereignisconsumerklasse zu erstellen, um eine oder mehrere Methoden zum Senden von Ereignissen an Ihren physischen Consumer zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="77417-115">You should be able to create instances of your permanent event consumer class to describe one or more ways to send events to your physical consumer.</span></span> <span data-ttu-id="77417-116">Weitere Informationen finden Sie unter [Erstellen eines logischen](creating-a-logical-consumer.md)Consumers.</span><span class="sxs-lookup"><span data-stu-id="77417-116">For more information, see [Creating a Logical Consumer](creating-a-logical-consumer.md).</span></span>

 

 



