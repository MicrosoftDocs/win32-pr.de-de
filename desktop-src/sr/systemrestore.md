---
title: SystemRestore-Klasse
description: Bietet Methoden zum Deaktivieren und Aktivieren der Überwachung, zum Auflisten verfügbarer Wiederherstellungspunkte und zum Initiieren einer Wiederherstellung auf dem lokalen System.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- System Restore-Systemwiederherstellung
- System Restore Class System Restore, beschrieben
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040731"
---
# <a name="systemrestore-class"></a><span data-ttu-id="dd099-105">SystemRestore-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd099-105">SystemRestore class</span></span>

<span data-ttu-id="dd099-106">Bietet Methoden zum Deaktivieren und Aktivieren der Überwachung, zum Auflisten verfügbarer Wiederherstellungspunkte und zum Initiieren einer Wiederherstellung auf dem lokalen System.</span><span class="sxs-lookup"><span data-stu-id="dd099-106">Provides methods for disabling and enabling monitoring, listing available restore points, and initiating a restore on the local system.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd099-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd099-107">Syntax</span></span>

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a><span data-ttu-id="dd099-108">Member</span><span class="sxs-lookup"><span data-stu-id="dd099-108">Members</span></span>

<span data-ttu-id="dd099-109">Die **SystemRestore** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd099-109">The **SystemRestore** class has these types of members:</span></span>

-   [<span data-ttu-id="dd099-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="dd099-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd099-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd099-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd099-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="dd099-112">Methods</span></span>

<span data-ttu-id="dd099-113">Die **SystemRestore** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dd099-113">The **SystemRestore** class has these methods.</span></span>



| <span data-ttu-id="dd099-114">Methode</span><span class="sxs-lookup"><span data-stu-id="dd099-114">Method</span></span>                                                             | <span data-ttu-id="dd099-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd099-115">Description</span></span>                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="dd099-116">**CreateRestorePoint**</span><span class="sxs-lookup"><span data-stu-id="dd099-116">**CreateRestorePoint**</span></span>](createrestorepoint-systemrestore.md)     | <span data-ttu-id="dd099-117">Erstellt einen Wiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="dd099-117">Creates a restore point.</span></span><br/>                         |
| [<span data-ttu-id="dd099-118">**Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="dd099-118">**Disable**</span></span>](disable-systemrestore.md)                           | <span data-ttu-id="dd099-119">Deaktiviert die Überwachung auf einem bestimmten Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="dd099-119">Disables monitoring on a particular drive.</span></span><br/>       |
| [<span data-ttu-id="dd099-120">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="dd099-120">**Enable**</span></span>](enable-systemrestore.md)                             | <span data-ttu-id="dd099-121">Aktiviert die Überwachung auf einem bestimmten Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="dd099-121">Enables monitoring on a particular drive.</span></span><br/>        |
| [<span data-ttu-id="dd099-122">**Getlastrestorestatus**</span><span class="sxs-lookup"><span data-stu-id="dd099-122">**GetLastRestoreStatus**</span></span>](getlastrestorestatus-systemrestore.md) | <span data-ttu-id="dd099-123">Ruft den Status der letzten Systemwiederherstellung ab.</span><span class="sxs-lookup"><span data-stu-id="dd099-123">Retrieves the status of the last system restore.</span></span><br/> |
| [<span data-ttu-id="dd099-124">**Restore**</span><span class="sxs-lookup"><span data-stu-id="dd099-124">**Restore**</span></span>](restore-systemrestore.md)                           | <span data-ttu-id="dd099-125">Initiiert eine Systemwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="dd099-125">Initiates a system restore.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="dd099-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd099-126">Properties</span></span>

<span data-ttu-id="dd099-127">Die **SystemRestore** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd099-127">The **SystemRestore** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd099-128">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="dd099-128">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd099-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd099-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="dd099-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd099-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd099-131">Der Zeitpunkt, zu dem die Zustandsänderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="dd099-131">The time at which the state change occurred.</span></span>

</dd> <dt>

