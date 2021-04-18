---
description: Die instance- \_ Methode des-Objekts aus dem-Objekt () erstellt einen Enumerator, der die Instanzen des aktuellen Klassen Objekts zurückgibt. Diese Methode implementiert eine einfache Abfrage. Komplexere Abfragen erfordern möglicherweise die Verwendung von SWbemServices.Execquery.
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.tgt_platform: multiple
title: SWbemObject.Instances_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Instances_
- ISWbemObject.Instances_
- ISWbemObject.Instances_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c573c1e94cd473d22483c7b6a2c801c3e6bcb9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350911"
---
# <a name="swbemobjectinstances_-method"></a><span data-ttu-id="e5c73-105">Errbemubject. Instance- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="e5c73-105">SWbemObject.Instances\_ method</span></span>

<span data-ttu-id="e5c73-106">Die **instance \_** - [**Methode des-Objekts aus**](swbemobject.md) dem-Objekt () erstellt einen Enumerator, der die Instanzen des aktuellen Klassen Objekts zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e5c73-106">The **Instances\_** method of the [**SWbemObject**](swbemobject.md) object creates an enumerator that returns the instances of the current class object.</span></span> <span data-ttu-id="e5c73-107">Diese Methode implementiert eine einfache Abfrage.</span><span class="sxs-lookup"><span data-stu-id="e5c73-107">This method implements a simple query.</span></span> <span data-ttu-id="e5c73-108">Komplexere Abfragen erfordern möglicherweise die Verwendung von [**SWbemServices.Execquery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="e5c73-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="e5c73-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e5c73-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c73-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5c73-110">Syntax</span></span>


```VB
objWbemObjectSet = .Instances_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e5c73-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5c73-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c73-112">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e5c73-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c73-113">Eine ganze Zahl, die das Verhalten des Aufrufes bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c73-113">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="e5c73-114">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="e5c73-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="e5c73-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="e5c73-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="e5c73-116">Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e5c73-116">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="e5c73-117">Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.</span><span class="sxs-lookup"><span data-stu-id="e5c73-117">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="e5c73-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemflagbidirektionale \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="e5c73-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="e5c73-119">Bewirkt, dass WMI Zeiger auf Objekte der-Enumeration behält, bis der Client den Enumerator freigibt.</span><span class="sxs-lookup"><span data-stu-id="e5c73-119">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="e5c73-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="e5c73-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="e5c73-121">Standardwert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="e5c73-121">Default value for this parameter.</span></span> <span data-ttu-id="e5c73-122">Dieses Flag bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e5c73-122">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="e5c73-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="e5c73-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="e5c73-124">Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e5c73-124">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="e5c73-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="e5c73-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="e5c73-126">Erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.</span><span class="sxs-lookup"><span data-stu-id="e5c73-126">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="e5c73-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="e5c73-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="e5c73-128">Der Standardwert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="e5c73-128">Default for this parameter.</span></span> <span data-ttu-id="e5c73-129">Dieser Wert erzwingt, dass die Enumeration alle Klassen in der Hierarchie einschließt.</span><span class="sxs-lookup"><span data-stu-id="e5c73-129">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="e5c73-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="e5c73-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="e5c73-131">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e5c73-131">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e5c73-132">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e5c73-132">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c73-133">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="e5c73-133">Typically, this is undefined.</span></span> <span data-ttu-id="e5c73-134">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e5c73-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="e5c73-135">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="e5c73-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c73-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5c73-136">Return value</span></span>

<span data-ttu-id="e5c73-137">Wenn die Methode erfolgreich ist, gibt ein [**errbemubjectset**](swbemobjectset.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e5c73-137">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e5c73-138">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e5c73-138">Error codes</span></span>

<span data-ttu-id="e5c73-139">Nach dem Abschluss der- **Instanzen \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5c73-139">After the completion of the **Instances\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e5c73-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="e5c73-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="e5c73-141">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen von Instanzen der angegebenen Klasse.</span><span class="sxs-lookup"><span data-stu-id="e5c73-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="e5c73-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e5c73-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e5c73-143">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="e5c73-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e5c73-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="e5c73-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="e5c73-145">Die angegebene Klasse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e5c73-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e5c73-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="e5c73-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e5c73-147">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e5c73-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e5c73-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="e5c73-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="e5c73-149">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e5c73-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5c73-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5c73-150">Remarks</span></span>

<span data-ttu-id="e5c73-151">Die **instance \_** -Methode funktioniert nur für Klassen Objekte.</span><span class="sxs-lookup"><span data-stu-id="e5c73-151">The **Instances\_** method only works for class objects.</span></span> <span data-ttu-id="e5c73-152">Es ist kein Fehler, wenn die zurückgegebene Auflistung keine Elemente aufweist.</span><span class="sxs-lookup"><span data-stu-id="e5c73-152">It is not an error for the returned collection to have zero elements.</span></span> <span data-ttu-id="e5c73-153">Das Standardverhalten für diese Methode ist aufgrund des *IFlags* -Standardwerts **wbemFlagReturnImmediately** [*SemiSynchron*](gloss-s.md) .</span><span class="sxs-lookup"><span data-stu-id="e5c73-153">The default behavior for this method is [*semisynchronous*](gloss-s.md) because of the default *IFlags* value **wbemFlagReturnImmediately**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c73-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5c73-154">Requirements</span></span>



| <span data-ttu-id="e5c73-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5c73-155">Requirement</span></span> | <span data-ttu-id="e5c73-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e5c73-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c73-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5c73-157">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c73-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5c73-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5c73-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5c73-159">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c73-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5c73-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5c73-161">Header</span><span class="sxs-lookup"><span data-stu-id="e5c73-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5c73-162"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c73-162"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5c73-163">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e5c73-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="e5c73-164"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e5c73-164"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e5c73-165">DLL</span><span class="sxs-lookup"><span data-stu-id="e5c73-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5c73-166"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5c73-166"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5c73-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="e5c73-167">CLSID</span></span><br/>                    | <span data-ttu-id="e5c73-168">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="e5c73-168">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="e5c73-169">IID</span><span class="sxs-lookup"><span data-stu-id="e5c73-169">IID</span></span><br/>                      | <span data-ttu-id="e5c73-170">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="e5c73-170">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="e5c73-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5c73-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c73-172">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="e5c73-172">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="e5c73-173">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="e5c73-173">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




