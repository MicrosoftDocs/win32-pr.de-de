---
title: Standardeinstellungen .NET Framework
description: .NET Framework 4,5 ist Standard, und .NET Framework 3,5 ist optional.
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "106338098"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a><span data-ttu-id="341e1-103">.NET Framework 4,5 ist Standard, und .NET Framework 3,5 ist optional.</span><span class="sxs-lookup"><span data-stu-id="341e1-103">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>

## <a name="platforms"></a><span data-ttu-id="341e1-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="341e1-104">Platforms</span></span>

<span data-ttu-id="341e1-105">**Clients**   Windows 8</span><span class="sxs-lookup"><span data-stu-id="341e1-105">**Clients**   Windows 8</span></span>  
<span data-ttu-id="341e1-106">**Server**   Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="341e1-106">**Servers**   Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="341e1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="341e1-107">Description</span></span>

<span data-ttu-id="341e1-108">.NET Framework 4,5 ist in Windows 8 standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="341e1-108">.NET Framework 4.5 is enabled by default in Windows 8.</span></span> <span data-ttu-id="341e1-109">Windows 8 umfasst .NET 3,5 nicht standardmäßig, aber die Dateien für .NET 3,5 sind auf dem Windows 8-Installationsmedium als optionales Feature verfügbar.</span><span class="sxs-lookup"><span data-stu-id="341e1-109">Windows 8 does not include .NET 3.5 by default, but the files for .NET 3.5 are available on the Windows 8 installation media as an optional feature.</span></span>

<span data-ttu-id="341e1-110">Wenn für den Benutzer ein Upgrade von Windows 7 auf Windows 8 ausgeführt wird, ist .NET Framework 3,5 vollständig aktiviert, um sicherzustellen, dass alle apps auf dem Computer weiterhin ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="341e1-110">If the user is upgrading from Windows 7 to Windows 8, .NET Framework 3.5 is fully enabled to ensure that any apps on the computer continue to work correctly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="341e1-111">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="341e1-111">Manifestation</span></span>

<span data-ttu-id="341e1-112">Wenn der Benutzer eine Neuinstallation von Windows 8 durchführt und dann apps installiert, für die .NET Framework 3,5 (oder 2,0) erforderlich ist, wird eine Anforderung für die erforderlichen .NET 3,5-Dateien auslöst.</span><span class="sxs-lookup"><span data-stu-id="341e1-112">If the user performs a clean installation of Windows 8, and then installs apps that require .NET Framework 3.5 (or 2.0), they will trigger a request for the necessary .NET 3.5 files.</span></span> <span data-ttu-id="341e1-113">Normalerweise werden die fehlenden Dateien von Windows Update heruntergeladen (nachdem der Benutzer zur Berechtigung aufgefordert wurde), aber wenn der Zugriff auf Windows Update nicht möglich ist, schlägt die Aktivierung von .NET Framework 3,5 fehl, es sei denn, es wurde eine alternative Quelle für die fehlenden Dateien angegeben.</span><span class="sxs-lookup"><span data-stu-id="341e1-113">Normally the missing files will be downloaded from Windows Update (after asking the user for permission), but if access to Windows Update is not possible, enabling .NET Framework 3.5 will fail unless an alternate source for the missing files has been specified.</span></span>

## <a name="mitigation"></a><span data-ttu-id="341e1-114">Minderung</span><span class="sxs-lookup"><span data-stu-id="341e1-114">Mitigation</span></span>

<span data-ttu-id="341e1-115">So aktivieren Sie .NET Framework 3,5 nur auf Testcomputern mit einer sauberen Installation von Windows 8:</span><span class="sxs-lookup"><span data-stu-id="341e1-115">To enable .NET Framework 3.5 on only test machines with clean installs of Windows 8:</span></span>

