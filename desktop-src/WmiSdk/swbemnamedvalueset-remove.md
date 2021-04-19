---
description: Die Remove-Methode des "Swap Name"-Objekts löscht einen benannten Wert aus dem Kontext.
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: Taubemnamedvalueset. Remove-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d41ecd7d28b95534c8e6d88d1c57756c269cf790
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362879"
---
# <a name="swbemnamedvaluesetremove-method"></a><span data-ttu-id="ef4e2-103">Swap. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="ef4e2-103">SWbemNamedValueSet.Remove method</span></span>

<span data-ttu-id="ef4e2-104">Die **Remove** -Methode des " [**Swap Name**](swbemnamedvalueset.md) "-Objekts löscht einen benannten Wert aus dem Kontext.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-104">The **Remove** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object deletes a named value from the context.</span></span>

<span data-ttu-id="ef4e2-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ef4e2-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef4e2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef4e2-106">Syntax</span></span>


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ef4e2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef4e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef4e2-108">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="ef4e2-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4e2-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-109">Required.</span></span> <span data-ttu-id="ef4e2-110">Der Name des zu entfernenden Werts.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-110">Name of the value to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ef4e2-111">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ef4e2-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4e2-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-112">Reserved.</span></span> <span data-ttu-id="ef4e2-113">Dieser Wert muss NULL sein, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef4e2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef4e2-114">Return value</span></span>

<span data-ttu-id="ef4e2-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef4e2-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ef4e2-116">Error codes</span></span>

<span data-ttu-id="ef4e2-117">Nach Abschluss der **Remove** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-117">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ef4e2-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ef4e2-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ef4e2-119">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ef4e2-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ef4e2-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ef4e2-121">Es wurde ein ungültiger Parameter angegeben, oder der Namespace konnte nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="ef4e2-122">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="ef4e2-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="ef4e2-123">Das angeforderte Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ef4e2-123">The requested item was not found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef4e2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef4e2-124">Requirements</span></span>



| <span data-ttu-id="ef4e2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef4e2-125">Requirement</span></span> | <span data-ttu-id="ef4e2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ef4e2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4e2-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef4e2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ef4e2-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef4e2-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef4e2-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef4e2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ef4e2-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef4e2-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef4e2-131">Header</span><span class="sxs-lookup"><span data-stu-id="ef4e2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef4e2-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef4e2-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef4e2-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ef4e2-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef4e2-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ef4e2-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ef4e2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ef4e2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef4e2-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef4e2-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef4e2-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="ef4e2-137">CLSID</span></span><br/>                    | <span data-ttu-id="ef4e2-138">CLSID- \_ Swap-namedvalueset</span><span class="sxs-lookup"><span data-stu-id="ef4e2-138">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="ef4e2-139">IID</span><span class="sxs-lookup"><span data-stu-id="ef4e2-139">IID</span></span><br/>                      | <span data-ttu-id="ef4e2-140">IID \_ iswbemnamedvalueset</span><span class="sxs-lookup"><span data-stu-id="ef4e2-140">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="ef4e2-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef4e2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef4e2-142">**Austausch Elementname**</span><span class="sxs-lookup"><span data-stu-id="ef4e2-142">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




