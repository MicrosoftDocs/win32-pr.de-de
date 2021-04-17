---
description: Die Add-Methode des-Objekts "Swap Name" fügt der-Auflistung ein "-Objekt"-Objekt hinzu. Wenn ein Element bereits in der Auflistung mit dem gleichen Namen vorhanden ist, wird es durch das neue Element ersetzt.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: "' Taubemnamedvalueset. Add '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528481"
---
# <a name="swbemnamedvaluesetadd-method"></a><span data-ttu-id="8c22e-104">Methode ' Swap-namedvalueset. Add '</span><span class="sxs-lookup"><span data-stu-id="8c22e-104">SWbemNamedValueSet.Add method</span></span>

<span data-ttu-id="8c22e-105">Die **Add** -Methode des-Objekts " [**Swap Name**](swbemnamedvalueset.md) " fügt der-Auflistung [**ein "**](swbemnamedvalue.md) -Objekt"-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="8c22e-105">The **Add** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span> <span data-ttu-id="8c22e-106">Wenn ein Element bereits in der Auflistung mit dem gleichen Namen vorhanden ist, wird es durch das neue Element ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8c22e-106">If an element already exists in the collection with the same name, the new element replaces it.</span></span>

<span data-ttu-id="8c22e-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8c22e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c22e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c22e-108">Syntax</span></span>


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8c22e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c22e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c22e-110">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="8c22e-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c22e-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8c22e-111">Required.</span></span> <span data-ttu-id="8c22e-112">Der Name des neuen Werts.</span><span class="sxs-lookup"><span data-stu-id="8c22e-112">Name of the new value.</span></span>

</dd> <dt>

<span data-ttu-id="8c22e-113">*varval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c22e-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c22e-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8c22e-114">Required.</span></span> <span data-ttu-id="8c22e-115">Variant, der den neuen Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="8c22e-115">Variant that represents the new value.</span></span>

</dd> <dt>

<span data-ttu-id="8c22e-116">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8c22e-116">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c22e-117">Reserviert und muss auf 0 (null) festgelegt werden, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="8c22e-117">Reserved and must be set to zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c22e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c22e-118">Return value</span></span>

<span data-ttu-id="8c22e-119">Wenn der Vorgang erfolgreich ist, gibt diese Methode das neu geänderte oder neu erstellte " [**Swap Name**](swbemnamedvalue.md) "-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8c22e-119">If successful, this method returns the newly modified or newly created [**SWbemNamedValue**](swbemnamedvalue.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c22e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c22e-120">Remarks</span></span>

<span data-ttu-id="8c22e-121">Beispiele zum Hinzufügen und Abrufen benannter [**Werte finden Sie**](swbemnamedvalue-value.md)unter "".</span><span class="sxs-lookup"><span data-stu-id="8c22e-121">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c22e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c22e-122">Requirements</span></span>



| <span data-ttu-id="8c22e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c22e-123">Requirement</span></span> | <span data-ttu-id="8c22e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8c22e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c22e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c22e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8c22e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c22e-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c22e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c22e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8c22e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c22e-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c22e-129">Header</span><span class="sxs-lookup"><span data-stu-id="8c22e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c22e-130"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c22e-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c22e-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8c22e-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="8c22e-132"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8c22e-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8c22e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8c22e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c22e-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c22e-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8c22e-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="8c22e-135">CLSID</span></span><br/>                    | <span data-ttu-id="8c22e-136">CLSID- \_ Swap-namedvalueset</span><span class="sxs-lookup"><span data-stu-id="8c22e-136">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="8c22e-137">IID</span><span class="sxs-lookup"><span data-stu-id="8c22e-137">IID</span></span><br/>                      | <span data-ttu-id="8c22e-138">IID \_ iswbemnamedvalueset</span><span class="sxs-lookup"><span data-stu-id="8c22e-138">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="8c22e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c22e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c22e-140">**Austausch Elementname**</span><span class="sxs-lookup"><span data-stu-id="8c22e-140">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




