---
description: Die Item-Methode des Objekts "Swap PropertySet" Ruft eine benannte "taubemproperty" aus der Auflistung ab. Dies ist die Standardmethode für dieses Objekt.
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: "' Swap PropertySet. Item '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218292"
---
# <a name="swbempropertysetitem-method"></a><span data-ttu-id="211e5-104">Taubempropertyset. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="211e5-104">SWbemPropertySet.Item method</span></span>

<span data-ttu-id="211e5-105">Die **Item** -Methode des Objekts " [**Swap PropertySet**](swbempropertyset.md) " Ruft eine benannte " [**taubemproperty**](swbemproperty.md) " aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="211e5-105">The **Item** method of the [**SWbemPropertySet**](swbempropertyset.md) object gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="211e5-106">Dies ist die Standardmethode für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="211e5-106">This is the default method for this object.</span></span>

<span data-ttu-id="211e5-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="211e5-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="211e5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="211e5-108">Syntax</span></span>


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="211e5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="211e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="211e5-110">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="211e5-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="211e5-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="211e5-111">Required.</span></span> <span data-ttu-id="211e5-112">Der Name der abzurufenden Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="211e5-112">Name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="211e5-113">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="211e5-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="211e5-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="211e5-114">Reserved.</span></span> <span data-ttu-id="211e5-115">Dieser Wert muss NULL sein, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="211e5-115">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="211e5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="211e5-116">Return value</span></span>

<span data-ttu-id="211e5-117">Bei erfolgreicher Ausführung wird das angeforderte " [**Swap Property**](swbemproperty.md) "-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="211e5-117">If successful, the requested [**SWbemProperty**](swbemproperty.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="211e5-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="211e5-118">Error codes</span></span>

<span data-ttu-id="211e5-119">Nach dem Abschluss der **Element** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="211e5-119">After the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="211e5-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="211e5-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="211e5-121">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="211e5-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="211e5-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="211e5-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="211e5-123">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="211e5-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="211e5-124">**wbemErrOutOfMemory** -2147749896</span><span class="sxs-lookup"><span data-stu-id="211e5-124">**wbemErrOutOfMemory** - 2147749896</span></span>
</dt> <dd>

<span data-ttu-id="211e5-125">Nicht genügend Arbeitsspeicher für die Ausführung dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="211e5-125">Not enough memory for this method to execute.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="211e5-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="211e5-126">Requirements</span></span>



| <span data-ttu-id="211e5-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="211e5-127">Requirement</span></span> | <span data-ttu-id="211e5-128">Wert</span><span class="sxs-lookup"><span data-stu-id="211e5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="211e5-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="211e5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="211e5-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="211e5-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="211e5-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="211e5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="211e5-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="211e5-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="211e5-133">Header</span><span class="sxs-lookup"><span data-stu-id="211e5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="211e5-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="211e5-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="211e5-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="211e5-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="211e5-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="211e5-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="211e5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="211e5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="211e5-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="211e5-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="211e5-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="211e5-139">CLSID</span></span><br/>                    | <span data-ttu-id="211e5-140">CLSID- \_ Swap-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="211e5-140">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="211e5-141">IID</span><span class="sxs-lookup"><span data-stu-id="211e5-141">IID</span></span><br/>                      | <span data-ttu-id="211e5-142">IID \_ iswbempropertyset</span><span class="sxs-lookup"><span data-stu-id="211e5-142">IID\_ISWbemPropertySet</span></span><br/>                                                       |



 

 




