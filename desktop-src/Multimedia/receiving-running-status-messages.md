---
title: Empfangen von Running-Status Nachrichten
description: Empfangen von Running-Status Nachrichten
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- Music Instrument Digital Interface (OPC), Ausführungsstatus
- INSTRUMENTS (Music Instrument Digital Interface),Ausführungsstatus
- Aufzeichnen von AUDIO-AUDIO,Ausführungsstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4d782e1e25c718ddd177d1d9baf471d0715d70680b65920052e85d6fffc551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371345"
---
# <a name="receiving-running-status-messages"></a>Empfangen von Running-Status Nachrichten

Die *STANDARD-SPEZIFIKATION FÜR DIE DATEIEN 1.0* ermöglicht die Verwendung des *Ausführungsstatus,* wenn eine Nachricht das gleiche Status-Byte wie die vorherige Nachricht hat. Wenn der Ausführungsstatus verwendet wird, kann das Status byte der nachfolgenden Nachrichten ausgelassen werden. Alle EINGABEGERÄTEtreiber sind erforderlich, um Nachrichten mit dem Ausführungsstatus in vollständige Nachrichten zu erweitern, sodass Sie immer vollständige MELDUNGEN von einem CAB-Eingabegerätetreiber erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Recording RECORDING Audio (Aufzeichnen von AUDIO)](recording-midi-audio.md)
</dt> </dl>

 

 




