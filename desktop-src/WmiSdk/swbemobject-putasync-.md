---
description: Die putasync- \_ Methode von "errbemubject" erstellt oder aktualisiert eine Instanz oder ein Klassenobjekt in Windows-Verwaltungsinstrumentation (WMI).
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: SWbemObject.PutAsync_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218304"
---
# <a name="swbemobjectputasync_-method"></a><span data-ttu-id="9b26f-103">Errbemubject. putasync- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="9b26f-103">SWbemObject.PutAsync\_ method</span></span>

<span data-ttu-id="9b26f-104">Die **putasync \_** -Methode von " [**errbemubject**](swbemobject.md) " erstellt oder aktualisiert eine Instanz oder ein Klassenobjekt in Windows-Verwaltungsinstrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9b26f-104">The **PutAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously creates or updates an instance or class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="9b26f-105">Sie können diese Methode verwenden, nachdem Sie Eigenschaften oder Methoden in " **errbewbject**" geändert haben, und Ihre Änderungen werden in WMI geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9b26f-105">You can use this method after you modify any properties or methods in **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="9b26f-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9b26f-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b26f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b26f-107">Syntax</span></span>


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9b26f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b26f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b26f-109">*objwbemsink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b26f-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-110">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9b26f-110">Required.</span></span> <span data-ttu-id="9b26f-111">Objekt Senke, die asynchron das Ergebnis des **Put** -Vorgangs empfängt.</span><span class="sxs-lookup"><span data-stu-id="9b26f-111">Object sink that asynchronously receives the result of the **put** operation.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-112">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9b26f-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-113">Bestimmt, ob der-Befehl die Klasse oder Instanz erstellt oder aktualisiert und ob der Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b26f-113">Determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="9b26f-114">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="9b26f-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="9b26f-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemchangeflagupdatecompatible \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9b26f-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-116">Ermöglicht es, eine Klasse zu aktualisieren, wenn keine abgeleiteten Klassen vorhanden sind und keine Instanzen für diese Klasse vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9b26f-116">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="9b26f-117">Sie ermöglicht auch Updates in allen Fällen, wenn die Änderung nur an wichtigen Qualifizierern (z. b. der **Beschreibungs** Qualifizierer) erfolgt.</span><span class="sxs-lookup"><span data-stu-id="9b26f-117">It also allows updates in all cases if the change is just to unimportant qualifiers (for example the **Description** qualifier).</span></span> <span data-ttu-id="9b26f-118">Dies ist das Standardverhalten für diesen-Befehl und wird aus Gründen der Kompatibilität mit früheren Versionen von WMI verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b26f-118">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="9b26f-119">Wenn die Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="9b26f-119">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="9b26f-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemchangeflagupdatesafemode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="9b26f-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-121">Ermöglicht das Aktualisieren von Klassen, auch wenn untergeordnete Klassen vorhanden sind, wenn die Änderung keine Konflikte mit untergeordneten Klassen verursacht.</span><span class="sxs-lookup"><span data-stu-id="9b26f-121">Allows updates of classes, even if there are child classes, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="9b26f-122">Sie können dieses Flag verwenden, wenn Sie einer Basisklasse eine neue Eigenschaft hinzufügen, die zuvor nicht in einer der untergeordneten Klassen erwähnt wurde.</span><span class="sxs-lookup"><span data-stu-id="9b26f-122">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="9b26f-123">Wenn die Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="9b26f-123">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="9b26f-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>Wbemchangeflagupdateforcemode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="9b26f-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-125">Erzwingt das Aktualisieren von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9b26f-125">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="9b26f-126">Beispielsweise erzwingt dieses Flag ein Update, wenn ein Klassen Qualifizierer in einer untergeordneten Klasse definiert wurde, und die Basisklasse versucht, denselben Qualifizierer in Konflikt mit dem vorhandenen zu addieren.</span><span class="sxs-lookup"><span data-stu-id="9b26f-126">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class attempts to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="9b26f-127">Im Force-Modus wird dieser Konflikt gelöst, indem der widersprüchliche Qualifizierer in der untergeordneten Klasse gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="9b26f-127">In force mode this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="9b26f-128">Wenn die Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="9b26f-128">If the class has instances the update fails.</span></span>

