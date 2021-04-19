---
description: Gibt eine Auflistung von-Objekten (Klassen oder Instanzen) zurück, die als Endpunkte bezeichnet werden, die einem angegebenen Objekt zugeordnet sind.
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: "' Swap Services. associatorsof '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0208ef23158d71a5174fcb6759acba1d64bd09a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362277"
---
# <a name="swbemservicesassociatorsof-method"></a><span data-ttu-id="44c90-103">Methode "Swap Services. associatorsof"</span><span class="sxs-lookup"><span data-stu-id="44c90-103">SWbemServices.AssociatorsOf method</span></span>

<span data-ttu-id="44c90-104">Die **associatorsof** -Methode des [**Swap Services**](swbemservices.md) -Objekts gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die als Endpunkte bezeichnet werden, die einem angegebenen Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="44c90-104">The **AssociatorsOf** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="44c90-105">Diese Methode führt die gleiche Funktion aus, die die assoziatoren der WQL-Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="44c90-105">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="44c90-106">Diese Methode wird standardmäßig im semisynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="44c90-106">This method is called in the semisynchronous mode by default.</span></span> <span data-ttu-id="44c90-107">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="44c90-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="44c90-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="44c90-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="44c90-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="44c90-109">Syntax</span></span>


```VB
objWbemObjectSet = .AssociatorsOf( _
  ByVal strObjectPath, _
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



## <a name="parameters"></a><span data-ttu-id="44c90-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="44c90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44c90-111">*strobjectpath*</span><span class="sxs-lookup"><span data-stu-id="44c90-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="44c90-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="44c90-112">Required.</span></span> <span data-ttu-id="44c90-113">Eine Zeichenfolge, die den Objekt Pfad der Quell Klasse oder-Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="44c90-113">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="44c90-114">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="44c90-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c90-115">*strassocclass* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-115">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-116">Eine Zeichenfolge, die eine Association-Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="44c90-116">String that contains an association class.</span></span> <span data-ttu-id="44c90-117">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte mit der Quelle über die angegebene Zuordnungs Klasse oder eine Klasse, die von dieser Zuordnungs Klasse abgeleitet ist, verknüpft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="44c90-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class that is derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-118">" *strautclass* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-119">Eine Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="44c90-119">String that contains a class name.</span></span> <span data-ttu-id="44c90-120">Wenn angegeben, gibt dieser optionale Parameter an, dass die zurückgegebenen Endpunkte zu der in diesem Parameter angegebenen Klasse gehören bzw. davon abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="44c90-120">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-121">" *stringetrole* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-121">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-122">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="44c90-122">String that contains a property name.</span></span> <span data-ttu-id="44c90-123">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quell Objekt spielen müssen.</span><span class="sxs-lookup"><span data-stu-id="44c90-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="44c90-124">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="44c90-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-125">*Rolle "Rolle* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-125">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-126">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="44c90-126">String that contains a property name.</span></span> <span data-ttu-id="44c90-127">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quell Objekt teilnehmen müssen, in dem das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="44c90-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="44c90-128">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="44c90-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-129">*bclassesonly* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-129">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-130">Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="44c90-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="44c90-131">Dabei handelt es sich um die Klassen, zu denen die Endpunkt Instanzen gehören.</span><span class="sxs-lookup"><span data-stu-id="44c90-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="44c90-132">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="44c90-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-133">*bschemaonly* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-133">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-134">Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="44c90-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="44c90-135">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="44c90-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="44c90-136">Sie kann nur auf " **true** " festgelegt werden, wenn der *strobjectpath* -Parameter den Objekt Pfad einer Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="44c90-136">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="44c90-137">Wenn der Wert auf **true** festgelegt ist, stellen die zurückgegebenen Endpunkte Klassen dar, die entsprechend der Quell Klasse im Schema zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="44c90-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-138">"otrequirements *dassocqualifizierer* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-138">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-139">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="44c90-139">String that contains a qualifier name.</span></span> <span data-ttu-id="44c90-140">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte über eine Association-Klasse, die den angegebenen Qualifizierer enthält, dem Quell Objekt zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="44c90-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-141">" *stringdqualifier* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-141">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-142">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="44c90-142">String that contains a qualifier name.</span></span> <span data-ttu-id="44c90-143">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte den angegebenen Qualifizierer einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="44c90-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-144">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-144">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-145">Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="44c90-145">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="44c90-146">Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately**, der die-Methode im semisynchronen Modus aufruft.</span><span class="sxs-lookup"><span data-stu-id="44c90-146">The default value for this parameter is **wbemFlagReturnImmediately**, which calls the method in the semisynchronous mode.</span></span> <span data-ttu-id="44c90-147">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="44c90-147">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="44c90-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="44c90-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="44c90-149">Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="44c90-149">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="44c90-150">Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.</span><span class="sxs-lookup"><span data-stu-id="44c90-150">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="44c90-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemflagbidirektionale \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="44c90-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="44c90-152">Bewirkt, dass WMI Zeiger auf Objekte der-Enumeration behält, bis der Client den Enumerator freigibt.</span><span class="sxs-lookup"><span data-stu-id="44c90-152">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="44c90-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="44c90-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="44c90-154">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="44c90-154">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="44c90-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="44c90-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="44c90-156">Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="44c90-156">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="44c90-157">Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="44c90-157">This flag calls the method in synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="44c90-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="44c90-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="44c90-159">Bewirkt, dass WMI zusammen mit der Basisklassen Definition Klassen Änderungs Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="44c90-159">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="44c90-160">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="44c90-160">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="44c90-161">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="44c90-161">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44c90-162">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="44c90-162">Typically, this is undefined.</span></span> <span data-ttu-id="44c90-163">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="44c90-163">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="44c90-164">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="44c90-164">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44c90-165">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44c90-165">Return value</span></span>

<span data-ttu-id="44c90-166">Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**errbemubjectset**](swbemobjectset.md) -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44c90-166">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44c90-167">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="44c90-167">Error codes</span></span>

<span data-ttu-id="44c90-168">Nach dem Abschluss der **associatorsof** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="44c90-168">After the completion of the **AssociatorsOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="44c90-169">Eine zurückgegebene Auflistung mit 0 (null) Elementen ist kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="44c90-169">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="44c90-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="44c90-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="44c90-171">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="44c90-171">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-172">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="44c90-172">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="44c90-173">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="44c90-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="44c90-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="44c90-175">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="44c90-175">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="44c90-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="44c90-177">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="44c90-177">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="44c90-178">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="44c90-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="44c90-179">Das angeforderte Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="44c90-179">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44c90-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44c90-180">Remarks</span></span>

<span data-ttu-id="44c90-181">Die-Methode ruft die Instanzen verwalteter Ressourcen, die einer angegebenen Ressource zugeordnet sind, über eine oder mehrere Zuordnungs Klassen ab.</span><span class="sxs-lookup"><span data-stu-id="44c90-181">The method retrieves the instances of managed resources that are associated with a specified resource through one or more association classes.</span></span> <span data-ttu-id="44c90-182">Sie geben den Objekt Pfad für den ursprünglichen Endpunkt an, und associatorsof gibt die verwalteten Ressourcen am gegenüberliegenden Endpunkt zurück.</span><span class="sxs-lookup"><span data-stu-id="44c90-182">You provide the object path for the originating endpoint, and AssociatorsOf returns the managed resources at the opposite endpoint.</span></span> <span data-ttu-id="44c90-183">Die associatorsof-Methode führt die gleiche Funktion aus, die die assoziatoren der WQL-Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="44c90-183">The AssociatorsOf method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="44c90-184">Weitere Informationen zu den assoziatoren von WQL-Abfragen, Quell Instanzen und Endpunkten finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="44c90-184">For more information about the ASSOCIATORS OF WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44c90-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44c90-185">Requirements</span></span>



| <span data-ttu-id="44c90-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44c90-186">Requirement</span></span> | <span data-ttu-id="44c90-187">Wert</span><span class="sxs-lookup"><span data-stu-id="44c90-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44c90-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44c90-188">Minimum supported client</span></span><br/> | <span data-ttu-id="44c90-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44c90-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44c90-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44c90-190">Minimum supported server</span></span><br/> | <span data-ttu-id="44c90-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44c90-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44c90-192">Header</span><span class="sxs-lookup"><span data-stu-id="44c90-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="44c90-193"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="44c90-193"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="44c90-194">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="44c90-194">Type library</span></span><br/>             | <dl> <span data-ttu-id="44c90-195"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="44c90-195"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="44c90-196">DLL</span><span class="sxs-lookup"><span data-stu-id="44c90-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44c90-197"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44c90-197"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="44c90-198">CLSID</span><span class="sxs-lookup"><span data-stu-id="44c90-198">CLSID</span></span><br/>                    | <span data-ttu-id="44c90-199">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="44c90-199">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="44c90-200">IID</span><span class="sxs-lookup"><span data-stu-id="44c90-200">IID</span></span><br/>                      | <span data-ttu-id="44c90-201">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="44c90-201">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="44c90-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44c90-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c90-203">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="44c90-203">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="44c90-204">**"Errbemujeject. ASSOCIATORS"\_**</span><span class="sxs-lookup"><span data-stu-id="44c90-204">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="44c90-205">**"Errbemubject. associatorsasync"\_**</span><span class="sxs-lookup"><span data-stu-id="44c90-205">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="44c90-206">**Swap Services. associatorsofasync**</span><span class="sxs-lookup"><span data-stu-id="44c90-206">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="44c90-207">**"Errbemubject. References"\_**</span><span class="sxs-lookup"><span data-stu-id="44c90-207">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="44c90-208">**"Swap Services. referencesto"**</span><span class="sxs-lookup"><span data-stu-id="44c90-208">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




