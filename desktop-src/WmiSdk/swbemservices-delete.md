---
description: Löscht die im Objekt Pfad angegebene Klasse oder Instanz. Sie können nur Objekte im aktuellen Namespace löschen.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Methode ' Swap Services. delete ' (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485443"
---
# <a name="swbemservicesdelete-method"></a><span data-ttu-id="07ad1-104">Swap Services. Delete-Methode</span><span class="sxs-lookup"><span data-stu-id="07ad1-104">SWbemServices.Delete method</span></span>

<span data-ttu-id="07ad1-105">Die **Delete** -Methode des [**Swap Services**](swbemservices.md) -Objekts löscht die im Objekt Pfad angegebene Klasse oder Instanz.</span><span class="sxs-lookup"><span data-stu-id="07ad1-105">The **Delete** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance that is specified in the object path.</span></span> <span data-ttu-id="07ad1-106">Sie können nur Objekte im aktuellen Namespace löschen.</span><span class="sxs-lookup"><span data-stu-id="07ad1-106">You can only delete objects in the current namespace.</span></span>

<span data-ttu-id="07ad1-107">Wenn ein dynamischer Anbieter die Klasse oder Instanz bereitstellt, können Sie dieses Objekt nur dann löschen, wenn der Anbieter das Löschen von Klassen oder Instanzen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="07ad1-107">If a dynamic provider supplies the class or instance, you cannot delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="07ad1-108">Diese Methode wird im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="07ad1-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="07ad1-109">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="07ad1-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="07ad1-110">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="07ad1-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="07ad1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="07ad1-111">Syntax</span></span>


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="07ad1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="07ad1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07ad1-113">*strobjectpath*</span><span class="sxs-lookup"><span data-stu-id="07ad1-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="07ad1-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="07ad1-114">Required.</span></span> <span data-ttu-id="07ad1-115">Eine Zeichenfolge, die den Objekt Pfad zu dem Objekt enthält, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="07ad1-115">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="07ad1-116">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="07ad1-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="07ad1-117">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="07ad1-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07ad1-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="07ad1-118">Reserved.</span></span> <span data-ttu-id="07ad1-119">Dieser Wert muss null (0) sein.</span><span class="sxs-lookup"><span data-stu-id="07ad1-119">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="07ad1-120">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="07ad1-120">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07ad1-121">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="07ad1-121">Typically, this is undefined.</span></span> <span data-ttu-id="07ad1-122">Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="07ad1-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="07ad1-123">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="07ad1-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07ad1-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07ad1-124">Return value</span></span>

<span data-ttu-id="07ad1-125">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="07ad1-125">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07ad1-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="07ad1-126">Error codes</span></span>

<span data-ttu-id="07ad1-127">Nach dem Abschluss der **Delete** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="07ad1-127">After the completion of the **Delete** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="07ad1-128">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="07ad1-128">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="07ad1-129">Der aktuelle Kontext verfügt nicht über die erforderlichen Sicherheitsrechte, um das Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="07ad1-129">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="07ad1-130">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="07ad1-130">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="07ad1-131">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="07ad1-131">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="07ad1-132">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="07ad1-132">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="07ad1-133">Die angegebene Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="07ad1-133">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="07ad1-134">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="07ad1-134">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="07ad1-135">Das Objekt kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="07ad1-135">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="07ad1-136">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="07ad1-136">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="07ad1-137">Das Objekt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="07ad1-137">Object does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="07ad1-138">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="07ad1-138">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="07ad1-139">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="07ad1-139">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07ad1-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07ad1-140">Remarks</span></span>

<span data-ttu-id="07ad1-141">Die Methode " **waybemservices. Delete** " kann verwendet werden, wenn der Schlüsseleigenschaft für das Objekt kein Wert zugewiesen wird, da diese Methode nur einen Objekt Pfad als Eingabe erfordert.</span><span class="sxs-lookup"><span data-stu-id="07ad1-141">The **SWbemServices.Delete** method can be used when the key property for the object is not given a value, because this method only requires an object path as input.</span></span> <span data-ttu-id="07ad1-142">Diese Methode kann in Situationen verwendet werden, in denen das Austauschen von " [**errbemubject. Delete \_**](swbemobject-delete-.md) " aufgrund eines fehlenden Schlüssel Werts fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="07ad1-142">This method can be used in situations where [**SWbemObject.Delete\_**](swbemobject-delete-.md) fails for lack of a key value.</span></span> <span data-ttu-id="07ad1-143">Wenn das Objekt über die Datei " [**Swap. Put \_**](swbemobject-put-.md)" in WMI übernommen wird, wurde ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt durch den-Befehl abgerufen.</span><span class="sxs-lookup"><span data-stu-id="07ad1-143">If the object is committed to WMI through [**SWbemObject.Put\_**](swbemobject-put-.md), then an [**SWbemObjectPath**](swbemobjectpath.md) object was obtained through the call.</span></span>

## <a name="examples"></a><span data-ttu-id="07ad1-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07ad1-144">Examples</span></span>

<span data-ttu-id="07ad1-145">Im folgenden Beispiel wird eine neue Klasse erstellt, eine Eigenschaft hinzugefügt, die kein Schlüssel ist, die neue Klasse in das Repository schreibt, und der Pfad des neuen Klassen Objekts wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07ad1-145">The following example creates a new class, adds a property that is not a key, writes the new class to the repository, and displays the path of the new class object.</span></span> <span data-ttu-id="07ad1-146">Das Skript erzeugt dann eine Instanz der neuen Klasse, schreibt die Instanz und zeigt den Pfad an.</span><span class="sxs-lookup"><span data-stu-id="07ad1-146">The script then spawns an instance of the new class, writes the instance, and displays the path.</span></span> <span data-ttu-id="07ad1-147">Beachten Sie, dass das Skript sowohl die-Klasse als auch Ihre-Instanzen aus dem Repository löscht, indem die-Klasse gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="07ad1-147">Note that the script deletes both the class and its instances from the repository by deleting the class.</span></span> <span data-ttu-id="07ad1-148">Weitere Informationen zu WMI-Klassen und-Instanzen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md) und [Common Information Model](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="07ad1-148">For more information about WMI classes and instances, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Common Information Model](common-information-model.md).</span></span>


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="07ad1-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07ad1-149">Requirements</span></span>



| <span data-ttu-id="07ad1-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07ad1-150">Requirement</span></span> | <span data-ttu-id="07ad1-151">Wert</span><span class="sxs-lookup"><span data-stu-id="07ad1-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07ad1-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07ad1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="07ad1-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07ad1-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07ad1-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07ad1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="07ad1-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07ad1-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07ad1-156">Header</span><span class="sxs-lookup"><span data-stu-id="07ad1-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="07ad1-157"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="07ad1-157"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="07ad1-158">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="07ad1-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="07ad1-159"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="07ad1-159"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="07ad1-160">DLL</span><span class="sxs-lookup"><span data-stu-id="07ad1-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07ad1-161"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07ad1-161"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="07ad1-162">CLSID</span><span class="sxs-lookup"><span data-stu-id="07ad1-162">CLSID</span></span><br/>                    | <span data-ttu-id="07ad1-163">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="07ad1-163">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="07ad1-164">IID</span><span class="sxs-lookup"><span data-stu-id="07ad1-164">IID</span></span><br/>                      | <span data-ttu-id="07ad1-165">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="07ad1-165">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="07ad1-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07ad1-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ad1-167">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="07ad1-167">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="07ad1-168">**Errbemubjectpath**</span><span class="sxs-lookup"><span data-stu-id="07ad1-168">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

 




