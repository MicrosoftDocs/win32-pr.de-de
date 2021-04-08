---
description: Die Klasse "MIDI/in" besteht aus den für die Eingabe verwendeten MIDI-Sequencern. Sie greifen auf diese Geräte mithilfe der Funktionen von MIDI zu, die im Platform Software Development Kit (SDK) beschrieben werden.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749537"
---
# <a name="midiin"></a><span data-ttu-id="0cd3a-104">MIDI/in</span><span class="sxs-lookup"><span data-stu-id="0cd3a-104">midi/in</span></span>

<span data-ttu-id="0cd3a-105">Die Klasse "MIDI/in" besteht aus den für die Eingabe verwendeten MIDI-Sequencern.</span><span class="sxs-lookup"><span data-stu-id="0cd3a-105">The midi/in device class consists of MIDI sequencers that are used for input.</span></span> <span data-ttu-id="0cd3a-106">Sie greifen auf diese Geräte mithilfe der Funktionen von MIDI zu, die im Platform Software Development Kit (SDK) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0cd3a-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="0cd3a-107">Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element **dwstringformat** auf den Binär Wert StringFormat festlegen \_ und diesen zusätzlichen Member anhängen:</span><span class="sxs-lookup"><span data-stu-id="0cd3a-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="0cd3a-108">Der Member " **enviceid** " ist der Bezeichner eines geschlossenen MIDI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="0cd3a-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="0cd3a-109">Sie verwenden diesen Bezeichner in einem aufzurufenden Befehl der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion zum Öffnen des Geräts für die Eingabe.</span><span class="sxs-lookup"><span data-stu-id="0cd3a-109">You use this identifier in a call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function to open the device for input.</span></span> <span data-ttu-id="0cd3a-110">Sie können das resultierende Geräte Handle verwenden, um die Daten von MIDI von der Zeile oder dem Telefongerät aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0cd3a-110">You can use the resulting device handle to record MIDI data from the line or phone device.</span></span>

<span data-ttu-id="0cd3a-111">Weitere Informationen zu den Funktionen von MIDI finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0cd3a-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
