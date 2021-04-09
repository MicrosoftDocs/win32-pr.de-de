---
description: Erstellt einen Enumerator, der die Instanzen einer angegebenen Klasse gemäß den vom Benutzer angegebenen Auswahlkriterien zurückgibt.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: "' Swap Services. InstancesOf '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOf
- ISWbemServices.InstancesOf
- ISWbemServices.InstancesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2386b52160b1e2a08c5a345b67922ed24afc44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868571"
---
# <a name="swbemservicesinstancesof-method"></a><span data-ttu-id="0d731-103">Swap Services. InstancesOf-Methode</span><span class="sxs-lookup"><span data-stu-id="0d731-103">SWbemServices.InstancesOf method</span></span>

<span data-ttu-id="0d731-104">Die **InstancesOf** -Methode des [**Swap Services**](swbemservices.md) -Objekts erstellt einen Enumerator, der die Instanzen einer angegebenen Klasse gemäß den vom Benutzer angegebenen Auswahlkriterien zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0d731-104">The **InstancesOf** method of the [**SWbemServices**](swbemservices.md) object creates an enumerator that returns the instances of a specified class according to the user-specified selection criteria.</span></span> <span data-ttu-id="0d731-105">Diese Methode implementiert eine einfache Abfrage.</span><span class="sxs-lookup"><span data-stu-id="0d731-105">This method implements a simple query.</span></span> <span data-ttu-id="0d731-106">Komplexere Abfragen erfordern möglicherweise die Verwendung von [**SWbemServices.Execquery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="0d731-106">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="0d731-107">Die-Methode wird im semisynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0d731-107">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="0d731-108">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0d731-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="0d731-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0d731-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d731-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d731-110">Syntax</span></span>


