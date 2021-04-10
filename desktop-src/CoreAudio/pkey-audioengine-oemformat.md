---
description: Die Eigenschaft "pkey \_ Audioengine \_ oemformat" gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird. Die Werte werden vom OEM in einer INF-Datei aufgefüllt.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127428"
---
# <a name="pkey_audioengine_oemformat"></a><span data-ttu-id="3bb10-104">Pkey \_ Audioengine- \_ oemformat</span><span class="sxs-lookup"><span data-stu-id="3bb10-104">PKEY\_AudioEngine\_OEMFormat</span></span>

<span data-ttu-id="3bb10-105">Die Eigenschaft "pkey \_ Audioengine \_ oemformat" gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3bb10-105">The PKEY\_AudioEngine\_OEMFormat property specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="3bb10-106">Die Werte werden vom OEM in einer INF-Datei aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="3bb10-106">The values are populated by the OEM in an .inf file.</span></span>

<span data-ttu-id="3bb10-107">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf einen VT- \_ BLOB festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3bb10-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="3bb10-108">Der **BLOB** -Member der **PROPVARIANT** -Struktur ist eine Struktur vom Typ " **BLOB** ", die zwei Member enthält.</span><span class="sxs-lookup"><span data-stu-id="3bb10-108">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="3bb10-109">Member **BLOB. cbSize** ist ein **DWORD** -Wert, der die Anzahl der Bytes in der Formatbeschreibung angibt.</span><span class="sxs-lookup"><span data-stu-id="3bb10-109">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="3bb10-110">Member **BLOB. pblobdata** verweist auf eine **WaveFormatEx** -Struktur, die die Formatbeschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="3bb10-110">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="3bb10-111">Weitere Informationen zum BLOB finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3bb10-111">For more information about BLOB, see the Windows SDK documentation.</span></span> <span data-ttu-id="3bb10-112">Weitere Informationen zu **WaveFormatEx** finden Sie in der Windows-DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3bb10-112">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb10-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bb10-113">Requirements</span></span>



| <span data-ttu-id="3bb10-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bb10-114">Requirement</span></span> | <span data-ttu-id="3bb10-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3bb10-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb10-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bb10-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb10-117">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bb10-117">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3bb10-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bb10-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb10-119">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bb10-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3bb10-120">Header</span><span class="sxs-lookup"><span data-stu-id="3bb10-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bb10-121"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bb10-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bb10-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bb10-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb10-123">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="3bb10-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="3bb10-124">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bb10-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




