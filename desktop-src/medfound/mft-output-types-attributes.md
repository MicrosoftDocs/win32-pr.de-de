---
description: Enthält die registrierten Ausgabetypen für eine Media Foundation Transformation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: MFT_OUTPUT_TYPES_Attributes-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354571"
---
# <a name="mft_output_types_attributes-attribute"></a><span data-ttu-id="ee457-103">Attribut Attribute für MFT- \_ Ausgabe \_ Typen \_</span><span class="sxs-lookup"><span data-stu-id="ee457-103">MFT\_OUTPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="ee457-104">Enthält die registrierten Ausgabetypen für eine Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="ee457-104">Contains the registered output types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="ee457-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ee457-105">Data type</span></span>

<span data-ttu-id="ee457-106">**MFT \_ Registrieren \_ von \_ \[ \]** **als \[ Byte \]** gespeicherten Typinformationen</span><span class="sxs-lookup"><span data-stu-id="ee457-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="remarks"></a><span data-ttu-id="ee457-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee457-107">Remarks</span></span>

<span data-ttu-id="ee457-108">Dieses Attribut wird für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**motenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ee457-108">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="ee457-109">Dieses Attribut enthält ein Array von [**MFT \_ Register \_ Type \_ Info**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) -Strukturen, die ein oder mehrere Ausgabeformate beschreiben, die vom MFT unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ee457-109">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more output formats supported by the MFT.</span></span> <span data-ttu-id="ee457-110">Diese Werte werden aus der Registrierung entnommen und dienen als Hinweis für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ee457-110">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="ee457-111">Die MFT unterstützt möglicherweise weitere Formate.</span><span class="sxs-lookup"><span data-stu-id="ee457-111">The MFT might support additional formats.</span></span> <span data-ttu-id="ee457-112">Um das tatsächliche Ausgabeformat festzulegen, müssen Sie die MFT erstellen und [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ee457-112">To set the actual output format, you must create the MFT and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="ee457-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ee457-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee457-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee457-114">Requirements</span></span>



| <span data-ttu-id="ee457-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee457-115">Requirement</span></span> | <span data-ttu-id="ee457-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ee457-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee457-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee457-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ee457-118">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ee457-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ee457-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee457-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ee457-120">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ee457-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ee457-121">Header</span><span class="sxs-lookup"><span data-stu-id="ee457-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee457-122"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ee457-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee457-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee457-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee457-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ee457-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee457-125">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="ee457-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




