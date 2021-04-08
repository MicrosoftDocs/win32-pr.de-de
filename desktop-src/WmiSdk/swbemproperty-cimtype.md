---
description: Die Eigenschaft "CimType" des Objekts "Swap Property" ist eine Ganzzahl, mit der der CIM-Typ dieser Eigenschaft bestimmt werden kann. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: "' Taubemproperty. CimType '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959904"
---
# <a name="swbempropertycimtype-property"></a><span data-ttu-id="0063b-104">Taubemproperty. CimType (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0063b-104">SWbemProperty.CIMType property</span></span>

<span data-ttu-id="0063b-105">Die Eigenschaft " **CimType** " des Objekts " [**Swap Property**](swbemproperty.md) " ist eine Ganzzahl, mit der der CIM-Typ dieser Eigenschaft bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0063b-105">The **CIMType** property of the [**SWbemProperty**](swbemproperty.md) object is an integer that can be used to determine the CIM type of this property.</span></span> <span data-ttu-id="0063b-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0063b-106">This property is read-only.</span></span>

<span data-ttu-id="0063b-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0063b-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="0063b-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0063b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0063b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0063b-109">Syntax</span></span>


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a><span data-ttu-id="0063b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0063b-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0063b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0063b-111">Remarks</span></span>

<span data-ttu-id="0063b-112">Weitere Informationen zu gültigen Typen für diese Eigenschaft finden Sie unter [**wbemcimtypeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="0063b-112">For more information about valid types for this property, see [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>

<span data-ttu-id="0063b-113">Instanzen von eingebetteten Objekten werden in zusammengesetzten Objekten als Eigenschaften vom Typ **CIM- \_ Objekt** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0063b-113">Instances of embedded objects are stored in composite objects as properties of type **CIM\_OBJECT**.</span></span> <span data-ttu-id="0063b-114">Um die Klasse eines eingebetteten Objekts in einer Instanz einer zusammengesetzten Klasse zu ermitteln, müssen Sie den **CimType-Qualifizierer** der Eigenschaft **CIM- \_ Objekttyp** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0063b-114">To determine the class of an embedded object in an instance of a composite class, you must examine the **CIMType** qualifier of the **CIM\_OBJECT** type property.</span></span>

<span data-ttu-id="0063b-115">Die Objekt Verweise in einer Association-Klasse werden in Eigenschaften des Typs **CIM- \_ Verweis** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0063b-115">The object references in an association class are stored in properties of type **CIM\_REFERENCE**.</span></span> <span data-ttu-id="0063b-116">Um die eigentlichen Objekt Pfade zu ermitteln, müssen Sie den **CimType-Qualifizierer** der Eigenschaft **CIM- \_ Verweistyp** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0063b-116">To determine the actual object paths you must examine the **CIMType** qualifier of the **CIM\_REFERENCE** type property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0063b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0063b-117">Requirements</span></span>



| <span data-ttu-id="0063b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0063b-118">Requirement</span></span> | <span data-ttu-id="0063b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0063b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0063b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0063b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0063b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0063b-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0063b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0063b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0063b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0063b-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0063b-124">Header</span><span class="sxs-lookup"><span data-stu-id="0063b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0063b-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0063b-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0063b-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0063b-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="0063b-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0063b-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0063b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0063b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0063b-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0063b-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0063b-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="0063b-130">CLSID</span></span><br/>                    | <span data-ttu-id="0063b-131">CLSID- \_ Swap-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0063b-131">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="0063b-132">IID</span><span class="sxs-lookup"><span data-stu-id="0063b-132">IID</span></span><br/>                      | <span data-ttu-id="0063b-133">IID \_ iswbemproperty</span><span class="sxs-lookup"><span data-stu-id="0063b-133">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




