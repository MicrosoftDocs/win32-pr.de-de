---
description: Die Remove-Methode des-Objekts aus der-Auflistung löscht einen benannten Qualifizierer.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Taubemqualifierset. Remove-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 39c95f268328bc0cad3f3c0874b633fc36c4f5b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528472"
---
# <a name="swbemqualifiersetremove-method"></a><span data-ttu-id="518a9-103">Taubemqualifierset. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="518a9-103">SWbemQualifierSet.Remove method</span></span>

<span data-ttu-id="518a9-104">Die **Remove** -Methode des [**-Objekts aus der-**](swbemqualifierset.md) Auflistung löscht einen benannten Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="518a9-104">The **Remove** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object deletes a named qualifier from the collection.</span></span>

<span data-ttu-id="518a9-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="518a9-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="518a9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="518a9-106">Syntax</span></span>


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="518a9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="518a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="518a9-108">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="518a9-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="518a9-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="518a9-109">Required.</span></span> <span data-ttu-id="518a9-110">Der Name des zu entfernenden Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="518a9-110">Name of the qualifier to remove.</span></span>

</dd> <dt>

<span data-ttu-id="518a9-111">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="518a9-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="518a9-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="518a9-112">Reserved.</span></span> <span data-ttu-id="518a9-113">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="518a9-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="518a9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="518a9-114">Return value</span></span>

<span data-ttu-id="518a9-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="518a9-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="518a9-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="518a9-116">Error codes</span></span>

<span data-ttu-id="518a9-117">Nach Abschluss der **Remove** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="518a9-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="518a9-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="518a9-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="518a9-119">Der *IFlags* -Parameter war ungültig.</span><span class="sxs-lookup"><span data-stu-id="518a9-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="518a9-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="518a9-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="518a9-121">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="518a9-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="518a9-122">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="518a9-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="518a9-123">Der angegebene Qualifizierer ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="518a9-123">Specified qualifier does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="518a9-124">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="518a9-124">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="518a9-125">Das Entfernen dieses Qualifizierers ist unzulässig.</span><span class="sxs-lookup"><span data-stu-id="518a9-125">Removing this qualifier is illegal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="518a9-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="518a9-126">Remarks</span></span>

<span data-ttu-id="518a9-127">Beim Entfernen von Elementen ist es nicht möglich, eine Auflistung zu durchlaufen, denn wenn Sie ein Element aus einer Auflistung entfernen, wird der Auflistungs Zeiger zum nächsten Element verschoben.</span><span class="sxs-lookup"><span data-stu-id="518a9-127">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="518a9-128">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="518a9-128">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="518a9-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="518a9-129">Requirements</span></span>



| <span data-ttu-id="518a9-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="518a9-130">Requirement</span></span> | <span data-ttu-id="518a9-131">Wert</span><span class="sxs-lookup"><span data-stu-id="518a9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="518a9-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="518a9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="518a9-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="518a9-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="518a9-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="518a9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="518a9-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="518a9-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="518a9-136">Header</span><span class="sxs-lookup"><span data-stu-id="518a9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="518a9-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="518a9-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="518a9-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="518a9-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="518a9-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="518a9-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="518a9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="518a9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="518a9-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="518a9-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="518a9-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="518a9-142">CLSID</span></span><br/>                    | <span data-ttu-id="518a9-143">CLSID- \_ Swap-Gruppe</span><span class="sxs-lookup"><span data-stu-id="518a9-143">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="518a9-144">IID</span><span class="sxs-lookup"><span data-stu-id="518a9-144">IID</span></span><br/>                      | <span data-ttu-id="518a9-145">IID \_ iswbemqualifierset</span><span class="sxs-lookup"><span data-stu-id="518a9-145">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="518a9-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="518a9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="518a9-147">**Swap-qualifierset**</span><span class="sxs-lookup"><span data-stu-id="518a9-147">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="518a9-148">**Austauschen von "austauschen. hinzufügen"**</span><span class="sxs-lookup"><span data-stu-id="518a9-148">**SWbemQualifierSet.Add**</span></span>](swbemqualifierset-add.md)
</dt> </dl>

 

 




