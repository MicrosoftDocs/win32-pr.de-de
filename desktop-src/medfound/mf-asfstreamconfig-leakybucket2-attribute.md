---
description: Legt die Spitze &\# 0034; Leaky Bucket&\# 0034; Parameter fest (siehe Hinweise), um eine Windows Media-Datei zu codieren. Diese Parameter werden für die Spitzen Bitrate verwendet. Legen Sie dieses Attribut mithilfe der imfasf streamconfig-Schnittstelle fest.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET2-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358580"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a><span data-ttu-id="ed911-105">MF \_ asfstreamconfig \_ LEAKYBUCKET2-Attribut</span><span class="sxs-lookup"><span data-stu-id="ed911-105">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2 attribute</span></span>

<span data-ttu-id="ed911-106">Legt die Spitzen Parameter "Leaky Bucket" (siehe Hinweise) zum Codieren einer Windows Media-Datei fest.</span><span class="sxs-lookup"><span data-stu-id="ed911-106">Sets the peak "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="ed911-107">Diese Parameter werden für die Spitzen Bitrate verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed911-107">These parameters are used for the peak bit rate.</span></span> <span data-ttu-id="ed911-108">Legen Sie dieses Attribut mithilfe der [**imfasf streamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="ed911-108">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="ed911-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ed911-109">Data type</span></span>

<span data-ttu-id="ed911-110">Bytearray</span><span class="sxs-lookup"><span data-stu-id="ed911-110">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="ed911-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed911-111">Remarks</span></span>

<span data-ttu-id="ed911-112">Der Wert dieses Attributs ist ein Array von drei **DWORD**-s in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="ed911-112">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="ed911-113">Bitrate in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="ed911-113">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="ed911-114">Puffer Fenster in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="ed911-114">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="ed911-115">Anfängliche Puffer Füllgröße in Byte.</span><span class="sxs-lookup"><span data-stu-id="ed911-115">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="ed911-116">Weitere Informationen zum "Leaky Bucket"-Konzept finden Sie im Thema " [Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) " in der Dokumentation zum Windows Media-Format SDK.</span><span class="sxs-lookup"><span data-stu-id="ed911-116">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="ed911-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ed911-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed911-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed911-118">Requirements</span></span>



| <span data-ttu-id="ed911-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed911-119">Requirement</span></span> | <span data-ttu-id="ed911-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ed911-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed911-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed911-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ed911-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed911-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ed911-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed911-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ed911-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed911-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ed911-125">Header</span><span class="sxs-lookup"><span data-stu-id="ed911-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed911-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed911-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed911-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed911-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed911-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ed911-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ed911-129">ASF-Attribute</span><span class="sxs-lookup"><span data-stu-id="ed911-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="ed911-130">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="ed911-130">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="ed911-131">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="ed911-131">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="ed911-132">**MF \_ asfstreamconfig \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="ed911-132">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




