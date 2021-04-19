---
description: Gibt ein "errbemubjectset"-Objekt zurück.
ms.assetid: cfe08956-7215-4e2e-a279-6e86f14e5c27
ms.tgt_platform: multiple
title: "' Swap Services. SubclassesOf '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e8c23dee5ee3f0a1cf5babe37d0ccb6aa0a3ac7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343788"
---
# <a name="swbemservicessubclassesof-method"></a><span data-ttu-id="9558c-103">Methode ' Swap Services. SubclassesOf '</span><span class="sxs-lookup"><span data-stu-id="9558c-103">SWbemServices.SubclassesOf method</span></span>

<span data-ttu-id="9558c-104">Die **SubclassesOf** -Methode des-Objekts von " [**errbemservices**](swbemservices.md) " gibt ein " [**errbewbjectset**](swbemobjectset.md) "-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9558c-104">The **SubclassesOf** method of the [**SWbemServices**](swbemservices.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="9558c-105">Bei diesem Objekt handelt es sich um eine Auflistung von Unterklassen einer angegebenen Klasse.</span><span class="sxs-lookup"><span data-stu-id="9558c-105">This object is a collection of subclasses of a specified class.</span></span> <span data-ttu-id="9558c-106">Elemente in der zurückgegebenen Auflistung können mithilfe von Standard Auflistungs Methoden abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9558c-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="9558c-107">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="9558c-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="9558c-108">Diese Methode funktioniert nur für Klassen Objekte.</span><span class="sxs-lookup"><span data-stu-id="9558c-108">This method only works for class objects.</span></span>

<span data-ttu-id="9558c-109">Die-Methode wird im semisynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9558c-109">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="9558c-110">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9558c-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="9558c-111">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9558c-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9558c-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="9558c-112">Syntax</span></span>


```VB
objWbemObjectSet = .SubclassesOf( _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9558c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9558c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9558c-114">" *Strauch Klasse* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="9558c-114">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9558c-115">Gibt einen übergeordneten Klassennamen an.</span><span class="sxs-lookup"><span data-stu-id="9558c-115">Specifies a parent class name.</span></span> <span data-ttu-id="9558c-116">Nur Unterklassen dieser Klasse geben im Enumerator zurück.</span><span class="sxs-lookup"><span data-stu-id="9558c-116">Only subclasses of this class return in the enumerator.</span></span> <span data-ttu-id="9558c-117">Wenn Sie diesen Parameter leer lassen und *IFlags* den Wert **wbemqueryflagflache** hat, werden nur die Klassen der obersten Ebene zurückgegeben (d. h. Klassen, die über keine übergeordnete Klasse verfügen).</span><span class="sxs-lookup"><span data-stu-id="9558c-117">If you leave this parameter blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="9558c-118">Wenn dieser Parameter leer ist, und *IFlags* den Wert **wbemqueryflagdeep** hat, werden alle Klassen innerhalb des Namespace zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9558c-118">If this parameter is blank and *iFlags* is **wbemQueryFlagDeep** all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="9558c-119">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9558c-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9558c-120">Bestimmt, wie detailliert der aufzurufende Aufzählung ist.</span><span class="sxs-lookup"><span data-stu-id="9558c-120">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="9558c-121">Die Standardwerte für diesen Parameter lauten **wbemFlagReturnImmediately** und **wbemqueryflagdeep**.</span><span class="sxs-lookup"><span data-stu-id="9558c-121">The default values for this parameter are **wbemFlagReturnImmediately** and **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="9558c-122">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="9558c-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="9558c-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="9558c-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="9558c-124">Erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.</span><span class="sxs-lookup"><span data-stu-id="9558c-124">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="9558c-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9558c-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9558c-126">Der Standardwert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="9558c-126">Default for this parameter.</span></span> <span data-ttu-id="9558c-127">Dieser Wert erzwingt eine rekursive Enumeration in alle Unterklassen, die von der angegebenen übergeordneten Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9558c-127">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="9558c-128">Die übergeordnete Klasse wird nicht in der-Enumeration zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9558c-128">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="9558c-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="9558c-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="9558c-130">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9558c-130">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="9558c-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9558c-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9558c-132">Bewirkt, dass dieser-Vorgang blockiert wird, bis der-Befehl abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9558c-132">Causes this call to block until the call has completed.</span></span> <span data-ttu-id="9558c-133">Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9558c-133">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="9558c-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="9558c-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="9558c-135">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9558c-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="9558c-136">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="9558c-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9558c-137">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9558c-137">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9558c-138">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9558c-138">Typically, this is undefined.</span></span> <span data-ttu-id="9558c-139">Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient.</span><span class="sxs-lookup"><span data-stu-id="9558c-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider servicing the request.</span></span> <span data-ttu-id="9558c-140">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="9558c-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9558c-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9558c-141">Return value</span></span>

<span data-ttu-id="9558c-142">Wenn die Methode erfolgreich ist, wird ein " [**errbemubjectset**](swbemobjectset.md) "-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9558c-142">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9558c-143">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9558c-143">Error codes</span></span>

<span data-ttu-id="9558c-144">Nach dem Abschluss der **SubclassesOf** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="9558c-144">After the completion of the **SubclassesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="9558c-145">Eine zurückgegebene Auflistung mit 0 (null) Elementen ist kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="9558c-145">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="9558c-146">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="9558c-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="9558c-147">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9558c-147">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="9558c-148">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9558c-148">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9558c-149">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9558c-149">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9558c-150">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="9558c-150">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="9558c-151">Die angegebene Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9558c-151">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="9558c-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9558c-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9558c-153">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="9558c-153">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="9558c-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9558c-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9558c-155">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9558c-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9558c-156">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9558c-156">Examples</span></span>

<span data-ttu-id="9558c-157">Das folgende PowerShell-Beispiel zeigt, wie die Unterklassen einer Klasse auf einem Remote System abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9558c-157">The following PowerShell sample shows how to retrieve the subclasses of a class on a remote system.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="9558c-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9558c-158">Requirements</span></span>



| <span data-ttu-id="9558c-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9558c-159">Requirement</span></span> | <span data-ttu-id="9558c-160">Wert</span><span class="sxs-lookup"><span data-stu-id="9558c-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9558c-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9558c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9558c-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9558c-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9558c-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9558c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9558c-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9558c-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9558c-165">Header</span><span class="sxs-lookup"><span data-stu-id="9558c-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="9558c-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9558c-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9558c-167">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9558c-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="9558c-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9558c-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9558c-169">DLL</span><span class="sxs-lookup"><span data-stu-id="9558c-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9558c-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9558c-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9558c-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="9558c-171">CLSID</span></span><br/>                    | <span data-ttu-id="9558c-172">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="9558c-172">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="9558c-173">IID</span><span class="sxs-lookup"><span data-stu-id="9558c-173">IID</span></span><br/>                      | <span data-ttu-id="9558c-174">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="9558c-174">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="9558c-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9558c-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9558c-176">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="9558c-176">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="9558c-177">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="9558c-177">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




