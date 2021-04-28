---
description: 'SWbemServices.AssociatorsOfAsync-Methode: Gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die Endpunkte genannt werden, die einem angegebenen Objekt zugeordnet sind.'
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: SWbemServices.AssociatorsOfAsync-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4b16eed97c891b4b4f5bd283496868d99f9e0fbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103668"
---
# <a name="swbemservicesassociatorsofasync-method"></a><span data-ttu-id="ec2a1-103">SWbemServices.AssociatorsOfAsync-Methode</span><span class="sxs-lookup"><span data-stu-id="ec2a1-103">SWbemServices.AssociatorsOfAsync method</span></span>

<span data-ttu-id="ec2a1-104">Die **AssociatorsOfAsync-Methode** des [**SWbemServices-Objekts**](swbemservices.md) gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die Endpunkte genannt werden, die einem angegebenen Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-104">The **AssociatorsOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="ec2a1-105">Der Aufruf von **AssociatorsOfAsync** wird sofort zurückgegeben, und die Ergebnisse und der Status werden dem Aufrufer über Ereignisse zurückgegeben, die an die Senke übermittelt werden, die in *objWbemSink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-105">The call to **AssociatorsOfAsync** returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="ec2a1-106">Um jedes zurückgegebene Objekt zu verarbeiten, erstellen Sie einen *objWbemSink*. [**OnObjectReady-Ereignishandler.**](swbemsink-onobjectready.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event handler.</span></span>

<span data-ttu-id="ec2a1-107">Nachdem alle Objekte eingetroffen sind, erfolgt die Verarbeitung im *objWbemSink*. [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-107">After all the objects arrive, processing is done in the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span> <span data-ttu-id="ec2a1-108">Diese Methode führt dieselbe Funktion aus, die von der ASSOCIATORS OF WQL-Abfrage ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span> <span data-ttu-id="ec2a1-109">Weitere Informationen zum Erstellen einer Senke finden Sie unter [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-109">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="ec2a1-110">Die -Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-110">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="ec2a1-111">Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="ec2a1-112">Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-112">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2a1-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec2a1-113">Syntax</span></span>


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
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
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ec2a1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec2a1-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec2a1-115">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="ec2a1-115">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="ec2a1-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-116">Required.</span></span> <span data-ttu-id="ec2a1-117">Objektsenke, die die Objekte asynchron empfängt.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-117">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="ec2a1-118">Erstellen Sie ein [**SWbemSink-Objekt,**](swbemsink.md) um die Objekte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-118">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-119">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="ec2a1-119">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="ec2a1-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-120">Required.</span></span> <span data-ttu-id="ec2a1-121">Zeichenfolge, die den Objektpfad der Quellklasse oder -instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-121">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="ec2a1-122">Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-122">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-123">*strAssocClass* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-123">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-124">Zeichenfolge, die eine Zuordnungsklasse enthält.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-124">String that contains an association class.</span></span> <span data-ttu-id="ec2a1-125">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte der Quelle über die angegebene Zuordnungsklasse oder eine von dieser Zuordnungsklasse abgeleitete Klasse zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-125">When specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-126">*strResultClass* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-126">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-127">Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-127">String that contains a class name.</span></span> <span data-ttu-id="ec2a1-128">Falls angegeben, gibt dieser optionale Parameter an, dass die zurückgegebenen Endpunkte zu der in diesem Parameter angegebenen Klasse gehören oder von dieser abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-128">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-129">*strResultRole* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-129">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-130">Zeichenfolge, die einen Eigenschaftennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-130">String that contains a property name.</span></span> <span data-ttu-id="ec2a1-131">Falls angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quellobjekt spielen müssen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-131">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="ec2a1-132">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-132">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-133">*strRole* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-133">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-134">Zeichenfolge, die einen Eigenschaftennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-134">String that contains a property name.</span></span> <span data-ttu-id="ec2a1-135">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quellobjekt teilnehmen müssen, in dem das Quellobjekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-135">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="ec2a1-136">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-136">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-137">*bClassesOnly* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-137">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-138">Ein boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle von tatsächlichen Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-138">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="ec2a1-139">Dies sind die Klassen, zu denen die Endpunktinstanzen gehören.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-139">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="ec2a1-140">Der Standardwert für diesen Parameter ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-140">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-141">*bSchemaOnly* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-141">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-142">Boolescher Wert, der angibt, ob die Abfrage für das Schema und nicht für die Daten gilt.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-142">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="ec2a1-143">Der Standardwert für diesen Parameter ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-143">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="ec2a1-144">Sie kann nur auf **TRUE** festgelegt werden, wenn der *strObjectPath-Parameter* den Objektpfad einer Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-144">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="ec2a1-145">Bei True **stellen die** zurückgegebenen Endpunkte Klassen dar, die der Quellklasse im Schema entsprechend zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-145">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-146">*strRequiredAssocQualifier* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-146">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-147">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-147">String that contains a qualifier name.</span></span> <span data-ttu-id="ec2a1-148">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte dem Quellobjekt über eine Zuordnungsklasse zugeordnet werden müssen, die den angegebenen Qualifizierer enthält.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-148">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-149">*strRequiredQualifier* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-149">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-150">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-150">String that contains a qualifier name.</span></span> <span data-ttu-id="ec2a1-151">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte den angegebenen Qualifizierer enthalten müssen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-151">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-152">*iFlags* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-152">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-153">Eine ganze Zahl, die die zusätzlichen Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-153">Integer that specifies the additional flags to the operation.</span></span> <span data-ttu-id="ec2a1-154">Der Standardwert für diesen Parameter ist **wbemFlagDontSendStatus.**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-154">The default for this parameter is **wbemFlagDontSendStatus**.</span></span> <span data-ttu-id="ec2a1-155">Dieser Parameter kann die folgenden Werte akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-155">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="ec2a1-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus\*\* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="ec2a1-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="ec2a1-157">Bewirkt, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-157">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="ec2a1-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus\*\* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="ec2a1-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ec2a1-159">Verhindert, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-159">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="ec2a1-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers\*\* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="ec2a1-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="ec2a1-161">Bewirkt, dass WMI Klassenänderungsdaten zusammen mit der Basisklassendefinition zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-161">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="ec2a1-162">Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-162">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ec2a1-163">*objWbemNamedValueSet* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-163">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-164">In der Regel ist dies nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-164">Typically, this is undefined.</span></span> <span data-ttu-id="ec2a1-165">Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung wartet.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-165">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="ec2a1-166">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-166">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-167">*objWbemAsyncContext* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="ec2a1-167">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-168">Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-168">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="ec2a1-169">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mit derselben Objektsenke vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-169">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="ec2a1-170">Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-170">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="ec2a1-171">Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode**](swbemnamedvalueset-item.md) extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-171">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="ec2a1-172">Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-172">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec2a1-173">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec2a1-173">Return value</span></span>

<span data-ttu-id="ec2a1-174">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-174">This method does not return a value.</span></span> <span data-ttu-id="ec2a1-175">Bei Erfolg empfängt die Senke ein [**OnObjectReady-Ereignis**](swbemsink-onobjectready.md) pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-175">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="ec2a1-176">Nach der letzten Instanz empfängt die Objektsenke ein [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-176">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ec2a1-177">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ec2a1-177">Error codes</span></span>

<span data-ttu-id="ec2a1-178">Nach Abschluss der **AssociatorsOfAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-178">After the completion of the **AssociatorsOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ec2a1-179">**wbemErrAccessDenied** – 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-180">Der aktuelle Benutzer verfügt nicht über die Berechtigung, eine oder mehrere der vom Aufruf zurückgegebenen Klassen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-180">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-181">**wbemErrFailed** – 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-181">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-182">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-182">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-183">**wbemErrInvalidParameter** – 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-184">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-184">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-185">**wbemErrOutOfMemory** – 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-186">Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-186">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a1-187">**wbemErrNotFound** – 2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="ec2a1-188">Angefordertes Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-188">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec2a1-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec2a1-189">Remarks</span></span>

<span data-ttu-id="ec2a1-190">Dieser Aufruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-190">This call returns immediately.</span></span> <span data-ttu-id="ec2a1-191">Die angeforderten Objekte und der Status werden an den Aufrufer über Rückrufe zurückgegeben, die an die in *objWbemSink* angegebene Senke übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-191">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="ec2a1-192">Um jedes Objekt nach der Rückgabe zu verarbeiten, erstellen Sie *ein objWbemSink -Objekt.* [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-192">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="ec2a1-193">Nachdem alle -Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in Ihrer Implementierung von *objWbemSink ausführen.* [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-193">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="ec2a1-194">Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-194">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="ec2a1-195">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-195">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="ec2a1-196">Informationen zum Beseitigen der Risiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-196">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="ec2a1-197">Verwenden Sie *den parameter objWbemAsyncContext* in Skripts, um die Quelle eines Aufrufs zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ec2a1-197">Use the *objWbemAsyncContext* parameter in scripts to verify the source of a call.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec2a1-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec2a1-198">Requirements</span></span>



| <span data-ttu-id="ec2a1-199">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec2a1-199">Requirement</span></span> | <span data-ttu-id="ec2a1-200">Wert</span><span class="sxs-lookup"><span data-stu-id="ec2a1-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2a1-201">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-201">Minimum supported client</span></span><br/> | <span data-ttu-id="ec2a1-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec2a1-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec2a1-203">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec2a1-203">Minimum supported server</span></span><br/> | <span data-ttu-id="ec2a1-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec2a1-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec2a1-205">Header</span><span class="sxs-lookup"><span data-stu-id="ec2a1-205">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec2a1-206"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ec2a1-206"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec2a1-207">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ec2a1-207">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec2a1-208"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec2a1-208"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec2a1-209">DLL</span><span class="sxs-lookup"><span data-stu-id="ec2a1-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec2a1-210"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec2a1-210"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec2a1-211">CLSID</span><span class="sxs-lookup"><span data-stu-id="ec2a1-211">CLSID</span></span><br/>                    | <span data-ttu-id="ec2a1-212">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="ec2a1-212">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="ec2a1-213">IID</span><span class="sxs-lookup"><span data-stu-id="ec2a1-213">IID</span></span><br/>                      | <span data-ttu-id="ec2a1-214">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="ec2a1-214">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="ec2a1-215">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec2a1-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2a1-216">**Swbemservices**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-216">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="ec2a1-217">**SWbemObject.Associators\_**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-217">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="ec2a1-218">**SWbemObject.AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-218">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="ec2a1-219">**SWbemObject.References\_**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-219">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="ec2a1-220">**SWbemObject.ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-220">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)
</dt> <dt>

[<span data-ttu-id="ec2a1-221">**SWbemServices.ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-221">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="ec2a1-222">**SWbemServices.ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="ec2a1-222">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

