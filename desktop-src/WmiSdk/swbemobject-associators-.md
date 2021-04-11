---
description: Die ASSOCIATORS- \_ Methode des-Objekts von "errberobject" gibt eine Auflistung von-Objekten (Klassen oder Instanzen) zurück, die dem aktuellen-Objekt zugeordnet sind.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: SWbemObject.Associators_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1f9ff4536936661ece54b5bff29e500ce6e98d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960435"
---
# <a name="swbemobjectassociators_-method"></a><span data-ttu-id="c001d-103">Errbemubject. ASSOCIATORS- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="c001d-103">SWbemObject.Associators\_ method</span></span>

<span data-ttu-id="c001d-104">Die **ASSOCIATORS \_** -Methode des-Objekts von " [**errberobject**](swbemobject.md) " gibt eine Auflistung von-Objekten (Klassen oder Instanzen) zurück, die dem aktuellen-Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c001d-104">The **Associators\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="c001d-105">Diese zurückgegebenen Objekte werden als Endpunkte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c001d-105">These returned objects are called endpoints.</span></span> <span data-ttu-id="c001d-106">Diese Methode führt die gleiche Funktion aus, die die assoziatoren der WQL-Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="c001d-106">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="c001d-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c001d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c001d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c001d-108">Syntax</span></span>


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c001d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c001d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c001d-110">*strassocclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-110">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-111">Eine Zeichenfolge, die eine Association-Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="c001d-111">String that contains an association class.</span></span> <span data-ttu-id="c001d-112">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte mit der Quelle über die angegebene Zuordnungs Klasse oder eine von dieser Zuordnungs Klasse abgeleitete Klasse verknüpft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c001d-112">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-113">" *strautclass* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-114">Eine Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c001d-114">String that contains a class name.</span></span> <span data-ttu-id="c001d-115">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte der in diesem Parameter angegebenen Klasse angehören oder von dieser abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c001d-115">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-116">" *stringetrole* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-116">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-117">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c001d-117">String that contains a property name.</span></span> <span data-ttu-id="c001d-118">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quell Objekt spielen müssen.</span><span class="sxs-lookup"><span data-stu-id="c001d-118">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="c001d-119">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="c001d-119">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-120">*Rolle "Rolle* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-120">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-121">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c001d-121">String that contains a property name.</span></span> <span data-ttu-id="c001d-122">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quell Objekt teilnehmen müssen, in dem das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="c001d-122">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="c001d-123">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="c001d-123">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-124">*bclassesonly* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-124">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-125">Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c001d-125">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="c001d-126">Dabei handelt es sich um die Klassen, zu denen die Endpunkt Instanzen gehören.</span><span class="sxs-lookup"><span data-stu-id="c001d-126">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="c001d-127">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c001d-127">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-128">*bschemaonly* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-128">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-129">Dies ist ein boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c001d-129">This is a Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="c001d-130">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c001d-130">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="c001d-131">Sie kann nur auf " **true** " festgelegt werden, wenn das Objekt, für das diese Methode aufgerufen wird, eine Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="c001d-131">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="c001d-132">Wenn der Wert auf **true** festgelegt ist, stellen die Menge der zurückgegebenen Endpunkte Klassen dar, die entsprechend der Quell Klasse im Schema zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c001d-132">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-133">"otrequirements *dassocqualifizierer* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-133">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-134">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c001d-134">String that contains a qualifier name.</span></span> <span data-ttu-id="c001d-135">Dieser Parameter gibt, sofern angegeben, an, dass die zurückgegebenen Endpunkte mit dem Quell Objekt über eine Association-Klasse verknüpft werden müssen, die den angegebenen Qualifizierer einschließt.</span><span class="sxs-lookup"><span data-stu-id="c001d-135">This parameter, if specified, indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-136">" *stringdqualifier* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-136">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-137">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c001d-137">String that contains a qualifier name.</span></span> <span data-ttu-id="c001d-138">Dieser Parameter gibt, sofern angegeben, an, dass die zurückgegebenen Endpunkte den angegebenen Qualifizierer einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="c001d-138">This parameter, if specified, indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-139">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-139">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-140">Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="c001d-140">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="c001d-141">Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately**, der den-Rückruf anweist, sofort zurückzukehren, anstatt zu warten, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c001d-141">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="c001d-142">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c001d-142">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="c001d-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="c001d-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="c001d-144">Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c001d-144">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="c001d-145">Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.</span><span class="sxs-lookup"><span data-stu-id="c001d-145">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="c001d-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemflagbidirektionale \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c001d-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c001d-147">Bewirkt, dass WMI Zeiger auf Objekte der-Enumeration behält, bis der Client den Enumerator freigibt.</span><span class="sxs-lookup"><span data-stu-id="c001d-147">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="c001d-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="c001d-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="c001d-149">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c001d-149">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="c001d-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c001d-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c001d-151">Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c001d-151">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c001d-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="c001d-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c001d-153">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c001d-153">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="c001d-154">Durch einschließen dieses Flags ist der lokalisierte Beschreibungs-qualifizierertext für Klassen, Eigenschaften und Methoden verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c001d-154">Including this flag makes the localized description qualifier text available for classes, properties and methods.</span></span> <span data-ttu-id="c001d-155">Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="c001d-155">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c001d-156">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c001d-156">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c001d-157">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c001d-157">Typically, this is undefined.</span></span> <span data-ttu-id="c001d-158">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c001d-158">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="c001d-159">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="c001d-159">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c001d-160">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c001d-160">Return value</span></span>

