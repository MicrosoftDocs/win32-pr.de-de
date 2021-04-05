---
title: Abfragen und Festlegen des Tempos
description: Abfragen und Festlegen des Tempos
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- Digital Instrumentation Digital Interface (MIDI), Tempo
- MIDI (Digital Interface Digital Interface), Tempo
- MCI-MIDI Sequencer, Tempo
- MCI_STATUS-Befehl
- Sequenz Tempo
- Lern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714579"
---
# <a name="querying-and-setting-the-tempo"></a>Abfragen und Festlegen des Tempos

Um das Tempo einer Sequenz abzurufen, verwenden Sie den Befehl " [**MCI- \_ Status**](mci-status.md) ", und legen Sie das Element " **dwitem** " der [**MCI- \_ statusparametestruktur \_**](mci-status-parms.md) auf MCI \_ Seq \_ Status \_ Tempo fest. Wenn der **MCI- \_ Status** Befehl erfolgreich ist, enthält der **dwreturn** -Member der **MCI- \_ statusparamegenstruktur \_** das aktuelle Tempo.

Um das Tempo zu ändern, verwenden Sie den Befehl [**MCI \_ set**](mci-set.md) mit der Struktur von [**MCI \_ Seq \_ Set- \_ para**](mci-seq-set-parms.md) Metern, geben das MCI \_ Seq \_ Set \_ temflag an und legen den **dwtempo** -Member der Struktur auf das gewünschte Tempo fest.

Die Art und Weise, wie temdargestellt wird, hängt vom Divisions Typ der Sequenz ab. Wenn der Divisions Typ ppqn ist, wird das Tempo in Beats pro Minute dargestellt. Wenn der Divisions Typ einem der SMPTE-Divisions Typen entspricht, wird das Tempo in Frames pro Sekunde dargestellt. Weitere Informationen zum Bestimmen des Divisions Typs einer Sequenz finden Sie unter [Abrufen des sequenzdivisions Typs](retrieving-the-sequence-division-type.md).

 

 




