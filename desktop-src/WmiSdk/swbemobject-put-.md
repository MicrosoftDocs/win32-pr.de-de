---
description: Die Put- \_ Methode von "errbemubject" erstellt oder aktualisiert eine Instanz oder ein Klassenobjekt in Windows-Verwaltungsinstrumentation (WMI). Sie können diese Methode verwenden, nachdem Sie Eigenschaften oder Methoden in einem Swap-Objekt geändert haben, und Ihre Änderungen werden in WMI geschrieben.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: SWbemObject.Put_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f5ca9b79c9def8f209da37e0ef1cfddefa0dbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347065"
---
# <a name="swbemobjectput_-method"></a><span data-ttu-id="f2cef-104">Errbemubject. Put- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="f2cef-104">SWbemObject.Put\_ method</span></span>

<span data-ttu-id="f2cef-105">Die **Put \_** -Methode von " [**errbemubject**](swbemobject.md) " erstellt oder aktualisiert eine Instanz oder ein Klassenobjekt in Windows-Verwaltungsinstrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f2cef-105">The **Put\_** method of [**SWbemObject**](swbemobject.md) creates or updates an instance or a class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="f2cef-106">Sie können diese Methode verwenden, nachdem Sie Eigenschaften oder Methoden in einem **Swap-Objekt** geändert haben, und Ihre Änderungen werden in WMI geschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2cef-106">You can use this method after you modify any properties or methods in an **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="f2cef-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f2cef-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2cef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2cef-108">Syntax</span></span>


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f2cef-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2cef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2cef-110">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f2cef-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-111">Dieser Parameter bestimmt, ob der-Befehl die Klasse oder Instanz erstellt oder aktualisiert und ob der Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f2cef-111">This parameter determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="f2cef-112">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="f2cef-112">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="f2cef-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemchangeflagupdatecompatible \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f2cef-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f2cef-114">Ermöglicht es, eine Klasse zu aktualisieren, wenn keine abgeleiteten Klassen vorhanden sind und keine Instanzen für diese Klasse vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f2cef-114">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="f2cef-115">Es lässt auch Updates in allen Fällen zu, wenn die Änderung lediglich an unbedeutende Qualifizierer (z. b. der **Beschreibungs** Qualifizierer) erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f2cef-115">It also allows updates in all cases if the change is just to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="f2cef-116">Dies ist das Standardverhalten für diesen-Befehl und wird aus Gründen der Kompatibilität mit früheren Versionen von WMI verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2cef-116">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="f2cef-117">Wenn die Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="f2cef-117">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="f2cef-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemchangeflagupdatesafemode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="f2cef-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="f2cef-119">Ermöglicht das Aktualisieren von Klassen auch dann, wenn untergeordnete Klassen vorhanden sind, wenn die Änderung keine Konflikte mit untergeordneten Klassen verursacht.</span><span class="sxs-lookup"><span data-stu-id="f2cef-119">Allows updates of classes even if there are child classes if the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="f2cef-120">Sie können dieses Flag verwenden, wenn Sie einer Basisklasse eine neue Eigenschaft hinzufügen, die zuvor nicht in einer der untergeordneten Klassen erwähnt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2cef-120">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="f2cef-121">Wenn die Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="f2cef-121">If the class has instances the update fails.</span></span> <span data-ttu-id="f2cef-122">Wenn die Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="f2cef-122">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="f2cef-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>Wbemchangeflagupdateforcemode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="f2cef-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="f2cef-124">Dieses Flag erzwingt die Aktualisierung von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f2cef-124">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="f2cef-125">Dieses Flag erzwingt z. b. eine Aktualisierung, wenn ein Klassen Qualifizierer in einer untergeordneten Klasse definiert wurde, und die Basisklasse versucht, denselben Qualifizierer hinzuzufügen und in Konflikt mit dem vorhandenen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f2cef-125">For example, this flag will force an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier and in conflict with the existing one.</span></span> <span data-ttu-id="f2cef-126">Im Force-Modus würde dieser Konflikt durch Löschen des in Konflikt stehenden Qualifizierers in der untergeordneten Klasse behoben werden.</span><span class="sxs-lookup"><span data-stu-id="f2cef-126">In force mode this conflict would be resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="f2cef-127">Wenn die Klasse über Instanzen verfügt, kann das Update nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f2cef-127">If the class has instances the update will fail.</span></span>

