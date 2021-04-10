---
description: WMI verwendet einen standardmäßigen Windows-Sicherheits Deskriptor, um den Zugriff auf WMI-Namespaces zu steuern.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Zugriff auf WMI-Namespaces
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960621"
---
# <a name="access-to-wmi-namespaces"></a><span data-ttu-id="30514-103">Zugriff auf WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="30514-103">Access to WMI Namespaces</span></span>

<span data-ttu-id="30514-104">WMI verwendet einen standardmäßigen Windows- *Sicherheits Deskriptor* , um den Zugriff auf WMI-Namespaces zu steuern.</span><span class="sxs-lookup"><span data-stu-id="30514-104">WMI uses a standard Windows *security descriptor* to control access to WMI namespaces.</span></span> <span data-ttu-id="30514-105">Wenn Sie eine Verbindung mit WMI herstellen, indem Sie entweder den WMI-Moniker "winmgmts" oder einen Aufruf an " [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) " oder " [**Swap. ConnectServer**](swbemlocator-connectserver.md)" aufrufen, stellen Sie eine Verbindung mit einem bestimmten Namespace her.</span><span class="sxs-lookup"><span data-stu-id="30514-105">When you connect to WMI, either through the WMI "winmgmts" moniker or a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) or [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), you connect to a specific namespace.</span></span>

<span data-ttu-id="30514-106">Die folgenden Informationen werden in diesem Thema behandelt:</span><span class="sxs-lookup"><span data-stu-id="30514-106">The following information is discussed in this topic:</span></span>

