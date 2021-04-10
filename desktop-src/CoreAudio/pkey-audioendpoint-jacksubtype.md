---
description: Die Eigenschaft "pkey \_ audioendpoint \_ jacksubtype" enthält eine Ausgabe Kategorie-GUID für ein audioendpunktgerät.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127437"
---
# <a name="pkey_audioendpoint_jacksubtype"></a><span data-ttu-id="1566d-103">Pkey- \_ audioendpoint-" \_ jacksubtype"</span><span class="sxs-lookup"><span data-stu-id="1566d-103">PKEY\_AudioEndpoint\_JackSubType</span></span>

<span data-ttu-id="1566d-104">Die Eigenschaft " **pkey \_ audioendpoint \_ jacksubtype** " enthält eine Ausgabe Kategorie-GUID für ein audioendpunktgerät.</span><span class="sxs-lookup"><span data-stu-id="1566d-104">The **PKEY\_AudioEndpoint\_JackSubType** property contains an output category GUID for an audio endpoint device.</span></span> <span data-ttu-id="1566d-105">Die Header Datei "ksmedia. h" definiert die GUIDs. jeder GUID gibt den Verbindungstyp an.</span><span class="sxs-lookup"><span data-stu-id="1566d-105">The header file Ksmedia.h defines the GUIDs; each GUID specifies the type of connection.</span></span> <span data-ttu-id="1566d-106">Diese GUIDs verfügen auch über zugehörige Pin-Kategorien.</span><span class="sxs-lookup"><span data-stu-id="1566d-106">These GUIDs also have associated pin categories.</span></span> <span data-ttu-id="1566d-107">Die Header Datei "ksmedia. h" definiert z. b. die GUID **ksnodetype \_ DisplayPort- \_ Schnittstelle** für einen anzeigeport, der eine Verbindung mit der von der GUID **Pinname \_ DisplayPort \_ out** definierten KS-Pin herstellt.</span><span class="sxs-lookup"><span data-stu-id="1566d-107">For example, header file Ksmedia.h defines the GUID **KSNODETYPE\_DISPLAYPORT\_INTERFACE** for a display port that connects with the KS pin defined by the GUID **PINNAME\_DISPLAYPORT\_OUT**.</span></span>

<span data-ttu-id="1566d-108">Weitere Informationen finden Sie in der Beschreibung der Eigenschaften der PIN-Kategorie in der Windows-DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="1566d-108">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="1566d-109">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf **VT \_ LPWSTR** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1566d-109">The **vt** member of the **PROPVARIANT** structure is set to **VT\_LPWSTR**.</span></span>

<span data-ttu-id="1566d-110">Der **pwszval** -Member der **PROPVARIANT** -Struktur verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die eine Kategorie-GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="1566d-110">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="1566d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1566d-111">Requirements</span></span>



| <span data-ttu-id="1566d-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1566d-112">Requirement</span></span> | <span data-ttu-id="1566d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1566d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1566d-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1566d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1566d-115">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1566d-115">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1566d-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1566d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1566d-117">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1566d-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1566d-118">Header</span><span class="sxs-lookup"><span data-stu-id="1566d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1566d-119"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1566d-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1566d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1566d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1566d-121">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="1566d-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="1566d-122">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="1566d-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




