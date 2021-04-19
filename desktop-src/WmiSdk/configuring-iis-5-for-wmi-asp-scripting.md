---
description: Alle Authentifizierungs Einstellungen werden über den Internetdienste-Manager vorgenommen.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Konfigurieren von IIS 5,0 und höher für die WMI-ASP-Skripterstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355640"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a><span data-ttu-id="717ed-103">Konfigurieren von IIS 5,0 und höher für die WMI-ASP-Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="717ed-103">Configuring IIS 5.0 and Later for WMI ASP Scripting</span></span>

<span data-ttu-id="717ed-104">Alle Authentifizierungs Einstellungen werden über den Internetdienste-Manager vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="717ed-104">All authentication settings are made through the Internet Services Manager.</span></span>

<span data-ttu-id="717ed-105">Beachten Sie beim Konfigurieren von Internet Information Server (IIS) 5,0 und IIS 6,0 Security für WMI ASP-Skripts die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="717ed-105">When configuring Internet Information Server (IIS) 5.0 and IIS 6.0 security for WMI ASP scripts, consider the following issues:</span></span>

-   [<span data-ttu-id="717ed-106">Authentifizierungsebene</span><span class="sxs-lookup"><span data-stu-id="717ed-106">Authentication level</span></span>](#authentication-level)

    <span data-ttu-id="717ed-107">Sie können auf Server-, Verzeichnis-oder Dateiebene konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="717ed-107">You can configure at the server, directory, or file level.</span></span>

-   [<span data-ttu-id="717ed-108">Authentifizierungs Einstellung</span><span class="sxs-lookup"><span data-stu-id="717ed-108">Authentication setting</span></span>](#authentication-setting)

    <span data-ttu-id="717ed-109">Sie können die Authentifizierung auf anonyme, integrierte Fenster oder beides festlegen.</span><span class="sxs-lookup"><span data-stu-id="717ed-109">You can set authentication to Anonymous, Integrated Windows, or both.</span></span>

-   [<span data-ttu-id="717ed-110">Schutz</span><span class="sxs-lookup"><span data-stu-id="717ed-110">Protection</span></span>](#protection)

    <span data-ttu-id="717ed-111">Sie können festlegen, dass der ASP-Prozess in-Process (niedriger Schutz) oder außerhalb des Prozesses ausgeführt wird, indem Sie Dllhost.exe (mittlerer oder hoher Schutz) verwenden.</span><span class="sxs-lookup"><span data-stu-id="717ed-111">You can set the ASP to run in-process (low protection), or out-of-process by using Dllhost.exe (medium or high protection).</span></span>

## <a name="authentication-level"></a><span data-ttu-id="717ed-112">Authentifizierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="717ed-112">Authentication Level</span></span>

<span data-ttu-id="717ed-113">Zur zusätzlichen Sicherheit können Sie die Authentifizierung auf Verzeichnis-oder Dateiebene konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="717ed-113">For added security, you can configure the authentication at the directory or file level.</span></span>

<span data-ttu-id="717ed-114">Wenn die Authentifizierung auf Serverebene festgelegt ist, werden alle nachfolgenden Verzeichnisse und Dateien der Server Authentifizierung entsprechen, sofern Sie nicht explizit auf Verzeichnis-oder Dateiebene geändert werden.</span><span class="sxs-lookup"><span data-stu-id="717ed-114">If authentication is set at the server level, all subsequent directories and files adhere to the server authentication unless explicitly altered at the directory or file level.</span></span> <span data-ttu-id="717ed-115">Sie können eine Verzeichnisstruktur erstellen, die alle WMI-ASP-Skripts enthält, in denen HTML-Seiten und für WMI spezifische-spezifische Informationen unabhängig vom Rest des Servers konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="717ed-115">You can create a directory structure to contain all WMI ASP scripts where HTML pages and ASPs specific to WMI can be configured independently from the rest of the server.</span></span> <span data-ttu-id="717ed-116">Führen Sie das folgende Verfahren aus, um die Authentifizierungs Ebene eines Servers, Verzeichnisses oder einer Datei zu ändern.</span><span class="sxs-lookup"><span data-stu-id="717ed-116">Perform the following procedure to change the authentication level of a server, directory, or file.</span></span>

<span data-ttu-id="717ed-117">**So legen Sie die Authentifizierung auf einer beliebigen Ebene fest**</span><span class="sxs-lookup"><span data-stu-id="717ed-117">**To set the authentication at any level**</span></span>

1.  <span data-ttu-id="717ed-118">Doppelklicken Sie in der Systemsteuerung auf **Verwaltung**, und doppelklicken Sie dann auf das IIS-Snap-in.</span><span class="sxs-lookup"><span data-stu-id="717ed-118">In Control Panel, double-click **Administrative Tools**, and then double-click the IIS snap-in.</span></span>

2.  <span data-ttu-id="717ed-119">Suchen Sie das ASP-Seiten Symbol, und öffnen Sie dann die Eigenschaften für die festzulegende Ebene (Server, Verzeichnis oder Datei).</span><span class="sxs-lookup"><span data-stu-id="717ed-119">Locate the ASP page icon, and then open the properties for the level to set, which can be server, directory, or file.</span></span>

    > [!Note]  
    > <span data-ttu-id="717ed-120">Die Authentifizierungs Einstellungen befinden sich auf der Registerkarte **Verzeichnis Sicherheit** oder **Datei Sicherheit** des **Eigenschaften** Blatts.</span><span class="sxs-lookup"><span data-stu-id="717ed-120">Authentication settings are located on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

     

## <a name="authentication-setting"></a><span data-ttu-id="717ed-121">Authentifizierungs Einstellung</span><span class="sxs-lookup"><span data-stu-id="717ed-121">Authentication Setting</span></span>

<span data-ttu-id="717ed-122">Bei WMI-ASP-Skripts bietet die Kombination aus aktivierter anonymer Authentifizierung (deaktiviert) und integrierter Windows-Authentifizierung (aktiviert) mehr Möglichkeiten zum Festlegen der Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="717ed-122">For WMI ASP scripts, the combination of Anonymous authentication turned off (unchecked), and Integrated Windows authentication turned on (checked) provides greater opportunity to set security.</span></span> <span data-ttu-id="717ed-123">Um die IIS-Authentifizierungs Einstellungen von NT LAN Manager (NTLM), Passport oder Digest verwenden zu können, müssen Sie die Remote Aktivierungs Berechtigungen aktivieren, da der Benutzer als Netzwerk Identität behandelt und Remote protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="717ed-123">To use NT LAN Manager (NTLM), Passport, or Digest IIS authentication settings, you must turn on the remote enable privileges, because the user is treated as a network identity and logged remotely.</span></span> <span data-ttu-id="717ed-124">Die Einstellung für die Remote Aktivierung ist für die anonyme Authentifizierung und die Standard Authentifizierung nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="717ed-124">The remote enable setting is not required for Anonymous and Basic authentication.</span></span> <span data-ttu-id="717ed-125">Das System ist jedoch viel weniger sicher, wenn Sie die anonyme Authentifizierung und die Standard Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="717ed-125">However, the system is much less secure when you are using Anonymous and Basic authentication.</span></span>

<span data-ttu-id="717ed-126">Wenn die anonyme Authentifizierung mit oder ohne integrierte Windows-Authentifizierung verwendet wird, besteht der sicherste Ansatz darin, eine Anmeldung zu verwenden, bei der ein Benutzer einen Benutzernamen und ein Kennwort eingeben muss.</span><span class="sxs-lookup"><span data-stu-id="717ed-126">If Anonymous authentication is used with or without Integrated Windows authentication, the most secure approach is to use a logon that requires a user to enter a username and password.</span></span> <span data-ttu-id="717ed-127">Die Standardanmeldung ist die IIS-Identität, aber eine Anmeldung kann erstellt werden, indem bestimmte Berechtigungen verwendet werden, die für die WMI-ASP-Skripts geeignet sind und als Konto für die anonymen oder Gast Verbindungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="717ed-127">The default logon is the IIS identity, but a logon can be created by using specific permissions suited for the WMI ASP Scripts that can be used as the account for the anonymous or guest connections.</span></span>

<span data-ttu-id="717ed-128">Wenn Sie eine Anmelde-ID auswählen, bei der es sich nicht um eine IIS-Identität handelt, deaktivieren Sie das Kontrollkästchen **IIS-Kennwort steuern** , und geben Sie das richtige Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="717ed-128">If you choose a logon identifier that is not an IIS identity, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="717ed-129">Dadurch werden alle anonymen oder Gast Verbindungen gezwungen, den Anmelde Bezeichner zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="717ed-129">This forces all anonymous or guest connections to use the logon identifier.</span></span> <span data-ttu-id="717ed-130">Durch das Erstellen einer Anmeldung getrennt von der IIS-Identität können die Berechtigungen eines Kontos, das auf WMI zugreift, ohne Auswirkung auf die anderen Verzeichnisse oder Dateien auf dem IIS-Server gesteuert werden – es sei denn, die Authentifizierung ist auf Serverebene festgelegt.</span><span class="sxs-lookup"><span data-stu-id="717ed-130">By creating a logon separate from the IIS identity, the privileges of an account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="717ed-131">Führen Sie das folgende Verfahren aus, um die Authentifizierungsanforderungen für die ASP-Seite mithilfe des IIS-Snap-Ins in der Systemsteuerung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="717ed-131">Perform the following procedure to set the authentication requirements for the ASP page using the IIS snap-in in the Control Panel.</span></span>

<span data-ttu-id="717ed-132">**So gelangen Sie zur Konto Einstellung**</span><span class="sxs-lookup"><span data-stu-id="717ed-132">**To get to the account setting**</span></span>

1.  <span data-ttu-id="717ed-133">Doppelklicken Sie in der Systemsteuerung auf das Symbol **Verwaltung** , öffnen Sie das IIS-Snap-in, suchen Sie die ASP-Seite, und öffnen Sie die Eigenschaften der festzulegenden Ebene (Server, Verzeichnis oder Datei).</span><span class="sxs-lookup"><span data-stu-id="717ed-133">In Control Panel, double-click the **Administrative Tools** icon, open the IIS snap-in, locate your ASP page, and open the properties of the level to set, which can be server, directory, or file.</span></span>

    <span data-ttu-id="717ed-134">Die Authentifizierungs Einstellungen befinden sich auf der Registerkarte **Verzeichnis Sicherheit** oder **Datei Sicherheit** des **Eigenschaften** Blatts.</span><span class="sxs-lookup"><span data-stu-id="717ed-134">Authentication settings can be found on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

2.  <span data-ttu-id="717ed-135">Klicken Sie im Bereich anonyme Authentifizierung auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="717ed-135">In the Anonymous authentication area, click **Edit**.</span></span>

3.  <span data-ttu-id="717ed-136">Wenn ein anderer Anmelde-ID als die IIS-Identität ausgewählt ist, deaktivieren Sie das Kontrollkästchen zum **Steuern des Kennworts für IIS zulassen**, und geben Sie das richtige Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="717ed-136">If a logon identifier other than the IIS identity is selected, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="717ed-137">Dadurch werden alle anonymen oder Gast Verbindungen gezwungen, den Anmelde Bezeichner zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="717ed-137">This forces all anonymous or guest connections to use the logon identifier.</span></span>

<span data-ttu-id="717ed-138">Durch die Verwendung einer anderen Anmeldung als der IIS-Identität können die Berechtigungen des Kontos, das auf WMI zugreift, ohne Auswirkung auf die anderen Verzeichnisse oder Dateien auf dem IIS-Server gesteuert werden – es sei denn, die Authentifizierung ist auf Serverebene festgelegt.</span><span class="sxs-lookup"><span data-stu-id="717ed-138">By using a logon different from the IIS identity, the privileges of the account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="717ed-139">Die vorherige Konfiguration ermöglicht dem IIS-Server die Verwendung der anonymen Authentifizierung in einigen Bereichen, der integrierten Windows-Authentifizierung oder der gemischten Authentifizierung in anderen.</span><span class="sxs-lookup"><span data-stu-id="717ed-139">The previous configuration allows the IIS server to use Anonymous authentication in some areas, and Integrated Windows or mixed authentication in others.</span></span>

## <a name="protection"></a><span data-ttu-id="717ed-140">Schutz</span><span class="sxs-lookup"><span data-stu-id="717ed-140">Protection</span></span>

<span data-ttu-id="717ed-141">Beim Konfigurieren des IIS-Servers sollte bei der letzten Überlegung der Schutz beim Ausführen eines ASP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="717ed-141">The last consideration when configuring the IIS server is which protection to use when executing an ASP.</span></span>

<span data-ttu-id="717ed-142">Sie können einen ASP festlegen, um Folgendes auszuführen:</span><span class="sxs-lookup"><span data-stu-id="717ed-142">You can set an ASP to run the following:</span></span>

-   <span data-ttu-id="717ed-143">Prozess interne zu IIS (niedriger Schutz).</span><span class="sxs-lookup"><span data-stu-id="717ed-143">In-process to IIS (low protection).</span></span>

-   <span data-ttu-id="717ed-144">Extern zu IIS mit Dllhost.exe als Pool oder außerhalb des Prozesses (gepoolter mittlerer Schutz).</span><span class="sxs-lookup"><span data-stu-id="717ed-144">External to IIS with Dllhost.exe as pooled or out-of-process (pooled medium protection).</span></span>

-   <span data-ttu-id="717ed-145">Out-of-Process-Self-Host (hoher Schutz).</span><span class="sxs-lookup"><span data-stu-id="717ed-145">Out-of-process self-host (high protection).</span></span>

> [!Note]  
> <span data-ttu-id="717ed-146">Verwenden Sie in einem Pool zusammengefasste Hosts, um die Sicherheit und Leistung am besten auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="717ed-146">For the best balance of security and performance, use pooled host.</span></span>

 

 

 



