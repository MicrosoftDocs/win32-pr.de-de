---
description: Medien Sitzungs Ereignisse
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: Medien Sitzungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e128fc5e11f70fe47d02356ce44629b98bfdfe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361766"
---
# <a name="media-session-events"></a>Medien Sitzungs Ereignisse

Die meisten Vorgänge der Medien Sitzung werden asynchron ausgeführt, sodass die Anwendung auf Ereignisse über die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle der Medien Sitzung lauschen muss. (Die [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstelle erbt **imfmediaeventgenerator**.) Die genaue Reihenfolge der Ereignisse hängt von Ihrer Anwendung ab, aber die folgenden Ereignisse werden von der Medien Sitzung in nahezu jeder Situation ausgelöst.



| Ereignis                                                                  | BESCHREIBUNG                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Meendof Presentation](meendofpresentation.md)                         | Wird ausgelöst, wenn die Medienquelle die Präsentation abgeschlossen hat. Daten können zu diesem Zeitpunkt weiterhin durch die Pipeline verschoben werden.                                                                                                     |
| [Meerror](meerror.md)                                                 | Wird ausgelöst, wenn beim Streaming ein Fehler auftritt.                                                                                                                                                                                    |
| [Mesessionclosed](mesessionclosed.md)                                 | Wird ausgelöst, wenn die [**Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) -Methode abgeschlossen wird. Dieses Ereignis ist das letzte Ereignis, das die Warteschlange für Medien Sitzungen hat. Nachdem Sie dieses Ereignis erhalten haben, können Sie die von Ihnen erstellten Medienquellen sicher Herunterfahren. |
| [Mesessionend](mesessionended.md)                                   | Wird ausgelöst, wenn die Medien Sitzung mit der letzten Präsentation abgeschlossen wird.                                                                                                                                                              |
| [Mesessionnotifypresentationtime](mesessionnotifypresentationtime.md) | Benachrichtigt die Anwendung über die Präsentationszeit, wann die neue Präsentation gestartet wird.                                                                                                                                        |
| [Mesessionstarted](mesessionstarted.md)                               | Wird ausgelöst, wenn die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) Methode abgeschlossen wird. Wenn ein Fehler aufgetreten ist, verschieben sich die Daten an diesem Punkt durch die Pipeline.                                                                          |
| [Mesessiontopologyset](mesessiontopologyset.md)                       | Wird ausgelöst, wenn die [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode abgeschlossen wird. Die Anwendung muss keine Aktion ausführen, es sei denn, es tritt ein Fehler auf.                                                                 |
| [Mesessiontopologystatus](mesessiontopologystatus.md)                 | Wird zu verschiedenen Zeitpunkten ausgelöst, wenn der Status einer Topologie geändert wird.                                                                                                                                                                 |



 

Die [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) -Methode gibt kein Ereignis aus. Die **Shutdown** -Methode ist synchron. Nachdem diese Methode zurückgegeben wurde, ist es sicher, den Ereignis Rückruf Zeiger freizugeben.

Zusätzlich zu den Ereignissen aus der Medien Sitzung empfängt die Anwendung möglicherweise Ereignisse von den Medien senken in der Topologie. Hierbei kann es sich um benutzerdefinierte Ereignisse handeln, die von der Medien Senke definiert werden. diese kann beliebige Daten enthalten Die Senke könnte z. b. die Ereignisdaten aus den Quelldaten ableiten, die aus einer nicht vertrauenswürdigen externen Quelle stammen können. Eine Anwendung sollte alle Ereignisse ignorieren, die Sie nicht erkennt, und beim Auswerten von Ereignisdaten Vorsicht walten lassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> </dl>

 

 