<span data-ttu-id="f2cef-128">Wenn Sie eine statische Klasse mithilfe des Force-Modus aktualisieren, werden alle Instanzen dieser Klasse gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f2cef-128">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="f2cef-129">Bei einem erzwungenen Update für eine Anbieter Klasse werden keine Instanzen der-Klasse gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f2cef-129">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="f2cef-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemchangeflagkreateorupdate \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f2cef-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f2cef-131">Bewirkt, dass die Klasse oder Instanz erstellt wird, wenn Sie nicht vorhanden ist oder überschrieben wird, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f2cef-131">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="f2cef-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemchangeflagkreateonly \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="f2cef-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="f2cef-133">Wird nur für die Erstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2cef-133">Used for creation only.</span></span> <span data-ttu-id="f2cef-134">Der-Rückruf schlägt fehl, wenn die Klasse oder Instanz bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f2cef-134">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="f2cef-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemchangeflagupdateonly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="f2cef-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="f2cef-136">Bewirkt, dass dieser Update Vorgang aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f2cef-136">Causes this call to update.</span></span> <span data-ttu-id="f2cef-137">Die Klasse oder Instanz muss vorhanden sein, damit der-Befehl erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="f2cef-137">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="f2cef-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="f2cef-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="f2cef-139">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f2cef-139">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="f2cef-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f2cef-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f2cef-141">Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f2cef-141">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="f2cef-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="f2cef-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="f2cef-143">Bewirkt, dass WMI Klassen Zusatzdaten und die Basisklassen Definition schreibt.</span><span class="sxs-lookup"><span data-stu-id="f2cef-143">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="f2cef-144">Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="f2cef-144">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f2cef-145">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f2cef-145">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-146">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f2cef-146">Typically, this is undefined.</span></span> <span data-ttu-id="f2cef-147">Andernfalls handelt es sich um ein Objekt vom Typ" [**errbemujectpath**](swbemobjectpath.md) ", dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f2cef-147">Otherwise, this is an [**SWbemObjectPath**](swbemobjectpath.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="f2cef-148">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="f2cef-148">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2cef-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2cef-149">Return value</span></span>

<span data-ttu-id="f2cef-150">Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2cef-150">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="f2cef-151">Dieses Objekt enthält den Objekt Pfad der-Instanz oder der-Klasse, für die erfolgreich ein Commit in WMI durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2cef-151">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2cef-152">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f2cef-152">Error codes</span></span>

<span data-ttu-id="f2cef-153">Nach dem Abschluss der **Put \_** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="f2cef-153">After the completion of the **Put\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f2cef-154">**wbemErrAccessDenied** -2147749891</span><span class="sxs-lookup"><span data-stu-id="f2cef-154">**wbemErrAccessDenied** - 2147749891</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-155">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Aktualisieren einer Instanz der angegebenen Klasse.</span><span class="sxs-lookup"><span data-stu-id="f2cef-155">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="f2cef-156">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="f2cef-156">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-157">Das Flag " **wbemchangeflagkreateonly** " wurde angegeben, aber die Instanz ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f2cef-157">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f2cef-158">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f2cef-158">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-159">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2cef-159">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f2cef-160">**wbemErrIllegalNull** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="f2cef-160">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-161">Der Wert **Nothing** wurde für eine Eigenschaft angegeben, die möglicherweise nicht " **Nothing**" ist.</span><span class="sxs-lookup"><span data-stu-id="f2cef-161">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="f2cef-162">Ein Beispiel für eine solche Eigenschaft ist eine, die durch einen **Schlüssel-,** **indizierten** oder **Not \_ null** -Qualifizierer gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="f2cef-162">An example of such a property is one marked by a **Key,** **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="f2cef-163">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="f2cef-163">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-164">Die angegebene Instanz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f2cef-164">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f2cef-165">**wbemErrInvalidParameter** -0x80041008</span><span class="sxs-lookup"><span data-stu-id="f2cef-165">**wbemErrInvalidParameter** - 0x80041008</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-166">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f2cef-166">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f2cef-167">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="f2cef-167">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-168">Das Flag " **wbemchangeflagupdateonly** " wurde angegeben, aber die Instanz oder Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f2cef-168">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="f2cef-169">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="f2cef-169">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-170">Erforderliche Eigenschaften für Klassen wurden nicht alle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2cef-170">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="f2cef-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="f2cef-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f2cef-172">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f2cef-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2cef-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2cef-173">Requirements</span></span>



| <span data-ttu-id="f2cef-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2cef-174">Requirement</span></span> | <span data-ttu-id="f2cef-175">Wert</span><span class="sxs-lookup"><span data-stu-id="f2cef-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2cef-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2cef-176">Minimum supported client</span></span><br/> | <span data-ttu-id="f2cef-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2cef-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2cef-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2cef-178">Minimum supported server</span></span><br/> | <span data-ttu-id="f2cef-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2cef-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2cef-180">Header</span><span class="sxs-lookup"><span data-stu-id="f2cef-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2cef-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2cef-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2cef-182">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f2cef-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2cef-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2cef-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2cef-184">DLL</span><span class="sxs-lookup"><span data-stu-id="f2cef-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2cef-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2cef-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2cef-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="f2cef-186">CLSID</span></span><br/>                    | <span data-ttu-id="f2cef-187">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="f2cef-187">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="f2cef-188">IID</span><span class="sxs-lookup"><span data-stu-id="f2cef-188">IID</span></span><br/>                      | <span data-ttu-id="f2cef-189">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="f2cef-189">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="f2cef-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2cef-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2cef-191">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="f2cef-191">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="f2cef-192">**Errbemubjectpath. Class**</span><span class="sxs-lookup"><span data-stu-id="f2cef-192">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="f2cef-193">**Swap Property**</span><span class="sxs-lookup"><span data-stu-id="f2cef-193">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="f2cef-194">**Austausch Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="f2cef-194">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

