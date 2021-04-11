---
description: Speichert ein-Objekt asynchron in einem Namespace. Bei erfolgreicher Ausführung sendet diese Methode ein onabgeschlossene-Ereignis an das "slibemsink"-Objekt, das als Eingabeparameter angegeben wird.
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.tgt_platform: multiple
title: "' Taubemservicesex. putasync '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 06f470ed6f8cbd497ba3d3a3a77c5a8b4e5748c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042584"
---
# <a name="swbemservicesexputasync-method"></a><span data-ttu-id="ad254-104">Methode ' Swap Service Type. putasync '</span><span class="sxs-lookup"><span data-stu-id="ad254-104">SWbemServicesEx.PutAsync method</span></span>

<span data-ttu-id="ad254-105">Die **putasync** -Methode des-Objekts von " [**taubemservicesex**](swbemservicesex.md) " speichert ein-Objekt asynchron in einem Namespace.</span><span class="sxs-lookup"><span data-stu-id="ad254-105">The **PutAsync** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves an object asynchronously to a namespace.</span></span> <span data-ttu-id="ad254-106">Bei erfolgreicher Ausführung sendet diese Methode ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis an das " [**slibemsink**](swbemsink.md) "-Objekt, das als Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad254-106">When successful, this method sends an [**OnCompleted**](swbemsink-oncompleted.md) event to the [**SWbemSink**](swbemsink.md) object that is specified as an input parameter.</span></span>

<span data-ttu-id="ad254-107">Diese Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ad254-107">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="ad254-108">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ad254-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="ad254-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ad254-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad254-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad254-110">Syntax</span></span>


