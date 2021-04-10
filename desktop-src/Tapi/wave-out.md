---
description: Die Geräteklasse "Wave/Out" besteht aus Audiogeräten für die Ausgabe von Wave-Audiodaten auf niedriger Ebene.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: Wave/Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975a3308b6f0b29e130ad07534494e1cb1d991a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869187"
---
# <a name="waveout"></a><span data-ttu-id="ef592-103">Wave/Out</span><span class="sxs-lookup"><span data-stu-id="ef592-103">wave/out</span></span>

<span data-ttu-id="ef592-104">Die Geräteklasse "Wave/Out" besteht aus Audiogeräten für die Ausgabe von Wave-Audiodaten auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="ef592-104">The wave/out device class consists of audio devices for low-level wave audio output.</span></span> <span data-ttu-id="ef592-105">Sie greifen auf diese Geräte mithilfe der Wave-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ef592-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="ef592-106">Geräte in dieser Klasse sind Zeilen Geräten zugeordnet, die den Typ linemediamode \_ automatedvoice unterstützen, der im **dwmediamodes** -Member der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für das liniengerät angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef592-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="ef592-107">Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element **dwstringformat** auf den Binär Wert StringFormat festlegen \_ und diesen zusätzlichen Member anhängen:</span><span class="sxs-lookup"><span data-stu-id="ef592-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="ef592-108">Der Member " **enviceid** " ist der Bezeichner eines geschlossenen Audiogeräts.</span><span class="sxs-lookup"><span data-stu-id="ef592-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="ef592-109">Sie verwenden diesen Bezeichner in einem Aufrufe der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion, um das Gerät für die Ausgabe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ef592-109">You use this identifier in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="ef592-110">Sie können das resultierende Geräte Handle verwenden, um digitalisierte Audiodaten an der Zeile oder dem Telefongerät wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="ef592-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="ef592-111">Obwohl eine "Wave"-Geräteklasse auch für Wellen Audiogeräte auf niedriger Ebene vorhanden ist, sollten Sie immer die Wave/Out-Geräteklasse für eine Wellen Ausgabe auf niedriger Ebene verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef592-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/out device class for low-level wave output.</span></span>

<span data-ttu-id="ef592-112">Weitere Informationen zu den Wave-Funktionen finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ef592-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
