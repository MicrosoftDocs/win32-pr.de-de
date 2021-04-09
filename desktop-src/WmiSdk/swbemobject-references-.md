---
description: Die References- \_ Methode des-Objekts von "errbemabject" gibt eine Auflistung aller Zuordnungs Klassen oder-Instanzen zurück, die auf das aktuelle-Objekt verweisen.
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: SWbemObject.References_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.References_
- ISWbemObject.References_
- ISWbemObject.References_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3349ff104a5f0730ee99735a230d265fffd1333f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868587"
---
# <a name="swbemobjectreferences_-method"></a><span data-ttu-id="5d47e-103">Errbemubject. References- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="5d47e-103">SWbemObject.References\_ method</span></span>

<span data-ttu-id="5d47e-104">Die **References \_** -Methode des-Objekts von " [**errbemabject**](swbemobject.md) " gibt eine Auflistung aller Zuordnungs Klassen oder-Instanzen zurück, die auf das aktuelle-Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="5d47e-104">The **References\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of all association classes or instances that refer to the current object.</span></span>

<span data-ttu-id="5d47e-105">Diese Methode führt dieselbe Funktion aus wie die [Verweise der](references-of-statement.md) WQL-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="5d47e-105">This method performs the same function as the [REFERENCES OF](references-of-statement.md) WQL query.</span></span>

<span data-ttu-id="5d47e-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5d47e-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d47e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d47e-107">Syntax</span></span>


```VB
objWbemObjectSet = .References_( _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5d47e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d47e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d47e-109">" *strautclass* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5d47e-109">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-110">Eine Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="5d47e-110">String that contains a class name.</span></span> <span data-ttu-id="5d47e-111">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte der in diesem Parameter angegebenen Klasse angehören oder von dieser abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5d47e-111">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d47e-112">*Rolle "Rolle* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5d47e-112">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-113">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="5d47e-113">String that contains a property name.</span></span> <span data-ttu-id="5d47e-114">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte auf diejenigen beschränkt werden müssen, in denen das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="5d47e-114">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="5d47e-115">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="5d47e-115">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="5d47e-116">*bclassesonly* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5d47e-116">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-117">Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d47e-117">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="5d47e-118">Dabei handelt es sich um die Klassen, zu denen die Zuordnungs Objekte gehören.</span><span class="sxs-lookup"><span data-stu-id="5d47e-118">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="5d47e-119">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="5d47e-119">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5d47e-120">*bschemaonly* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5d47e-120">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-121">Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d47e-121">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="5d47e-122">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="5d47e-122">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="5d47e-123">Sie kann nur auf " **true** " festgelegt werden, wenn das Objekt, für das diese Methode aufgerufen wird, eine Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="5d47e-123">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="5d47e-124">Wenn der Wert auf **true** festgelegt ist, stellt der Satz der zurückgegebenen Endpunkte Klassen dar, die der Quell Klasse im Schema entsprechend zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5d47e-124">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="5d47e-125">" *stringdqualifier* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5d47e-125">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-126">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="5d47e-126">String that contains a qualifier name.</span></span> <span data-ttu-id="5d47e-127">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte den angegebenen Qualifizierer einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="5d47e-127">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="5d47e-128">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5d47e-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-129">Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="5d47e-129">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="5d47e-130">Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately**, der den-Rückruf anweist, sofort zurückzukehren, anstatt zu warten, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5d47e-130">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="5d47e-131">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="5d47e-131">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="5d47e-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="5d47e-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="5d47e-133">Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d47e-133">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="5d47e-134">Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.</span><span class="sxs-lookup"><span data-stu-id="5d47e-134">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="5d47e-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemflagbidirektionale \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5d47e-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5d47e-136">Bewirkt, dass Windows-Verwaltungsinstrumentation (WMI) Zeiger auf Objekte der-Enumeration behält, bis der Client den Enumerator freigibt.</span><span class="sxs-lookup"><span data-stu-id="5d47e-136">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="5d47e-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="5d47e-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="5d47e-138">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d47e-138">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="5d47e-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5d47e-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5d47e-140">Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5d47e-140">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="5d47e-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="5d47e-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="5d47e-142">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5d47e-142">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="5d47e-143">Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="5d47e-143">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5d47e-144">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5d47e-144">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-145">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="5d47e-145">Typically, this is undefined.</span></span> <span data-ttu-id="5d47e-146">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5d47e-146">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="5d47e-147">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="5d47e-147">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d47e-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d47e-148">Return value</span></span>

<span data-ttu-id="5d47e-149">Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**errbemubjectset**](swbemobjectset.md) -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5d47e-149">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5d47e-150">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="5d47e-150">Error codes</span></span>

<span data-ttu-id="5d47e-151">Nach dem Abschluss der **References \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="5d47e-151">After the completion of the **References\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5d47e-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="5d47e-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-153">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5d47e-153">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="5d47e-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5d47e-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-155">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="5d47e-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5d47e-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5d47e-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-157">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="5d47e-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="5d47e-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5d47e-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5d47e-159">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5d47e-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d47e-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d47e-160">Remarks</span></span>

<span data-ttu-id="5d47e-161">Weitere Informationen zu den verweisen der zugeordneten WQL-Abfrage, Quell Instanzen und Zuordnungs Objekte finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="5d47e-161">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d47e-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d47e-162">Requirements</span></span>



| <span data-ttu-id="5d47e-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d47e-163">Requirement</span></span> | <span data-ttu-id="5d47e-164">Wert</span><span class="sxs-lookup"><span data-stu-id="5d47e-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d47e-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d47e-165">Minimum supported client</span></span><br/> | <span data-ttu-id="5d47e-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d47e-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d47e-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d47e-167">Minimum supported server</span></span><br/> | <span data-ttu-id="5d47e-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d47e-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d47e-169">Header</span><span class="sxs-lookup"><span data-stu-id="5d47e-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d47e-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d47e-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d47e-171">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5d47e-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="5d47e-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5d47e-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5d47e-173">DLL</span><span class="sxs-lookup"><span data-stu-id="5d47e-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d47e-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d47e-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5d47e-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="5d47e-175">CLSID</span></span><br/>                    | <span data-ttu-id="5d47e-176">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="5d47e-176">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="5d47e-177">IID</span><span class="sxs-lookup"><span data-stu-id="5d47e-177">IID</span></span><br/>                      | <span data-ttu-id="5d47e-178">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="5d47e-178">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="5d47e-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d47e-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d47e-180">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="5d47e-180">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="5d47e-181">**"Errbemujeject. ASSOCIATORS"\_**</span><span class="sxs-lookup"><span data-stu-id="5d47e-181">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="5d47e-182">**"Taubemservices. associatorsof"**</span><span class="sxs-lookup"><span data-stu-id="5d47e-182">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="5d47e-183">**"Swap Services. referencesto"**</span><span class="sxs-lookup"><span data-stu-id="5d47e-183">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