1.  <span data-ttu-id="341e1-116">Kopieren \\ \\ Sie die Quellen SxS \\ aus dem Image des bereitgestellten Betriebssystem-Build ISO in dotnet35 oder einen ähnlichen Ordner.</span><span class="sxs-lookup"><span data-stu-id="341e1-116">Copy \\sources\\sxs\\ from the mounted operating system build ISO image to dotnet35 or similar folder.</span></span> <span data-ttu-id="341e1-117">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="341e1-117">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="341e1-118">Führen Sie diese Befehlszeile mit Administrator Berechtigungen aus:</span><span class="sxs-lookup"><span data-stu-id="341e1-118">Execute this command line using admin privileges:</span></span>
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> <span data-ttu-id="341e1-119">Der Ordner "Sources \\ SxS" darf nicht als Verteilungsmechanismus verwendet werden, da dies kein unterstützter Mechanismus ist.</span><span class="sxs-lookup"><span data-stu-id="341e1-119">The sources\\SxS folder must not be used as a redistribution mechanism since this is not a supported mechanism.</span></span>



## <a name="solution"></a><span data-ttu-id="341e1-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="341e1-120">Solution</span></span>

<span data-ttu-id="341e1-121">**Für Consumer:**</span><span class="sxs-lookup"><span data-stu-id="341e1-121">**For consumers:**</span></span>

<span data-ttu-id="341e1-122">Windows 8 umfasst einen Mechanismus, der .NET Framework 3,5 automatisch aktiviert, wenn versucht wird, das verteilbare Paket zu installieren, oder wenn ein Anwendungsinstallations Programm, das .NET 3,5 benötigt, das verteilbare Paket aufruft.</span><span class="sxs-lookup"><span data-stu-id="341e1-122">Windows 8 includes a mechanism that automatically enables .NET Framework 3.5 when attempting to install the redistributable package or when an application installer that needs .NET 3.5 invokes the redistributable.</span></span>

<span data-ttu-id="341e1-123">**Für App-Entwickler (und IT-Administratoren):**</span><span class="sxs-lookup"><span data-stu-id="341e1-123">**For App developers (and IT Administrators):**</span></span>

