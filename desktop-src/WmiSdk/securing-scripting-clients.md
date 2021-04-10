---
description: Skripts und Visual Basic Anwendungen müssen die DCOM-Sicherheit festlegen, insbesondere für den Remote Zugriff. Außerdem müssen Sie möglicherweise Berechtigungen aktivieren.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Sichern von Skript Clients
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215328"
---
# <a name="securing-scripting-clients"></a><span data-ttu-id="dbe69-103">Sichern von Skript Clients</span><span class="sxs-lookup"><span data-stu-id="dbe69-103">Securing Scripting Clients</span></span>

<span data-ttu-id="dbe69-104">Skripts und Visual Basic Anwendungen müssen die DCOM-Sicherheit festlegen, insbesondere für den Remote Zugriff. Außerdem müssen Sie möglicherweise Berechtigungen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dbe69-104">Scripts and Visual Basic applications must set DCOM security, especially for remote access, and may also need to enable privileges.</span></span>

## <a name="default-access-permissions"></a><span data-ttu-id="dbe69-105">Standard Zugriffsberechtigungen</span><span class="sxs-lookup"><span data-stu-id="dbe69-105">Default Access Permissions</span></span>

<span data-ttu-id="dbe69-106">Der WMI-Zugriff unterscheidet sich zwischen lokalen Computern und Remote Computern.</span><span class="sxs-lookup"><span data-stu-id="dbe69-106">WMI access differs between local and remote computers.</span></span> <span data-ttu-id="dbe69-107">Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="dbe69-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="dbe69-108">Im folgenden sind die Standard Zugriffsberechtigungen nach Konto aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="dbe69-108">The following are the default access permissions by account:</span></span>

-   <span data-ttu-id="dbe69-109">Alle, LocalService, Network Service</span><span class="sxs-lookup"><span data-stu-id="dbe69-109">Everyone, LocalService, NetworkService</span></span>

    <span data-ttu-id="dbe69-110">Berechtigung zum Lesen oder Schreiben von Daten und zum Ausführen von [*Anbieter Methoden*](gloss-p.md) auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="dbe69-110">Permission to read or write data and to run [*provider methods*](gloss-p.md) on the local computer.</span></span> <span data-ttu-id="dbe69-111">Diese Konten können keine neuen Klassen erstellen oder neue Anbieter installieren.</span><span class="sxs-lookup"><span data-stu-id="dbe69-111">These accounts cannot create new classes or install new providers.</span></span>

-   <span data-ttu-id="dbe69-112">Administratorkonten</span><span class="sxs-lookup"><span data-stu-id="dbe69-112">Administrator accounts</span></span>

    <span data-ttu-id="dbe69-113">Vollzugriff auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="dbe69-113">Full control on local computer.</span></span> <span data-ttu-id="dbe69-114">Beim Herstellen einer Verbindung mit einem Remote Computer muss das Konto auch ein lokaler Administrator auf dem Remote Computer sein.</span><span class="sxs-lookup"><span data-stu-id="dbe69-114">When connecting to a remote computer, the account must be a local administrator on the remote computer also.</span></span>

## <a name="securing-a-scripting-client"></a><span data-ttu-id="dbe69-115">Sichern eines Skript Clients</span><span class="sxs-lookup"><span data-stu-id="dbe69-115">Securing a Scripting Client</span></span>

<span data-ttu-id="dbe69-116">WMI-Skripting-und Visual Basic Anwendungen müssen DCOM-Sicherheitsstufen entsprechend für die Betriebssysteme festlegen, auf die Sie abzielen.</span><span class="sxs-lookup"><span data-stu-id="dbe69-116">WMI scripting and Visual Basic applications must set DCOM security levels appropriately for the operating systems they are targeting.</span></span> <span data-ttu-id="dbe69-117">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="dbe69-117">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="dbe69-118">Beim Herstellen einer Verbindung mit einem Remote Computer müssen Sie möglicherweise den Dienst (NTLM oder Kerberos) ändern, der die Authentifizierung behandelt.</span><span class="sxs-lookup"><span data-stu-id="dbe69-118">When connecting to a remote computer, you may need to change the service (NTLM or Kerberos) that handles authentication.</span></span> <span data-ttu-id="dbe69-119">Weitere Informationen finden Sie unter [Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript](setting-the-authentication-service-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="dbe69-119">For more information, see [Setting the Authentication Service Using VBScript](setting-the-authentication-service-using-vbscript.md).</span></span>

<span data-ttu-id="dbe69-120">Der Zugriff auf einige WMI-Klassen oder-Daten erfordert möglicherweise eine Berechtigung, die nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dbe69-120">Access to some WMI classes or data may require a privilege that is not enabled.</span></span> <span data-ttu-id="dbe69-121">Beispielsweise müssen Sie beim Herstellen einer Verbindung mit der Win32-Klasse [**" \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) " die Sicherheits Berechtigung einschließen.</span><span class="sxs-lookup"><span data-stu-id="dbe69-121">For example, you must include the Security privilege when connecting to the [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) class.</span></span> <span data-ttu-id="dbe69-122">Weitere Informationen finden Sie unter [Ausführen von privilegierten Vorgängen mit VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="dbe69-122">For more information, see [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="dbe69-123">Wenn Sie von einer Active Server Seite (ASP) aus auf WMI zugreifen, ist eine IIS-Konfiguration erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dbe69-123">If you are accessing WMI from an Active Server Page (ASP), then some IIS configuration is required.</span></span> <span data-ttu-id="dbe69-124">Weitere Informationen finden Sie unter [Konfigurieren von IIS 5,0 und höher für die WMI-ASP-Skript](configuring-iis-5-for-wmi-asp-scripting.md)Erstellung.</span><span class="sxs-lookup"><span data-stu-id="dbe69-124">For more information, see [Configuring IIS 5.0 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>

<span data-ttu-id="dbe69-125">Möglicherweise versuchen Sie, eine Verbindung mit einem Namespace herzustellen, für den eine verschlüsselte Verbindung erforderlich ist, d. h. eine, die eine Authentifizierungs Ebene von PKTPRIVACY erfordert.</span><span class="sxs-lookup"><span data-stu-id="dbe69-125">You may be trying to connect to a namespace which requires an encrypted connection, in other words, one that requires an authentication level of pktPrivacy.</span></span> <span data-ttu-id="dbe69-126">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="dbe69-126">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

 

 
