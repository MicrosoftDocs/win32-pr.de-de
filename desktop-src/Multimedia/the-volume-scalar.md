---
title: Volumeskalar
description: Volumeskalar
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- Digital Instrumentation Digital Interface (MIDI), Volume skalare
- MIDI (Digital Instrumentation Digital Interface), volumeskalar
- MIDI-Mapper, volumeskalar
- volumeskalar
- MIDI-Mapper, Anpassen von Ausgabe Ebenen
- Anpassen von Ausgabe Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39566a10ca909030b60ff197f009b6afe05ce51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037621"
---
# <a name="the-volume-scalar"></a><span data-ttu-id="ae13c-109">Volumeskalar</span><span class="sxs-lookup"><span data-stu-id="ae13c-109">The Volume Scalar</span></span>

<span data-ttu-id="ae13c-110">Der Skalarwert des Volumes besteht darin, Anpassungen zwischen den relativen Ausgabe Ebenen verschiedener Patches in einem Synthesizer zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="ae13c-110">The purpose of the volume scalar is to allow adjustments between the relative output levels of different patches on a synthesizer.</span></span> <span data-ttu-id="ae13c-111">Wenn z. b. der Bass-Patch in einem Synthesizer im Vergleich zum Klavier Patch zu hoch ist, können Sie die Setup Zuordnung ändern, um das Bass Volume nach unten oder das Klavier Volume zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="ae13c-111">For example, if the bass patch on a synthesizer is too loud compared with its piano patch, you can change the setup map to scale the bass volume down or the piano volume up.</span></span>

<span data-ttu-id="ae13c-112">Der volumeskalar gibt einen Prozentwert an, mit dem alle Nachrichten des MIDI-Haupt volumecontrollers geändert werden, die einer zugeordneten Programm Änderungs Nachricht folgen.</span><span class="sxs-lookup"><span data-stu-id="ae13c-112">The volume scalar specifies a percentage value for changing all MIDI main-volume controller messages that follow an associated program-change message.</span></span> <span data-ttu-id="ae13c-113">Wenn der skalare volumewert beispielsweise 50% beträgt, ändert der MIDI-Mapper die Nachrichten des MIDI-Haupt volumecontrollers, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ae13c-113">For example, if the volume scalar value is 50%, the MIDI Mapper modifies MIDI main-volume controller messages as shown in the following illustration.</span></span>

![Bild von MIDI-Mapper](images/mmap-a04.gif)

 

 