<span data-ttu-id="9b26f-129">Wenn Sie eine statische Klasse mithilfe des Force-Modus aktualisieren, werden alle Instanzen dieser Klasse gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9b26f-129">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="9b26f-130">Bei einem erzwungenen Update für eine Anbieter Klasse werden keine Instanzen der-Klasse gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9b26f-130">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="9b26f-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemchangeflagkreateorupdate \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9b26f-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-132">Bewirkt, dass die Klasse oder Instanz erstellt wird, wenn Sie nicht vorhanden ist oder überschrieben wird, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9b26f-132">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="9b26f-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemchangeflagkreateonly \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="9b26f-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-134">Wird nur für die Erstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b26f-134">Used for creation only.</span></span> <span data-ttu-id="9b26f-135">Der-Rückruf schlägt fehl, wenn die Klasse oder Instanz bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9b26f-135">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="9b26f-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemchangeflagupdateonly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="9b26f-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-137">Bewirkt, dass dieser Update Vorgang aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9b26f-137">Causes this call to update.</span></span> <span data-ttu-id="9b26f-138">Die Klasse oder Instanz muss vorhanden sein, damit der-Befehl erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="9b26f-138">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="9b26f-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="9b26f-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-140">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b26f-140">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="9b26f-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9b26f-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-142">Bewirkt, dass dieser-Befehl blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9b26f-142">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="9b26f-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="9b26f-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-144">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den " [**slibemsink. OnProgress**](swbemsink-onprogress.md) "-Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="9b26f-144">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="9b26f-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9b26f-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-146">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="9b26f-146">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="9b26f-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="9b26f-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="9b26f-148">Bewirkt, dass WMI Klassen Zusatzdaten zusammen mit der Basisklassen Definition schreibt.</span><span class="sxs-lookup"><span data-stu-id="9b26f-148">Causes WMI to write class amendment data along with the base class definition.</span></span> <span data-ttu-id="9b26f-149">Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="9b26f-149">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9b26f-150">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9b26f-150">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-151">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9b26f-151">Typically, this is undefined.</span></span> <span data-ttu-id="9b26f-152">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9b26f-152">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="9b26f-153">Ein Anbieter, der diese Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="9b26f-153">A provider that supports or requires this information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-154">*objwbemasynccontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9b26f-154">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-155">Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b26f-155">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="9b26f-156">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="9b26f-156">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="9b26f-157">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b26f-157">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="9b26f-158">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b26f-158">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="9b26f-159">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9b26f-159">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b26f-160">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b26f-160">Return value</span></span>

<span data-ttu-id="9b26f-161">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9b26f-161">This method does not return a value.</span></span> <span data-ttu-id="9b26f-162">Wenn der-Befehl erfolgreich ausgeführt wurde, empfängt das [**onobjectput**](swbemsink-onobjectput.md) -Ereignis der angegebenen Objekt Senke ein " [**errbecombjectpath**](swbemobjectpath.md) "-Objekt, das den Objekt Pfad der Instanz oder Klasse enthält, für die erfolgreich ein Commit in WMI ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9b26f-162">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, containing the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9b26f-163">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9b26f-163">Error codes</span></span>

