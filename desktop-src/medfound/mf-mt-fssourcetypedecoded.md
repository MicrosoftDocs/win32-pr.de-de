---
description: Gibt an, ob ein Decoder beim Festlegen von Zeitstempeln decodierungszeit Stempel (DTS) verwenden kann.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366248"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="4ffea-103">MF \_ MT- \_ Attribut "f"</span><span class="sxs-lookup"><span data-stu-id="4ffea-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="4ffea-104">Gibt an, dass ein Medientyp automatisch decodiert wird.</span><span class="sxs-lookup"><span data-stu-id="4ffea-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="4ffea-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4ffea-105">Data type</span></span>

<span data-ttu-id="4ffea-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ffea-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="4ffea-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ffea-107">Remarks</span></span>
<span data-ttu-id="4ffea-108">Ein Medientyp ist als Attribut gekennzeichnet, um anzugeben, dass dieser nicht in der physischen Quelle vorhanden ist und von der Pipeline synthetisiert wird.</span><span class="sxs-lookup"><span data-stu-id="4ffea-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="4ffea-109">Der Wert 1 (true) gibt an, dass der Medientyp synthetisiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ffea-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="4ffea-110">Der Wert 0 (false) oder der Wert, der nicht vorhanden ist, gibt an, dass dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="4ffea-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="4ffea-111">In der aktuellen Version sollte dieses Attribut anstelle der MD_MT_FSSourceTypeDecoded Konstante mit dem folgenden GUID-Wert angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="4ffea-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="4ffea-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ffea-112">Requirements</span></span>



| <span data-ttu-id="4ffea-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ffea-113">Requirement</span></span> | <span data-ttu-id="4ffea-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4ffea-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4ffea-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ffea-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4ffea-116">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4ffea-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4ffea-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ffea-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4ffea-118">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4ffea-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="4ffea-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ffea-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ffea-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4ffea-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




