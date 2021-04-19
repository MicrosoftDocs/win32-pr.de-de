---
title: Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps
description: Verwenden Sie diese Vorschläge, um Probleme zu beheben, die beim Packen, bereitstellen oder Abfragen eines App-Pakets auftreten.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/25/2021
ms.locfileid: "106372785"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a><span data-ttu-id="685b5-103">Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps</span><span class="sxs-lookup"><span data-stu-id="685b5-103">Troubleshooting packaging, deployment, and query of Windows apps</span></span>

<span data-ttu-id="685b5-104">Verwenden Sie diese Vorschläge, um Probleme zu beheben, die beim Packen, bereitstellen oder Abfragen eines Windows-App-Pakets (. msix/. AppX) als Entwickler auftreten.</span><span class="sxs-lookup"><span data-stu-id="685b5-104">Use these suggestions to troubleshoot problems you experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer.</span></span>

> [!NOTE]
> <span data-ttu-id="685b5-105">Dieser Artikel richtet sich an Entwickler.</span><span class="sxs-lookup"><span data-stu-id="685b5-105">This article is intended for developers.</span></span> <span data-ttu-id="685b5-106">Wenn Sie kein Entwickler sind und Hilfe bei der Installation einer Windows-App suchen, finden Sie weitere Informationen unter [Windows-Support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span><span class="sxs-lookup"><span data-stu-id="685b5-106">If you are not a developer and you are looking for help with a Windows app installation error, see [Windows support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span></span>

## <a name="get-diagnostic-information"></a><span data-ttu-id="685b5-107">Diagnoseinformationen erhalten</span><span class="sxs-lookup"><span data-stu-id="685b5-107">Get diagnostic information</span></span>

<span data-ttu-id="685b5-108">Wenn eine API fehlschlägt, wird ein Fehlercode zurückgegeben, der das Problem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="685b5-108">When an API fails, it returns an error code that describes the problem.</span></span> <span data-ttu-id="685b5-109">Wenn der Fehlercode nicht genügend Informationen liefert, finden Sie weitere Diagnoseinformationen in den detaillierten Ereignisprotokollen.</span><span class="sxs-lookup"><span data-stu-id="685b5-109">If the error code doesn't provide enough information, you find more diagnostic information in the detailed event logs.</span></span>

<span data-ttu-id="685b5-110">Führen Sie die folgenden Schritte aus, um mit **Ereignisanzeige** auf die Paket-und Bereitstellungs Ereignisprotokolle zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="685b5-110">To access the packaging and deployment event logs by using **Event Viewer**, follow these steps:</span></span>

1. <span data-ttu-id="685b5-111">Führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="685b5-111">Perform one of the following steps:</span></span>

    * <span data-ttu-id="685b5-112">Klicken Sie im Menü Windows auf **Start** , geben Sie **Ereignisanzeige** ein, und **drücken Sie die EINGABETASTE**.</span><span class="sxs-lookup"><span data-stu-id="685b5-112">Click **Start** on the Windows menu, type **Event Viewer**, and **press Enter**.</span></span>
    * <span data-ttu-id="685b5-113">Führen Sie **eventvwr. msc** aus.</span><span class="sxs-lookup"><span data-stu-id="685b5-113">Run **eventvwr.msc**.</span></span>

2. <span data-ttu-id="685b5-114">Erweitern Sie auf der linken Seite **Ereignisanzeige (local)**  >  **Anwendungs-und Dienst Protokolle**  >  **Microsoft**  >  **Windows**.</span><span class="sxs-lookup"><span data-stu-id="685b5-114">In the left page, expand **Event Viewer (Local)** > **Applications and Services Logs** > **Microsoft** > **Windows**.</span></span>
3. <span data-ttu-id="685b5-115">Überprüfen Sie die verfügbaren Protokolle in den folgenden Kategorien:</span><span class="sxs-lookup"><span data-stu-id="685b5-115">Check for available logs under these categories:</span></span>

    * <span data-ttu-id="685b5-116">**Appxpackagingom**  >  **Microsoft-Windows-appxpackaging/Operational**</span><span class="sxs-lookup"><span data-stu-id="685b5-116">**AppxPackagingOM** > **Microsoft-Windows-AppxPackaging/Operational**</span></span>
    * <span data-ttu-id="685b5-117">**Appxdeployment-Server**  >  **Microsoft-Windows-appxdeploymentserver/Operational**</span><span class="sxs-lookup"><span data-stu-id="685b5-117">**AppXDeployment-Server** > **Microsoft-Windows-AppXDeploymentServer/Operational**</span></span>

<span data-ttu-id="685b5-118">Sehen Sie sich zunächst die Protokolle unter **appxdeployment-Server** an.</span><span class="sxs-lookup"><span data-stu-id="685b5-118">Start by looking at the logs under **AppXDeployment-Server**.</span></span> <span data-ttu-id="685b5-119">Wenn der Fehler durch **0x80073cf0** oder **ERROR_INSTALL_OPEN_PACKAGE_FAILED** verursacht wurde, sind möglicherweise weitere Details in den **appxpackagingom** -Protokollen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="685b5-119">If the error was caused by **0x80073CF0** or **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, additional details may be present in the **AppxpackagingOM** logs.</span></span>

<span data-ttu-id="685b5-120">Sie können auch den Befehl [Get-appxlog](/powershell/module/appx/get-appxlog) in PowerShell verwenden, um die ersten protokollierten Ereignisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="685b5-120">You can also use the [Get-AppxLog](/powershell/module/appx/get-appxlog) command in PowerShell to get the first few logged events.</span></span> <span data-ttu-id="685b5-121">Im folgenden Beispiel werden die dem letzten Bereitstellungs Vorgang zugeordneten Protokolle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="685b5-121">The following example displays the logs associated with the most recent deployment operation.</span></span>

```PowerShell
Get-Appxlog
```

<span data-ttu-id="685b5-122">Im folgenden Beispiel werden die Protokolle angezeigt, die dem letzten Bereitstellungs Vorgang in einer interaktiven Tabelle in einem separaten Fenster zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="685b5-122">The following example displays the logs associated with the most recent deployment operation in an interactive table in a separate window.</span></span>

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a><span data-ttu-id="685b5-123">Häufige Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="685b5-123">Common error codes</span></span>

<span data-ttu-id="685b5-124">In dieser Tabelle sind einige der häufigsten Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="685b5-124">This table lists some of the most common error codes.</span></span> <span data-ttu-id="685b5-125">Wenn Sie bei einem dieser Fehler weitere Hilfe benötigen oder wenn Sie einen Fehlercode finden, der nicht in dieser Liste enthalten ist, finden Sie weitere Informationen unter [zusätzliche Hilfe Optionen](#get-additional-help).</span><span class="sxs-lookup"><span data-stu-id="685b5-125">If you need further help with one of these errors, or if you're encountering an error code not in this list, see [additional help options](#get-additional-help).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="685b5-126">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="685b5-126">Error code</span></span></th>
<th><span data-ttu-id="685b5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="685b5-127">Value</span></span></th>
<th><span data-ttu-id="685b5-128">Beschreibung und mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="685b5-128">Description and possible causes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><span data-ttu-id="685b5-129"><strong>E_FILENOTFOUND</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-129"><strong>E_FILENOTFOUND</strong></span></span></td>
<td><span data-ttu-id="685b5-130">0x80070002</span><span class="sxs-lookup"><span data-stu-id="685b5-130">0x80070002</span></span></td>
<td><span data-ttu-id="685b5-131">Datei oder Pfad nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="685b5-131">File or path is not found.</span></span> <span data-ttu-id="685b5-132">Dies kann während einer com-Export der Typbibliothek-Validierung vorkommen, dass der Pfad für das Verzeichnis tatsächlich in Ihrem msix-Paket vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-132">This can occur during a COM  typelib validation requires that the path for the directory actually exist within your MSIX package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-133"><strong>ERROR_BAD_FORMAT</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-133"><strong>ERROR_BAD_FORMAT</strong></span></span></td>
<td><span data-ttu-id="685b5-134">0x8007000B</span><span class="sxs-lookup"><span data-stu-id="685b5-134">0x8007000B</span></span></td>
<td><span data-ttu-id="685b5-135">Das Paket ist nicht ordnungsgemäß formatiert und muss neu erstellt oder neu signiert werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-135">The package isn't correctly formatted and needs to be re-built or re-signed.</span></span><br/> <span data-ttu-id="685b5-136">Dieser Fehler kann auftreten, wenn der Antragsteller Name des Signatur Zertifikats und der Name des AppxManifest.xml Verlegers nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="685b5-136">You may get this error if there is a mismatch between the signing certificate subject name and the AppxManifest.xml publisher name.</span></span><br/> <span data-ttu-id="685b5-137">Weitere Informationen finden <a href="how-to-sign-a-package-using-signtool.md">Sie unter Signieren eines App-Pakets mit SignTool</a>.</span><span class="sxs-lookup"><span data-stu-id="685b5-137">See <a href="how-to-sign-a-package-using-signtool.md">How to sign an app package using SignTool</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-138"><strong>E_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-138"><strong>E_INVALIDARG</strong></span></span></td>
<td><span data-ttu-id="685b5-139">0x80070057</span><span class="sxs-lookup"><span data-stu-id="685b5-139">0x80070057</span></span></td>
<td><span data-ttu-id="685b5-140">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-140">One or more arguments are not valid.</span></span> <span data-ttu-id="685b5-141">Wenn Sie das AppXDeployment-Server-Ereignisprotokoll überprüfen und folgendes Ereignis sehen: "beim Installieren des Pakets konnte die Windows. repositoryExtension-Erweiterung aufgrund des folgenden Fehlers nicht registriert werden: der Parameter ist falsch."</span><span class="sxs-lookup"><span data-stu-id="685b5-141">If you check the AppXDeployment-Server event log and see the following event: "While installing the package, the system failed to register the windows.repositoryExtension extension due to the following error: The parameter is incorrect."</span></span> <br/> <span data-ttu-id="685b5-142">Dieser Fehler wird möglicherweise angezeigt, wenn die Elemente Display Name oder Description des Manifests Zeichen enthalten, die von der Windows-Firewall nicht zugelassen werden. nämlich |  und alle, da Windows das appcontainer-Profil für das Paket nicht erstellen konnte.</span><span class="sxs-lookup"><span data-stu-id="685b5-142">You may get this error if the manifest elements DisplayName or Description contain characters disallowed by Windows firewall; namely  |  and  all , due to which Windows fails to create the AppContainer profile for the package.</span></span> <span data-ttu-id="685b5-143">Entfernen Sie diese Zeichen aus dem Manifest, und versuchen Sie, das Paket zu installieren.</span><span class="sxs-lookup"><span data-stu-id="685b5-143">Please remove these characters from the manifest and try installing the package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-144"><strong>ERROR_INSTALL_OPEN_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-144"><strong>ERROR_INSTALL_OPEN_</strong></span></span><br/> <span data-ttu-id="685b5-145"><strong>PACKAGE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-145"><strong>PACKAGE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-146">0x80073CF0</span><span class="sxs-lookup"><span data-stu-id="685b5-146">0x80073CF0</span></span></td>
<td><span data-ttu-id="685b5-147">Das Paket konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-147">The package couldn't be opened.</span></span><br/> <span data-ttu-id="685b5-148">Mögliche Ursachen:</span><span class="sxs-lookup"><span data-stu-id="685b5-148">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="685b5-149">Das Paket ist nicht signiert.</span><span class="sxs-lookup"><span data-stu-id="685b5-149">The package is unsigned.</span></span></li>
<li><span data-ttu-id="685b5-150">Der Herausgeber Name stimmt nicht mit dem Signaturzertifikat Betreff.</span><span class="sxs-lookup"><span data-stu-id="685b5-150">The publisher name doesn't match the signing certificate subject.</span></span></li>
<li><span data-ttu-id="685b5-151">Das file://-Präfix fehlt, oder das Paket wurde am angegebenen Speicherort nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="685b5-151">The file:// prefix is missing or the package couldn't be found at the specified location.</span></span></li>
</ul>
<span data-ttu-id="685b5-152">Weitere Informationen finden Sie im Ereignisprotokoll " <strong>appxpackagingom</strong> ".</span><span class="sxs-lookup"><span data-stu-id="685b5-152">For more information, check the <strong>AppxPackagingOM</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span></span><br/> <span data-ttu-id="685b5-154"><strong>NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-154"><strong>NOT_FOUND</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-155">0x80073cf1</span><span class="sxs-lookup"><span data-stu-id="685b5-155">0x80073CF1</span></span></td>
<td><span data-ttu-id="685b5-156">Das Paket wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="685b5-156">The package couldn't be found.</span></span><br/> <span data-ttu-id="685b5-157">Dieser Fehler wird möglicherweise angezeigt, wenn Sie ein Paket entfernen, das nicht für den aktuellen Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-157">You may get this error while removing a package that isn't installed for the current user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-158"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-158"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-159"><strong>Paketen</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-159"><strong>PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-160">0x80073cf2</span><span class="sxs-lookup"><span data-stu-id="685b5-160">0x80073CF2</span></span></td>
<td><span data-ttu-id="685b5-161">Die Paketdaten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-161">The package data isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span></span><br/> <span data-ttu-id="685b5-163"><strong>DEPENDENCY_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-163"><strong>DEPENDENCY_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-164">0x80073CF3</span><span class="sxs-lookup"><span data-stu-id="685b5-164">0x80073CF3</span></span></td>
<td><span data-ttu-id="685b5-165">Fehler bei Updates, Abhängigkeiten oder Konfliktüberprüfung des Pakets.</span><span class="sxs-lookup"><span data-stu-id="685b5-165">The package failed update, dependency, or conflict validation.</span></span><br/> <span data-ttu-id="685b5-166">Mögliche Ursachen:</span><span class="sxs-lookup"><span data-stu-id="685b5-166">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="685b5-167">Das eingehende Paket ist mit einem installierten Paket nicht vereinbar.</span><span class="sxs-lookup"><span data-stu-id="685b5-167">The incoming package conflicts with an installed package.</span></span></li>
<li><span data-ttu-id="685b5-168">Eine angegebene Paketabhängigkeit wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="685b5-168">A specified package dependency can't be found.</span></span></li>
<li><span data-ttu-id="685b5-169">Das Paket unterstützt nicht die richtige Prozessorarchitektur.</span><span class="sxs-lookup"><span data-stu-id="685b5-169">The package doesn't support the correct processor architecture.</span></span></li>
</ul>
<span data-ttu-id="685b5-170">Überprüfen Sie das Ereignisprotokoll " <strong>appxdeployment-Server</strong> ", um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="685b5-170">For more informtion, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-171"><strong>ERROR_INSTALL_OUT_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-171"><strong>ERROR_INSTALL_OUT_</strong></span></span><br/> <span data-ttu-id="685b5-172"><strong>OF_DISK_SPACE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-172"><strong>OF_DISK_SPACE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-173">0x80073cf4</span><span class="sxs-lookup"><span data-stu-id="685b5-173">0x80073CF4</span></span></td>
<td><span data-ttu-id="685b5-174">Auf Ihrem Computer ist nicht genügend Speicherplatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="685b5-174">There isn't enough disk space on your computer.</span></span> <span data-ttu-id="685b5-175">Freigeben Sie Speicherplatz, und versuchen Sie es noch mal.</span><span class="sxs-lookup"><span data-stu-id="685b5-175">Free some space and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-176"><strong>ERROR_INSTALL_NETWORK_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-176"><strong>ERROR_INSTALL_NETWORK_</strong></span></span><br/> <span data-ttu-id="685b5-177"><strong>Fehler</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-177"><strong>FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-178">0x80073cf5</span><span class="sxs-lookup"><span data-stu-id="685b5-178">0x80073CF5</span></span></td>
<td><span data-ttu-id="685b5-179">Das Paket kann nicht heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-179">The package can't be downloaded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-180"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-180"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="685b5-181"><strong>REGISTRATION_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-181"><strong>REGISTRATION_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-182">0x80073cf6</span><span class="sxs-lookup"><span data-stu-id="685b5-182">0x80073CF6</span></span></td>
<td><span data-ttu-id="685b5-183">Das Paket kann nicht registriert werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-183">The package can't be registered.</span></span><br/> <span data-ttu-id="685b5-184">Weitere Informationen finden Sie im Ereignisprotokoll " <strong>appxdeployment-Server</strong> ".</span><span class="sxs-lookup"><span data-stu-id="685b5-184">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-185"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-185"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="685b5-186"><strong>DEREGISTRATION_EFAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-186"><strong>DEREGISTRATION_EFAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-187">0x80073cf7</span><span class="sxs-lookup"><span data-stu-id="685b5-187">0x80073CF7</span></span></td>
<td><span data-ttu-id="685b5-188">Die Registrierung des Pakets kann nicht aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-188">The package can't be unregistered.</span></span><br/> <span data-ttu-id="685b5-189">Dieser Fehler kann beim Entfernen eines Pakets auftreten.</span><span class="sxs-lookup"><span data-stu-id="685b5-189">You may get this error while removing a package.</span></span><br/> <span data-ttu-id="685b5-190">Weitere Informationen finden Sie im Ereignisprotokoll " <strong>appxdeployment-Server</strong> ".</span><span class="sxs-lookup"><span data-stu-id="685b5-190">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-191"><strong>ERROR_INSTALL_CANCEL</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-191"><strong>ERROR_INSTALL_CANCEL</strong></span></span></td>
<td><span data-ttu-id="685b5-192">0x80073cf8</span><span class="sxs-lookup"><span data-stu-id="685b5-192">0x80073CF8</span></span></td>
<td><span data-ttu-id="685b5-193">Der Benutzer hat die Installations Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="685b5-193">The user canceled the install request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-194"><strong>ERROR_INSTALL_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-194"><strong>ERROR_INSTALL_FAILED</strong></span></span></td>
<td><span data-ttu-id="685b5-195">0x80073cf9</span><span class="sxs-lookup"><span data-stu-id="685b5-195">0x80073CF9</span></span></td>
<td><span data-ttu-id="685b5-196">Fehler beim Installieren des Pakets.</span><span class="sxs-lookup"><span data-stu-id="685b5-196">Package install failed.</span></span> <span data-ttu-id="685b5-197">Wenden Sie sich an den Softwarehersteller.</span><span class="sxs-lookup"><span data-stu-id="685b5-197">Contact the software vendor.</span></span><br/> <span data-ttu-id="685b5-198">Weitere Informationen finden Sie im Ereignisprotokoll " <strong>appxdeployment-Server</strong> ".</span><span class="sxs-lookup"><span data-stu-id="685b5-198">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-199"><strong>ERROR_REMOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-199"><strong>ERROR_REMOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="685b5-200">0x80073cfa</span><span class="sxs-lookup"><span data-stu-id="685b5-200">0x80073CFA</span></span></td>
<td><span data-ttu-id="685b5-201">Fehler beim Entfernen des Pakets.</span><span class="sxs-lookup"><span data-stu-id="685b5-201">Package removal failed.</span></span><br/> <span data-ttu-id="685b5-202">Dieser Fehler tritt möglicherweise für Fehler auf, die während der Paket Deinstallation auftreten.</span><span class="sxs-lookup"><span data-stu-id="685b5-202">You may get this error for failures that occur during package uninstall.</span></span><br/> <span data-ttu-id="685b5-203">Weitere Informationen finden Sie unter <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>removepackageasync</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="685b5-203">For more information, see <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-204"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-204"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="685b5-205"><strong>ALREADY_EXISTS</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-205"><strong>ALREADY_EXISTS</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-206">0x80073CFB</span><span class="sxs-lookup"><span data-stu-id="685b5-206">0x80073CFB</span></span></td>
<td><span data-ttu-id="685b5-207">Das bereitgestellte Paket ist bereits installiert, und eine erneute Installation des Pakets wird blockiert.</span><span class="sxs-lookup"><span data-stu-id="685b5-207">The provided package is already installed, and reinstallation of the package is blocked.</span></span> <br/> <span data-ttu-id="685b5-208">Dieser Fehler wird möglicherweise angezeigt, wenn Sie ein Paket installieren, das nicht bitweise mit dem bereits installierten Paket identisch ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-208">You may get this error if installing a package that is not bitwise identical to the package that is already installed.</span></span> <span data-ttu-id="685b5-209">Beachten Sie, dass die digitale Signatur auch Teil des Pakets ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-209">Note that the digital signature is also part of the package.</span></span> <span data-ttu-id="685b5-210">Wenn ein Paket neu erstellt oder zurückgetreten wird, ist es daher nicht mehr bitweise identisch mit dem zuvor installierten Paket.</span><span class="sxs-lookup"><span data-stu-id="685b5-210">Hence if a package is rebuilt or resigned, it is no longer bitwise identical to the previously installed package.</span></span> <span data-ttu-id="685b5-211">Es gibt zwei Möglichkeiten, diesen Fehler zu beheben: (1) Inkrementieren Sie die Versionsnummer der APP, erstellen Sie das Paket neu, und setzen Sie es ab (2) entfernen Sie das alte Paket für jeden Benutzer im System, bevor Sie das neue Paket installieren.</span><span class="sxs-lookup"><span data-stu-id="685b5-211">Two possible options to fix this error are: (1) Increment the version number of the app, then rebuild and resign the package (2) Remove the old package for every user on the system before installing the new package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span></span></td>
<td><span data-ttu-id="685b5-213">0x80073cfc</span><span class="sxs-lookup"><span data-stu-id="685b5-213">0x80073CFC</span></span></td>
<td><span data-ttu-id="685b5-214">Die APP kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-214">The app can't be started.</span></span> <span data-ttu-id="685b5-215">Versuchen Sie, die APP erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="685b5-215">Try reinstalling the app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-216"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-216"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="685b5-217"><strong>PREREQUISITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-217"><strong>PREREQUISITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-218">0x80073cfd</span><span class="sxs-lookup"><span data-stu-id="685b5-218">0x80073CFD</span></span></td>
<td><span data-ttu-id="685b5-219">Eine angegebene Installations Voraussetzung konnte nicht erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-219">A specified install prerequisite couldn't be satisfied.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-220"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-220"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="685b5-221"><strong>REPOSITORY_CORRUPTED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-221"><strong>REPOSITORY_CORRUPTED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-222">0x80073cfe</span><span class="sxs-lookup"><span data-stu-id="685b5-222">0x80073CFE</span></span></td>
<td><span data-ttu-id="685b5-223">Das Paketrepository ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="685b5-223">The package repository is corrupted.</span></span><br/> <span data-ttu-id="685b5-224">Dieser Fehler kann angezeigt werden, wenn der Ordner, auf den dieser Registrierungsschlüssel verweist, nicht vorhanden oder beschädigt ist:</span><span class="sxs-lookup"><span data-stu-id="685b5-224">You may get this error if the folder referenced by this registry key doesn't exist or is corrupted:</span></span> <br/> <span data-ttu-id="685b5-225"><strong>HKLM\Software\Microsoft\Windows</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-225"><strong>HKLM\Software\Microsoft\Windows\</strong></span></span><br/> <span data-ttu-id="685b5-226"><strong>Currentversion\appx\packagerepositorienroot</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span></span><br/> <span data-ttu-id="685b5-227">Aktualisieren Sie Ihren PC, um diesen Status wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="685b5-227">To recover from this state, refresh your PC.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-228"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-228"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="685b5-229"><strong>POLICY_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-229"><strong>POLICY_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-230">0x80073CFF</span><span class="sxs-lookup"><span data-stu-id="685b5-230">0x80073CFF</span></span></td>
<td><span data-ttu-id="685b5-231">Zum Installieren dieser APP benötigen Sie eine Entwicklerlizenz oder ein Sideload-fähiges System.</span><span class="sxs-lookup"><span data-stu-id="685b5-231">To install this app, you need a developer license or a sideloading-enabled system.</span></span> <br/> <span data-ttu-id="685b5-232">Dieser Fehler kann auftreten, wenn das Paket nicht eine der folgenden Anforderungen erfüllt:</span><span class="sxs-lookup"><span data-stu-id="685b5-232">You may get this error if the package doesn't meet one of the following requirements:</span></span><br/>
<ul>
<li><span data-ttu-id="685b5-233">Die APP wird mit F5 in Visual Studio auf einem Computer mit einer Windows-Entwicklerlizenz bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="685b5-233">The app is deployed using F5 in Visual Studio on a computer with a Windows developer license.</span></span></li>
<li><span data-ttu-id="685b5-234">Das Paket wird mit einer Microsoft-Signatur signiert und als Teil von Windows oder im Microsoft Store bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="685b5-234">The package is signed with a Microsoft signature and deployed as part of Windows or from the Microsoft Store.</span></span></li>
<li><span data-ttu-id="685b5-235">Das Paket wird mit einer vertrauenswürdigen Signatur signiert und auf einem Computer installiert, auf dem eine Entwicklerlizenz, ein in die Domäne eingebundener Computer mit der Richtlinie "zukerwallvertrauensatpps" aktiviert ist, oder ein Computer mit einer Windows-Sideload-Lizenz mit aktivierter Richtlinie "Zuordners"</span><span class="sxs-lookup"><span data-stu-id="685b5-235">The package is signed with a trusted signature and installed on a computer with a developer license, a domain-joined computer with the AllowAllTrustedApps policy enabled, or a computer with a Windows Sideloading license with the AllowAllTrustedApps policy enabled.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-236"><strong>ERROR_PACKAGE_UPDATING</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-236"><strong>ERROR_PACKAGE_UPDATING</strong></span></span></td>
<td><span data-ttu-id="685b5-237">0x80073d00</span><span class="sxs-lookup"><span data-stu-id="685b5-237">0x80073D00</span></span></td>
<td><span data-ttu-id="685b5-238">Die APP kann nicht gestartet werden, da Sie zurzeit aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="685b5-238">The app can't be started because it's currently updating.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-239"><strong>ERROR_DEPLOYMENT_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-239"><strong>ERROR_DEPLOYMENT_</strong></span></span><br/> <span data-ttu-id="685b5-240"><strong>BLOCKED_BY_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-240"><strong>BLOCKED_BY_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-241">0x80073d01</span><span class="sxs-lookup"><span data-stu-id="685b5-241">0x80073D01</span></span></td>
<td><span data-ttu-id="685b5-242">Der Paket Bereitstellungs Vorgang wird durch die Richtlinie blockiert.</span><span class="sxs-lookup"><span data-stu-id="685b5-242">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="685b5-243">Wenden Sie sich an Ihren Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="685b5-243">Contact your system administrator.</span></span><br/> <span data-ttu-id="685b5-244">Mögliche Ursachen:</span><span class="sxs-lookup"><span data-stu-id="685b5-244">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="685b5-245">Die Paket Bereitstellung wird durch Anwendungs Steuerungs Richtlinien blockiert.</span><span class="sxs-lookup"><span data-stu-id="685b5-245">Package deployment is blocked by Application Control Policies.</span></span></li>
<li><span data-ttu-id="685b5-246">Die Paket Bereitstellung wird durch die &quot; Richtlinie Bereitstellung von Vorgängen in speziellen Profilen zulassen blockiert &quot; .</span><span class="sxs-lookup"><span data-stu-id="685b5-246">Package deployment is blocked by the &quot;Allow deployment operations in special profiles&quot; policy.</span></span></li>
</ul>
<span data-ttu-id="685b5-247">Einer der möglichen Gründe ist die Notwendigkeit eines roamingprofils.</span><span class="sxs-lookup"><span data-stu-id="685b5-247">One of the possible reasons is a need for a roaming profile.</span></span> <span data-ttu-id="685b5-248">Informationen zum Einrichten Roamingbenutzerprofile für Benutzerkonten finden Sie unter Bereitstellen von <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Roamingbenutzerprofilen</a>.</span><span class="sxs-lookup"><span data-stu-id="685b5-248">For information about setting up Roaming User Profiles on user accounts, see <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Deploy Roaming User Profiles</a>.</span></span> <span data-ttu-id="685b5-249">Wenn auf Ihrem System keine Richtlinien konfiguriert sind und dieser Fehler weiterhin angezeigt wird, sind Sie möglicherweise mit einem temporären Profil angemeldet.</span><span class="sxs-lookup"><span data-stu-id="685b5-249">If there are no policies configured on your system and you still see this error, perhaps you are logged in with a temporary profile.</span></span> <span data-ttu-id="685b5-250">Melden Sie sich ab, und melden Sie sich erneut an. Wiederholen Sie dann den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="685b5-250">Log out and log in again, then try the operation again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-251"><strong>ERROR_PACKAGES_IN_USE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-251"><strong>ERROR_PACKAGES_IN_USE</strong></span></span></td>
<td><span data-ttu-id="685b5-252">0x80073d02</span><span class="sxs-lookup"><span data-stu-id="685b5-252">0x80073D02</span></span></td>
<td><span data-ttu-id="685b5-253">Das Paket konnte nicht installiert werden, da die von ihm modifizierenden Ressourcen zurzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-253">The package couldn't be installed because resources it modifies are currently in use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-254"><strong>ERROR_RECOVERY_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-254"><strong>ERROR_RECOVERY_</strong></span></span><br/> <span data-ttu-id="685b5-255"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-255"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-256">0x80073d03</span><span class="sxs-lookup"><span data-stu-id="685b5-256">0x80073D03</span></span></td>
<td><span data-ttu-id="685b5-257">Das Paket konnte nicht wieder hergestellt werden, da für die Wiederherstellung erforderliche Daten beschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="685b5-257">The package couldn't be recovered because data that's necessary for recovery is corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-258"><strong>ERROR_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-258"><strong>ERROR_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-259"><strong>STAGED_SIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-259"><strong>STAGED_SIGNATURE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-260">0x80073d04</span><span class="sxs-lookup"><span data-stu-id="685b5-260">0x80073D04</span></span></td>
<td><span data-ttu-id="685b5-261">Die Signatur ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-261">The signature isn't valid.</span></span> <span data-ttu-id="685b5-262">Zum Registrieren im Entwicklermodus müssen appxsignature. P7X "und AppxBlockMap.xml gültig sein oder nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="685b5-262">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or shouldn't be present.</span></span><br/> <span data-ttu-id="685b5-263">Wenn Sie ein Entwickler sind, der mit Visual Studio F5 verwendet, stellen Sie sicher, dass Ihr erstelltes Projektverzeichnis keine Signatur-oder Blockierungs Dateien aus früheren Versionen des Pakets enthält.</span><span class="sxs-lookup"><span data-stu-id="685b5-263">If you are a developer using F5 with Visual Studio, ensure that your built project directory doesn't contain signature or block map files from previous versions of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-264"><strong>ERROR_DELETING_EXISTING_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-264"><strong>ERROR_DELETING_EXISTING_</strong></span></span><br/> <span data-ttu-id="685b5-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-266">0x80073d05</span><span class="sxs-lookup"><span data-stu-id="685b5-266">0x80073D05</span></span></td>
<td><span data-ttu-id="685b5-267">Beim Löschen der bereits vorhandenen Anwendungsdaten des Pakets ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="685b5-267">An error occurred while deleting the package's previously existing application data.</span></span><br/> <span data-ttu-id="685b5-268">Dieser Fehler kann angezeigt werden, wenn der <a href="/previous-versions/hh441475(v=vs.110)">Simulator</a> ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="685b5-268">You can get this error if the <a href="/previous-versions/hh441475(v=vs.110)">simulator</a> is running.</span></span> <span data-ttu-id="685b5-269">Schließen Sie den Simulator.</span><span class="sxs-lookup"><span data-stu-id="685b5-269">Close the simulator.</span></span> <span data-ttu-id="685b5-270">Dieser Fehler kann auch ausgegeben werden, wenn Dateien in den App-Daten geöffnet sind (wenn Sie z. b. eine Protokolldatei in einem Text-Editor geöffnet haben).</span><span class="sxs-lookup"><span data-stu-id="685b5-270">You can also get this error if there are files open in the app data (for example, if you have a log file open in a text editor).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-271"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-271"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="685b5-272"><strong>PACKAGE_DOWNGRADE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-272"><strong>PACKAGE_DOWNGRADE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-273">0x80073d06</span><span class="sxs-lookup"><span data-stu-id="685b5-273">0x80073D06</span></span></td>
<td><span data-ttu-id="685b5-274">Das Paket konnte nicht installiert werden, da bereits eine höhere Version dieses Pakets installiert ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-274">The package couldn't be installed because a higher version of this package is already installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-275"><strong>ERROR_SYSTEM_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-275"><strong>ERROR_SYSTEM_</strong></span></span><br/> <span data-ttu-id="685b5-276"><strong>NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-276"><strong>NEEDS_REMEDIATION</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-277">0x80073d07</span><span class="sxs-lookup"><span data-stu-id="685b5-277">0x80073D07</span></span></td>
<td><span data-ttu-id="685b5-278">Ein Fehler in einer System Binärdatei wurde erkannt.</span><span class="sxs-lookup"><span data-stu-id="685b5-278">An error in a system binary was detected.</span></span> <span data-ttu-id="685b5-279">Versuchen Sie, den PC zu aktualisieren, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="685b5-279">To fix the problem, try refreshing the PC.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-280"><strong>ERROR_APPX_INTEGRITY_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-280"><strong>ERROR_APPX_INTEGRITY_</strong></span></span><br/> <span data-ttu-id="685b5-281"><strong>FAILURE_EXTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-281"><strong>FAILURE_EXTERNAL</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-282">0x80073d08</span><span class="sxs-lookup"><span data-stu-id="685b5-282">0x80073D08</span></span></td>
<td><span data-ttu-id="685b5-283">Auf dem System wurde eine beschädigte nicht-Windows-Binärdatei erkannt.</span><span class="sxs-lookup"><span data-stu-id="685b5-283">A corrupted non-Windows binary was detected on the system.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-284"><strong>ERROR_RESILIENCY_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-284"><strong>ERROR_RESILIENCY_</strong></span></span><br/> <span data-ttu-id="685b5-285"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-285"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-286">0x80073d09</span><span class="sxs-lookup"><span data-stu-id="685b5-286">0x80073D09</span></span></td>
<td><span data-ttu-id="685b5-287">Der Vorgang konnte nicht fortgesetzt werden, da für die Wiederherstellung erforderliche Daten beschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="685b5-287">The operation couldn't be resumed because data that's necessary for recovery is corrupted.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span></span><br/> <span data-ttu-id="685b5-289"><strong>SERVICE_NOT_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-289"><strong>SERVICE_NOT_RUNNING</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-290">0x80073d0a</span><span class="sxs-lookup"><span data-stu-id="685b5-290">0x80073D0A</span></span></td>
<td><span data-ttu-id="685b5-291">Das Paket konnte nicht installiert werden, da der Windows-Firewall-Dienst nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="685b5-291">The package couldn't be installed because the Windows Firewall service isn't running.</span></span> <span data-ttu-id="685b5-292">Aktivieren Sie den Windows-Firewall-Dienst, und versuchen Sie es erneut</span><span class="sxs-lookup"><span data-stu-id="685b5-292">Enable the Windows Firewall service and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="685b5-294">0x80073d0b</span><span class="sxs-lookup"><span data-stu-id="685b5-294">0x80073D0B</span></span></td>
<td><span data-ttu-id="685b5-295">Fehler beim Verschieben des Pakets.</span><span class="sxs-lookup"><span data-stu-id="685b5-295">The package move operation failed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-296"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-296"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="685b5-297"><strong>NOT_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-297"><strong>NOT_EMPTY</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-298">0x80073d0c</span><span class="sxs-lookup"><span data-stu-id="685b5-298">0x80073D0C</span></span></td>
<td><span data-ttu-id="685b5-299">Der Bereitstellungs Vorgang ist fehlgeschlagen, da das Volume nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-299">The deployment operation failed because the volume is not empty.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-300"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-300"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="685b5-301"><strong>Aufzu</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-301"><strong>OFFLINE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-302">0x80073d0d</span><span class="sxs-lookup"><span data-stu-id="685b5-302">0x80073D0D</span></span></td>
<td><span data-ttu-id="685b5-303">Fehler beim Bereitstellungs Vorgang, weil das Volume offline ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-303">The deployment operation failed because the volume is offline.</span></span> <span data-ttu-id="685b5-304">Bei einem Paket Update verweist das Volume auf das installierte Volume aller Paketversionen.</span><span class="sxs-lookup"><span data-stu-id="685b5-304">For a package update, the volume refers to the installed volume of all package versions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-305"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-305"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="685b5-306"><strong>Kork</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-306"><strong>CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-307">0x80073d0e</span><span class="sxs-lookup"><span data-stu-id="685b5-307">0x80073D0E</span></span></td>
<td><span data-ttu-id="685b5-308">Der Bereitstellungs Vorgang ist fehlgeschlagen, da das angegebene Volume beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-308">The deployment operation failed because the specified volume is corrupt.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span></span><br/> <strong></strong><br/></td>
<td><span data-ttu-id="685b5-310">0x80073d0f</span><span class="sxs-lookup"><span data-stu-id="685b5-310">0x80073D0F</span></span></td>
<td><span data-ttu-id="685b5-311">Der Bereitstellungs Vorgang ist fehlgeschlagen, da die angegebene Anwendung zuerst registriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="685b5-311">The deployment operation failed because the specified application needs to be registered first.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-312"><strong>ERROR_INSTALL_WRONG_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-312"><strong>ERROR_INSTALL_WRONG_</strong></span></span><br/> <span data-ttu-id="685b5-313"><strong>PROCESSOR_ARCHITECTURE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-313"><strong>PROCESSOR_ARCHITECTURE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-314">0x80073d10</span><span class="sxs-lookup"><span data-stu-id="685b5-314">0x80073D10</span></span></td>
<td><span data-ttu-id="685b5-315">Der Bereitstellungs Vorgang ist fehlgeschlagen, weil das Paket die falsche Prozessorarchitektur als Ziel hat.</span><span class="sxs-lookup"><span data-stu-id="685b5-315">The deployment operation failed because the package targets the wrong processor architecture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-316"><strong>ERROR_DEV_SIDELOAD_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-316"><strong>ERROR_DEV_SIDELOAD_</strong></span></span><br/> <span data-ttu-id="685b5-317"><strong>LIMIT_EXCEEDED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-317"><strong>LIMIT_EXCEEDED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-318">0x80073d11</span><span class="sxs-lookup"><span data-stu-id="685b5-318">0x80073D11</span></span></td>
<td><span data-ttu-id="685b5-319">Sie haben die maximal zulässige Anzahl von Entwicklern, die auf diesem Gerät zulässig sind, erreicht.</span><span class="sxs-lookup"><span data-stu-id="685b5-319">You have reached the maximum number of developer sideloaded packages allowed on this device.</span></span> <span data-ttu-id="685b5-320">Deinstallieren Sie ein Sideload-Paket, und versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="685b5-320">Please uninstall a sideloaded package and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="685b5-322"><strong>PACKAGE_REQUIRES_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-322"><strong>PACKAGE_REQUIRES_</strong></span></span><br/> <span data-ttu-id="685b5-323"><strong>MAIN_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-323"><strong>MAIN_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-324">0x80073d12</span><span class="sxs-lookup"><span data-stu-id="685b5-324">0x80073D12</span></span></td>
<td><span data-ttu-id="685b5-325">Zum Installieren dieses optionalen Pakets ist ein Haupt-App-Paket erforderlich.</span><span class="sxs-lookup"><span data-stu-id="685b5-325">A main app package is required to install this optional package.</span></span> <span data-ttu-id="685b5-326">Installieren Sie zuerst das Hauptpaket, und wiederholen Sie den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="685b5-326">Install the main package first and try again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-327"><strong>ERROR_PACKAGE_NOT_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-327"><strong>ERROR_PACKAGE_NOT_</strong></span></span><br/> <span data-ttu-id="685b5-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-329">0x80073d13</span><span class="sxs-lookup"><span data-stu-id="685b5-329">0x80073D13</span></span></td>
<td><span data-ttu-id="685b5-330">Dieser APP-Pakettyp wird in diesem Dateisystem nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="685b5-330">This app package type is not supported on this filesystem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-331"><strong>ERROR_PACKAGE_MOVE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-331"><strong>ERROR_PACKAGE_MOVE_</strong></span></span><br/> <span data-ttu-id="685b5-332"><strong>BLOCKED_BY_STREAMING</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-332"><strong>BLOCKED_BY_STREAMING</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-333">0x80073d14</span><span class="sxs-lookup"><span data-stu-id="685b5-333">0x80073D14</span></span></td>
<td><span data-ttu-id="685b5-334">Der paketverschiebungs Vorgang wird blockiert, bis die Anwendung das Streaming abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="685b5-334">Package move operation is blocked until the application has finished streaming.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="685b5-336"><strong>PACKAGE_APPLICATIONID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-336"><strong>PACKAGE_APPLICATIONID_</strong></span></span><br/> <span data-ttu-id="685b5-337"><strong>NOT_UNIQUE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-337"><strong>NOT_UNIQUE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-338">0x80073d15</span><span class="sxs-lookup"><span data-stu-id="685b5-338">0x80073D15</span></span></td>
<td><span data-ttu-id="685b5-339">Ein Haupt-oder ein anderes optionales App-Paket verfügt über dieselbe Anwendungs-ID wie dieses optionale Paket.</span><span class="sxs-lookup"><span data-stu-id="685b5-339">A main or another optional app package has the same application ID as this optional package.</span></span> <span data-ttu-id="685b5-340">Ändern Sie die Anwendungs-ID für das optionale Paket, um Konflikte zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="685b5-340">Change the application ID for the optional package to avoid conflicts.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-341"><strong>ERROR_PACKAGE_STAGING_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-341"><strong>ERROR_PACKAGE_STAGING_</strong></span></span><br/> <span data-ttu-id="685b5-342"><strong>ONHOLD</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-342"><strong>ONHOLD</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-343">0x80073d16</span><span class="sxs-lookup"><span data-stu-id="685b5-343">0x80073D16</span></span></td>
<td><span data-ttu-id="685b5-344">Diese stagingsitzung wurde gespeichert, damit ein anderer stagingvorgang priorisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="685b5-344">This staging session has been held to allow another staging operation to be prioritized.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-345"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-345"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-346"><strong>RELATED_SET_UPDATE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-346"><strong>RELATED_SET_UPDATE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-347">0x80073d17</span><span class="sxs-lookup"><span data-stu-id="685b5-347">0x80073D17</span></span></td>
<td><span data-ttu-id="685b5-348">Ein zugehöriger Satz kann nicht aktualisiert werden, da der aktualisierte Satz ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-348">A related set cannot be updated because the updated set is invalid.</span></span> <span data-ttu-id="685b5-349">Alle Pakete in der zugehörigen Gruppe müssen gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-349">All packages in the related set must be updated at the same time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="685b5-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="685b5-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-353">0x80073d18</span><span class="sxs-lookup"><span data-stu-id="685b5-353">0x80073D18</span></span></td>
<td><span data-ttu-id="685b5-354">Ein optionales Paket mit einem FullTrust-Einstiegspunkt erfordert, dass das Hauptpaket über die Funktion " <strong>runfulltrust</strong> " verfügt.</span><span class="sxs-lookup"><span data-stu-id="685b5-354">An optional package with a FullTrust entry point requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="685b5-356"><strong>BY_USER_LOG_OFF</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-356"><strong>BY_USER_LOG_OFF</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-357">0x80073d19</span><span class="sxs-lookup"><span data-stu-id="685b5-357">0x80073D19</span></span></td>
<td><span data-ttu-id="685b5-358">Ein Fehler ist aufgetreten, da ein Benutzer abgemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="685b5-358">An error occurred because a user was logged off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="685b5-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="685b5-361"><strong>PACKAGE_PROVISIONED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-361"><strong>PACKAGE_PROVISIONED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-362">0x80073d1a</span><span class="sxs-lookup"><span data-stu-id="685b5-362">0x80073D1A</span></span></td>
<td><span data-ttu-id="685b5-363">Für eine optionale Paket Bereitstellung muss das Abhängigkeits Hauptpaket ebenfalls bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-363">An optional package provision requires the dependency main package to also be provisioned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="685b5-365"><strong>CHECK_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-365"><strong>CHECK_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-366">0x80073d1b</span><span class="sxs-lookup"><span data-stu-id="685b5-366">0x80073D1B</span></span></td>
<td><span data-ttu-id="685b5-367">Fehler bei der <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">Überprüfung des SmartScreen-Rufs</a>durch die Pakete.</span><span class="sxs-lookup"><span data-stu-id="685b5-367">The packages failed the <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="685b5-369"><strong>CHECK_TIMEDOUT</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-369"><strong>CHECK_TIMEDOUT</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-370">0x80073d1c</span><span class="sxs-lookup"><span data-stu-id="685b5-370">0x80073D1C</span></span></td>
<td><span data-ttu-id="685b5-371">Timeout beim <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">Überprüfen der SmartScreen-Ruf</a> .</span><span class="sxs-lookup"><span data-stu-id="685b5-371">The <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a> operation timed out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span></span><br/> <span data-ttu-id="685b5-373"><strong>NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-373"><strong>NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-374">0x80073d1d</span><span class="sxs-lookup"><span data-stu-id="685b5-374">0x80073D1D</span></span></td>
<td><span data-ttu-id="685b5-375">Die aktuelle Bereitstellungs Option wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="685b5-375">The current deployment option is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-376"><strong>ERROR_APPINSTALLER_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-376"><strong>ERROR_APPINSTALLER_</strong></span></span><br/> <span data-ttu-id="685b5-377"><strong>ACTIVATION_BLOCKED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-377"><strong>ACTIVATION_BLOCKED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-378">0x80073d1e</span><span class="sxs-lookup"><span data-stu-id="685b5-378">0x80073D1E</span></span></td>
<td><span data-ttu-id="685b5-379">Die Aktivierung wird aufgrund der appinstaller-Aktualisierungs Einstellungen für diese APP blockiert.</span><span class="sxs-lookup"><span data-stu-id="685b5-379">Activation is blocked due to the .appinstaller update settings for this app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-380"><strong>ERROR_REGISTRATION_FROM_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-380"><strong>ERROR_REGISTRATION_FROM_</strong></span></span><br/> <span data-ttu-id="685b5-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-382">0x80073d1f</span><span class="sxs-lookup"><span data-stu-id="685b5-382">0x80073D1F</span></span></td>
<td><span data-ttu-id="685b5-383">Remote Laufwerke werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="685b5-383">Remote drives are not supported.</span></span> <span data-ttu-id="685b5-384">Verwenden Sie <strong> \\ "Server\Freigabe"</strong> zum Registrieren eines Remote Pakets.</span><span class="sxs-lookup"><span data-stu-id="685b5-384">Use <strong>\\server\share</strong> to register a remote package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-385"><strong>ERROR_APPX_RAW_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-385"><strong>ERROR_APPX_RAW_</strong></span></span><br/> <span data-ttu-id="685b5-386"><strong>DATA_WRITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-386"><strong>DATA_WRITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-387">0x80073d20</span><span class="sxs-lookup"><span data-stu-id="685b5-387">0x80073D20</span></span></td>
<td><span data-ttu-id="685b5-388">Fehler beim Verarbeiten und schreiben heruntergeladener Paketdaten auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="685b5-388">Failed to process and write downloaded package data to disk.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="685b5-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-391">0x80073d21</span><span class="sxs-lookup"><span data-stu-id="685b5-391">0x80073D21</span></span></td>
<td><span data-ttu-id="685b5-392">Der Bereitstellungs Vorgang wurde aufgrund einer Paket familienrichtlinie blockiert, die bereit Stellungen auf einem nicht-System Volume einschränkt.</span><span class="sxs-lookup"><span data-stu-id="685b5-392">The deployment operation was blocked due to a per-package-family policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="685b5-393">Gemäß der Richtlinie muss diese APP auf dem Systemlaufwerk installiert werden, dies ist jedoch nicht als Standard festgelegt.</span><span class="sxs-lookup"><span data-stu-id="685b5-393">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="685b5-394">Legen Sie unter Speichereinstellungen das Systemlaufwerk als Standard Speicherort fest, um neuen Inhalt zu speichern, und wiederholen Sie dann die Installation.</span><span class="sxs-lookup"><span data-stu-id="685b5-394">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="685b5-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-397">0x80073d22</span><span class="sxs-lookup"><span data-stu-id="685b5-397">0x80073D22</span></span></td>
<td><span data-ttu-id="685b5-398">Der Bereitstellungs Vorgang wurde aufgrund einer Computer weiten Richtlinie blockiert, die bereit Stellungen auf einem nicht-System Volume einschränkt.</span><span class="sxs-lookup"><span data-stu-id="685b5-398">The deployment operation was blocked due to a machine-wide policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="685b5-399">Gemäß der Richtlinie muss diese APP auf dem Systemlaufwerk installiert werden, dies ist jedoch nicht als Standard festgelegt.</span><span class="sxs-lookup"><span data-stu-id="685b5-399">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="685b5-400">Legen Sie unter Speichereinstellungen das Systemlaufwerk als Standard Speicherort fest, um neuen Inhalt zu speichern, und wiederholen Sie dann die Installation.</span><span class="sxs-lookup"><span data-stu-id="685b5-400">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="685b5-402"><strong>BY_PROFILE_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-402"><strong>BY_PROFILE_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-403">0x80073d23</span><span class="sxs-lookup"><span data-stu-id="685b5-403">0x80073D23</span></span></td>
<td><span data-ttu-id="685b5-404">Der Bereitstellungs Vorgang wurde blockiert, weil eine spezielle Profil Bereitstellung nicht zulässig ist (spezielle Profile sind Benutzerprofile, bei denen Änderungen verworfen werden, nachdem sich der Benutzer abgemeldet hat).</span><span class="sxs-lookup"><span data-stu-id="685b5-404">The deployment operation was blocked because special profile deployment is not allowed (special profiles are user profiles where changes are discarded after the user signs out).</span></span> <span data-ttu-id="685b5-405">Melden Sie sich bei einem Konto an, das kein spezielles Profil ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-405">Try logging into an account that is not a special profile.</span></span> <span data-ttu-id="685b5-406">Sie können versuchen, sich beim aktuellen Konto anzumelden und sich wieder anzumelden oder sich bei einem anderen Konto anzumelden.</span><span class="sxs-lookup"><span data-stu-id="685b5-406">You can try logging out and logging back into the current account, or try logging into a different account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span></span><br/> <span data-ttu-id="685b5-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span></span><br/> <span data-ttu-id="685b5-409"><strong>Befinden</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-409"><strong>DIRECTORY</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-410">0x80073d24</span><span class="sxs-lookup"><span data-stu-id="685b5-410">0x80073D24</span></span></td>
<td><span data-ttu-id="685b5-411">Der Bereitstellungs Vorgang ist aufgrund des <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">änderbaren Paket Verzeichnisses</a>eines in Konflikt stehenden Pakets fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="685b5-411">The deployment operation failed due to a conflicting package's <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">mutable package directory</a>.</span></span> <span data-ttu-id="685b5-412">Entfernen Sie das vorhandene Paket mit dem in Konflikt stehenden änderbaren Paket Verzeichnis, um dieses Paket zu installieren.</span><span class="sxs-lookup"><span data-stu-id="685b5-412">To install this package, remove the existing package with the conflicting mutable package directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span></span><br/> <span data-ttu-id="685b5-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-415">0x80073d25</span><span class="sxs-lookup"><span data-stu-id="685b5-415">0x80073D25</span></span></td>
<td><span data-ttu-id="685b5-416">Die Paketinstallation ist fehlgeschlagen, weil eine Singleton-Ressource angegeben und ein anderer Benutzer mit installiertem Paket angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-416">The package installation failed because a singleton resource was specified and another user with that package installed is logged in.</span></span> <span data-ttu-id="685b5-417">Stellen Sie sicher, dass alle aktiven Benutzer mit installiertem Paket abgemeldet werden, und wiederholen Sie die Installation.</span><span class="sxs-lookup"><span data-stu-id="685b5-417">Make sure that all active users with the package installed are logged out and retry installation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-418">ERROR_DIFFERENT_VERSION_<strong></strong></span><span class="sxs-lookup"><span data-stu-id="685b5-418">ERROR_DIFFERENT_VERSION_<strong></strong></span></span><br/> <span data-ttu-id="685b5-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-420">0x80073d26</span><span class="sxs-lookup"><span data-stu-id="685b5-420">0x80073D26</span></span></td>
<td><span data-ttu-id="685b5-421">Die Paketinstallation ist fehlgeschlagen, da eine andere Version des Dienstanbieter installiert ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-421">The package installation failed because a different version of the service is installed.</span></span> <span data-ttu-id="685b5-422">Versuchen Sie, eine neuere Version des Pakets zu installieren.</span><span class="sxs-lookup"><span data-stu-id="685b5-422">Try installing a newer version of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-423"><strong>ERROR_SERVICE_EXISTS_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-423"><strong>ERROR_SERVICE_EXISTS_</strong></span></span><br/> <span data-ttu-id="685b5-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-425">0x80073d27</span><span class="sxs-lookup"><span data-stu-id="685b5-425">0x80073D27</span></span></td>
<td><span data-ttu-id="685b5-426">Die Paketinstallation ist fehlgeschlagen, da eine Version des Dienstanbieter außerhalb eines msix-/AppX-Pakets vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-426">The package installation failed because a version of the service exists outside of an .msix/.appx package.</span></span> <span data-ttu-id="685b5-427">Wenden Sie sich an den Softwarehersteller.</span><span class="sxs-lookup"><span data-stu-id="685b5-427">Contact your software vendor.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span></span><br/> <span data-ttu-id="685b5-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-430">0x80073d28</span><span class="sxs-lookup"><span data-stu-id="685b5-430">0x80073D28</span></span></td>
<td><span data-ttu-id="685b5-431">Die Paketinstallation ist fehlgeschlagen, da Administratorrechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="685b5-431">The package installation failed because administrator privileges are required.</span></span> <span data-ttu-id="685b5-432">Bitten Sie einen Administrator, dieses Paket zu installieren.</span><span class="sxs-lookup"><span data-stu-id="685b5-432">Contact an administrator to install this package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-433"><strong>ERROR_REDIRECTION_TO_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-433"><strong>ERROR_REDIRECTION_TO_</strong></span></span><br/> <span data-ttu-id="685b5-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-435">0x80073d29</span><span class="sxs-lookup"><span data-stu-id="685b5-435">0x80073D29</span></span></td>
<td><span data-ttu-id="685b5-436">Die Paket Bereitstellung ist fehlgeschlagen, da der Vorgang zu einem Standardkonto umgeleitet worden wäre, als der Aufrufer dies nicht getan hat.</span><span class="sxs-lookup"><span data-stu-id="685b5-436">The package deployment failed because the operation would have redirected to default account, when the caller said not to do so.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-437"><strong>ERROR_PACKAGE_LACKS_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-437"><strong>ERROR_PACKAGE_LACKS_</strong></span></span><br/> <span data-ttu-id="685b5-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-439">0x80073d2a</span><span class="sxs-lookup"><span data-stu-id="685b5-439">0x80073D2A</span></span></td>
<td><span data-ttu-id="685b5-440">Die Paket Bereitstellung ist fehlgeschlagen, da das Paket eine Funktion zum systemeigenen Ziel dieses Hosts erfordert.</span><span class="sxs-lookup"><span data-stu-id="685b5-440">The package deployment failed because the package requires a capability to natively target this host.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="685b5-442"><strong>INVALID_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-442"><strong>INVALID_CONTENT</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-443">0x80073d2b</span><span class="sxs-lookup"><span data-stu-id="685b5-443">0x80073D2B</span></span></td>
<td><span data-ttu-id="685b5-444">Fehler bei der Paket Bereitstellung, weil der zugehörige Inhalt für ein nicht signiertes Paket ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-444">The package deployment failed because its content is not valid for an unsigned package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="685b5-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-447">0x80073d2c</span><span class="sxs-lookup"><span data-stu-id="685b5-447">0x80073D2C</span></span></td>
<td><span data-ttu-id="685b5-448">Die Paket Bereitstellung ist fehlgeschlagen, da sich der Verleger nicht im nicht signierten Namespace befindet.</span><span class="sxs-lookup"><span data-stu-id="685b5-448">The package deployment failed because its publisher is not in the unsigned namespace.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="685b5-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-451">0x80073d2d</span><span class="sxs-lookup"><span data-stu-id="685b5-451">0x80073D2D</span></span></td>
<td><span data-ttu-id="685b5-452">Fehler bei der Paket Bereitstellung, weil der Verleger nicht im signierten Namespace ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-452">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span></span><br/> <span data-ttu-id="685b5-454"><strong>LOCATION_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-454"><strong>LOCATION_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-455">0x80073d2e</span><span class="sxs-lookup"><span data-stu-id="685b5-455">0x80073D2E</span></span></td>
<td><span data-ttu-id="685b5-456">Fehler bei der Paket Bereitstellung, weil der Verleger nicht im signierten Namespace ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-456">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span></span><br/> <span data-ttu-id="685b5-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="685b5-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-460">0x80073d2f</span><span class="sxs-lookup"><span data-stu-id="685b5-460">0x80073D2F</span></span></td>
<td><span data-ttu-id="685b5-461">Eine Host Laufzeitabhängigkeit zum Auflösen eines Pakets mit voll vertrauenswürdigem Inhalt erfordert, dass das Hauptpaket über die Funktion " <strong>runfulltrust</strong> " verfügt.</span><span class="sxs-lookup"><span data-stu-id="685b5-461">A host runtime dependency resolving to a package with full trust content requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="685b5-463">0x80080200</span><span class="sxs-lookup"><span data-stu-id="685b5-463">0x80080200</span></span></td>
<td><span data-ttu-id="685b5-464">Interner Fehler bei der Paket-API.</span><span class="sxs-lookup"><span data-stu-id="685b5-464">The packaging API has encountered an internal error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-465"><strong>APPX_E_INTERLEAVING_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-465"><strong>APPX_E_INTERLEAVING_</strong></span></span><br/> <span data-ttu-id="685b5-466"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-466"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-467">0x80080201</span><span class="sxs-lookup"><span data-stu-id="685b5-467">0x80080201</span></span></td>
<td><span data-ttu-id="685b5-468">Das Paket ist ungültig, weil sein Inhalt überlappend ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-468">The package isn't valid because its contents are interleaved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-469"><strong>APPX_E_RELATIONSHIPS_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-469"><strong>APPX_E_RELATIONSHIPS_</strong></span></span><br/> <span data-ttu-id="685b5-470"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-470"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-471">0x80080202</span><span class="sxs-lookup"><span data-stu-id="685b5-471">0x80080202</span></span></td>
<td><span data-ttu-id="685b5-472">Das Paket ist ungültig, weil es OPC-Beziehungen enthält.</span><span class="sxs-lookup"><span data-stu-id="685b5-472">The package isn't valid because it contains OPC relationships.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-473"><strong>APPX_E_MISSING_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-473"><strong>APPX_E_MISSING_</strong></span></span><br/> <span data-ttu-id="685b5-474"><strong>REQUIRED_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-474"><strong>REQUIRED_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-475">0x80080203</span><span class="sxs-lookup"><span data-stu-id="685b5-475">0x80080203</span></span></td>
<td><span data-ttu-id="685b5-476">Das Paket ist ungültig, weil ein Manifest oder eine Block Zuordnung fehlt, oder eine Code Integritäts Datei ist vorhanden, aber eine Signatur Datei fehlt.</span><span class="sxs-lookup"><span data-stu-id="685b5-476">The package isn't valid because it's missing a manifest or block map, or a code integrity file is present but a signature file is missing.</span></span><br/> <span data-ttu-id="685b5-477">Stellen Sie sicher, dass für das Paket mindestens eine der folgenden erforderlichen Dateien fehlt:</span><span class="sxs-lookup"><span data-stu-id="685b5-477">Ensure that the package isn't missing one or more of these required files:</span></span><br/>
<ul>
<li><span data-ttu-id="685b5-478">\AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="685b5-478">\AppxManifest.xml</span></span></li>
<li><span data-ttu-id="685b5-479">\AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="685b5-479">\AppxBlockMap.xml</span></span></li>
</ul>
<span data-ttu-id="685b5-480">Wenn das Paket \AppxMetadata\CodeIntegrity.cat enthält, muss es auch \appxsignature.p7xenthalten.</span><span class="sxs-lookup"><span data-stu-id="685b5-480">If the package contains \AppxMetadata\CodeIntegrity.cat, it must also contain \AppxSignature.p7x.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-481"><strong>APPX_E_INVALID_MANIFEST</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-481"><strong>APPX_E_INVALID_MANIFEST</strong></span></span></td>
<td><span data-ttu-id="685b5-482">0x80080204</span><span class="sxs-lookup"><span data-stu-id="685b5-482">0x80080204</span></span></td>
<td><span data-ttu-id="685b5-483">Die AppxManifest.xml Datei des Pakets ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-483">The package's AppxManifest.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span></span></td>
<td><span data-ttu-id="685b5-485">0x80080205</span><span class="sxs-lookup"><span data-stu-id="685b5-485">0x80080205</span></span></td>
<td><span data-ttu-id="685b5-486">Die AppxBlockMap.xml Datei des Pakets ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-486">The package's AppxBlockMap.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span></span></td>
<td><span data-ttu-id="685b5-488">0x80080206</span><span class="sxs-lookup"><span data-stu-id="685b5-488">0x80080206</span></span></td>
<td><span data-ttu-id="685b5-489">Der Paket Inhalt kann nicht gelesen werden, da er beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-489">The package contents can't be read because it's corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-490"><strong>APPX_E_BLOCK_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-490"><strong>APPX_E_BLOCK_</strong></span></span><br/> <span data-ttu-id="685b5-491"><strong>HASH_INVALID</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-491"><strong>HASH_INVALID</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-492">0x80080207</span><span class="sxs-lookup"><span data-stu-id="685b5-492">0x80080207</span></span></td>
<td><span data-ttu-id="685b5-493">Der berechnete Hashwert des Blocks entspricht nicht dem in der Block Zuordnung gespeicherten Wert.</span><span class="sxs-lookup"><span data-stu-id="685b5-493">The computed hash value of the block doesn't match the has value stored in the block map.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-494"><strong>APPX_E_REQUESTED_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-494"><strong>APPX_E_REQUESTED_</strong></span></span><br/> <span data-ttu-id="685b5-495"><strong>RANGE_TOO_LARGE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-495"><strong>RANGE_TOO_LARGE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-496">0x80080208</span><span class="sxs-lookup"><span data-stu-id="685b5-496">0x80080208</span></span></td>
<td><span data-ttu-id="685b5-497">Der angeforderte Byte Bereich beträgt mehr als 4 GB, wenn er in einen Byte Bereich von Blöcken übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="685b5-497">The requested byte range is over 4 GB when translated to a byte range of blocks.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-498"><strong>TRUST_E_NOSIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-498"><strong>TRUST_E_NOSIGNATURE</strong></span></span></td>
<td><span data-ttu-id="685b5-499">0x800B0100</span><span class="sxs-lookup"><span data-stu-id="685b5-499">0x800B0100</span></span></td>
<td><span data-ttu-id="685b5-500">Es ist keine Signatur im Betreff vorhanden.</span><span class="sxs-lookup"><span data-stu-id="685b5-500">No signature is present in the subject.</span></span><br/> <span data-ttu-id="685b5-501">Dieser Fehler kann angezeigt werden, wenn das Paket nicht signiert oder die Signatur ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="685b5-501">You may get this error if the package is unsigned or the signature isn't valid.</span></span> <span data-ttu-id="685b5-502">Das Paket muss zur Bereitstellung signiert sein.</span><span class="sxs-lookup"><span data-stu-id="685b5-502">The package must be signed to be deployed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span></span></td>
<td><span data-ttu-id="685b5-504">0x800B0109</span><span class="sxs-lookup"><span data-stu-id="685b5-504">0x800B0109</span></span></td>
<td><span data-ttu-id="685b5-505">Eine Zertifikat Kette wurde verarbeitet, aber in einem Stamm Zertifikat beendet, dem der Vertrauens Anbieter nicht vertraut.</span><span class="sxs-lookup"><span data-stu-id="685b5-505">A certificate chain processed, but terminated in a root certificate which isn't trusted by the trust provider.</span></span><br/> <span data-ttu-id="685b5-506">Siehe <a href="/previous-versions/br230260(v=vs.110)">Signieren eines Pakets</a>.</span><span class="sxs-lookup"><span data-stu-id="685b5-506">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-507"><strong>CERT_E_CHAINING</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-507"><strong>CERT_E_CHAINING</strong></span></span></td>
<td><span data-ttu-id="685b5-508">0x800b010a</span><span class="sxs-lookup"><span data-stu-id="685b5-508">0x800B010A</span></span></td>
<td><span data-ttu-id="685b5-509">Eine Zertifikat Kette konnte nicht für eine vertrauenswürdige Stamm Zertifizierungsstelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-509">A certificate chain couldn't be built to a trusted root certification authority.</span></span><br/> <span data-ttu-id="685b5-510">Siehe <a href="/previous-versions/br230260(v=vs.110)">Signieren eines Pakets</a>.</span><span class="sxs-lookup"><span data-stu-id="685b5-510">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-511"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="685b5-511"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="685b5-512"><strong>SIP_CLIENT_DATA</strong> </span><span class="sxs-lookup"><span data-stu-id="685b5-512"><strong>SIP_CLIENT_DATA</strong> </span></span><br/></td>
<td><span data-ttu-id="685b5-513">0x80080209</span><span class="sxs-lookup"><span data-stu-id="685b5-513">0x80080209</span></span></td>
<td><span data-ttu-id="685b5-514">Die <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>Struktur, die zum Signieren des Pakets verwendet wurde, enthielt nicht die erforderlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="685b5-514">The <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>structure used to sign the package didn't contain the required data</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-515"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="685b5-515"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="685b5-516"><strong>KEY_INFO</strong> </span><span class="sxs-lookup"><span data-stu-id="685b5-516"><strong>KEY_INFO</strong> </span></span><br/></td>
<td><span data-ttu-id="685b5-517">0x8008020a</span><span class="sxs-lookup"><span data-stu-id="685b5-517">0x8008020A</span></span></td>
<td><span data-ttu-id="685b5-518">Die <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> Struktur, die zum Verschlüsseln oder Entschlüsseln des Pakets verwendet wird, enthält ungültige Daten.</span><span class="sxs-lookup"><span data-stu-id="685b5-518">The <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> structure used to encrypt or decrypt the package contains invalid data.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-519"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-519"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-520"><strong>Contentgroupmap</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-520"><strong>CONTENTGROUPMAP</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-521">0x8008020b</span><span class="sxs-lookup"><span data-stu-id="685b5-521">0x8008020B</span></span></td>
<td><span data-ttu-id="685b5-522">Die Inhalts Gruppen Zuordnung des msix/AppX-Pakets ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-522">The .msix/.appx package's content group map is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-523"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-523"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-524"><strong>Appinstaller</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-524"><strong>APPINSTALLER</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-525">0x8008020c</span><span class="sxs-lookup"><span data-stu-id="685b5-525">0x8008020C</span></span></td>
<td><span data-ttu-id="685b5-526">Die <a href="/windows/msix/app-installer/app-installer-root">appinstaller-Datei</a> für das Paket ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-526">The <a href="/windows/msix/app-installer/app-installer-root">.appinstaller file</a> for the package is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-527"><strong>APPX_E_DELTA_BASELINE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-527"><strong>APPX_E_DELTA_BASELINE_</strong></span></span><br/> <span data-ttu-id="685b5-528"><strong>VERSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-528"><strong>VERSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-529">0x8008020d</span><span class="sxs-lookup"><span data-stu-id="685b5-529">0x8008020D</span></span></td>
<td><span data-ttu-id="685b5-530">Die baselinepaketversion im Delta Paket stimmt nicht mit der Version in dem zu aktualisierenden Basispaket ab.</span><span class="sxs-lookup"><span data-stu-id="685b5-530">The baseline package version in delta package does not match the version in the baseline package to be updated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span></span><br/> <span data-ttu-id="685b5-532"><strong>MISSING_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-532"><strong>MISSING_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-533">0x8008020e</span><span class="sxs-lookup"><span data-stu-id="685b5-533">0x8008020E</span></span></td>
<td><span data-ttu-id="685b5-534">Im Delta Paket fehlt eine Datei aus dem aktualisierten Paket.</span><span class="sxs-lookup"><span data-stu-id="685b5-534">The delta package is missing a file from the updated package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-535"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-535"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-536"><strong>DELTA_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-536"><strong>DELTA_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-537">0x8008020f</span><span class="sxs-lookup"><span data-stu-id="685b5-537">0x8008020F</span></span></td>
<td><span data-ttu-id="685b5-538">Das Delta Paket ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-538">The delta package is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-539"><strong>APPX_E_DELTA_APPENDED_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-539"><strong>APPX_E_DELTA_APPENDED_</strong></span></span><br/> <span data-ttu-id="685b5-540"><strong>PACKAGE_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-540"><strong>PACKAGE_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-541">0x80080210</span><span class="sxs-lookup"><span data-stu-id="685b5-541">0x80080210</span></span></td>
<td><span data-ttu-id="685b5-542">Das angefügte Delta Paket ist für den aktuellen Vorgang nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="685b5-542">The delta appended package is not allowed for the current operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-543"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-543"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-544"><strong>PACKAGING_LAYOUT</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-544"><strong>PACKAGING_LAYOUT</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-545">0x80080211</span><span class="sxs-lookup"><span data-stu-id="685b5-545">0x80080211</span></span></td>
<td><span data-ttu-id="685b5-546">Die paketlayoutdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-546">The packaging layout file is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-547"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-547"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-548"><strong>Packagesignconfig</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-548"><strong>PACKAGESIGNCONFIG</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-549">0x80080212</span><span class="sxs-lookup"><span data-stu-id="685b5-549">0x80080212</span></span></td>
<td><span data-ttu-id="685b5-550">Die Datei "packagesignconfig" ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-550">The packageSignConfig file is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-551"><strong>APPX_E_RESOURCESPRI_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-551"><strong>APPX_E_RESOURCESPRI_</strong></span></span><br/> <span data-ttu-id="685b5-552"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-552"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-553">0x80080213</span><span class="sxs-lookup"><span data-stu-id="685b5-553">0x80080213</span></span></td>
<td><span data-ttu-id="685b5-554">Die Datei "Resources. pri" ist nicht zulässig, wenn das Paket Manifest keine Ressourcen Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="685b5-554">The resources.pri file is not allowed when there are no resource elements in the package manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-555"><strong>APPX_E_FILE_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-555"><strong>APPX_E_FILE_</strong></span></span><br/> <span data-ttu-id="685b5-556"><strong>COMPRESSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-556"><strong>COMPRESSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-557">0x80080214</span><span class="sxs-lookup"><span data-stu-id="685b5-557">0x80080214</span></span></td>
<td><span data-ttu-id="685b5-558">Der Komprimierungs Status der Datei in der Baseline und des aktualisierten Pakets stimmt nicht mit.</span><span class="sxs-lookup"><span data-stu-id="685b5-558">The compression state of file in baseline and updated package does not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685b5-559"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-559"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-561">0x80080215</span><span class="sxs-lookup"><span data-stu-id="685b5-561">0x80080215</span></span></td>
<td><span data-ttu-id="685b5-562">Nicht-AppX-Erweiterungen sind bei Nutz Last Paketen, die auf ältere Plattformen abzielen, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="685b5-562">Non .appx extensions are not allowed for payload packages targeting older platforms.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685b5-563"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-563"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="685b5-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span><span class="sxs-lookup"><span data-stu-id="685b5-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span></span><br/></td>
<td><span data-ttu-id="685b5-565">0x80080216</span><span class="sxs-lookup"><span data-stu-id="685b5-565">0x80080216</span></span></td>
<td><span data-ttu-id="685b5-566">Die Datei "verschlüsselungsexclusionfilelist" ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="685b5-566">The encryptionExclusionFileList file is invalid.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a><span data-ttu-id="685b5-567">Anwendungen werden nicht gestartet, und ihre Namen sind abdimmt.</span><span class="sxs-lookup"><span data-stu-id="685b5-567">Applications don't start and their names are dimmed</span></span>

<span data-ttu-id="685b5-568">Auf einem Windows 10-basierten Computer können Sie einige Anwendungen nicht starten, und die Anwendungsnamen werden abgeblendet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="685b5-568">On a Windows 10-based computer, you cannot start some applications, and the application names appear dimmed.</span></span>

![Einige Anwendungsnamen werden im Startmenü abgeblendet angezeigt.](./images/app-names-dimmed.png)

<span data-ttu-id="685b5-570">Wenn Sie versuchen, eine Anwendung durch Auswahl des abzurufenden namens zu öffnen, erhalten Sie möglicherweise eine der folgenden Fehlermeldungen:</span><span class="sxs-lookup"><span data-stu-id="685b5-570">When you try to open an application by selecting the dimmed name, you may receive one of the following error messages:</span></span>

> <span data-ttu-id="685b5-571">Es gibt ein Problem mit \<*application name*> .</span><span class="sxs-lookup"><span data-stu-id="685b5-571">There's a problem with \<*application name*>.</span></span> <span data-ttu-id="685b5-572">Bitten Sie den Systemadministrator, ihn zu reparieren oder neu zu installieren.</span><span class="sxs-lookup"><span data-stu-id="685b5-572">Contact your system administrator about repairing or reinstalling it</span></span>  
> <span data-ttu-id="685b5-573">Fehler: diese APP kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-573">Error: This app can't open</span></span>

<span data-ttu-id="685b5-574">Außerdem werden die folgenden Ereignis Einträge im Protokoll "Microsoft-Windows-twinui/Operational" unter "Applications" **und "services\microsoft\windows\apps**" protokolliert:</span><span class="sxs-lookup"><span data-stu-id="685b5-574">Additionally, the following event entries are logged in the "Microsoft-Windows-TWinUI/Operational" log under **Applications and Services\Microsoft\Windows\Apps**:</span></span>

> <span data-ttu-id="685b5-575">Protokoll Name: Microsoft-Windows-twinui/Operational</span><span class="sxs-lookup"><span data-stu-id="685b5-575">Log Name: Microsoft-Windows-TWinUI/Operational</span></span>  
> <span data-ttu-id="685b5-576">Quelle: Microsoft-Windows-immersive Shell</span><span class="sxs-lookup"><span data-stu-id="685b5-576">Source: Microsoft-Windows-Immersive-Shell</span></span>  
> <span data-ttu-id="685b5-577">Datum: <*Datum*></span><span class="sxs-lookup"><span data-stu-id="685b5-577">Date: <*date*></span></span>  
> <span data-ttu-id="685b5-578">Ereignis-ID: 5960</span><span class="sxs-lookup"><span data-stu-id="685b5-578">Event ID: 5960</span></span>  
> <span data-ttu-id="685b5-579">Aufgaben Kategorie: (5960)</span><span class="sxs-lookup"><span data-stu-id="685b5-579">Task Category: (5960)</span></span>  
> <span data-ttu-id="685b5-580">Ebene: Fehler</span><span class="sxs-lookup"><span data-stu-id="685b5-580">Level: Error</span></span>  
> <span data-ttu-id="685b5-581">Schlüsselwörter:</span><span class="sxs-lookup"><span data-stu-id="685b5-581">Keywords:</span></span>  
> <span data-ttu-id="685b5-582">Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="685b5-582">Description:</span></span>  
> <span data-ttu-id="685b5-583">Aktivierung der APP Microsoft.BingNews_8wekyb3d8bbwe! Appexnews für Windows.</span><span class="sxs-lookup"><span data-stu-id="685b5-583">Activation of the app Microsoft.BingNews_8wekyb3d8bbwe!AppexNews for the Windows.</span></span> <span data-ttu-id="685b5-584">Der Start Vertrag wurde mit dem Fehler 0x80073cfc blockiert, weil sich das zugehörige Paket im Status "geändert" befindet.</span><span class="sxs-lookup"><span data-stu-id="685b5-584">Launch contract was blocked with error 0x80073CFC because its package is in state: Modified.</span></span>  

### <a name="cause"></a><span data-ttu-id="685b5-585">Ursache</span><span class="sxs-lookup"><span data-stu-id="685b5-585">Cause</span></span>

<span data-ttu-id="685b5-586">Dieses Problem tritt auf, weil der Registrierungs Eintrag für den Statuswert des entsprechenden Pakets der Anwendung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="685b5-586">This issue occurs because the registry entry for the status value of application's corresponding package was modified.</span></span>

### <a name="resolution"></a><span data-ttu-id="685b5-587">Lösung</span><span class="sxs-lookup"><span data-stu-id="685b5-587">Resolution</span></span>

> [!WARNING]
> <span data-ttu-id="685b5-588">Durch die unsachgemäße Änderung der Registrierung mit dem Registrierungs-Editor oder einer anderen Methode können schwerwiegende Probleme verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="685b5-588">Serious problems might occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="685b5-589">U. U. ist in einem solchen Fall sogar die Neuinstallation des Betriebssystems erforderlich.</span><span class="sxs-lookup"><span data-stu-id="685b5-589">These problems might require that you reinstall the operating system.</span></span> <span data-ttu-id="685b5-590">Microsoft garantiert nicht, dass diese Probleme behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="685b5-590">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="685b5-591">Das Bearbeiten der Registrierung erfolgt auf eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="685b5-591">Modify the registry at your own risk.</span></span>

<span data-ttu-id="685b5-592">So beheben Sie dieses Problem:</span><span class="sxs-lookup"><span data-stu-id="685b5-592">To fix this issue:</span></span>

1. <span data-ttu-id="685b5-593">Starten Sie den Registrierungs-Editor, und suchen Sie dann den **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="685b5-593">Start Registry Editor, and then locate the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** subkey.</span></span>
2. <span data-ttu-id="685b5-594">Um die Unterschlüssel Daten zu sichern, klicken Sie mit der rechten Maustaste auf **PackageList**, wählen Sie **exportieren** aus, und speichern Sie die Daten dann als Registrierungsdatei.</span><span class="sxs-lookup"><span data-stu-id="685b5-594">To back up the subkey data, right-click **PackageList**, select **Export**, and then save the data as a registry file.</span></span>
3. <span data-ttu-id="685b5-595">Führen Sie für jede Anwendung, die in den Ereignis-ID 5960-Protokoll Einträgen aufgeführt ist, die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="685b5-595">For each of the applications that are listed in the Event ID 5960 log entries, follow these steps:</span></span>  
   1. <span data-ttu-id="685b5-596">Suchen Sie den Eintrag **packagestatus** .</span><span class="sxs-lookup"><span data-stu-id="685b5-596">Locate the **PackageStatus** entry.</span></span>
   2. <span data-ttu-id="685b5-597">Legen Sie den Wert von **packagestatus** auf **0**(null) fest.</span><span class="sxs-lookup"><span data-stu-id="685b5-597">Set the value of **PackageStatus** to zero (**0**).</span></span>
   > [!NOTE]  
   > <span data-ttu-id="685b5-598">Wenn unter **PackageList** keine Einträge für die Anwendung vorhanden sind, hat das Problem eine andere Ursache.</span><span class="sxs-lookup"><span data-stu-id="685b5-598">If there are no entries for the application under **PackageList**, then the issue has some other cause.</span></span> <span data-ttu-id="685b5-599">Im Fall des Beispiel Ereignisses in diesem Artikel wird der vollständige Unterschlüssel **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span><span class="sxs-lookup"><span data-stu-id="685b5-599">In the case of the example event in this article, the full subkey is **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span></span>
4. <span data-ttu-id="685b5-600">Starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="685b5-600">Restart the computer.</span></span>

## <a name="get-additional-help"></a><span data-ttu-id="685b5-601">Zusätzliche Hilfe abrufen</span><span class="sxs-lookup"><span data-stu-id="685b5-601">Get additional help</span></span>

<span data-ttu-id="685b5-602">Wenn Sie weitere Hilfe bei der Behebung eines Problems benötigen, das Sie beim Verpacken, bereitstellen oder Abfragen eines Windows-App-Pakets (. msix/. AppX) als Entwickler haben, finden Sie weitere Informationen unter Support Ressourcen für Entwickler.</span><span class="sxs-lookup"><span data-stu-id="685b5-602">If you need further help with resolving a problem you are experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer, refer to these additional developer support resources.</span></span>

- <span data-ttu-id="685b5-603">[Microsoft Q&a](/answers/topics/uwp.html?filter=all&sort=active) bietet relevante und rechtzeitige Antworten auf technische Probleme von einer Community von Experten und Microsoft-Technikern.</span><span class="sxs-lookup"><span data-stu-id="685b5-603">[Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offers relevant and timely answers to your technical problems from a community of experts and Microsoft engineers.</span></span>
- <span data-ttu-id="685b5-604">Zur Unterstützung der Community bei der Entwicklung finden Sie in unseren [Foren](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)und [StackOverflow](https://stackoverflow.com/questions).</span><span class="sxs-lookup"><span data-stu-id="685b5-604">For community assistance with development questions, there are our [forums](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required), and [StackOverflow](https://stackoverflow.com/questions).</span></span>
- <span data-ttu-id="685b5-605">Auf der [Windows Developer Support](https://developer.microsoft.com/windows/support) -Website werden Weitere Supportoptionen erläutert.</span><span class="sxs-lookup"><span data-stu-id="685b5-605">The [Windows developer support](https://developer.microsoft.com/windows/support) site explains other support options.</span></span>

## <a name="related-topics"></a><span data-ttu-id="685b5-606">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="685b5-606">Related topics</span></span>

- [<span data-ttu-id="685b5-607">Signieren eines App-Pakets mit SignTool</span><span class="sxs-lookup"><span data-stu-id="685b5-607">How to sign an app package using SignTool</span></span>](how-to-sign-a-package-using-signtool.md)
- [<span data-ttu-id="685b5-608">Problembehandlung bei App-Paket Signatur Fehlern</span><span class="sxs-lookup"><span data-stu-id="685b5-608">How to troubleshoot app package signature errors</span></span>](how-to-troubleshoot-app-package-signature-errors.md)
