---
title: Sequencer-Fehler
description: Sequencer-Fehler
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- MCIERR-Rückgabewerte, Sequencerfehler
- Multimediareferenz, Sequencerfehler
- Referenz zu Multimediafehlern, Sequencerfehlern
- Media Control Interface (MCI), Sequencerfehler
- MCI (Media Control Interface), Sequencerfehler
- Referenz zu MCI,Sequencer-Fehlern
- MCI-Referenz, Sequencerfehler
- Media Control Interface (MCI), Fehler
- MCI (Media Control Interface), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- Sequencerfehler
- MCI-Sequencerfehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea7e5b38d5541041e8ec065c8cad31f9d31ed1bfa9f22562aba1bf1ff04039b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371128"
---
# <a name="sequencer-errors"></a>Sequencer-Fehler

Die folgenden zusätzlichen Rückgabewerte werden für MCI-Sequencer definiert:



| Wert                          | Bedeutung                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ SEQ \_ DIV \_ INKOMPATIBEL | Die Zeitformate von "song pointer" und SMPTE sind singular. Sie können sie nicht zusammen verwenden.                                                              |
| MCIERR \_ SEQ \_ NOMIDIPRESENT     | Dieses System verfügt über keine installierten SYSTEMS-Geräte. Verwenden Sie die Treiberoption aus dem Systemsteuerung, um einen GIGABYTE-Treiber zu installieren.                                       |
| MCIERR \_ SEQ \_ PORT \_ INUSE       | Der angegebene PORTS wird bereits verwendet. Warten Sie, bis es kostenlos ist. Versuchen Sie es dann erneut.                                                                       |
| MCIERR \_ SEQ \_ PORT \_ MAPNODEVICE | Das aktuelle SETUP des MAPPER-Mappers bezieht sich auf ein SYSTEMS-Gerät, das nicht auf dem System installiert ist. Verwenden Sie den MAPPer VON DER SYSTEMSTEUERUNG, um das Setup zu bearbeiten. |
| MCIERR \_ SEQ \_ PORT \_ MISCERROR   | Fehler beim angegebenen Port.                                                                                                                   |
| MCIERR \_ SEQ \_ PORT \_ NONEXISTENT | Das angegebene SYSTEMS-Gerät ist nicht auf dem System installiert. Verwenden Sie die Treiberoption aus dem Systemsteuerung, um ein GERÄT zu installieren.                        |
| MCIERR \_ SEQ \_ PORTUNSPECIFIED   | Für das System ist kein aktueller PORTS angegeben.                                                                                                  |
| MCIERR \_ SEQ \_ TIMER             | Alle Multimediatimer werden von anderen Anwendungen verwendet. Beenden Sie eine dieser Anwendungen. Versuchen Sie es dann erneut.                                             |



 

 

 




