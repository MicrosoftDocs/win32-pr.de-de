---
description: Legt den Mittelwert &\# 0034; Leaky Bucket&\# 0034;-Parametern fest (siehe Hinweise), um eine Windows Media-Datei zu codieren. Legen Sie dieses Attribut mithilfe der imfasf streamconfig-Schnittstelle fest.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET1-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348870"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a><span data-ttu-id="d4730-104">MF \_ asfstreamconfig \_ LEAKYBUCKET1-Attribut</span><span class="sxs-lookup"><span data-stu-id="d4730-104">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1 attribute</span></span>

<span data-ttu-id="d4730-105">Legt die durchschnittlichen Parameter für "Leaky Bucket" (siehe Hinweise) zum Codieren einer Windows Media-Datei fest.</span><span class="sxs-lookup"><span data-stu-id="d4730-105">Sets the average "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="d4730-106">Legen Sie dieses Attribut mithilfe der [**imfasf streamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="d4730-106">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4730-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d4730-107">Data type</span></span>

<span data-ttu-id="d4730-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="d4730-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="d4730-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4730-109">Remarks</span></span>

<span data-ttu-id="d4730-110">Der Wert dieses Attributs ist ein Array von drei **DWORD**-s in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="d4730-110">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="d4730-111">Bitrate in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="d4730-111">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="d4730-112">Puffer Fenster in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="d4730-112">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="d4730-113">Anfängliche Puffer Füllgröße in Byte.</span><span class="sxs-lookup"><span data-stu-id="d4730-113">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="d4730-114">Weitere Informationen zum "Leaky Bucket"-Konzept finden Sie im Thema " [Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) " in der Dokumentation zum Windows Media-Format SDK.</span><span class="sxs-lookup"><span data-stu-id="d4730-114">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="d4730-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="d4730-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4730-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4730-116">Requirements</span></span>



| <span data-ttu-id="d4730-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4730-117">Requirement</span></span> | <span data-ttu-id="d4730-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d4730-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4730-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4730-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4730-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4730-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d4730-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4730-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4730-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4730-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d4730-123">Header</span><span class="sxs-lookup"><span data-stu-id="d4730-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4730-124"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4730-124"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4730-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4730-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4730-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="d4730-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4730-127">ASF-Attribute</span><span class="sxs-lookup"><span data-stu-id="d4730-127">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4730-128">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="d4730-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="d4730-129">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="d4730-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="d4730-130">**MF \_ asfstreamconfig \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="d4730-130">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




