---
description: Enthält den Klassen Bezeichner (CLSID) einer Media Foundation Transformation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: MFT_TRANSFORM_CLSID_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959237"
---
# <a name="mft_transform_clsid_attribute-attribute"></a><span data-ttu-id="0710b-103">Attribut Attribut der MFT- \_ Transformation für \_ CLSID \_</span><span class="sxs-lookup"><span data-stu-id="0710b-103">MFT\_TRANSFORM\_CLSID\_Attribute attribute</span></span>

<span data-ttu-id="0710b-104">Enthält den Klassen Bezeichner (CLSID) einer Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="0710b-104">Contains the class identifier (CLSID) of a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="0710b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0710b-105">Data type</span></span>

<span data-ttu-id="0710b-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="0710b-106">**GUID**</span></span>

## <a name="getset"></a><span data-ttu-id="0710b-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="0710b-107">Get/set</span></span>

<span data-ttu-id="0710b-108">Um dieses Attribut abzurufen, wenden Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)an.</span><span class="sxs-lookup"><span data-stu-id="0710b-108">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="0710b-109">Um dieses Attribut festzulegen, wenden Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)an.</span><span class="sxs-lookup"><span data-stu-id="0710b-109">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="0710b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0710b-110">Remarks</span></span>

<span data-ttu-id="0710b-111">Dieses Attribut wird für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**motenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0710b-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="0710b-112">Dieses Attribut wird vom Aktivierungs Objekt intern verwendet, wenn es die MFT erstellt.</span><span class="sxs-lookup"><span data-stu-id="0710b-112">This attribute is used internally by the activation object when it creates the MFT.</span></span> <span data-ttu-id="0710b-113">Anwendungen sollten diese CLSID nicht direkt verwenden, um die MFT zu erstellen, da das Aktivierungs Objekt möglicherweise die MFT initialisieren muss.</span><span class="sxs-lookup"><span data-stu-id="0710b-113">Applications should not use this CLSID directly to create the MFT, because the activation object might need to initialize the MFT.</span></span> <span data-ttu-id="0710b-114">Um eine Instanz des MFT zu erstellen, rufen Sie daher [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) für das Aktivierungs Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="0710b-114">Therefore, to create an instance of the MFT, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the activation object.</span></span>

<span data-ttu-id="0710b-115">Beachten Sie, dass sich die [**motenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion in dieser Hinsicht anders verhält als die [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0710b-115">Note that the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function behaves differently than the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function in this respect.</span></span> <span data-ttu-id="0710b-116">Die **mftenum** -Funktion gibt CLSIDs zurück, die von der Anwendung an die **cokreatumstance** -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="0710b-116">The **MFTEnum** function returns CLSIDs, which the application passes to the **CoCreateInstance** function.</span></span> <span data-ttu-id="0710b-117">Die **MF** -Funktion gibt anstelle von CLSIDs Aktivierungs Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="0710b-117">The **MFTEnumEx** function returns activation objects rather than CLSIDs.</span></span>

<span data-ttu-id="0710b-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="0710b-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0710b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0710b-119">Requirements</span></span>



| <span data-ttu-id="0710b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0710b-120">Requirement</span></span> | <span data-ttu-id="0710b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0710b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0710b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0710b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0710b-123">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0710b-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0710b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0710b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0710b-125">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0710b-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0710b-126">Header</span><span class="sxs-lookup"><span data-stu-id="0710b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0710b-127"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0710b-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0710b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0710b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0710b-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0710b-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0710b-130">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="0710b-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




