---
title: Sequencer-Fehler
description: Sequencer-Fehler
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- Mcierr-Rückgabewerte, Sequencer-Fehler
- Multimedia-Referenz, Sequencer-Fehler
- Referenz für Multimedia-, Sequencer-Fehler
- Media Control Interface (MCI), Sequencer-Fehler
- MCI (Medien Steuerungs Schnittstelle), Sequencer-Fehler
- Referenz für MCI, Sequencer-Fehler
- MCI-Referenz, Sequencer-Fehler
- Media Control Interface (MCI), Fehler
- MCI (Medien Steuerungs Schnittstelle), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- Sequencer-Fehler
- MCI-Sequencer-Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710440"
---
# <a name="sequencer-errors"></a>Sequencer-Fehler

Die folgenden zusätzlichen Rückgabewerte werden für MCI-Sequencer definiert:



| Wert                          | Bedeutung                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| mcierr, nicht \_ \_ \_ kompatibel | Die Zeitformate von "Song Pointer" und "SMPTE" sind Singular. Sie können nicht gleichzeitig verwendet werden.                                                              |
| mcierr/ \_ q- \_ nomidipresent     | Dieses System verfügt über keine installierten MIDI-Geräte. Verwenden Sie die Option Drivers in der Systemsteuerung, um einen MIDI-Treiber zu installieren.                                       |
| mcierr- \_ \_ Port- \_ InUse       | Der angegebene MIDI-Port wird bereits verwendet. Warten Sie, bis der Vorgang kostenlos ist. versuchen Sie es dann erneut.                                                                       |
| mcierr/ \_ q- \_ Port \_ mapnodevice | Das aktuelle Installationsprogramm für das MIDI-Mapper bezieht sich auf ein auf dem System nicht installiertes MIDI-Gerät. Verwenden Sie den System Steuerungs-Mapper in der Systemsteuerung, um das Setup zu bearbeiten. |
| Fehler beim mcierr- \_ /q- \_ Port. \_   | Fehler beim angegebenen Port.                                                                                                                   |
| mcierr- \_ \_ Port ist \_ nicht vorhanden. | Das angegebene MIDI-Gerät ist nicht auf dem System installiert. Verwenden Sie die Option Drivers in der Systemsteuerung, um ein MIDI-Gerät zu installieren.                        |
| \_nicht spezifizierter mcierr- \_ Port   | Das System verfügt über keinen aktuellen, von Ihnen angegebenen MIDI-Port.                                                                                                  |
| mcierr-Zeit Geber \_ \_             | Alle Multimediatimer werden von anderen Anwendungen verwendet. Beenden Sie eine dieser Anwendungen. versuchen Sie es dann erneut.                                             |



 

 

 




