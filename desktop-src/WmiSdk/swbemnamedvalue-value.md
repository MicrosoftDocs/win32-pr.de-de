---
description: Die Value-Eigenschaft des-Objekts von ' Swap Name ' gibt den Variant-Wert eines ' Swap NamedValue '-Elements zurück.
ms.assetid: f9609bd2-893a-48c3-9faa-93cd033c4109
ms.tgt_platform: multiple
title: "' Taubemnamedvalue. Value '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue.Value
- ISWbemNamedValue.Value
- ISWbemNamedValue.get_Value
- ISWbemNamedValue.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bf63b15a27c1149341200f29e938bdba6cd7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130988"
---
# <a name="swbemnamedvaluevalue-property"></a><span data-ttu-id="eea17-103">"Swap NamedValue. Value"-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eea17-103">SWbemNamedValue.Value property</span></span>

<span data-ttu-id="eea17-104">Die **value** -Eigenschaft des-Objekts von ' [**Swap Name**](swbemnamedvalue.md) ' gibt den Variant-Wert eines ' **Swap NamedValue** '-Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="eea17-104">The **Value** property of the [**SWbemNamedValue**](swbemnamedvalue.md) object returns the variant value of an **SWbemNamedValue** item.</span></span> <span data-ttu-id="eea17-105">Dies ist die Standard Eigenschaft für die Objekte " **Swap Name** ".</span><span class="sxs-lookup"><span data-stu-id="eea17-105">This is the default property for **SWbemNamedValue** objects.</span></span> <span data-ttu-id="eea17-106">Änderungen, die an der Value-Eigenschaft vorgenommen werden, werden automatisch in der Auflistung von [**Swap namedvalueset**](swbemnamedvalueset.md) reflektiert, zu der das Objekt " **Swap Name Name** " gehört.</span><span class="sxs-lookup"><span data-stu-id="eea17-106">Changes made to the value property are reflected automatically in the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection to which the **SWbemNamedValue** object belongs.</span></span>

<span data-ttu-id="eea17-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eea17-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="eea17-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="eea17-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea17-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="eea17-109">Syntax</span></span>


```VB
SWbemNamedValue.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="eea17-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="eea17-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="eea17-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eea17-111">Requirements</span></span>



| <span data-ttu-id="eea17-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eea17-112">Requirement</span></span> | <span data-ttu-id="eea17-113">Wert</span><span class="sxs-lookup"><span data-stu-id="eea17-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eea17-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eea17-114">Minimum supported client</span></span><br/> | <span data-ttu-id="eea17-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eea17-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eea17-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eea17-116">Minimum supported server</span></span><br/> | <span data-ttu-id="eea17-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eea17-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eea17-118">Header</span><span class="sxs-lookup"><span data-stu-id="eea17-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea17-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eea17-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eea17-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="eea17-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="eea17-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eea17-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eea17-122">DLL</span><span class="sxs-lookup"><span data-stu-id="eea17-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea17-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea17-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eea17-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="eea17-124">CLSID</span></span><br/>                    | <span data-ttu-id="eea17-125">CLSID- \_ Swap-NamedValue</span><span class="sxs-lookup"><span data-stu-id="eea17-125">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="eea17-126">IID</span><span class="sxs-lookup"><span data-stu-id="eea17-126">IID</span></span><br/>                      | <span data-ttu-id="eea17-127">IID \_ iswbemnamedvalue</span><span class="sxs-lookup"><span data-stu-id="eea17-127">IID\_ISWbemNamedValue</span></span><br/>                                                        |



 

 




