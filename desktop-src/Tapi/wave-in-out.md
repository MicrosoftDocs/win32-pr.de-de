---
description: Die Geräteklasse "Wave/in/out" besteht aus vollständigen Duplex Audiogeräten.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: Wave/in/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349940"
---
# <a name="waveinout"></a><span data-ttu-id="419b2-103">Wave/in/out</span><span class="sxs-lookup"><span data-stu-id="419b2-103">wave/in/out</span></span>

<span data-ttu-id="419b2-104">Die Geräteklasse "Wave/in/out" besteht aus vollständigen Duplex Audiogeräten.</span><span class="sxs-lookup"><span data-stu-id="419b2-104">The wave/in/out device class consists of full duplex audio devices.</span></span> <span data-ttu-id="419b2-105">Sie greifen auf diese Geräte mithilfe der Wave-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="419b2-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="419b2-106">Geräte in dieser Klasse sind Zeilen Geräten zugeordnet, die den Typ linemediamode \_ automatedvoice unterstützen, der im **dwmediamodes** -Member der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für das liniengerät angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="419b2-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="419b2-107">Die Funktionen " [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) " und " [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) " füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element " **dwstringformat** " auf den binären Wert "StringFormat" festlegen \_ und zwei zusätzliche Member anhängen:</span><span class="sxs-lookup"><span data-stu-id="419b2-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending two additional members:</span></span>

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

<span data-ttu-id="419b2-108">Die Member " **de viceingeid** " und " **deviceoutid** " sind Bezeichner eines geschlossenen Audiogeräts.</span><span class="sxs-lookup"><span data-stu-id="419b2-108">The **DeviceInId** and **DeviceOutId** members are identifiers of a closed audio device.</span></span> <span data-ttu-id="419b2-109">Sie verwenden diese Bezeichner in einem Aufrufe der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion, um das Gerät für die Ausgabe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="419b2-109">You use these identifiers in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="419b2-110">Sie können das resultierende Geräte Handle verwenden, um digitalisierte Audiodaten an der Zeile oder dem Telefongerät wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="419b2-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="419b2-111">Weitere Informationen zu den Wave-Funktionen finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="419b2-111">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
