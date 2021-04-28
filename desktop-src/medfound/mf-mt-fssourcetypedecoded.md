---
description: 'MF_MT_FSSourceTypeDecoded Attribut: Gibt an, ob ein Decoder Beim Festlegen von Zeitstempeln Decodierungszeitstempel (DTS) verwenden kann.'
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093088"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="c8543-103">MF \_ MT \_ FSSourceTypeDecoded-Attribut</span><span class="sxs-lookup"><span data-stu-id="c8543-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="c8543-104">Gibt an, dass ein Medientyp automatisch decodiert wird.</span><span class="sxs-lookup"><span data-stu-id="c8543-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="c8543-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c8543-105">Data type</span></span>

<span data-ttu-id="c8543-106">**BOOL als** **UINT32 gespeichert**</span><span class="sxs-lookup"><span data-stu-id="c8543-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="c8543-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8543-107">Remarks</span></span>
<span data-ttu-id="c8543-108">Ein Medientyp wird als Attribut markiert, um anzugeben, dass dies in der physischen Quelle nicht vorhanden ist und von der Pipeline synthetisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c8543-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="c8543-109">Der Wert 1 (TRUE) gibt an, dass der Medientyp synthetisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c8543-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="c8543-110">Der Wert 0 (FALSE) oder der wert, der nicht vorhanden ist, gibt an, dass dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="c8543-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="c8543-111">In der aktuellen Version sollte dieses Attribut mithilfe des folgenden GUID-Werts anstelle der MD_MT_FSSourceTypeDecoded angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="c8543-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="c8543-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8543-112">Requirements</span></span>



| <span data-ttu-id="c8543-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8543-113">Requirement</span></span> | <span data-ttu-id="c8543-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c8543-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8543-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8543-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c8543-116">Windows 8 \[ Desktop-Apps \| UWP-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8543-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c8543-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8543-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c8543-118">UWP-Apps für Windows Server \[ 2012-Desktop-Apps \|\]</span><span class="sxs-lookup"><span data-stu-id="c8543-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="c8543-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8543-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8543-120">Alphabetische Liste Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c8543-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




