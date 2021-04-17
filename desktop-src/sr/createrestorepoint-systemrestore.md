---
title: Methode "foraterestorepoint" der SystemRestore-Klasse
description: Erstellt einen Wiederherstellungspunkt.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Methode zum Wiederherstellen von "foraterestorepoint"
- Methode zum Wiederherstellen der Methode "foraterestorepoint", System Restore-Klasse
- System Restore-Klassen System Wiederherstellung, Methode ' Methode '
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477145"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a><span data-ttu-id="4e6dd-106">Methode "foraterestorepoint" der SystemRestore-Klasse</span><span class="sxs-lookup"><span data-stu-id="4e6dd-106">CreateRestorePoint method of the SystemRestore class</span></span>

<span data-ttu-id="4e6dd-107">Erstellt einen Wiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-107">Creates a restore point.</span></span>

<span data-ttu-id="4e6dd-108">Diese Methode ist das Skript fähige Äquivalent der [**srsettrestorepoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-108">This method is the scriptable equivalent of the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e6dd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e6dd-109">Syntax</span></span>


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a><span data-ttu-id="4e6dd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e6dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e6dd-111">*Beschreibung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e6dd-111">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e6dd-112">Die Beschreibung, die angezeigt werden soll, damit der Benutzer problemlos einen Wiederherstellungspunkt identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-112">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="4e6dd-113">Die maximale Länge einer ANSI-Zeichenfolge beträgt Max \_ .</span><span class="sxs-lookup"><span data-stu-id="4e6dd-113">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="4e6dd-114">Die maximale Länge einer Unicode-Zeichenfolge ist Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4e6dd-114">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="4e6dd-115">Weitere Informationen finden Sie unter [Wiederherstellungspunkt-Beschreibungs Text](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="4e6dd-115">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e6dd-116">*Restorepointtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e6dd-116">*RestorePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e6dd-117">Der Typ des Wiederherstellungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-117">The type of restore point.</span></span> <span data-ttu-id="4e6dd-118">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-118">This member can be one of the following values.</span></span>



| <span data-ttu-id="4e6dd-119">Typ des Wiederherstellungs Punkts</span><span class="sxs-lookup"><span data-stu-id="4e6dd-119">Restore point type</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="4e6dd-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4e6dd-120">Meaning</span></span>                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="4e6dd-121"><dt>**Anwendung \_ Installieren**</dt> von <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-121"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="4e6dd-122">Eine Anwendung wurde installiert.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-122">An application has been installed.</span></span><br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="4e6dd-123"><dt>**Anwendung \_ Deinstallieren**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-123"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="4e6dd-124">Eine Anwendung wurde deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-124">An application has been uninstalled.</span></span><br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="4e6dd-125"><dt>**Gerät \_ Treiber \_ Installation**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-125"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="4e6dd-126">Ein Gerätetreiber wurde installiert.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-126">A device driver has been installed.</span></span><br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="4e6dd-127"><dt>**Ändern \_ Einstellungen**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-127"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="4e6dd-128">Eine Anwendung verfügt über Features, die hinzugefügt oder entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-128">An application has had features added or removed.</span></span><br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="4e6dd-129"><dt>**Abgebrochen \_ Vorgang**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-129"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="4e6dd-130">Eine Anwendung muss den erstellten Wiederherstellungspunkt löschen.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-130">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="4e6dd-131">Beispielsweise verwendet eine Anwendung dieses Flag, wenn ein Benutzer eine Installation abbricht.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-131">For example, an application would use this flag when a user cancels an installation.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4e6dd-132">*EventType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e6dd-132">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e6dd-133">Art des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-133">The type of event.</span></span> <span data-ttu-id="4e6dd-134">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-134">This member can be one of the following values.</span></span>



| <span data-ttu-id="4e6dd-135">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="4e6dd-135">Event type</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="4e6dd-136">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4e6dd-136">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="4e6dd-137"><dt>**Anfang \_ \_System \_ Änderung**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-137"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="4e6dd-138">Eine Systemänderung wurde begonnen.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-138">A system change has begun.</span></span> <span data-ttu-id="4e6dd-139">Bei einem nachfolgenden, nicht aufzurufenden Befehl wird kein neuer Wiederherstellungspunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-139">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="4e6dd-140">Für nachfolgende Aufrufe müssen die Systemänderung am Ende \_ \_ \_ und nicht das Ende der \_ Systemänderung verwendet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="4e6dd-140">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="4e6dd-141"><dt>**Anfang \_ System \_ Änderung**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-141"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="4e6dd-142">Eine Systemänderung wurde begonnen.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-142">A system change has begun.</span></span> <br/> <span data-ttu-id="4e6dd-143">Bei einem nachfolgenden-Rückruf muss die Systemänderung am Ende des Systems \_ \_ nicht \_ \_ geändert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="4e6dd-143">A subsequent call must use END\_SYSTEM\_CHANGE, not END\_NESTED\_SYSTEM\_CHANGE.</span></span><br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="4e6dd-144"><dt>**Ende \_ \_System \_ Änderung**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-144"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="4e6dd-145">Eine Systemänderung wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-145">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="4e6dd-146"><dt>**Ende \_ System \_ Änderung**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-146"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="4e6dd-147">Eine Systemänderung wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-147">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e6dd-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e6dd-148">Return value</span></span>

<span data-ttu-id="4e6dd-149">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-149">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4e6dd-150">Andernfalls gibt die Methode einen der com-Fehlercodes zurück, die in WinError. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-150">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e6dd-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e6dd-151">Remarks</span></span>

<span data-ttu-id="4e6dd-152">\* \* Windows 8: \* \*</span><span class="sxs-lookup"><span data-stu-id="4e6dd-152">\*\*Windows 8:  \*\*</span></span>

<span data-ttu-id="4e6dd-153">Ein neuer Registrierungsschlüssel ermöglicht Anwendungsentwicklern das Ändern der Häufigkeit der Wiederherstellungspunkt Erstellung.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-153">A new registry key enables application developers to change the frequency of restore-point creation.</span></span>

<span data-ttu-id="4e6dd-154">Anwendungen sollten diesen Schlüssel erstellen, um ihn zu verwenden, da er im System nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-154">Applications should create this key to use it because it will not preexist in the system.</span></span> <span data-ttu-id="4e6dd-155">Wenn der Schlüssel nicht vorhanden ist, wird standardmäßig Folgendes angewendet:</span><span class="sxs-lookup"><span data-stu-id="4e6dd-155">The following will apply by default if the key does not exist.</span></span> <span data-ttu-id="4e6dd-156">Wenn eine Anwendung die Methode "Methode zum Erstellen eines Wiederherstellungs Punkts" aufruft, überspringt **Windows das Erstellen** dieses neuen Wiederherstellungs Punkts, wenn in den letzten 24 Stunden Wiederherstellungspunkte erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-156">If an application calls the **CreateRestorePoint** method to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.</span></span> <span data-ttu-id="4e6dd-157">Die Methode " **kreaterestorepoint** " gibt " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-157">The **CreateRestorePoint** method returns **S\_OK**.</span></span>

<span data-ttu-id="4e6dd-158">Entwickler können Anwendungen schreiben, die den **DWORD** -Wert **systemrestorepointkreationfrequency** unter dem Registrierungsschlüssel **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-158">Developers can write applications that create the **DWORD** value **SystemRestorePointCreationFrequency** under the registry key **HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SystemRestore**.</span></span> <span data-ttu-id="4e6dd-159">Mit dem Wert dieses Registrierungsschlüssels kann die Häufigkeit der Wiederherstellungspunkt Erstellung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-159">The value of this registry key can change the frequency of restore point creation.</span></span> <span data-ttu-id="4e6dd-160">Mit dem Wert dieses Registrierungsschlüssels kann die Häufigkeit der Wiederherstellungspunkt Erstellung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-160">The value of this registry key can change the frequency of restore point creation.</span></span>

<span data-ttu-id="4e6dd-161">Wenn die Anwendung "" zum Erstellen eines Wiederherstellungs Punkts "" mit dem Wert "" auf " **", und** der Wert des Registrierungsschlüssels "0" aufruft, wird die Erstellung des neuen Wiederherstellungs Punkts nicht überspringt.</span><span class="sxs-lookup"><span data-stu-id="4e6dd-161">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.</span></span>

<span data-ttu-id="4e6dd-162">Wenn die Anwendung "" zum Erstellen eines Wiederherstellungs Punkts mit "" "" "" "" "," "und der Registrierungsschlüssel Wert" N "ist, überspringt die Systemwiederherstellung die Erstellung eines neuen Wiederherstellungs **Punkts, wenn** in den letzten N Minuten Wiederherstellungspunkte erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="4e6dd-162">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.</span></span>

## <a name="examples"></a><span data-ttu-id="4e6dd-163">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e6dd-163">Examples</span></span>


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="4e6dd-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e6dd-164">Requirements</span></span>



| <span data-ttu-id="4e6dd-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e6dd-165">Requirement</span></span> | <span data-ttu-id="4e6dd-166">Wert</span><span class="sxs-lookup"><span data-stu-id="4e6dd-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4e6dd-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e6dd-167">Minimum supported client</span></span><br/> | <span data-ttu-id="4e6dd-168">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e6dd-168">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4e6dd-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e6dd-169">Minimum supported server</span></span><br/> | <span data-ttu-id="4e6dd-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4e6dd-170">None supported</span></span><br/>                                                         |
| <span data-ttu-id="4e6dd-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e6dd-171">Namespace</span></span><br/>                | <span data-ttu-id="4e6dd-172">\\Standardwert</span><span class="sxs-lookup"><span data-stu-id="4e6dd-172">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="4e6dd-173">MOF</span><span class="sxs-lookup"><span data-stu-id="4e6dd-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e6dd-174"><dt>SR. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4e6dd-174"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e6dd-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e6dd-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e6dd-176">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="4e6dd-176">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





