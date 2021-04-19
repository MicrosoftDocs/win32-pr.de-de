---
description: Die subclasses- \_ Methode des "errbemubject"-Objekts gibt ein "errbewbjectset"-Objekt zurück.
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: SWbemObject.Subclasses_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348284"
---
# <a name="swbemobjectsubclasses_-method"></a><span data-ttu-id="f7bef-103">Methode "errbemubject. subclasses" \_</span><span class="sxs-lookup"><span data-stu-id="f7bef-103">SWbemObject.Subclasses\_ method</span></span>

<span data-ttu-id="f7bef-104">Die **subclasses \_** -Methode des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein " [**errbewbjectset**](swbemobjectset.md) "-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f7bef-104">The **Subclasses\_** method of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="f7bef-105">Dieses Objekt ist eine Auflistung von Unterklassen des aktuellen-Objekts, das eine-Klasse sein muss.</span><span class="sxs-lookup"><span data-stu-id="f7bef-105">This object is a collection of subclasses of the current object, which must be a class.</span></span> <span data-ttu-id="f7bef-106">Elemente in der zurückgegebenen Auflistung können mithilfe von Standard Auflistungs Methoden abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f7bef-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="f7bef-107">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="f7bef-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="f7bef-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f7bef-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7bef-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7bef-109">Syntax</span></span>


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f7bef-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7bef-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7bef-111">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f7bef-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7bef-112">Eine ganze Zahl, die bestimmt, wie detailliert der aufzurufende Aufzählung</span><span class="sxs-lookup"><span data-stu-id="f7bef-112">Integer that determines how detailed the call enumerates.</span></span> <span data-ttu-id="f7bef-113">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="f7bef-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="f7bef-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f7bef-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f7bef-115">Erzwingt eine rekursive Enumeration in alle Unterklassen, die von der angegebenen übergeordneten Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f7bef-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="f7bef-116">Die übergeordnete Klasse selbst wird nicht in der-Enumeration zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f7bef-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="f7bef-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="f7bef-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="f7bef-118">Standardwert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="f7bef-118">Default value for this parameter.</span></span> <span data-ttu-id="f7bef-119">Es erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.</span><span class="sxs-lookup"><span data-stu-id="f7bef-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="f7bef-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>WbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="f7bef-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*WbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="f7bef-121">Bewirkt, dass der-Rückruf sofort zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="f7bef-121">Causes the call to return immediately</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="f7bef-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f7bef-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f7bef-123">Bewirkt, dass dieser-Vorgang blockiert wird, bis der-Befehl abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f7bef-123">Causes this call to block until the call has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="f7bef-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="f7bef-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="f7bef-125">Bewirkt, dass WMI zusammen mit der Basisklassen Definition Klassen Änderungs Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f7bef-125">Causes WMI to return class amendment data along with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f7bef-126">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f7bef-126">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7bef-127">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f7bef-127">Typically, this is undefined.</span></span> <span data-ttu-id="f7bef-128">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f7bef-128">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="f7bef-129">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="f7bef-129">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7bef-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7bef-130">Return value</span></span>

<span data-ttu-id="f7bef-131">Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**errbemubjectset**](swbemobjectset.md) -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f7bef-131">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7bef-132">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f7bef-132">Error codes</span></span>

<span data-ttu-id="f7bef-133">Nach dem Abschluss der **Unterklassen \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="f7bef-133">After the completion of the **Subclasses\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f7bef-134">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="f7bef-134">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="f7bef-135">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7bef-135">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="f7bef-136">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f7bef-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f7bef-137">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="f7bef-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f7bef-138">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="f7bef-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="f7bef-139">Die angegebene Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f7bef-139">Specified class did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="f7bef-140">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f7bef-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f7bef-141">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="f7bef-141">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="f7bef-142">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="f7bef-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f7bef-143">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f7bef-143">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7bef-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7bef-144">Remarks</span></span>

<span data-ttu-id="f7bef-145">Es ist kein Fehler, wenn die zurückgegebene Auflistung keine Elemente enthält, wenn keine Unterklassen des aktuellen-Objekts vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f7bef-145">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="f7bef-146">Die **Unterklassen \_** Methode funktioniert nur für Klassen Objekte.</span><span class="sxs-lookup"><span data-stu-id="f7bef-146">The **Subclasses\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7bef-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7bef-147">Requirements</span></span>



| <span data-ttu-id="f7bef-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7bef-148">Requirement</span></span> | <span data-ttu-id="f7bef-149">Wert</span><span class="sxs-lookup"><span data-stu-id="f7bef-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7bef-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7bef-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f7bef-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7bef-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7bef-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7bef-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f7bef-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7bef-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7bef-154">Header</span><span class="sxs-lookup"><span data-stu-id="f7bef-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7bef-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7bef-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7bef-156">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f7bef-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7bef-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f7bef-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f7bef-158">DLL</span><span class="sxs-lookup"><span data-stu-id="f7bef-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7bef-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7bef-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f7bef-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="f7bef-160">CLSID</span></span><br/>                    | <span data-ttu-id="f7bef-161">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="f7bef-161">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="f7bef-162">IID</span><span class="sxs-lookup"><span data-stu-id="f7bef-162">IID</span></span><br/>                      | <span data-ttu-id="f7bef-163">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="f7bef-163">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="f7bef-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7bef-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7bef-165">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="f7bef-165">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="f7bef-166">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="f7bef-166">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




