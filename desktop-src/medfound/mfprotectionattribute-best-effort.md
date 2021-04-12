---
description: Legen Sie als Attribut für ein IMF OutputSchema-Objekt fest.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: MFPROTECTIONATTRIBUTE_BEST_EFFORT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215419"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a><span data-ttu-id="6fadd-103">MF Protection Attribute- \_ Attribut mit Best möglichen \_ Anstrengungen</span><span class="sxs-lookup"><span data-stu-id="6fadd-103">MFPROTECTIONATTRIBUTE\_BEST\_EFFORT attribute</span></span>

<span data-ttu-id="6fadd-104">Legen Sie als Attribut für ein [**IMF OutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="6fadd-104">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span> <span data-ttu-id="6fadd-105">Wenn dieses Attribut vorhanden ist, wird ein fehlerhafter Versuch, den Schutz anzuwenden, ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6fadd-105">If this attribute is present, a failed attempt to apply the protection is ignored.</span></span> <span data-ttu-id="6fadd-106">Wenn der zugeordnete Attribut Wert **true** ist, sollte das Schutzschema mit dem [mfschutzattribute \_ \_](mfprotectionattribute-fail-over.md) -Attribut "Failover" angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fadd-106">If the associated attribute value is **TRUE**, the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute should be applied.</span></span>

## <a name="data-type"></a><span data-ttu-id="6fadd-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6fadd-107">Data type</span></span>

<span data-ttu-id="6fadd-108">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fadd-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6fadd-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fadd-109">Remarks</span></span>

<span data-ttu-id="6fadd-110">Wenn **true**, erzwingen Sie das Schutzschema mit dem [mfschutzattribute \_ \_](mfprotectionattribute-fail-over.md) -Attribut "Failover", wenn das Festlegen dieses Schutzes fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6fadd-110">If **TRUE**, enforce the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute if setting this protection fails.</span></span>

<span data-ttu-id="6fadd-111">Legen Sie als Attribut für ein [**IMF OutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="6fadd-111">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fadd-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fadd-112">Requirements</span></span>



| <span data-ttu-id="6fadd-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fadd-113">Requirement</span></span> | <span data-ttu-id="6fadd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6fadd-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6fadd-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fadd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6fadd-116">Nur Windows 8 \[ UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6fadd-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6fadd-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fadd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6fadd-118">Windows Server 2012 \[ UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6fadd-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6fadd-119">Header</span><span class="sxs-lookup"><span data-stu-id="6fadd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fadd-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fadd-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fadd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fadd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fadd-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6fadd-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6fadd-123">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="6fadd-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




