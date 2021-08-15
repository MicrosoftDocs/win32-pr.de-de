---
title: Empfangen Running-Status Nachrichten
description: Empfangen Running-Status Nachrichten
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- Instrument Digital Interface (KEYBOARD), Ausführungsstatus
- KEYBOARD (Keyboard Instrument Digital Interface), Ausführungsstatus
- Aufzeichnung von audio,running status (AUFZEICHNUNG DES AUDIO-Audios, Ausführungsstatus)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4d782e1e25c718ddd177d1d9baf471d0715d70680b65920052e85d6fffc551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371345"
---
# <a name="receiving-running-status-messages"></a>Empfangen Running-Status Nachrichten

Die  *Standard-FORMAT Files 1.0-Spezifikation* ermöglicht die Verwendung des Ausführungsstatus, wenn eine Nachricht das gleiche Status-Byte wie die vorherige Meldung hat. Wenn der Ausführungsstatus verwendet wird, kann das Status byte nachfolgender Nachrichten weggelassen werden. Alle EINGABE-Eingabegerätetreiber sind erforderlich, um Nachrichten mit dem Ausführungsstatus in vollständige Nachrichten zu erweitern, sodass Sie immer vollständigeBENACHRICHTIGUNG-Nachrichten von einem EINGABEGERÄTE-Treiber erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von TONS-Audio](recording-midi-audio.md)
</dt> </dl>

 

 




