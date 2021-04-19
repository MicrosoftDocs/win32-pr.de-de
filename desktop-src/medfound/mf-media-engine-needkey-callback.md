---
description: Attribut, das bei der Erstellung in imfmediaengineneedkeynotify an die Medien-Engine weitergegeben wird.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: MF_MEDIA_ENGINE_NEEDKEY_CALLBACK-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363891"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a><span data-ttu-id="5785f-103">MF-Medienmodul, \_ \_ \_ needkey- \_ Rückruf Attribut</span><span class="sxs-lookup"><span data-stu-id="5785f-103">MF\_MEDIA\_ENGINE\_NEEDKEY\_CALLBACK attribute</span></span>

<span data-ttu-id="5785f-104">Attribut, das bei der Erstellung in [**imfmediaengineneedkeynotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) an die Medien-Engine weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5785f-104">Attribute which is passed in the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) to the media engine on creation.</span></span>

## <a name="data-type"></a><span data-ttu-id="5785f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5785f-105">Data type</span></span>

<span data-ttu-id="5785f-106">**IMF mediaengineneedkeynotify \* *_ gespeichert als _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="5785f-106">**IMFMediaEngineNeedKeyNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="5785f-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="5785f-107">Get/set</span></span>

<span data-ttu-id="5785f-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="5785f-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="5785f-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="5785f-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="5785f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5785f-110">Remarks</span></span>

<span data-ttu-id="5785f-111">Der Wert dieses Attributs ist ein Zeiger auf die [**imfmediaengineneedkeynotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) -Schnittstelle, die von der Anwendung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="5785f-111">The value of this attribute is a pointer to the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) interface, implemented by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="5785f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5785f-112">Requirements</span></span>



| <span data-ttu-id="5785f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5785f-113">Requirement</span></span> | <span data-ttu-id="5785f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="5785f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5785f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5785f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5785f-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="5785f-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5785f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5785f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5785f-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5785f-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5785f-119">IDL</span><span class="sxs-lookup"><span data-stu-id="5785f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5785f-120"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5785f-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5785f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5785f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5785f-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5785f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