-   [<span data-ttu-id="30514-107">WMI-Namespace Sicherheit</span><span class="sxs-lookup"><span data-stu-id="30514-107">WMI Namespace Security</span></span>](#wmi-namespace-security)
-   [<span data-ttu-id="30514-108">WMI-Namespace Überwachung</span><span class="sxs-lookup"><span data-stu-id="30514-108">WMI Namespace Auditing</span></span>](#wmi-namespace-auditing)
-   [<span data-ttu-id="30514-109">Typen von Namespace Ereignissen</span><span class="sxs-lookup"><span data-stu-id="30514-109">Types of Namespace Events</span></span>](#types-of-namespace-events)
-   [<span data-ttu-id="30514-110">Namespace-Zugriffs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="30514-110">Namespace Access Settings</span></span>](#namespace-access-settings)
-   [<span data-ttu-id="30514-111">Standard Berechtigungen für WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="30514-111">Default Permissions on WMI Namespaces</span></span>](#default-permissions-on-wmi-namespaces)
-   [<span data-ttu-id="30514-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30514-112">Related topics</span></span>](#related-topics)

## <a name="wmi-namespace-security"></a><span data-ttu-id="30514-113">WMI-Namespace Sicherheit</span><span class="sxs-lookup"><span data-stu-id="30514-113">WMI Namespace Security</span></span>

<span data-ttu-id="30514-114">WMI verwaltet die Namespace Sicherheit, indem das [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des Benutzers, der eine Verbindung mit dem-Namespace herstellt, mit der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) des-Namespace verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="30514-114">WMI maintains namespace security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user connecting to the namespace with the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the namespace.</span></span> <span data-ttu-id="30514-115">Weitere Informationen zur Windows-Sicherheit finden [Sie unter Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="30514-115">For more information about Windows security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="30514-116">Beachten Sie, dass sich die [Benutzerkontensteuerung (User Account Control, UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) ab Windows Vista auf den Zugriff auf WMI-Daten auswirkt und was mit dem [*WMI-Steuer*](gloss-w.md)Element konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="30514-116">Be aware that, starting with Windows Vista, [User Account Control (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="30514-117">Weitere Informationen finden Sie unter [Standard Berechtigungen für WMI-Namespaces](#default-permissions-on-wmi-namespaces) und [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="30514-117">For more information, see [Default Permissions on WMI Namespaces](#default-permissions-on-wmi-namespaces) and [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="30514-118">Der Zugriff auf WMI-Namespaces wird ebenfalls beeinträchtigt, wenn die Verbindung von einem Remote Computer aus erfolgt.</span><span class="sxs-lookup"><span data-stu-id="30514-118">Access to WMI namespaces is also affected when the connection is from a remote computer.</span></span> <span data-ttu-id="30514-119">Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md), [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md)und Herstellen einer [Verbindung über die Windows-Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="30514-119">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md), [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md), and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span>

<span data-ttu-id="30514-120">Anbieter müssen sich auf die Identitätswechsel Einstellung für die Verbindung verlassen, um zu bestimmen, ob das Client Skript oder die Anwendung Daten empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="30514-120">Providers must rely on the impersonation setting for the connection to determine if the client script or application should receive data.</span></span> <span data-ttu-id="30514-121">Weitere Informationen zu Skript-und Client Anwendungen finden Sie unter [Festlegen der Prozesssicherheit für Client](setting-client-application-process-security.md)Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="30514-121">For more information about script and client applications, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="30514-122">Weitere Informationen zum Identitätswechsel des [*Anbieters*](gloss-p.md) finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="30514-122">For more information about [*provider*](gloss-p.md) impersonation, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

## <a name="wmi-namespace-auditing"></a><span data-ttu-id="30514-123">WMI-Namespace Überwachung</span><span class="sxs-lookup"><span data-stu-id="30514-123">WMI Namespace Auditing</span></span>

<span data-ttu-id="30514-124">WMI verwendet zum Überwachen der Namespace Aktivität die-Namespace [*System-Zugriffs Steuerungs Listen (SACL)*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="30514-124">WMI uses the namespace [*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) to audit namespace activity.</span></span> <span data-ttu-id="30514-125">Um die Überwachung von WMI-Namespaces zu aktivieren, verwenden Sie die Registerkarte **Sicherheit** des [*WMI-Steuer*](gloss-w.md) Elements, um die Überwachungs Einstellungen für den-Namespace zu ändern.</span><span class="sxs-lookup"><span data-stu-id="30514-125">To enable auditing of WMI namespaces, use the **Security** tab on the [*WMI Control*](gloss-w.md) to change the auditing settings for the namespace.</span></span>

<span data-ttu-id="30514-126">Die Überwachung wird während der Installation des Betriebssystems nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="30514-126">Auditing is not enabled during the installation of the operating system.</span></span> <span data-ttu-id="30514-127">Um die Überwachung zu aktivieren, klicken Sie im Fenster Standard **Sicherheit** auf **die Registerkarte** Überwachung.</span><span class="sxs-lookup"><span data-stu-id="30514-127">To enable auditing, click the **Auditing** tab in the standard **Security** window.</span></span> <span data-ttu-id="30514-128">Anschließend können Sie einen Überwachungs Eintrag hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="30514-128">Then you can add an auditing entry.</span></span>

<span data-ttu-id="30514-129">Gruppenrichtlinie für den lokalen Computer muss so festgelegt werden, dass die Überwachung zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="30514-129">Group Policy for the local computer must be set to allow auditing.</span></span> <span data-ttu-id="30514-130">Sie können die Überwachung aktivieren, indem Sie das MMC-Snap-in "gpeer dit. msc" und " **Objektzugriff** überwachen" unter **Computer Konfiguration**  >  **Windows-Einstellungen**  >  **Sicherheitseinstellungen**  >  **lokale Richtlinien** Überwachungs  >  **Richtlinie** festlegen.</span><span class="sxs-lookup"><span data-stu-id="30514-130">You can enable auditing by running the Gpedit.msc MMC snap-in and setting **Audit Object Access** under **Computer Configuration** > **Windows Settings** > **Security Settings** > **Local Policies** > **Audit Policy**.</span></span>

<span data-ttu-id="30514-131">Ein Überwachungs Eintrag bearbeitet die SACL des Namespace.</span><span class="sxs-lookup"><span data-stu-id="30514-131">An auditing entry edits the SACL of the namespace.</span></span> <span data-ttu-id="30514-132">Wenn Sie einen Überwachungs Eintrag hinzufügen, handelt es sich entweder um einen Benutzer, eine Gruppe, einen Computer oder einen integrierten Sicherheits Prinzipal.</span><span class="sxs-lookup"><span data-stu-id="30514-132">When you add an auditing entry, it is either a user, group, computer, or built-in security principal.</span></span> <span data-ttu-id="30514-133">Nachdem Sie den Eintrag hinzugefügt haben, können Sie die Zugriffs Vorgänge festlegen, die zu Sicherheitsprotokoll Ereignissen führen.</span><span class="sxs-lookup"><span data-stu-id="30514-133">After adding the entry, you can set the access operations that result in Security Log events.</span></span> <span data-ttu-id="30514-134">Beispielsweise können Sie für die Gruppe Authentifizierte Benutzer auf Methoden ausführen klicken.</span><span class="sxs-lookup"><span data-stu-id="30514-134">For example, for the group Authenticated Users, you can click Execute Methods.</span></span> <span data-ttu-id="30514-135">Diese Einstellung führt zu Sicherheitsprotokoll Ereignissen, wenn ein Mitglied der Gruppe "authentifizierte Benutzer" eine Methode in diesem Namespace ausführt.</span><span class="sxs-lookup"><span data-stu-id="30514-135">This setting results in Security Log events whenever a member of the Authenticated Users group executes a method in that namespace.</span></span> <span data-ttu-id="30514-136">Die Ereignis-ID für WMI-Ereignisse lautet 4662.</span><span class="sxs-lookup"><span data-stu-id="30514-136">The Event ID for WMI events is 4662.</span></span>

<span data-ttu-id="30514-137">Ihr Konto muss sich in der Gruppe "Administratoren" befinden und mit erhöhten Rechten ausgeführt werden, um die Überwachungs Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="30514-137">Your account must be in the Administrators group and running under elevated privilege to change the auditing settings.</span></span> <span data-ttu-id="30514-138">Das integrierte Administrator Konto kann auch die Sicherheit oder die Überwachung für einen Namespace ändern.</span><span class="sxs-lookup"><span data-stu-id="30514-138">The built-in Administrator account can also change the security or auditing for a namespace.</span></span> <span data-ttu-id="30514-139">Weitere Informationen zur Ausführung im erweiterten Modus finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="30514-139">For more information about running in elevated mode, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="30514-140">Die WMI-Überwachung generiert Erfolgs-oder Fehlerereignisse für Zugriffsversuche auf WMI-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="30514-140">WMI auditing generates success or failure events for attempts to access WMI namespaces.</span></span> <span data-ttu-id="30514-141">Der Dienst überwacht nicht den Erfolg oder das Fehlschlagen von Anbieter Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="30514-141">The service does not audit the success or failure of provider operations.</span></span> <span data-ttu-id="30514-142">Wenn ein Skript z. b. eine Verbindung mit WMI und einem Namespace herstellt, kann dies fehlschlagen, weil das Konto, unter dem das Skript ausgeführt wird, keinen Zugriff auf den Namespace hat oder einen Vorgang, z. b. das Bearbeiten der DACL, nicht gestattet, das nicht erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="30514-142">For example, when a script connects to WMI and a namespace, it may fail because the account under which the script is running does not have access to that the namespace or may attempt an operation, such as editing the DACL, that is not granted.</span></span>

<span data-ttu-id="30514-143">Wenn Sie unter einem Konto der Gruppe "Administratoren" ausgeführt werden, können Sie die Namespace-Überwachungs Ereignisse auf der **Ereignisanzeige** -Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="30514-143">If you are running under an account in the Administrators group, you can view the namespace auditing events in the **Event Viewer** user interface.</span></span>

## <a name="types-of-namespace-events"></a><span data-ttu-id="30514-144">Typen von Namespace Ereignissen</span><span class="sxs-lookup"><span data-stu-id="30514-144">Types of Namespace Events</span></span>

<span data-ttu-id="30514-145">WMI verfolgt die folgenden Ereignis Typen im Sicherheits Ereignisprotokoll:</span><span class="sxs-lookup"><span data-stu-id="30514-145">WMI traces the following types of events in the Security Event Log:</span></span>

-   <span data-ttu-id="30514-146">Überprüfung erfolgreich</span><span class="sxs-lookup"><span data-stu-id="30514-146">Audit Success</span></span>

    <span data-ttu-id="30514-147">Der Vorgang muss zwei Schritte für eine erfolgreiche Überprüfung ausführen.</span><span class="sxs-lookup"><span data-stu-id="30514-147">The operation must successfully complete two steps for an Audit Success.</span></span> <span data-ttu-id="30514-148">Zuerst ermöglicht WMI den Zugriff auf die Client Anwendung oder das Skript basierend auf der Client-sid und der Namespace-DACL.</span><span class="sxs-lookup"><span data-stu-id="30514-148">First, WMI grants access to the client application or script based on the client SID and the namespace DACL.</span></span> <span data-ttu-id="30514-149">Zweitens entspricht der angeforderte Vorgang den Zugriffsrechten in der Namespace-SACL für diesen Benutzer bzw. diese Gruppe.</span><span class="sxs-lookup"><span data-stu-id="30514-149">Second, the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

-   <span data-ttu-id="30514-150">Überwachungs Fehler</span><span class="sxs-lookup"><span data-stu-id="30514-150">Audit Failure</span></span>

    <span data-ttu-id="30514-151">WMI verweigert den Zugriff auf den-Namespace, aber der angeforderte Vorgang entspricht den Zugriffsrechten in der Namespace-SACL für diesen Benutzer bzw. diese Gruppe.</span><span class="sxs-lookup"><span data-stu-id="30514-151">WMI denies access to the namespace, but the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

## <a name="namespace-access-settings"></a><span data-ttu-id="30514-152">Namespace-Zugriffs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="30514-152">Namespace Access Settings</span></span>

<span data-ttu-id="30514-153">Sie können die Namespace-Zugriffsrechte für verschiedene Konten auf dem WMI-Steuerelement anzeigen.</span><span class="sxs-lookup"><span data-stu-id="30514-153">You can view the namespace access rights for various accounts on the WMI Control.</span></span> <span data-ttu-id="30514-154">Diese Konstanten werden unter [**Namespace-Zugriffsrechte Konstanten**](namespace-access-rights-constants.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="30514-154">These constants are described in [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span> <span data-ttu-id="30514-155">Sie können den Zugriff auf einen WMI-Namespace mithilfe des WMI-Steuer Elements oder Programm gesteuert ändern.</span><span class="sxs-lookup"><span data-stu-id="30514-155">You can change the access to a WMI namespace using the WMI Control or programmatically.</span></span> <span data-ttu-id="30514-156">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="30514-156">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="30514-157">WMI überwacht Änderungen in allen Zugriffsberechtigungen, die in der folgenden Liste aufgeführt sind, mit Ausnahme der Berechtigung "Remote Aktivierung".</span><span class="sxs-lookup"><span data-stu-id="30514-157">WMI audits changes in all of the access permissions listed in the following list except for the Remote Enable permission.</span></span> <span data-ttu-id="30514-158">Die Änderungen werden als Überwachungs Erfolg oder Fehler protokolliert, der der Berechtigung zum Bearbeiten der Sicherheit entspricht.</span><span class="sxs-lookup"><span data-stu-id="30514-158">The changes are logged as audit success or failure corresponding to the Edit Security permission.</span></span>

<dl> <dt>

<span data-ttu-id="30514-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Methoden ausführen</span><span class="sxs-lookup"><span data-stu-id="30514-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Execute Methods</span></span>
</dt> <dd>

<span data-ttu-id="30514-160">Ermöglicht dem Benutzer das Ausführen von Methoden, die in WMI-Klassen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="30514-160">Permits the user to execute methods defined on WMI classes.</span></span> <span data-ttu-id="30514-161">Entspricht der **WBEM- \_ Methode \_ Execute** Access-Berechtigungs Konstante.</span><span class="sxs-lookup"><span data-stu-id="30514-161">Corresponds to the **WBEM\_METHOD\_EXECUTE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="30514-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Vollständiger Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="30514-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Full Write</span></span>
</dt> <dd>

<span data-ttu-id="30514-163">Ermöglicht den vollständigen Lese-, Schreib-und Lösch Zugriff auf WMI-Klassen und-Klassen Instanzen (statisch und dynamisch).</span><span class="sxs-lookup"><span data-stu-id="30514-163">Permits full read, write, and delete access to WMI classes and class instances, both static and dynamic.</span></span> <span data-ttu-id="30514-164">Entspricht der Berechtigungs Konstante für den **\_ vollständigen \_ Schreib \_ Zugriff von WBEM** .</span><span class="sxs-lookup"><span data-stu-id="30514-164">Corresponds to the **WBEM\_FULL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="30514-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Partieller Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="30514-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Partial Write</span></span>
</dt> <dd>

<span data-ttu-id="30514-166">Ermöglicht den Schreibzugriff auf statische WMI-Klassen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="30514-166">Permits write access to static WMI class instances.</span></span> <span data-ttu-id="30514-167">Entspricht der Zugriffs Berechtigungs Konstante für **\_ partielle \_ Schreib \_ Vorgänge von WBEM** .</span><span class="sxs-lookup"><span data-stu-id="30514-167">Corresponds to the **WBEM\_PARTIAL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="30514-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Anbieter Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="30514-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Provider Write</span></span>
</dt> <dd>

<span data-ttu-id="30514-169">Ermöglicht den Schreibzugriff auf dynamische WMI-Klassen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="30514-169">Permits write access to dynamic WMI class instances.</span></span> <span data-ttu-id="30514-170">Entspricht der Zugriffs Berechtigungs Konstante für den **WBEM- \_ Schreib \_ Anbieter** .</span><span class="sxs-lookup"><span data-stu-id="30514-170">Corresponds to the **WBEM\_WRITE\_PROVIDER** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="30514-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Konto aktivieren</span><span class="sxs-lookup"><span data-stu-id="30514-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Enable Account</span></span>
</dt> <dd>

<span data-ttu-id="30514-172">Ermöglicht den Lesezugriff auf WMI-Klassen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="30514-172">Permits read access to WMI class instances.</span></span> <span data-ttu-id="30514-173">Entspricht der Berechtigung zum Aktivieren der Zugriffsberechtigung für **WBEM \_** .</span><span class="sxs-lookup"><span data-stu-id="30514-173">Corresponds to the **WBEM\_ENABLE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="30514-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote Aktivierung</span><span class="sxs-lookup"><span data-stu-id="30514-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote Enable</span></span>
</dt> <dd>

<span data-ttu-id="30514-175">Ermöglicht den Zugriff auf den-Namespace durch Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="30514-175">Permits access to the namespace by remote computers.</span></span> <span data-ttu-id="30514-176">Entspricht der Zugriffs Berechtigungs Konstante für den WBEM-RAS-Zugriff **\_ \_** .</span><span class="sxs-lookup"><span data-stu-id="30514-176">Corresponds to the **WBEM\_REMOTE\_ACCESS** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="30514-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Sicherheit lesen</span><span class="sxs-lookup"><span data-stu-id="30514-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Read Security</span></span>
</dt> <dd>

<span data-ttu-id="30514-178">Ermöglicht den schreibgeschützten Zugriff auf DACL-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="30514-178">Permits read-only access to DACL settings.</span></span> <span data-ttu-id="30514-179">Entspricht der Konstante für den **Lese \_** Zugriff auf die Zugriffsberechtigung.</span><span class="sxs-lookup"><span data-stu-id="30514-179">Corresponds to the **READ\_CONTROL** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="30514-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Sicherheit bearbeiten</span><span class="sxs-lookup"><span data-stu-id="30514-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Edit Security</span></span>
</dt> <dd>

<span data-ttu-id="30514-181">Ermöglicht Schreibzugriff auf DACL-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="30514-181">Permits write access to DACL settings.</span></span> <span data-ttu-id="30514-182">Entspricht der Konstante zum **Schreiben der \_ DAC** -Zugriffsberechtigung.</span><span class="sxs-lookup"><span data-stu-id="30514-182">Corresponds to the **WRITE\_DAC** access permission constant.</span></span>

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a><span data-ttu-id="30514-183">Standard Berechtigungen für WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="30514-183">Default Permissions on WMI Namespaces</span></span>

<span data-ttu-id="30514-184">Die Standard Sicherheitsgruppen lauten:</span><span class="sxs-lookup"><span data-stu-id="30514-184">The default security groups are:</span></span>

-   <span data-ttu-id="30514-185">Authentifizierte Benutzer</span><span class="sxs-lookup"><span data-stu-id="30514-185">Authenticated Users</span></span>
-   <span data-ttu-id="30514-186">LOKALER DIENST</span><span class="sxs-lookup"><span data-stu-id="30514-186">LOCAL SERVICE</span></span>
-   <span data-ttu-id="30514-187">NETZWERKDIENST</span><span class="sxs-lookup"><span data-stu-id="30514-187">NETWORK SERVICE</span></span>
-   <span data-ttu-id="30514-188">Administratoren (auf dem lokalen Computer)</span><span class="sxs-lookup"><span data-stu-id="30514-188">Administrators (on the local computer)</span></span>

<span data-ttu-id="30514-189">Die Standard Zugriffsberechtigungen für die authentifizierten Benutzer, den lokalen Dienst und den Netzwerkdienst lauten:</span><span class="sxs-lookup"><span data-stu-id="30514-189">The default access permissions for the Authenticated Users, LOCAL SERVICE, and NETWORK SERVICE are:</span></span>

-   <span data-ttu-id="30514-190">Methoden ausführen</span><span class="sxs-lookup"><span data-stu-id="30514-190">Execute Methods</span></span>
-   <span data-ttu-id="30514-191">Vollständiger Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="30514-191">Full Write</span></span>
-   <span data-ttu-id="30514-192">Konto aktivieren</span><span class="sxs-lookup"><span data-stu-id="30514-192">Enable Account</span></span>

<span data-ttu-id="30514-193">Konten in der Gruppe "Administratoren" sind alle Rechte verfügbar, einschließlich der Bearbeitung von Sicherheits Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="30514-193">Accounts in the Administrators group have all rights available to them, including editing security descriptors.</span></span> <span data-ttu-id="30514-194">Aufgrund der Benutzerkontensteuerung (User Account Control, UAC) muss das WMI-Steuerelement oder das Skript jedoch mit erhöhter Sicherheit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="30514-194">However, because of User Account Control (UAC), the WMI Control or the script must be running at elevated security.</span></span> <span data-ttu-id="30514-195">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="30514-195">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="30514-196">Manchmal muss ein Skript oder eine Anwendung eine Administrator Berechtigung, wie z. b. **SeSecurityPrivilege**, aktivieren, um einen Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="30514-196">Sometimes a script or application must enable an administrator privilege, such as **SeSecurityPrivilege**, to carry out an operation.</span></span> <span data-ttu-id="30514-197">Ein Skript kann z. b. die [**getsecuritydescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) -Methode der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Klasse ohne **SeSecurityPrivilege** ausführen und die Sicherheitsinformationen in der freigegebenen [*Zugriffs Steuerungs Liste (DACL)*](/windows/desktop/SecGloss/d-gly) der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)des Drucker Objekts abrufen.</span><span class="sxs-lookup"><span data-stu-id="30514-197">For example, a script can execute the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class without **SeSecurityPrivilege** and get the security information in the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) of the printer object [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="30514-198">Die SACL-Informationen werden jedoch nur dann an das Skript zurückgegeben, wenn die **SeSecurityPrivilege** -Berechtigung verfügbar ist und für das Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="30514-198">However, the SACL information is not returned to the script unless the **SeSecurityPrivilege** privilege is available and enabled for the account.</span></span> <span data-ttu-id="30514-199">Wenn für das Konto nicht die Berechtigung verfügbar ist, kann es nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="30514-199">If the account does not have the privilege available, then it cannot be enabled.</span></span> <span data-ttu-id="30514-200">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="30514-200">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="30514-201">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30514-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30514-202">Informationen zu WMI</span><span class="sxs-lookup"><span data-stu-id="30514-202">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
