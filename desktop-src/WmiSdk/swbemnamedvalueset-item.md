---
description: Die Item-Methode des "Swap Name"-Objekts Ruft ein "taubemnamedvalue"-Objekt aus der Auflistung ab.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: Swap-namedvalueset. Item-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528478"
---
# <a name="swbemnamedvaluesetitem-method"></a><span data-ttu-id="8f14c-103">Swap-namedvalueset. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="8f14c-103">SWbemNamedValueSet.Item method</span></span>

<span data-ttu-id="8f14c-104">Die **Item** -Methode des " [**Swap Name**](swbemnamedvalueset.md) "-Objekts Ruft ein " [**taubemnamedvalue**](swbemnamedvalue.md) "-Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="8f14c-104">The **Item** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object gets an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span>

<span data-ttu-id="8f14c-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8f14c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f14c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f14c-106">Syntax</span></span>


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8f14c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f14c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f14c-108">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="8f14c-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f14c-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8f14c-109">Required.</span></span> <span data-ttu-id="8f14c-110">Der Name des abzurufenden Werts.</span><span class="sxs-lookup"><span data-stu-id="8f14c-110">Name of the value to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="8f14c-111">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8f14c-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f14c-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8f14c-112">Reserved.</span></span> <span data-ttu-id="8f14c-113">Dieser Wert muss NULL sein, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="8f14c-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f14c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f14c-114">Return value</span></span>

<span data-ttu-id="8f14c-115">Wenn erfolgreich, wird das angeforderte " [**Swap Name**](swbemnamedvalue.md) "-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8f14c-115">If successful, the requested [**SWbemNamedValue**](swbemnamedvalue.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8f14c-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8f14c-116">Error codes</span></span>

<span data-ttu-id="8f14c-117">Nach Abschluss der **Element** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="8f14c-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8f14c-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8f14c-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8f14c-119">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8f14c-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8f14c-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8f14c-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8f14c-121">Es wurde ein ungültiger Parameter angegeben, oder der Namespace konnte nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="8f14c-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="8f14c-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8f14c-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8f14c-123">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8f14c-123">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f14c-124">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="8f14c-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="8f14c-125">Das angeforderte Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="8f14c-125">The requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f14c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f14c-126">Remarks</span></span>

<span data-ttu-id="8f14c-127">Beispiele zum Hinzufügen und Abrufen benannter [**Werte finden Sie**](swbemnamedvalue-value.md)unter "".</span><span class="sxs-lookup"><span data-stu-id="8f14c-127">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f14c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f14c-128">Requirements</span></span>



| <span data-ttu-id="8f14c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f14c-129">Requirement</span></span> | <span data-ttu-id="8f14c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="8f14c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f14c-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f14c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8f14c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f14c-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f14c-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f14c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8f14c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f14c-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f14c-135">Header</span><span class="sxs-lookup"><span data-stu-id="8f14c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f14c-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f14c-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f14c-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8f14c-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="8f14c-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8f14c-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8f14c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8f14c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f14c-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f14c-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8f14c-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="8f14c-141">CLSID</span></span><br/>                    | <span data-ttu-id="8f14c-142">CLSID- \_ Swap-namedvalueset</span><span class="sxs-lookup"><span data-stu-id="8f14c-142">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="8f14c-143">IID</span><span class="sxs-lookup"><span data-stu-id="8f14c-143">IID</span></span><br/>                      | <span data-ttu-id="8f14c-144">IID \_ iswbemnamedvalueset</span><span class="sxs-lookup"><span data-stu-id="8f14c-144">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="8f14c-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f14c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f14c-146">**Austausch Elementname**</span><span class="sxs-lookup"><span data-stu-id="8f14c-146">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




