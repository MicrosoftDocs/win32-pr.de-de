---
description: Gibt eine Auflistung aller Zuordnungs Klassen oder-Instanzen zurück, die auf eine bestimmte Quell Klasse oder Instanz verweisen.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: Methode ' Swap Services. referencesto ' (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73addea189815d1594d0963fbdd6e20c562b3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131913"
---
# <a name="swbemservicesreferencesto-method"></a><span data-ttu-id="0fb42-103">Methode ' Swap Services. referencesto '</span><span class="sxs-lookup"><span data-stu-id="0fb42-103">SWbemServices.ReferencesTo method</span></span>

<span data-ttu-id="0fb42-104">Die **referencesto** -Methode des [**Swap Services**](swbemservices.md) -Objekts gibt eine Auflistung aller Zuordnungs Klassen oder-Instanzen zurück, die auf eine bestimmte Quell Klasse oder Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="0fb42-104">The **ReferencesTo** method of the [**SWbemServices**](swbemservices.md) object returns a collection of all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="0fb42-105">Diese Methode führt die gleiche Funktion aus, die die [Verweise der](references-of-statement.md) WQL-Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fb42-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="0fb42-106">Diese Methode wird im semisynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0fb42-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="0fb42-107">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0fb42-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="0fb42-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0fb42-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb42-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fb42-109">Syntax</span></span>


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0fb42-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fb42-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb42-111">*strobjectpath*</span><span class="sxs-lookup"><span data-stu-id="0fb42-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="0fb42-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb42-112">Required.</span></span> <span data-ttu-id="0fb42-113">Eine Zeichenfolge, die den Objekt Pfad der Quelle für diese Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="0fb42-113">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="0fb42-114">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="0fb42-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-115">" *strautclass* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="0fb42-115">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-116">Eine Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="0fb42-116">String that contains a class name.</span></span> <span data-ttu-id="0fb42-117">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte der in diesem Parameter angegebenen Klasse angehören oder von dieser abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0fb42-117">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-118">*Rolle "Rolle* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="0fb42-118">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-119">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="0fb42-119">String that contains a property name.</span></span> <span data-ttu-id="0fb42-120">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte auf diejenigen beschränkt werden müssen, in denen das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="0fb42-120">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="0fb42-121">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="0fb42-121">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-122">*bclassesonly* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="0fb42-122">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-123">Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fb42-123">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="0fb42-124">Dabei handelt es sich um die Klassen, zu denen die Zuordnungs Objekte gehören.</span><span class="sxs-lookup"><span data-stu-id="0fb42-124">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="0fb42-125">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="0fb42-125">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-126">*bschemaonly* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="0fb42-126">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-127">Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fb42-127">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="0fb42-128">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="0fb42-128">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="0fb42-129">Sie kann nur auf " **true** " festgelegt werden, wenn der *strobjectpath* -Parameter den Objekt Pfad einer Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="0fb42-129">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="0fb42-130">Wenn der Wert auf **true** festgelegt ist, stellt der Satz der zurückgegebenen Endpunkte Klassen dar, die der Quell Klasse im Schema entsprechend zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0fb42-130">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-131">" *stringdqualifier* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="0fb42-131">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-132">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="0fb42-132">String that contains a qualifier name.</span></span> <span data-ttu-id="0fb42-133">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte den angegebenen Qualifizierer einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="0fb42-133">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-134">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="0fb42-134">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-135">Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="0fb42-135">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="0fb42-136">Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately**, der den-Rückruf anweist, sofort zurückzukehren, anstatt zu warten, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0fb42-136">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="0fb42-137">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="0fb42-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="0fb42-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="0fb42-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="0fb42-139">Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0fb42-139">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="0fb42-140">Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.</span><span class="sxs-lookup"><span data-stu-id="0fb42-140">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="0fb42-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemflagbidirektionale \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0fb42-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0fb42-142">Bewirkt, dass Windows-Verwaltungsinstrumentation (WMI) Zeiger auf Objekte der-Enumeration behält, bis der Client den Enumerator freigibt.</span><span class="sxs-lookup"><span data-stu-id="0fb42-142">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="0fb42-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="0fb42-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="0fb42-144">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0fb42-144">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="0fb42-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0fb42-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0fb42-146">Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0fb42-146">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="0fb42-147">Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0fb42-147">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="0fb42-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="0fb42-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="0fb42-149">Bewirkt, dass WMI zusammen mit der Basisklassen Definition Klassen Änderungs Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0fb42-149">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="0fb42-150">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="0fb42-150">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0fb42-151">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="0fb42-151">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-152">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="0fb42-152">Typically, this is undefined.</span></span> <span data-ttu-id="0fb42-153">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0fb42-153">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="0fb42-154">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="0fb42-154">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fb42-155">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fb42-155">Return value</span></span>

<span data-ttu-id="0fb42-156">Wenn die Methode erfolgreich ist, gibt die Methode ein " [**errbewbjectset**](swbemobjectset.md) "-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0fb42-156">If the method is successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0fb42-157">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0fb42-157">Error codes</span></span>

<span data-ttu-id="0fb42-158">Nach dem Abschluss der **referencesto** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="0fb42-158">After the completion of the **ReferencesTo** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="0fb42-159">Eine zurückgegebene Auflistung mit 0 (null) Elementen ist kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="0fb42-159">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="0fb42-160">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="0fb42-160">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-161">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0fb42-161">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-162">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0fb42-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-163">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="0fb42-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-164">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="0fb42-164">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-165">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="0fb42-165">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-166">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0fb42-166">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-167">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0fb42-167">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0fb42-168">**wbemflaguseamendedqualifizierer** -131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="0fb42-168">**wbemFlagUseAmendedQualifiers** - 131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="0fb42-169">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0fb42-169">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fb42-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fb42-170">Remarks</span></span>

<span data-ttu-id="0fb42-171">Weitere Informationen zu den verweisen der zugeordneten WQL-Abfrage, Quell Instanzen und Zuordnungs Objekte finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0fb42-171">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb42-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fb42-172">Requirements</span></span>



| <span data-ttu-id="0fb42-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fb42-173">Requirement</span></span> | <span data-ttu-id="0fb42-174">Wert</span><span class="sxs-lookup"><span data-stu-id="0fb42-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb42-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fb42-175">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb42-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fb42-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fb42-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fb42-177">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb42-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fb42-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fb42-179">Header</span><span class="sxs-lookup"><span data-stu-id="0fb42-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fb42-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fb42-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0fb42-181">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0fb42-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="0fb42-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0fb42-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0fb42-183">DLL</span><span class="sxs-lookup"><span data-stu-id="0fb42-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fb42-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fb42-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0fb42-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="0fb42-185">CLSID</span></span><br/>                    | <span data-ttu-id="0fb42-186">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="0fb42-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="0fb42-187">IID</span><span class="sxs-lookup"><span data-stu-id="0fb42-187">IID</span></span><br/>                      | <span data-ttu-id="0fb42-188">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="0fb42-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="0fb42-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fb42-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb42-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="0fb42-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="0fb42-191">**"Errbemujeject. ASSOCIATORS"\_**</span><span class="sxs-lookup"><span data-stu-id="0fb42-191">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="0fb42-192">**"Errbemubject. References"\_**</span><span class="sxs-lookup"><span data-stu-id="0fb42-192">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="0fb42-193">**"Taubemservices. associatorsof"**</span><span class="sxs-lookup"><span data-stu-id="0fb42-193">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> </dl>

 

 