<span data-ttu-id="dd099-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd099-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd099-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd099-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="dd099-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd099-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd099-135">Die Beschreibung, die angezeigt werden soll, damit der Benutzer problemlos einen Wiederherstellungspunkt identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="dd099-135">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="dd099-136">Die maximale Länge einer ANSI-Zeichenfolge beträgt Max \_ .</span><span class="sxs-lookup"><span data-stu-id="dd099-136">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="dd099-137">Die maximale Länge einer Unicode-Zeichenfolge ist Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dd099-137">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="dd099-138">Weitere Informationen finden Sie unter [Wiederherstellungspunkt-Beschreibungs Text](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="dd099-138">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd099-139">**EventType**</span><span class="sxs-lookup"><span data-stu-id="dd099-139">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd099-140">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd099-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd099-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd099-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd099-142">Art des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="dd099-142">The type of event.</span></span> <span data-ttu-id="dd099-143">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dd099-143">This member can be one of the following values.</span></span>



| <span data-ttu-id="dd099-144">Wert</span><span class="sxs-lookup"><span data-stu-id="dd099-144">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="dd099-145">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dd099-145">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="dd099-146"><dt>**Anfang \_ \_System \_ Änderung**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-146"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="dd099-147">Eine Systemänderung wurde begonnen.</span><span class="sxs-lookup"><span data-stu-id="dd099-147">A system change has begun.</span></span> <span data-ttu-id="dd099-148">Bei einem nachfolgenden, nicht aufzurufenden Befehl wird kein neuer Wiederherstellungspunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd099-148">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="dd099-149">Für nachfolgende Aufrufe müssen die Systemänderung am Ende \_ \_ \_ und nicht das Ende der \_ Systemänderung verwendet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="dd099-149">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="dd099-150"><dt>**Anfang \_ System \_ Änderung**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-150"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="dd099-151">Eine Systemänderung wurde begonnen.</span><span class="sxs-lookup"><span data-stu-id="dd099-151">A system change has begun.</span></span><br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="dd099-152"><dt>**Ende \_ \_System \_ Änderung**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-152"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="dd099-153">Eine Systemänderung wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="dd099-153">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="dd099-154"><dt>**Ende \_ System \_ Änderung**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-154"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="dd099-155">Eine Systemänderung wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="dd099-155">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="dd099-156">**Restorepointtype**</span><span class="sxs-lookup"><span data-stu-id="dd099-156">**RestorePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd099-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd099-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd099-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd099-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd099-159">Der Typ des Wiederherstellungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="dd099-159">The type of restore point.</span></span> <span data-ttu-id="dd099-160">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dd099-160">This member can be one of the following values.</span></span>



| <span data-ttu-id="dd099-161">Wert</span><span class="sxs-lookup"><span data-stu-id="dd099-161">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="dd099-162">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dd099-162">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="dd099-163"><dt>**Anwendung \_ Installieren**</dt> von <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-163"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="dd099-164">Eine Anwendung wurde installiert.</span><span class="sxs-lookup"><span data-stu-id="dd099-164">An application has been installed.</span></span><br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="dd099-165"><dt>**Anwendung \_ Deinstallieren**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-165"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="dd099-166">Eine Anwendung wurde deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="dd099-166">An application has been uninstalled.</span></span><br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="dd099-167"><dt>**Abgebrochen \_ Vorgang**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-167"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="dd099-168">Eine Anwendung muss den erstellten Wiederherstellungspunkt löschen.</span><span class="sxs-lookup"><span data-stu-id="dd099-168">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="dd099-169">Beispielsweise verwendet eine Anwendung dieses Flag, wenn ein Benutzer eine Installation abbricht.</span><span class="sxs-lookup"><span data-stu-id="dd099-169">For example, an application would use this flag when a user cancels an installation.</span></span> <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="dd099-170"><dt>**Gerät \_ Treiber \_ Installation**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-170"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="dd099-171">Ein Gerätetreiber wurde installiert.</span><span class="sxs-lookup"><span data-stu-id="dd099-171">A device driver has been installed.</span></span><br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="dd099-172"><dt>**Ändern \_ Einstellungen**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-172"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="dd099-173">Eine Anwendung verfügt über Features, die hinzugefügt oder entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="dd099-173">An application has had features added or removed.</span></span><br/>                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="dd099-174">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="dd099-174">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd099-175">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd099-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd099-176">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd099-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd099-177">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="dd099-177">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dd099-178">Die Sequenznummer des Wiederherstellungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="dd099-178">The sequence number of the restore point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd099-179">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd099-179">Remarks</span></span>

<span data-ttu-id="dd099-180">Sie können eine Liste von Wiederherstellungs Punkten abrufen, indem Sie die Methode " [**slibemservices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) " verwenden, um eine Sammlung von **SystemRestore** -Objekten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dd099-180">You can obtain a list of restore points by using the [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) method to retrieve a collection of **SystemRestore** objects.</span></span> <span data-ttu-id="dd099-181">Sie können die Klasseneigenschaften verwenden, um den Wiederherstellungspunkt zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dd099-181">You can use the class properties to identify the restore point.</span></span>

## <a name="examples"></a><span data-ttu-id="dd099-182">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd099-182">Examples</span></span>

<span data-ttu-id="dd099-183">Das folgende Beispielskript listet die aktuellen Wiederherstellungspunkte auf.</span><span class="sxs-lookup"><span data-stu-id="dd099-183">The following sample script enumerates the current restore points.</span></span>


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a><span data-ttu-id="dd099-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd099-184">Requirements</span></span>



| <span data-ttu-id="dd099-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd099-185">Requirement</span></span> | <span data-ttu-id="dd099-186">Wert</span><span class="sxs-lookup"><span data-stu-id="dd099-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dd099-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd099-187">Minimum supported client</span></span><br/> | <span data-ttu-id="dd099-188">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd099-188">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dd099-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd099-189">Minimum supported server</span></span><br/> | <span data-ttu-id="dd099-190">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd099-190">None supported</span></span><br/>                                                         |
| <span data-ttu-id="dd099-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd099-191">Namespace</span></span><br/>                | <span data-ttu-id="dd099-192">\\Standardwert</span><span class="sxs-lookup"><span data-stu-id="dd099-192">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="dd099-193">MOF</span><span class="sxs-lookup"><span data-stu-id="dd099-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd099-194"><dt>SR. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-194"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd099-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd099-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd099-196">Windows-Verwaltungsinstrumentation</span><span class="sxs-lookup"><span data-stu-id="dd099-196">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

