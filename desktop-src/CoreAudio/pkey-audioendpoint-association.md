---
description: Die pkey \_ audioendpoint \_ -Zuordnungs Eigenschaft ordnet einem audioendpunktgerät eine-PIN-Kategorie (Kernel Streaming) zu.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345634"
---
# <a name="pkey_audioendpoint_association"></a><span data-ttu-id="22cb9-103">Pkey \_ audioendpoint-Zuordnung \_</span><span class="sxs-lookup"><span data-stu-id="22cb9-103">PKEY\_AudioEndpoint\_Association</span></span>

<span data-ttu-id="22cb9-104">Die **pkey \_ audioendpoint \_** -Zuordnungs Eigenschaft ordnet einem audioendpunktgerät eine-PIN-Kategorie (Kernel Streaming) zu.</span><span class="sxs-lookup"><span data-stu-id="22cb9-104">The **PKEY\_AudioEndpoint\_Association** property associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span> <span data-ttu-id="22cb9-105">Die INF-Datei, mit der ein Audioadapter installiert wird, weist jeder anheft-PIN im Adapter eine PIN-Kategorie zu.</span><span class="sxs-lookup"><span data-stu-id="22cb9-105">The .inf file that installs an audio adapter assigns a pin category to each KS pin in the adapter.</span></span> <span data-ttu-id="22cb9-106">Eine anheft-PIN auf einem Adapter Gerät stellt den Punkt dar, an dem ein Audiostream das Gerät betritt oder verlässt.</span><span class="sxs-lookup"><span data-stu-id="22cb9-106">A KS pin on an adapter device represents the point at which an audio stream enters or leaves the device.</span></span> <span data-ttu-id="22cb9-107">Eine PIN-Kategorie ist eine GUID, die den Typ der von einer Pin-Pin ausgeführten Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="22cb9-107">A pin category is a GUID that specifies the type of function performed by a KS pin.</span></span> <span data-ttu-id="22cb9-108">Die Header Datei "ksmedia. h" definiert z. b. die PIN-Kategorie GUID ksnodetype \_ Mikrofon, um eine KS-PIN anzugeben, die mit einem Mikrofon verbunden ist, und ksnodetype- \_ Kopfhörer, um eine KS-PIN anzugeben, die eine Verbindung mit dem</span><span class="sxs-lookup"><span data-stu-id="22cb9-108">For example, header file Ksmedia.h defines pin-category GUID KSNODETYPE\_MICROPHONE to indicate a KS pin that connects to a microphone, and KSNODETYPE\_HEADPHONES to indicate a KS pin that connects to headphones.</span></span> <span data-ttu-id="22cb9-109">Weitere Informationen finden Sie in der Beschreibung der Eigenschaften der PIN-Kategorie in der Windows-DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="22cb9-109">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="22cb9-110">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ LPWSTR festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22cb9-110">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="22cb9-111">Der **pwszval** -Member der **PROPVARIANT** -Struktur verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die eine-PIN-Kategorie-GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="22cb9-111">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a KS pin category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="22cb9-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22cb9-112">Requirements</span></span>



| <span data-ttu-id="22cb9-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22cb9-113">Requirement</span></span> | <span data-ttu-id="22cb9-114">Wert</span><span class="sxs-lookup"><span data-stu-id="22cb9-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22cb9-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22cb9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="22cb9-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22cb9-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="22cb9-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22cb9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="22cb9-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22cb9-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="22cb9-119">Header</span><span class="sxs-lookup"><span data-stu-id="22cb9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="22cb9-120"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="22cb9-120"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22cb9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22cb9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22cb9-122">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="22cb9-122">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="22cb9-123">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="22cb9-123">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




