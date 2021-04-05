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
# <a name="querying-and-setting-the-tempo"></a><span data-ttu-id="82d6d-109">Abfragen und Festlegen des Tempos</span><span class="sxs-lookup"><span data-stu-id="82d6d-109">Querying and Setting the Tempo</span></span>

<span data-ttu-id="82d6d-110">Um das Tempo einer Sequenz abzurufen, verwenden Sie den Befehl " [**MCI- \_ Status**](mci-status.md) ", und legen Sie das Element " **dwitem** " der [**MCI- \_ statusparametestruktur \_**](mci-status-parms.md) auf MCI \_ Seq \_ Status \_ Tempo fest.</span><span class="sxs-lookup"><span data-stu-id="82d6d-110">To retrieve the tempo of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_TEMPO.</span></span> <span data-ttu-id="82d6d-111">Wenn der **MCI- \_ Status** Befehl erfolgreich ist, enthält der **dwreturn** -Member der **MCI- \_ statusparamegenstruktur \_** das aktuelle Tempo.</span><span class="sxs-lookup"><span data-stu-id="82d6d-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure contains the current tempo.</span></span>

<span data-ttu-id="82d6d-112">Um das Tempo zu ändern, verwenden Sie den Befehl [**MCI \_ set**](mci-set.md) mit der Struktur von [**MCI \_ Seq \_ Set- \_ para**](mci-seq-set-parms.md) Metern, geben das MCI \_ Seq \_ Set \_ temflag an und legen den **dwtempo** -Member der Struktur auf das gewünschte Tempo fest.</span><span class="sxs-lookup"><span data-stu-id="82d6d-112">To change tempo, use the [**MCI\_SET**](mci-set.md) command with the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, specifying the MCI\_SEQ\_SET\_TEMPO flag and setting the **dwTempo** member of the structure to the desired tempo.</span></span>

<span data-ttu-id="82d6d-113">Die Art und Weise, wie temdargestellt wird, hängt vom Divisions Typ der Sequenz ab.</span><span class="sxs-lookup"><span data-stu-id="82d6d-113">The way tempo is represented depends on the division type of the sequence.</span></span> <span data-ttu-id="82d6d-114">Wenn der Divisions Typ ppqn ist, wird das Tempo in Beats pro Minute dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d6d-114">If the division type is PPQN, the tempo is represented in beats per minute.</span></span> <span data-ttu-id="82d6d-115">Wenn der Divisions Typ einem der SMPTE-Divisions Typen entspricht, wird das Tempo in Frames pro Sekunde dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d6d-115">If the division type is one of the SMPTE division types, the tempo is represented in frames per second.</span></span> <span data-ttu-id="82d6d-116">Weitere Informationen zum Bestimmen des Divisions Typs einer Sequenz finden Sie unter [Abrufen des sequenzdivisions Typs](retrieving-the-sequence-division-type.md).</span><span class="sxs-lookup"><span data-stu-id="82d6d-116">For information about determining the division type of a sequence, see [Retrieving the Sequence Division Type](retrieving-the-sequence-division-type.md).</span></span>

 

 




