---
description: Um die Sicherheit des Host Prozesses (wmiprvse.exe) des freigegebenen Anbieters des Windows-Verwaltungsinstrumentation (WMI) zu verbessern, wurden Änderungen an Windows-Plattformen vorgenommen, mit denen der Anbieter Host Prozess mit einer Dienst Sicherheits-ID (SID) gesichert wird.
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Registrierungsschlüssel und-Werte zum Steuern der Anbieter Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c7dd990c1a9ebbc1242af5ce4601ce6eb22a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350934"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a><span data-ttu-id="96dd8-103">Registrierungsschlüssel und-Werte zum Steuern der Anbieter Sicherheit</span><span class="sxs-lookup"><span data-stu-id="96dd8-103">Registry Keys and Values for Controlling Provider Security</span></span>

<span data-ttu-id="96dd8-104">Um die Sicherheit des Host Prozesses (wmiprvse.exe) des freigegebenen Anbieters des Windows-Verwaltungsinstrumentation (WMI) zu verbessern, wurden Änderungen an Windows-Plattformen vorgenommen, mit denen der Anbieter Host Prozess mit einer [*Dienst Sicherheits-ID (SID)*](gloss-s.md)gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="96dd8-104">To enhance the security of the Windows Management Instrumentation (WMI) shared provider host process (wmiprvse.exe), changes were made to Windows platforms that secure the provider host process with a [*service security identifier (SID)*](gloss-s.md).</span></span> <span data-ttu-id="96dd8-105">Durch diese Änderungen werden die folgenden Betriebsmodi für den freigegebenen WMI-Host eingeführt: sicher und kompatibel.</span><span class="sxs-lookup"><span data-stu-id="96dd8-105">These changes introduce the following running modes for the WMI shared host: secure and compatible.</span></span>

<span data-ttu-id="96dd8-106">Die folgenden Abschnitte werden in diesem Thema behandelt:</span><span class="sxs-lookup"><span data-stu-id="96dd8-106">The following sections are covered in this topic:</span></span>