<span data-ttu-id="c001d-161">Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**errbemubjectset**](swbemobjectset.md) -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c001d-161">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c001d-162">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c001d-162">Error codes</span></span>

<span data-ttu-id="c001d-163">Nach Abschluss der **ASSOCIATORS \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="c001d-163">After completion of the **Associators\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c001d-164">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="c001d-164">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c001d-165">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die vom-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c001d-165">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-166">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c001d-166">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c001d-167">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c001d-167">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-168">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c001d-168">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c001d-169">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c001d-169">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c001d-170">**wbemErrOutOfMemory** -2147749894</span><span class="sxs-lookup"><span data-stu-id="c001d-170">**wbemErrOutOfMemory** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="c001d-171">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c001d-171">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c001d-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c001d-172">Remarks</span></span>

<span data-ttu-id="c001d-173">Weitere Informationen zu den assoziatoren der zugeordneten WQL-Abfrage, Quell Instanzen und Endpunkte finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="c001d-173">For more information about the ASSOCIATORS OF associated WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c001d-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c001d-174">Requirements</span></span>



| <span data-ttu-id="c001d-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c001d-175">Requirement</span></span> | <span data-ttu-id="c001d-176">Wert</span><span class="sxs-lookup"><span data-stu-id="c001d-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c001d-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c001d-177">Minimum supported client</span></span><br/> | <span data-ttu-id="c001d-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c001d-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c001d-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c001d-179">Minimum supported server</span></span><br/> | <span data-ttu-id="c001d-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c001d-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c001d-181">Header</span><span class="sxs-lookup"><span data-stu-id="c001d-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="c001d-182"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c001d-182"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c001d-183">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c001d-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="c001d-184"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c001d-184"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c001d-185">DLL</span><span class="sxs-lookup"><span data-stu-id="c001d-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c001d-186"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c001d-186"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c001d-187">CLSID</span><span class="sxs-lookup"><span data-stu-id="c001d-187">CLSID</span></span><br/>                    | <span data-ttu-id="c001d-188">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="c001d-188">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c001d-189">IID</span><span class="sxs-lookup"><span data-stu-id="c001d-189">IID</span></span><br/>                      | <span data-ttu-id="c001d-190">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="c001d-190">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c001d-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c001d-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c001d-192">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="c001d-192">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="c001d-193">**"Errbemubject. References"\_**</span><span class="sxs-lookup"><span data-stu-id="c001d-193">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="c001d-194">**"Taubemservices. associatorsof"**</span><span class="sxs-lookup"><span data-stu-id="c001d-194">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="c001d-195">**"Swap Services. referencesto"**</span><span class="sxs-lookup"><span data-stu-id="c001d-195">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




