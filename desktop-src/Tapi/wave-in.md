---
description: Die Wave/in-Geräteklasse besteht aus Audiogeräten für eine Wave-Audioeingabe auf niedriger Ebene.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: Wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217750"
---
# <a name="wavein"></a><span data-ttu-id="d64f2-103">Wave/in</span><span class="sxs-lookup"><span data-stu-id="d64f2-103">wave/in</span></span>

<span data-ttu-id="d64f2-104">Die Wave/in-Geräteklasse besteht aus Audiogeräten für eine Wave-Audioeingabe auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="d64f2-104">The wave/in device class consists of audio devices for low-level wave audio input.</span></span> <span data-ttu-id="d64f2-105">Sie greifen auf diese Geräte mithilfe der Wave-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d64f2-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="d64f2-106">Geräte in dieser Klasse sind Zeilen Geräten zugeordnet, die den Typ linemediamode \_ automatedvoice unterstützen, der im **dwmediamodes** -Member der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für das liniengerät angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d64f2-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="d64f2-107">Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element **dwstringformat** auf den Binär Wert StringFormat festlegen \_ und diesen zusätzlichen Member anhängen:</span><span class="sxs-lookup"><span data-stu-id="d64f2-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="d64f2-108">Der Member " **enviceid** " ist der Bezeichner eines geschlossenen Audiogeräts.</span><span class="sxs-lookup"><span data-stu-id="d64f2-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="d64f2-109">Sie verwenden diesen Bezeichner in einem Aufrufe der [**waveinopen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion, um das Gerät für die Eingabe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d64f2-109">You use this identifier in a call to the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open the device for input.</span></span> <span data-ttu-id="d64f2-110">Sie können das resultierende Geräte Handle verwenden, um digitalisierte Audiodaten von der Zeile oder dem Telefongerät aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="d64f2-110">You can use the resulting device handle to record digitized audio data from the line or phone device.</span></span>

<span data-ttu-id="d64f2-111">Obwohl eine "Wave"-Geräteklasse auch für Wellen Audiogeräte auf niedriger Ebene vorhanden ist, sollten Sie immer die Wave/in-Geräteklasse für Wellen Eingaben auf niedriger Ebene verwenden.</span><span class="sxs-lookup"><span data-stu-id="d64f2-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/in device class for low-level wave input.</span></span>

<span data-ttu-id="d64f2-112">Weitere Informationen zu den Wave-Funktionen finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d64f2-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
