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
# <a name="standard-consumer-classes"></a>Standard Consumer-Klassen

In der folgenden Tabelle werden die Klassen für vorinstallierte, permanente WMI-Consumer aufgeführt. Sie können Instanzen dieser Klassen erstellen, um die permanente Consumerklasse bereitzustellen, die den logischen Consumer bereitstellt, der antwortet, wenn Sie durch die im Filter angegebenen Ereignisse ausgelöst wird. Verwenden Sie z. b. die [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse, um das Skript zu definieren, das ausgeführt wird, wenn ein bestimmtes Ereignis eintritt.

Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standardconsumern](monitoring-and-responding-to-events-with-standard-consumers.md) und [Überwachungs Ereignissen](monitoring-events.md).



| Klasse                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Activescripteventconsumer**](activescripteventconsumer.md)               | Führt ein vordefiniertes Skript in einer beliebigen Skriptsprache aus, wenn ein Ereignis zugestellt wird.<br/> Beispiel: [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md)<br/>                                         |
| [**Commandlineeventconsumer**](commandlineeventconsumer.md)                 | Hiermit wird ein beliebiger Prozess im Kontext des lokalen Systems gestartet, wenn ein Ereignis an ihn übermittelt wird.<br/> Beispiel: [Ausführen eines Programms von der Befehlszeile auf Grundlage eines Ereignisses](running-a-program-from-the-command-line-based-on-an-event.md)<br/> |
| [**Logfileeventconsumer**](logfileeventconsumer.md)                         | Schreibt angepasste Zeichen folgen in eine Text Protokolldatei, wenn Ereignisse an Sie übermittelt werden.<br/> Beispiel: [Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses](writing-to-a-log-file-based-on-an-event.md)<br/>                                                   |
| [**Nteventlogeventconsumer**](nteventlogeventconsumer.md)                   | Protokolliert eine bestimmte Meldung im Windows-Ereignisprotokoll, wenn ein Ereignis zugestellt wird.<br/> Beispiel: [Protokollierung in NT-Ereignisprotokoll basierend auf einem Ereignis](logging-to-nt-event-log-based-on-an-event.md)<br/>                                          |
| [**Scriptingstandardconsumersetting**](scriptingstandardconsumersetting.md) | Stellt Registrierungsdaten bereit, die allen Instanzen der [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse gemeinsam sind.<br/>                                                                                                            |
| [**Smtpeer-Consumer**](smtpeventconsumer.md)                               | Sendet immer dann eine e-Mail-Nachricht mit SMTP, wenn ein Ereignis zugestellt wird.<br/> Beispiel: [Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md)<br/>                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von Ereignissen](monitoring-events.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> <dt>

[Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md)
</dt> <dt>

[Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




