---
description: 'SWbemServices.AssociatorsOf-Methode: Gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die Endpunkte genannt werden, die einem angegebenen Objekt zugeordnet sind.'
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: SWbemServices.AssociatorsOf-Methode (Wbemdisp.h)
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
ms.openlocfilehash: 95dc8e16939c345b6f885980dd2f1194f180ac5e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103688"
---
# <a name="swbemservicesassociatorsof-method"></a><span data-ttu-id="4746b-103">SWbemServices.AssociatorsOf-Methode</span><span class="sxs-lookup"><span data-stu-id="4746b-103">SWbemServices.AssociatorsOf method</span></span>

<span data-ttu-id="4746b-104">Die **AssociatorsOf-Methode** des [**SWbemServices-Objekts**](swbemservices.md) gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die als Endpunkte bezeichnet werden, die einem angegebenen Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4746b-104">The **AssociatorsOf** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="4746b-105">Diese Methode führt dieselbe Funktion aus wie die ASSOCIATORS OF WQL-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="4746b-105">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="4746b-106">Diese Methode wird standardmäßig im semisynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4746b-106">This method is called in the semisynchronous mode by default.</span></span> <span data-ttu-id="4746b-107">Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)</span><span class="sxs-lookup"><span data-stu-id="4746b-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="4746b-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)</span><span class="sxs-lookup"><span data-stu-id="4746b-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4746b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4746b-109">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4746b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4746b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4746b-111">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="4746b-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="4746b-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4746b-112">Required.</span></span> <span data-ttu-id="4746b-113">Eine Zeichenfolge, die den Objektpfad der Quellklasse oder -instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="4746b-113">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="4746b-114">Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)</span><span class="sxs-lookup"><span data-stu-id="4746b-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="4746b-115">*strAssocClass* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-115">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-116">Eine Zeichenfolge, die eine Zuordnungsklasse enthält.</span><span class="sxs-lookup"><span data-stu-id="4746b-116">String that contains an association class.</span></span> <span data-ttu-id="4746b-117">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte der Quelle über die angegebene Zuordnungsklasse oder eine Klasse zugeordnet werden müssen, die von dieser Zuordnungsklasse abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="4746b-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class that is derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-118">*strResultClass* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-119">Eine Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="4746b-119">String that contains a class name.</span></span> <span data-ttu-id="4746b-120">Wenn angegeben, gibt dieser optionale Parameter an, dass die zurückgegebenen Endpunkte zu der in diesem Parameter angegebenen Klasse gehören oder von ihr abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4746b-120">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-121">*strResultRole* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-121">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-122">Eine Zeichenfolge, die einen Eigenschaftennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="4746b-122">String that contains a property name.</span></span> <span data-ttu-id="4746b-123">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte in ihrer Zuordnung zum Quellobjekt eine bestimmte Rolle spielen müssen.</span><span class="sxs-lookup"><span data-stu-id="4746b-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="4746b-124">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="4746b-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-125">*strRole* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-125">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-126">Zeichenfolge, die einen Eigenschaftennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="4746b-126">String that contains a property name.</span></span> <span data-ttu-id="4746b-127">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quellobjekt teilnehmen müssen, in dem das Quellobjekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="4746b-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="4746b-128">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="4746b-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-129">*bClassesOnly* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-129">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-130">Ein boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle von tatsächlichen Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4746b-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="4746b-131">Dies sind die Klassen, zu denen die Endpunktinstanzen gehören.</span><span class="sxs-lookup"><span data-stu-id="4746b-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="4746b-132">Der Standardwert für diesen Parameter ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="4746b-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-133">*bSchemaOnly* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-133">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-134">Boolescher Wert, der angibt, ob die Abfrage für das Schema und nicht für die Daten gilt.</span><span class="sxs-lookup"><span data-stu-id="4746b-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="4746b-135">Der Standardwert für diesen Parameter ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="4746b-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="4746b-136">Sie kann nur auf **TRUE** festgelegt werden, wenn der *strObjectPath-Parameter* den Objektpfad einer Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="4746b-136">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="4746b-137">Bei Festlegung auf **TRUE** stellen die zurückgegebenen Endpunkte Klassen dar, die der Quellklasse im Schema entsprechend zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4746b-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-138">*strRequiredAssocQualifier* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-138">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-139">Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="4746b-139">String that contains a qualifier name.</span></span> <span data-ttu-id="4746b-140">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte dem Quellobjekt über eine Zuordnungsklasse zugeordnet werden müssen, die den angegebenen Qualifizierer enthält.</span><span class="sxs-lookup"><span data-stu-id="4746b-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-141">*strRequiredQualifier* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-141">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-142">Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="4746b-142">String that contains a qualifier name.</span></span> <span data-ttu-id="4746b-143">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte den angegebenen Qualifizierer enthalten müssen.</span><span class="sxs-lookup"><span data-stu-id="4746b-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-144">*iFlags* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-144">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-145">Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="4746b-145">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="4746b-146">Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately,** der die -Methode im semisynchronen Modus aufruft.</span><span class="sxs-lookup"><span data-stu-id="4746b-146">The default value for this parameter is **wbemFlagReturnImmediately**, which calls the method in the semisynchronous mode.</span></span> <span data-ttu-id="4746b-147">Dieser Parameter kann die folgenden Werte akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="4746b-147">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="4746b-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly( (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="4746b-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="4746b-149">Bewirkt, dass ein vorwärts enumerator zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4746b-149">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="4746b-150">Vorwärts-Enumeratoren sind im Allgemeinen viel schneller und verwenden weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber sie lassen keine Aufrufe von [**SWbemObject.Clone zu. \_**](swbemobject-clone-.md)</span><span class="sxs-lookup"><span data-stu-id="4746b-150">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="4746b-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional( (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="4746b-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4746b-152">Bewirkt, dass WMI Zeiger auf Objekte der Enumeration behält, bis der Client den Enumerator frei gibt.</span><span class="sxs-lookup"><span data-stu-id="4746b-152">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="4746b-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately( (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="4746b-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="4746b-154">Bewirkt, dass der Aufruf sofort zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="4746b-154">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="4746b-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete\*\* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="4746b-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4746b-156">Bewirkt, dass dieser Aufruf blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4746b-156">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="4746b-157">Dieses Flag ruft die -Methode im synchronen Modus auf.</span><span class="sxs-lookup"><span data-stu-id="4746b-157">This flag calls the method in synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="4746b-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers\*\* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="4746b-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="4746b-159">Bewirkt, dass WMI Klassenänderungsdaten zusammen mit der Basisklassendefinition zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="4746b-159">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="4746b-160">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)</span><span class="sxs-lookup"><span data-stu-id="4746b-160">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4746b-161">*objwbemNamedValueSet* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="4746b-161">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4746b-162">In der Regel ist dies nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4746b-162">Typically, this is undefined.</span></span> <span data-ttu-id="4746b-163">Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient.</span><span class="sxs-lookup"><span data-stu-id="4746b-163">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="4746b-164">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="4746b-164">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4746b-165">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4746b-165">Return value</span></span>

<span data-ttu-id="4746b-166">Wenn der Aufruf erfolgreich ist, wird ein [**SWbemObjectSet-Objekt**](swbemobjectset.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4746b-166">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4746b-167">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4746b-167">Error codes</span></span>

<span data-ttu-id="4746b-168">Nach Abschluss der **AssociatorsOf-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="4746b-168">After the completion of the **AssociatorsOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="4746b-169">Eine zurückgegebene Auflistung mit null Elementen ist kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="4746b-169">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="4746b-170">**wbemErrAccessDenied** – 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="4746b-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="4746b-171">Der aktuelle Benutzer verfügt nicht über die Berechtigung, eine oder mehrere der vom Aufruf zurückgegebenen Klassen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4746b-171">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-172">**wbemErrFailed** – 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4746b-172">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4746b-173">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="4746b-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-174">**wbemErrInvalidParameter** – 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="4746b-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4746b-175">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="4746b-175">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-176">**wbemErrOutOfMemory** – 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="4746b-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="4746b-177">Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4746b-177">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4746b-178">**wbemErrNotFound** – 2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="4746b-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="4746b-179">Angefordertes Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="4746b-179">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4746b-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4746b-180">Remarks</span></span>

<span data-ttu-id="4746b-181">Die -Methode ruft die Instanzen verwalteter Ressourcen ab, die einer angegebenen Ressource über eine oder mehrere Zuordnungsklassen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4746b-181">The method retrieves the instances of managed resources that are associated with a specified resource through one or more association classes.</span></span> <span data-ttu-id="4746b-182">Sie geben den Objektpfad für den ursprünglichen Endpunkt an, und AssociatorsOf gibt die verwalteten Ressourcen am entgegengesetzten Endpunkt zurück.</span><span class="sxs-lookup"><span data-stu-id="4746b-182">You provide the object path for the originating endpoint, and AssociatorsOf returns the managed resources at the opposite endpoint.</span></span> <span data-ttu-id="4746b-183">Die AssociatorsOf-Methode führt dieselbe Funktion wie die ASSOCIATORS OF WQL-Abfrage aus.</span><span class="sxs-lookup"><span data-stu-id="4746b-183">The AssociatorsOf method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="4746b-184">Weitere Informationen über die ASSOCIATORS OF WQL-Abfrage, Quellinstanzen und Endpunkte finden Sie unter [ASSOCIATORS OF-Anweisung.](associators-of-statement.md)</span><span class="sxs-lookup"><span data-stu-id="4746b-184">For more information about the ASSOCIATORS OF WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4746b-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4746b-185">Requirements</span></span>



| <span data-ttu-id="4746b-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4746b-186">Requirement</span></span> | <span data-ttu-id="4746b-187">Wert</span><span class="sxs-lookup"><span data-stu-id="4746b-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4746b-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4746b-188">Minimum supported client</span></span><br/> | <span data-ttu-id="4746b-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4746b-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4746b-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4746b-190">Minimum supported server</span></span><br/> | <span data-ttu-id="4746b-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4746b-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4746b-192">Header</span><span class="sxs-lookup"><span data-stu-id="4746b-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="4746b-193"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="4746b-193"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4746b-194">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4746b-194">Type library</span></span><br/>             | <dl> <span data-ttu-id="4746b-195"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4746b-195"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4746b-196">DLL</span><span class="sxs-lookup"><span data-stu-id="4746b-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4746b-197"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4746b-197"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4746b-198">CLSID</span><span class="sxs-lookup"><span data-stu-id="4746b-198">CLSID</span></span><br/>                    | <span data-ttu-id="4746b-199">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="4746b-199">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="4746b-200">IID</span><span class="sxs-lookup"><span data-stu-id="4746b-200">IID</span></span><br/>                      | <span data-ttu-id="4746b-201">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="4746b-201">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="4746b-202">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4746b-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4746b-203">**Swbemservices**</span><span class="sxs-lookup"><span data-stu-id="4746b-203">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="4746b-204">**SWbemObject.Associators\_**</span><span class="sxs-lookup"><span data-stu-id="4746b-204">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="4746b-205">**SWbemObject.AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="4746b-205">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="4746b-206">**SWbemServices.AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="4746b-206">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="4746b-207">**SWbemObject.References\_**</span><span class="sxs-lookup"><span data-stu-id="4746b-207">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="4746b-208">**SWbemServices.ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="4746b-208">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




