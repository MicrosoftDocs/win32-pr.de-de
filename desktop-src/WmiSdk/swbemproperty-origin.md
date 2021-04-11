---
description: Die Origin-Eigenschaft des "Swap Property"-Objekts Ruft den Namen der WMI-Klasse ab, in der diese Eigenschaft eingeführt wurde. Für Klassen mit tiefen Vererbungs Hierarchien ist es häufig wünschenswert zu wissen, welche Eigenschaften in welchen Klassen deklariert wurden.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Taubemproperty. Origin-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216317"
---
# <a name="swbempropertyorigin-property"></a><span data-ttu-id="04a30-104">Taubemproperty. Origin (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="04a30-104">SWbemProperty.Origin property</span></span>

<span data-ttu-id="04a30-105">Die **Origin** -Eigenschaft des " [**Swap Property**](swbemproperty.md) "-Objekts Ruft den Namen der WMI-Klasse ab, in der diese Eigenschaft eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="04a30-105">The **Origin** property of the [**SWbemProperty**](swbemproperty.md) object retrieves the name of the WMI class in which this property was introduced.</span></span> <span data-ttu-id="04a30-106">Für Klassen mit tiefen Vererbungs Hierarchien ist es häufig wünschenswert zu wissen, welche Eigenschaften in welchen Klassen deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="04a30-106">For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes.</span></span>

<span data-ttu-id="04a30-107">Wenn die Eigenschaft lokal ist (siehe " [**austauschen**](swbemqualifier-islocal.md)von"), ist dieser Wert identisch mit der besitzenden Klasse.</span><span class="sxs-lookup"><span data-stu-id="04a30-107">If the property is local (see [**SWbemQualifier.IsLocal**](swbemqualifier-islocal.md)), this value is the same as the owning class.</span></span> <span data-ttu-id="04a30-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="04a30-108">This property is read-only.</span></span>

<span data-ttu-id="04a30-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="04a30-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="04a30-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="04a30-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a30-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="04a30-111">Syntax</span></span>


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="04a30-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="04a30-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="04a30-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04a30-113">Requirements</span></span>



| <span data-ttu-id="04a30-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04a30-114">Requirement</span></span> | <span data-ttu-id="04a30-115">Wert</span><span class="sxs-lookup"><span data-stu-id="04a30-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04a30-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04a30-116">Minimum supported client</span></span><br/> | <span data-ttu-id="04a30-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04a30-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04a30-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04a30-118">Minimum supported server</span></span><br/> | <span data-ttu-id="04a30-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04a30-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04a30-120">Header</span><span class="sxs-lookup"><span data-stu-id="04a30-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="04a30-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a30-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="04a30-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="04a30-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="04a30-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="04a30-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="04a30-124">DLL</span><span class="sxs-lookup"><span data-stu-id="04a30-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04a30-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04a30-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="04a30-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="04a30-126">CLSID</span></span><br/>                    | <span data-ttu-id="04a30-127">CLSID- \_ Swap-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04a30-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="04a30-128">IID</span><span class="sxs-lookup"><span data-stu-id="04a30-128">IID</span></span><br/>                      | <span data-ttu-id="04a30-129">IID \_ iswbemproperty</span><span class="sxs-lookup"><span data-stu-id="04a30-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




