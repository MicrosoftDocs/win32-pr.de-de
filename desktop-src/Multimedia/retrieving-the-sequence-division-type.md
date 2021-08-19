---
title: Abrufen des Sequenzdivisionstyps
description: Abrufen des Sequenzdivisionstyps
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- Music Instrument Digital Interface (OPC), Sequenzdivisionstyp
- INSTRUMENTS (Music Instrument Digital Interface), Sequenzdivisionstyp
- MCI-SEQUENZER, Divisionstyp
- MCI_STATUS Befehl
- Sequenzdivisionstyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28bb7e32097b888cdd3dec739eaccfc2a37dfe14060168fb11f0a7ca3d00e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801804"
---
# <a name="retrieving-the-sequence-division-type"></a>Abrufen des Sequenzdivisionstyps

Der *Divisionstyp* einer CAB-Sequenz bestimmt die Zeitspanne zwischen DEN EREIGNISSEN in der Sequenz. Um den Divisionstyp einer Sequenz zu bestimmen, verwenden Sie den [**Befehl MCI \_ STATUS,**](mci-status.md) und legen Sie den **dwItem-Member** der [**MCI \_ STATUS \_ PARMS-Struktur**](mci-status-parms.md) auf MCI \_ SEQ STATUS \_ \_ DIVTYPE fest.

Wenn der **MCI \_ STATUS-Befehl** erfolgreich ist, enthält der **dwReturn-Member** der **MCI \_ STATUS \_ PARMS-Struktur** einen der folgenden Werte, um den Divisionstyp anzugeben.



| Wert                        | Divisionstyp                     |
|------------------------------|-----------------------------------|
| MCI \_ SEQ \_ DIV \_ PPQN          | PPQN (Parts-per-quarter note)     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 24     | SMPTE, 24 Fps (Frames pro Sekunde) |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 25     | SMPTE, 25 FPS                     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 30     | SMPTE, 30 fps                     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP | SMPTE, Dropframe mit 30 FPS          |



 

Sie müssen den Divisionstyp einer Sequenz kennen, um deren Tempo zu ändern oder abzufragen. Sie können den Divisionstyp einer Sequenz nicht mithilfe des MCI-Sequencers ändern.

 

 




