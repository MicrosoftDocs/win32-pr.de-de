---
description: Enthält die registrierten Eingabetypen für eine Media Foundation Transformation (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: MFT_INPUT_TYPES_Attributes-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527917"
---
# <a name="mft_input_types_attributes-attribute"></a><span data-ttu-id="02046-103">Attribute-Attribut für MFT- \_ Eingabe \_ Typen \_</span><span class="sxs-lookup"><span data-stu-id="02046-103">MFT\_INPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="02046-104">Enthält die registrierten Eingabetypen für eine Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="02046-104">Contains the registered input types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="02046-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="02046-105">Data type</span></span>

<span data-ttu-id="02046-106">**MFT \_ Registrieren \_ von \_ \[ \]** **als \[ Byte \]** gespeicherten Typinformationen</span><span class="sxs-lookup"><span data-stu-id="02046-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="02046-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="02046-107">Get/set</span></span>

<span data-ttu-id="02046-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="02046-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="02046-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="02046-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="02046-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02046-110">Remarks</span></span>

<span data-ttu-id="02046-111">Dieses Attribut wird für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**motenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="02046-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="02046-112">Dieses Attribut enthält ein Array von [**MFT \_ Register \_ Type \_ Info**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) -Strukturen, die ein oder mehrere Eingabeformate beschreiben, die vom MFT unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="02046-112">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more input formats supported by the MFT.</span></span> <span data-ttu-id="02046-113">Diese Werte werden aus der Registrierung entnommen und dienen als Hinweis für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="02046-113">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="02046-114">Die MFT unterstützt möglicherweise weitere Formate.</span><span class="sxs-lookup"><span data-stu-id="02046-114">The MFT might support additional formats.</span></span> <span data-ttu-id="02046-115">Um das tatsächliche Eingabeformat festzulegen, müssen Sie die MFT erstellen und [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="02046-115">To set the actual input format, you must create the MFT and call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="02046-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="02046-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="02046-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02046-117">Requirements</span></span>



| <span data-ttu-id="02046-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02046-118">Requirement</span></span> | <span data-ttu-id="02046-119">Wert</span><span class="sxs-lookup"><span data-stu-id="02046-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02046-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02046-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02046-121">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="02046-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="02046-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02046-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02046-123">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="02046-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="02046-124">Header</span><span class="sxs-lookup"><span data-stu-id="02046-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="02046-125"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="02046-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02046-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02046-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02046-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="02046-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="02046-128">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="02046-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




