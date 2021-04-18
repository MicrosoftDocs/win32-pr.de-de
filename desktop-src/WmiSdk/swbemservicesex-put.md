---
description: Gibt ein "errbemubjectpath"-Objekt zurück, das den Pfad des Objekts enthält, in das die Daten geschrieben wurden.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: Methode ' Swap servicesex. Put ' (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357464"
---
# <a name="swbemservicesexput-method"></a><span data-ttu-id="0ca80-103">Methode ' Swap servicesex. Put '</span><span class="sxs-lookup"><span data-stu-id="0ca80-103">SWbemServicesEx.Put method</span></span>

<span data-ttu-id="0ca80-104">Die **Put** -Methode des Objekts " [**errbemservicesex**](swbemservicesex.md) " speichert das Objekt in dem Namespace, der an das-Objekt gebunden ist, und gibt ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurück, das den Pfad des Objekts enthält, in das die Daten geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="0ca80-104">The **Put** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves the object to the namespace bound to the object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span>

<span data-ttu-id="0ca80-105">Diese Methode wird im semisynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0ca80-105">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="0ca80-106">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0ca80-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="0ca80-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0ca80-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca80-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ca80-108">Syntax</span></span>


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0ca80-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ca80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ca80-110">*objwbemujekt*</span><span class="sxs-lookup"><span data-stu-id="0ca80-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca80-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0ca80-111">Required.</span></span> <span data-ttu-id="0ca80-112">Das neue-Objekt, das in den-Namespace eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ca80-112">The new object to be put in the namespace.</span></span> <span data-ttu-id="0ca80-113">Dabei kann es sich um ein neu erstelltes Objekt oder um ein geändertes Objekt handeln.</span><span class="sxs-lookup"><span data-stu-id="0ca80-113">This can be either a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="0ca80-114">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="0ca80-114">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-115">Dieser Parameter bestimmt, ob der-Befehl das-Objekt erstellt oder aktualisiert und ob der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0ca80-115">This parameter determines if the call creates or updates the object and if the call returns immediately.</span></span> <span data-ttu-id="0ca80-116">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="0ca80-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="0ca80-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemchangeflagupdatecompatible** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0ca80-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0ca80-118">Ermöglicht es, eine Klasse zu aktualisieren, wenn keine abgeleiteten Klassen vorhanden sind und keine Instanzen für diese Klasse vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0ca80-118">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="0ca80-119">Sie ermöglicht auch Updates in allen Fällen, wenn die Änderung nur an wichtigen Qualifizierern (z. b. der **Beschreibungs** Qualifizierer) vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="0ca80-119">It also allows updates in all cases if the change is only to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="0ca80-120">Dies ist das Standardverhalten für diesen-Befehl und wird aus Gründen der Kompatibilität mit früheren Versionen von WMI verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ca80-120">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="0ca80-121">Wenn die Klasse über Instanzen verfügt, tritt bei der Aktualisierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0ca80-121">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="0ca80-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemchangeflagupdatesafemode** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="0ca80-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="0ca80-123">Ermöglicht das Aktualisieren von Klassen auch dann, wenn untergeordnete Klassen vorhanden sind, wenn die Änderung keine Konflikte mit untergeordneten Klassen verursacht.</span><span class="sxs-lookup"><span data-stu-id="0ca80-123">Allows updates of classes even if there are child classes, when the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="0ca80-124">Sie können dieses Flag verwenden, wenn Sie einer Basisklasse eine neue Eigenschaft hinzufügen, die zuvor nicht in einer der untergeordneten Klassen erwähnt wurde.</span><span class="sxs-lookup"><span data-stu-id="0ca80-124">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="0ca80-125">Wenn die Klasse über Instanzen verfügt, tritt bei der Aktualisierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0ca80-125">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="0ca80-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemchangeflagupdateforcemode** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="0ca80-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="0ca80-127">Dieses Flag erzwingt die Aktualisierung von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0ca80-127">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="0ca80-128">Beispielsweise erzwingt dieses Flag ein Update, wenn ein Klassen Qualifizierer in einer untergeordneten Klasse definiert wurde, und die Basisklasse versucht, denselben Qualifizierer in Konflikt mit dem vorhandenen zu addieren.</span><span class="sxs-lookup"><span data-stu-id="0ca80-128">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="0ca80-129">Im Force-Modus wird dieser Konflikt gelöst, indem der widersprüchliche Qualifizierer in der untergeordneten Klasse gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="0ca80-129">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="0ca80-130">Wenn die Klasse über Instanzen verfügt, tritt bei der Aktualisierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0ca80-130">If the class has instances, the update fails.</span></span>

<span data-ttu-id="0ca80-131">Die Verwendung des Force-Modus zum Aktualisieren einer statischen Klasse bewirkt, dass alle Instanzen dieser Klasse gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="0ca80-131">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="0ca80-132">Bei einem erzwungenen Update für eine Anbieter Klasse werden keine Instanzen der-Klasse gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0ca80-132">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="0ca80-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemchangeflagkreateorupdate** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0ca80-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0ca80-134">Bewirkt, dass die Klasse oder Instanz erstellt wird, wenn Sie nicht vorhanden ist, oder überschrieben, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ca80-134">Causes the class or instance to be created if it does not exist, or overwritten if it already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="0ca80-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemchangeflagkreateonly** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="0ca80-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="0ca80-136">Wird nur für die Erstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ca80-136">Used for creation only.</span></span> <span data-ttu-id="0ca80-137">Der-Rückruf schlägt fehl, wenn die Klasse oder Instanz bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ca80-137">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="0ca80-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemchangeflagupdateonly** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="0ca80-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="0ca80-139">Bewirkt, dass dieser-Befehl nur ein Update durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="0ca80-139">Causes this call to only do an update.</span></span> <span data-ttu-id="0ca80-140">Die Klasse oder Instanz muss vorhanden sein, damit der-Befehl erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="0ca80-140">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="0ca80-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="0ca80-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="0ca80-142">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0ca80-142">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="0ca80-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemflagreturn. Complete** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0ca80-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0ca80-144">Bewirkt, dass dieser-Vorgang blockiert wird, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0ca80-144">Causes this call to block until the operation has completed.</span></span> <span data-ttu-id="0ca80-145">Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0ca80-145">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="0ca80-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemflaguseamendedqualifizierer** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="0ca80-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="0ca80-147">Bewirkt, dass WMI Klassen Zusatzdaten und die Basisklassen Definition schreibt.</span><span class="sxs-lookup"><span data-stu-id="0ca80-147">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="0ca80-148">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="0ca80-148">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0ca80-149">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="0ca80-149">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-150">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="0ca80-150">Typically, this is undefined.</span></span> <span data-ttu-id="0ca80-151">Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ca80-151">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="0ca80-152">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="0ca80-152">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ca80-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ca80-153">Return value</span></span>

<span data-ttu-id="0ca80-154">Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0ca80-154">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="0ca80-155">Dieses Objekt enthält den Objekt Pfad der-Instanz oder der-Klasse, für die erfolgreich ein Commit in WMI durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0ca80-155">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0ca80-156">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0ca80-156">Error codes</span></span>

<span data-ttu-id="0ca80-157">Nach dem Abschluss der **Put** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="0ca80-157">After the completion of the **Put** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="0ca80-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="0ca80-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-159">Der aktuelle Benutzer verfügt nicht über die Berechtigung für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0ca80-159">Current user does not have the permission for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0ca80-160">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="0ca80-160">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-161">Das Flag " **wbemchangeflagkreateonly** " wurde angegeben, aber die Instanz ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0ca80-161">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0ca80-162">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0ca80-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-163">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="0ca80-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="0ca80-164">**wbemErrIllegalNull** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="0ca80-164">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-165">Für eine Eigenschaft, die nicht **null** sein darf, wurde ein **null** -Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="0ca80-165">A value of **NULL** was specified for a property that cannot be **NULL**.</span></span> <span data-ttu-id="0ca80-166">Ein Beispiel für eine solche Eigenschaft ist eine, die durch einen [**Schlüssel**](standard-qualifiers.md)-, **indizierten** oder **Not \_ null** -Qualifizierer gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="0ca80-166">An example of such a property is one marked by a [**Key**](standard-qualifiers.md), **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="0ca80-167">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="0ca80-167">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-168">Das angegebene Objekt ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0ca80-168">The specified object is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0ca80-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="0ca80-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-170">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0ca80-170">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0ca80-171">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="0ca80-171">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-172">Das Flag " **wbemchangeflagupdateonly** " wurde angegeben, aber die Instanz oder Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0ca80-172">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="0ca80-173">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="0ca80-173">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-174">Erforderliche Eigenschaften für Klassen wurden nicht alle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0ca80-174">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="0ca80-175">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0ca80-175">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0ca80-176">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0ca80-176">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ca80-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ca80-177">Requirements</span></span>



| <span data-ttu-id="0ca80-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ca80-178">Requirement</span></span> | <span data-ttu-id="0ca80-179">Wert</span><span class="sxs-lookup"><span data-stu-id="0ca80-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca80-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ca80-180">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca80-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ca80-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0ca80-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ca80-182">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca80-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ca80-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ca80-184">Header</span><span class="sxs-lookup"><span data-stu-id="0ca80-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ca80-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ca80-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ca80-186">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0ca80-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="0ca80-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0ca80-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0ca80-188">DLL</span><span class="sxs-lookup"><span data-stu-id="0ca80-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ca80-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ca80-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0ca80-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="0ca80-190">CLSID</span></span><br/>                    | <span data-ttu-id="0ca80-191">CLSID \_ iswbemservicesex</span><span class="sxs-lookup"><span data-stu-id="0ca80-191">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="0ca80-192">IID</span><span class="sxs-lookup"><span data-stu-id="0ca80-192">IID</span></span><br/>                      | <span data-ttu-id="0ca80-193">IID \_ iswbemservicesex</span><span class="sxs-lookup"><span data-stu-id="0ca80-193">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

 




