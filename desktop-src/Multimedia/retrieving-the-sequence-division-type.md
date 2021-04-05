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
# <a name="retrieving-the-sequence-division-type"></a><span data-ttu-id="afb7b-108">Abrufen des Sequenz Divisions Typs</span><span class="sxs-lookup"><span data-stu-id="afb7b-108">Retrieving the Sequence Division Type</span></span>

<span data-ttu-id="afb7b-109">Der *Divisions Typ* einer MIDI-Sequenz bestimmt die Zeitspanne zwischen den MIDI-Ereignissen in der Sequenz.</span><span class="sxs-lookup"><span data-stu-id="afb7b-109">The *division type* of a MIDI sequence determines the amount of time between MIDI events in the sequence.</span></span> <span data-ttu-id="afb7b-110">Verwenden Sie zum Bestimmen des Divisions Typs einer Sequenz den Befehl " [**MCI- \_ Status**](mci-status.md) ", und legen Sie das Element " **dwitem** " der [**MCI- \_ \_ statusparameterstruktur**](mci-status-parms.md) auf den MCI \_ SEQ-Status " \_ \_ divtype" fest.</span><span class="sxs-lookup"><span data-stu-id="afb7b-110">To determine the division type of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_DIVTYPE .</span></span>

<span data-ttu-id="afb7b-111">Wenn der **MCI- \_ Status** Befehl erfolgreich ist, enthält der **dwreturn** -Member der **MCI- \_ statusparameterstruktur \_** einen der folgenden Werte, um den Divisions Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="afb7b-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure will contain one of the following values to indicate the division type.</span></span>



| <span data-ttu-id="afb7b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="afb7b-112">Value</span></span>                        | <span data-ttu-id="afb7b-113">Divisions Typ</span><span class="sxs-lookup"><span data-stu-id="afb7b-113">Division type</span></span>                     |
|------------------------------|-----------------------------------|
| <span data-ttu-id="afb7b-114">MCI \ \_ \_ div \_ ppqn</span><span class="sxs-lookup"><span data-stu-id="afb7b-114">MCI\_SEQ\_DIV\_PPQN</span></span>          | <span data-ttu-id="afb7b-115">Ppqn (Teile pro Quartal Hinweis)</span><span class="sxs-lookup"><span data-stu-id="afb7b-115">PPQN (parts-per-quarter note)</span></span>     |
| <span data-ttu-id="afb7b-116">MCI \ \_ \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="afb7b-116">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>     | <span data-ttu-id="afb7b-117">SMPTE, 24 fps (Frames pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="afb7b-117">SMPTE, 24 fps (frames per second)</span></span> |
| <span data-ttu-id="afb7b-118">MCI Server \_ \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="afb7b-118">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>     | <span data-ttu-id="afb7b-119">SMPTE, 25 fps</span><span class="sxs-lookup"><span data-stu-id="afb7b-119">SMPTE, 25 fps</span></span>                     |
| <span data-ttu-id="afb7b-120">MCI Server \_ \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="afb7b-120">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>     | <span data-ttu-id="afb7b-121">SMPTE, 30 fps</span><span class="sxs-lookup"><span data-stu-id="afb7b-121">SMPTE, 30 fps</span></span>                     |
| <span data-ttu-id="afb7b-122">MCI-Server \ \_ \_ div \_ SMPTE \_ 30drop</span><span class="sxs-lookup"><span data-stu-id="afb7b-122">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span> | <span data-ttu-id="afb7b-123">SMPTE, 30-fps-Ablage Rahmen</span><span class="sxs-lookup"><span data-stu-id="afb7b-123">SMPTE, 30 fps drop frame</span></span>          |



 

<span data-ttu-id="afb7b-124">Sie müssen den Divisions Typ einer Sequenz kennen, der geändert werden soll, oder sein Tempo Abfragen.</span><span class="sxs-lookup"><span data-stu-id="afb7b-124">You must know the division type of a sequence to change or query its tempo.</span></span> <span data-ttu-id="afb7b-125">Der Divisions Typ einer Sequenz kann nicht mithilfe des MCI-Sequencers geändert werden.</span><span class="sxs-lookup"><span data-stu-id="afb7b-125">You cannot change the division type of a sequence by using the MCI sequencer.</span></span>

 

 




