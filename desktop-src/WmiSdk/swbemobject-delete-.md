---
description: Die Delete- \_ Methode des-Objekts von "Swap" löscht entweder die aktuelle Klasse oder die aktuelle Instanz.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: SWbemObject.Delete_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d994c8a9b9e0af9d4bd884c89cd67280513c9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042585"
---
# <a name="swbemobjectdelete_-method"></a><span data-ttu-id="b64b3-103">Errbemubject. Delete- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="b64b3-103">SWbemObject.Delete\_ method</span></span>

<span data-ttu-id="b64b3-104">Die **Delete \_** -Methode des-Objekts von " [**Swap**](swbemobject.md) " löscht entweder die aktuelle Klasse oder die aktuelle Instanz.</span><span class="sxs-lookup"><span data-stu-id="b64b3-104">The **Delete\_** method of the [**SWbemObject**](swbemobject.md) object deletes either the current class or the current instance.</span></span> <span data-ttu-id="b64b3-105">Wenn ein dynamischer Anbieter die Klasse oder Instanz bereitstellt, ist es manchmal nicht möglich, dieses Objekt zu löschen, es sei denn, der Anbieter unterstützt das Löschen von Klassen oder Instanzen.</span><span class="sxs-lookup"><span data-stu-id="b64b3-105">If a dynamic provider supplies the class or instance, it is sometimes not possible to delete this object unless the provider supports class or instance deletion.</span></span> <span data-ttu-id="b64b3-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b64b3-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b64b3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b64b3-107">Syntax</span></span>


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b64b3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b64b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64b3-109">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b64b3-109">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64b3-110">Reserviert und muss 0 (null) sein, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="b64b3-110">Reserved and must be 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="b64b3-111">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b64b3-111">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64b3-112">Dieser Parameter ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b64b3-112">This parameter is typically undefined.</span></span> <span data-ttu-id="b64b3-113">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b64b3-113">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b64b3-114">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="b64b3-114">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64b3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b64b3-115">Return value</span></span>

<span data-ttu-id="b64b3-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b64b3-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b64b3-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b64b3-117">Error codes</span></span>

<span data-ttu-id="b64b3-118">Nach Abschluss der **Delete \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="b64b3-118">After completion of the **Delete\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b64b3-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b64b3-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b64b3-120">Der aktuelle Kontext verfügt nicht über die erforderlichen Sicherheitsrechte, um das Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b64b3-120">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="b64b3-121">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b64b3-121">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b64b3-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b64b3-122">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b64b3-123">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="b64b3-123">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="b64b3-124">Die angegebene Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b64b3-124">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b64b3-125">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="b64b3-125">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="b64b3-126">Das Objekt kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b64b3-126">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="b64b3-127">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="b64b3-127">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="b64b3-128">Das Objekt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b64b3-128">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b64b3-129">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b64b3-129">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b64b3-130">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b64b3-130">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b64b3-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b64b3-131">Remarks</span></span>

<span data-ttu-id="b64b3-132">Bei **der \_ Delete** -Methode tritt ein Fehler auf, wenn eine neue Instanz von " [**errbemujebject**](swbemobject.md) " erstellt wird, aber für die Schlüsseleigenschaft kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b64b3-132">The **Delete\_** method fails if a new instance of [**SWbemObject**](swbemobject.md) is created, but no value is supplied for the key property.</span></span> <span data-ttu-id="b64b3-133">Windows-Verwaltungsinstrumentation (WMI) generiert automatisch einen GUID-Wert (Globally Unique Identifier), aber ein GUID-Wert wird von " **errbewbject. \_ Delete**" nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b64b3-133">Windows Management Instrumentation (WMI) generates a globally unique identifier (GUID) value automatically, but a GUID value is not accepted by **SWbemObject.Delete\_**.</span></span> <span data-ttu-id="b64b3-134">In diesem Fall funktioniert " [**Swap Services. Delete**](swbemservices-delete.md)", das den Objekt Pfad verwendet.</span><span class="sxs-lookup"><span data-stu-id="b64b3-134">In this case, [**SWbemServices.Delete**](swbemservices-delete.md), which uses the object path works.</span></span> <span data-ttu-id="b64b3-135">Beachten Sie, dass ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt von der Methode " [**errbemubject. Put \_**](swbemobject-put-.md) " zurückgegeben wird, nachdem ein Objekt an WMI übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b64b3-135">Note that an [**SWbemObjectPath**](swbemobjectpath.md) object is returned by the [**SWbemObject.Put\_**](swbemobject-put-.md) method after an object is committed to WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="b64b3-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b64b3-136">Examples</span></span>

<span data-ttu-id="b64b3-137">Im folgenden Beispiel wird eine neue Klasse erstellt: Fügt eine Schlüsseleigenschaft hinzu. schreibt die neue Klasse in das Repository. und zeigt den Pfad des neuen Klassen Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b64b3-137">The following example creates a new class; adds a key property; writes the new class to the repository; and displays the path of the new class object.</span></span> <span data-ttu-id="b64b3-138">Das Skript erzeugt dann eine Instanz der neuen Klasse. schreibt Sie; und zeigt den Pfad an.</span><span class="sxs-lookup"><span data-stu-id="b64b3-138">The script then spawns an instance of the new class; writes it; and displays the path.</span></span> <span data-ttu-id="b64b3-139">Beachten Sie, dass das Skript sowohl die-Klasse als auch Ihre-Instanzen aus dem Repository löscht, indem einfach die-Klasse gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b64b3-139">Note that the script deletes both the class and its instances from the repository by simply deleting the class.</span></span>


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="b64b3-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b64b3-140">Requirements</span></span>



| <span data-ttu-id="b64b3-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b64b3-141">Requirement</span></span> | <span data-ttu-id="b64b3-142">Wert</span><span class="sxs-lookup"><span data-stu-id="b64b3-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b64b3-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b64b3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b64b3-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b64b3-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b64b3-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b64b3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b64b3-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b64b3-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b64b3-147">Header</span><span class="sxs-lookup"><span data-stu-id="b64b3-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b64b3-148"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b64b3-148"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b64b3-149">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b64b3-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="b64b3-150"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b64b3-150"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b64b3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b64b3-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b64b3-152"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b64b3-152"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b64b3-153">CLSID</span><span class="sxs-lookup"><span data-stu-id="b64b3-153">CLSID</span></span><br/>                    | <span data-ttu-id="b64b3-154">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="b64b3-154">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="b64b3-155">IID</span><span class="sxs-lookup"><span data-stu-id="b64b3-155">IID</span></span><br/>                      | <span data-ttu-id="b64b3-156">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="b64b3-156">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




