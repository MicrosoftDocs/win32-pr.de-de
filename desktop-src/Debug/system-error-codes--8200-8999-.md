---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 8200-8999 und ist für Entwickler bestimmt.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: System Fehler Codes (8200-8999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214158"
---
# <a name="system-error-codes-8200-8999"></a><span data-ttu-id="d4525-103">System Fehler Codes (8200-8999)</span><span class="sxs-lookup"><span data-stu-id="d4525-103">System Error Codes (8200-8999)</span></span>

> [!NOTE]
> <span data-ttu-id="d4525-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="d4525-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="d4525-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d4525-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="d4525-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 8200 bis 8999 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d4525-106">The following list describes [system error codes](system-error-codes.md) for errors 8200 to 8999.</span></span> <span data-ttu-id="d4525-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="d4525-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="d4525-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="d4525-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="d4525-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**Fehler- \_ DS \_ nicht \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="d4525-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR\_DS\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-110">8200 (0x2008)</span><span class="sxs-lookup"><span data-stu-id="d4525-110">8200 (0x2008)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-111">Fehler beim Installieren des Verzeichnis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d4525-111">An error occurred while installing the directory service.</span></span> <span data-ttu-id="d4525-112">Weitere Informationen finden Sie im Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="d4525-112">For more information, see the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**Fehler- \_ DS- \_ Mitgliedschaft \_ \_ lokal ausgewertet**</span><span class="sxs-lookup"><span data-stu-id="d4525-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR\_DS\_MEMBERSHIP\_EVALUATED\_LOCALLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-114">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="d4525-114">8201 (0x2009)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-115">Der Verzeichnisdienst hat die Gruppenmitgliedschaften lokal ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="d4525-115">The directory service evaluated group memberships locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**Fehler- \_ DS \_ kein \_ Attribut \_ oder \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="d4525-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR\_DS\_NO\_ATTRIBUTE\_OR\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-117">8202 (0x200a)</span><span class="sxs-lookup"><span data-stu-id="d4525-117">8202 (0x200A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-118">Das angegebene Verzeichnisdienst Attribut oder der angegebene Wert ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-118">The specified directory service attribute or value does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**Fehler- \_ DS \_ ungültige \_ Attribut \_ Syntax.**</span><span class="sxs-lookup"><span data-stu-id="d4525-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR\_DS\_INVALID\_ATTRIBUTE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-120">8203 (0x200b)</span><span class="sxs-lookup"><span data-stu-id="d4525-120">8203 (0x200B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-121">Die für den Verzeichnisdienst angegebene Attribut Syntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-121">The attribute syntax specified to the directory service is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**Fehler \_ DS \_ - \_ Attributtyp nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="d4525-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR\_DS\_ATTRIBUTE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-123">8204 (0x200c)</span><span class="sxs-lookup"><span data-stu-id="d4525-123">8204 (0x200C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-124">Der für den Verzeichnisdienst angegebene Attributtyp ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="d4525-124">The attribute type specified to the directory service is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**Fehler- \_ DS- \_ Attribut oder- \_ \_ Wert \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="d4525-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR\_DS\_ATTRIBUTE\_OR\_VALUE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-126">8205 (0x200d)</span><span class="sxs-lookup"><span data-stu-id="d4525-126">8205 (0x200D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-127">Das angegebene Verzeichnisdienst Attribut oder der angegebene Wert ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-127">The specified directory service attribute or value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**Fehler- \_ DS \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="d4525-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR\_DS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-129">8206 (0x200e)</span><span class="sxs-lookup"><span data-stu-id="d4525-129">8206 (0x200E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-130">Der Verzeichnisdienst ist ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="d4525-130">The directory service is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**Fehler- \_ DS nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="d4525-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-132">8207 (0x200f)</span><span class="sxs-lookup"><span data-stu-id="d4525-132">8207 (0x200F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-133">Der Verzeichnisdienst ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4525-133">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**Fehler " \_ DS \_ keine \_ RIDs \_ zugeordnet"**</span><span class="sxs-lookup"><span data-stu-id="d4525-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR\_DS\_NO\_RIDS\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-135">8208 (0x2010)</span><span class="sxs-lookup"><span data-stu-id="d4525-135">8208 (0x2010)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-136">Der Verzeichnisdienst kann keinen relativen Bezeichner zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d4525-136">The directory service was unable to allocate a relative identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**Fehler- \_ DS \_ keine \_ weiteren \_ RIDs**</span><span class="sxs-lookup"><span data-stu-id="d4525-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR\_DS\_NO\_MORE\_RIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-138">8209 (0x2011)</span><span class="sxs-lookup"><span data-stu-id="d4525-138">8209 (0x2011)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-139">Der Verzeichnisdienst hat den Pool relativer Bezeichner ausgeschöpft.</span><span class="sxs-lookup"><span data-stu-id="d4525-139">The directory service has exhausted the pool of relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**Fehler \_ DS \_ falscher \_ Rollen \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="d4525-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR\_DS\_INCORRECT\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-141">8210 (0x2012)</span><span class="sxs-lookup"><span data-stu-id="d4525-141">8210 (0x2012)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-142">Der angeforderte Vorgang konnte nicht ausgeführt werden, da der Verzeichnisdienst nicht der Master für diese Art von Vorgang ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-142">The requested operation could not be performed because the directory service is not the master for that type of operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**Fehler \_ DS \_ ridmgr- \_ Init- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERROR\_DS\_RIDMGR\_INIT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-144">8211 (0x2013)</span><span class="sxs-lookup"><span data-stu-id="d4525-144">8211 (0x2013)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-145">Der Verzeichnisdienst konnte das Subsystem, das relative Bezeichner ordnet, nicht initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d4525-145">The directory service was unable to initialize the subsystem that allocates relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**Fehler- \_ DS- \_ obj- \_ Klassen \_ Verletzung**</span><span class="sxs-lookup"><span data-stu-id="d4525-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR\_DS\_OBJ\_CLASS\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-147">8212 (0x2014)</span><span class="sxs-lookup"><span data-stu-id="d4525-147">8212 (0x2014)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-148">Der angeforderte Vorgang erfüllte mindestens eine Einschränkung, die der Klasse des-Objekts zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-148">The requested operation did not satisfy one or more constraints associated with the class of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**Fehler " \_ DS" \_ auf " \_ \_ nicht \_ Blatt"**</span><span class="sxs-lookup"><span data-stu-id="d4525-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR\_DS\_CANT\_ON\_NON\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-150">8213 (0x2015)</span><span class="sxs-lookup"><span data-stu-id="d4525-150">8213 (0x2015)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-151">Der Verzeichnisdienst kann den angeforderten Vorgang nur für ein Blatt Objekt ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4525-151">The directory service can perform the requested operation only on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**Fehler " \_ DS" \_ \_ bei \_ RDN**</span><span class="sxs-lookup"><span data-stu-id="d4525-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR\_DS\_CANT\_ON\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-153">8214 (0x2016)</span><span class="sxs-lookup"><span data-stu-id="d4525-153">8214 (0x2016)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-154">Der Verzeichnisdienst kann den angeforderten Vorgang nicht für das RDN-Attribut eines Objekts ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4525-154">The directory service cannot perform the requested operation on the RDN attribute of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**Error \_ DS \_ cant \_ mod \_ obj- \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="d4525-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR\_DS\_CANT\_MOD\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-156">8215 (0x2017)</span><span class="sxs-lookup"><span data-stu-id="d4525-156">8215 (0x2017)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-157">Der Verzeichnisdienst hat einen Versuch erkannt, die Objektklasse eines Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d4525-157">The directory service detected an attempt to modify the object class of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**Fehler-DS-DOM-Verschiebungs \_ \_ \_ \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**ERROR\_DS\_CROSS\_DOM\_MOVE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-159">8216 (0x2018)</span><span class="sxs-lookup"><span data-stu-id="d4525-159">8216 (0x2018)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-160">Der angeforderte Domänen übergreifende Verschiebungs Vorgang konnte nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-160">The requested cross-domain move operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**Fehler- \_ DS- \_ GC \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="d4525-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR\_DS\_GC\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-162">8217 (0x2019)</span><span class="sxs-lookup"><span data-stu-id="d4525-162">8217 (0x2019)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-163">Es kann keine Verbindung mit dem globalen Katalogserver hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-163">Unable to contact the global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**fehlerfrei \_ gegebene \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="d4525-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERROR\_SHARED\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-165">8218 (0x201a)</span><span class="sxs-lookup"><span data-stu-id="d4525-165">8218 (0x201A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-166">Das Policy-Objekt ist freigegeben und kann nur am Stamm geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-166">The policy object is shared and can only be modified at the root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**das Fehler \_ Richtlinien \_ Objekt wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**ERROR\_POLICY\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-168">8219 (0x201b)</span><span class="sxs-lookup"><span data-stu-id="d4525-168">8219 (0x201B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-169">Das Richtlinien Objekt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-169">The policy object does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_nur Fehler \_ Richtlinie \_ in \_ DS**</span><span class="sxs-lookup"><span data-stu-id="d4525-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**ERROR\_POLICY\_ONLY\_IN\_DS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-171">8220 (0x201c)</span><span class="sxs-lookup"><span data-stu-id="d4525-171">8220 (0x201C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-172">Die angeforderten Richtlinien Informationen befinden sich nur im Verzeichnisdienst.</span><span class="sxs-lookup"><span data-stu-id="d4525-172">The requested policy information is only in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**Fehler bei herauf Stufung \_ \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="d4525-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**ERROR\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-174">8221 (0x201d)</span><span class="sxs-lookup"><span data-stu-id="d4525-174">8221 (0x201D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-175">Eine Domänen Controller-herauf Stufung ist zurzeit aktiv.</span><span class="sxs-lookup"><span data-stu-id="d4525-175">A domain controller promotion is currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**Fehler "keine herauf Stufung \_ \_ \_ aktiv"**</span><span class="sxs-lookup"><span data-stu-id="d4525-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR\_NO\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-177">8222 (0x201e)</span><span class="sxs-lookup"><span data-stu-id="d4525-177">8222 (0x201E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-178">Eine Domänen Controller-herauf Stufung ist zurzeit nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="d4525-178">A domain controller promotion is not currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**Fehler \_ DS- \_ Vorgangs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**ERROR\_DS\_OPERATIONS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-180">8224 (0x2020)</span><span class="sxs-lookup"><span data-stu-id="d4525-180">8224 (0x2020)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-181">Ein Vorgangs Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-181">An operations error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**Fehler- \_ DS- \_ Protokoll \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**ERROR\_DS\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-183">8225 (0x2021)</span><span class="sxs-lookup"><span data-stu-id="d4525-183">8225 (0x2021)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-184">Es ist ein Protokollfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-184">A protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**Fehler bei ' \_ \_ timelimit ' \_ überschritten.**</span><span class="sxs-lookup"><span data-stu-id="d4525-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR\_DS\_TIMELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-186">8226 (0x2022)</span><span class="sxs-lookup"><span data-stu-id="d4525-186">8226 (0x2022)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-187">Das Zeitlimit für diese Anforderung wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d4525-187">The time limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**Fehler " \_ DS \_ SizeLimit" \_ überschritten.**</span><span class="sxs-lookup"><span data-stu-id="d4525-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR\_DS\_SIZELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-189">8227 (0x2023)</span><span class="sxs-lookup"><span data-stu-id="d4525-189">8227 (0x2023)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-190">Die Größenbeschränkung für diese Anforderung wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d4525-190">The size limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**Fehler- \_ DS- \_ Administrator \_ Limit \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="d4525-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERROR\_DS\_ADMIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-192">8228 (0x2024)</span><span class="sxs-lookup"><span data-stu-id="d4525-192">8228 (0x2024)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-193">Der administrative Grenzwert für diese Anforderung wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d4525-193">The administrative limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**Fehler- \_ DS- \_ Vergleich \_ false**</span><span class="sxs-lookup"><span data-stu-id="d4525-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR\_DS\_COMPARE\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-195">8229 (0x2025)</span><span class="sxs-lookup"><span data-stu-id="d4525-195">8229 (0x2025)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-196">Die Vergleichs Antwort war ' false '.</span><span class="sxs-lookup"><span data-stu-id="d4525-196">The compare response was false.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**Fehler- \_ DS mit \_ \_ true vergleichen**</span><span class="sxs-lookup"><span data-stu-id="d4525-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR\_DS\_COMPARE\_TRUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-198">8230 (0x2026)</span><span class="sxs-lookup"><span data-stu-id="d4525-198">8230 (0x2026)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-199">Die Vergleichs Antwort war "true".</span><span class="sxs-lookup"><span data-stu-id="d4525-199">The compare response was true.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**Fehler-DS-Authentifizierungs \_ \_ \_ Methode \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="d4525-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERROR\_DS\_AUTH\_METHOD\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-201">8231 (0x2027)</span><span class="sxs-lookup"><span data-stu-id="d4525-201">8231 (0x2027)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-202">Die angeforderte Authentifizierungsmethode wird vom Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-202">The requested authentication method is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**Fehler \_ DS \_ starke Authentifizierung \_ \_ erforderlich.**</span><span class="sxs-lookup"><span data-stu-id="d4525-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR\_DS\_STRONG\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-204">8232 (0x2028)</span><span class="sxs-lookup"><span data-stu-id="d4525-204">8232 (0x2028)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-205">Für diesen Server ist eine sicherere Authentifizierungsmethode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4525-205">A more secure authentication method is required for this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**Fehler- \_ DS- \_ ungeeignete Authentifizierung \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR\_DS\_INAPPROPRIATE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-207">8233 (0x2029)</span><span class="sxs-lookup"><span data-stu-id="d4525-207">8233 (0x2029)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-208">Nicht geeignete Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="d4525-208">Inappropriate authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**Fehler \_ DS-Authentifizierung \_ \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="d4525-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR\_DS\_AUTH\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-210">8234 (0x202a)</span><span class="sxs-lookup"><span data-stu-id="d4525-210">8234 (0x202A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-211">Der Authentifizierungsmechanismus ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="d4525-211">The authentication mechanism is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**Fehler- \_ DS- \_ Referenz**</span><span class="sxs-lookup"><span data-stu-id="d4525-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**ERROR\_DS\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-213">8235 (0x202b)</span><span class="sxs-lookup"><span data-stu-id="d4525-213">8235 (0x202B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-214">Vom Server wurde eine Referenz zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4525-214">A referral was returned from the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**Fehler- \_ DS nicht \_ Verfügbare \_ Crit- \_ Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="d4525-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR\_DS\_UNAVAILABLE\_CRIT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-216">8236 (0x202c)</span><span class="sxs-lookup"><span data-stu-id="d4525-216">8236 (0x202C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-217">Die angeforderte kritische Erweiterung wird vom Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-217">The server does not support the requested critical extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**Fehler- \_ DS- \_ Vertraulichkeit \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4525-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR\_DS\_CONFIDENTIALITY\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-219">8237 (0x202d)</span><span class="sxs-lookup"><span data-stu-id="d4525-219">8237 (0x202D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-220">Für diese Anforderung ist eine sichere Verbindung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4525-220">This request requires a secure connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**Fehler- \_ DS- \_ ungeeignet \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR\_DS\_INAPPROPRIATE\_MATCHING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-222">8238 (0x202e)</span><span class="sxs-lookup"><span data-stu-id="d4525-222">8238 (0x202E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-223">Ungeeignete Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="d4525-223">Inappropriate matching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**Fehler-DS-Einschränkungs \_ \_ \_ Verletzung**</span><span class="sxs-lookup"><span data-stu-id="d4525-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR\_DS\_CONSTRAINT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-225">8239 (0x202f)</span><span class="sxs-lookup"><span data-stu-id="d4525-225">8239 (0x202F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-226">Eine Einschränkungs Verletzung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-226">A constraint violation occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**Fehler- \_ DS ist \_ kein \_ solches \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="d4525-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR\_DS\_NO\_SUCH\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-228">8240 (0x2030)</span><span class="sxs-lookup"><span data-stu-id="d4525-228">8240 (0x2030)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-229">Ein solches Objekt ist auf dem Server nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-229">There is no such object on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**Fehler- \_ DS- \_ Alias \_ Problem**</span><span class="sxs-lookup"><span data-stu-id="d4525-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERROR\_DS\_ALIAS\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-231">8241 (0x2031)</span><span class="sxs-lookup"><span data-stu-id="d4525-231">8241 (0x2031)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-232">Es liegt ein Alias Problem vor.</span><span class="sxs-lookup"><span data-stu-id="d4525-232">There is an alias problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**Fehler- \_ DS \_ ungültige \_ DN- \_ Syntax**</span><span class="sxs-lookup"><span data-stu-id="d4525-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR\_DS\_INVALID\_DN\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-234">8242 (0x2032)</span><span class="sxs-lookup"><span data-stu-id="d4525-234">8242 (0x2032)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-235">Es wurde eine ungültige DN-Syntax angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4525-235">An invalid dn syntax has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**Fehler- \_ DS \_ ist \_ Blatt**</span><span class="sxs-lookup"><span data-stu-id="d4525-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERROR\_DS\_IS\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-237">8243 (0x2033)</span><span class="sxs-lookup"><span data-stu-id="d4525-237">8243 (0x2033)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-238">Das-Objekt ist ein Blatt Objekt.</span><span class="sxs-lookup"><span data-stu-id="d4525-238">The object is a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**Fehler- \_ DS- \_ Alias- \_ Deref- \_ Problem**</span><span class="sxs-lookup"><span data-stu-id="d4525-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERROR\_DS\_ALIAS\_DEREF\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-240">8244 (0x2034)</span><span class="sxs-lookup"><span data-stu-id="d4525-240">8244 (0x2034)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-241">Es gibt ein Alias Dereferenzierungsproblem.</span><span class="sxs-lookup"><span data-stu-id="d4525-241">There is an alias dereferencing problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**Fehler- \_ DS ist \_ nicht \_ zur \_ Ausführung bereit**</span><span class="sxs-lookup"><span data-stu-id="d4525-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR\_DS\_UNWILLING\_TO\_PERFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-243">8245 (0x2035)</span><span class="sxs-lookup"><span data-stu-id="d4525-243">8245 (0x2035)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-244">Der Server kann die Anforderung nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4525-244">The server is unwilling to process the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**Fehler- \_ DS- \_ Schleifen \_ Erkennung**</span><span class="sxs-lookup"><span data-stu-id="d4525-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR\_DS\_LOOP\_DETECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-246">8246 (0x2036)</span><span class="sxs-lookup"><span data-stu-id="d4525-246">8246 (0x2036)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-247">Eine-Schleife wurde erkannt.</span><span class="sxs-lookup"><span data-stu-id="d4525-247">A loop has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**Fehler- \_ DS- \_ Benennungs \_ Verletzung**</span><span class="sxs-lookup"><span data-stu-id="d4525-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR\_DS\_NAMING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-249">8247 (0x2037)</span><span class="sxs-lookup"><span data-stu-id="d4525-249">8247 (0x2037)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-250">Es gibt eine Benennungs Verletzung.</span><span class="sxs-lookup"><span data-stu-id="d4525-250">There is a naming violation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**Fehler- \_ DS- \_ Objekt \_ Ergebnisse \_ zu \_ groß**</span><span class="sxs-lookup"><span data-stu-id="d4525-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERROR\_DS\_OBJECT\_RESULTS\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-252">8248 (0x2038)</span><span class="sxs-lookup"><span data-stu-id="d4525-252">8248 (0x2038)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-253">Das Resultset ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="d4525-253">The result set is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**Fehler- \_ DS wirkt sich auf \_ \_ mehrere \_ DSAs aus**</span><span class="sxs-lookup"><span data-stu-id="d4525-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERROR\_DS\_AFFECTS\_MULTIPLE\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-255">8249 (0x2039)</span><span class="sxs-lookup"><span data-stu-id="d4525-255">8249 (0x2039)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-256">Der Vorgang wirkt sich auf mehrere DSAs aus.</span><span class="sxs-lookup"><span data-stu-id="d4525-256">The operation affects multiple DSAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**Fehler \_ DS- \_ Server \_ nach unten**</span><span class="sxs-lookup"><span data-stu-id="d4525-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR\_DS\_SERVER\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-258">8250 (0x203a)</span><span class="sxs-lookup"><span data-stu-id="d4525-258">8250 (0x203A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-259">Der Server ist nicht funktionstüchtig.</span><span class="sxs-lookup"><span data-stu-id="d4525-259">The server is not operational.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**Fehler- \_ DS \_ local- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**ERROR\_DS\_LOCAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-261">8251 (0x203b)</span><span class="sxs-lookup"><span data-stu-id="d4525-261">8251 (0x203B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-262">Ein lokaler Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-262">A local error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**Fehler- \_ DS- \_ Codierungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**ERROR\_DS\_ENCODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-264">8252 (0x203c)</span><span class="sxs-lookup"><span data-stu-id="d4525-264">8252 (0x203C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-265">Es ist ein Codierungsfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-265">An encoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**Fehler \_ DS- \_ Decodierungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**ERROR\_DS\_DECODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-267">8253 (0x203d)</span><span class="sxs-lookup"><span data-stu-id="d4525-267">8253 (0x203D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-268">Ein Decodierungs Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-268">A decoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**Fehler- \_ DS- \_ Filter \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="d4525-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR\_DS\_FILTER\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-270">8254 (0x203e)</span><span class="sxs-lookup"><span data-stu-id="d4525-270">8254 (0x203E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-271">Der Suchfilter kann nicht erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-271">The search filter cannot be recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**Fehler \_ DS- \_ param- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**ERROR\_DS\_PARAM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-273">8255 (0x203f)</span><span class="sxs-lookup"><span data-stu-id="d4525-273">8255 (0x203F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-274">Mindestens ein Parameter ist unzulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-274">One or more parameters are illegal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**Fehler- \_ DS \_ nicht \_ unterstützt**</span><span class="sxs-lookup"><span data-stu-id="d4525-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR\_DS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-276">8256 (0x2040)</span><span class="sxs-lookup"><span data-stu-id="d4525-276">8256 (0x2040)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-277">Die angegebene Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-277">The specified method is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**Fehler " \_ DS \_ keine \_ Ergebnisse \_ zurückgegeben"**</span><span class="sxs-lookup"><span data-stu-id="d4525-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR\_DS\_NO\_RESULTS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-279">8257 (0x2041)</span><span class="sxs-lookup"><span data-stu-id="d4525-279">8257 (0x2041)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-280">Es wurden keine Ergebnisse zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4525-280">No results were returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**Fehler- \_ DS- \_ Steuerelement \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="d4525-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERROR\_DS\_CONTROL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-282">8258 (0x2042)</span><span class="sxs-lookup"><span data-stu-id="d4525-282">8258 (0x2042)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-283">Das angegebene Steuerelement wird vom Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-283">The specified control is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**Fehler- \_ DS- \_ Client \_ Schleife**</span><span class="sxs-lookup"><span data-stu-id="d4525-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR\_DS\_CLIENT\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-285">8259 (0x2043)</span><span class="sxs-lookup"><span data-stu-id="d4525-285">8259 (0x2043)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-286">Vom Client wurde eine Verweis Schleife erkannt.</span><span class="sxs-lookup"><span data-stu-id="d4525-286">A referral loop was detected by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**Fehler- \_ DS- \_ Verweis \_ Limit \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="d4525-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERROR\_DS\_REFERRAL\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-288">8260 (0x2044)</span><span class="sxs-lookup"><span data-stu-id="d4525-288">8260 (0x2044)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-289">Das Limit für den voreingestellten Verweis wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d4525-289">The preset referral limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**Fehler der \_ DS- \_ Sortier \_ Steuerung \_ fehlt.**</span><span class="sxs-lookup"><span data-stu-id="d4525-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR\_DS\_SORT\_CONTROL\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-291">8261 (0x2045)</span><span class="sxs-lookup"><span data-stu-id="d4525-291">8261 (0x2045)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-292">Die Suche erfordert ein SORT-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d4525-292">The search requires a SORT control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**Fehler- \_ DS- \_ Offset \_ Bereichs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**ERROR\_DS\_OFFSET\_RANGE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-294">8262 (0x2046)</span><span class="sxs-lookup"><span data-stu-id="d4525-294">8262 (0x2046)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-295">Die Suchergebnisse überschreiten den angegebenen Offset Bereich.</span><span class="sxs-lookup"><span data-stu-id="d4525-295">The search results exceed the offset range specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**Fehler \_ DS \_ ridmgr \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="d4525-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR\_DS\_RIDMGR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-297">8263 (0x2047)</span><span class="sxs-lookup"><span data-stu-id="d4525-297">8263 (0x2047)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-298">Der Verzeichnisdienst hat festgestellt, dass das Subsystem, von dem relative Bezeichner zugewiesen werden, deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-298">The directory service detected the subsystem that allocates relative identifiers is disabled.</span></span> <span data-ttu-id="d4525-299">Dies kann als Schutzmechanismus auftreten, wenn das System festlegt, dass ein signifikanter Anteil relativer Bezeichner (RIDs) erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-299">This can occur as a protective mechanism when the system determines a significant portion of relative identifiers (RIDs) have been exhausted.</span></span> <span data-ttu-id="d4525-300"><https://go.microsoft.com/fwlink/p/?linkid=228610>Die empfohlenen Diagnose Schritte und das Verfahren zum erneuten Aktivieren der Kontoerstellung finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="d4525-300">Please see <https://go.microsoft.com/fwlink/p/?linkid=228610> for recommended diagnostic steps and the procedure to re-enable account creation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**Fehler \_ DS-Stamm \_ \_ muss \_ \_ NC sein**</span><span class="sxs-lookup"><span data-stu-id="d4525-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERROR\_DS\_ROOT\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-302">8301 (0x206d)</span><span class="sxs-lookup"><span data-stu-id="d4525-302">8301 (0x206D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-303">Das Stamm Objekt muss den Anfang eines Namens Kontexts aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d4525-303">The root object must be the head of a naming context.</span></span> <span data-ttu-id="d4525-304">Das Stamm Objekt kann kein instanziertes übergeordnetes Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d4525-304">The root object cannot have an instantiated parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**Fehler- \_ DS \_ Add Replica- \_ Replikat \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR\_DS\_ADD\_REPLICA\_INHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-306">8302 (0x206e)</span><span class="sxs-lookup"><span data-stu-id="d4525-306">8302 (0x206E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-307">Der Vorgang Replikat hinzufügen kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-307">The add replica operation cannot be performed.</span></span> <span data-ttu-id="d4525-308">Der namens Kontext muss beschreibbar sein, damit das Replikat erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4525-308">The naming context must be writeable in order to create the replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**Fehler " \_ DS- \_ ATT \_ nicht def" \_ \_ im \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="d4525-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-310">8303 (0x206f)</span><span class="sxs-lookup"><span data-stu-id="d4525-310">8303 (0x206F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-311">Ein Verweis auf ein Attribut, das nicht im Schema definiert ist, ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-311">A reference to an attribute that is not defined in the schema occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**Fehler \_ DS \_ Maximale \_ obj- \_ Größe \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="d4525-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERROR\_DS\_MAX\_OBJ\_SIZE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-313">8304 (0x2070)</span><span class="sxs-lookup"><span data-stu-id="d4525-313">8304 (0x2070)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-314">Die maximale Größe eines Objekts wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d4525-314">The maximum size of an object has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**Fehler \_ DS \_ obj \_ Zeichen folgen \_ Name ist \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR\_DS\_OBJ\_STRING\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-316">8305 (0x2071)</span><span class="sxs-lookup"><span data-stu-id="d4525-316">8305 (0x2071)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-317">Es wurde versucht, ein Objekt mit einem Namen, der bereits verwendet wird, dem Verzeichnis hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4525-317">An attempt was made to add an object to the directory with a name that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**Fehler \_ - \_ DS \_ \_ \_ im \_ Schema ist kein RDN definiert.**</span><span class="sxs-lookup"><span data-stu-id="d4525-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR\_DS\_NO\_RDN\_DEFINED\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-319">8306 (0x2072)</span><span class="sxs-lookup"><span data-stu-id="d4525-319">8306 (0x2072)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-320">Es wurde versucht, ein Objekt einer Klasse hinzuzufügen, für die im Schema kein RDN definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-320">An attempt was made to add an object of a class that does not have an RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**Fehler \_ DS \_ RDN \_ stimmt nicht \_ mit \_ Schema identisch**</span><span class="sxs-lookup"><span data-stu-id="d4525-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERROR\_DS\_RDN\_DOESNT\_MATCH\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-322">8307 (0x2073)</span><span class="sxs-lookup"><span data-stu-id="d4525-322">8307 (0x2073)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-323">Es wurde versucht, ein Objekt mithilfe eines RDN hinzuzufügen, der nicht dem im Schema definierten RDN entspricht.</span><span class="sxs-lookup"><span data-stu-id="d4525-323">An attempt was made to add an object using an RDN that is not the RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**Fehler \_ DS \_ keine \_ angeforderten \_ ATTS \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR\_DS\_NO\_REQUESTED\_ATTS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-325">8308 (0x2074)</span><span class="sxs-lookup"><span data-stu-id="d4525-325">8308 (0x2074)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-326">Keines der angeforderten Attribute wurde für die Objekte gefunden.</span><span class="sxs-lookup"><span data-stu-id="d4525-326">None of the requested attributes were found on the objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**Fehler " \_ DS- \_ Benutzer \_ Puffer \_ zu \_ klein"**</span><span class="sxs-lookup"><span data-stu-id="d4525-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR\_DS\_USER\_BUFFER\_TO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-328">8309 (0x2075)</span><span class="sxs-lookup"><span data-stu-id="d4525-328">8309 (0x2075)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-329">Der Benutzer Puffer ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="d4525-329">The user buffer is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**Fehler " \_ DS \_ ATT" \_ befindet sich \_ nicht \_ im \_ obj.**</span><span class="sxs-lookup"><span data-stu-id="d4525-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR\_DS\_ATT\_IS\_NOT\_ON\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-331">8310 (0x2076)</span><span class="sxs-lookup"><span data-stu-id="d4525-331">8310 (0x2076)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-332">Das im-Vorgang angegebene-Attribut ist für das-Objekt nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-332">The attribute specified in the operation is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**Fehler DS unzulässiger \_ \_ mod- \_ \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="d4525-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR\_DS\_ILLEGAL\_MOD\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-334">8311 (0x2077)</span><span class="sxs-lookup"><span data-stu-id="d4525-334">8311 (0x2077)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-335">Ungültiger Änderungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d4525-335">Illegal modify operation.</span></span> <span data-ttu-id="d4525-336">Ein Aspekt der Änderung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-336">Some aspect of the modification is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**Fehler " \_ DS \_ obj" \_ zu \_ groß.**</span><span class="sxs-lookup"><span data-stu-id="d4525-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERROR\_DS\_OBJ\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-338">8312 (0x2078)</span><span class="sxs-lookup"><span data-stu-id="d4525-338">8312 (0x2078)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-339">Das angegebene Objekt ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="d4525-339">The specified object is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**Fehler \_ DS fehlerhafter \_ \_ \_ Instanztyp**</span><span class="sxs-lookup"><span data-stu-id="d4525-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERROR\_DS\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-341">8313 (0x2079)</span><span class="sxs-lookup"><span data-stu-id="d4525-341">8313 (0x2079)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-342">Der angegebene Instanztyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-342">The specified instance type is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**Fehler- \_ DS- \_ MasterDSA \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4525-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR\_DS\_MASTERDSA\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-344">8314 (0x207a)</span><span class="sxs-lookup"><span data-stu-id="d4525-344">8314 (0x207A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-345">Der Vorgang muss an einer Master-DSA ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-345">The operation must be performed at a master DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**Fehler- \_ DS- \_ Objekt \_ Klasse \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4525-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**ERROR\_DS\_OBJECT\_CLASS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-347">8315 (0x207b)</span><span class="sxs-lookup"><span data-stu-id="d4525-347">8315 (0x207B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-348">Das Objektklassen Attribut muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-348">The object class attribute must be specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**Fehler- \_ DS \_ fehlendes \_ Erforderliches \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="d4525-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR\_DS\_MISSING\_REQUIRED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-350">8316 (0x207c)</span><span class="sxs-lookup"><span data-stu-id="d4525-350">8316 (0x207C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-351">Ein erforderliches Attribut fehlt.</span><span class="sxs-lookup"><span data-stu-id="d4525-351">A required attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**Fehler \_ DS- \_ ATT \_ nicht \_ DEF \_ für \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="d4525-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_FOR\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-353">8317 (0x207d)</span><span class="sxs-lookup"><span data-stu-id="d4525-353">8317 (0x207D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-354">Es wurde versucht, ein Objekt so zu ändern, dass es ein Attribut enthält, das für seine Klasse nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-354">An attempt was made to modify an object to include an attribute that is not legal for its class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**Fehler \_ DS- \_ ATT ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERROR\_DS\_ATT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-356">8318 (0x207e)</span><span class="sxs-lookup"><span data-stu-id="d4525-356">8318 (0x207E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-357">Das angegebene Attribut ist für das Objekt bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-357">The specified attribute is already present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**Fehler \_ DS Fehler beim \_ \_ Hinzufügen von \_ ATT- \_ Werten**</span><span class="sxs-lookup"><span data-stu-id="d4525-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR\_DS\_CANT\_ADD\_ATT\_VALUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-359">8320 (0x2080)</span><span class="sxs-lookup"><span data-stu-id="d4525-359">8320 (0x2080)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-360">Das angegebene Attribut ist nicht vorhanden oder weist keine Werte auf.</span><span class="sxs-lookup"><span data-stu-id="d4525-360">The specified attribute is not present, or has no values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**Fehler- \_ DS- \_ Einschränkung mit einem \_ Wert \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR\_DS\_SINGLE\_VALUE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-362">8321 (0x2081)</span><span class="sxs-lookup"><span data-stu-id="d4525-362">8321 (0x2081)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-363">Für ein Attribut, das nur über einen Wert verfügen kann, wurden mehrere Werte angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4525-363">Multiple values were specified for an attribute that can have only one value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**Fehler- \_ DS- \_ Bereichs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="d4525-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERROR\_DS\_RANGE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-365">8322 (0x2082)</span><span class="sxs-lookup"><span data-stu-id="d4525-365">8322 (0x2082)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-366">Ein Wert für das-Attribut war nicht im zulässigen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="d4525-366">A value for the attribute was not in the acceptable range of values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**Fehler \_ DS \_ ATT \_ Val ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERROR\_DS\_ATT\_VAL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-368">8323 (0x2083)</span><span class="sxs-lookup"><span data-stu-id="d4525-368">8323 (0x2083)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-369">Der angegebene Wert ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-369">The specified value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**Fehler DS-Fehler " \_ DS nicht \_ \_ \_ vorhanden \_ ".**</span><span class="sxs-lookup"><span data-stu-id="d4525-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-371">8324 (0x2084)</span><span class="sxs-lookup"><span data-stu-id="d4525-371">8324 (0x2084)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-372">Das Attribut kann nicht entfernt werden, weil es für das Objekt nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-372">The attribute cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**Fehler \_ " \_ DS \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT\_VAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-374">8325 (0x2085)</span><span class="sxs-lookup"><span data-stu-id="d4525-374">8325 (0x2085)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-375">Der Attribut Wert kann nicht entfernt werden, weil er im Objekt nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-375">The attribute value cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**Fehler "DS-Stamm" darf kein unter Bericht \_ \_ \_ \_ sein \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR\_DS\_ROOT\_CANT\_BE\_SUBREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-377">8326 (0x2086)</span><span class="sxs-lookup"><span data-stu-id="d4525-377">8326 (0x2086)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-378">Das angegebene Stamm Objekt kann kein unter Bericht sein.</span><span class="sxs-lookup"><span data-stu-id="d4525-378">The specified root object cannot be a subref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**Fehler- \_ DS \_ keine \_ Verkettung**</span><span class="sxs-lookup"><span data-stu-id="d4525-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR\_DS\_NO\_CHAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-380">8327 (0x2087)</span><span class="sxs-lookup"><span data-stu-id="d4525-380">8327 (0x2087)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-381">Verkettung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-381">Chaining is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**Fehler- \_ DS \_ keine \_ verkettete \_ Eval**</span><span class="sxs-lookup"><span data-stu-id="d4525-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR\_DS\_NO\_CHAINED\_EVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-383">8328 (0x2088)</span><span class="sxs-lookup"><span data-stu-id="d4525-383">8328 (0x2088)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-384">Verkettete Auswertung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-384">Chained evaluation is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**Fehler " \_ DS \_ kein über \_ geordnetes \_ Objekt"**</span><span class="sxs-lookup"><span data-stu-id="d4525-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR\_DS\_NO\_PARENT\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-386">8329 (0x2089)</span><span class="sxs-lookup"><span data-stu-id="d4525-386">8329 (0x2089)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-387">Der Vorgang konnte nicht ausgeführt werden, da das übergeordnete Objekt instanziiert oder gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="d4525-387">The operation could not be performed because the object's parent is either uninstantiated or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**Fehler- \_ DS über \_ geordnetes Element \_ ist \_ ein \_ Alias**</span><span class="sxs-lookup"><span data-stu-id="d4525-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERROR\_DS\_PARENT\_IS\_AN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-389">8330 (0x208a)</span><span class="sxs-lookup"><span data-stu-id="d4525-389">8330 (0x208A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-390">Ein übergeordnetes Element, das ein Alias ist, ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-390">Having a parent that is an alias is not permitted.</span></span> <span data-ttu-id="d4525-391">Aliase sind Blattobjekte.</span><span class="sxs-lookup"><span data-stu-id="d4525-391">Aliases are leaf objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**Fehler \_ -DS-Fehler beim \_ \_ Mischen von \_ Master \_ und \_ Reps**</span><span class="sxs-lookup"><span data-stu-id="d4525-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR\_DS\_CANT\_MIX\_MASTER\_AND\_REPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-393">8331 (0x208b)</span><span class="sxs-lookup"><span data-stu-id="d4525-393">8331 (0x208B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-394">Das Objekt und das übergeordnete Element müssen denselben Typ aufweisen, entweder sowohl Master als auch beide Replikate.</span><span class="sxs-lookup"><span data-stu-id="d4525-394">The object and parent must be of the same type, either both masters or both replicas.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**Fehler DS untergeordnete Elemente \_ \_ \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="d4525-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR\_DS\_CHILDREN\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-396">8332 (0x208c)</span><span class="sxs-lookup"><span data-stu-id="d4525-396">8332 (0x208C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-397">Der Vorgang kann nicht ausgeführt werden, da untergeordnete Objekte vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d4525-397">The operation cannot be performed because child objects exist.</span></span> <span data-ttu-id="d4525-398">Dieser Vorgang kann nur für ein Blatt Objekt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-398">This operation can only be performed on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**Fehler " \_ DS \_ obj" \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERROR\_DS\_OBJ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-400">8333 (0x208d)</span><span class="sxs-lookup"><span data-stu-id="d4525-400">8333 (0x208D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-401">Das Verzeichnis Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d4525-401">Directory object not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**Fehler \_ beim \_ Alias "Aliasing \_ obj". \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERROR\_DS\_ALIASED\_OBJ\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-403">8334 (0x208e)</span><span class="sxs-lookup"><span data-stu-id="d4525-403">8334 (0x208E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-404">Das Alias Objekt fehlt.</span><span class="sxs-lookup"><span data-stu-id="d4525-404">The aliased object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**Fehler DS-Syntax für ungültigen \_ \_ \_ Namen \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR\_DS\_BAD\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-406">8335 (0x208f)</span><span class="sxs-lookup"><span data-stu-id="d4525-406">8335 (0x208F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-407">Der Objektname weist eine ungültige Syntax auf.</span><span class="sxs-lookup"><span data-stu-id="d4525-407">The object name has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**Fehler- \_ DS- \_ Alias \_ verweist \_ auf \_ Alias**</span><span class="sxs-lookup"><span data-stu-id="d4525-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERROR\_DS\_ALIAS\_POINTS\_TO\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-409">8336 (0x2090)</span><span class="sxs-lookup"><span data-stu-id="d4525-409">8336 (0x2090)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-410">Es ist nicht zulässig, dass ein Alias auf einen anderen Alias verweist.</span><span class="sxs-lookup"><span data-stu-id="d4525-410">It is not permitted for an alias to refer to another alias.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**Fehler \_ DS \_ cant \_ Deref- \_ Alias**</span><span class="sxs-lookup"><span data-stu-id="d4525-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR\_DS\_CANT\_DEREF\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-412">8337 (0x2091)</span><span class="sxs-lookup"><span data-stu-id="d4525-412">8337 (0x2091)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-413">Der Alias kann nicht dereferenziert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-413">The alias cannot be dereferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**Fehler- \_ DS \_ außerhalb des Gültigkeits \_ \_ Bereichs**</span><span class="sxs-lookup"><span data-stu-id="d4525-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR\_DS\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-415">8338 (0x2092)</span><span class="sxs-lookup"><span data-stu-id="d4525-415">8338 (0x2092)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-416">Der Vorgang liegt außerhalb des Gültigkeits Bereichs.</span><span class="sxs-lookup"><span data-stu-id="d4525-416">The operation is out of scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**Fehler- \_ DS- \_ Objekt \_ wird \_ entfernt.**</span><span class="sxs-lookup"><span data-stu-id="d4525-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR\_DS\_OBJECT\_BEING\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-418">8339 (0x2093)</span><span class="sxs-lookup"><span data-stu-id="d4525-418">8339 (0x2093)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-419">Der Vorgang kann nicht fortgesetzt werden, da das Objekt gerade entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-419">The operation cannot continue because the object is in the process of being removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**Fehler \_ DS \_ , \_ \_ DSA- \_ obj nicht löschen**</span><span class="sxs-lookup"><span data-stu-id="d4525-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR\_DS\_CANT\_DELETE\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-421">8340 (0x2094)</span><span class="sxs-lookup"><span data-stu-id="d4525-421">8340 (0x2094)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-422">Das DSA-Objekt kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-422">The DSA object cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**Fehler \_ DS \_ allgemeiner \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**ERROR\_DS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-424">8341 (0x2095)</span><span class="sxs-lookup"><span data-stu-id="d4525-424">8341 (0x2095)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-425">Ein Verzeichnisdienst Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-425">A directory service error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**Fehler \_ DS \_ DSA \_ muss \_ \_ int \_ Master sein.**</span><span class="sxs-lookup"><span data-stu-id="d4525-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR\_DS\_DSA\_MUST\_BE\_INT\_MASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-427">8342 (0x2096)</span><span class="sxs-lookup"><span data-stu-id="d4525-427">8342 (0x2096)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-428">Der Vorgang kann nur auf einem internen Master-DSA-Objekt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-428">The operation can only be performed on an internal master DSA object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**Fehler- \_ DS- \_ Klasse \_ nicht \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="d4525-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR\_DS\_CLASS\_NOT\_DSA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-430">8343 (0x2097)</span><span class="sxs-lookup"><span data-stu-id="d4525-430">8343 (0x2097)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-431">Das Objekt muss aus der Klasse DSA bestehen.</span><span class="sxs-lookup"><span data-stu-id="d4525-431">The object must be of class DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**Fehler \_ DS \_ sichert \_ Zugriffs \_ Rechte**</span><span class="sxs-lookup"><span data-stu-id="d4525-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERROR\_DS\_INSUFF\_ACCESS\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-433">8344 (0x2098)</span><span class="sxs-lookup"><span data-stu-id="d4525-433">8344 (0x2098)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-434">Unzureichende Zugriffsrechte zum Ausführen des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d4525-434">Insufficient access rights to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**Fehler-DS unzulässig. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR\_DS\_ILLEGAL\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-436">8345 (0x2099)</span><span class="sxs-lookup"><span data-stu-id="d4525-436">8345 (0x2099)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-437">Das Objekt kann nicht hinzugefügt werden, da das übergeordnete Element nicht in der Liste der möglichen Vorgesetzten enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-437">The object cannot be added because the parent is not on the list of possible superiors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**Fehler- \_ DS- \_ Attribut \_ im Besitz \_ von \_ Sam**</span><span class="sxs-lookup"><span data-stu-id="d4525-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERROR\_DS\_ATTRIBUTE\_OWNED\_BY\_SAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-439">8346 (0x209a)</span><span class="sxs-lookup"><span data-stu-id="d4525-439">8346 (0x209A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-440">Der Zugriff auf das-Attribut ist nicht zulässig, da das-Attribut im Besitz der Sicherheits Konten Verwaltung (Security Accounts Manager, Sam) ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-440">Access to the attribute is not permitted because the attribute is owned by the Security Accounts Manager (SAM).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**Fehler- \_ DS- \_ Name \_ zu \_ viele \_ Teile**</span><span class="sxs-lookup"><span data-stu-id="d4525-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR\_DS\_NAME\_TOO\_MANY\_PARTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-442">8347 (0x209b)</span><span class="sxs-lookup"><span data-stu-id="d4525-442">8347 (0x209B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-443">Der Name enthält zu viele Teile.</span><span class="sxs-lookup"><span data-stu-id="d4525-443">The name has too many parts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**Fehler- \_ DS- \_ Name \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="d4525-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR\_DS\_NAME\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-445">8348 (0x209c)</span><span class="sxs-lookup"><span data-stu-id="d4525-445">8348 (0x209C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-446">Der Name ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="d4525-446">The name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**Fehler \_ DS- \_ namens \_ Wert \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="d4525-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERROR\_DS\_NAME\_VALUE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-448">8349 (0x209d)</span><span class="sxs-lookup"><span data-stu-id="d4525-448">8349 (0x209D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-449">Der Name-Wert ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="d4525-449">The name value is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**Fehler " \_ DS- \_ Name" \_ kann nicht analysiert werden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR\_DS\_NAME\_UNPARSEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-451">8350 (0x209e)</span><span class="sxs-lookup"><span data-stu-id="d4525-451">8350 (0x209E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-452">Der Verzeichnisdienst hat einen Fehler beim Auswerten eines Namens gefunden.</span><span class="sxs-lookup"><span data-stu-id="d4525-452">The directory service encountered an error parsing a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**Fehler beim \_ DS- \_ \_ Namenstyp \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="d4525-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR\_DS\_NAME\_TYPE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-454">8351 (0x209f)</span><span class="sxs-lookup"><span data-stu-id="d4525-454">8351 (0x209F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-455">Der Verzeichnisdienst kann den Attributtyp für einen Namen nicht erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4525-455">The directory service cannot get the attribute type for a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**Fehler- \_ DS ist \_ kein \_ \_ Objekt.**</span><span class="sxs-lookup"><span data-stu-id="d4525-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR\_DS\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-457">8352 (0x20a0)</span><span class="sxs-lookup"><span data-stu-id="d4525-457">8352 (0x20A0)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-458">Der Name identifiziert kein Objekt. der Name identifiziert einen Phantom.</span><span class="sxs-lookup"><span data-stu-id="d4525-458">The name does not identify an object; the name identifies a phantom.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**Fehler " \_ DS \_ Sek. \_ \_ zu \_ kurz"**</span><span class="sxs-lookup"><span data-stu-id="d4525-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR\_DS\_SEC\_DESC\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-460">8353 (0x20a1)</span><span class="sxs-lookup"><span data-stu-id="d4525-460">8353 (0x20A1)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-461">Die Sicherheits Beschreibung ist zu kurz.</span><span class="sxs-lookup"><span data-stu-id="d4525-461">The security descriptor is too short.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**Fehler \_ DS \_ Sek., \_ \_ Ungültiger Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR\_DS\_SEC\_DESC\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-463">8354 (0x20a2)</span><span class="sxs-lookup"><span data-stu-id="d4525-463">8354 (0x20A2)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-464">Die Sicherheits Beschreibung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-464">The security descriptor is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**Fehler " \_ DS \_ kein \_ gelöschter \_ Name"**</span><span class="sxs-lookup"><span data-stu-id="d4525-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR\_DS\_NO\_DELETED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-466">8355 (0x20a3)</span><span class="sxs-lookup"><span data-stu-id="d4525-466">8355 (0x20A3)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-467">Fehler beim Erstellen des Namens für das gelöschte Objekt.</span><span class="sxs-lookup"><span data-stu-id="d4525-467">Failed to create name for deleted object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**Fehler-DS-unter Bericht \_ \_ \_ muss \_ übergeordnetes Element aufweisen \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERROR\_DS\_SUBREF\_MUST\_HAVE\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-469">8356 (0x20a4)</span><span class="sxs-lookup"><span data-stu-id="d4525-469">8356 (0x20A4)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-470">Das übergeordnete Element eines neuen unter Berichts muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d4525-470">The parent of a new subref must exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**Fehler \_ ' \_ NCName ' \_ muss ' \_ NC ' sein \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR\_DS\_NCNAME\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-472">8357 (0x20a5)</span><span class="sxs-lookup"><span data-stu-id="d4525-472">8357 (0x20A5)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-473">Das Objekt muss ein namens Kontext sein.</span><span class="sxs-lookup"><span data-stu-id="d4525-473">The object must be a naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**Fehler DS-Fehler beim \_ \_ \_ Hinzufügen des \_ Systems \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR\_DS\_CANT\_ADD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-475">8358 (0x20a6)</span><span class="sxs-lookup"><span data-stu-id="d4525-475">8358 (0x20A6)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-476">Es ist nicht zulässig, ein Attribut hinzuzufügen, das im Besitz des Systems ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-476">It is not permitted to add an attribute which is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**Fehler- \_ DS- \_ Klasse \_ muss \_ \_ konkret sein**</span><span class="sxs-lookup"><span data-stu-id="d4525-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**ERROR\_DS\_CLASS\_MUST\_BE\_CONCRETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-478">8359 (0x20a7)</span><span class="sxs-lookup"><span data-stu-id="d4525-478">8359 (0x20A7)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-479">Die Klasse des Objekts muss strukturell sein. eine abstrakte Klasse kann nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-479">The class of the object must be structural; you cannot instantiate an abstract class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**Fehler- \_ DS \_ ungültige \_ DMD**</span><span class="sxs-lookup"><span data-stu-id="d4525-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR\_DS\_INVALID\_DMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-481">8360 (0x20a8)</span><span class="sxs-lookup"><span data-stu-id="d4525-481">8360 (0x20A8)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-482">Das Schema Objekt konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-482">The schema object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**Fehler \_ DS \_ obj- \_ GUID \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="d4525-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERROR\_DS\_OBJ\_GUID\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-484">8361 (0x20a9)</span><span class="sxs-lookup"><span data-stu-id="d4525-484">8361 (0x20A9)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-485">Ein lokales Objekt mit dieser GUID ("Dead" oder "Alive") ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-485">A local object with this GUID (dead or alive) already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**Fehler- \_ DS \_ nicht \_ auf \_ Backlink**</span><span class="sxs-lookup"><span data-stu-id="d4525-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR\_DS\_NOT\_ON\_BACKLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-487">8362 (0x20aa)</span><span class="sxs-lookup"><span data-stu-id="d4525-487">8362 (0x20AA)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-488">Der Vorgang kann nicht für einen backbackink ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-488">The operation cannot be performed on a back link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**Fehler " \_ DS \_ No \_ CrossRef" \_ für \_ NC**</span><span class="sxs-lookup"><span data-stu-id="d4525-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR\_DS\_NO\_CROSSREF\_FOR\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-490">8363 (0x20ab)</span><span class="sxs-lookup"><span data-stu-id="d4525-490">8363 (0x20AB)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-491">Der Querverweis für den angegebenen Namens Kontext konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-491">The cross reference for the specified naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**Fehler-DS wird herunter \_ \_ \_ Gefahren**</span><span class="sxs-lookup"><span data-stu-id="d4525-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR\_DS\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-493">8364 (0x20ac)</span><span class="sxs-lookup"><span data-stu-id="d4525-493">8364 (0x20AC)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-494">Der Vorgang konnte nicht ausgeführt werden, da der Verzeichnisdienst heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-494">The operation could not be performed because the directory service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**Fehler \_ DS \_ unbekannter \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="d4525-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR\_DS\_UNKNOWN\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-496">8365 (0x20ad)</span><span class="sxs-lookup"><span data-stu-id="d4525-496">8365 (0x20AD)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-497">Das Verzeichnis Service Request ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-497">The directory service request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**Fehler \_ DS \_ ungültiger \_ Rollen \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="d4525-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR\_DS\_INVALID\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-499">8366 (0x20ae)</span><span class="sxs-lookup"><span data-stu-id="d4525-499">8366 (0x20AE)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-500">Das Rollen Besitzer Attribut konnte nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-500">The role owner attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**Fehler- \_ DS \_ konnte keine \_ Verbindung mit \_ dem Dienst**</span><span class="sxs-lookup"><span data-stu-id="d4525-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR\_DS\_COULDNT\_CONTACT\_FSMO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-502">8367 (0x20af)</span><span class="sxs-lookup"><span data-stu-id="d4525-502">8367 (0x20AF)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-503">Der angeforderte FSMO-Vorgang konnte nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-503">The requested FSMO operation failed.</span></span> <span data-ttu-id="d4525-504">Der aktuelle FSMO-Inhaber war nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="d4525-504">The current FSMO holder could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**Fehler- \_ DS- \_ Kreuz NC-DN- \_ \_ \_ Umbenennung**</span><span class="sxs-lookup"><span data-stu-id="d4525-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR\_DS\_CROSS\_NC\_DN\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-506">8368 (0x20b0)</span><span class="sxs-lookup"><span data-stu-id="d4525-506">8368 (0x20B0)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-507">Die Änderung eines DN in einem Benennungs Kontext ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-507">Modification of a DN across a naming context is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**Fehler \_ DS \_ nicht \_ \_ nur System \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR\_DS\_CANT\_MOD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-509">8369 (0x20b1)</span><span class="sxs-lookup"><span data-stu-id="d4525-509">8369 (0x20B1)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-510">Das Attribut kann nicht geändert werden, da es im Besitz des Systems ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-510">The attribute cannot be modified because it is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**nur Fehler- \_ DS- \_ Replikator \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR\_DS\_REPLICATOR\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-512">8370 (0x20b2)</span><span class="sxs-lookup"><span data-stu-id="d4525-512">8370 (0x20B2)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-513">Diese Funktion kann nur vom Replikator durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-513">Only the replicator can perform this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**Fehler \_ DS \_ obj- \_ Klasse \_ nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="d4525-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-515">8371 (0x20b3)</span><span class="sxs-lookup"><span data-stu-id="d4525-515">8371 (0x20B3)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-516">Die angegebene Klasse ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="d4525-516">The specified class is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**Fehler \_ DS \_ obj- \_ Klasse \_ nicht \_ Unterklasse**</span><span class="sxs-lookup"><span data-stu-id="d4525-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_SUBCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-518">8372 (0x20b4)</span><span class="sxs-lookup"><span data-stu-id="d4525-518">8372 (0x20B4)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-519">Die angegebene Klasse ist keine Unterklasse.</span><span class="sxs-lookup"><span data-stu-id="d4525-519">The specified class is not a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**Fehler \_ DS- \_ namens \_ Verweis \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="d4525-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR\_DS\_NAME\_REFERENCE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-521">8373 (0x20b5)</span><span class="sxs-lookup"><span data-stu-id="d4525-521">8373 (0x20B5)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-522">Der namens Verweis ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-522">The name reference is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**Fehler \_ DS-Querverweis ist \_ \_ \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERROR\_DS\_CROSS\_REF\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-524">8374 (0x20b6)</span><span class="sxs-lookup"><span data-stu-id="d4525-524">8374 (0x20B6)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-525">Ein Querverweis ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-525">A cross reference already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**Fehler- \_ DS-del-Master- \_ \_ \_ \_ CrossRef**</span><span class="sxs-lookup"><span data-stu-id="d4525-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR\_DS\_CANT\_DEL\_MASTER\_CROSSREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-527">8375 (0x20b7)</span><span class="sxs-lookup"><span data-stu-id="d4525-527">8375 (0x20B7)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-528">Es ist nicht zulässig, einen Master-Querverweis zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d4525-528">It is not permitted to delete a master cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**Fehler- \_ DS- \_ Teilstruktur \_ Benachrichtigung \_ nicht NC- \_ \_ Kopfzeile**</span><span class="sxs-lookup"><span data-stu-id="d4525-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR\_DS\_SUBTREE\_NOTIFY\_NOT\_NC\_HEAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-530">8376 (0x20b8)</span><span class="sxs-lookup"><span data-stu-id="d4525-530">8376 (0x20B8)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-531">Teilstruktur Benachrichtigungen werden nur auf NC-Köpfen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-531">Subtree notifications are only supported on NC heads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**Fehler- \_ DS \_ Benachrichtigungs \_ Filter \_ zu \_ Komplex**</span><span class="sxs-lookup"><span data-stu-id="d4525-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR\_DS\_NOTIFY\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-533">8377 (0x20b9)</span><span class="sxs-lookup"><span data-stu-id="d4525-533">8377 (0x20B9)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-534">Der Benachrichtigungs Filter ist zu komplex.</span><span class="sxs-lookup"><span data-stu-id="d4525-534">Notification filter is too complex.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**Fehler \_ DS \_ DUP \_ RDN**</span><span class="sxs-lookup"><span data-stu-id="d4525-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR\_DS\_DUP\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-536">8378 (0x20ba)</span><span class="sxs-lookup"><span data-stu-id="d4525-536">8378 (0x20BA)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-537">Fehler beim Aktualisieren des Schemas: doppelter RDN.</span><span class="sxs-lookup"><span data-stu-id="d4525-537">Schema update failed: duplicate RDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**Fehler \_ DS \_ - \_ OID-OID**</span><span class="sxs-lookup"><span data-stu-id="d4525-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR\_DS\_DUP\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-539">8379 (0x20bb)</span><span class="sxs-lookup"><span data-stu-id="d4525-539">8379 (0x20BB)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-540">Fehler beim Aktualisieren des Schemas: doppelte OID.</span><span class="sxs-lookup"><span data-stu-id="d4525-540">Schema update failed: duplicate OID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**Fehler \_ DS \_ DUP- \_ MAPI- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d4525-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERROR\_DS\_DUP\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-542">8380 (0x20bc)</span><span class="sxs-lookup"><span data-stu-id="d4525-542">8380 (0x20BC)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-543">Fehler beim Aktualisieren des Schemas: doppelter MAPI-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d4525-543">Schema update failed: duplicate MAPI identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**Fehler- \_ DS-Schema-ID- \_ \_ \_ \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="d4525-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR\_DS\_DUP\_SCHEMA\_ID\_GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-545">8381 (0x20bd)</span><span class="sxs-lookup"><span data-stu-id="d4525-545">8381 (0x20BD)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-546">Fehler beim Aktualisieren des Schemas: doppelte Schema-ID-GUID.</span><span class="sxs-lookup"><span data-stu-id="d4525-546">Schema update failed: duplicate schema-id GUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**Fehler "DS", \_ \_ LDAP- \_ \_ Anzeige \_ Name**</span><span class="sxs-lookup"><span data-stu-id="d4525-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR\_DS\_DUP\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-548">8382 (0x20be)</span><span class="sxs-lookup"><span data-stu-id="d4525-548">8382 (0x20BE)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-549">Fehler beim Aktualisieren des Schemas: doppelter LDAP-Anzeige Name.</span><span class="sxs-lookup"><span data-stu-id="d4525-549">Schema update failed: duplicate LDAP display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**Fehler- \_ DS \_ Semantic ATT- \_ \_ Test**</span><span class="sxs-lookup"><span data-stu-id="d4525-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR\_DS\_SEMANTIC\_ATT\_TEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-551">8383 (0x20bf)</span><span class="sxs-lookup"><span data-stu-id="d4525-551">8383 (0x20BF)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-552">Fehler beim Aktualisieren des Schemas: Bereich-kleiner als oberer Bereich.</span><span class="sxs-lookup"><span data-stu-id="d4525-552">Schema update failed: range-lower less than range upper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**Fehler- \_ DS- \_ Syntax Konflikt \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR\_DS\_SYNTAX\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-554">8384 (0x20c0)</span><span class="sxs-lookup"><span data-stu-id="d4525-554">8384 (0x20C0)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-555">Fehler beim Aktualisieren des Schemas: Syntax stimmt nicht überein.</span><span class="sxs-lookup"><span data-stu-id="d4525-555">Schema update failed: syntax mismatch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**Fehler \_ - \_ DS \_ in \_ muss vorhanden \_ sein**</span><span class="sxs-lookup"><span data-stu-id="d4525-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**ERROR\_DS\_EXISTS\_IN\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-557">8385 (0x20c1)</span><span class="sxs-lookup"><span data-stu-id="d4525-557">8385 (0x20C1)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-558">Fehler beim Löschen des Schemas: das Attribut wird in "muss enthalten" verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4525-558">Schema deletion failed: attribute is used in must-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**\_der Fehler DS ist \_ \_ in \_ möglicherweise vorhanden \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**ERROR\_DS\_EXISTS\_IN\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-560">8386 (0x20c2)</span><span class="sxs-lookup"><span data-stu-id="d4525-560">8386 (0x20C2)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-561">Fehler beim Löschen des Schemas: das Attribut wird in "Mai" verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4525-561">Schema deletion failed: attribute is used in may-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**\_nicht vorhandene Fehler-DS \_ \_ verfügen möglicherweise \_ über**</span><span class="sxs-lookup"><span data-stu-id="d4525-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERROR\_DS\_NONEXISTENT\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-563">8387 (0x20c3)</span><span class="sxs-lookup"><span data-stu-id="d4525-563">8387 (0x20C3)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-564">Fehler beim Aktualisieren des Schemas: das Attribut in "May-" ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-564">Schema update failed: attribute in may-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**\_ \_ nicht vorhandener Fehler-DS \_ muss \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERROR\_DS\_NONEXISTENT\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-566">8388 (0x20c4)</span><span class="sxs-lookup"><span data-stu-id="d4525-566">8388 (0x20C4)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-567">Fehler beim Aktualisieren des Schemas: das Attribut in "" darf nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d4525-567">Schema update failed: attribute in must-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**Fehler \_ DS \_ aux \_ CLS- \_ Test \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="d4525-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR\_DS\_AUX\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-569">8389 (0x20c5)</span><span class="sxs-lookup"><span data-stu-id="d4525-569">8389 (0x20C5)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-570">Fehler beim Aktualisieren des Schemas: die Klasse in der Liste der aux-Klassen ist nicht vorhanden oder keine Erweiterungs Klasse.</span><span class="sxs-lookup"><span data-stu-id="d4525-570">Schema update failed: class in aux-class list does not exist or is not an auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**Fehler \_ DS \_ nicht vorhandener \_ Poss \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="d4525-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR\_DS\_NONEXISTENT\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-572">8390 (0x20c6)</span><span class="sxs-lookup"><span data-stu-id="d4525-572">8390 (0x20C6)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-573">Fehler beim Aktualisieren des Schemas: Klasse in Poss-Vorgesetzten ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-573">Schema update failed: class in poss-superiors does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**Fehler- \_ DS \_ unter \_ CLS- \_ Test \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="d4525-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR\_DS\_SUB\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-575">8391 (0x20c7)</span><span class="sxs-lookup"><span data-stu-id="d4525-575">8391 (0x20C7)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-576">Fehler beim Aktualisieren des Schemas: die Klasse in der Liste der Unterklassen ist nicht vorhanden oder entspricht nicht den Hierarchie Regeln.</span><span class="sxs-lookup"><span data-stu-id="d4525-576">Schema update failed: class in subclassof list does not exist or does not satisfy hierarchy rules.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**Fehler \_ DS fehlerhafte RDN-Fehler- \_ \_ \_ ID- \_ \_ Syntax**</span><span class="sxs-lookup"><span data-stu-id="d4525-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR\_DS\_BAD\_RDN\_ATT\_ID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-578">8392 (0x20c8)</span><span class="sxs-lookup"><span data-stu-id="d4525-578">8392 (0x20C8)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-579">Fehler beim Aktualisieren des Schemas: RDN-ATT-ID weist falsche Syntax auf.</span><span class="sxs-lookup"><span data-stu-id="d4525-579">Schema update failed: Rdn-Att-Id has wrong syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**Fehler \_ - \_ DS \_ in \_ aux \_ CLS**</span><span class="sxs-lookup"><span data-stu-id="d4525-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERROR\_DS\_EXISTS\_IN\_AUX\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-581">8393 (0x20c9)</span><span class="sxs-lookup"><span data-stu-id="d4525-581">8393 (0x20C9)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-582">Fehler beim Löschen des Schemas: die Klasse wird als Hilfsklasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4525-582">Schema deletion failed: class is used as auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**Fehler \_ - \_ DS \_ in \_ Sub \_ CLS**</span><span class="sxs-lookup"><span data-stu-id="d4525-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERROR\_DS\_EXISTS\_IN\_SUB\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-584">8394 (0x20ca)</span><span class="sxs-lookup"><span data-stu-id="d4525-584">8394 (0x20CA)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-585">Fehler beim Löschen des Schemas: die Klasse wird als Unterklasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4525-585">Schema deletion failed: class is used as sub class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**Fehler \_ - \_ DS \_ im \_ Poss- \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="d4525-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERROR\_DS\_EXISTS\_IN\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-587">8395 (0x20cb)</span><span class="sxs-lookup"><span data-stu-id="d4525-587">8395 (0x20CB)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-588">Fehler beim Löschen des Schemas: die Klasse wird als "Poss Superior" verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4525-588">Schema deletion failed: class is used as poss superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**Fehler bei \_ DS \_ recalcschema. \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR\_DS\_RECALCSCHEMA\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-590">8396 (0x20cc)</span><span class="sxs-lookup"><span data-stu-id="d4525-590">8396 (0x20CC)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-591">Fehler beim Neuberechnen des Überprüfungs Caches durch Schema Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="d4525-591">Schema update failed in recalculating validation cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**Fehler "DS-Struktur \_ \_ Löschen" \_ \_ nicht \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="d4525-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR\_DS\_TREE\_DELETE\_NOT\_FINISHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-593">8397 (0x20cd)</span><span class="sxs-lookup"><span data-stu-id="d4525-593">8397 (0x20CD)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-594">Das Löschen der Struktur ist nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d4525-594">The tree deletion is not finished.</span></span> <span data-ttu-id="d4525-595">Die Anforderung muss erneut erfolgen, damit das Löschen der Struktur fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4525-595">The request must be made again to continue deleting the tree.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**Fehler \_ DS \_ nicht \_ Löschen**</span><span class="sxs-lookup"><span data-stu-id="d4525-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR\_DS\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-597">8398 (0x20ce)</span><span class="sxs-lookup"><span data-stu-id="d4525-597">8398 (0x20CE)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-598">Der angeforderte Löschvorgang konnte nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-598">The requested delete operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**Fehler \_ - \_ \_ ID: DS-Schema- \_ req- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d4525-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-600">8399 (0x20cf)</span><span class="sxs-lookup"><span data-stu-id="d4525-600">8399 (0x20CF)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-601">Der Bearbeiter-Klassen Bezeichner für den Schema Daten Satz kann nicht gelesen werden</span><span class="sxs-lookup"><span data-stu-id="d4525-601">Cannot read the governs class identifier for the schema record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**Fehler \_ DS ungültige \_ ATT- \_ \_ Schema \_ Syntax**</span><span class="sxs-lookup"><span data-stu-id="d4525-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR\_DS\_BAD\_ATT\_SCHEMA\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-603">8400 (0x20d0)</span><span class="sxs-lookup"><span data-stu-id="d4525-603">8400 (0x20D0)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-604">Das Attribut Schema weist eine ungültige Syntax auf.</span><span class="sxs-lookup"><span data-stu-id="d4525-604">The attribute schema has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**Fehler " \_ DS- \_ cant- \_ Cache \_ "**</span><span class="sxs-lookup"><span data-stu-id="d4525-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR\_DS\_CANT\_CACHE\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-606">8401 (0x20d1)</span><span class="sxs-lookup"><span data-stu-id="d4525-606">8401 (0x20D1)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-607">Das Attribut konnte nicht zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-607">The attribute could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**Fehler- \_ DS-Klasse für den \_ \_ Cache \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR\_DS\_CANT\_CACHE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-609">8402 (0x20d2)</span><span class="sxs-lookup"><span data-stu-id="d4525-609">8402 (0x20D2)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-610">Die Klasse konnte nicht zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-610">The class could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**Fehler \_ DS Fehler beim \_ Entfernen des ATT- \_ \_ \_ Caches.**</span><span class="sxs-lookup"><span data-stu-id="d4525-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_ATT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-612">8403 (0x20d3)</span><span class="sxs-lookup"><span data-stu-id="d4525-612">8403 (0x20D3)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-613">Das Attribut konnte nicht aus dem Cache entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-613">The attribute could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**Fehler \_ DS Fehler beim \_ Entfernen des \_ \_ Klassen \_ Caches.**</span><span class="sxs-lookup"><span data-stu-id="d4525-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_CLASS\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-615">8404 (0x20d4)</span><span class="sxs-lookup"><span data-stu-id="d4525-615">8404 (0x20D4)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-616">Die Klasse konnte nicht aus dem Cache entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-616">The class could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**Fehler " \_ DS-DN nicht \_ \_ abgerufen \_ "**</span><span class="sxs-lookup"><span data-stu-id="d4525-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR\_DS\_CANT\_RETRIEVE\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-618">8405 (0x20d5)</span><span class="sxs-lookup"><span data-stu-id="d4525-618">8405 (0x20D5)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-619">Das Distinguished Name-Attribut konnte nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-619">The distinguished name attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**Fehler \_ DS \_ fehlende \_ supref**</span><span class="sxs-lookup"><span data-stu-id="d4525-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR\_DS\_MISSING\_SUPREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-621">8406 (0x20d6)</span><span class="sxs-lookup"><span data-stu-id="d4525-621">8406 (0x20D6)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-622">Im Verzeichnisdienst wurde kein übergeordneter Verweis konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d4525-622">No superior reference has been configured for the directory service.</span></span> <span data-ttu-id="d4525-623">Der Verzeichnisdienst kann daher keine Verweise auf Objekte außerhalb dieser Gesamtstruktur ausgeben.</span><span class="sxs-lookup"><span data-stu-id="d4525-623">The directory service is therefore unable to issue referrals to objects outside this forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**Fehler \_ DS-Instanz konnte nicht \_ \_ abgerufen \_ werden**</span><span class="sxs-lookup"><span data-stu-id="d4525-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR\_DS\_CANT\_RETRIEVE\_INSTANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-625">8407 (0x20d7)</span><span class="sxs-lookup"><span data-stu-id="d4525-625">8407 (0x20D7)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-626">Das Instanztyp Attribut konnte nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-626">The instance type attribute could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**Fehler \_ \_ Code Inkonsistenzen \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERROR\_DS\_CODE\_INCONSISTENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-628">8408 (0x20d8)</span><span class="sxs-lookup"><span data-stu-id="d4525-628">8408 (0x20D8)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-629">Ein interner Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-629">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**Fehler- \_ DS- \_ Daten Bank \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**ERROR\_DS\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-631">8409 (0x20d9)</span><span class="sxs-lookup"><span data-stu-id="d4525-631">8409 (0x20D9)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-632">Ein Datenbankfehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-632">A database error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**Fehler \_ DS \_ governdssid \_ fehlt.**</span><span class="sxs-lookup"><span data-stu-id="d4525-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR\_DS\_GOVERNSID\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-634">8410 (0x20da)</span><span class="sxs-lookup"><span data-stu-id="d4525-634">8410 (0x20DA)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-635">Das Attribut ' governsID ' fehlt.</span><span class="sxs-lookup"><span data-stu-id="d4525-635">The attribute GOVERNSID is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**Fehler- \_ DS \_ fehlen \_ Erwartetes \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="d4525-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR\_DS\_MISSING\_EXPECTED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-637">8411 (0x20db)</span><span class="sxs-lookup"><span data-stu-id="d4525-637">8411 (0x20DB)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-638">Ein erwartetes Attribut fehlt.</span><span class="sxs-lookup"><span data-stu-id="d4525-638">An expected attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**Fehler \_ DS \_ NCName \_ fehlt \_ CR \_ Ref**</span><span class="sxs-lookup"><span data-stu-id="d4525-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR\_DS\_NCNAME\_MISSING\_CR\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-640">8412 (0x20dc)</span><span class="sxs-lookup"><span data-stu-id="d4525-640">8412 (0x20DC)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-641">Im angegebenen Namens Kontext fehlt ein Querverweis.</span><span class="sxs-lookup"><span data-stu-id="d4525-641">The specified naming context is missing a cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**Fehler bei \_ DS- \_ Sicherheits \_ Überprüfung \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**ERROR\_DS\_SECURITY\_CHECKING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-643">8413 (0x20dd)</span><span class="sxs-lookup"><span data-stu-id="d4525-643">8413 (0x20DD)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-644">Ein Sicherheits Überprüfungs Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-644">A security checking error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**Fehler- \_ DS- \_ Schema \_ nicht \_ geladen**</span><span class="sxs-lookup"><span data-stu-id="d4525-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERROR\_DS\_SCHEMA\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-646">8414 (0x20de)</span><span class="sxs-lookup"><span data-stu-id="d4525-646">8414 (0x20DE)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-647">Das Schema wurde nicht geladen.</span><span class="sxs-lookup"><span data-stu-id="d4525-647">The schema is not loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**Fehler bei \_ DS- \_ Schema \_ Zuweisung \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR\_DS\_SCHEMA\_ALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-649">8415 (0x20df)</span><span class="sxs-lookup"><span data-stu-id="d4525-649">8415 (0x20DF)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-650">Fehler bei der Schema Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="d4525-650">Schema allocation failed.</span></span> <span data-ttu-id="d4525-651">Überprüfen Sie, ob auf dem Computer wenig Arbeitsspeicher verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-651">Please check if the machine is running low on memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**Fehler-DS-Error- \_ \_ Schema- \_ \_ req- \_ Syntax**</span><span class="sxs-lookup"><span data-stu-id="d4525-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-653">8416 (0x20e0)</span><span class="sxs-lookup"><span data-stu-id="d4525-653">8416 (0x20E0)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-654">Fehler beim Abrufen der erforderlichen Syntax für das Attribut Schema.</span><span class="sxs-lookup"><span data-stu-id="d4525-654">Failed to obtain the required syntax for the attribute schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**Fehler \_ DS \_ gcverify- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**ERROR\_DS\_GCVERIFY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-656">8417 (0x20e1)</span><span class="sxs-lookup"><span data-stu-id="d4525-656">8417 (0x20E1)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-657">Fehler bei der Überprüfung des globalen Katalogs.</span><span class="sxs-lookup"><span data-stu-id="d4525-657">The global catalog verification failed.</span></span> <span data-ttu-id="d4525-658">Der globale Katalog ist nicht verfügbar, oder der Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-658">The global catalog is not available or does not support the operation.</span></span> <span data-ttu-id="d4525-659">Ein Teil des Verzeichnisses ist zurzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4525-659">Some part of the directory is currently not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**Fehler \_ DS- \_ DRA- \_ Schema \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="d4525-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR\_DS\_DRA\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-661">8418 (0x20e2)</span><span class="sxs-lookup"><span data-stu-id="d4525-661">8418 (0x20E2)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-662">Fehler beim Replikations Vorgang aufgrund eines Schema Konflikts zwischen den beteiligten Servern.</span><span class="sxs-lookup"><span data-stu-id="d4525-662">The replication operation failed because of a schema mismatch between the servers involved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**Fehler \_ DS \_ - \_ \_ DSA- \_ obj nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="d4525-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR\_DS\_CANT\_FIND\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-664">8419 (0x20E3)</span><span class="sxs-lookup"><span data-stu-id="d4525-664">8419 (0x20E3)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-665">Das DSA-Objekt konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-665">The DSA object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**Fehler " \_ DS nicht \_ gefunden" \_ \_ erwartet \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR\_DS\_CANT\_FIND\_EXPECTED\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-667">8420 (0x20e4)</span><span class="sxs-lookup"><span data-stu-id="d4525-667">8420 (0x20E4)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-668">Der namens Kontext konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-668">The naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**Fehler \_ DS \_ - \_ \_ NC konnte \_ im \_ Cache nicht gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR\_DS\_CANT\_FIND\_NC\_IN\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-670">8421 (0x20e5)</span><span class="sxs-lookup"><span data-stu-id="d4525-670">8421 (0x20E5)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-671">Der namens Kontext konnte im Cache nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-671">The naming context could not be found in the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**Fehler DS nicht untergeordnetes Element \_ \_ \_ Abrufen \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR\_DS\_CANT\_RETRIEVE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-673">8422 (0x20e6)</span><span class="sxs-lookup"><span data-stu-id="d4525-673">8422 (0x20E6)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-674">Das untergeordnete Objekt konnte nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-674">The child object could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**Fehler-DS-Sicherheit unzulässige \_ \_ \_ \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="d4525-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR\_DS\_SECURITY\_ILLEGAL\_MODIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-676">8423 (0x20e7)</span><span class="sxs-lookup"><span data-stu-id="d4525-676">8423 (0x20E7)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-677">Die Änderung ist aus Sicherheitsgründen nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-677">The modification was not permitted for security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**Fehler DS-Fehler beim \_ \_ Ersetzen des \_ \_ verborgenen \_ rec**</span><span class="sxs-lookup"><span data-stu-id="d4525-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR\_DS\_CANT\_REPLACE\_HIDDEN\_REC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-679">8424 (0x20e8)</span><span class="sxs-lookup"><span data-stu-id="d4525-679">8424 (0x20E8)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-680">Der Vorgang kann den verborgenen Datensatz nicht ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d4525-680">The operation cannot replace the hidden record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**Fehler \_ DS ungültige \_ \_ Hierarchie \_ Datei.**</span><span class="sxs-lookup"><span data-stu-id="d4525-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERROR\_DS\_BAD\_HIERARCHY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-682">8425 (0x20e9)</span><span class="sxs-lookup"><span data-stu-id="d4525-682">8425 (0x20E9)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-683">Die Hierarchie Datei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-683">The hierarchy file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**Fehler bei \_ DS-buildhierarchie- \_ \_ \_ Tabelle \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR\_DS\_BUILD\_HIERARCHY\_TABLE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-685">8426 (0x20ea)</span><span class="sxs-lookup"><span data-stu-id="d4525-685">8426 (0x20EA)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-686">Fehler beim Erstellen der Hierarchie Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d4525-686">The attempt to build the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**Fehler \_ DS- \_ Konfigurationsparameter \_ \_ fehlt.**</span><span class="sxs-lookup"><span data-stu-id="d4525-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR\_DS\_CONFIG\_PARAM\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-688">8427 (0x20eb)</span><span class="sxs-lookup"><span data-stu-id="d4525-688">8427 (0x20EB)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-689">Der Verzeichnis Konfigurationsparameter fehlt in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d4525-689">The directory configuration parameter is missing from the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**Fehler \_ beim \_ zählen der ab- \_ \_ Indizes \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR\_DS\_COUNTING\_AB\_INDICES\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-691">8428 (0x20ec)</span><span class="sxs-lookup"><span data-stu-id="d4525-691">8428 (0x20EC)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-692">Der Versuch, die Adressbuch Indizes zu zählen, ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="d4525-692">The attempt to count the address book indices failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**Fehler bei \_ DS- \_ Hierarchie \_ Tabelle \_ malloc \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_MALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-694">8429 (0x20ed)</span><span class="sxs-lookup"><span data-stu-id="d4525-694">8429 (0x20ED)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-695">Die Zuordnung der Hierarchie Tabelle ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="d4525-695">The allocation of the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**Interner Fehler bei \_ DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR\_DS\_INTERNAL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-697">8430 (0x20ee)</span><span class="sxs-lookup"><span data-stu-id="d4525-697">8430 (0x20EE)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-698">Der Verzeichnisdienst hat einen internen Fehler ermittelt.</span><span class="sxs-lookup"><span data-stu-id="d4525-698">The directory service encountered an internal failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**\_unbekannter Fehler DS. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**ERROR\_DS\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-700">8431 (0x20ef)</span><span class="sxs-lookup"><span data-stu-id="d4525-700">8431 (0x20EF)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-701">Unbekannter Fehler beim Verzeichnisdienst.</span><span class="sxs-lookup"><span data-stu-id="d4525-701">The directory service encountered an unknown failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**Fehler-DS-Stamm \_ \_ \_ erfordert \_ Klasse \_ Top**</span><span class="sxs-lookup"><span data-stu-id="d4525-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERROR\_DS\_ROOT\_REQUIRES\_CLASS\_TOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-703">8432 (0x20f 0)</span><span class="sxs-lookup"><span data-stu-id="d4525-703">8432 (0x20F0)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-704">Ein Stamm Objekt erfordert die Klasse "Top".</span><span class="sxs-lookup"><span data-stu-id="d4525-704">A root object requires a class of 'top'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**Fehler- \_ DS lehnt die Rollen für die \_ \_ \_ Rollen Schutz**</span><span class="sxs-lookup"><span data-stu-id="d4525-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR\_DS\_REFUSING\_FSMO\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-706">8433 (0x20f 1)</span><span class="sxs-lookup"><span data-stu-id="d4525-706">8433 (0x20F1)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-707">Dieser Verzeichnisserver wird heruntergefahren und kann nicht in den Besitz neuer Gleit Komma Rollen für den Einzel Master Besitz gelangen.</span><span class="sxs-lookup"><span data-stu-id="d4525-707">This directory server is shutting down, and cannot take ownership of new floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**Fehler- \_ DS \_ fehlende \_ \_ Einstellungen für den Anmelde Namen**</span><span class="sxs-lookup"><span data-stu-id="d4525-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR\_DS\_MISSING\_FSMO\_SETTINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-709">8434 (0x20f 2)</span><span class="sxs-lookup"><span data-stu-id="d4525-709">8434 (0x20F2)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-710">Der Verzeichnisdienst weist keine obligatorischen Konfigurationsinformationen auf und kann den Besitz von Rollen Rollen mit nur einem Master nicht ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d4525-710">The directory service is missing mandatory configuration information, and is unable to determine the ownership of floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**Fehler \_ DS \_ beim \_ überlassen von \_ \_ Rollen nicht möglich**</span><span class="sxs-lookup"><span data-stu-id="d4525-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR\_DS\_UNABLE\_TO\_SURRENDER\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-712">8435 (0x20f 3)</span><span class="sxs-lookup"><span data-stu-id="d4525-712">8435 (0x20F3)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-713">Der Verzeichnisdienst konnte den Besitz von mindestens einer Gleit Komma Rolle für den Einzel Master nicht auf andere Server übertragen.</span><span class="sxs-lookup"><span data-stu-id="d4525-713">The directory service was unable to transfer ownership of one or more floating single-master operation roles to other servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**Fehler "DS", \_ \_ \_ generisch**</span><span class="sxs-lookup"><span data-stu-id="d4525-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR\_DS\_DRA\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-715">8436 (0x20f 4)</span><span class="sxs-lookup"><span data-stu-id="d4525-715">8436 (0x20F4)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-716">Fehler beim Replikations Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d4525-716">The replication operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**Fehler \_ DS- \_ DRA- \_ ungültiger \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="d4525-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR\_DS\_DRA\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-718">8437 (0x20f 5)</span><span class="sxs-lookup"><span data-stu-id="d4525-718">8437 (0x20F5)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-719">Für diesen Replikations Vorgang wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4525-719">An invalid parameter was specified for this replication operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**Fehler- \_ DS- \_ DRA \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="d4525-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR\_DS\_DRA\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-721">8438 (0x20f 6)</span><span class="sxs-lookup"><span data-stu-id="d4525-721">8438 (0x20F6)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-722">Der Verzeichnisdienst ist zu stark ausgelastet, um den Replikations Vorgang zu diesem Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d4525-722">The directory service is too busy to complete the replication operation at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**Fehler \_ DS DRA-fehlerhafter \_ \_ \_ DN**</span><span class="sxs-lookup"><span data-stu-id="d4525-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR\_DS\_DRA\_BAD\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-724">8439 (0x20f 7)</span><span class="sxs-lookup"><span data-stu-id="d4525-724">8439 (0x20F7)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-725">Der für diesen Replikations Vorgang angegebene Distinguished Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-725">The distinguished name specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**Fehler DS-DRA-fehlerhafter \_ \_ \_ \_ NC**</span><span class="sxs-lookup"><span data-stu-id="d4525-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR\_DS\_DRA\_BAD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-727">8440 (0x20f 8)</span><span class="sxs-lookup"><span data-stu-id="d4525-727">8440 (0x20F8)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-728">Der für diesen Replikations Vorgang angegebene Benennungs Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-728">The naming context specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**Fehler \_ DS- \_ DRA- \_ DN \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="d4525-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR\_DS\_DRA\_DN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-730">8441 (0x20f 9)</span><span class="sxs-lookup"><span data-stu-id="d4525-730">8441 (0x20F9)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-731">Der für diesen Replikations Vorgang angegebene Distinguished Name ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-731">The distinguished name specified for this replication operation already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**Fehler \_ DS \_ ( \_ interner DRA- \_ Fehler)**</span><span class="sxs-lookup"><span data-stu-id="d4525-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**ERROR\_DS\_DRA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-733">8442 (0x20fa)</span><span class="sxs-lookup"><span data-stu-id="d4525-733">8442 (0x20FA)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-734">Im Replikationssystem ist ein interner Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-734">The replication system encountered an internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**Fehler \_ DS- \_ DRA- \_ inkonsistente \_ dit**</span><span class="sxs-lookup"><span data-stu-id="d4525-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR\_DS\_DRA\_INCONSISTENT\_DIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-736">8443 (0x20fb)</span><span class="sxs-lookup"><span data-stu-id="d4525-736">8443 (0x20FB)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-737">Beim Replikations Vorgang ist eine Daten Bank Inkonsistenz aufgetreten</span><span class="sxs-lookup"><span data-stu-id="d4525-737">The replication operation encountered a database inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**Fehler \_ bei \_ dsdra- \_ Verbindungs \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="d4525-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR\_DS\_DRA\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-739">8444 (0x20fc)</span><span class="sxs-lookup"><span data-stu-id="d4525-739">8444 (0x20FC)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-740">Der für diesen Replikations Vorgang angegebene Server konnte nicht kontaktiert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-740">The server specified for this replication operation could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**Fehler DS-DRA-fehlerhafter \_ \_ \_ \_ \_ Instanztyp**</span><span class="sxs-lookup"><span data-stu-id="d4525-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR\_DS\_DRA\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-742">8445 (0x20fd)</span><span class="sxs-lookup"><span data-stu-id="d4525-742">8445 (0x20FD)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-743">Beim Replikations Vorgang ist ein Objekt mit einem ungültigen Instanztyp aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-743">The replication operation encountered an object with an invalid instance type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**Fehler- \_ DS- \_ DRA \_ nicht \_ \_ genügend Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="d4525-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR\_DS\_DRA\_OUT\_OF\_MEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-745">8446 (0x20fe)</span><span class="sxs-lookup"><span data-stu-id="d4525-745">8446 (0x20FE)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-746">Der Replikations Vorgang konnte keinen Arbeitsspeicher zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d4525-746">The replication operation failed to allocate memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**Fehler \_ DS- \_ DRA-Mail- \_ \_ Problem**</span><span class="sxs-lookup"><span data-stu-id="d4525-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR\_DS\_DRA\_MAIL\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-748">8447 (0x20ff)</span><span class="sxs-lookup"><span data-stu-id="d4525-748">8447 (0x20FF)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-749">Beim Replikations Vorgang ist ein Fehler im e-Mail-System aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-749">The replication operation encountered an error with the mail system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**Fehler \_ DS- \_ DRA-Ref ist \_ \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERROR\_DS\_DRA\_REF\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-751">8448 (0x2100)</span><span class="sxs-lookup"><span data-stu-id="d4525-751">8448 (0x2100)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-752">Die Replikations Verweis Informationen für den Zielserver sind bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-752">The replication reference information for the target server already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**Fehler \_ DS- \_ DRA- \_ ref \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="d4525-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR\_DS\_DRA\_REF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-754">8449 (0x2101)</span><span class="sxs-lookup"><span data-stu-id="d4525-754">8449 (0x2101)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-755">Die Replikations Verweis Informationen für den Zielserver sind nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-755">The replication reference information for the target server does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**Fehler " \_ DS \_ DRA \_ obj" \_ ist \_ Rep \_ Source.**</span><span class="sxs-lookup"><span data-stu-id="d4525-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR\_DS\_DRA\_OBJ\_IS\_REP\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-757">8450 (0x2102)</span><span class="sxs-lookup"><span data-stu-id="d4525-757">8450 (0x2102)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-758">Der Benennungs Kontext kann nicht entfernt werden, da er auf einen anderen Server repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-758">The naming context cannot be removed because it is replicated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**Fehler \_ DS- \_ DRA-DB- \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**ERROR\_DS\_DRA\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-760">8451 (0x2103)</span><span class="sxs-lookup"><span data-stu-id="d4525-760">8451 (0x2103)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-761">Beim Replikations Vorgang ist ein Datenbankfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d4525-761">The replication operation encountered a database error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**Fehler- \_ DS \_ DRA \_ kein \_ Replikat**</span><span class="sxs-lookup"><span data-stu-id="d4525-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR\_DS\_DRA\_NO\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-763">8452 (0x2104)</span><span class="sxs-lookup"><span data-stu-id="d4525-763">8452 (0x2104)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-764">Der namens Kontext wird gerade entfernt oder nicht vom angegebenen Server repliziert.</span><span class="sxs-lookup"><span data-stu-id="d4525-764">The naming context is in the process of being removed or is not replicated from the specified server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**Fehler \_ DS- \_ DRA- \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="d4525-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR\_DS\_DRA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-766">8453 (0x2105)</span><span class="sxs-lookup"><span data-stu-id="d4525-766">8453 (0x2105)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-767">Der Replikations Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="d4525-767">Replication access was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**Fehler- \_ DS- \_ DRA \_ nicht \_ unterstützt**</span><span class="sxs-lookup"><span data-stu-id="d4525-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR\_DS\_DRA\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-769">8454 (0x2106)</span><span class="sxs-lookup"><span data-stu-id="d4525-769">8454 (0x2106)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-770">Der angeforderte Vorgang wird von dieser Version des Verzeichnis Dienstanbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-770">The requested operation is not supported by this version of the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**Fehler \_ DS- \_ DRA- \_ RPC \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="d4525-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR\_DS\_DRA\_RPC\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-772">8455 (0x2107)</span><span class="sxs-lookup"><span data-stu-id="d4525-772">8455 (0x2107)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-773">Der Remote Prozedur Rückruf für die Replikation wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d4525-773">The replication remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**Fehler \_ DS- \_ DRA- \_ Quelle \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="d4525-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERROR\_DS\_DRA\_SOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-775">8456 (0x2108)</span><span class="sxs-lookup"><span data-stu-id="d4525-775">8456 (0x2108)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-776">Der Quell Server lehnt zurzeit Replikations Anforderungen ab.</span><span class="sxs-lookup"><span data-stu-id="d4525-776">The source server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**Fehler \_ DS- \_ DRA- \_ Senke \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="d4525-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR\_DS\_DRA\_SINK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-778">8457 (0x2109)</span><span class="sxs-lookup"><span data-stu-id="d4525-778">8457 (0x2109)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-779">Der Zielserver lehnt zurzeit Replikations Anforderungen ab.</span><span class="sxs-lookup"><span data-stu-id="d4525-779">The destination server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**Fehler \_ DS- \_ DRA- \_ namens \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="d4525-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERROR\_DS\_DRA\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-781">8458 (0x210a)</span><span class="sxs-lookup"><span data-stu-id="d4525-781">8458 (0x210A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-782">Der Replikations Vorgang ist aufgrund eines Konflikts von Objektnamen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="d4525-782">The replication operation failed due to a collision of object names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**Fehler \_ DS- \_ DRA- \_ Quelle \_ neu installiert**</span><span class="sxs-lookup"><span data-stu-id="d4525-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR\_DS\_DRA\_SOURCE\_REINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-784">8459 (0x210b)</span><span class="sxs-lookup"><span data-stu-id="d4525-784">8459 (0x210B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-785">Die Replikations Quelle wurde neu installiert.</span><span class="sxs-lookup"><span data-stu-id="d4525-785">The replication source has been reinstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**Fehler \_ DS- \_ DRA \_ fehlt über \_ geordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="d4525-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR\_DS\_DRA\_MISSING\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-787">8460 (0x210c)</span><span class="sxs-lookup"><span data-stu-id="d4525-787">8460 (0x210C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-788">Der Replikations Vorgang ist fehlgeschlagen, da ein erforderliches übergeordnetes Objekt fehlt.</span><span class="sxs-lookup"><span data-stu-id="d4525-788">The replication operation failed because a required parent object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**Fehler \_ DS- \_ DRA \_ vorzeitig entfernt**</span><span class="sxs-lookup"><span data-stu-id="d4525-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR\_DS\_DRA\_PREEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-790">8461 (0x210d)</span><span class="sxs-lookup"><span data-stu-id="d4525-790">8461 (0x210D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-791">Der Replikations Vorgang wurde vorzeitig entfernt.</span><span class="sxs-lookup"><span data-stu-id="d4525-791">The replication operation was preempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**Fehler \_ DS- \_ DRA- \_ \_ Synchronisierung abbrechen**</span><span class="sxs-lookup"><span data-stu-id="d4525-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR\_DS\_DRA\_ABANDON\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-793">8462 (0x210e)</span><span class="sxs-lookup"><span data-stu-id="d4525-793">8462 (0x210E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-794">Der Versuch der Replikations Synchronisierung wurde aufgrund fehlender Updates abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d4525-794">The replication synchronization attempt was abandoned because of a lack of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**Fehler \_ DS- \_ DRA- \_ Herunterfahren**</span><span class="sxs-lookup"><span data-stu-id="d4525-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR\_DS\_DRA\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-796">8463 (0x210f)</span><span class="sxs-lookup"><span data-stu-id="d4525-796">8463 (0x210F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-797">Der Replikations Vorgang wurde beendet, da das System heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-797">The replication operation was terminated because the system is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**Fehler- \_ DS- \_ \_ inkompatible \_ partielle \_ Teilmenge**</span><span class="sxs-lookup"><span data-stu-id="d4525-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR\_DS\_DRA\_INCOMPATIBLE\_PARTIAL\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-799">8464 (0x2110)</span><span class="sxs-lookup"><span data-stu-id="d4525-799">8464 (0x2110)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-800">Fehler beim Synchronisierungs Versuch, weil der Ziel-DC derzeit darauf wartet, neue partielle Attribute aus der Quelle zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d4525-800">Synchronization attempt failed because the destination DC is currently waiting to synchronize new partial attributes from source.</span></span> <span data-ttu-id="d4525-801">Diese Bedingung ist normal, wenn eine aktuelle Schema Änderung den partiellen Attribut Satz geändert hat.</span><span class="sxs-lookup"><span data-stu-id="d4525-801">This condition is normal if a recent schema change modified the partial attribute set.</span></span> <span data-ttu-id="d4525-802">Der partielle Ziel Attribut Satz ist keine Teilmenge des partiellen Quell partiellen Attributs.</span><span class="sxs-lookup"><span data-stu-id="d4525-802">The destination partial attribute set is not a subset of source partial attribute set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**Fehler \_ DS- \_ DRA- \_ Quelle \_ ist \_ partielles \_ Replikat**</span><span class="sxs-lookup"><span data-stu-id="d4525-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERROR\_DS\_DRA\_SOURCE\_IS\_PARTIAL\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-804">8465 (0x2111)</span><span class="sxs-lookup"><span data-stu-id="d4525-804">8465 (0x2111)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-805">Fehler beim Replikations Synchronisierungs Versuch, weil ein Master Replikat versucht hat, eine Synchronisierung von einem Teil</span><span class="sxs-lookup"><span data-stu-id="d4525-805">The replication synchronization attempt failed because a master replica attempted to sync from a partial replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**Fehler bei der Verbindungsfehler- \_ \_ Verbindungs- \_ \_ Verbindungs \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="d4525-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR\_DS\_DRA\_EXTN\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-807">8466 (0x2112)</span><span class="sxs-lookup"><span data-stu-id="d4525-807">8466 (0x2112)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-808">Der für diesen Replikations Vorgang angegebene Server wurde kontaktiert, aber der Server konnte keinen zusätzlichen Server kontaktieren, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d4525-808">The server specified for this replication operation was contacted, but that server was unable to contact an additional server needed to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**Fehler " \_ DS- \_ Installations Schema nicht \_ \_ übereinstimmen"**</span><span class="sxs-lookup"><span data-stu-id="d4525-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR\_DS\_INSTALL\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-810">8467 (0x2113)</span><span class="sxs-lookup"><span data-stu-id="d4525-810">8467 (0x2113)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-811">Die Version des Verzeichnisdienst Schemas der Quell Gesamtstruktur ist nicht mit der Version des Verzeichnis Dienstanbieter auf diesem Computer kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d4525-811">The version of the directory service schema of the source forest is not compatible with the version of directory service on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**Fehler \_ DS \_ DUP- \_ Link- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d4525-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERROR\_DS\_DUP\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-813">8468 (0x2114)</span><span class="sxs-lookup"><span data-stu-id="d4525-813">8468 (0x2114)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-814">Fehler beim Aktualisieren des Schemas: Es ist bereits ein Attribut mit demselben Link Bezeichner vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-814">Schema update failed: An attribute with the same link identifier already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**Fehler \_ beim \_ Auflösen des Namens "DS" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR\_DS\_NAME\_ERROR\_RESOLVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-816">8469 (0x2115)</span><span class="sxs-lookup"><span data-stu-id="d4525-816">8469 (0x2115)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-817">Namens Übersetzung: generischer Verarbeitungsfehler.</span><span class="sxs-lookup"><span data-stu-id="d4525-817">Name translation: Generic processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**Fehler \_ DS- \_ namens \_ Fehler \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-819">8470 (0x2116)</span><span class="sxs-lookup"><span data-stu-id="d4525-819">8470 (0x2116)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-820">Namens Übersetzung: der Name oder unzureichende Rechte zum Anzeigen des Namens konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-820">Name translation: Could not find the name or insufficient right to see name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**Fehler \_ DS- \_ namens \_ Fehler ist \_ nicht \_ eindeutig.**</span><span class="sxs-lookup"><span data-stu-id="d4525-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-822">8471 (0x2117)</span><span class="sxs-lookup"><span data-stu-id="d4525-822">8471 (0x2117)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-823">Namens Übersetzung: der Eingabe Name ist mehreren Ausgabe Namen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d4525-823">Name translation: Input name mapped to more than one output name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**Fehler \_ DS \_ - \_ Name \_ keine \_ Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="d4525-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-825">8472 (0x2118)</span><span class="sxs-lookup"><span data-stu-id="d4525-825">8472 (0x2118)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-826">Namens Übersetzung: der Eingabe Name wurde gefunden, aber nicht das zugehörige Ausgabeformat.</span><span class="sxs-lookup"><span data-stu-id="d4525-826">Name translation: Input name found, but not the associated output format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**Fehler \_ DS- \_ Name \_ Fehler \_ Domäne \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERROR\_DS\_NAME\_ERROR\_DOMAIN\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-828">8473 (0x2119)</span><span class="sxs-lookup"><span data-stu-id="d4525-828">8473 (0x2119)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-829">Namens Übersetzung: Es konnte nicht vollständig aufgelöst werden. es wurde nur die Domäne gefunden.</span><span class="sxs-lookup"><span data-stu-id="d4525-829">Name translation: Unable to resolve completely, only the domain was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**Fehler \_ DS- \_ namens \_ Fehler \_ keine \_ syntaktische \_ Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="d4525-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_SYNTACTICAL\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-831">8474 (0x211a)</span><span class="sxs-lookup"><span data-stu-id="d4525-831">8474 (0x211A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-832">Namens Übersetzung: Es kann keine rein syntaktische Zuordnung auf dem Client ausgeführt werden, ohne dass die Verbindung übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-832">Name translation: Unable to perform purely syntactical mapping at the client without going out to the wire.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**Fehler- \_ DS, \_ erstellt, \_ ATT \_ mod**</span><span class="sxs-lookup"><span data-stu-id="d4525-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR\_DS\_CONSTRUCTED\_ATT\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-834">8475 (0x211b)</span><span class="sxs-lookup"><span data-stu-id="d4525-834">8475 (0x211B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-835">Die Änderung eines konstruierten Attributs ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-835">Modification of a constructed attribute is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**Fehler \_ DS \_ falsche \_ OM \_ obj- \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="d4525-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR\_DS\_WRONG\_OM\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-837">8476 (0x211c)</span><span class="sxs-lookup"><span data-stu-id="d4525-837">8476 (0x211C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-838">Die angegebene OM-Object-Klasse ist für ein Attribut mit der angegebenen Syntax falsch.</span><span class="sxs-lookup"><span data-stu-id="d4525-838">The OM-Object-Class specified is incorrect for an attribute with the specified syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**Fehler \_ DS- \_ DRA- \_ repl steht \_ aus.**</span><span class="sxs-lookup"><span data-stu-id="d4525-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR\_DS\_DRA\_REPL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-840">8477 (0x211d)</span><span class="sxs-lookup"><span data-stu-id="d4525-840">8477 (0x211D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-841">Die Replikations Anforderung wurde gepostet. warten auf Antwort.</span><span class="sxs-lookup"><span data-stu-id="d4525-841">The replication request has been posted; waiting for reply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**Fehler- \_ DS- \_ DS \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4525-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR\_DS\_DS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-843">8478 (0x211e)</span><span class="sxs-lookup"><span data-stu-id="d4525-843">8478 (0x211E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-844">Der angeforderte Vorgang erfordert einen Verzeichnisdienst, und keiner war verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4525-844">The requested operation requires a directory service, and none was available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**Fehler- \_ DS \_ ungültiger \_ LDAP- \_ Anzeige \_ Name.**</span><span class="sxs-lookup"><span data-stu-id="d4525-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR\_DS\_INVALID\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-846">8479 (0x211f)</span><span class="sxs-lookup"><span data-stu-id="d4525-846">8479 (0x211F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-847">Der LDAP-Anzeige Name der Klasse oder des Attributs enthält nicht-ASCII-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d4525-847">The LDAP display name of the class or attribute contains non-ASCII characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**Fehler- \_ DS, \_ nicht \_ Basis \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="d4525-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR\_DS\_NON\_BASE\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-849">8480 (0x2120)</span><span class="sxs-lookup"><span data-stu-id="d4525-849">8480 (0x2120)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-850">Der angeforderte Suchvorgang wird nur für Basis suchen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-850">The requested search operation is only supported for base searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**Fehler \_ beim \_ \_ Abrufen von \_ ATTS.**</span><span class="sxs-lookup"><span data-stu-id="d4525-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR\_DS\_CANT\_RETRIEVE\_ATTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-852">8481 (0x2121)</span><span class="sxs-lookup"><span data-stu-id="d4525-852">8481 (0x2121)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-853">Bei der Suche konnten keine Attribute aus der Datenbank abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-853">The search failed to retrieve attributes from the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**Fehler- \_ DS- \_ Backlink \_ ohne \_ Verknüpfung**</span><span class="sxs-lookup"><span data-stu-id="d4525-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR\_DS\_BACKLINK\_WITHOUT\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-855">8482 (0x2122)</span><span class="sxs-lookup"><span data-stu-id="d4525-855">8482 (0x2122)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-856">Beim Schema Aktualisierungs Vorgang wurde versucht, ein abwärts Verknüpfungs Attribut hinzuzufügen, das über keinen entsprechenden Forward-Link verfügt.</span><span class="sxs-lookup"><span data-stu-id="d4525-856">The schema update operation tried to add a backward link attribute that has no corresponding forward link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**Fehler \_ DS- \_ Epochen Konflikt \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR\_DS\_EPOCH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-858">8483 (0x2123)</span><span class="sxs-lookup"><span data-stu-id="d4525-858">8483 (0x2123)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-859">Quelle und Ziel einer Domänen übergreifenden Verschiebung stimmen nicht mit der Epochen Nummer des Objekts überein.</span><span class="sxs-lookup"><span data-stu-id="d4525-859">Source and destination of a cross-domain move do not agree on the object's epoch number.</span></span> <span data-ttu-id="d4525-860">Entweder die Quelle oder das Ziel hat nicht die neueste Version des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d4525-860">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**Fehler \_ DS- \_ src- \_ namens \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="d4525-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR\_DS\_SRC\_NAME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-862">8484 (0x2124)</span><span class="sxs-lookup"><span data-stu-id="d4525-862">8484 (0x2124)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-863">Quelle und Ziel einer Domänen übergreifenden Verschiebung stimmen nicht mit dem aktuellen Namen des Objekts überein.</span><span class="sxs-lookup"><span data-stu-id="d4525-863">Source and destination of a cross-domain move do not agree on the object's current name.</span></span> <span data-ttu-id="d4525-864">Entweder die Quelle oder das Ziel hat nicht die neueste Version des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d4525-864">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**Fehler \_ DS \_ src \_ und \_ DST \_ NC \_ identisch**</span><span class="sxs-lookup"><span data-stu-id="d4525-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR\_DS\_SRC\_AND\_DST\_NC\_IDENTICAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-866">8485 (0x2125)</span><span class="sxs-lookup"><span data-stu-id="d4525-866">8485 (0x2125)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-867">Quelle und Ziel für den Domänen übergreifenden Verschiebungs Vorgang sind identisch.</span><span class="sxs-lookup"><span data-stu-id="d4525-867">Source and destination for the cross-domain move operation are identical.</span></span> <span data-ttu-id="d4525-868">Der Aufrufer sollte anstelle eines Domänen übergreifenden Verschiebungs Vorgangs einen lokalen Verschiebungs Vorgang verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4525-868">Caller should use local move operation instead of cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**Fehler \_ DS \_ DST- \_ NC \_ -Konflikt**</span><span class="sxs-lookup"><span data-stu-id="d4525-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR\_DS\_DST\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-870">8486 (0x2126)</span><span class="sxs-lookup"><span data-stu-id="d4525-870">8486 (0x2126)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-871">Quelle und Ziel für eine Domänen übergreifende Verschiebung sind nicht in den Benennungs Kontexten in der Gesamtstruktur zu finden.</span><span class="sxs-lookup"><span data-stu-id="d4525-871">Source and destination for a cross-domain move are not in agreement on the naming contexts in the forest.</span></span> <span data-ttu-id="d4525-872">Entweder die Quelle oder das Ziel hat nicht die neueste Version des Partitions Containers.</span><span class="sxs-lookup"><span data-stu-id="d4525-872">Either source or destination does not have the latest version of the Partitions container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**Fehler- \_ DS \_ nicht \_ autoritative \_ für \_ DST \_ NC**</span><span class="sxs-lookup"><span data-stu-id="d4525-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR\_DS\_NOT\_AUTHORITIVE\_FOR\_DST\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-874">8487 (0x2127)</span><span class="sxs-lookup"><span data-stu-id="d4525-874">8487 (0x2127)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-875">Das Ziel einer Domänen übergreifenden Verschiebung ist für den Ziel namens Kontext nicht autoritativ.</span><span class="sxs-lookup"><span data-stu-id="d4525-875">Destination of a cross-domain move is not authoritative for the destination naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**Fehler- \_ DS- \_ src- \_ GUID-Konflikt \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR\_DS\_SRC\_GUID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-877">8488 (0x2128)</span><span class="sxs-lookup"><span data-stu-id="d4525-877">8488 (0x2128)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-878">Quelle und Ziel einer Domänen übergreifenden Verschiebung stimmen nicht mit der Identität des Quell Objekts überein.</span><span class="sxs-lookup"><span data-stu-id="d4525-878">Source and destination of a cross-domain move do not agree on the identity of the source object.</span></span> <span data-ttu-id="d4525-879">Entweder die Quelle oder das Ziel hat nicht die neueste Version des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="d4525-879">Either source or destination does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**Fehler \_ DS Fehler beim \_ Verschieben des \_ \_ gelöschten \_ Objekts.**</span><span class="sxs-lookup"><span data-stu-id="d4525-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR\_DS\_CANT\_MOVE\_DELETED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-881">8489 (0x2129)</span><span class="sxs-lookup"><span data-stu-id="d4525-881">8489 (0x2129)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-882">Ein Objekt, das über Domänen übergreifend verschoben wird, ist bereits bekannt, dass es vom Zielserver gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-882">Object being moved across-domains is already known to be deleted by the destination server.</span></span> <span data-ttu-id="d4525-883">Der Quell Server verfügt nicht über die aktuelle Version des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="d4525-883">The source server does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**Fehler \_ DS \_ PDC \_ - \_ Vorgang \_ wird ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="d4525-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR\_DS\_PDC\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-885">8490 (0x212a)</span><span class="sxs-lookup"><span data-stu-id="d4525-885">8490 (0x212A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-886">Es wird bereits ein anderer Vorgang ausgeführt, der exklusiven Zugriff auf den PDC-FSMO erfordert.</span><span class="sxs-lookup"><span data-stu-id="d4525-886">Another operation which requires exclusive access to the PDC FSMO is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**Fehler \_ - \_ DS \_ -Domänen übergreifende \_ Bereinigungs \_ -reqd**</span><span class="sxs-lookup"><span data-stu-id="d4525-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR\_DS\_CROSS\_DOMAIN\_CLEANUP\_REQD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-888">8491 (0x212b)</span><span class="sxs-lookup"><span data-stu-id="d4525-888">8491 (0x212B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-889">Ein Domänen übergreifender Verschiebungs Vorgang ist fehlgeschlagen, sodass zwei Versionen des verschogenen Objekts vorhanden sind, jeweils eine in den Quell-und Zieldomänen.</span><span class="sxs-lookup"><span data-stu-id="d4525-889">A cross-domain move operation failed such that two versions of the moved object exist - one each in the source and destination domains.</span></span> <span data-ttu-id="d4525-890">Das Zielobjekt muss entfernt werden, um das System in einen konsistenten Zustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="d4525-890">The destination object needs to be removed to restore the system to a consistent state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**Fehler DS unzulässiger xdom-Verschiebungs \_ \_ \_ \_ \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="d4525-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR\_DS\_ILLEGAL\_XDOM\_MOVE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-892">8492 (0x212c)</span><span class="sxs-lookup"><span data-stu-id="d4525-892">8492 (0x212C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-893">Dieses Objekt kann nicht über Domänen Grenzen hinweg verschoben werden, da Domänen übergreifende Verschiebungen für diese Klasse nicht zulässig sind oder das Objekt einige besondere Merkmale hat, z. b.: Vertrauensstellungs Konto oder eingeschränkte RID, wodurch die Verschiebung verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-893">This object may not be moved across domain boundaries either because cross-domain moves for this class are disallowed, or the object has some special characteristics, e.g.: trust account or restricted RID, which prevent its move.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**Fehler-DS-Fehler \_ \_ \_ mit \_ Acct- \_ Gruppen \_ mitgliedungen**</span><span class="sxs-lookup"><span data-stu-id="d4525-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR\_DS\_CANT\_WITH\_ACCT\_GROUP\_MEMBERSHPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-895">8493 (0x212d)</span><span class="sxs-lookup"><span data-stu-id="d4525-895">8493 (0x212D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-896">Objekte können nicht mithilfe von Mitgliedschaften über Domänen Grenzen hinweg verschoben werden, wenn Sie verschoben wurden. Dies würde die Mitgliedschaftsbedingungen der Konto Gruppe verletzen.</span><span class="sxs-lookup"><span data-stu-id="d4525-896">Can't move objects with memberships across domain boundaries as once moved, this would violate the membership conditions of the account group.</span></span> <span data-ttu-id="d4525-897">Entfernen Sie das Objekt aus allen Konto Gruppenmitgliedschaften, und wiederholen Sie den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d4525-897">Remove the object from any account group memberships and retry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**Fehler- \_ DS- \_ NC \_ muss \_ über \_ \_ geordnetes NC-Element verfügen**</span><span class="sxs-lookup"><span data-stu-id="d4525-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERROR\_DS\_NC\_MUST\_HAVE\_NC\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-899">8494 (0x212e)</span><span class="sxs-lookup"><span data-stu-id="d4525-899">8494 (0x212E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-900">Ein namens Kontext Kopf muss das unmittelbare untergeordnete Element eines anderen namens Kontext Kopfes und nicht eines inneren Knotens sein.</span><span class="sxs-lookup"><span data-stu-id="d4525-900">A naming context head must be the immediate child of another naming context head, not of an interior node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**Fehler \_ DS \_ CR \_ kann nicht überprüft \_ \_ werden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-902">8495 (0x212f)</span><span class="sxs-lookup"><span data-stu-id="d4525-902">8495 (0x212F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-903">Das Verzeichnis kann den vorgeschlagenen namens Kontext Namen nicht validieren, weil er kein Replikat des Namens Kontexts oberhalb des vorgeschlagenen namens Kontexts enthält.</span><span class="sxs-lookup"><span data-stu-id="d4525-903">The directory cannot validate the proposed naming context name because it does not hold a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="d4525-904">Stellen Sie sicher, dass die Domänen Namen-Master Rolle von einem Server gespeichert wird, der als globaler Katalogserver konfiguriert ist, und dass der Server mit seinen Replikations Partnern auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-904">Please ensure that the domain naming master role is held by a server that is configured as a global catalog server, and that the server is up to date with its replication partners.</span></span> <span data-ttu-id="d4525-905">(Gilt nur für Windows 2000 Domain Naming Masters.)</span><span class="sxs-lookup"><span data-stu-id="d4525-905">(Applies only to Windows 2000 Domain Naming masters.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**Fehler \_ DS \_ DST- \_ Domäne \_ nicht \_ nativ**</span><span class="sxs-lookup"><span data-stu-id="d4525-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR\_DS\_DST\_DOMAIN\_NOT\_NATIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-907">8496 (0x2130)</span><span class="sxs-lookup"><span data-stu-id="d4525-907">8496 (0x2130)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-908">Die Zieldomäne muss sich im einheitlichen Modus befinden.</span><span class="sxs-lookup"><span data-stu-id="d4525-908">Destination domain must be in native mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**Fehler \_ DS \_ fehlender \_ Infrastruktur \_ Container**</span><span class="sxs-lookup"><span data-stu-id="d4525-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR\_DS\_MISSING\_INFRASTRUCTURE\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-910">8497 (0x2131)</span><span class="sxs-lookup"><span data-stu-id="d4525-910">8497 (0x2131)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-911">Der Vorgang kann nicht ausgeführt werden, da der Server über keinen Infrastruktur Container in der relevanten Domäne verfügt.</span><span class="sxs-lookup"><span data-stu-id="d4525-911">The operation cannot be performed because the server does not have an infrastructure container in the domain of interest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**Fehler-DS-Fehler beim \_ \_ Verschieben der \_ \_ Konto \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d4525-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR\_DS\_CANT\_MOVE\_ACCOUNT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-913">8498 (0x2132)</span><span class="sxs-lookup"><span data-stu-id="d4525-913">8498 (0x2132)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-914">Domänen übergreifende Verschiebung von nicht leeren Konto Gruppen ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-914">Cross-domain move of non-empty account groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**Fehler DS-Fehler beim \_ \_ Verschieben der \_ \_ Ressourcen \_ Gruppe.**</span><span class="sxs-lookup"><span data-stu-id="d4525-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR\_DS\_CANT\_MOVE\_RESOURCE\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-916">8499 (0x2133)</span><span class="sxs-lookup"><span data-stu-id="d4525-916">8499 (0x2133)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-917">Die Domänen übergreifende Verschiebung von nicht leeren Ressourcengruppen ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-917">Cross-domain move of non-empty resource groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**Fehler- \_ DS \_ ungültiges \_ \_ suchflag**</span><span class="sxs-lookup"><span data-stu-id="d4525-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-919">8500 (0x2134)</span><span class="sxs-lookup"><span data-stu-id="d4525-919">8500 (0x2134)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-920">Die Suchflags für das Attribut sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-920">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="d4525-921">Das ANR-Bit ist nur für Attribute von Unicode-oder Teletex-Zeichen folgen gültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-921">The ANR bit is valid only on attributes of Unicode or Teletex strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**Fehler \_ DS \_ keine \_ Struktur \_ \_ über " \_ NC" Löschen**</span><span class="sxs-lookup"><span data-stu-id="d4525-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR\_DS\_NO\_TREE\_DELETE\_ABOVE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-923">8501 (0x2135)</span><span class="sxs-lookup"><span data-stu-id="d4525-923">8501 (0x2135)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-924">Struktur Löschungen, die bei einem Objekt beginnen, das einen NC-Head als Nachfolger hat, sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-924">Tree deletions starting at an object which has an NC head as a descendant are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**Fehler " \_ DS" \_ konnte \_ für \_ den \_ \_ Löschvorgang nicht gesperrt werden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR\_DS\_COULDNT\_LOCK\_TREE\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-926">8502 (0x2136)</span><span class="sxs-lookup"><span data-stu-id="d4525-926">8502 (0x2136)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-927">Der Verzeichnisdienst konnte eine Struktur in Vorbereitung auf das Löschen einer Struktur nicht sperren, weil die Struktur verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d4525-927">The directory service failed to lock a tree in preparation for a tree deletion because the tree was in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**Fehler- \_ DS \_ konnte \_ \_ Objekte für Struktur \_ \_ \_ Löschung nicht identifizieren**</span><span class="sxs-lookup"><span data-stu-id="d4525-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR\_DS\_COULDNT\_IDENTIFY\_OBJECTS\_FOR\_TREE\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-929">8503 (0x2137)</span><span class="sxs-lookup"><span data-stu-id="d4525-929">8503 (0x2137)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-930">Der Verzeichnisdienst konnte die Liste der Objekte, die gelöscht werden sollen, nicht identifizieren, während ein Baum gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-930">The directory service failed to identify the list of objects to delete while attempting a tree deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**Fehler \_ DS \_ Sam \_ Init \_ -Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-932">8504 (0x2138)</span><span class="sxs-lookup"><span data-stu-id="d4525-932">8504 (0x2138)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-933">Fehler bei der Initialisierung des Sicherheits Konten-Managers aufgrund des folgenden Fehlers: %1.</span><span class="sxs-lookup"><span data-stu-id="d4525-933">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="d4525-934">Fehler Status: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="d4525-934">Error Status: 0x%2.</span></span> <span data-ttu-id="d4525-935">Fahren Sie dieses System herunter, und starten Sie den Verzeichnisdienst-Wiederherstellungs Modus neu. Ausführliche Informationen finden Sie im Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="d4525-935">Please shutdown this system and reboot into Directory Services Restore Mode, check the event log for more detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**\_Verletzung der \_ Verletzung der sensiblen \_ Gruppe \_ für Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR\_DS\_SENSITIVE\_GROUP\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-937">8505 (0x2139)</span><span class="sxs-lookup"><span data-stu-id="d4525-937">8505 (0x2139)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-938">Nur ein Administrator kann die Mitgliedschafts Liste einer administrativen Gruppe ändern.</span><span class="sxs-lookup"><span data-stu-id="d4525-938">Only an administrator can modify the membership list of an administrative group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**Fehler \_ DS \_ cant \_ mod \_ primaryGroupId**</span><span class="sxs-lookup"><span data-stu-id="d4525-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR\_DS\_CANT\_MOD\_PRIMARYGROUPID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-940">8506 (0x213a)</span><span class="sxs-lookup"><span data-stu-id="d4525-940">8506 (0x213A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-941">Die primäre Gruppen-ID eines Domänen Controller Kontos kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-941">Cannot change the primary group ID of a domain controller account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**Fehler-DS ungültiges \_ \_ \_ Basis \_ Schema \_ mod.**</span><span class="sxs-lookup"><span data-stu-id="d4525-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR\_DS\_ILLEGAL\_BASE\_SCHEMA\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-943">8507 (0x213b)</span><span class="sxs-lookup"><span data-stu-id="d4525-943">8507 (0x213B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-944">Es wurde versucht, das Basis Schema zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d4525-944">An attempt is made to modify the base schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**Fehler- \_ DS \_ nicht sichere \_ Schema \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="d4525-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR\_DS\_NONSAFE\_SCHEMA\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-946">8508 (0x213c)</span><span class="sxs-lookup"><span data-stu-id="d4525-946">8508 (0x213C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-947">Das Hinzufügen eines neuen obligatorischen Attributs zu einer vorhandenen Klasse, das Löschen eines obligatorischen Attributs aus einer vorhandenen Klasse oder das Hinzufügen eines optionalen Attributs zur besonderen Klasse Top, das kein Backwardlink-Attribut ist (direkt oder durch Vererbung, z. b. durch das Hinzufügen oder Löschen einer Hilfsklasse), ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-947">Adding a new mandatory attribute to an existing class, deleting a mandatory attribute from an existing class, or adding an optional attribute to the special class Top that is not a backlink attribute (directly or through inheritance, for example, by adding or deleting an auxiliary class) is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**Fehler \_ DS \_ Schema \_ Update nicht \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="d4525-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR\_DS\_SCHEMA\_UPDATE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-949">8509 (0x213d)</span><span class="sxs-lookup"><span data-stu-id="d4525-949">8509 (0x213D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-950">Die Schema Aktualisierung ist auf diesem Domänen Controller nicht zulässig, da der Domänen Controller nicht der Schema-Rollen Besitzer ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-950">Schema update is not allowed on this DC because the DC is not the schema FSMO Role Owner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**Fehler " \_ DS nicht \_ \_ \_ unter \_ Schema erstellen"**</span><span class="sxs-lookup"><span data-stu-id="d4525-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR\_DS\_CANT\_CREATE\_UNDER\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-952">8510 (0x213e)</span><span class="sxs-lookup"><span data-stu-id="d4525-952">8510 (0x213E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-953">Ein Objekt dieser Klasse kann nicht unter dem Schema Container erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-953">An object of this class cannot be created under the schema container.</span></span> <span data-ttu-id="d4525-954">Sie können nur Attribut Schema-und Klassen Schema Objekte unter dem Schema Container erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4525-954">You can only create attribute-schema and class-schema objects under the schema container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**Fehler \_ DS \_ install \_ No \_ src \_ Sch \_ Version**</span><span class="sxs-lookup"><span data-stu-id="d4525-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR\_DS\_INSTALL\_NO\_SRC\_SCH\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-956">8511 (0x213f)</span><span class="sxs-lookup"><span data-stu-id="d4525-956">8511 (0x213F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-957">Die Replikat-/unterordnungsinstallation konnte das objectVersion-Attribut für den Schema Container auf dem Quell Domänen Controller nicht abrufen.</span><span class="sxs-lookup"><span data-stu-id="d4525-957">The replica/child install failed to get the objectVersion attribute on the schema container on the source DC.</span></span> <span data-ttu-id="d4525-958">Entweder fehlt das-Attribut im Schema Container, oder die angegebenen Anmelde Informationen verfügen nicht über die Berechtigung zum Lesen.</span><span class="sxs-lookup"><span data-stu-id="d4525-958">Either the attribute is missing on the schema container or the credentials supplied do not have permission to read it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**Fehler \_ DS \_ install \_ No \_ Sch \_ Version \_ in \_ IniFile**</span><span class="sxs-lookup"><span data-stu-id="d4525-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR\_DS\_INSTALL\_NO\_SCH\_VERSION\_IN\_INIFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-960">8512 (0x2140)</span><span class="sxs-lookup"><span data-stu-id="d4525-960">8512 (0x2140)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-961">Die Replikat-/unterordnungsinstallation konnte das objectVersion-Attribut im Schema Abschnitt der Datei schema.ini im Verzeichnis "System32" nicht lesen.</span><span class="sxs-lookup"><span data-stu-id="d4525-961">The replica/child install failed to read the objectVersion attribute in the SCHEMA section of the file schema.ini in the system32 directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**\_ \_ ungültiger \_ \_ Gruppentyp für Fehler-DS**</span><span class="sxs-lookup"><span data-stu-id="d4525-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR\_DS\_INVALID\_GROUP\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-963">8513 (0x2141)</span><span class="sxs-lookup"><span data-stu-id="d4525-963">8513 (0x2141)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-964">Der angegebene Gruppentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-964">The specified group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**Fehler \_ DS \_ No \_ Nest \_ Global Group \_ in \_ mixeddomain**</span><span class="sxs-lookup"><span data-stu-id="d4525-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_GLOBALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-966">8514 (0x2142)</span><span class="sxs-lookup"><span data-stu-id="d4525-966">8514 (0x2142)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-967">Globale Gruppen in einer gemischten Domäne können nicht geschachtelt werden, wenn die Gruppe für die Sicherheit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-967">You cannot nest global groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**Fehler \_ DS \_ No \_ Nest \_ localgroup \_ in \_ mixeddomain**</span><span class="sxs-lookup"><span data-stu-id="d4525-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_LOCALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-969">8515 (0x2143)</span><span class="sxs-lookup"><span data-stu-id="d4525-969">8515 (0x2143)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-970">Lokale Gruppen in einer gemischten Domäne können nicht geschachtelt werden, wenn die Gruppe für die Sicherheit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-970">You cannot nest local groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**Fehler \_ DS \_ Global \_ nicht \_ über \_ lokale \_ Member verfügen**</span><span class="sxs-lookup"><span data-stu-id="d4525-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-972">8516 (0x2144)</span><span class="sxs-lookup"><span data-stu-id="d4525-972">8516 (0x2144)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-973">Eine globale Gruppe kann keine lokale Gruppe als Mitglied haben.</span><span class="sxs-lookup"><span data-stu-id="d4525-973">A global group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**Fehler- \_ DS \_ Global \_ cant \_ haben \_ universellen \_ Member**</span><span class="sxs-lookup"><span data-stu-id="d4525-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-975">8517 (0x2145)</span><span class="sxs-lookup"><span data-stu-id="d4525-975">8517 (0x2145)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-976">Eine globale Gruppe kann keine universelle Gruppe als Mitglied haben.</span><span class="sxs-lookup"><span data-stu-id="d4525-976">A global group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**Fehler "DS Universal" darf kein \_ \_ \_ \_ \_ Lokales \_ Mitglied sein.**</span><span class="sxs-lookup"><span data-stu-id="d4525-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR\_DS\_UNIVERSAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-978">8518 (0x2146)</span><span class="sxs-lookup"><span data-stu-id="d4525-978">8518 (0x2146)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-979">Eine universelle Gruppe kann keine lokale Gruppe als Mitglied haben.</span><span class="sxs-lookup"><span data-stu-id="d4525-979">A universal group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**Fehler- \_ DS \_ Global \_ cant \_ hat \_ crossdomain- \_ Member**</span><span class="sxs-lookup"><span data-stu-id="d4525-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_CROSSDOMAIN\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-981">8519 (0x2147)</span><span class="sxs-lookup"><span data-stu-id="d4525-981">8519 (0x2147)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-982">Eine globale Gruppe darf kein Domänen übergreifendes Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d4525-982">A global group cannot have a cross-domain member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**Fehler \_ DS \_ local darf nicht \_ \_ über \_ crossdomain \_ local \_ Member verfügen**</span><span class="sxs-lookup"><span data-stu-id="d4525-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR\_DS\_LOCAL\_CANT\_HAVE\_CROSSDOMAIN\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-984">8520 (0x2148)</span><span class="sxs-lookup"><span data-stu-id="d4525-984">8520 (0x2148)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-985">Eine lokale Gruppe kann keine andere Domänen übergreifende lokale Gruppe als Mitglied haben.</span><span class="sxs-lookup"><span data-stu-id="d4525-985">A local group cannot have another cross domain local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**Fehler- \_ DS \_ haben \_ primäre \_ Member**</span><span class="sxs-lookup"><span data-stu-id="d4525-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERROR\_DS\_HAVE\_PRIMARY\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-987">8521 (0x2149)</span><span class="sxs-lookup"><span data-stu-id="d4525-987">8521 (0x2149)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-988">Eine Gruppe mit primären Mitgliedern kann nicht in eine Gruppe mit aktivierter Sicherheit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-988">A group with primary members cannot change to a security-disabled group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**Fehler bei DS-Zeichen folgen- \_ \_ SD- \_ \_ Konvertierung \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR\_DS\_STRING\_SD\_CONVERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-990">8522 (0x214a)</span><span class="sxs-lookup"><span data-stu-id="d4525-990">8522 (0x214A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-991">Die Schema Cache Auslastung konnte die Standard-SD-Zeichenfolge für ein Klassen Schema Objekt nicht konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d4525-991">The schema cache load failed to convert the string default SD on a class-schema object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**Fehler \_ DS- \_ Benennungs \_ Master- \_ GC**</span><span class="sxs-lookup"><span data-stu-id="d4525-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR\_DS\_NAMING\_MASTER\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-993">8523 (0x214b)</span><span class="sxs-lookup"><span data-stu-id="d4525-993">8523 (0x214B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-994">Nur DSAs, die als globale Katalogserver konfiguriert sind, sollten die Domänen Namen-Master-FSMO-Rolle enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="d4525-994">Only DSAs configured to be Global Catalog servers should be allowed to hold the Domain Naming Master FSMO role.</span></span> <span data-ttu-id="d4525-995">(Gilt nur für Windows 2000-Server.)</span><span class="sxs-lookup"><span data-stu-id="d4525-995">(Applies only to Windows 2000 servers.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**Fehler \_ DS \_ DNS- \_ Lookup \_ -Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR\_DS\_DNS\_LOOKUP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-997">8524 (0x214c)</span><span class="sxs-lookup"><span data-stu-id="d4525-997">8524 (0x214C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-998">Der DSA-Vorgang kann aufgrund eines Fehlers bei der DNS-Suche nicht fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-998">The DSA operation is unable to proceed because of a DNS lookup failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**Fehler- \_ DS \_ konnte \_ \_ SPNs nicht aktualisieren.**</span><span class="sxs-lookup"><span data-stu-id="d4525-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERROR\_DS\_COULDNT\_UPDATE\_SPNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1000">8525 (0x214d)</span><span class="sxs-lookup"><span data-stu-id="d4525-1000">8525 (0x214D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1001">Beim Verarbeiten einer Änderung des DNS-Host Namens für ein Objekt konnten die Werte des Dienst Prinzipal namens nicht synchron aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1001">While processing a change to the DNS Host Name for an object, the Service Principal Name values could not be kept in sync.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**Fehler "DS" konnte \_ \_ \_ SD nicht abrufen \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR\_DS\_CANT\_RETRIEVE\_SD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1003">8526 (0x214e)</span><span class="sxs-lookup"><span data-stu-id="d4525-1003">8526 (0x214E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1004">Das sicherheitsbeschreibungerattribut konnte nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1004">The Security Descriptor attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**Fehler- \_ DS- \_ Schlüssel \_ nicht \_ eindeutig**</span><span class="sxs-lookup"><span data-stu-id="d4525-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR\_DS\_KEY\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1006">8527 (0x214f)</span><span class="sxs-lookup"><span data-stu-id="d4525-1006">8527 (0x214F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1007">Das angeforderte Objekt wurde nicht gefunden, aber es wurde ein Objekt mit diesem Schlüssel gefunden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1007">The object requested was not found, but an object with that key was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**Fehler \_ DS \_ falsche \_ verknüpfte \_ ATT- \_ Syntax**</span><span class="sxs-lookup"><span data-stu-id="d4525-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR\_DS\_WRONG\_LINKED\_ATT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1009">8528 (0x2150)</span><span class="sxs-lookup"><span data-stu-id="d4525-1009">8528 (0x2150)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1010">Die Syntax des hinzugefügten verknüpften Attributs ist falsch.</span><span class="sxs-lookup"><span data-stu-id="d4525-1010">The syntax of the linked attribute being added is incorrect.</span></span> <span data-ttu-id="d4525-1011">Forward-Links können nur Syntax 2.5.5.1, 2.5.5.7 und 2.5.5.14 aufweisen, und Backlinks können nur Syntax 2.5.5.1 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1011">Forward links can only have syntax 2.5.5.1, 2.5.5.7, and 2.5.5.14, and backlinks can only have syntax 2.5.5.1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**Fehler- \_ DS \_ Sam \_ benötigt \_ bootkey- \_ Kennwort**</span><span class="sxs-lookup"><span data-stu-id="d4525-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1013">8529 (0x2151)</span><span class="sxs-lookup"><span data-stu-id="d4525-1013">8529 (0x2151)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1014">Der Sicherheits Konto-Manager muss das Start Kennwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4525-1014">Security Account Manager needs to get the boot password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**Fehler- \_ DS \_ Sam \_ benötigt \_ bootkey- \_ Diskette**</span><span class="sxs-lookup"><span data-stu-id="d4525-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_FLOPPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1016">8530 (0x2152)</span><span class="sxs-lookup"><span data-stu-id="d4525-1016">8530 (0x2152)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1017">Der Sicherheits Konto-Manager muss den Start Schlüssel von der Diskette erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4525-1017">Security Account Manager needs to get the boot key from floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**Fehler \_ DS \_ nicht \_ starten**</span><span class="sxs-lookup"><span data-stu-id="d4525-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR\_DS\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1019">8531 (0x2153)</span><span class="sxs-lookup"><span data-stu-id="d4525-1019">8531 (0x2153)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1020">Der Verzeichnisdienst kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1020">Directory Service cannot start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**Fehler \_ DS- \_ Init \_ -Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR\_DS\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1022">8532 (0x2154)</span><span class="sxs-lookup"><span data-stu-id="d4525-1022">8532 (0x2154)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1023">Verzeichnisdienste konnten nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1023">Directory Services could not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**Fehler- \_ DS \_ keine \_ Pkt- \_ Datenschutz \_ bei \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="d4525-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR\_DS\_NO\_PKT\_PRIVACY\_ON\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1025">8533 (0x2155)</span><span class="sxs-lookup"><span data-stu-id="d4525-1025">8533 (0x2155)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1026">Die Verbindung zwischen Client und Server erfordert den Datenschutz des Pakets oder besser.</span><span class="sxs-lookup"><span data-stu-id="d4525-1026">The connection between client and server requires packet privacy or better.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**Fehler- \_ DS- \_ Quell \_ Domäne \_ in der \_ Gesamtstruktur**</span><span class="sxs-lookup"><span data-stu-id="d4525-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERROR\_DS\_SOURCE\_DOMAIN\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1028">8534 (0x2156)</span><span class="sxs-lookup"><span data-stu-id="d4525-1028">8534 (0x2156)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1029">Die Quell Domäne befindet sich möglicherweise nicht in derselben Gesamtstruktur wie das Ziel.</span><span class="sxs-lookup"><span data-stu-id="d4525-1029">The source domain may not be in the same forest as destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**Fehler- \_ DS- \_ Ziel \_ Domäne \_ nicht \_ in \_ Gesamtstruktur**</span><span class="sxs-lookup"><span data-stu-id="d4525-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR\_DS\_DESTINATION\_DOMAIN\_NOT\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1031">8535 (0x2157)</span><span class="sxs-lookup"><span data-stu-id="d4525-1031">8535 (0x2157)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1032">Die Zieldomäne muss sich in der Gesamtstruktur befinden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1032">The destination domain must be in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**Fehler- \_ DS- \_ Ziel Überwachung \_ \_ nicht \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="d4525-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR\_DS\_DESTINATION\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1034">8536 (0x2158)</span><span class="sxs-lookup"><span data-stu-id="d4525-1034">8536 (0x2158)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1035">Der Vorgang erfordert, dass die Überwachung der Zieldomäne aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-1035">The operation requires that destination domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**Fehler \_ DS \_ - \_ \_ DC \_ für src \_ - \_ Domäne nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR\_DS\_CANT\_FIND\_DC\_FOR\_SRC\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1037">8537 (0x2159)</span><span class="sxs-lookup"><span data-stu-id="d4525-1037">8537 (0x2159)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1038">Der Vorgang konnte einen DC für die Quell Domäne nicht finden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1038">The operation couldn't locate a DC for the source domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**Fehler \_ DS \_ src \_ obj \_ nicht \_ Gruppe \_ oder \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d4525-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR\_DS\_SRC\_OBJ\_NOT\_GROUP\_OR\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1040">8538 (0x215 a)</span><span class="sxs-lookup"><span data-stu-id="d4525-1040">8538 (0x215A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1041">Das Quell Objekt muss eine Gruppe oder ein Benutzer sein.</span><span class="sxs-lookup"><span data-stu-id="d4525-1041">The source object must be a group or user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**Fehler \_ DS- \_ src-sid ist \_ \_ \_ in der \_ Gesamtstruktur vorhanden**</span><span class="sxs-lookup"><span data-stu-id="d4525-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR\_DS\_SRC\_SID\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1043">8539 (0x215 b)</span><span class="sxs-lookup"><span data-stu-id="d4525-1043">8539 (0x215B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1044">Die SID des Quell Objekts ist bereits in der Ziel Gesamtstruktur vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1044">The source object's SID already exists in destination forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**Fehler \_ DS \_ src \_ und \_ DST- \_ Objekt \_ Klasse stimmen nicht \_ überein.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR\_DS\_SRC\_AND\_DST\_OBJECT\_CLASS\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1046">8540 (0x215 c)</span><span class="sxs-lookup"><span data-stu-id="d4525-1046">8540 (0x215C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1047">Das Quell-und das Zielobjekt müssen denselben Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1047">The source and destination object must be of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**Fehler \_ Sam \_ Init \_ -Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1049">8541 (0x215 d)</span><span class="sxs-lookup"><span data-stu-id="d4525-1049">8541 (0x215D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1050">Fehler bei der Initialisierung des Sicherheits Konten-Managers aufgrund des folgenden Fehlers: %1.</span><span class="sxs-lookup"><span data-stu-id="d4525-1050">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="d4525-1051">Fehler Status: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="d4525-1051">Error Status: 0x%2.</span></span> <span data-ttu-id="d4525-1052">Klicken Sie auf OK, um das System herunterzufahren und in den abgesicherten Modus zu starten.</span><span class="sxs-lookup"><span data-stu-id="d4525-1052">Click OK to shut down the system and reboot into Safe Mode.</span></span> <span data-ttu-id="d4525-1053">Ausführliche Informationen finden Sie im Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="d4525-1053">Check the event log for detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**Fehler \_ DS- \_ DRA- \_ Schema \_ Info \_ Versand**</span><span class="sxs-lookup"><span data-stu-id="d4525-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR\_DS\_DRA\_SCHEMA\_INFO\_SHIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1055">8542 (0x215 e)</span><span class="sxs-lookup"><span data-stu-id="d4525-1055">8542 (0x215E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1056">Die Schema Informationen konnten nicht in die Replikations Anforderung eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1056">Schema information could not be included in the replication request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**Fehler \_ DS- \_ DRA- \_ Schema \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="d4525-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERROR\_DS\_DRA\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1058">8543 (0x215 f)</span><span class="sxs-lookup"><span data-stu-id="d4525-1058">8543 (0x215F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1059">Der Replikations Vorgang konnte aufgrund einer Schema Inkompatibilität nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1059">The replication operation could not be completed due to a schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**Fehler \_ DS- \_ DRA- \_ \_ Schema \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="d4525-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERROR\_DS\_DRA\_EARLIER\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1061">8544 (0x2160)</span><span class="sxs-lookup"><span data-stu-id="d4525-1061">8544 (0x2160)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1062">Der Replikations Vorgang konnte aufgrund einer vorherigen Schema Inkompatibilität nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1062">The replication operation could not be completed due to a previous schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**Fehler \_ DS \_ DRA \_ obj \_ NC \_ -Konflikt**</span><span class="sxs-lookup"><span data-stu-id="d4525-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR\_DS\_DRA\_OBJ\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1064">8545 (0x2161)</span><span class="sxs-lookup"><span data-stu-id="d4525-1064">8545 (0x2161)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1065">Das Replikations Update konnte nicht angewendet werden, da entweder die Quelle oder das Ziel noch keine Informationen zu einem letzten Domänen übergreifenden Verschiebungs Vorgang erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="d4525-1065">The replication update could not be applied because either the source or the destination has not yet received information regarding a recent cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**Fehler \_ DS \_ NC \_ \_ weist weiterhin \_ DSAs auf.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERROR\_DS\_NC\_STILL\_HAS\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1067">8546 (0x2162)</span><span class="sxs-lookup"><span data-stu-id="d4525-1067">8546 (0x2162)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1068">Die angeforderte Domäne konnte nicht gelöscht werden, da Domänen Controller vorhanden sind, die noch diese Domäne hosten.</span><span class="sxs-lookup"><span data-stu-id="d4525-1068">The requested domain could not be deleted because there exist domain controllers that still host this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**Fehler- \_ DS- \_ GC \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4525-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR\_DS\_GC\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1070">8547 (0x2163)</span><span class="sxs-lookup"><span data-stu-id="d4525-1070">8547 (0x2163)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1071">Der angeforderte Vorgang kann nur auf einem globalen Katalogserver ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1071">The requested operation can be performed only on a global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**Fehler \_ DS \_ lokaler \_ Member \_ von \_ \_ nur lokal**</span><span class="sxs-lookup"><span data-stu-id="d4525-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR\_DS\_LOCAL\_MEMBER\_OF\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1073">8548 (0x2164)</span><span class="sxs-lookup"><span data-stu-id="d4525-1073">8548 (0x2164)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1074">Eine lokale Gruppe kann nur Mitglied anderer lokaler Gruppen in der gleichen Domäne sein.</span><span class="sxs-lookup"><span data-stu-id="d4525-1074">A local group can only be a member of other local groups in the same domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**Fehler " \_ DS \_ Nein" \_ \_ in \_ universellen \_ Gruppen**</span><span class="sxs-lookup"><span data-stu-id="d4525-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR\_DS\_NO\_FPO\_IN\_UNIVERSAL\_GROUPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1076">8549 (0x2165)</span><span class="sxs-lookup"><span data-stu-id="d4525-1076">8549 (0x2165)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1077">Fremde Sicherheits Prinzipale können nicht zu universellen Gruppen gehören.</span><span class="sxs-lookup"><span data-stu-id="d4525-1077">Foreign security principals cannot be members of universal groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**Fehler \_ DS \_ nicht \_ \_ zum \_ GC hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="d4525-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR\_DS\_CANT\_ADD\_TO\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1079">8550 (0x2166)</span><span class="sxs-lookup"><span data-stu-id="d4525-1079">8550 (0x2166)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1080">Das Attribut darf aufgrund von Sicherheitsgründen nicht in den GC repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1080">The attribute is not allowed to be replicated to the GC because of security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**Fehler- \_ DS kein Prüfpunkt \_ \_ \_ mit \_ PDC**</span><span class="sxs-lookup"><span data-stu-id="d4525-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR\_DS\_NO\_CHECKPOINT\_WITH\_PDC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1082">8551 (0x2167)</span><span class="sxs-lookup"><span data-stu-id="d4525-1082">8551 (0x2167)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1083">Der Prüfpunkt mit dem PDC konnte nicht übernommen werden, weil derzeit zu viele Änderungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1083">The checkpoint with the PDC could not be taken because there too many modifications being processed currently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**Fehler der DS-Quell Überwachung ist \_ \_ \_ \_ nicht \_ aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR\_DS\_SOURCE\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1085">8552 (0x2168)</span><span class="sxs-lookup"><span data-stu-id="d4525-1085">8552 (0x2168)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1086">Der Vorgang erfordert, dass die Überwachung der Quell Domäne aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-1086">The operation requires that source domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**Fehler "DS-Fehler \_ \_ \_ \_ beim Erstellen in \_ nicht-Domäne \_ "**</span><span class="sxs-lookup"><span data-stu-id="d4525-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR\_DS\_CANT\_CREATE\_IN\_NONDOMAIN\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1088">8553 (0x2169)</span><span class="sxs-lookup"><span data-stu-id="d4525-1088">8553 (0x2169)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1089">Sicherheits Prinzipal Objekte können nur innerhalb von Domänen namens Kontexten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1089">Security principal objects can only be created inside domain naming contexts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**Fehler \_ DS \_ ungültiger \_ Name \_ für \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="d4525-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR\_DS\_INVALID\_NAME\_FOR\_SPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1091">8554 (0x216a)</span><span class="sxs-lookup"><span data-stu-id="d4525-1091">8554 (0x216A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1092">Ein Dienst Prinzipal Name (Service Principal Name, SPN) konnte nicht erstellt werden, da der angegebene Hostname nicht das erforderliche Format hat.</span><span class="sxs-lookup"><span data-stu-id="d4525-1092">A Service Principal Name (SPN) could not be constructed because the provided hostname is not in the necessary format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**Fehler- \_ DS- \_ Filter verwendet die \_ \_ Konstanten \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERROR\_DS\_FILTER\_USES\_CONTRUCTED\_ATTRS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1094">8555 (0x216b)</span><span class="sxs-lookup"><span data-stu-id="d4525-1094">8555 (0x216B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1095">Es wurde ein Filter mit konstruierten Attributen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1095">A Filter was passed that uses constructed attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**Fehler \_ DS \_ unicodePwd \_ nicht \_ in \_ Anführungszeichen**</span><span class="sxs-lookup"><span data-stu-id="d4525-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR\_DS\_UNICODEPWD\_NOT\_IN\_QUOTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1097">8556 (0x216c)</span><span class="sxs-lookup"><span data-stu-id="d4525-1097">8556 (0x216C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1098">Der unicodePwd-Attribut Wert muss in doppelte Anführungszeichen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1098">The unicodePwd attribute value must be enclosed in double quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**Fehler \_ DS- \_ Computer \_ Konto \_ Kontingent \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="d4525-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1100">8557 (0x216d)</span><span class="sxs-lookup"><span data-stu-id="d4525-1100">8557 (0x216D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1101">Der Computer konnte nicht der Domäne hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1101">Your computer could not be joined to the domain.</span></span> <span data-ttu-id="d4525-1102">Sie haben die maximale Anzahl von Computer Konten überschritten, die Sie in dieser Domäne erstellen dürfen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1102">You have exceeded the maximum number of computer accounts you are allowed to create in this domain.</span></span> <span data-ttu-id="d4525-1103">Wenden Sie sich an Ihren Systemadministrator, um dieses Limit zurückzusetzen oder zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1103">Contact your system administrator to have this limit reset or increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**Fehler- \_ DS \_ muss auf dem \_ \_ \_ \_ DST \_ -Domänen Controller ausgeführt werden**</span><span class="sxs-lookup"><span data-stu-id="d4525-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**ERROR\_DS\_MUST\_BE\_RUN\_ON\_DST\_DC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1105">8558 (0x216e)</span><span class="sxs-lookup"><span data-stu-id="d4525-1105">8558 (0x216E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1106">Aus Sicherheitsgründen muss der Vorgang auf dem Ziel-DC ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1106">For security reasons, the operation must be run on the destination DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**Fehler \_ DS \_ src \_ DC \_ muss \_ \_ SP4 \_ oder \_ höher sein.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR\_DS\_SRC\_DC\_MUST\_BE\_SP4\_OR\_GREATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1108">8559 (0x216f)</span><span class="sxs-lookup"><span data-stu-id="d4525-1108">8559 (0x216F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1109">Aus Sicherheitsgründen muss der Quell Domänen Controller NT4SP4 oder höher sein.</span><span class="sxs-lookup"><span data-stu-id="d4525-1109">For security reasons, the source DC must be NT4SP4 or greater.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**Fehler \_ DS-Struktur \_ \_ \_ Löschen \_ kritisch \_ obj**</span><span class="sxs-lookup"><span data-stu-id="d4525-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR\_DS\_CANT\_TREE\_DELETE\_CRITICAL\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1111">8560 (0x2170)</span><span class="sxs-lookup"><span data-stu-id="d4525-1111">8560 (0x2170)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1112">Wichtige Verzeichnisdienst-System Objekte können während Struktur Lösch Vorgängen nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1112">Critical Directory Service System objects cannot be deleted during tree delete operations.</span></span> <span data-ttu-id="d4525-1113">Das Löschen der Struktur wurde möglicherweise teilweise durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1113">The tree delete may have been partially performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**Fehler- \_ DS init-Fehler \_ \_ \_ Konsole**</span><span class="sxs-lookup"><span data-stu-id="d4525-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR\_DS\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1115">8561 (0x2171)</span><span class="sxs-lookup"><span data-stu-id="d4525-1115">8561 (0x2171)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1116">Verzeichnisdienste konnten aufgrund des folgenden Fehlers nicht gestartet werden: %1.</span><span class="sxs-lookup"><span data-stu-id="d4525-1116">Directory Services could not start because of the following error: %1.</span></span> <span data-ttu-id="d4525-1117">Fehler Status: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="d4525-1117">Error Status: 0x%2.</span></span> <span data-ttu-id="d4525-1118">Klicken Sie auf OK, um das System herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="d4525-1118">Please click OK to shutdown the system.</span></span> <span data-ttu-id="d4525-1119">Zur weiteren Systemdiagnose können Sie die Wiederherstellungskonsole verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1119">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**Fehler \_ DS \_ Sam \_ Init-Fehler \_ \_ Konsole**</span><span class="sxs-lookup"><span data-stu-id="d4525-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1121">8562 (0x2172)</span><span class="sxs-lookup"><span data-stu-id="d4525-1121">8562 (0x2172)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1122">Fehler bei der Initialisierung des Sicherheits Konten-Managers aufgrund des folgenden Fehlers: %1.</span><span class="sxs-lookup"><span data-stu-id="d4525-1122">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="d4525-1123">Fehler Status: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="d4525-1123">Error Status: 0x%2.</span></span> <span data-ttu-id="d4525-1124">Klicken Sie auf OK, um das System herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="d4525-1124">Please click OK to shutdown the system.</span></span> <span data-ttu-id="d4525-1125">Zur weiteren Systemdiagnose können Sie die Wiederherstellungskonsole verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1125">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**Fehler-DS-Gesamtstruktur \_ \_ \_ Version \_ zu \_ hoch**</span><span class="sxs-lookup"><span data-stu-id="d4525-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1127">8563 (0x2173)</span><span class="sxs-lookup"><span data-stu-id="d4525-1127">8563 (0x2173)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1128">Die Version des Betriebssystems ist nicht kompatibel mit der aktuellen AD DS Gesamtstruktur Funktionsebene oder AD LDS Konfigurationssatz-Funktionsebene.</span><span class="sxs-lookup"><span data-stu-id="d4525-1128">The version of the operating system is incompatible with the current AD DS forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="d4525-1129">Sie müssen ein Upgrade auf eine neue Version des Betriebssystems durchführen, bevor dieser Server zu einem AD DS Domänen Controller werden kann, oder Sie können eine AD LDS Instanz in dieser AD DS Gesamtstruktur oder AD LDS Konfigurationssatz hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1129">You must upgrade to a new version of the operating system before this server can become an AD DS Domain Controller or add an AD LDS Instance in this AD DS Forest or AD LDS Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**Fehler- \_ DS- \_ Domänen \_ Version \_ zu \_ hoch**</span><span class="sxs-lookup"><span data-stu-id="d4525-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1131">8564 (0x2174)</span><span class="sxs-lookup"><span data-stu-id="d4525-1131">8564 (0x2174)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1132">Die installierte Version des Betriebssystems ist mit der aktuellen Domänen Funktionsebene nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d4525-1132">The version of the operating system installed is incompatible with the current domain functional level.</span></span> <span data-ttu-id="d4525-1133">Sie müssen ein Upgrade auf eine neue Version des Betriebssystems ausführen, bevor dieser Server als Domänen Controller in dieser Domäne verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4525-1133">You must upgrade to a new version of the operating system before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**Fehler-DS-Gesamtstruktur \_ \_ \_ Version \_ zu \_ niedrig**</span><span class="sxs-lookup"><span data-stu-id="d4525-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1135">8565 (0x2175)</span><span class="sxs-lookup"><span data-stu-id="d4525-1135">8565 (0x2175)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1136">Die auf diesem Server installierte Version des Betriebssystems unterstützt nicht mehr die aktuelle AD DS-Gesamtstruktur Funktionsebene oder AD LDS Konfigurationssatz-Funktionsebene.</span><span class="sxs-lookup"><span data-stu-id="d4525-1136">The version of the operating system installed on this server no longer supports the current AD DS Forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="d4525-1137">Sie müssen die Funktionsebene der AD DS-Gesamtstruktur oder die AD LDS Konfigurationssatz-Funktionsebene erhöhen, bevor dieser Server ein AD DS Domänen Controller oder eine AD LDS Instanz in dieser Gesamtstruktur oder diesem Konfigurationssatz werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4525-1137">You must raise the AD DS Forest functional level or AD LDS Configuration Set functional level before this server can become an AD DS Domain Controller or an AD LDS Instance in this Forest or Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**Fehler- \_ DS- \_ Domänen \_ Version \_ zu \_ niedrig**</span><span class="sxs-lookup"><span data-stu-id="d4525-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1139">8566 (0x2176)</span><span class="sxs-lookup"><span data-stu-id="d4525-1139">8566 (0x2176)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1140">Die auf diesem Server installierte Version des Betriebssystems unterstützt die aktuelle Domänen Funktionsebene nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="d4525-1140">The version of the operating system installed on this server no longer supports the current domain functional level.</span></span> <span data-ttu-id="d4525-1141">Sie müssen die Domänen Funktionsebene erhöhen, bevor dieser Server als Domänen Controller in dieser Domäne verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4525-1141">You must raise the domain functional level before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**Fehler- \_ DS \_ inkompatible \_ Version**</span><span class="sxs-lookup"><span data-stu-id="d4525-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR\_DS\_INCOMPATIBLE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1143">8567 (0x2177)</span><span class="sxs-lookup"><span data-stu-id="d4525-1143">8567 (0x2177)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1144">Die auf diesem Server installierte Version des Betriebssystems ist nicht mit der Funktionsebene der Domäne oder der Gesamtstruktur kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d4525-1144">The version of the operating system installed on this server is incompatible with the functional level of the domain or forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**Fehler \_ DS \_ niedrige \_ DSA- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="d4525-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR\_DS\_LOW\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1146">8568 (0x2178)</span><span class="sxs-lookup"><span data-stu-id="d4525-1146">8568 (0x2178)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1147">Die Funktionsebene der Domäne (oder Gesamtstruktur) kann nicht auf den angeforderten Wert fest gegeben werden, weil mindestens ein Domänen Controller in der Domäne (oder Gesamtstruktur) vorhanden ist, die sich auf einer niedrigeren inkompatiblen Funktionsebene befinden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1147">The functional level of the domain (or forest) cannot be raised to the requested value, because there exist one or more domain controllers in the domain (or forest) that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**Fehler \_ DS \_ keine \_ Verhaltens \_ Version \_ in \_ mixeddomain**</span><span class="sxs-lookup"><span data-stu-id="d4525-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR\_DS\_NO\_BEHAVIOR\_VERSION\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1149">8569 (0x2179)</span><span class="sxs-lookup"><span data-stu-id="d4525-1149">8569 (0x2179)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1150">Die Gesamtstruktur Funktionsebene kann nicht auf den angeforderten Wert fest liegen, da sich eine oder mehrere Domänen noch im gemischten Domänen Modus befinden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1150">The forest functional level cannot be raised to the requested value since one or more domains are still in mixed domain mode.</span></span> <span data-ttu-id="d4525-1151">Alle Domänen in der Gesamtstruktur müssen sich im einheitlichen Modus befinden, damit Sie die Gesamtstruktur Funktionsebene erhöhen können.</span><span class="sxs-lookup"><span data-stu-id="d4525-1151">All domains in the forest must be in native mode, for you to raise the forest functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**Fehler- \_ DS \_ nicht \_ unterstützte \_ Sortier \_ Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="d4525-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR\_DS\_NOT\_SUPPORTED\_SORT\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1153">8570 (0x217a)</span><span class="sxs-lookup"><span data-stu-id="d4525-1153">8570 (0x217A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1154">Die angeforderte Sortierreihenfolge wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1154">The sort order requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**Fehler \_ DS- \_ Name \_ nicht \_ eindeutig**</span><span class="sxs-lookup"><span data-stu-id="d4525-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR\_DS\_NAME\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1156">8571 (0x217b)</span><span class="sxs-lookup"><span data-stu-id="d4525-1156">8571 (0x217B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1157">Der angeforderte Name ist bereits als eindeutiger Bezeichner vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1157">The requested name already exists as a unique identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**Fehler \_ DS- \_ Computer \_ Konto \_ erstellt \_ PRENT4**</span><span class="sxs-lookup"><span data-stu-id="d4525-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_CREATED\_PRENT4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1159">8572 (0x217c)</span><span class="sxs-lookup"><span data-stu-id="d4525-1159">8572 (0x217C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1160">Das Computer Konto wurde vor dem Computer Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1160">The machine account was created pre-NT4.</span></span> <span data-ttu-id="d4525-1161">Das Konto muss neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1161">The account needs to be recreated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**Fehler- \_ DS \_ aus dem \_ \_ Versions \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="d4525-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR\_DS\_OUT\_OF\_VERSION\_STORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1163">8573 (0x217d)</span><span class="sxs-lookup"><span data-stu-id="d4525-1163">8573 (0x217D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1164">Die Datenbank befindet sich außerhalb des Versionsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d4525-1164">The database is out of version store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**Fehler- \_ DS- \_ kompatible Steuer \_ Elemente \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="d4525-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR\_DS\_INCOMPATIBLE\_CONTROLS\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1166">8574 (0x217e)</span><span class="sxs-lookup"><span data-stu-id="d4525-1166">8574 (0x217E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1167">Der Vorgang kann nicht fortgesetzt werden, da mehrere widersprüchliche Steuerelemente verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1167">Unable to continue operation because multiple conflicting controls were used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**Fehler \_ DS \_ keine \_ Verweis \_ Domäne**</span><span class="sxs-lookup"><span data-stu-id="d4525-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR\_DS\_NO\_REF\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1169">8575 (0x217f)</span><span class="sxs-lookup"><span data-stu-id="d4525-1169">8575 (0x217F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1170">Es wurde keine gültige Sicherheits beschreibungerverweisdomäne für diese Partition gefunden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1170">Unable to find a valid security descriptor reference domain for this partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**Fehler \_ DS \_ reservierte \_ Link- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d4525-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERROR\_DS\_RESERVED\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1172">8576 (0x2180)</span><span class="sxs-lookup"><span data-stu-id="d4525-1172">8576 (0x2180)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1173">Fehler beim Aktualisieren des Schemas: der Link Bezeichner ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="d4525-1173">Schema update failed: The link identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**Fehler \_ DS- \_ Link- \_ ID \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="d4525-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERROR\_DS\_LINK\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1175">8577 (0x2181)</span><span class="sxs-lookup"><span data-stu-id="d4525-1175">8577 (0x2181)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1176">Fehler beim Aktualisieren des Schemas: Es sind keine Link Bezeichner verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4525-1176">Schema update failed: There are no link identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**Fehler der DS-Verfügbarkeits Gruppe ( \_ \_ \_ \_ \_ Universal \_ Member).**</span><span class="sxs-lookup"><span data-stu-id="d4525-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR\_DS\_AG\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1178">8578 (0x2182)</span><span class="sxs-lookup"><span data-stu-id="d4525-1178">8578 (0x2182)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1179">Eine Konto Gruppe kann keine universelle Gruppe als Mitglied haben.</span><span class="sxs-lookup"><span data-stu-id="d4525-1179">An account group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**Fehler \_ DS- \_ modififydn \_ \_ durch \_ \_ Instanztyp unzulässig**</span><span class="sxs-lookup"><span data-stu-id="d4525-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1181">8579 (0x2183)</span><span class="sxs-lookup"><span data-stu-id="d4525-1181">8579 (0x2183)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1182">Umbenennen oder Verschieben von Vorgängen für namens Kontext Köpfe oder schreibgeschützte Objekte sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1182">Rename or move operations on naming context heads or read-only objects are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**Fehler \_ ' \_ keine \_ Objekt \_ Verschiebung ' \_ in \_ Schema \_ NC**</span><span class="sxs-lookup"><span data-stu-id="d4525-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR\_DS\_NO\_OBJECT\_MOVE\_IN\_SCHEMA\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1184">8580 (0x2184)</span><span class="sxs-lookup"><span data-stu-id="d4525-1184">8580 (0x2184)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1185">Verschiebe Vorgänge für Objekte im Schema namens Kontext sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1185">Move operations on objects in the schema naming context are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**Fehler \_ DS- \_ modififydn ist \_ \_ durch \_ Flag unzulässig.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1187">8581 (0x2185)</span><span class="sxs-lookup"><span data-stu-id="d4525-1187">8581 (0x2185)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1188">Für das Objekt wurde ein Systemflag festgelegt, und das Objekt kann nicht verschoben oder umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1188">A system flag has been set on the object and does not allow the object to be moved or renamed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**Fehler \_ DS \_ MODIFYDN \_ falsches über \_ geordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="d4525-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR\_DS\_MODIFYDN\_WRONG\_GRANDPARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1190">8582 (0x2186)</span><span class="sxs-lookup"><span data-stu-id="d4525-1190">8582 (0x2186)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1191">Dieses Objekt ist nicht berechtigt, seinen übergeordneten übergeordneten Container zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d4525-1191">This object is not allowed to change its grandparent container.</span></span> <span data-ttu-id="d4525-1192">Die Verschiebung ist für dieses Objekt nicht zulässig, aber auf gleich geordnete Container beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1192">Moves are not forbidden on this object, but are restricted to sibling containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**Fehler- \_ DS- \_ namens \_ Fehler \_ Vertrauensstellungs \_ Referenz**</span><span class="sxs-lookup"><span data-stu-id="d4525-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERROR\_DS\_NAME\_ERROR\_TRUST\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1194">8583 (0x2187)</span><span class="sxs-lookup"><span data-stu-id="d4525-1194">8583 (0x2187)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1195">Das vollständige auflösen ist nicht möglich, es wird ein Verweis auf eine andere Gesamtstruktur generiert.</span><span class="sxs-lookup"><span data-stu-id="d4525-1195">Unable to resolve completely, a referral to another forest is generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**Fehler \_ \_ wird \_ auf \_ Standard \_ Server nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR\_NOT\_SUPPORTED\_ON\_STANDARD\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1197">8584 (0x2188)</span><span class="sxs-lookup"><span data-stu-id="d4525-1197">8584 (0x2188)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1198">Die angeforderte Aktion wird auf dem Standard Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1198">The requested action is not supported on standard server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**Fehler \_ DS \_ - \_ Zugriff \_ \_ auf Remote Teil \_ von \_ AD**</span><span class="sxs-lookup"><span data-stu-id="d4525-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR\_DS\_CANT\_ACCESS\_REMOTE\_PART\_OF\_AD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1200">8585 (0x2189)</span><span class="sxs-lookup"><span data-stu-id="d4525-1200">8585 (0x2189)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1201">Auf eine Partition des Verzeichnis Dienstanbieter, die sich auf einem Remote Server befindet, konnte nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1201">Could not access a partition of the directory service located on a remote server.</span></span> <span data-ttu-id="d4525-1202">Stellen Sie sicher, dass mindestens ein Server für die betreffende Partition ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-1202">Make sure at least one server is running for the partition in question.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**Fehler \_ DS \_ CR \_ kann nicht überprüft werden \_ \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="d4525-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE\_V2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1204">8586 (0x218 a)</span><span class="sxs-lookup"><span data-stu-id="d4525-1204">8586 (0x218A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1205">Das Verzeichnis kann den vorgeschlagenen namens Kontext (oder Partitionsnamen) nicht validieren, weil er kein Replikat enthält und keine Verbindung mit einem Replikat des Namens Kontexts oberhalb des vorgeschlagenen namens Kontexts aufnehmen kann.</span><span class="sxs-lookup"><span data-stu-id="d4525-1205">The directory cannot validate the proposed naming context (or partition) name because it does not hold a replica nor can it contact a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="d4525-1206">Stellen Sie sicher, dass der übergeordnete Benennungs Kontext ordnungsgemäß in DNS registriert ist, und dass mindestens ein Replikat dieses Namens Kontexts durch den Domänen Namen Master erreichbar ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-1206">Please ensure that the parent naming context is properly registered in DNS, and at least one replica of this naming context is reachable by the Domain Naming master.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**Fehler- \_ DS- \_ Thread \_ Limit \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="d4525-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERROR\_DS\_THREAD\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1208">8587 (0x218 b)</span><span class="sxs-lookup"><span data-stu-id="d4525-1208">8587 (0x218B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1209">Der Thread Grenzwert für diese Anforderung wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d4525-1209">The thread limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**Fehler- \_ DS ist \_ nicht \_ am nächsten**</span><span class="sxs-lookup"><span data-stu-id="d4525-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR\_DS\_NOT\_CLOSEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1211">8588 (0x218 c)</span><span class="sxs-lookup"><span data-stu-id="d4525-1211">8588 (0x218C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1212">Der globale Katalogserver befindet sich nicht am nächstgelegenen Standort.</span><span class="sxs-lookup"><span data-stu-id="d4525-1212">The Global catalog server is not in the closest site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**Fehler- \_ DS konnte \_ \_ \_ keinen SPN \_ ohne \_ Server \_ Verweis ableiten.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_WITHOUT\_SERVER\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1214">8589 (0x218 d)</span><span class="sxs-lookup"><span data-stu-id="d4525-1214">8589 (0x218D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1215">Die DS kann keinen Dienst Prinzipal Namen (SPN) ableiten, mit dem der Zielserver gegenseitig authentifiziert werden kann, da das zugehörige Server Objekt in der lokalen DS-Datenbank kein serverReference-Attribut aufweist.</span><span class="sxs-lookup"><span data-stu-id="d4525-1215">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the corresponding server object in the local DS database has no serverReference attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**Fehler \_ beim \_ Einzel \_ Benutzermodus im Einzelbenutzer \_ Modus \_ .**</span><span class="sxs-lookup"><span data-stu-id="d4525-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR\_DS\_SINGLE\_USER\_MODE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1217">8590 (0x218 e)</span><span class="sxs-lookup"><span data-stu-id="d4525-1217">8590 (0x218E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1218">Der Verzeichnisdienst konnte nicht in den Einzelbenutzermodus wechseln.</span><span class="sxs-lookup"><span data-stu-id="d4525-1218">The Directory Service failed to enter single user mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**Fehler \_ DS \_ ntdscript- \_ Syntax \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**ERROR\_DS\_NTDSCRIPT\_SYNTAX\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1220">8591 (0x218 f)</span><span class="sxs-lookup"><span data-stu-id="d4525-1220">8591 (0x218F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1221">Der Verzeichnisdienst kann das Skript aufgrund eines Syntax Fehlers nicht analysieren.</span><span class="sxs-lookup"><span data-stu-id="d4525-1221">The Directory Service cannot parse the script because of a syntax error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**Fehler \_ DS \_ ntdscript- \_ Prozess \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERROR\_DS\_NTDSCRIPT\_PROCESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1223">8592 (0x2190)</span><span class="sxs-lookup"><span data-stu-id="d4525-1223">8592 (0x2190)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1224">Der Verzeichnisdienst kann das Skript aufgrund eines Fehlers nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4525-1224">The Directory Service cannot process the script because of an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**Fehler- \_ DS \_ unterschiedlicher \_ repl- \_ Epochen**</span><span class="sxs-lookup"><span data-stu-id="d4525-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERROR\_DS\_DIFFERENT\_REPL\_EPOCHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1226">8593 (0x2191)</span><span class="sxs-lookup"><span data-stu-id="d4525-1226">8593 (0x2191)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1227">Der Verzeichnisdienst kann den angeforderten Vorgang nicht ausführen, da sich die beteiligten Server unterschiedlichen Replikations Epochen befinden (in der Regel im Zusammenhang mit einem Domänen umbenennen, der gerade ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="d4525-1227">The directory service cannot perform the requested operation because the servers involved are of different replication epochs (which is usually related to a domain rename that is in progress).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**Fehler- \_ DS \_ DRS- \_ Erweiterungen \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="d4525-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERROR\_DS\_DRS\_EXTENSIONS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1229">8594 (0x2192)</span><span class="sxs-lookup"><span data-stu-id="d4525-1229">8594 (0x2192)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1230">Die Verzeichnisdienst Bindung muss aufgrund einer Änderung der Server Erweiterungs Informationen erneut ausgehandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1230">The directory service binding must be renegotiated due to a change in the server extensions information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**Fehler \_ \_ \_ \_ bei der Änderung der Replikat Gruppe \_ \_ für den \_ \_ deaktivierten \_ CR**</span><span class="sxs-lookup"><span data-stu-id="d4525-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR\_DS\_REPLICA\_SET\_CHANGE\_NOT\_ALLOWED\_ON\_DISABLED\_CR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1232">8595 (0x2193)</span><span class="sxs-lookup"><span data-stu-id="d4525-1232">8595 (0x2193)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1233">Der Vorgang ist für einen deaktivierten Kreuz Verweis nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1233">Operation not allowed on a disabled cross ref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**Fehler- \_ DS \_ keine \_ msDS \_ -initid**</span><span class="sxs-lookup"><span data-stu-id="d4525-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR\_DS\_NO\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1235">8596 (0x2194)</span><span class="sxs-lookup"><span data-stu-id="d4525-1235">8596 (0x2194)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1236">Fehler beim Aktualisieren des Schemas: Es sind keine Werte für MSDS-IntID verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4525-1236">Schema update failed: No values for msDS-IntId are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**Fehler \_ DS \_ DUP \_ msDS \_ -initid**</span><span class="sxs-lookup"><span data-stu-id="d4525-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR\_DS\_DUP\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1238">8597 (0x2195)</span><span class="sxs-lookup"><span data-stu-id="d4525-1238">8597 (0x2195)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1239">Fehler beim Aktualisieren des Schemas: doppelte MSDS-initid.</span><span class="sxs-lookup"><span data-stu-id="d4525-1239">Schema update failed: Duplicate msDS-INtId.</span></span> <span data-ttu-id="d4525-1240">Wiederholen Sie den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d4525-1240">Retry the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**Fehler \_ - \_ DS \_ in \_ rDNAttID**</span><span class="sxs-lookup"><span data-stu-id="d4525-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERROR\_DS\_EXISTS\_IN\_RDNATTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1242">8598 (0x2196)</span><span class="sxs-lookup"><span data-stu-id="d4525-1242">8598 (0x2196)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1243">Fehler beim Löschen des Schemas: das Attribut wird in rDNAttID verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4525-1243">Schema deletion failed: attribute is used in rDNAttID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**Fehler bei \_ DS- \_ Autorisierung. \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR\_DS\_AUTHORIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1245">8599 (0x2197)</span><span class="sxs-lookup"><span data-stu-id="d4525-1245">8599 (0x2197)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1246">Der Verzeichnisdienst konnte die Anforderung nicht autorisieren.</span><span class="sxs-lookup"><span data-stu-id="d4525-1246">The directory service failed to authorize the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**Fehler- \_ DS \_ ungültiges \_ Skript**</span><span class="sxs-lookup"><span data-stu-id="d4525-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR\_DS\_INVALID\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1248">8600 (0x2198)</span><span class="sxs-lookup"><span data-stu-id="d4525-1248">8600 (0x2198)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1249">Der Verzeichnisdienst kann das Skript nicht verarbeiten, da er ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-1249">The Directory Service cannot process the script because it is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**Fehler \_ bei \_ Remote- \_ CrossRef- \_ op \_ -Fehler.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR\_DS\_REMOTE\_CROSSREF\_OP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1251">8601 (0x2199)</span><span class="sxs-lookup"><span data-stu-id="d4525-1251">8601 (0x2199)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1252">Fehler beim Remote Vorgang zum Erstellen eines quer Verweises auf dem Domänen Namen-Master-Hauptschlüssel.</span><span class="sxs-lookup"><span data-stu-id="d4525-1252">The remote create cross reference operation failed on the Domain Naming Master FSMO.</span></span> <span data-ttu-id="d4525-1253">Der Fehler des Vorgangs liegt in den erweiterten Daten.</span><span class="sxs-lookup"><span data-stu-id="d4525-1253">The operation's error is in the extended data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**Fehler- \_ DS- \_ Querverweis \_ \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="d4525-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR\_DS\_CROSS\_REF\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1255">8602 (0x219a)</span><span class="sxs-lookup"><span data-stu-id="d4525-1255">8602 (0x219A)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1256">Ein Querverweis wird lokal mit dem gleichen Namen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4525-1256">A cross reference is in use locally with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**Fehler-DS konnte keinen \_ \_ \_ \_ SPN \_ für \_ Gelöschte \_ Domäne ableiten.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_FOR\_DELETED\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1258">8603 (0x219b)</span><span class="sxs-lookup"><span data-stu-id="d4525-1258">8603 (0x219B)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1259">Die DS kann keinen Dienst Prinzipal Namen (Service Principal Name, SPN) ableiten, mit dem der Zielserver gegenseitig authentifiziert werden kann, da die Domäne des Servers aus der Gesamtstruktur gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="d4525-1259">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the server's domain has been deleted from the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**Fehler \_ DS \_ \_ \_ kann nicht mit \_ Beschreib barem \_ NC herabgestuft werden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR\_DS\_CANT\_DEMOTE\_WITH\_WRITEABLE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1261">8604 (0x219c)</span><span class="sxs-lookup"><span data-stu-id="d4525-1261">8604 (0x219C)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1262">Beschreibbare NCS verhindern, dass dieser Domänen Controller herabgestuft wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-1262">Writeable NCs prevent this DC from demoting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**Fehler \_ DS \_ doppelte \_ ID \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR\_DS\_DUPLICATE\_ID\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1264">8605 (0x219d)</span><span class="sxs-lookup"><span data-stu-id="d4525-1264">8605 (0x219D)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1265">Das angeforderte Objekt hat einen nicht eindeutigen Bezeichner und kann nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1265">The requested object has a non-unique identifier and cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**Fehler- \_ DS \_ unzureichende \_ attr \_ zum Erstellen des \_ \_ Objekts**</span><span class="sxs-lookup"><span data-stu-id="d4525-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR\_DS\_INSUFFICIENT\_ATTR\_TO\_CREATE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1267">8606 (0x219e)</span><span class="sxs-lookup"><span data-stu-id="d4525-1267">8606 (0x219E)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1268">Zum Erstellen eines Objekts wurden unzureichende Attribute angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4525-1268">Insufficient attributes were given to create an object.</span></span> <span data-ttu-id="d4525-1269">Dieses Objekt ist möglicherweise nicht vorhanden, weil es möglicherweise gelöscht wurde und bereits eine Garbage Collection durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d4525-1269">This object may not exist because it may have been deleted and already garbage collected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**Fehler- \_ DS- \_ Gruppen \_ Konvertierungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4525-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**ERROR\_DS\_GROUP\_CONVERSION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1271">8607 (0x219f)</span><span class="sxs-lookup"><span data-stu-id="d4525-1271">8607 (0x219F)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1272">Die Gruppe kann aufgrund von Attribut Einschränkungen für den angeforderten Gruppentyp nicht konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1272">The group cannot be converted due to attribute restrictions on the requested group type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**Fehler-DS-Fehler beim \_ \_ Verschieben der APP- \_ \_ \_ Basis \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d4525-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_BASIC\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1274">8608 (0x21a0)</span><span class="sxs-lookup"><span data-stu-id="d4525-1274">8608 (0x21A0)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1275">Die Domänen übergreifende Verschiebung von nicht leeren grundlegenden Anwendungs Gruppen ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1275">Cross-domain move of non-empty basic application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**Fehler-DS-Fehler beim \_ \_ Verschieben der APP- \_ \_ \_ Abfrage \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d4525-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_QUERY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1277">8609 (0x21a1)</span><span class="sxs-lookup"><span data-stu-id="d4525-1277">8609 (0x21A1)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1278">Domänen übergreifende Verschiebung von nicht leeren Abfrage basierten Anwendungs Gruppen ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1278">Cross-domain move of non-empty query based application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**Fehler- \_ DS- \_ Rolle \_ nicht \_ überprüft**</span><span class="sxs-lookup"><span data-stu-id="d4525-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERROR\_DS\_ROLE\_NOT\_VERIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1280">8610 (0x21a2)</span><span class="sxs-lookup"><span data-stu-id="d4525-1280">8610 (0x21A2)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1281">Der Besitz der Rolle der Rolle konnte nicht überprüft werden, da die zugehörige Verzeichnis Partition mit mindestens einem Replikations Partner nicht erfolgreich repliziert wurde.</span><span class="sxs-lookup"><span data-stu-id="d4525-1281">The FSMO role ownership could not be verified because its directory partition has not replicated successfully with at least one replication partner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**Fehler der \_ DS- \_ WKO- \_ Container \_ darf nicht \_ \_ speziell sein**</span><span class="sxs-lookup"><span data-stu-id="d4525-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERROR\_DS\_WKO\_CONTAINER\_CANNOT\_BE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1283">8611 (0x21a3)</span><span class="sxs-lookup"><span data-stu-id="d4525-1283">8611 (0x21A3)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1284">Der Zielcontainer für eine Umleitung eines bekannten Objekt Containers darf nicht bereits ein spezieller Container sein.</span><span class="sxs-lookup"><span data-stu-id="d4525-1284">The target container for a redirection of a well known object container cannot already be a special container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**Fehler \_ \_ \_ beim Umbenennen \_ der Domäne in \_ Bearbeitung**</span><span class="sxs-lookup"><span data-stu-id="d4525-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR\_DS\_DOMAIN\_RENAME\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1286">8612 (0x21a4)</span><span class="sxs-lookup"><span data-stu-id="d4525-1286">8612 (0x21A4)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1287">Der Verzeichnisdienst kann den angeforderten Vorgang nicht ausführen, weil ein Domänen Umbenennungs Vorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4525-1287">The Directory Service cannot perform the requested operation because a domain rename operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**Fehler \_ DS \_ vorhandenes untergeordnetes \_ AD- \_ \_ NC**</span><span class="sxs-lookup"><span data-stu-id="d4525-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR\_DS\_EXISTING\_AD\_CHILD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1289">8613 (0x21a5)</span><span class="sxs-lookup"><span data-stu-id="d4525-1289">8613 (0x21A5)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1290">Der Verzeichnisdienst hat eine untergeordnete Partition unter dem angeforderten Partitionsnamen erkannt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1290">The directory service detected a child partition below the requested partition name.</span></span> <span data-ttu-id="d4525-1291">Die Partitions Hierarchie muss in einer Top-Down-Methode erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1291">The partition hierarchy must be created in a top down method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**Fehler \_ der \_ repl- \_ Lebensdauer \_ überschritten.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR\_DS\_REPL\_LIFETIME\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1293">8614 (0x21a6)</span><span class="sxs-lookup"><span data-stu-id="d4525-1293">8614 (0x21A6)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1294">Der Verzeichnisdienst kann nicht mit diesem Server repliziert werden, weil die Zeit seit der letzten Replikation mit diesem Server die Tombstone-Lebensdauer überschritten hat.</span><span class="sxs-lookup"><span data-stu-id="d4525-1294">The directory service cannot replicate with this server because the time since the last replication with this server has exceeded the tombstone lifetime.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**Fehler- \_ DS \_ \_ in \_ System \_ Container nicht zulässig**</span><span class="sxs-lookup"><span data-stu-id="d4525-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR\_DS\_DISALLOWED\_IN\_SYSTEM\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1296">8615 (0x21a7)</span><span class="sxs-lookup"><span data-stu-id="d4525-1296">8615 (0x21A7)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1297">Der angeforderte Vorgang ist für ein Objekt im System Container nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1297">The requested operation is not allowed on an object under the system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**Fehler- \_ DS \_ LDAP- \_ Sende Warteschlange \_ \_ voll**</span><span class="sxs-lookup"><span data-stu-id="d4525-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR\_DS\_LDAP\_SEND\_QUEUE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1299">8616 (0x21a8)</span><span class="sxs-lookup"><span data-stu-id="d4525-1299">8616 (0x21A8)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1300">Die LDAP-Server-netzwerksendewarteschlange wurde aufgefüllt, da der Client die Ergebnisse seiner Anforderungen nicht schnell genug verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d4525-1300">The LDAP servers network send queue has filled up because the client is not processing the results of its requests fast enough.</span></span> <span data-ttu-id="d4525-1301">Es werden keine weiteren Anforderungen verarbeitet, bis der Client abfängt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1301">No more requests will be processed until the client catches up.</span></span> <span data-ttu-id="d4525-1302">Wenn der Client nicht abfängt, wird er getrennt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1302">If the client does not catch up then it will be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**Fehler DS-DRA-Timeout- \_ \_ \_ \_ \_ Zeit Plan Fenster**</span><span class="sxs-lookup"><span data-stu-id="d4525-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERROR\_DS\_DRA\_OUT\_SCHEDULE\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1304">8617 (0x21a9)</span><span class="sxs-lookup"><span data-stu-id="d4525-1304">8617 (0x21A9)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1305">Die geplante Replikation wurde nicht durchgeführt, da das System ausgelastet war, um die Anforderung innerhalb des Zeit Plan Fensters auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1305">The scheduled replication did not take place because the system was too busy to execute the request within the schedule window.</span></span> <span data-ttu-id="d4525-1306">Die Replikations Warteschlange ist überlastet</span><span class="sxs-lookup"><span data-stu-id="d4525-1306">The replication queue is overloaded.</span></span> <span data-ttu-id="d4525-1307">Reduzieren Sie die Anzahl der Partner, oder verringern Sie die geplante Replikations Häufigkeit.</span><span class="sxs-lookup"><span data-stu-id="d4525-1307">Consider reducing the number of partners or decreasing the scheduled replication frequency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**Fehler- \_ DS- \_ Richtlinie \_ nicht \_ bekannt**</span><span class="sxs-lookup"><span data-stu-id="d4525-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR\_DS\_POLICY\_NOT\_KNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1309">8618 (0x21aa)</span><span class="sxs-lookup"><span data-stu-id="d4525-1309">8618 (0x21AA)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1310">Zu diesem Zeitpunkt kann nicht ermittelt werden, ob die branchreplikations Richtlinie auf dem Hub-Domänen Controller verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-1310">At this time, it cannot be determined if the branch replication policy is available on the hub domain controller.</span></span> <span data-ttu-id="d4525-1311">Wiederholen Sie den Vorgang zu einem späteren Zeitpunkt, um Replikations Latenzen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1311">Please retry at a later time to account for replication latencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**Fehler " \_ kein \_ Standort \_ Einstellungs \_ Objekt"**</span><span class="sxs-lookup"><span data-stu-id="d4525-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR\_NO\_SITE\_SETTINGS\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1313">8619 (0x21ab)</span><span class="sxs-lookup"><span data-stu-id="d4525-1313">8619 (0x21AB)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1314">Das Standort Einstellungs Objekt für den angegebenen Standort ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1314">The site settings object for the specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**Fehler \_ keine \_ geheimen Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="d4525-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR\_NO\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1316">8620 (0x21ac)</span><span class="sxs-lookup"><span data-stu-id="d4525-1316">8620 (0x21AC)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1317">Der lokale Konto Speicher enthält kein geheimes Material für das angegebene Konto.</span><span class="sxs-lookup"><span data-stu-id="d4525-1317">The local account store does not contain secret material for the specified account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**Fehler " \_ kein \_ Beschreib barer \_ DC \_ gefunden".**</span><span class="sxs-lookup"><span data-stu-id="d4525-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR\_NO\_WRITABLE\_DC\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1319">8621 (0x21ad)</span><span class="sxs-lookup"><span data-stu-id="d4525-1319">8621 (0x21AD)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1320">Es konnte kein Beschreib barer Domänen Controller in der Domäne gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1320">Could not find a writable domain controller in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**Fehler " \_ DS \_ kein \_ Server \_ Objekt"**</span><span class="sxs-lookup"><span data-stu-id="d4525-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR\_DS\_NO\_SERVER\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1322">8622 (0x21ae)</span><span class="sxs-lookup"><span data-stu-id="d4525-1322">8622 (0x21AE)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1323">Das Server Objekt für den Domänen Controller ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1323">The server object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**Fehler " \_ DS \_ kein \_ NTDSA- \_ Objekt"**</span><span class="sxs-lookup"><span data-stu-id="d4525-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR\_DS\_NO\_NTDSA\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1325">8623 (0x21af)</span><span class="sxs-lookup"><span data-stu-id="d4525-1325">8623 (0x21AF)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1326">Das NTDS-Einstellungs Objekt für den Domänen Controller ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1326">The NTDS Settings object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**Fehler " \_ DS \_ nicht- \_ ASQ- \_ Suche"**</span><span class="sxs-lookup"><span data-stu-id="d4525-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR\_DS\_NON\_ASQ\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1328">8624 (0x21b0)</span><span class="sxs-lookup"><span data-stu-id="d4525-1328">8624 (0x21B0)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1329">Der angeforderte Suchvorgang wird für ASQ-suchen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1329">The requested search operation is not supported for ASQ searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**Fehler bei DS-Überwachungs Fehler \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR\_DS\_AUDIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1331">8625 (0x21b1)</span><span class="sxs-lookup"><span data-stu-id="d4525-1331">8625 (0x21B1)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1332">Für den Vorgang konnte kein erforderliches Überwachungs Ereignis generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1332">A required audit event could not be generated for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**Fehler \_ DS \_ ungültige \_ \_ suchflag- \_ Unterstruktur.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_SUBTREE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1334">8626 (0x21b2)</span><span class="sxs-lookup"><span data-stu-id="d4525-1334">8626 (0x21B2)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1335">Die Suchflags für das Attribut sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1335">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="d4525-1336">Das Teilstruktur-indexbit ist nur für einwertige Attribute gültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1336">The subtree index bit is valid only on single valued attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**Fehler- \_ DS \_ ungültiges \_ \_ suchflag- \_ Tupel.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_TUPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1338">8627 (0x21b3)</span><span class="sxs-lookup"><span data-stu-id="d4525-1338">8627 (0x21B3)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1339">Die Suchflags für das Attribut sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1339">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="d4525-1340">Das tupelindexbit ist nur für Attribute von Unicode-Zeichen folgen gültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1340">The tuple index bit is valid only on attributes of Unicode strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**Fehler- \_ DS- \_ Hierarchie \_ Tabelle \_ zu \_ tief**</span><span class="sxs-lookup"><span data-stu-id="d4525-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_TOO\_DEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1342">8628 (0x21b4)</span><span class="sxs-lookup"><span data-stu-id="d4525-1342">8628 (0x21B4)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1343">Die Adressbücher sind zu tief geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1343">The address books are nested too deeply.</span></span> <span data-ttu-id="d4525-1344">Fehler beim Erstellen der Hierarchie Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d4525-1344">Failed to build the hierarchy table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**Fehler \_ DS-Vektor für beschädigte \_ \_ \_ Utd- \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="d4525-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR\_DS\_DRA\_CORRUPT\_UTD\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1346">8629 (0x21b5)</span><span class="sxs-lookup"><span data-stu-id="d4525-1346">8629 (0x21B5)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1347">Der angegebene Aktualitäts Vektor ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="d4525-1347">The specified up-to-date-ness vector is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**Fehler \_ DS \_ DRA- \_ Geheimnisse \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="d4525-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR\_DS\_DRA\_SECRETS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1349">8630 (0x21b6)</span><span class="sxs-lookup"><span data-stu-id="d4525-1349">8630 (0x21B6)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1350">Die Anforderung zum Replizieren von geheimen Schlüsseln wird verweigert.</span><span class="sxs-lookup"><span data-stu-id="d4525-1350">The request to replicate secrets is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**Fehler- \_ DS \_ reservierte \_ MAPI- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d4525-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR\_DS\_RESERVED\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1352">8631 (0x21b7)</span><span class="sxs-lookup"><span data-stu-id="d4525-1352">8631 (0x21B7)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1353">Fehler beim Aktualisieren des Schemas: der MAPI-Bezeichner ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="d4525-1353">Schema update failed: The MAPI identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**Fehler \_ DS- \_ MAPI- \_ ID \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="d4525-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR\_DS\_MAPI\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1355">8632 (0x21b8)</span><span class="sxs-lookup"><span data-stu-id="d4525-1355">8632 (0x21B8)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1356">Fehler beim Aktualisieren des Schemas: Es sind keine MAPI-Bezeichner verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4525-1356">Schema update failed: There are no MAPI identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**Fehler- \_ DS in \_ DRA \_ fehlt \_ krbtgt \_ Secret**</span><span class="sxs-lookup"><span data-stu-id="d4525-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR\_DS\_DRA\_MISSING\_KRBTGT\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1358">8633 (0x21b9)</span><span class="sxs-lookup"><span data-stu-id="d4525-1358">8633 (0x21B9)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1359">Der Replikations Vorgang ist fehlgeschlagen, da die erforderlichen Attribute des lokalen krbtgt-Objekts fehlen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1359">The replication operation failed because the required attributes of the local krbtgt object are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**Fehler \_ DS \_ Domänen \_ Name ist \_ \_ in der \_ Gesamtstruktur vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR\_DS\_DOMAIN\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1361">8634 (0x21ba)</span><span class="sxs-lookup"><span data-stu-id="d4525-1361">8634 (0x21BA)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1362">Der Domänen Name der vertrauenswürdigen Domäne ist bereits in der Gesamtstruktur vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1362">The domain name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**Fehler \_ DS \_ - \_ flatname ist \_ \_ in der \_ Gesamtstruktur vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR\_DS\_FLAT\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1364">8635 (0x21bb)</span><span class="sxs-lookup"><span data-stu-id="d4525-1364">8635 (0x21BB)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1365">Der flatname der vertrauenswürdigen Domäne ist bereits in der Gesamtstruktur vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1365">The flat name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**Fehler bei \_ ungültigem \_ Benutzer \_ Prinzipal \_ Namen**</span><span class="sxs-lookup"><span data-stu-id="d4525-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR\_INVALID\_USER\_PRINCIPAL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1367">8636 (0x21bc)</span><span class="sxs-lookup"><span data-stu-id="d4525-1367">8636 (0x21BC)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1368">Der Benutzer Prinzipal Name (User Principal Name, UPN) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d4525-1368">The User Principal Name (UPN) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**Fehler \_ DS-OID zugeordnete \_ Gruppe darf \_ \_ \_ \_ keine \_ Mitglieder aufweisen.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR\_DS\_OID\_MAPPED\_GROUP\_CANT\_HAVE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1370">8637 (0x21bd)</span><span class="sxs-lookup"><span data-stu-id="d4525-1370">8637 (0x21BD)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1371">OID zugeordnete Gruppen dürfen keine Member aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1371">OID mapped groups cannot have members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**Fehler- \_ DS- \_ OID \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d4525-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR\_DS\_OID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1373">8638 (0x21be)</span><span class="sxs-lookup"><span data-stu-id="d4525-1373">8638 (0x21BE)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1374">Die angegebene OID wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1374">The specified OID cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**Fehler \_ DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERROR\_DS\_DRA\_RECYCLED\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1376">8639 (0x21bf)</span><span class="sxs-lookup"><span data-stu-id="d4525-1376">8639 (0x21BF)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1377">Der Replikations Vorgang ist fehlgeschlagen, da das Zielobjekt, auf das durch einen Linkwert verwiesen wird,</span><span class="sxs-lookup"><span data-stu-id="d4525-1377">The replication operation failed because the target object referred by a link value is recycled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**Fehler- \_ DS \_ unzulässige \_ NC- \_ Umleitung**</span><span class="sxs-lookup"><span data-stu-id="d4525-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR\_DS\_DISALLOWED\_NC\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1379">8640 (0x21c0)</span><span class="sxs-lookup"><span data-stu-id="d4525-1379">8640 (0x21C0)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1380">Beim Umleitungs Vorgang ist ein Fehler aufgetreten, da sich das Zielobjekt in einem anderen NC als der Domänen-NC des aktuellen Domänen Controllers befindet.</span><span class="sxs-lookup"><span data-stu-id="d4525-1380">The redirect operation failed because the target object is in a NC different from the domain NC of the current domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**Fehler \_ DS \_ High \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="d4525-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR\_DS\_HIGH\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1382">8641 (0x21c1)</span><span class="sxs-lookup"><span data-stu-id="d4525-1382">8641 (0x21C1)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1383">Die Funktionsebene des AD LDS Konfigurations Satzes kann nicht auf den angeforderten Wert gesenkt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1383">The functional level of the AD LDS configuration set cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**Fehler \_ DS \_ High \_ DSA- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="d4525-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR\_DS\_HIGH\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1385">8642 (0x21c2)</span><span class="sxs-lookup"><span data-stu-id="d4525-1385">8642 (0x21C2)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1386">Die Funktionsebene der Domäne (oder Gesamtstruktur) kann nicht auf den angeforderten Wert gesenkt werden.</span><span class="sxs-lookup"><span data-stu-id="d4525-1386">The functional level of the domain (or forest) cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**Fehler \_ DS \_ niedrige \_ ADLDS- \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="d4525-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR\_DS\_LOW\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1388">8643 (0x21c3)</span><span class="sxs-lookup"><span data-stu-id="d4525-1388">8643 (0x21C3)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1389">Die Funktionsebene des AD LDS Konfigurations Satzes kann nicht auf den angeforderten Wert festgelegt werden, da mindestens eine ADLDS-Instanz vorhanden ist, die sich auf einer niedrigeren inkompatiblen Funktionsebene befindet.</span><span class="sxs-lookup"><span data-stu-id="d4525-1389">The functional level of the AD LDS configuration set cannot be raised to the requested value, because there exist one or more ADLDS instances that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**Fehler \_ Domänen- \_ sid identisch mit der \_ \_ \_ lokalen \_ Arbeitsstation**</span><span class="sxs-lookup"><span data-stu-id="d4525-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**ERROR\_DOMAIN\_SID\_SAME\_AS\_LOCAL\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1391">8644 (0x21c4)</span><span class="sxs-lookup"><span data-stu-id="d4525-1391">8644 (0x21C4)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1392">Der Domänen Beitritt kann nicht abgeschlossen werden, da die SID der Domäne, die Sie beitreten wollten, mit der SID dieses Computers identisch ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-1392">The domain join cannot be completed because the SID of the domain you attempted to join was identical to the SID of this machine.</span></span> <span data-ttu-id="d4525-1393">Dies ist ein Symptom für eine nicht ordnungsgemäß geklonte Betriebssystem Installation.</span><span class="sxs-lookup"><span data-stu-id="d4525-1393">This is a symptom of an improperly cloned operating system install.</span></span> <span data-ttu-id="d4525-1394">Sie sollten systreup auf diesem Computer ausführen, um eine neue Computer-SID zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d4525-1394">You should run sysprep on this machine in order to generate a new machine SID.</span></span> <span data-ttu-id="d4525-1395">Unter <https://go.microsoft.com/fwlink/p/?linkid=168895> finden Sie weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1395">Please see <https://go.microsoft.com/fwlink/p/?linkid=168895> for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**Fehler beim Wiederherstellen der \_ \_ Sam- \_ \_ Validierung \_**</span><span class="sxs-lookup"><span data-stu-id="d4525-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR\_DS\_UNDELETE\_SAM\_VALIDATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1397">8645 (0x21c5)</span><span class="sxs-lookup"><span data-stu-id="d4525-1397">8645 (0x21C5)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1398">Der Vorgang zum Wiederherstellen ist fehlgeschlagen, weil der SAM-Kontoname oder der zusätzliche SAM-Konto Name des nicht gelöschten Objekts mit einem vorhandenen Live Objekt in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="d4525-1398">The undelete operation failed because the Sam Account Name or Additional Sam Account Name of the object being undeleted conflicts with an existing live object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4525-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**\_fehlerhafter \_ \_ Kontotyp**</span><span class="sxs-lookup"><span data-stu-id="d4525-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR\_INCORRECT\_ACCOUNT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4525-1400">8646 (0x21c6)</span><span class="sxs-lookup"><span data-stu-id="d4525-1400">8646 (0x21C6)</span></span>
</dt> <dt>



<span data-ttu-id="d4525-1401">Das System ist für das angegebene Konto nicht autorisierend und kann daher den Vorgang nicht durchführen.</span><span class="sxs-lookup"><span data-stu-id="d4525-1401">The system is not authoritative for the specified account and therefore cannot complete the operation.</span></span> <span data-ttu-id="d4525-1402">Wiederholen Sie den Vorgang mithilfe des Anbieters, der diesem Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4525-1402">Please retry the operation using the provider associated with this account.</span></span> <span data-ttu-id="d4525-1403">Wenn es sich hierbei um einen Online Anbieter handelt, verwenden Sie die Online Website des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="d4525-1403">If this is an online provider please use the provider's online site.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="d4525-1404">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4525-1404">Requirements</span></span>



| <span data-ttu-id="d4525-1405">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4525-1405">Requirement</span></span> | <span data-ttu-id="d4525-1406">Wert</span><span class="sxs-lookup"><span data-stu-id="d4525-1406">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4525-1407">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4525-1407">Minimum supported client</span></span><br/> | <span data-ttu-id="d4525-1408">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4525-1408">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d4525-1409">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4525-1409">Minimum supported server</span></span><br/> | <span data-ttu-id="d4525-1410">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4525-1410">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4525-1411">Header</span><span class="sxs-lookup"><span data-stu-id="d4525-1411">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4525-1412"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4525-1412"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4525-1413">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4525-1413">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4525-1414">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="d4525-1414">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




