---
description: In der folgenden Tabelle sind die Klassen für vorinstallierte permanente WMI-Consumer aufgeführt.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Standard-Consumerklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f89463a459adb3dd800f77564002366c7500a2abbaa6010444ba7890802d5a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315277"
---
# <a name="standard-consumer-classes"></a>Standard-Consumerklassen

In der folgenden Tabelle sind die Klassen für vorinstallierte permanente WMI-Consumer aufgeführt. Sie können Instanzen dieser Klassen erstellen, um die permanente Consumerklasse bereitzustellen, um den logischen Consumer bereitzustellen, der reagiert, wenn er durch die im Filter angegebenen Ereignisse ausgelöst wird. Verwenden Sie beispielsweise die [**ActiveScriptEventConsumer-Klasse,**](activescripteventconsumer.md) um das Skript zu definieren, das ausgeführt wird, wenn ein angegebenes Ereignis auftritt.

Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern](monitoring-and-responding-to-events-with-standard-consumers.md) und Überwachen von [Ereignissen.](monitoring-events.md)



| Klasse                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md)               | Führt ein vordefiniertes Skript in einer beliebigen Skriptsprache aus, wenn ein Ereignis an das Skript übermittelt wird.<br/> Beispiel: [Ausführen eines Skripts basierend auf einem Ereignis](running-a-script-based-on-an-event.md)<br/>                                         |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)                 | Startet einen beliebigen Prozess im lokalen Systemkontext, wenn ein Ereignis an ihn übermittelt wird.<br/> Beispiel: [Ausführen eines Programms über die Befehlszeile basierend auf einem Ereignis](running-a-program-from-the-command-line-based-on-an-event.md)<br/> |
| [**LogFileEventConsumer**](logfileeventconsumer.md)                         | Schreibt benutzerdefinierte Zeichenfolgen in eine Textdatei, wenn Ereignisse an sie übermittelt werden.<br/> Beispiel: [Schreiben in eine Protokolldatei basierend auf einem Ereignis](writing-to-a-log-file-based-on-an-event.md)<br/>                                                   |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)                   | Protokolliert eine bestimmte Nachricht im Windows Ereignisprotokoll, wenn ein Ereignis an das Ereignis übermittelt wird.<br/> Beispiel: [Protokollierung im NT-Ereignisprotokoll basierend auf einem Ereignis](logging-to-nt-event-log-based-on-an-event.md)<br/>                                          |
| [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md) | Stellt Registrierungsdaten bereit, die allen Instanzen der [**ActiveScriptEventConsumer-Klasse**](activescripteventconsumer.md) gemeinsam sind.<br/>                                                                                                            |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                               | Sendet bei jeder Zustellung eines Ereignisses eine E-Mail-Nachricht mitHILFE von SMTP.<br/> Beispiel: [Senden von E-Mails basierend auf einem Ereignis](sending-e-mail-based-on-an-event.md)<br/>                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von Ereignissen](monitoring-events.md)
</dt> <dt>

[Empfangen von Ereignissen zu jedem Zeitpunkt](receiving-events-at-all-times.md)
</dt> <dt>

[Ausführen eines Skripts basierend auf einem Ereignis](running-a-script-based-on-an-event.md)
</dt> <dt>

[Senden von E-Mails basierend auf einem Ereignis](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