```VB
SWbemServicesEx.PutAsync( _
  ByVal objWbemSink, _
  ByVal ojbWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ad254-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad254-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad254-112">*objwbemsink*</span><span class="sxs-lookup"><span data-stu-id="ad254-112">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="ad254-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ad254-113">Required.</span></span> <span data-ttu-id="ad254-114">Objekt Senke, die die-Objekte asynchron empfängt.</span><span class="sxs-lookup"><span data-stu-id="ad254-114">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="ad254-115">Erstellen Sie ein " [**Swap**](swbemsink.md) "-Objekt, um die Objekte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ad254-115">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-116">*ojbwbejbject*</span><span class="sxs-lookup"><span data-stu-id="ad254-116">*ojbWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="ad254-117">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ad254-117">Required.</span></span> <span data-ttu-id="ad254-118">Das neue-Objekt, das in den-Namespace eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad254-118">The new object to be put in the namespace.</span></span> <span data-ttu-id="ad254-119">Hierbei kann es sich um ein neu erstelltes Objekt oder ein geändertes Objekt handeln.</span><span class="sxs-lookup"><span data-stu-id="ad254-119">This may be a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-120">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="ad254-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad254-121">Dieser Parameter bestimmt, ob der-Befehl das-Objekt erstellt oder aktualisiert und ob der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad254-121">This parameter determines whether the call creates or updates the object and whether the call returns immediately.</span></span> <span data-ttu-id="ad254-122">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="ad254-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="ad254-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemchangeflagupdatecompatible** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="ad254-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ad254-124">Ermöglicht es, eine Klasse zu aktualisieren, wenn keine abgeleiteten Klassen und keine Instanzen für die Klasse vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ad254-124">Allows a class to be updated when there are no derived classes and no instances for the class.</span></span> <span data-ttu-id="ad254-125">Sie ermöglicht auch Updates in allen Fällen, in denen sich die Änderung nur an wichtigen Qualifizierern, z. b. dem **Beschreibungs** Qualifizierer, befindet</span><span class="sxs-lookup"><span data-stu-id="ad254-125">It also allows updates in all cases when the change is only to unimportant qualifiers, for example, the **Description** qualifier.</span></span> <span data-ttu-id="ad254-126">Dies ist das Standardverhalten für diesen-Befehl und wird aus Gründen der Kompatibilität mit früheren Versionen von WMI verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad254-126">This is the default behavior for this call, and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="ad254-127">Wenn die Klasse über Instanzen verfügt, tritt bei der Aktualisierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ad254-127">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="ad254-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemchangeflagupdatesafemode** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="ad254-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="ad254-129">Ermöglicht das Aktualisieren von Klassen auch dann, wenn untergeordnete Klassen vorhanden sind und die Änderung keine Konflikte mit den untergeordneten Klassen verursacht.</span><span class="sxs-lookup"><span data-stu-id="ad254-129">Allows updates of classes even when there are child classes and the change does not cause conflicts with the child classes.</span></span> <span data-ttu-id="ad254-130">Verwenden Sie dieses Flag, wenn Sie einer Basisklasse eine neue Eigenschaft hinzufügen, die zuvor in einer der untergeordneten Klassen nicht erwähnt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad254-130">Use this flag when adding a new property to a base class that is not mentioned previously in any of the child classes.</span></span> <span data-ttu-id="ad254-131">Wenn die Klasse über Instanzen verfügt, tritt bei der Aktualisierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ad254-131">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="ad254-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemchangeflagupdateforcemode** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="ad254-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="ad254-133">Dieses Flag erzwingt die Aktualisierung von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ad254-133">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="ad254-134">Beispielsweise erzwingt dieses Flag ein Update, wenn ein Klassen Qualifizierer in einer untergeordneten Klasse definiert ist, und die Basisklasse versucht, denselben Qualifizierer in Konflikt mit dem vorhandenen zu addieren.</span><span class="sxs-lookup"><span data-stu-id="ad254-134">For example, this flag forces an update when a class qualifier is defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="ad254-135">Im Force-Modus wird dieser Konflikt gelöst, indem der widersprüchliche Qualifizierer in der untergeordneten Klasse gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ad254-135">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="ad254-136">Wenn die Klasse über Instanzen verfügt, tritt bei der Aktualisierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ad254-136">If the class has instances, the update fails.</span></span>

<span data-ttu-id="ad254-137">Die Verwendung des Force-Modus zum Aktualisieren einer statischen Klasse bewirkt, dass alle Instanzen dieser Klasse gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ad254-137">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="ad254-138">Bei einem erzwungenen Update für eine Anbieter Klasse werden keine Instanzen der-Klasse gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ad254-138">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="ad254-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemchangeflagkreateorupdate** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="ad254-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ad254-140">Bewirkt, dass die Klasse oder Instanz erstellt wird, wenn Sie nicht vorhanden ist, oder überschrieben, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad254-140">Causes the class or instance to be created if it does not exist, or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="ad254-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemchangeflagkreateonly** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="ad254-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="ad254-142">Wird nur für die Erstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad254-142">Used for creation only.</span></span> <span data-ttu-id="ad254-143">Der-Rückruf schlägt fehl, wenn die Klasse oder Instanz bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad254-143">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="ad254-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemchangeflagupdateonly** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="ad254-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="ad254-145">Bewirkt, dass dieser Update Vorgang aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ad254-145">Causes this call to update.</span></span> <span data-ttu-id="ad254-146">Die Klasse oder Instanz muss vorhanden sein, damit der-Befehl erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="ad254-146">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="ad254-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="ad254-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="ad254-148">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad254-148">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="ad254-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemflagreturn. Complete** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="ad254-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ad254-150">Bewirkt, dass dieser-Vorgang blockiert wird, bis die Abfrage beendet ist.</span><span class="sxs-lookup"><span data-stu-id="ad254-150">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="ad254-151">Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ad254-151">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="ad254-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemflaguseamendedqualifizierer** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="ad254-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="ad254-153">Bewirkt, dass WMI Klassen Zusatzdaten und die Basisklassen Definition schreibt.</span><span class="sxs-lookup"><span data-stu-id="ad254-153">Causes WMI to write class amendment data and the base class definition.</span></span> <span data-ttu-id="ad254-154">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="ad254-154">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ad254-155">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="ad254-155">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad254-156">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="ad254-156">Typically, this is undefined.</span></span> <span data-ttu-id="ad254-157">Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad254-157">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="ad254-158">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="ad254-158">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-159">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="ad254-159">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad254-160">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ad254-160">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="ad254-161">Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ad254-161">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="ad254-162">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ad254-162">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="ad254-163">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="ad254-163">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="ad254-164">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ad254-164">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad254-165">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad254-165">Return value</span></span>

<span data-ttu-id="ad254-166">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ad254-166">This method does not return a value.</span></span> <span data-ttu-id="ad254-167">Wenn der-Befehl erfolgreich ausgeführt wurde, empfängt das [**onobjectput**](swbemsink-onobjectput.md) -Ereignis der angegebenen Objekt Senke ein " [**errbecombjectpath**](swbemobjectpath.md) "-Objekt, das den Objekt Pfad der Instanz oder Klasse enthält, für die erfolgreich ein Commit in WMI ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad254-167">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, which contains the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ad254-168">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ad254-168">Error codes</span></span>

<span data-ttu-id="ad254-169">Nach dem Abschluss der **putasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="ad254-169">After the completion of the **PutAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ad254-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="ad254-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="ad254-171">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Aktualisieren einer Instanz der angegebenen Klasse.</span><span class="sxs-lookup"><span data-stu-id="ad254-171">Current user does not have the permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-172">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="ad254-172">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="ad254-173">Das Flag " **wbemchangeflagkreateonly** " wurde angegeben, aber die Instanz ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ad254-173">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-174">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ad254-174">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ad254-175">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ad254-175">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-176">**wbemErrIllegalNull** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="ad254-176">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="ad254-177">Für eine Eigenschaft, die nicht NULL sein darf, wurde ein NULL-Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="ad254-177">A value of Null was specified for a property that cannot be Null.</span></span> <span data-ttu-id="ad254-178">Ein Beispiel für eine solche Eigenschaft ist eine, die durch einen **Schlüssel**-, **indizierten** oder **Not \_ null** -Qualifizierer gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="ad254-178">An example of such a property is one marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-179">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="ad254-179">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="ad254-180">Die angegebene Instanz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ad254-180">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-181">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ad254-181">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ad254-182">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ad254-182">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-183">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="ad254-183">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="ad254-184">Das Flag " **wbemchangeflagupdateonly** " wurde angegeben, aber die Instanz oder Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ad254-184">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-185">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="ad254-185">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="ad254-186">Erforderliche Eigenschaften für Klassen wurden nicht alle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ad254-186">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="ad254-187">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ad254-187">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ad254-188">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ad254-188">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad254-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad254-189">Remarks</span></span>

<span data-ttu-id="ad254-190">Dieser Aufruf wird sofort zurückgegeben, und die Ergebnisse und der Status werden mithilfe von Ereignissen, die an die in *objwbemsink* angegebene Senke gesendet werden, an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad254-190">This call returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="ad254-191">Um jedes Objekt zu verarbeiten, wenn es eingeht, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="ad254-191">To handle each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="ad254-192">Jede Verarbeitung, die nach dem Eintreffen aller Objekte erfolgt, erfolgt in einer Unterroutine für die *objwbemsink*. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ad254-192">Any processing done after all the objects arrive is done in a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="ad254-193">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="ad254-193">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="ad254-194">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="ad254-194">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="ad254-195">Um die Risiken auszuschließen, finden Sie weitere Informationen unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="ad254-195">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad254-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad254-196">Requirements</span></span>



| <span data-ttu-id="ad254-197">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad254-197">Requirement</span></span> | <span data-ttu-id="ad254-198">Wert</span><span class="sxs-lookup"><span data-stu-id="ad254-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad254-199">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad254-199">Minimum supported client</span></span><br/> | <span data-ttu-id="ad254-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad254-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad254-201">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad254-201">Minimum supported server</span></span><br/> | <span data-ttu-id="ad254-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad254-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad254-203">Header</span><span class="sxs-lookup"><span data-stu-id="ad254-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad254-204"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad254-204"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad254-205">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ad254-205">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad254-206"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ad254-206"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ad254-207">DLL</span><span class="sxs-lookup"><span data-stu-id="ad254-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad254-208"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad254-208"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad254-209">CLSID</span><span class="sxs-lookup"><span data-stu-id="ad254-209">CLSID</span></span><br/>                    | <span data-ttu-id="ad254-210">CLSID \_ iswbemservicesex</span><span class="sxs-lookup"><span data-stu-id="ad254-210">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="ad254-211">IID</span><span class="sxs-lookup"><span data-stu-id="ad254-211">IID</span></span><br/>                      | <span data-ttu-id="ad254-212">IID \_ iswbemservicesex</span><span class="sxs-lookup"><span data-stu-id="ad254-212">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

