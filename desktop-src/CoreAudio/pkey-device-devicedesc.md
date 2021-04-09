---
description: Die Eigenschaft "devicedebug" des pkey- \_ Geräts \_ enthält die Geräte Beschreibung des Endpunkt Geräts (z. b \# . &0034; Sprecher&\# 0034;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860588"
---
# <a name="pkey_device_devicedesc"></a><span data-ttu-id="9463d-103">Pkey- \_ Gerät \_ devicedebug</span><span class="sxs-lookup"><span data-stu-id="9463d-103">PKEY\_Device\_DeviceDesc</span></span>

<span data-ttu-id="9463d-104">Die Eigenschaft " **\_ \_ devicedebug" des pkey-Geräts** enthält die Geräte Beschreibung des Endpunkt Geräts (z. b. "Sprecher").</span><span class="sxs-lookup"><span data-stu-id="9463d-104">The **PKEY\_Device\_DeviceDesc** property contains the device description of the endpoint device (for example, "Speakers").</span></span>

<span data-ttu-id="9463d-105">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ LPWSTR festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9463d-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="9463d-106">Der **pwszval** -Member der **PROPVARIANT** -Struktur verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die die Geräte Beschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="9463d-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the device description.</span></span>

## <a name="requirements"></a><span data-ttu-id="9463d-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9463d-107">Requirements</span></span>



| <span data-ttu-id="9463d-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9463d-108">Requirement</span></span> | <span data-ttu-id="9463d-109">Wert</span><span class="sxs-lookup"><span data-stu-id="9463d-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9463d-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9463d-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9463d-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9463d-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9463d-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9463d-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9463d-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9463d-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="9463d-114">Header</span><span class="sxs-lookup"><span data-stu-id="9463d-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="9463d-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="9463d-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9463d-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9463d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9463d-117">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="9463d-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="9463d-118">Geräteeigenschaften</span><span class="sxs-lookup"><span data-stu-id="9463d-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




