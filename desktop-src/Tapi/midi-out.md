---
description: Die Geräteklasse "MIDI/Out" besteht aus den für die Ausgabe verwendeten MIDI-Sequencern. Sie greifen auf diese Geräte mithilfe der Funktionen von MIDI zu, die im Platform Software Development Kit (SDK) beschrieben werden.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: "\"MIDI/Out\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214369"
---
# <a name="midiout"></a><span data-ttu-id="91f1c-104">"MIDI/Out"</span><span class="sxs-lookup"><span data-stu-id="91f1c-104">midi/out</span></span>

<span data-ttu-id="91f1c-105">Die Geräteklasse "MIDI/Out" besteht aus den für die Ausgabe verwendeten MIDI-Sequencern.</span><span class="sxs-lookup"><span data-stu-id="91f1c-105">The midi/out device class consists of MIDI sequencers that are used for output.</span></span> <span data-ttu-id="91f1c-106">Sie greifen auf diese Geräte mithilfe der Funktionen von MIDI zu, die im Platform Software Development Kit (SDK) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="91f1c-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="91f1c-107">Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element **dwstringformat** auf den Binär Wert StringFormat festlegen \_ und diesen zusätzlichen Member anhängen:</span><span class="sxs-lookup"><span data-stu-id="91f1c-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="91f1c-108">Der Member " **enviceid** " ist der Bezeichner eines geschlossenen MIDI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="91f1c-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="91f1c-109">Sie verwenden diesen Bezeichner in einem Aufrufe der [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion, um das Gerät für die Ausgabe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="91f1c-109">You use this identifier in a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function to open the device for output.</span></span> <span data-ttu-id="91f1c-110">Sie können das resultierende Geräte Handle verwenden, um die Daten von MIDI an der Zeile oder dem Telefongerät wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="91f1c-110">You can use the resulting device handle to play MIDI data at the line or phone device.</span></span>

<span data-ttu-id="91f1c-111">Weitere Informationen zu den Funktionen von MIDI finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="91f1c-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
