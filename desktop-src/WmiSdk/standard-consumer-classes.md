---
description: In der folgenden Tabelle werden die Klassen für vorinstallierte, permanente WMI-Consumer aufgeführt.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Standard Consumer-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a5033077f3dabf90d3e935b2dfec9fad892f630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218487"
---
# <a name="standard-consumer-classes"></a><span data-ttu-id="2ec23-103">Standard Consumer-Klassen</span><span class="sxs-lookup"><span data-stu-id="2ec23-103">Standard Consumer Classes</span></span>

<span data-ttu-id="2ec23-104">In der folgenden Tabelle werden die Klassen für vorinstallierte, permanente WMI-Consumer aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ec23-104">The following table lists the classes for WMI preinstalled permanent consumers.</span></span> <span data-ttu-id="2ec23-105">Sie können Instanzen dieser Klassen erstellen, um die permanente Consumerklasse bereitzustellen, die den logischen Consumer bereitstellt, der antwortet, wenn Sie durch die im Filter angegebenen Ereignisse ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="2ec23-105">You can create instances of these classes to provide the permanent consumer class to supply the logical consumer that responds when triggered by the events specified in the filter.</span></span> <span data-ttu-id="2ec23-106">Verwenden Sie z. b. die [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse, um das Skript zu definieren, das ausgeführt wird, wenn ein bestimmtes Ereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="2ec23-106">For example, use the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to define the script that executes when a specified event occurs.</span></span>

<span data-ttu-id="2ec23-107">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standardconsumern](monitoring-and-responding-to-events-with-standard-consumers.md) und [Überwachungs Ereignissen](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="2ec23-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md) and [Monitoring Events](monitoring-events.md).</span></span>



| <span data-ttu-id="2ec23-108">Klasse</span><span class="sxs-lookup"><span data-stu-id="2ec23-108">Class</span></span>                                                                        | <span data-ttu-id="2ec23-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ec23-109">Description</span></span>                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ec23-110">**Activescripteventconsumer**</span><span class="sxs-lookup"><span data-stu-id="2ec23-110">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md)               | <span data-ttu-id="2ec23-111">Führt ein vordefiniertes Skript in einer beliebigen Skriptsprache aus, wenn ein Ereignis zugestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2ec23-111">Executes a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span><br/> <span data-ttu-id="2ec23-112">Beispiel: [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="2ec23-112">Example: [Running a Script Based on an Event](running-a-script-based-on-an-event.md)</span></span><br/>                                         |
| [<span data-ttu-id="2ec23-113">**Commandlineeventconsumer**</span><span class="sxs-lookup"><span data-stu-id="2ec23-113">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)                 | <span data-ttu-id="2ec23-114">Hiermit wird ein beliebiger Prozess im Kontext des lokalen Systems gestartet, wenn ein Ereignis an ihn übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="2ec23-114">Launches an arbitrary process in the local system context when an event is delivered to it.</span></span><br/> <span data-ttu-id="2ec23-115">Beispiel: [Ausführen eines Programms von der Befehlszeile auf Grundlage eines Ereignisses](running-a-program-from-the-command-line-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="2ec23-115">Example: [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md)</span></span><br/> |
| [<span data-ttu-id="2ec23-116">**Logfileeventconsumer**</span><span class="sxs-lookup"><span data-stu-id="2ec23-116">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)                         | <span data-ttu-id="2ec23-117">Schreibt angepasste Zeichen folgen in eine Text Protokolldatei, wenn Ereignisse an Sie übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="2ec23-117">Writes customized strings to a text log file when events are delivered to it.</span></span><br/> <span data-ttu-id="2ec23-118">Beispiel: [Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses](writing-to-a-log-file-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="2ec23-118">Example: [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md)</span></span><br/>                                                   |
| [<span data-ttu-id="2ec23-119">**Nteventlogeventconsumer**</span><span class="sxs-lookup"><span data-stu-id="2ec23-119">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)                   | <span data-ttu-id="2ec23-120">Protokolliert eine bestimmte Meldung im Windows-Ereignisprotokoll, wenn ein Ereignis zugestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2ec23-120">Logs a specific message to the Windows event log when an event is delivered to it.</span></span><br/> <span data-ttu-id="2ec23-121">Beispiel: [Protokollierung in NT-Ereignisprotokoll basierend auf einem Ereignis](logging-to-nt-event-log-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="2ec23-121">Example: [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md)</span></span><br/>                                          |
| [<span data-ttu-id="2ec23-122">**Scriptingstandardconsumersetting**</span><span class="sxs-lookup"><span data-stu-id="2ec23-122">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md) | <span data-ttu-id="2ec23-123">Stellt Registrierungsdaten bereit, die allen Instanzen der [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="2ec23-123">Provides registration data common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="2ec23-124">**Smtpeer-Consumer**</span><span class="sxs-lookup"><span data-stu-id="2ec23-124">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                               | <span data-ttu-id="2ec23-125">Sendet immer dann eine e-Mail-Nachricht mit SMTP, wenn ein Ereignis zugestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2ec23-125">Sends an email message using SMTP each time an event is delivered to it.</span></span><br/> <span data-ttu-id="2ec23-126">Beispiel: [Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="2ec23-126">Example: [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md)</span></span><br/>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="2ec23-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ec23-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ec23-128">Überwachen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="2ec23-128">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="2ec23-129">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="2ec23-129">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="2ec23-130">Ausführen eines Skripts auf der Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2ec23-130">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="2ec23-131">Senden von e-Mails auf der Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2ec23-131">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




