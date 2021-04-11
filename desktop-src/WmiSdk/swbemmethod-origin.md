---
description: Die Origin-Eigenschaft des Objekts "Swap Method" gibt den Namen der Klasse zurück, in der diese Methode eingeführt wurde.
ms.assetid: da98393b-af95-47ad-b589-663063f65afb
ms.tgt_platform: multiple
title: "' Taubemmethod. Origin '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.Origin
- ISWbemMethod.Origin
- ISWbemMethod.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1b903a2c55bbd571a9cd1f36a51812a70c123cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215323"
---
# <a name="swbemmethodorigin-property"></a><span data-ttu-id="0973e-103">Taubemmethod. Origin (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0973e-103">SWbemMethod.Origin property</span></span>

<span data-ttu-id="0973e-104">Die **Origin** -Eigenschaft des Objekts " [**Swap Method**](swbemmethod.md) " gibt den Namen der Klasse zurück, in der diese Methode eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0973e-104">The **Origin** property of the [**SWbemMethod**](swbemmethod.md) object returns the name of the class in which this method was introduced.</span></span> <span data-ttu-id="0973e-105">Für Klassen mit tiefen Vererbungs Hierarchien ist es häufig wünschenswert zu wissen, welche Methoden in welchen Klassen deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="0973e-105">For classes with deep inheritance hierarchies, it is often desirable to know which methods were declared in which classes.</span></span> <span data-ttu-id="0973e-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0973e-106">This property is read-only.</span></span>

<span data-ttu-id="0973e-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0973e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="0973e-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0973e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0973e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0973e-109">Syntax</span></span>


```VB
SWbemMethod.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="0973e-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0973e-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="0973e-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0973e-111">Requirements</span></span>



| <span data-ttu-id="0973e-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0973e-112">Requirement</span></span> | <span data-ttu-id="0973e-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0973e-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0973e-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0973e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0973e-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0973e-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0973e-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0973e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0973e-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0973e-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0973e-118">Header</span><span class="sxs-lookup"><span data-stu-id="0973e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0973e-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0973e-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0973e-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="0973e-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0973e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0973e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0973e-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0973e-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="0973e-124">CLSID</span></span><br/>                    | <span data-ttu-id="0973e-125">CLSID- \_ Swap-Methode</span><span class="sxs-lookup"><span data-stu-id="0973e-125">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="0973e-126">IID</span><span class="sxs-lookup"><span data-stu-id="0973e-126">IID</span></span><br/>                      | <span data-ttu-id="0973e-127">IID \_ iswbemmethod</span><span class="sxs-lookup"><span data-stu-id="0973e-127">IID\_ISWbemMethod</span></span><br/>                                                            |



 

 




