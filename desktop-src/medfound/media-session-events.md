---
description: Mediensitzungsereignisse
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: Mediensitzungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffecb3f4e3f4b3a3b30be95fcc45adcb81c1a84dd04ed8cf637bad759512a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724010"
---
# <a name="media-session-events"></a>Mediensitzungsereignisse

Die meisten Vorgänge der Mediensitzung werden asynchron ausgeführt, sodass die Anwendung mithilfe der [**MEDIAMediaEventGenerator-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) der Mediensitzung auf Ereignisse lauschen muss. (Die [**BENUTZEROBERFLÄCHEMEDIASession-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) erbt **DEN VERERBMEDIAEventGenerator.)** Die genaue Abfolge der Ereignisse hängt von Ihrer Anwendung ab, aber die folgenden Ereignisse werden von der Mediensitzung in fast jeder Situation ausgelöst.



| Ereignis                                                                  | Beschreibung                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEEndOfPresentation](meendofpresentation.md)                         | Wird ausgelöst, wenn die Medienquelle die Präsentation abgeschlossen hat. Möglicherweise bewegen sich die Daten zu diesem Zeitpunkt noch durch die Pipeline.                                                                                                     |
| [MEError](meerror.md)                                                 | Wird ausgelöst, wenn während des Streamings ein Fehler auftritt.                                                                                                                                                                                    |
| [MESessionClosed](mesessionclosed.md)                                 | Wird ausgelöst, [**wenn die Close-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) abgeschlossen ist. Dieses Ereignis ist das letzte Ereignis, das die Mediensitzung in die Warteschlange einreiht. Nachdem Sie dieses Ereignis erhalten haben, können Sie alle von Ihnen erstellten Medienquellen herunterfahren. |
| [MESessionEnded](mesessionended.md)                                   | Wird ausgelöst, wenn die Mediensitzung mit der letzten Präsentation beendet wurde.                                                                                                                                                              |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) | Benachrichtigt die Anwendung der Präsentationszeit, wenn die neue Präsentation gestartet wird.                                                                                                                                        |
| [MESessionStarted](mesessionstarted.md)                               | Wird ausgelöst, wenn [**die Start-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) abgeschlossen ist. Sofern kein Fehler aufgetreten ist, werden die Daten an diesem Punkt durch die Pipeline bewegt.                                                                          |
| [MESessionTopologySet](mesessiontopologyset.md)                       | Wird ausgelöst, wenn [**die SetTopology-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) abgeschlossen ist. Sofern kein Fehler auftritt, muss die Anwendung keine Maßnahmen ergreifen.                                                                 |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                 | Wird zu verschiedenen Zeitpunkten ausgelöst, wenn sich der Status einer Topologie ändert.                                                                                                                                                                 |



 

Die [**METHODE FÜR DIE 10-000-000-000-000-Methode (SHUTDOWNMediaSession::Shutdown)**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) gibt kein Ereignis aus. Die **Shutdown-Methode** ist synchron. Nachdem diese Methode zurückgegeben wurde, ist es sicher, den Ereignisrückrufzeiger frei zu geben.

Zusätzlich zu Ereignissen aus der Mediensitzung kann die Anwendung Ereignisse von den Mediensenken in der Topologie empfangen. Dies können benutzerdefinierte Ereignisse sein, die von der Mediensenke definiert werden und beliebige Daten enthalten können. Beispielsweise kann die Senke die Ereignisdaten von den Quelldaten ableiten, die aus einer nicht vertrauenswürdigen externen Quelle stammen können. Eine Anwendung sollte alle Ereignisse ignorieren, die sie nicht erkennt, und beim Verarbeiten von Ereignisdaten vorsichtsacht vorgehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mediensitzung](media-session.md)
</dt> </dl>

 

 