-   [<span data-ttu-id="96dd8-107">Sicherer und kompatibler Modus</span><span class="sxs-lookup"><span data-stu-id="96dd8-107">Secure and Compatible Modes</span></span>](#secure-and-compatible-modes)
-   [<span data-ttu-id="96dd8-108">Registrierungsschlüssel und-Werte</span><span class="sxs-lookup"><span data-stu-id="96dd8-108">Registry Keys and Values</span></span>](#registry-keys-and-values)
-   [<span data-ttu-id="96dd8-109">Konfigurieren eines Anbieters für die Durchführung im sicheren oder kompatiblen Modus</span><span class="sxs-lookup"><span data-stu-id="96dd8-109">Configuring a Provider to Run in Secure or Compatible Mode</span></span>](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a><span data-ttu-id="96dd8-110">Sicherer und kompatibler Modus</span><span class="sxs-lookup"><span data-stu-id="96dd8-110">Secure and Compatible Modes</span></span>

<span data-ttu-id="96dd8-111">Ab Windows 7 wurden die folgenden zwei laufenden Modi für den freigegebenen WMI-Host Prozess hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="96dd8-111">Starting in Windows 7, the following two running modes for the WMI shared host process were added:</span></span>

<dl> <dt>

<span data-ttu-id="96dd8-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Sicherer Modus</span><span class="sxs-lookup"><span data-stu-id="96dd8-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Secure mode</span></span>
</dt> <dd>

<span data-ttu-id="96dd8-113">Die Prozess Ressourcen des WMI-Anbieter Hosts sind mit einer [*Dienst-SID*](gloss-s.md)gesichert.</span><span class="sxs-lookup"><span data-stu-id="96dd8-113">WMI provider host process resources are secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="96dd8-114">Nur die *Dienst-SID* verfügt über Berechtigungen für diese Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="96dd8-114">Only the *service SID* has permissions for these resources.</span></span>

</dd> <dt>

<span data-ttu-id="96dd8-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Kompatibler Modus</span><span class="sxs-lookup"><span data-stu-id="96dd8-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Compatible mode</span></span>
</dt> <dd>

<span data-ttu-id="96dd8-116">Der Host Prozess für den freigegebenen WMI-Anbieter ist nicht mit einer [*Dienst-SID*](gloss-s.md)gesichert.</span><span class="sxs-lookup"><span data-stu-id="96dd8-116">The WMI shared provider host process is not secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="96dd8-117">Der Anbieter Host Prozess ermöglicht den Zugriff auf die Konten Network Service oder LocalService, abhängig vom Hostingmodell.</span><span class="sxs-lookup"><span data-stu-id="96dd8-117">The provider host process allows access to the NetworkService or LocalService accounts depending on the hosting model.</span></span> <span data-ttu-id="96dd8-118">Weitere Informationen zum Hosting von Modellen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="96dd8-118">For more information about hosting models, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

<span data-ttu-id="96dd8-119">**Windows Vista und Windows Server 2008:** Um auf die Registrierungsschlüssel und-Werte zum Steuern des sicheren und kompatiblen Modus für den Anbieter Host Prozess zuzugreifen, müssen Sie das Sicherheitsupdate in [KB 959454](https://support.microsoft.com/kb/959454)installieren.</span><span class="sxs-lookup"><span data-stu-id="96dd8-119">**Windows Vista and Windows Server 2008:** To access the registry keys and values for controlling secure and compatible modes for the provider host process, you must install the security update in [KB 959454](https://support.microsoft.com/kb/959454).</span></span> <span data-ttu-id="96dd8-120">Weitere Informationen finden Sie im [Microsoft-Sicherheits Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span><span class="sxs-lookup"><span data-stu-id="96dd8-120">For more information, see the [Microsoft Security Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span></span>

## <a name="registry-keys-and-values"></a><span data-ttu-id="96dd8-121">Registrierungsschlüssel und-Werte</span><span class="sxs-lookup"><span data-stu-id="96dd8-121">Registry Keys and Values</span></span>

<span data-ttu-id="96dd8-122">Die Einstellungen für den sicheren und kompatiblen Modus werden über Registrierungsschlüssel angegeben.</span><span class="sxs-lookup"><span data-stu-id="96dd8-122">The secure and compatible mode settings are specified through registry keys.</span></span> <span data-ttu-id="96dd8-123">Die Registrierungsschlüssel für WMI befinden sich in der Registrierung unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="96dd8-123">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<span data-ttu-id="96dd8-124">Die folgenden Registrierungsschlüssel und **DWORD** -Werte, die in der folgenden Liste beschrieben werden, wurden hinzugefügt, um das Verhalten von WMI-Anbietern zu steuern.</span><span class="sxs-lookup"><span data-stu-id="96dd8-124">The following registry keys and **DWORD** value described in the following list were added to control the behavior of WMI providers.</span></span>

<dl> <dt>

<span data-ttu-id="96dd8-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**Securedhostproviders**</span><span class="sxs-lookup"><span data-stu-id="96dd8-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="96dd8-126">Dieser Schlüssel steuert das Verhalten einzelner Anbieter.</span><span class="sxs-lookup"><span data-stu-id="96dd8-126">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="96dd8-127">Alle Anbieter, die in diesem Schlüssel aufgelistet sind, werden immer im sicheren Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-127">All of the providers that are listed in this key always run in secure mode.</span></span> <span data-ttu-id="96dd8-128">Alle Eingangsbox Anbieter, die mit Windows ausgeliefert werden, sind unter diesem Schlüssel aufgeführt und werden standardmäßig im sicheren Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-128">All inbox providers that are shipped with Windows are listed under this key, and are run in secure mode by default.</span></span>

<span data-ttu-id="96dd8-129">Dieser Schlüssel hat Vorrang vor Anbietern, die im Schlüssel **compatiblehostproviders** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="96dd8-129">This key takes precedence over providers listed in the **CompatibleHostProviders** key.</span></span>

</dd> <dt>

<span data-ttu-id="96dd8-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**Compatiblehostproviders**</span><span class="sxs-lookup"><span data-stu-id="96dd8-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="96dd8-131">Dieser Schlüssel steuert das Verhalten einzelner Anbieter.</span><span class="sxs-lookup"><span data-stu-id="96dd8-131">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="96dd8-132">Alle Anbieter, die in diesem Schlüssel aufgelistet sind, werden immer im kompatiblen Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-132">All providers that are listed in this key always run in compatible mode.</span></span> <span data-ttu-id="96dd8-133">Dieser Schlüssel ist standardmäßig leer.</span><span class="sxs-lookup"><span data-stu-id="96dd8-133">This key is empty by default.</span></span>

<span data-ttu-id="96dd8-134">Wenn ein Anbieter im Schlüssel **securedhostproviders** und im Schlüssel **compatiblehostproviders** aufgeführt ist, wird der Anbieter im sicheren Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-134">If a provider is listed both in the **SecuredHostProviders** key and in the **CompatibleHostProviders** key, the provider is run in secure mode.</span></span>

> [!Note]  
> <span data-ttu-id="96dd8-135">Der Schlüssel **compatiblehostproviders** bietet Anwendungs Kompatibilität für Anwendungen von Drittanbietern, wenn der **DefaultSecuredHost** -Schlüssel auf 1 festgelegt ist und der Anbieter bekanntermaßen nicht im sicheren Modus funktioniert.</span><span class="sxs-lookup"><span data-stu-id="96dd8-135">The **CompatibleHostProviders** key provides application compatibility for third-party applications if the **DefaultSecuredHost** key is set to 1 and the provider is known to not function in secure mode.</span></span>

 

</dd> <dt>

<span data-ttu-id="96dd8-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span><span class="sxs-lookup"><span data-stu-id="96dd8-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span></span>
</dt> <dd>

<span data-ttu-id="96dd8-137">Ein globaler **DWORD** -Registrierungs Wert, der bestimmt, ob alle Anbieter, die nicht in den Schlüsseln **securedhostproviders** oder **compatiblehostproviders** aufgeführt sind, im sicheren oder kompatiblen Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="96dd8-137">A global registry **DWORD** value that determines whether all of the providers, which are not listed in the **SecuredHostProviders** or **CompatibleHostProviders** keys, are run in the secure or compatible mode.</span></span> <span data-ttu-id="96dd8-138">Dieser **DWORD** -Wert ermöglicht dem Administrator, den Modus zu entscheiden, der von einem Drittanbieter ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="96dd8-138">This **DWORD** value lets the administrator decide under which mode a third-party provider must run.</span></span> <span data-ttu-id="96dd8-139">Standardmäßig ist dieser Wert auf 0 (null) festgelegt, und alle Drittanbieter Anbieter werden im kompatiblen Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-139">By default, this value is set to zero and all third-party providers are run in compatible mode.</span></span> <span data-ttu-id="96dd8-140">Administratoren können Ihren Computer standardmäßig sicherer machen, indem Sie den **DefaultSecuredHost** -Wert auf "1" festlegen.</span><span class="sxs-lookup"><span data-stu-id="96dd8-140">Administrators can make their computer more secure by default by setting the **DefaultSecuredHost** value to 1.</span></span>

> [!Note]  
> <span data-ttu-id="96dd8-141">Der **DefaultSecuredHost** -Wert hat keine Auswirkung auf die anderen Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="96dd8-141">The **DefaultSecuredHost** value does not affect the other registry keys.</span></span> <span data-ttu-id="96dd8-142">Die im **securedhostproviders** -Schlüssel aufgelisteten Anbieter bleiben im sicheren Modus, und die im **Kompatibilitäts Hostproviders** -Schlüssel aufgeführten Anbieter bleiben im kompatiblen Modus.</span><span class="sxs-lookup"><span data-stu-id="96dd8-142">The providers that are listed in the **SecuredHostProviders** key remain in secure mode, and the ones that are listed in the **CompatibleHostProviders** key remain in compatible mode.</span></span>

 

<span data-ttu-id="96dd8-143">Folgende Einstellungen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="96dd8-143">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="96dd8-144"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="96dd8-144"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="96dd8-145">Gibt an, dass Anbieter im kompatiblen Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="96dd8-145">Specifies that providers run in compatible mode.</span></span>

</dd> <dt>

<span data-ttu-id="96dd8-146"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="96dd8-146"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="96dd8-147">Gibt an, dass Anbieter im sicheren Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="96dd8-147">Specifies that providers run in secure mode.</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="96dd8-148">In der folgenden Liste sind die möglichen Registrierungs Einstellungen und die zugehörigen laufenden Modi für einen Anbieter aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="96dd8-148">The following list lists the possible registry settings and the associated running modes for a provider.</span></span>



| <span data-ttu-id="96dd8-149">Unter securedhostproviders aufgeführt</span><span class="sxs-lookup"><span data-stu-id="96dd8-149">Listed under SecuredHostProviders</span></span> | <span data-ttu-id="96dd8-150">Unter compatiblehostproviders aufgeführt</span><span class="sxs-lookup"><span data-stu-id="96dd8-150">Listed under CompatibleHostProviders</span></span> | <span data-ttu-id="96dd8-151">DefaultSecuredHost-Einstellung</span><span class="sxs-lookup"><span data-stu-id="96dd8-151">DefaultSecuredHost Setting</span></span> | <span data-ttu-id="96dd8-152">Mode</span><span class="sxs-lookup"><span data-stu-id="96dd8-152">Mode</span></span>       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| <span data-ttu-id="96dd8-153">Nein</span><span class="sxs-lookup"><span data-stu-id="96dd8-153">No</span></span>                                | <span data-ttu-id="96dd8-154">Nein</span><span class="sxs-lookup"><span data-stu-id="96dd8-154">No</span></span>                                   | <span data-ttu-id="96dd8-155">0</span><span class="sxs-lookup"><span data-stu-id="96dd8-155">0</span></span>                          | <span data-ttu-id="96dd8-156">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="96dd8-156">Compatible</span></span> |
| <span data-ttu-id="96dd8-157">Nein</span><span class="sxs-lookup"><span data-stu-id="96dd8-157">No</span></span>                                | <span data-ttu-id="96dd8-158">Ja</span><span class="sxs-lookup"><span data-stu-id="96dd8-158">Yes</span></span>                                  | <span data-ttu-id="96dd8-159">0</span><span class="sxs-lookup"><span data-stu-id="96dd8-159">0</span></span>                          | <span data-ttu-id="96dd8-160">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="96dd8-160">Compatible</span></span> |
| <span data-ttu-id="96dd8-161">Ja</span><span class="sxs-lookup"><span data-stu-id="96dd8-161">Yes</span></span>                               | <span data-ttu-id="96dd8-162">Nein</span><span class="sxs-lookup"><span data-stu-id="96dd8-162">No</span></span>                                   | <span data-ttu-id="96dd8-163">0</span><span class="sxs-lookup"><span data-stu-id="96dd8-163">0</span></span>                          | <span data-ttu-id="96dd8-164">Sicher</span><span class="sxs-lookup"><span data-stu-id="96dd8-164">Secure</span></span>     |
| <span data-ttu-id="96dd8-165">Ja</span><span class="sxs-lookup"><span data-stu-id="96dd8-165">Yes</span></span>                               | <span data-ttu-id="96dd8-166">Ja</span><span class="sxs-lookup"><span data-stu-id="96dd8-166">Yes</span></span>                                  | <span data-ttu-id="96dd8-167">0</span><span class="sxs-lookup"><span data-stu-id="96dd8-167">0</span></span>                          | <span data-ttu-id="96dd8-168">Sicher</span><span class="sxs-lookup"><span data-stu-id="96dd8-168">Secure</span></span>     |
| <span data-ttu-id="96dd8-169">Nein</span><span class="sxs-lookup"><span data-stu-id="96dd8-169">No</span></span>                                | <span data-ttu-id="96dd8-170">Nein</span><span class="sxs-lookup"><span data-stu-id="96dd8-170">No</span></span>                                   | <span data-ttu-id="96dd8-171">1</span><span class="sxs-lookup"><span data-stu-id="96dd8-171">1</span></span>                          | <span data-ttu-id="96dd8-172">Sicher</span><span class="sxs-lookup"><span data-stu-id="96dd8-172">Secure</span></span>     |
| <span data-ttu-id="96dd8-173">Nein</span><span class="sxs-lookup"><span data-stu-id="96dd8-173">No</span></span>                                | <span data-ttu-id="96dd8-174">Ja</span><span class="sxs-lookup"><span data-stu-id="96dd8-174">Yes</span></span>                                  | <span data-ttu-id="96dd8-175">1</span><span class="sxs-lookup"><span data-stu-id="96dd8-175">1</span></span>                          | <span data-ttu-id="96dd8-176">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="96dd8-176">Compatible</span></span> |
| <span data-ttu-id="96dd8-177">Ja</span><span class="sxs-lookup"><span data-stu-id="96dd8-177">Yes</span></span>                               | <span data-ttu-id="96dd8-178">Nein</span><span class="sxs-lookup"><span data-stu-id="96dd8-178">No</span></span>                                   | <span data-ttu-id="96dd8-179">1</span><span class="sxs-lookup"><span data-stu-id="96dd8-179">1</span></span>                          | <span data-ttu-id="96dd8-180">Sicher</span><span class="sxs-lookup"><span data-stu-id="96dd8-180">Secure</span></span>     |
| <span data-ttu-id="96dd8-181">Ja</span><span class="sxs-lookup"><span data-stu-id="96dd8-181">Yes</span></span>                               | <span data-ttu-id="96dd8-182">Ja</span><span class="sxs-lookup"><span data-stu-id="96dd8-182">Yes</span></span>                                  | <span data-ttu-id="96dd8-183">1</span><span class="sxs-lookup"><span data-stu-id="96dd8-183">1</span></span>                          | <span data-ttu-id="96dd8-184">Sicher</span><span class="sxs-lookup"><span data-stu-id="96dd8-184">Secure</span></span>     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a><span data-ttu-id="96dd8-185">Konfigurieren eines Anbieters für die Durchführung im sicheren oder kompatiblen Modus</span><span class="sxs-lookup"><span data-stu-id="96dd8-185">Configuring a Provider to Run in Secure or Compatible Mode</span></span>

<span data-ttu-id="96dd8-186">Die Registrierungsschlüssel können mithilfe der Gruppenrichtlinien-Verwaltungskonsole (GPMC) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="96dd8-186">The registry keys can be modified using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="96dd8-187">Weitere Informationen finden Sie unter [Gruppenrichtlinien-Verwaltungskonsole](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="96dd8-187">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="96dd8-188">Die folgenden Verfahren veranschaulichen, wie Sie Einstellungen für den sicheren und kompatiblen Modus mithilfe von Gruppenrichtlinien Einstellungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="96dd8-188">The following procedures illustrate how to manage secure and compatible mode settings by using group policy preferences.</span></span> <span data-ttu-id="96dd8-189">Weitere Informationen zu Gruppenrichtlinien Einstellungen finden Sie in der [Übersicht über Gruppenrichtlinie Einstellungen](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="96dd8-189">For more information about group policy preferences, see the [Group Policy Preferences Overview](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span></span>

<span data-ttu-id="96dd8-190">**So fügen Sie dem sicheren oder kompatiblen Modus einen Anbieter mithilfe von Gruppenrichtlinie hinzu**</span><span class="sxs-lookup"><span data-stu-id="96dd8-190">**To add a provider to either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="96dd8-191">Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="96dd8-191">Open the GPMC.</span></span>
2.  <span data-ttu-id="96dd8-192">Erstellen Sie ein Gruppenrichtlinie Objekt (GPO).</span><span class="sxs-lookup"><span data-stu-id="96dd8-192">Create a Group Policy Object (GPO).</span></span>
3.  <span data-ttu-id="96dd8-193">Bearbeiten Sie das Gruppenrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-193">Edit the GPO.</span></span>
4.  <span data-ttu-id="96dd8-194">Navigieren Sie zu Einstellungen/Windows-Einstellungen/Registrierung.</span><span class="sxs-lookup"><span data-stu-id="96dd8-194">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="96dd8-195">Klicken Sie mit der rechten Maustaste, und wählen Sie **neu... Registrierung**.</span><span class="sxs-lookup"><span data-stu-id="96dd8-195">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="96dd8-196">Diese Aktion stellt eine Benutzeroberfläche dar, auf der Sie Registrierungsinformationen eingeben können.</span><span class="sxs-lookup"><span data-stu-id="96dd8-196">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="96dd8-197">Wählen Sie den Befehl **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="96dd8-197">Select the **Create** command.</span></span>
7.  <span data-ttu-id="96dd8-198">Wählen Sie den folgenden Registrierungsschlüssel Pfad aus:</span><span class="sxs-lookup"><span data-stu-id="96dd8-198">Select the following registry key path:</span></span>

    <span data-ttu-id="96dd8-199">**Sicherer Modus: HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **securedhostproviders**</span><span class="sxs-lookup"><span data-stu-id="96dd8-199">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="96dd8-200">**Kompatibler Modus: HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **compatiblehostproviders**</span><span class="sxs-lookup"><span data-stu-id="96dd8-200">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="96dd8-201">Geben Sie im Feld **Name** den Namen des Anbieters ein, den Sie diesem Schlüssel hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="96dd8-201">In the **name** field, enter the name of the provider you want to add to this key.</span></span> <span data-ttu-id="96dd8-202">Der Anbieter Name muss das folgende Format aufweisen: <namespace> : <\_ \_ RelPath>.</span><span class="sxs-lookup"><span data-stu-id="96dd8-202">The provider name must be in the following format: <namespace>:<\_\_RELPATH>.</span></span> <span data-ttu-id="96dd8-203">Beispiel \\ : root cimv2: \_ \_ win32provider. Name = "MyProvider".</span><span class="sxs-lookup"><span data-stu-id="96dd8-203">For example, root\\cimv2:\_\_win32provider.name="MyProvider".</span></span>
9.  <span data-ttu-id="96dd8-204">Geben Sie im Feld **Daten** den Wert 0 ein.</span><span class="sxs-lookup"><span data-stu-id="96dd8-204">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="96dd8-205">Klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="96dd8-205">Click OK.</span></span>

<span data-ttu-id="96dd8-206">**So entfernen Sie einen Anbieter aus dem sicheren oder kompatiblen Modus mithilfe von Gruppenrichtlinie**</span><span class="sxs-lookup"><span data-stu-id="96dd8-206">**To remove a provider from either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="96dd8-207">Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="96dd8-207">Open the GPMC.</span></span>
2.  <span data-ttu-id="96dd8-208">Erstellen Sie ein Gruppenrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-208">Create a GPO.</span></span>
3.  <span data-ttu-id="96dd8-209">Bearbeiten Sie das Gruppenrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-209">Edit the GPO.</span></span>
4.  <span data-ttu-id="96dd8-210">Navigieren Sie zu Einstellungen/Windows-Einstellungen/Registrierung.</span><span class="sxs-lookup"><span data-stu-id="96dd8-210">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="96dd8-211">Klicken Sie mit der rechten Maustaste, und wählen Sie **neu... Registrierung**.</span><span class="sxs-lookup"><span data-stu-id="96dd8-211">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="96dd8-212">Diese Aktion stellt eine Benutzeroberfläche dar, auf der Sie Registrierungsinformationen eingeben können.</span><span class="sxs-lookup"><span data-stu-id="96dd8-212">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="96dd8-213">Wählen Sie den Befehl **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="96dd8-213">Select the **Remove** command.</span></span>
7.  <span data-ttu-id="96dd8-214">Wählen Sie den folgenden Registrierungsschlüssel Pfad aus:</span><span class="sxs-lookup"><span data-stu-id="96dd8-214">Select the following registry key path:</span></span>

    <span data-ttu-id="96dd8-215">**Sicherer Modus: HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **securedhostproviders**</span><span class="sxs-lookup"><span data-stu-id="96dd8-215">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="96dd8-216">**Kompatibler Modus: HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **compatiblehostproviders**</span><span class="sxs-lookup"><span data-stu-id="96dd8-216">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="96dd8-217">Geben Sie im Feld **Name** den Namen des Anbieters ein, den Sie aus diesem Schlüssel entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="96dd8-217">In the **name** field, enter the name of the provider you want to remove from this key.</span></span>
9.  <span data-ttu-id="96dd8-218">Geben Sie im Feld **Daten** den Wert 0 ein.</span><span class="sxs-lookup"><span data-stu-id="96dd8-218">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="96dd8-219">Klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="96dd8-219">Click OK.</span></span>

<span data-ttu-id="96dd8-220">Das folgende Verfahren enthält Details zum Ändern des Verhaltens von Anbietern, die nicht in den Schlüsseln **securedhostproviders** oder **compatiblehostproviders** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="96dd8-220">The following procedure provides details about how to modify the behavior of providers that are not listed in either the **SecuredHostProviders** or **CompatibleHostProviders** keys.</span></span>

<span data-ttu-id="96dd8-221">**So ändern Sie den Standardwert des Schlüssels DefaultSecuredHost mithilfe von Gruppenrichtlinie**</span><span class="sxs-lookup"><span data-stu-id="96dd8-221">**To change the default value of the DefaultSecuredHost key by using Group Policy**</span></span>

1.  <span data-ttu-id="96dd8-222">Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="96dd8-222">Open the GPMC.</span></span>
2.  <span data-ttu-id="96dd8-223">Erstellen Sie ein Gruppenrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-223">Create a GPO.</span></span>
3.  <span data-ttu-id="96dd8-224">Bearbeiten Sie das Gruppenrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="96dd8-224">Edit the GPO.</span></span>
4.  <span data-ttu-id="96dd8-225">Navigieren Sie zu Einstellungen/Windows-Einstellungen/Registrierung.</span><span class="sxs-lookup"><span data-stu-id="96dd8-225">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="96dd8-226">Klicken Sie mit der rechten Maustaste, und wählen Sie **neu... Registrierung**.</span><span class="sxs-lookup"><span data-stu-id="96dd8-226">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="96dd8-227">Diese Aktion stellt eine Benutzeroberfläche dar, auf der Sie Registrierungsinformationen eingeben können.</span><span class="sxs-lookup"><span data-stu-id="96dd8-227">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="96dd8-228">Wählen Sie den Befehl **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="96dd8-228">Select the **Update** command.</span></span>
7.  <span data-ttu-id="96dd8-229">Wählen Sie den folgenden Registrierungsschlüssel Pfad aus: **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="96dd8-229">Select the following registry key path: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**.</span></span>
8.  <span data-ttu-id="96dd8-230">Geben Sie im Feld **Name den Namen** **DefaultSecuredHost** ein.</span><span class="sxs-lookup"><span data-stu-id="96dd8-230">In the **name** field, enter **DefaultSecuredHost**.</span></span>
9.  <span data-ttu-id="96dd8-231">Geben Sie im Feld **Daten** den Wert 0 für den kompatiblen Modus oder 1 für den sicheren Modus ein.</span><span class="sxs-lookup"><span data-stu-id="96dd8-231">In the **data** field, enter 0 for compatible mode or 1 for secure mode.</span></span>
10. <span data-ttu-id="96dd8-232">Klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="96dd8-232">Click OK.</span></span>

 

 