```VB
objWbemObjectSet = .InstancesOf( _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0d731-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d731-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d731-112">*Klasse*</span><span class="sxs-lookup"><span data-stu-id="0d731-112">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="0d731-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d731-113">Required.</span></span> <span data-ttu-id="0d731-114">Eine Zeichenfolge, die den Namen der Klasse enthält, für die-Instanzen gewünscht werden.</span><span class="sxs-lookup"><span data-stu-id="0d731-114">String that contains the name of the class for which instances are desired.</span></span> <span data-ttu-id="0d731-115">Dieser Parameter darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="0d731-115">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="0d731-116">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="0d731-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d731-117">Dieser Parameter bestimmt, wie detailliert der aufzurufende Aufzählung und ob dieser aufgerufen wird, sobald dieser aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0d731-117">This parameter determines how detailed the call enumerates and if this call returns immediately.</span></span> <span data-ttu-id="0d731-118">Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="0d731-118">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="0d731-119">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="0d731-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="0d731-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="0d731-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="0d731-121">Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d731-121">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="0d731-122">Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.</span><span class="sxs-lookup"><span data-stu-id="0d731-122">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="0d731-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemflagbidirektionale \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0d731-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0d731-124">Bewirkt, dass WMI Zeiger auf Objekte der-Enumeration behält, bis der Client den Enumerator freigibt.</span><span class="sxs-lookup"><span data-stu-id="0d731-124">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="0d731-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="0d731-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="0d731-126">Standardwert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="0d731-126">Default value for this parameter.</span></span> <span data-ttu-id="0d731-127">Dieses Flag bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d731-127">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="0d731-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0d731-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0d731-129">Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0d731-129">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="0d731-130">Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0d731-130">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="0d731-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="0d731-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="0d731-132">Erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.</span><span class="sxs-lookup"><span data-stu-id="0d731-132">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="0d731-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0d731-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0d731-134">Standardwert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="0d731-134">Default value for this parameter.</span></span> <span data-ttu-id="0d731-135">Dieser Wert erzwingt, dass die Enumeration alle Klassen in der Hierarchie einschließt.</span><span class="sxs-lookup"><span data-stu-id="0d731-135">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="0d731-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="0d731-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="0d731-137">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0d731-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="0d731-138">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="0d731-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0d731-139">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="0d731-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d731-140">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="0d731-140">Typically, this is undefined.</span></span> <span data-ttu-id="0d731-141">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0d731-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="0d731-142">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="0d731-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d731-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d731-143">Return value</span></span>

<span data-ttu-id="0d731-144">Wenn der Vorgang erfolgreich ist, gibt die Methode einen " [**errbewbjectset**](swbemobjectset.md)" zurück.</span><span class="sxs-lookup"><span data-stu-id="0d731-144">If successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="0d731-145">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0d731-145">Error codes</span></span>

<span data-ttu-id="0d731-146">Nach dem Abschluss der **InstancesOf** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="0d731-146">Upon the completion of the **InstancesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="0d731-147">Ein zurückgegebener Enumerator mit 0 (null) Elementen ist kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="0d731-147">A returned enumerator with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="0d731-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="0d731-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="0d731-149">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen von Instanzen der angegebenen Klasse.</span><span class="sxs-lookup"><span data-stu-id="0d731-149">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="0d731-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0d731-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0d731-151">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="0d731-151">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0d731-152">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="0d731-152">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="0d731-153">Die angegebene Klasse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0d731-153">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0d731-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="0d731-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="0d731-155">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0d731-155">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0d731-156">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0d731-156">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0d731-157">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0d731-157">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d731-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d731-158">Remarks</span></span>

<span data-ttu-id="0d731-159">Die **InstancesOf** -Methode funktioniert nur für Klassen Objekte.</span><span class="sxs-lookup"><span data-stu-id="0d731-159">The **InstancesOf** method only works for class objects.</span></span>

<span data-ttu-id="0d731-160">Standardmäßig führt InstancesOf einen Deep-Abruf durch.</span><span class="sxs-lookup"><span data-stu-id="0d731-160">By default, InstancesOf performs a deep retrieval.</span></span> <span data-ttu-id="0d731-161">Das heißt, dass InstancesOf alle Instanzen der verwalteten Ressource, die Sie identifizieren, und alle Instanzen aller Unterklassen, die unter der Zielklasse definiert sind, abruft.</span><span class="sxs-lookup"><span data-stu-id="0d731-161">That is, InstancesOf retrieves all instances of the managed resource you identify and all instances of all the subclasses defined beneath the target class.</span></span> <span data-ttu-id="0d731-162">Das folgende Skript ruft z. b. alle Ressourcen ab, die von allen dynamischen Klassen modelliert werden, die unter der \_ abstrakten Klasse des CIM-Dienstanbieter definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0d731-162">For example, the following script retrieves all of the resources modeled by all of the dynamic classes defined beneath the CIM\_Service abstract class.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



<span data-ttu-id="0d731-163">Wenn Sie dieses Skript ausführen, erhalten Sie Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="0d731-163">If you run this script, you will get information back.</span></span> <span data-ttu-id="0d731-164">Diese Informationen werden jedoch nicht auf die auf einem Computer installierten Dienste beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0d731-164">However, this information will not be limited to the services installed on a computer.</span></span> <span data-ttu-id="0d731-165">Stattdessen enthält Sie Informationen von allen untergeordneten Klassen des [**CIM- \_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/cim-service), einschließlich [**Win32 \_ System Driver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) und [**Win32 \_ applicationservice**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d731-165">Instead, it will include information from all child classes of [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), including [**Win32\_SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) and [**Win32\_ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d731-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d731-166">Requirements</span></span>



| <span data-ttu-id="0d731-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d731-167">Requirement</span></span> | <span data-ttu-id="0d731-168">Wert</span><span class="sxs-lookup"><span data-stu-id="0d731-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d731-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d731-169">Minimum supported client</span></span><br/> | <span data-ttu-id="0d731-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d731-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d731-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d731-171">Minimum supported server</span></span><br/> | <span data-ttu-id="0d731-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d731-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d731-173">Header</span><span class="sxs-lookup"><span data-stu-id="0d731-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d731-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d731-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d731-175">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0d731-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d731-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d731-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d731-177">DLL</span><span class="sxs-lookup"><span data-stu-id="0d731-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d731-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d731-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d731-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="0d731-179">CLSID</span></span><br/>                    | <span data-ttu-id="0d731-180">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="0d731-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="0d731-181">IID</span><span class="sxs-lookup"><span data-stu-id="0d731-181">IID</span></span><br/>                      | <span data-ttu-id="0d731-182">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="0d731-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="0d731-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d731-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d731-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="0d731-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="0d731-185">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="0d731-185">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

