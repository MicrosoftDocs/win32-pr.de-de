---
title: CFSTR_DSPROPERTYPAGEINFO (DSClient. h)
description: Das cfstr \_ dspropertypageinfo-Zwischenablage Format bietet einen HGLOBAL-Wert, der eine dspropertypageinfo-Struktur enthält.
ms.assetid: 84ed1322-fee3-44ee-873e-57586261ff62
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSPROPERTYPAGEINFO
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259c9addbb3ee41c7b12cd7ea77eb8393b69daaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040450"
---
# <a name="cfstr_dspropertypageinfo"></a><span data-ttu-id="0d6a0-103">cfstr \_ dspropertypageinfo</span><span class="sxs-lookup"><span data-stu-id="0d6a0-103">CFSTR\_DSPROPERTYPAGEINFO</span></span>

<dl> <dt>

<span data-ttu-id="0d6a0-104"><span id="CFSTR_DSPROPERTYPAGEINFO"></span><span id="cfstr_dspropertypageinfo"></span>**cfstr \_ dspropertypageinfo**</span><span class="sxs-lookup"><span data-stu-id="0d6a0-104"><span id="CFSTR_DSPROPERTYPAGEINFO"></span><span id="cfstr_dspropertypageinfo"></span>**CFSTR\_DSPROPERTYPAGEINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d6a0-105">"Dsproppageinfo"</span><span class="sxs-lookup"><span data-stu-id="0d6a0-105">"DsPropPageInfo"</span></span>
</dt> <dt>



<span data-ttu-id="0d6a0-106">Das **cfstr \_ dspropertypageinfo** -Zwischenablage Format bietet einen **HGLOBAL** -Wert, der eine [**dspropertypageinfo**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-106">The **CFSTR\_DSPROPERTYPAGEINFO** clipboard format provides an **HGLOBAL** that contains a [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) structure.</span></span> <span data-ttu-id="0d6a0-107">Die **dspropertypageinfo** -Struktur enthält die optionale Zeichenfolge, die die Erweiterung den **adminpropertysheet** -und/oder **shellpropertysheet** -Parameterwerten hinzugefügt hat, als die Erweiterung registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-107">The **DSPROPERTYPAGEINFO** structure contains the optional string that the extension added to the **adminPropertySheet** and/or **shellPropertySheet** parameter values when the extension was registered.</span></span> <span data-ttu-id="0d6a0-108">Weitere Informationen zur Festlegung dieser Zeichenfolge finden Sie unter [Registrieren des COM-Objekts der Eigenschaften Seite in einem Anzeigespezifizierer](registering-the-property-page-com-object-in-a-display-specifier.md).</span><span class="sxs-lookup"><span data-stu-id="0d6a0-108">For more information about how this string is set, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d6a0-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d6a0-109">Requirements</span></span>



| <span data-ttu-id="0d6a0-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d6a0-110">Requirement</span></span> | <span data-ttu-id="0d6a0-111">Wert</span><span class="sxs-lookup"><span data-stu-id="0d6a0-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6a0-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d6a0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0d6a0-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d6a0-113">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="0d6a0-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d6a0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0d6a0-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d6a0-115">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="0d6a0-116">Header</span><span class="sxs-lookup"><span data-stu-id="0d6a0-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d6a0-117"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d6a0-117"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d6a0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d6a0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d6a0-119">**Dspropertypageinfo**</span><span class="sxs-lookup"><span data-stu-id="0d6a0-119">**DSPROPERTYPAGEINFO**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo)
</dt> <dt>

[<span data-ttu-id="0d6a0-120">Registrieren des COM-Objekts der Eigenschaften Seite in einem Anzeigespezifizierer</span><span class="sxs-lookup"><span data-stu-id="0d6a0-120">Registering the Property Page COM Object in a Display Specifier</span></span>](registering-the-property-page-com-object-in-a-display-specifier.md)
</dt> </dl>

 

 





