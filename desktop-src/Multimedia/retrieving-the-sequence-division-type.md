---
title: Abrufen des Sequenz Divisions Typs
description: Abrufen des Sequenz Divisions Typs
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- Digital Instrumentation Digital Interface (MIDI), Sequence Division Type
- MIDI (Digital Interface Digital Interface), Sequence Division Type
- MCI-Konfigurations-Sequencer, Divisions Typ
- MCI_STATUS-Befehl
- Typ der Sequenz Division
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6586a33fe4a5225fdcdca21e413104388d5831d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947666"
---
# <a name="retrieving-the-sequence-division-type"></a>Abrufen des Sequenz Divisions Typs

Der *Divisions Typ* einer MIDI-Sequenz bestimmt die Zeitspanne zwischen den MIDI-Ereignissen in der Sequenz. Verwenden Sie zum Bestimmen des Divisions Typs einer Sequenz den Befehl " [**MCI- \_ Status**](mci-status.md) ", und legen Sie das Element " **dwitem** " der [**MCI- \_ \_ statusparameterstruktur**](mci-status-parms.md) auf den MCI \_ SEQ-Status " \_ \_ divtype" fest.

Wenn der **MCI- \_ Status** Befehl erfolgreich ist, enthält der **dwreturn** -Member der **MCI- \_ statusparameterstruktur \_** einen der folgenden Werte, um den Divisions Typ anzugeben.



| Wert                        | Divisions Typ                     |
|------------------------------|-----------------------------------|
| MCI \ \_ \_ div \_ ppqn          | Ppqn (Teile pro Quartal Hinweis)     |
| MCI \ \_ \_ div \_ SMPTE \_ 24     | SMPTE, 24 fps (Frames pro Sekunde) |
| MCI Server \_ \_ div \_ SMPTE \_ 25     | SMPTE, 25 fps                     |
| MCI Server \_ \_ div \_ SMPTE \_ 30     | SMPTE, 30 fps                     |
| MCI-Server \ \_ \_ div \_ SMPTE \_ 30drop | SMPTE, 30-fps-Ablage Rahmen          |



 

Sie müssen den Divisions Typ einer Sequenz kennen, der geändert werden soll, oder sein Tempo Abfragen. Der Divisions Typ einer Sequenz kann nicht mithilfe des MCI-Sequencers geändert werden.

 

 




