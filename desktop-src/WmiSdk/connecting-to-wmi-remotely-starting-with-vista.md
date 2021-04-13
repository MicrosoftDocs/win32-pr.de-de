---
description: Zum Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remote Computer müssen Sie möglicherweise die Einstellungen für die Windows-Firewall, die Benutzerkontensteuerung (User Account Control, UAC), DCOM oder den Common Information Model Objekt-Manager (CIMOM) ändern.
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Einrichten einer Remote-WMI-Verbindung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528616"
---
# <a name="setting-up-a-remote-wmi-connection"></a><span data-ttu-id="896e7-103">Einrichten einer Remote-WMI-Verbindung</span><span class="sxs-lookup"><span data-stu-id="896e7-103">Setting up a Remote WMI Connection</span></span>

<span data-ttu-id="896e7-104">Zum Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remote Computer müssen Sie möglicherweise die Einstellungen für die [Windows-Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), die [Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM oder den Common Information Model Objekt-Manager (CIMOM) ändern.</span><span class="sxs-lookup"><span data-stu-id="896e7-104">Connecting to a WMI namespace on a remote computer may require that you change the settings for [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM, or Common Information Model Object Manager (CIMOM).</span></span>

<span data-ttu-id="896e7-105">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="896e7-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="896e7-106">Windows-Firewall-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="896e7-106">Windows Firewall Settings</span></span>](#windows-firewall-settings)
-   [<span data-ttu-id="896e7-107">Einstellungen der Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="896e7-107">User Account Control Settings</span></span>](#user-account-control-settings)
-   [<span data-ttu-id="896e7-108">DCOM-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="896e7-108">DCOM Settings</span></span>](#dcom-settings)
-   [<span data-ttu-id="896e7-109">CIMOM-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="896e7-109">CIMOM Settings</span></span>](#cimom-settings)
-   [<span data-ttu-id="896e7-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="896e7-110">Related topics</span></span>](#related-topics)

## <a name="windows-firewall-settings"></a><span data-ttu-id="896e7-111">Windows-Firewalleinstellungen</span><span class="sxs-lookup"><span data-stu-id="896e7-111">Windows Firewall Settings</span></span>

<span data-ttu-id="896e7-112">WMI-Einstellungen für Windows-Firewall-Einstellungen ermöglichen nur WMI-Verbindungen und keine anderen DCOM-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="896e7-112">WMI settings for Windows Firewall settings enable only WMI connections, rather than other DCOM applications as well.</span></span>

<span data-ttu-id="896e7-113">Eine Ausnahme muss in der Firewall für WMI auf dem Remote Zielcomputer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="896e7-113">An exception must be set in the firewall for WMI on the remote target computer.</span></span> <span data-ttu-id="896e7-114">Die Ausnahme für WMI ermöglicht WMI, Remote Verbindungen und asynchrone Rückrufe zu Unsecapp.exe zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="896e7-114">The exception for WMI allows WMI to receive remote connections and asynchronous callbacks to Unsecapp.exe.</span></span> <span data-ttu-id="896e7-115">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="896e7-115">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="896e7-116">Wenn eine Client Anwendung eine eigene Senke erstellt, muss diese Senke explizit den Firewallausnahmen hinzugefügt werden, damit Rückrufe erfolgreich ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="896e7-116">If a client application creates its own sink, that sink must be explicitly added to the firewall exceptions to allow callbacks to succeed.</span></span>

<span data-ttu-id="896e7-117">Die Ausnahme für WMI funktioniert auch, wenn WMI mit einem Fixed-Port mit dem Befehl **winmgmt/standalonehost** gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="896e7-117">The exception for WMI also works if WMI has been started with a fixed port, using the **winmgmt /standalonehost** command.</span></span> <span data-ttu-id="896e7-118">Weitere Informationen finden Sie unter [Einrichten eines Fixed-Ports für WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="896e7-118">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="896e7-119">Sie können den WMI-Datenverkehr über die Benutzeroberfläche der Windows-Firewall aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="896e7-119">You can enable or disable WMI traffic through the Windows Firewall UI.</span></span>

<span data-ttu-id="896e7-120">**So aktivieren oder deaktivieren Sie WMI-Datenverkehr über die Firewall**</span><span class="sxs-lookup"><span data-stu-id="896e7-120">**To enable or disable WMI traffic using firewall UI**</span></span>

1.  <span data-ttu-id="896e7-121">Klicken Sie in der **Systemsteuerung** auf **Sicherheit** und dann auf **Windows-Firewall**.</span><span class="sxs-lookup"><span data-stu-id="896e7-121">In the **Control Panel**, click **Security** and then click **Windows Firewall**.</span></span>
2.  <span data-ttu-id="896e7-122">Klicken Sie auf **Einstellungen ändern** und dann auf die Registerkarte **Ausnahmen** .</span><span class="sxs-lookup"><span data-stu-id="896e7-122">Click **Change Settings** and then click the **Exceptions** tab.</span></span>
3.  <span data-ttu-id="896e7-123">Aktivieren Sie im Fenster Ausnahmen das Kontrollkästchen für **Windows-Verwaltungsinstrumentation (WMI)** , um den WMI-Datenverkehr über die Firewall zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="896e7-123">In the Exceptions window, select the check box for **Windows Management Instrumentation (WMI)** to enable WMI traffic through the firewall.</span></span> <span data-ttu-id="896e7-124">Deaktivieren Sie das Kontrollkästchen, um den WMI-Datenverkehr zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="896e7-124">To disable WMI traffic, clear the check box.</span></span>

<span data-ttu-id="896e7-125">Sie können den WMI-Datenverkehr über die Firewall an der Eingabeaufforderung aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="896e7-125">You can enable or disable WMI traffic through the firewall at the command prompt.</span></span>

<span data-ttu-id="896e7-126">**So aktivieren oder deaktivieren Sie WMI-Datenverkehr an der Eingabeaufforderung mithilfe der WMI-Regelgruppe**</span><span class="sxs-lookup"><span data-stu-id="896e7-126">**To enable or disable WMI traffic at command prompt using WMI rule group**</span></span>

-   <span data-ttu-id="896e7-127">Verwenden Sie die folgenden Befehle an einer Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="896e7-127">Use the following commands at a command prompt.</span></span> <span data-ttu-id="896e7-128">Geben Sie Folgendes ein, um den WMI-Datenverkehr über die Firewall zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="896e7-128">Type the following to enable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="896e7-129">**netsh advfirewall firewall set rule Group = "Windows Management Instrumentation (WMI)" New enable = yes**</span><span class="sxs-lookup"><span data-stu-id="896e7-129">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**</span></span>

    <span data-ttu-id="896e7-130">Geben Sie folgenden Befehl ein, um den WMI-Datenverkehr über die Firewall zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="896e7-130">Type the following command to disable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="896e7-131">**netsh advfirewall firewall set rule Group = "Windows Management Instrumentation (WMI)" New enable = no**</span><span class="sxs-lookup"><span data-stu-id="896e7-131">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**</span></span>

<span data-ttu-id="896e7-132">Anstatt den einzelnen WMI-Regel Gruppen Befehl zu verwenden, können Sie auch einzelne Befehle für jeden DCOM-, WMI-Dienst und jede Senke verwenden.</span><span class="sxs-lookup"><span data-stu-id="896e7-132">Rather than using the single WMI rule group command, you also can use individual commands for each of the DCOM, WMI service, and sink.</span></span>

<span data-ttu-id="896e7-133">**So aktivieren Sie WMI-Datenverkehr mit separaten Regeln für DCOM, WMI, Rückruf Senke und ausgehende Verbindungen**</span><span class="sxs-lookup"><span data-stu-id="896e7-133">**To enable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="896e7-134">Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für den DCOM-Port 135 einzurichten.</span><span class="sxs-lookup"><span data-stu-id="896e7-134">To establish a firewall exception for DCOM port 135, use the following command.</span></span>

    <span data-ttu-id="896e7-135">**netsh advfirewall Firewall Add Rule dir = in Name = "DCOM" Program =% systemroot% \\ system32 \\svchost.exe Service = RPCSS Action = Allow Protocol = TCP localport = 135**</span><span class="sxs-lookup"><span data-stu-id="896e7-135">**netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot%\\system32\\svchost.exe service=rpcss action=allow protocol=TCP localport=135**</span></span>

2.  <span data-ttu-id="896e7-136">Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für den WMI-Dienst einzurichten.</span><span class="sxs-lookup"><span data-stu-id="896e7-136">To establish a firewall exception for the WMI service, use the following command.</span></span>

    <span data-ttu-id="896e7-137">**netsh advfirewall Firewall Add Rule dir = in Name = "WMI" Program =% systemroot% \\ system32 \\svchost.exe Service = WinMgmt Action = Allow Protocol = TCP localport = any**</span><span class="sxs-lookup"><span data-stu-id="896e7-137">**netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot%\\system32\\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**</span></span>

3.  <span data-ttu-id="896e7-138">Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für die Senke zu erstellen, die Rückrufe von einem Remote Computer empfängt.</span><span class="sxs-lookup"><span data-stu-id="896e7-138">To establish a firewall exception for the sink that receives callbacks from a remote computer, use the following command.</span></span>

    <span data-ttu-id="896e7-139">**netsh advfirewall Firewall Add Rule dir = in Name = "unabcapp" Program =% systemroot% \\ system32 \\ WBEM \\unsecapp.exe Action = Allow**</span><span class="sxs-lookup"><span data-stu-id="896e7-139">**netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot%\\system32\\wbem\\unsecapp.exe action=allow**</span></span>

4.  <span data-ttu-id="896e7-140">Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für ausgehende Verbindungen mit einem Remote Computer einzurichten, mit dem der lokale Computer asynchron kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="896e7-140">To establish a firewall exception for outgoing connections to a remote computer that the local computer is communicating with asynchronously, use the following command.</span></span>

    <span data-ttu-id="896e7-141">**netsh advfirewall Firewall Add Rule dir = out Name = "WMI \_ out" Program =% systemroot% \\ system32 \\svchost.exe Service = WinMgmt Action = Allow Protocol = TCP localport = any**</span><span class="sxs-lookup"><span data-stu-id="896e7-141">**netsh advfirewall firewall add rule dir=out name ="WMI\_OUT" program=%systemroot%\\system32\\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**</span></span>

<span data-ttu-id="896e7-142">Verwenden Sie die folgenden Befehle, um die Firewallausnahmen separat zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="896e7-142">To disable the firewall exceptions separately, use the following commands.</span></span>

<span data-ttu-id="896e7-143">**So deaktivieren Sie WMI-Datenverkehr mit separaten Regeln für DCOM, WMI, Rückruf Senke und ausgehende Verbindungen**</span><span class="sxs-lookup"><span data-stu-id="896e7-143">**To disable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="896e7-144">Zum Deaktivieren der DCOM-Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="896e7-144">To disable the DCOM exception.</span></span>

    <span data-ttu-id="896e7-145">**netsh advfirewall Firewall Delete Rule Name = "DCOM"**</span><span class="sxs-lookup"><span data-stu-id="896e7-145">**netsh advfirewall firewall delete rule name="DCOM"**</span></span>

2.  <span data-ttu-id="896e7-146">Zum Deaktivieren der Ausnahme des WMI-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="896e7-146">To disable the WMI service exception.</span></span>

    <span data-ttu-id="896e7-147">**netsh advfirewall Firewall Delete Rule Name = "WMI"**</span><span class="sxs-lookup"><span data-stu-id="896e7-147">**netsh advfirewall firewall delete rule name="WMI"**</span></span>

3.  <span data-ttu-id="896e7-148">, Wenn die Senke Ausnahme deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="896e7-148">To disable the sink exception.</span></span>

    <span data-ttu-id="896e7-149">**netsh advfirewall Firewall Delete Rule Name = "unabcapp"**</span><span class="sxs-lookup"><span data-stu-id="896e7-149">**netsh advfirewall firewall delete rule name="UnsecApp"**</span></span>

4.  <span data-ttu-id="896e7-150">, Wenn die ausgehende Ausnahme deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="896e7-150">To disable the outgoing exception.</span></span>

    <span data-ttu-id="896e7-151">**netsh advfirewall Firewall Delete Rule Name = "WMI \_ out"**</span><span class="sxs-lookup"><span data-stu-id="896e7-151">**netsh advfirewall firewall delete rule name="WMI\_OUT"**</span></span>

## <a name="user-account-control-settings"></a><span data-ttu-id="896e7-152">Einstellungen der Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="896e7-152">User Account Control Settings</span></span>

<span data-ttu-id="896e7-153">Die Benutzerkontensteuerung (User Account Control, UAC)-Zugriffs Token-Filterung kann beeinflussen, welche Vorgänge in WMI-Namespaces zulässig sind oder welche Daten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="896e7-153">User Account Control (UAC) access-token filtering can affect which operations are allowed in WMI namespaces or what data is returned.</span></span> <span data-ttu-id="896e7-154">Unter UAC werden alle Konten in der lokalen Administratoren Gruppe mit einem Standardbenutzer [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)ausgeführt, das auch als UAC-Zugriffs Token-Filterung bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="896e7-154">Under UAC, all accounts in the local Administrators group run with a standard user [*access token*](/windows/desktop/SecGloss/a-gly), also known as UAC access-token filtering.</span></span> <span data-ttu-id="896e7-155">Ein Administrator Konto kann ein Skript mit erhöhten Berechtigungen ausführen – "als Administrator ausführen".</span><span class="sxs-lookup"><span data-stu-id="896e7-155">An administrator account can run a script with an elevated privilege—"Run as Administrator".</span></span>

<span data-ttu-id="896e7-156">Wenn Sie keine Verbindung mit dem integrierten Administrator Konto herstellen, wirkt sich UAC anders auf die Verbindungen mit einem Remote Computer aus, je nachdem, ob sich die beiden Computer in einer Domäne oder Arbeitsgruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="896e7-156">When you are not connecting to the built-in Administrator account, UAC affects connections to a remote computer differently depending on whether the two computers are in a domain or a workgroup.</span></span> <span data-ttu-id="896e7-157">Weitere Informationen zu UAC und Remote Verbindungen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="896e7-157">For more information about UAC and remote connections, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="dcom-settings"></a><span data-ttu-id="896e7-158">DCOM-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="896e7-158">DCOM Settings</span></span>

<span data-ttu-id="896e7-159">Weitere Informationen zu DCOM-Einstellungen finden Sie unter [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="896e7-159">For more information on DCOM settings, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span> <span data-ttu-id="896e7-160">Die UAC wirkt sich jedoch auf Verbindungen für nicht-Domänen Benutzerkonten aus.</span><span class="sxs-lookup"><span data-stu-id="896e7-160">However, UAC affects connections for nondomain user accounts.</span></span> <span data-ttu-id="896e7-161">Wenn Sie über ein nicht-Domänen Benutzerkonto, das in der lokalen Administratoren Gruppe des Remote Computers enthalten ist, eine Verbindung mit einem Remote Computer herstellen, müssen Sie dem Konto explizit Remote-DCOM-Zugriff,-Aktivierung und-Startrechte erteilen.</span><span class="sxs-lookup"><span data-stu-id="896e7-161">If you connect to a remote computer using a nondomain user account included in the local Administrators group of the remote computer, then you must explicitly grant remote DCOM access, activation, and launch rights to the account.</span></span>

## <a name="cimom-settings"></a><span data-ttu-id="896e7-162">CIMOM-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="896e7-162">CIMOM Settings</span></span>

<span data-ttu-id="896e7-163">Die CIMOM-Einstellungen müssen aktualisiert werden, wenn die Remote Verbindung zwischen Computern besteht, die keine Vertrauensstellung haben. Andernfalls tritt bei einer asynchronen Verbindung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="896e7-163">The CIMOM settings need to be updated if the remote connection is between computers that do not have a trust relationship; otherwise, an asynchronous connection will fail.</span></span> <span data-ttu-id="896e7-164">Diese Einstellung sollte für Computer in derselben Domäne oder in vertrauenswürdigen Domänen nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="896e7-164">This setting should not be modified for computers in the same domain or in trusted domains.</span></span>

<span data-ttu-id="896e7-165">Der folgende Registrierungs Eintrag muss geändert werden, um anonyme Rückrufe zuzulassen:</span><span class="sxs-lookup"><span data-stu-id="896e7-165">The following registry entry needs to be modified to allow anonymous callbacks:</span></span>

<span data-ttu-id="896e7-166">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Zuteilungs Nummer**</span><span class="sxs-lookup"><span data-stu-id="896e7-166">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**AllowAnonymousCallback**</span></span><dl> <dt>

               Data type
</dt> <dd>               <span data-ttu-id="896e7-167">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="896e7-167">REG\_DWORD</span></span></dd> </dl>

<span data-ttu-id="896e7-168">Wenn der Wert von "Zuordnungen" auf "0" festgelegt ist, verhindert der WMI-Dienst anonyme **Rückrufe** an den Client.</span><span class="sxs-lookup"><span data-stu-id="896e7-168">If the **AllowAnonymousCallback** value is set to 0, the WMI service prevents anonymous callbacks to the client.</span></span> <span data-ttu-id="896e7-169">Wenn der Wert auf 1 festgelegt ist, lässt der WMI-Dienst anonyme Rückrufe an den Client zu.</span><span class="sxs-lookup"><span data-stu-id="896e7-169">If the value is set to 1, the WMI service allows anonymous callbacks to the client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="896e7-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="896e7-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="896e7-171">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="896e7-171">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
