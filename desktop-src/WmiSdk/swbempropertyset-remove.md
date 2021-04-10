---
description: Die Remove-Methode des Objekts "Swap PropertySet" löscht eine Eigenschaft aus der Sammlung "Swap PropertySet".
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: "' Swap PropertySet. Remove '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130980"
---
# <a name="swbempropertysetremove-method"></a><span data-ttu-id="8354e-103">Methode ' Swap PropertySet. Remove '</span><span class="sxs-lookup"><span data-stu-id="8354e-103">SWbemPropertySet.Remove method</span></span>

<span data-ttu-id="8354e-104">Die **Remove** -Methode des Objekts " [**Swap PropertySet**](swbempropertyset.md) " löscht eine Eigenschaft aus der Sammlung " **Swap PropertySet** ".</span><span class="sxs-lookup"><span data-stu-id="8354e-104">The **Remove** method of the [**SWbemPropertySet**](swbempropertyset.md) object deletes a property from the **SWbemPropertySet** collection.</span></span>

<span data-ttu-id="8354e-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8354e-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8354e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8354e-106">Syntax</span></span>


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8354e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8354e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8354e-108">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="8354e-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8354e-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8354e-109">Required.</span></span> <span data-ttu-id="8354e-110">Der Name des zu entfernenden Elements.</span><span class="sxs-lookup"><span data-stu-id="8354e-110">Name of the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="8354e-111">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8354e-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8354e-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8354e-112">Reserved.</span></span> <span data-ttu-id="8354e-113">Wenn angegeben, muss dieser Wert 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="8354e-113">This value must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8354e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8354e-114">Return value</span></span>

<span data-ttu-id="8354e-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8354e-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8354e-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8354e-116">Error codes</span></span>

<span data-ttu-id="8354e-117">Nach Abschluss der **Remove** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="8354e-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8354e-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8354e-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8354e-119">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8354e-119">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8354e-120">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="8354e-120">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="8354e-121">Der Benutzer hat versucht, eine Eigenschaft zu löschen, die nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="8354e-121">User attempted to delete a property that cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="8354e-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8354e-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8354e-123">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="8354e-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="8354e-124">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="8354e-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="8354e-125">Die angegebene Eigenschaft ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8354e-125">Specified property does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8354e-126">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8354e-126">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8354e-127">Nicht genügend Arbeitsspeicher für die Ausführung dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="8354e-127">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="8354e-128">**wbemErrPropagatedProperty** -142927303552 (0x2147219380)</span><span class="sxs-lookup"><span data-stu-id="8354e-128">**wbemErrPropagatedProperty** - 142927303552 (0x2147219380)</span></span>
</dt> <dd>

<span data-ttu-id="8354e-129">Der Benutzer hat versucht, eine Eigenschaft zu löschen, deren Besitzer er nicht war.</span><span class="sxs-lookup"><span data-stu-id="8354e-129">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="8354e-130">Die Eigenschaft wurde von einer übergeordneten Klasse vererbt.</span><span class="sxs-lookup"><span data-stu-id="8354e-130">The property was inherited from a parent class.</span></span>

</dd> <dt>

<span data-ttu-id="8354e-131">**wbemErrResetToDefault** -2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="8354e-131">**wbemErrResetToDefault** - 2147758082 (0x80043002)</span></span>
</dt> <dd>

<span data-ttu-id="8354e-132">Der Benutzer löschte einen Außerkraftsetzungs Standardwert für die aktuelle Klasse.</span><span class="sxs-lookup"><span data-stu-id="8354e-132">User deleted an override default value for the current class.</span></span> <span data-ttu-id="8354e-133">Der Standardwert für diese Eigenschaft in der übergeordneten Klasse wurde reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8354e-133">The default value for this property in the parent class has been reactivated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8354e-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8354e-134">Remarks</span></span>

<span data-ttu-id="8354e-135">Eigenschaften können nicht aus Klassen Instanzen oder abgeleiteten Klassen mit geerbten Eigenschaften entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8354e-135">Properties cannot be removed from class instances or derived classes with inherited properties.</span></span> <span data-ttu-id="8354e-136">Bei solchen löschversuchen wird ein Fehler ausgegeben, und die-Eigenschaft wird nicht entfernt. die-Eigenschaft wird auf ihren Standardwert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="8354e-136">Such deletion attempts raise an error and the property is not removed; the property is reset to its default value.</span></span>

<span data-ttu-id="8354e-137">Beim Entfernen von Elementen ist es nicht möglich, eine Auflistung zu durchlaufen, denn wenn Sie ein Element aus einer Auflistung entfernen, wird der Auflistungs Zeiger zum nächsten Element verschoben.</span><span class="sxs-lookup"><span data-stu-id="8354e-137">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="8354e-138">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="8354e-138">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8354e-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8354e-139">Examples</span></span>

<span data-ttu-id="8354e-140">Ein Codebeispiel, in dem diese Methode verwendet wird, finden Sie im Thema zu " [**Swap-PropertySet**](swbempropertyset.md) ".</span><span class="sxs-lookup"><span data-stu-id="8354e-140">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="8354e-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8354e-141">Requirements</span></span>



| <span data-ttu-id="8354e-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8354e-142">Requirement</span></span> | <span data-ttu-id="8354e-143">Wert</span><span class="sxs-lookup"><span data-stu-id="8354e-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8354e-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8354e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="8354e-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8354e-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8354e-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8354e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="8354e-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8354e-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8354e-148">Header</span><span class="sxs-lookup"><span data-stu-id="8354e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="8354e-149"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8354e-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8354e-150">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8354e-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="8354e-151"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8354e-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8354e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="8354e-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8354e-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8354e-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8354e-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="8354e-154">CLSID</span></span><br/>                    | <span data-ttu-id="8354e-155">CLSID- \_ Swap-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="8354e-155">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="8354e-156">IID</span><span class="sxs-lookup"><span data-stu-id="8354e-156">IID</span></span><br/>                      | <span data-ttu-id="8354e-157">IID \_ iswbempropertyset</span><span class="sxs-lookup"><span data-stu-id="8354e-157">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="8354e-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8354e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8354e-159">**Swap PropertySet**</span><span class="sxs-lookup"><span data-stu-id="8354e-159">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="8354e-160">**Austauschen von "Swap PropertySet. Add"**</span><span class="sxs-lookup"><span data-stu-id="8354e-160">**SWbemPropertySet.Add**</span></span>](swbempropertyset-add.md)
</dt> </dl>

 

 




