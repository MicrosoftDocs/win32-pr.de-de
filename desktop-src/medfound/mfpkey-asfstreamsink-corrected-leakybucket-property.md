---
description: Gibt den &\# 0034; Leaky Bucket&\# 0034; Parameter für einen Stream in einer ASF-Medien Senke an.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862955"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a><span data-ttu-id="5c2af-103">Mfpkey \_ asfstreamsink \_ korrigiert \_ leakybucket-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5c2af-103">MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET property</span></span>

<span data-ttu-id="5c2af-104">Gibt die Parameter für den "Leaky Bucket" (siehe Hinweise) für einen Datenstrom in einer ASF-Medien Senke an.</span><span class="sxs-lookup"><span data-stu-id="5c2af-104">Specifies the "leaky bucket" parameters (see Remarks) for a stream on an ASF media sink.</span></span>



<span data-ttu-id="5c2af-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5c2af-105">Data type</span></span>

<span data-ttu-id="5c2af-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="5c2af-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5c2af-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="5c2af-107">PROPVARIANT member</span></span>

<span data-ttu-id="5c2af-108">Array von **DWORD** -Werten (**CAUL**)</span><span class="sxs-lookup"><span data-stu-id="5c2af-108">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="5c2af-109">VT \_ Vector \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="5c2af-109">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="5c2af-110">**CAUL**</span><span class="sxs-lookup"><span data-stu-id="5c2af-110">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="5c2af-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c2af-111">Remarks</span></span>

<span data-ttu-id="5c2af-112">Eine Anwendung kann diese Eigenschaft für einen Datenstrom der ASF-Medien Senke festlegen, nachdem der Medientyp für den Stream ausgehandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="5c2af-112">An application can set this property on a stream of the ASF media sink after the media type for the stream is negotiated.</span></span> <span data-ttu-id="5c2af-113">Verwenden Sie diese Eigenschaft, um das tatsächliche Puffer Fenster anzugeben, das der Windows Media-Codec verwenden wird.</span><span class="sxs-lookup"><span data-stu-id="5c2af-113">Use this property to specify the actual buffer window that the Windows Media codec will use.</span></span> <span data-ttu-id="5c2af-114">Sie können diese Informationen vom Codec abrufen, indem Sie die **iwmcodecleakybucket** -Schnittstelle verwenden, die im Windows Media-Format-SDK dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="5c2af-114">You can obtain this information from the codec by using the **IWMCodecLeakyBucket** interface, which is documented in the Windows Media Format SDK.</span></span>

<span data-ttu-id="5c2af-115">Der Wert dieser Eigenschaft ist ein Array von drei **DWORD** -Werten in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="5c2af-115">The value of this property is an array of three **DWORD** values in the following order:</span></span>

-   <span data-ttu-id="5c2af-116">Bitrate in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="5c2af-116">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="5c2af-117">Puffergröße in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5c2af-117">Buffer size, in bytes.</span></span>
-   <span data-ttu-id="5c2af-118">Anfängliche Puffer Füllgröße in Byte.</span><span class="sxs-lookup"><span data-stu-id="5c2af-118">Initial buffer fullness, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2af-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c2af-119">Requirements</span></span>



| <span data-ttu-id="5c2af-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c2af-120">Requirement</span></span> | <span data-ttu-id="5c2af-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5c2af-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2af-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c2af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2af-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c2af-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5c2af-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c2af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2af-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c2af-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5c2af-126">Header</span><span class="sxs-lookup"><span data-stu-id="5c2af-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c2af-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c2af-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2af-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c2af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2af-129">**IMF-Senke**</span><span class="sxs-lookup"><span data-stu-id="5c2af-129">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[<span data-ttu-id="5c2af-130">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c2af-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




