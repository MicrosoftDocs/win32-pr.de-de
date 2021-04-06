---
description: Der strprivilege-Parameter der Methode "slibemprivilegeset. addasstring" und der Parameter "iprivilege" für "slibemprivilegeset. Add" erfordern Berechtigungs Zeichenfolgen aus "wbemprivilegeenum".
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Berechtigungs Konstanten (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759768"
---
# <a name="privilege-constants"></a><span data-ttu-id="475d8-103">Berechtigungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="475d8-103">Privilege Constants</span></span>

<span data-ttu-id="475d8-104">Der *strprivilege* -Parameter der Methode " [**slibemprivilegeset. addasstring**](swbemprivilegeset-addasstring.md) " und der Parameter " *iprivilege* " für " [**slibemprivilegeset. Add**](swbemprivilegeset-add.md) " erfordern Berechtigungs Zeichenfolgen aus " [wbemprivilegeenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)".</span><span class="sxs-lookup"><span data-stu-id="475d8-104">The *strPrivilege* parameter of the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method and the *iPrivilege* parameter for [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) require privilege strings from [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="475d8-105">Weitere Informationen zum Verwenden von Berechtigungs Konstanten finden Sie unter [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="475d8-105">For more information about how to use privilege constants, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="475d8-106">Die folgenden Konstanten sind in [**wbemprivilegeenumeration**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)definiert.</span><span class="sxs-lookup"><span data-stu-id="475d8-106">The following constants are defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="475d8-107">Die folgende Liste enthält die äquivalenten Konstanten für C++ und Zeichen folgen für die Skripterstellung.</span><span class="sxs-lookup"><span data-stu-id="475d8-107">The following list includes the equivalent constants for C++ and strings for scripting.</span></span> <span data-ttu-id="475d8-108">Um den Namen der Skripterstellung zu bilden, entfernen Sie "SE" und "Privilege" aus dem C++-Konstantennamen.</span><span class="sxs-lookup"><span data-stu-id="475d8-108">To form the scripting short name, remove the "Se" and "Privilege" from the C++ constant name.</span></span>

<span data-ttu-id="475d8-109">Im folgenden VBScript-Codebeispiel wird gezeigt, wie die RemoteShutdown-Berechtigung in einem Skript aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="475d8-109">The following VBScript code example shows how to enable the RemoteShutdown privilege in a script.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



<span data-ttu-id="475d8-110">Viele WMI-Methoden erfordern, dass mindestens eine Berechtigung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="475d8-110">Many WMI methods require that one or more permission be enabled.</span></span> <span data-ttu-id="475d8-111">Wenn einem Konto keine Berechtigung erteilt wurde, kann es für den Methoden Aufrufvorgang nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="475d8-111">If an account has not been granted a privilege, it cannot be enabled for the method call.</span></span>

<dl> <dt>

<span data-ttu-id="475d8-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemprivilegekreatetoken**</span><span class="sxs-lookup"><span data-stu-id="475d8-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="475d8-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-114">C++ Constant: **SE \_ Create \_ Token \_ Name** String: **secreatetokenprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-114">C++ constant: **SE\_CREATE\_TOKEN\_NAME** string: **SeCreateTokenPrivilege**</span></span>

<span data-ttu-id="475d8-115">Name der Skripterstellung **: "** ".</span><span class="sxs-lookup"><span data-stu-id="475d8-115">Scripting short name: **CreateToken**</span></span>

<span data-ttu-id="475d8-116">Erforderlich, um ein primäres Tokenobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="475d8-116">Required to create a primary token object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemprivilegeprimarytoken**</span><span class="sxs-lookup"><span data-stu-id="475d8-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-118">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="475d8-118">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-119">C++-Konstante: **seassignprimaryaufkenprivilege** -Zeichenfolge: **seassignprimaryanmelkenprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-119">C++ constant: **SeAssignPrimaryTokenPrivilege** string: **SeAssignPrimaryTokenPrivilege**</span></span>

<span data-ttu-id="475d8-120">Name der Skripterstellung: **zugriffprimarytoken**</span><span class="sxs-lookup"><span data-stu-id="475d8-120">Scripting short name: **AssignPrimaryToken**</span></span>

<span data-ttu-id="475d8-121">Ist erforderlich, um ein Token auf Prozessebene zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="475d8-121">Required to replace a process-level token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemprivilegelockmemory**</span><span class="sxs-lookup"><span data-stu-id="475d8-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-123">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="475d8-123">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-124">C++-Konstante: Zeichenfolge für den **\_ \_ Speicher \_ Namen der SE-Sperre** : **SeLockMemoryPrivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-124">C++ constant: **SE\_LOCK\_MEMORY\_NAME** string: **SeLockMemoryPrivilege**</span></span>

<span data-ttu-id="475d8-125">Kurzname für Skripterstellung: **lockmemory**</span><span class="sxs-lookup"><span data-stu-id="475d8-125">Scripting short name: **LockMemory**</span></span>

<span data-ttu-id="475d8-126">Zum Sperren von Seiten im Arbeitsspeicher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="475d8-126">Required to lock pages in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemprivilegilegeingekreasequota**</span><span class="sxs-lookup"><span data-stu-id="475d8-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="475d8-128">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-129">C++-Konstante: **SE \_ Erhöhung des \_ Kontingent \_ namens** String: **seinkreasequotaprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-129">C++ constant: **SE\_INCREASE\_QUOTA\_NAME** string: **SeIncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="475d8-130">Kurzname für Skripterstellung: Erstellungs **Berechtigung**</span><span class="sxs-lookup"><span data-stu-id="475d8-130">Scripting short name: **IncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="475d8-131">Erforderlich zum Anpassen von Speicher Kontingenten für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="475d8-131">Required to adjust memory quotas for a process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemprivilegemachineaccount**</span><span class="sxs-lookup"><span data-stu-id="475d8-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-133">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="475d8-133">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-134">C++-Konstante: **SE \_ Macine \_ Account \_ Name** String: **tarmachineaccountprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-134">C++ constant: **SE\_MACINE\_ACCOUNT\_NAME** string: **SeMachineAccountPrivilege**</span></span>

<span data-ttu-id="475d8-135">Kurzname für Skripterstellung: **MachineAccount**</span><span class="sxs-lookup"><span data-stu-id="475d8-135">Scripting short name: **MachineAccount**</span></span>

<span data-ttu-id="475d8-136">Erforderlich zum Hinzufügen von Arbeitsstationen zu einer Domäne.</span><span class="sxs-lookup"><span data-stu-id="475d8-136">Required to add workstations to a domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemprivilegetcb**</span><span class="sxs-lookup"><span data-stu-id="475d8-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-138">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="475d8-138">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-139">C++-Konstante: **SE \_ TCB \_ Name** String: **SeTcbPrivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-139">C++ constant: **SE\_TCB\_NAME** string: **SeTcbPrivilege**</span></span>

<span data-ttu-id="475d8-140">Kurzname für Skripterstellung: **TCB**</span><span class="sxs-lookup"><span data-stu-id="475d8-140">Scripting short name: **Tcb**</span></span>

<span data-ttu-id="475d8-141">Erforderlich, um als Teil des Betriebssystems zu agieren.</span><span class="sxs-lookup"><span data-stu-id="475d8-141">Required to act as part of the operating system.</span></span> <span data-ttu-id="475d8-142">Der Inhaber ist Teil der vertrauenswürdigen Computer Basis.</span><span class="sxs-lookup"><span data-stu-id="475d8-142">The holder is part of the trusted computer base.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemprivilegeseatur**</span><span class="sxs-lookup"><span data-stu-id="475d8-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-144">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="475d8-144">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-145">C++-Konstante: **SE- \_ Sicherheits \_ Namen** Zeichenfolge: **SeSecurityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-145">C++ constant: **SE\_SECURITY\_NAME** string: **SeSecurityPrivilege**</span></span>

<span data-ttu-id="475d8-146">Skript Kurzname: **Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="475d8-146">Scripting short name: **Security**</span></span>

<span data-ttu-id="475d8-147">Erforderlich zum Verwalten der Überwachung und des NT-Sicherheitsprotokolls.</span><span class="sxs-lookup"><span data-stu-id="475d8-147">Required to manage auditing and the NT security log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemprivilegetakeownership**</span><span class="sxs-lookup"><span data-stu-id="475d8-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-149">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="475d8-149">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-150">C++-Konstante **: \_ SE \_ Besitz \_ Name** Zeichenfolge **: "** "</span><span class="sxs-lookup"><span data-stu-id="475d8-150">C++ constant: **SE\_TAKE\_OWNERSHIP\_NAME** string: **SeTakeOwnershipPrivilege**</span></span>

<span data-ttu-id="475d8-151">Kurzname der Skripterstellung: **Take Ownership**</span><span class="sxs-lookup"><span data-stu-id="475d8-151">Scripting short name: **TakeOwnership**</span></span>

<span data-ttu-id="475d8-152">Erforderlich, um den Besitz von Dateien oder anderen Objekten ohne einen [*Access Control Eintrag*](/windows/desktop/SecGloss/a-gly) (ACE) in der *Zugriffs Steuerungs Liste* (DACL) zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="475d8-152">Required to assume ownership of files or other objects without having an [*Access Control Entry*](/windows/desktop/SecGloss/a-gly) (ACE) in the *discretionary access control list* (DACL).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemprivilegeloaddriver**</span><span class="sxs-lookup"><span data-stu-id="475d8-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-154">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="475d8-154">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-155">C++-Konstante **: \_ \_ Treiber** Zeichenfolge für "SE laden": **SeLoadDriverPrivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-155">C++ constant: **SE\_LOAD\_DRIVER** string: **SeLoadDriverPrivilege**</span></span>

<span data-ttu-id="475d8-156">Kurzname für Skripterstellung: **LoadDriver**</span><span class="sxs-lookup"><span data-stu-id="475d8-156">Scripting short name: **LoadDriver**</span></span>

<span data-ttu-id="475d8-157">Erforderlich zum Laden oder Entladen eines Gerätetreibers.</span><span class="sxs-lookup"><span data-stu-id="475d8-157">Required to load or unload a device driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemprivilegesystemprofile**</span><span class="sxs-lookup"><span data-stu-id="475d8-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-159">10 (0xa)</span><span class="sxs-lookup"><span data-stu-id="475d8-159">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-160">C++-Konstante: Name der namens Zeichenfolge für das **\_ System \_ Profil \_** : **sesystemprofileprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-160">C++ constant: **SE\_SYSTEM\_PROFILE\_NAME** string: **SeSystemProfilePrivilege**</span></span>

<span data-ttu-id="475d8-161">Kurzname für Skripterstellung: **Systemprofile**</span><span class="sxs-lookup"><span data-stu-id="475d8-161">Scripting short name: **SystemProfile**</span></span>

<span data-ttu-id="475d8-162">Erforderlich, um Profilinformationen zur Systemleistung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="475d8-162">Required to gather profile information about system performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemprivilegesystemtime**</span><span class="sxs-lookup"><span data-stu-id="475d8-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-164">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="475d8-164">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-165">C++-Konstante: **SE \_ SYSTEMTIME**- \_ namens Zeichenfolge: **SeSystemtimePrivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-165">C++ constant: **SE\_SYSTEMTIME**\_NAME string: **SeSystemtimePrivilege**</span></span>

<span data-ttu-id="475d8-166">Kurzname für Skripterstellung: **SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="475d8-166">Scripting short name: **Systemtime**</span></span>

<span data-ttu-id="475d8-167">Erforderlich, um die Systemzeit zu ändern.</span><span class="sxs-lookup"><span data-stu-id="475d8-167">Required to change the system time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemprivilegeprofilesingleprocess**</span><span class="sxs-lookup"><span data-stu-id="475d8-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-169">12 (0xc)</span><span class="sxs-lookup"><span data-stu-id="475d8-169">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-170">C++-Konstante: **SE \_ Prof \_ Single \_ Process \_ Name** String: **sprofilesingleprocessprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-170">C++ constant: **SE\_PROF\_SINGLE\_PROCESS\_NAME** string: **SeProfileSingleProcessPrivilege**</span></span>

<span data-ttu-id="475d8-171">Skript Kurzname: **profilesingleprocess**</span><span class="sxs-lookup"><span data-stu-id="475d8-171">Scripting short name: **ProfileSingleProcess**</span></span>

<span data-ttu-id="475d8-172">Erforderlich, um Profilinformationen für einen einzelnen Prozess zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="475d8-172">Required to gather profile information for a single process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemprivilegilegeingekreasebasepriority**</span><span class="sxs-lookup"><span data-stu-id="475d8-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-174">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="475d8-174">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-175">C++ Constant: **SE \_ Inc \_ \_ \_ Name der Basis Priorität** Zeichenfolge: **seinkreasebasepriorityprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-175">C++ constant: **SE\_INC\_BASE\_PRIORITY\_NAME** string: **SeIncreaseBasePriorityPrivilege**</span></span>

<span data-ttu-id="475d8-176">Name der Skripterstellung: **erstellebasepriority**</span><span class="sxs-lookup"><span data-stu-id="475d8-176">Scripting short name: **IncreaseBasePriority**</span></span>

<span data-ttu-id="475d8-177">Erforderlich, um die Planungs Priorität zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="475d8-177">Required to increase scheduling priority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemprivilegekreatepagefile**</span><span class="sxs-lookup"><span data-stu-id="475d8-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-179">14 (0xe)</span><span class="sxs-lookup"><span data-stu-id="475d8-179">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-180">C++-Konstante: **SE \_ Create \_ Pagefile \_ Name** String: **secreatepagefileprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-180">C++ constant: **SE\_CREATE\_PAGEFILE\_NAME** string: **SeCreatePagefilePrivilege**</span></span>

<span data-ttu-id="475d8-181">Kurzname für Skript **Erstellung: "** ".</span><span class="sxs-lookup"><span data-stu-id="475d8-181">Scripting short name: **CreatePagefile**</span></span>

<span data-ttu-id="475d8-182">Erforderlich zum Erstellen einer Pagefile-Datei.</span><span class="sxs-lookup"><span data-stu-id="475d8-182">Required to create a pagefile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemprivilegekreatepermanent**</span><span class="sxs-lookup"><span data-stu-id="475d8-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-184">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="475d8-184">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-185">C++-Konstante: **SE \_ Create \_ permanent \_ Name** String: **SeCreatePermanentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-185">C++ constant: **SE\_CREATE\_PERMANENT\_NAME** string: **SeCreatePermanentPrivilege**</span></span>

<span data-ttu-id="475d8-186">Kurzname für Skripterstellung: " **kreatepermanent** "</span><span class="sxs-lookup"><span data-stu-id="475d8-186">Scripting short name: **CreatePermanent**</span></span>

<span data-ttu-id="475d8-187">Erforderlich, um permanente freigegebene Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="475d8-187">Required to create permanent shared objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemprivilegebackup**</span><span class="sxs-lookup"><span data-stu-id="475d8-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-189">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="475d8-189">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-190">C++-Konstante: **SE \_ Backup \_ Name** String: " **sbackupprivilege** "</span><span class="sxs-lookup"><span data-stu-id="475d8-190">C++ constant: **SE\_BACKUP\_NAME** string: **SeBackupPrivilege**</span></span>

<span data-ttu-id="475d8-191">Kurzname für Skripterstellung: **Sicherung**</span><span class="sxs-lookup"><span data-stu-id="475d8-191">Scripting short name: **Backup**</span></span>

<span data-ttu-id="475d8-192">Zum Sichern von Dateien und Verzeichnissen erforderlich, unabhängig von der für die Datei angegebenen ACL.</span><span class="sxs-lookup"><span data-stu-id="475d8-192">Required to backup files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemprivilegerestore**</span><span class="sxs-lookup"><span data-stu-id="475d8-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-194">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="475d8-194">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-195">C++ Constant: **SE \_ Restore \_ Name** String: **SeRestorePrivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-195">C++ constant: **SE\_RESTORE\_NAME** string: **SeRestorePrivilege**</span></span>

<span data-ttu-id="475d8-196">Skript Kurzname: **Restore**</span><span class="sxs-lookup"><span data-stu-id="475d8-196">Scripting short name: **Restore**</span></span>

<span data-ttu-id="475d8-197">Ist erforderlich, um Dateien und Verzeichnisse unabhängig von der für die Datei angegebenen ACL wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="475d8-197">Required to restore files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemprivilegeshutdown**</span><span class="sxs-lookup"><span data-stu-id="475d8-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-199">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="475d8-199">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-200">C++-Konstante: **SE \_ Shutdown \_ Name** String: **SeShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-200">C++ constant: **SE\_SHUTDOWN\_NAME** string: **SeShutdownPrivilege**</span></span>

<span data-ttu-id="475d8-201">Kurzname für Skripterstellung: **herunter** fahren</span><span class="sxs-lookup"><span data-stu-id="475d8-201">Scripting short name: **Shutdown**</span></span>

<span data-ttu-id="475d8-202">Erforderlich, um das lokale System herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="475d8-202">Required to shut down the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemprivilegedebug**</span><span class="sxs-lookup"><span data-stu-id="475d8-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-204">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="475d8-204">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-205">C++-Konstante: **SE \_ Debug \_ Name** String: " **sdebugprivilege** "</span><span class="sxs-lookup"><span data-stu-id="475d8-205">C++ constant: **SE\_DEBUG\_NAME** string: **SeDebugPrivilege**</span></span>

<span data-ttu-id="475d8-206">Kurzname für Skripterstellung: **Debug**</span><span class="sxs-lookup"><span data-stu-id="475d8-206">Scripting short name: **Debug**</span></span>

<span data-ttu-id="475d8-207">Erforderlich, um den Arbeitsspeicher eines Prozesses zu Debuggen und anzupassen, der im Besitz eines anderen Kontos ist</span><span class="sxs-lookup"><span data-stu-id="475d8-207">Required to debug and adjust the memory of a process owned by another account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemprivilegeaudit**</span><span class="sxs-lookup"><span data-stu-id="475d8-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-209">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="475d8-209">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-210">C++-Konstante: SE-Überwachungs **\_ \_ Name** Zeichen **Folge: "** ".</span><span class="sxs-lookup"><span data-stu-id="475d8-210">C++ constant: **SE\_AUDIT\_NAME** string: **SeAuditPrivilege**</span></span>

<span data-ttu-id="475d8-211">Kurzname für Skripterstellung: **Audit**</span><span class="sxs-lookup"><span data-stu-id="475d8-211">Scripting short name: **Audit**</span></span>

<span data-ttu-id="475d8-212">Erforderlich, um Überwachungs Einträge im NT-Sicherheitsprotokoll zu generieren.</span><span class="sxs-lookup"><span data-stu-id="475d8-212">Required to generate audit entries in the NT Security log.</span></span> <span data-ttu-id="475d8-213">Nur sichere Server sollten über dieses Privileg verfügen.</span><span class="sxs-lookup"><span data-stu-id="475d8-213">Only secure servers should have this privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemprivilegesystemenvironment**</span><span class="sxs-lookup"><span data-stu-id="475d8-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-215">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="475d8-215">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-216">C++-Konstante: namens Zeichenfolge für die **SE- \_ System Umgebung: \_ \_** **sesystemenvironment Privilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-216">C++ constant: **SE\_SYSTEM\_ENVIRONMENT\_NAME** string: **SeSystemEnvironmentPrivilege**</span></span>

<span data-ttu-id="475d8-217">Kurzname für Skripterstellung: **systemenvironment**</span><span class="sxs-lookup"><span data-stu-id="475d8-217">Scripting short name: **SystemEnvironment**</span></span>

<span data-ttu-id="475d8-218">Erforderlich, um das nicht flüchtige RAM von Systemen zu ändern, die diese Art von Arbeitsspeicher zum Speichern von Konfigurationsdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="475d8-218">Required to modify the nonvolatile RAM of systems that use this type of memory to store configuration data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemprivilegechangenotifizieren**</span><span class="sxs-lookup"><span data-stu-id="475d8-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-220">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="475d8-220">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-221">C++-Konstante: **SE- \_ Änderungs \_ \_ Name** Zeichenfolge: " **abchangenotifyprivilege** "</span><span class="sxs-lookup"><span data-stu-id="475d8-221">C++ constant: **SE\_CHANGE\_NOTIFY\_NAME** string: **SeChangeNotifyPrivilege**</span></span>

<span data-ttu-id="475d8-222">Kurzname für Skripterstellung: **changenotifizieren**</span><span class="sxs-lookup"><span data-stu-id="475d8-222">Scripting short name: **ChangeNotify**</span></span>

<span data-ttu-id="475d8-223">Ist erforderlich, um Benachrichtigungen über Änderungen an Dateien oder Verzeichnissen zu empfangen und durchgängige Zugriffs Überprüfungen zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="475d8-223">Required to receive notifications of changes to files or directories and bypass traversal access checks.</span></span> <span data-ttu-id="475d8-224">Dieses Privileg ist standardmäßig für alle Benutzer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="475d8-224">This privilege is enabled by default for all users.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemprivilegeremuteshutdown**</span><span class="sxs-lookup"><span data-stu-id="475d8-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-226">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="475d8-226">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-227">C++-Konstante: **SE \_ Remote \_ Shutdown \_ Name** String: **SeRemoteShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-227">C++ constant: **SE\_REMOTE\_SHUTDOWN\_NAME** string: **SeRemoteShutdownPrivilege**</span></span>

<span data-ttu-id="475d8-228">Kurzname für Skripterstellung: **RemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="475d8-228">Scripting short name: **RemoteShutdown**</span></span>

<span data-ttu-id="475d8-229">Zum Herunterfahren eines Remote Computers erforderlich.</span><span class="sxs-lookup"><span data-stu-id="475d8-229">Required to shut down a remote computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemprivilegeundock**</span><span class="sxs-lookup"><span data-stu-id="475d8-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-231">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="475d8-231">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-232">C++-Konstante: **SE \_ Undock- \_ namens** Zeichenfolge: " **sundockprivilege** "</span><span class="sxs-lookup"><span data-stu-id="475d8-232">C++ constant: **SE\_UNDOCK\_NAME** string: **SeUndockPrivilege**</span></span>

<span data-ttu-id="475d8-233">Skript Kurzname: **Abdocken**</span><span class="sxs-lookup"><span data-stu-id="475d8-233">Scripting short name: **Undock**</span></span>

<span data-ttu-id="475d8-234">Ist erforderlich, um einen Laptop von einer Docking Station zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="475d8-234">Required to remove a laptop from a docking station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemprivilegesyncagent**</span><span class="sxs-lookup"><span data-stu-id="475d8-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-236">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="475d8-236">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-237">C++-Konstante: Name Zeichenfolge für den **SE \_ Sync- \_ Agent \_** : **sesyncagentprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-237">C++ constant: **SE\_SYNC\_AGENT\_NAME** string: **SeSyncAgentPrivilege**</span></span>

<span data-ttu-id="475d8-238">Kurzname für Skripterstellung: **SyncAgent**</span><span class="sxs-lookup"><span data-stu-id="475d8-238">Scripting short name: **SyncAgent**</span></span>

<span data-ttu-id="475d8-239">Erforderlich zum Synchronisieren von Verzeichnisdienst Daten.</span><span class="sxs-lookup"><span data-stu-id="475d8-239">Required to synchronize directory service data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemprivilegeenabledelegation**</span><span class="sxs-lookup"><span data-stu-id="475d8-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-241">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="475d8-241">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-242">C++-Konstante: **SE \_ Aktivieren der \_ Delegierungs \_ namens** Zeichenfolge: **seenabledelegationprivilege**</span><span class="sxs-lookup"><span data-stu-id="475d8-242">C++ constant: **SE\_ENABLE\_DELEGATION\_NAME** string: **SeEnableDelegationPrivilege**</span></span>

<span data-ttu-id="475d8-243">Skript Kurzname: **enabledelegation**</span><span class="sxs-lookup"><span data-stu-id="475d8-243">Scripting short name: **EnableDelegation**</span></span>

<span data-ttu-id="475d8-244">Erforderlich, damit Computer-und Benutzerkonten für die Delegierung vertrauenswürdig sind.</span><span class="sxs-lookup"><span data-stu-id="475d8-244">Required to enable computer and user accounts to be trusted for delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="475d8-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemprivilegemanagevolume**</span><span class="sxs-lookup"><span data-stu-id="475d8-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="475d8-246">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="475d8-246">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="475d8-247">C++-Konstante: **SE \_ Manage \_ Volume \_ Name** String: " **smanagevolumeprivilege** "</span><span class="sxs-lookup"><span data-stu-id="475d8-247">C++ constant: **SE\_MANAGE\_VOLUME\_NAME** string: **SeManageVolumePrivilege**</span></span>

<span data-ttu-id="475d8-248">Skript Kurzname: **managevolume**</span><span class="sxs-lookup"><span data-stu-id="475d8-248">Scripting short name: **ManageVolume**</span></span>

<span data-ttu-id="475d8-249">Erforderlich zum Ausführen von Volumewartungsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="475d8-249">Required to perform volume maintenance tasks.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="475d8-250">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="475d8-250">Requirements</span></span>



| <span data-ttu-id="475d8-251">Anforderung</span><span class="sxs-lookup"><span data-stu-id="475d8-251">Requirement</span></span> | <span data-ttu-id="475d8-252">Wert</span><span class="sxs-lookup"><span data-stu-id="475d8-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="475d8-253">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="475d8-253">Minimum supported client</span></span><br/> | <span data-ttu-id="475d8-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="475d8-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="475d8-255">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="475d8-255">Minimum supported server</span></span><br/> | <span data-ttu-id="475d8-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="475d8-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="475d8-257">Header</span><span class="sxs-lookup"><span data-stu-id="475d8-257">Header</span></span><br/>                   | <dl> <span data-ttu-id="475d8-258"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="475d8-258"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="475d8-259">IDL</span><span class="sxs-lookup"><span data-stu-id="475d8-259">IDL</span></span><br/>                      | <dl> <span data-ttu-id="475d8-260"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="475d8-260"><dt>Wbemdisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="475d8-261">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="475d8-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="475d8-262">Skript-API-Konstanten</span><span class="sxs-lookup"><span data-stu-id="475d8-262">Scripting API Constants</span></span>](scripting-api-constants.md)
</dt> <dt>

[<span data-ttu-id="475d8-263">**Austausch Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="475d8-263">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="475d8-264">**Wbemprivilegeumum**</span><span class="sxs-lookup"><span data-stu-id="475d8-264">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="475d8-265">Ausführen privilegierter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="475d8-265">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="475d8-266">Ausführen privilegierter Vorgänge mit VBScript</span><span class="sxs-lookup"><span data-stu-id="475d8-266">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