<span data-ttu-id="9b26f-164">Nach dem Abschluss der **putasync \_** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b26f-164">After the completion of the **PutAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9b26f-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="9b26f-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-166">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Aktualisieren einer Instanz der angegebenen Klasse.</span><span class="sxs-lookup"><span data-stu-id="9b26f-166">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-167">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="9b26f-167">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-168">Das Flag " **wbemchangeflagkreateonly** " wurde angegeben, aber die Instanz ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9b26f-168">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-169">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9b26f-169">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-170">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9b26f-170">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-171">**wbemErrIllegalNull** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="9b26f-171">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-172">Der Wert **Nothing** wurde für eine Eigenschaft angegeben, die möglicherweise nicht " **Nothing**" ist.</span><span class="sxs-lookup"><span data-stu-id="9b26f-172">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="9b26f-173">Ein Beispiel für eine solche Eigenschaft ist eine, die durch einen **Schlüssel**-, **indizierten** oder **Not \_ null** -Qualifizierer gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="9b26f-173">An example of such a property is one that is marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-174">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="9b26f-174">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-175">Die angegebene Instanz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9b26f-175">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-176">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9b26f-176">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-177">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9b26f-177">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-178">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="9b26f-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-179">Das Flag " **wbemchangeflagupdateonly** " wurde angegeben, aber die Instanz oder Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9b26f-179">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-180">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="9b26f-180">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-181">Erforderliche Eigenschaften für Klassen wurden nicht alle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b26f-181">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="9b26f-182">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9b26f-182">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9b26f-183">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9b26f-183">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b26f-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b26f-184">Remarks</span></span>

<span data-ttu-id="9b26f-185">Dieser Aufruf wird sofort zurückgegeben, und das Ergebnis des Put-Vorgangs wird an den **Aufrufer** zurückgegeben, indem Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9b26f-185">This call returns immediately, and the result of the **put** operation is returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="9b26f-186">Implementieren Sie *objwbemsink*.</span><span class="sxs-lookup"><span data-stu-id="9b26f-186">Implement the *objWbemSink*.</span></span> <span data-ttu-id="9b26f-187">[**Onobjectput**](swbemsink-onobjectput.md) -Methode zum Abrufen des Objekt Pfads der Instanz oder Klasse, die in das WMI-Repository geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="9b26f-187">[**OnObjectPut**](swbemsink-onobjectput.md) method to obtain the object path of the instance or class that is written to the WMI repository.</span></span> <span data-ttu-id="9b26f-188">Weitere Informationen zu Sink-Methoden finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9b26f-188">For more information about sink methods, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="9b26f-189">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="9b26f-189">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="9b26f-190">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9b26f-190">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="9b26f-191">Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="9b26f-191">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="9b26f-192">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9b26f-192">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b26f-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b26f-193">Requirements</span></span>



| <span data-ttu-id="9b26f-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b26f-194">Requirement</span></span> | <span data-ttu-id="9b26f-195">Wert</span><span class="sxs-lookup"><span data-stu-id="9b26f-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b26f-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b26f-196">Minimum supported client</span></span><br/> | <span data-ttu-id="9b26f-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b26f-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b26f-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b26f-198">Minimum supported server</span></span><br/> | <span data-ttu-id="9b26f-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b26f-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b26f-200">Header</span><span class="sxs-lookup"><span data-stu-id="9b26f-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b26f-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b26f-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b26f-202">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9b26f-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b26f-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9b26f-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9b26f-204">DLL</span><span class="sxs-lookup"><span data-stu-id="9b26f-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b26f-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b26f-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b26f-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="9b26f-206">CLSID</span></span><br/>                    | <span data-ttu-id="9b26f-207">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="9b26f-207">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="9b26f-208">IID</span><span class="sxs-lookup"><span data-stu-id="9b26f-208">IID</span></span><br/>                      | <span data-ttu-id="9b26f-209">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="9b26f-209">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="9b26f-210">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b26f-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b26f-211">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="9b26f-211">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="9b26f-212">**Errbemubjectpath. Class**</span><span class="sxs-lookup"><span data-stu-id="9b26f-212">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="9b26f-213">**Swap Property**</span><span class="sxs-lookup"><span data-stu-id="9b26f-213">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="9b26f-214">**Austausch Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="9b26f-214">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