<span data-ttu-id="341e1-124">IT-Administratoren können .NET 3,5-apps so konfigurieren, dass Sie entweder unter .NET 3,5 oder .NET 4,5 ausgeführt werden (je nachdem, was bereits installiert ist).</span><span class="sxs-lookup"><span data-stu-id="341e1-124">IT administrators can configure .NET 3.5 apps to run on either .NET 3.5 or .NET 4.5 (depending on what's already installed).</span></span> <span data-ttu-id="341e1-125">Um eine verwaltete App entweder auf 3,5 oder 4,5 auszuführen, fügen Sie einfach einen Abschnitt in der Anwendungs Konfigurationsdatei hinzu.</span><span class="sxs-lookup"><span data-stu-id="341e1-125">In order to run a managed app on either 3.5 or 4.5, just add a section in the application configuration file.</span></span> <span data-ttu-id="341e1-126">Dadurch wird sichergestellt, dass die APP, wenn .NET 3,5 installiert ist, auf .NET 3,5 ausgeführt wird. Andernfalls wird die APP unter .NET 4,5 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="341e1-126">This will ensure that if .NET 3.5 is installed, the app will run on .NET 3.5; otherwise the app will run on .NET 4.5.</span></span> <span data-ttu-id="341e1-127">Ein Beispiel für den zusätzlichen Abschnitt in der Konfigurationsdatei finden Sie unten:</span><span class="sxs-lookup"><span data-stu-id="341e1-127">An example of the additional section in the configuration file is provided below:</span></span>


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



<span data-ttu-id="341e1-128">**Für Unternehmens OEMs:**</span><span class="sxs-lookup"><span data-stu-id="341e1-128">**For enterprise OEMs:**</span></span>

<span data-ttu-id="341e1-129">So aktivieren Sie .NET Framework 3,5 für EEAP-Builds und für Anwendungen, die keinen Zugriff auf Windows Update haben:</span><span class="sxs-lookup"><span data-stu-id="341e1-129">To enable .NET Framework 3.5 for EEAP builds and for applications that do not have access to Windows Update:</span></span>

1.  <span data-ttu-id="341e1-130">Kopieren \\ Sie die Quellen \\ SxS \\ aus dem Image des bereitgestellten Betriebssystem-Build ISO in den Ordner dotnet35 oder einen ähnlichen Ordner</span><span class="sxs-lookup"><span data-stu-id="341e1-130">Copy \\sources\\sxs\\ from the mounted OS build ISO image to the dotnet35 or similar folder.</span></span> <span data-ttu-id="341e1-131">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="341e1-131">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="341e1-132">Legen Sie den RegKey fest:</span><span class="sxs-lookup"><span data-stu-id="341e1-132">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



<span data-ttu-id="341e1-133">**Für Unternehmen:**</span><span class="sxs-lookup"><span data-stu-id="341e1-133">**For enterprises:**</span></span>

<span data-ttu-id="341e1-134">Für Computer, die für die Verwendung von WSUS für die Wartung konfiguriert sind, können Sie einen Registrierungs Eintrag festlegen, um zuzulassen, dass der Computer Windows Update für die Aktivierung von .NET 3,5 anstelle von WSUS verwendet (wenn Sie dies tun), erfolgt die Wartung weiterhin von WSUS.</span><span class="sxs-lookup"><span data-stu-id="341e1-134">For machines that are configured to use WSUS for servicing, you can set a registry entry to allow the machine to use Windows Update for enabling .NET 3.5 instead of WSUS (servicing will still be done from WSUS if you do this).</span></span>

-   <span data-ttu-id="341e1-135">Legen Sie den RegKey fest:</span><span class="sxs-lookup"><span data-stu-id="341e1-135">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



<span data-ttu-id="341e1-136">Dieser Registrierungs Eintrag kann auch über Gruppenrichtlinie (lokale Computer Richtlinie > Computerkonfiguration-> administrative Vorlagen-> System festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="341e1-136">This registry entry can also be set via Group Policy (Local Computer Policy -> Computer Configuration -> Administrative Templates -> System.</span></span> <span data-ttu-id="341e1-137">Wählen Sie die Einstellung Einstellungen für die Installation optionaler Komponenten und die Reparatur von Komponenten angeben aus.</span><span class="sxs-lookup"><span data-stu-id="341e1-137">Select the setting  Specify settings for optional component installation and component repair .</span></span>

<span data-ttu-id="341e1-138">Wenn Sie die Option Kontakt Windows Update direkt zum Herunterladen von Reparatur Inhalt anstelle von Windows Server Update Services (WSUS) auswählen, werden bei jedem Versuch, Windows-Features hinzuzufügen (z. b. .NET Framework 3,5) oder Reparatur Features, Dateidownloads aus Windows Update auslöst.</span><span class="sxs-lookup"><span data-stu-id="341e1-138">If you select  Contact Windows Update directly to download repair content instead of Windows Server Update Services (WSUS) , any attempts to add Windows features (for example, .NET Framework 3.5) or repair features will trigger file downloads from Windows Update.</span></span> <span data-ttu-id="341e1-139">Zielcomputer benötigen Internet-und Wu-Zugriff für diese Option.</span><span class="sxs-lookup"><span data-stu-id="341e1-139">Target computers require Internet and WU access for this option.</span></span> <span data-ttu-id="341e1-140">Bei normalen Wartungs Vorgängen wird WSUS weiterhin verwendet, wenn es als Quelle konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="341e1-140">Normal servicing operations continue to use WSUS if it has been configured as a source.</span></span>

<span data-ttu-id="341e1-141">**Hinweis zum Festlegen des lokalen Quell Speicher Orts über Registrierungseinträge**</span><span class="sxs-lookup"><span data-stu-id="341e1-141">**A note regarding setting local source location via registry entries**</span></span>

<span data-ttu-id="341e1-142">IT-Administratoren können lokale Quell Speicherorte für .NET 3,5-Dateien mithilfe eines Registrierungs Eintrags festlegen, sodass Benutzer das Dialogfeld "Windows-Funktionen hinzufügen/entfernen" verwenden können, um Funktionen mit fehlender Nutzlast zu aktivieren, ohne einen Quell Speicherort angeben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="341e1-142">IT administrators can set local source location(s) for .NET 3.5 files via a registry entry, so that users can use the Add/Remove Windows Features dialog to enable features with missing payload without having to specify a source location.</span></span> <span data-ttu-id="341e1-143">Der Wert des Registrierungs Eintrags kann über eine Gruppenrichtlinie gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="341e1-143">The value of the registry entry can be controlled via group policy.</span></span>

<span data-ttu-id="341e1-144">Dieser Registrierungs Eintrag wird unterstützt:</span><span class="sxs-lookup"><span data-stu-id="341e1-144">This registry entry is supported:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="341e1-145">Eingabe</span><span class="sxs-lookup"><span data-stu-id="341e1-145">Entry</span></span></th>
<th><span data-ttu-id="341e1-146">type</span><span class="sxs-lookup"><span data-stu-id="341e1-146">Type</span></span></th>
<th><span data-ttu-id="341e1-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="341e1-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="341e1-148">Lokaler Quellpfad</span><span class="sxs-lookup"><span data-stu-id="341e1-148">Local Source Path</span></span></td>
<td><span data-ttu-id="341e1-149">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="341e1-149">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="341e1-150">Lokale Quell Pfade, die standardmäßig verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="341e1-150">Local source path(s) to be used by default.</span></span> <span data-ttu-id="341e1-151">Es können mehrere Pfade angegeben werden. Sie sollten durch, getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="341e1-151">Multiple paths can be specified; they should be separated by  ; .</span></span> <span data-ttu-id="341e1-152">Standorte werden in der Reihenfolge durchsucht, in der Sie angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="341e1-152">Locations will be searched in the order they are specified.</span></span> <br/> <span data-ttu-id="341e1-153">Lokale Quell Standorte, die in der Befehlszeile des Befehlszeile angegeben sind, haben Vorrang vor den in diesem Registrierungs Eintrag angegebenen Positionen.</span><span class="sxs-lookup"><span data-stu-id="341e1-153">Local source location(s) that are specified on the DISM command line, take precedence over locations specified in this registry entry.</span></span> <span data-ttu-id="341e1-154">Ordner Speicherorte können in diesem Registrierungs Eintrag angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="341e1-154">Folder locations can be specified in this registry entry.</span></span> <br/> <span data-ttu-id="341e1-155">Wims können verwendet werden, aber der Pfad muss in die WIM-Datei gesetzt werden. Es ist nicht erforderlich, es zu installieren, z. b.:</span><span class="sxs-lookup"><span data-stu-id="341e1-155">WIMs can be used, but the path must be to the WIM file; there is no need to mount it, for example:</span></span> <br/> <dl> <span data-ttu-id="341e1-156">Wim: \\ machine\share\file.Wim: 1</span><span class="sxs-lookup"><span data-stu-id="341e1-156">wim:\\machine\share\file.wim:1</span></span><br />
</dl> <span data-ttu-id="341e1-157">Beachten Sie den 1 am Ende.</span><span class="sxs-lookup"><span data-stu-id="341e1-157">Notice the  1  at the end.</span></span> <span data-ttu-id="341e1-158">Sie müssen den numerischen Index des Abbilds angeben, das Sie in der WIM-Datei verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="341e1-158">You must specify the numerical index of the image you want to use in the WIM file.</span></span> <br/> <span data-ttu-id="341e1-159">Bei einer bereitgestellten WIM muss der Quellpfad auf das Windows-Verzeichnis des bereitgestellten Images statt auf den Einfügepunkt verweisen (z. b.:/Source: <mount_point> \Windows anstelle von/Source: <mount_point> ).</span><span class="sxs-lookup"><span data-stu-id="341e1-159">For a mounted WIM, the source path needs to refer to the windows directory of the mounted image, rather than to the mount point (for example: /source:<mount_point>\windows rather than /source:<mount_point>).</span></span> <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a><span data-ttu-id="341e1-160">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="341e1-160">Resources</span></span>

<dl>

[<span data-ttu-id="341e1-161">Implementieren der Registrierungs basierten Richtlinie</span><span class="sxs-lookup"><span data-stu-id="341e1-161">Implementing Registry-based Policy</span></span>](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>