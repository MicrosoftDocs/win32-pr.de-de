---
description: Der Windows Update-Agent (WUA) kann verwendet werden, um Computer auf Sicherheitsupdates zu überprüfen, ohne eine Verbindung mit Windows Update oder einem WSUS-Server (Windows Server Update Services) herzustellen. Dadurch können Computer, die nicht mit dem Internet verbunden sind, auf Sicherheitsupdates überprüft werden. Die Offline Überprüfung von Updates erfordert das Herunterladen einer signierten Datei (Wsusscn2.cab) von Windows Update.
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: Verwenden von WUA, um Offline nach Updates zu suchen
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 242ff3655f4ab469d8d768a94f8dc8e529e0da74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342719"
---
# <a name="using-wua-to-scan-for-updates-offline"></a><span data-ttu-id="500e5-104">Verwenden von WUA, um Offline nach Updates zu suchen</span><span class="sxs-lookup"><span data-stu-id="500e5-104">Using WUA to Scan for Updates Offline</span></span>

<span data-ttu-id="500e5-105">Der Windows Update-Agent (WUA) kann verwendet werden, um Computer auf Sicherheitsupdates zu überprüfen, ohne eine Verbindung mit Windows Update oder einem WSUS-Server (Windows Server Update Services) herzustellen. Dadurch können Computer, die nicht mit dem Internet verbunden sind, auf Sicherheitsupdates überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="500e5-105">Windows Update Agent (WUA) can be used to scan computers for security updates without connecting to Windows Update or to a Windows Server Update Services (WSUS) server, which enables computers that are not connected to the Internet to be scanned for security updates.</span></span>

<span data-ttu-id="500e5-106">Die Offline Überprüfung von Updates erfordert das Herunterladen einer signierten Datei (Wsusscn2.cab) von Windows Update.</span><span class="sxs-lookup"><span data-stu-id="500e5-106">Offline scanning for updates requires the download of a signed file, Wsusscn2.cab, from Windows Update.</span></span>

<span data-ttu-id="500e5-107">Die Wsusscn2.cab-Datei ist eine CAB-Datei, die von Microsoft signiert wird.</span><span class="sxs-lookup"><span data-stu-id="500e5-107">The Wsusscn2.cab file is a cabinet file that is signed by Microsoft.</span></span> <span data-ttu-id="500e5-108">Diese Datei enthält Informationen zu sicherheitsbezogenen Updates, die von Microsoft veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="500e5-108">This file contains info about security-related updates that are published by Microsoft.</span></span> <span data-ttu-id="500e5-109">Computer, die nicht mit dem Internet verbunden sind, können gescannt werden, um festzustellen, ob diese sicherheitsbezogenen Updates vorhanden oder erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="500e5-109">Computers that aren't connected to the Internet can be scanned to see whether these security-related updates are present or required.</span></span> <span data-ttu-id="500e5-110">Die Wsusscn2.cab Datei enthält die Sicherheitsupdates nicht selbst, sodass Sie erforderliche sicherheitsrelevante Updates auf andere Weise abrufen und installieren müssen.</span><span class="sxs-lookup"><span data-stu-id="500e5-110">The Wsusscn2.cab file doesn't contain the security updates themselves so you must obtain and install any needed security-related updates through other means.</span></span> <span data-ttu-id="500e5-111">Neue Versionen der Wsusscn2.cab Datei werden regelmäßig freigegeben, wenn sicherheitsrelevante Updates auf der Windows Update Website veröffentlicht, entfernt oder überarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="500e5-111">New versions of the Wsusscn2.cab file are released periodically as security-related updates are released, removed, or revised on the Windows Update site.</span></span> <span data-ttu-id="500e5-112">Die neueste Wsusscn2.cab Datei steht unter folgendem Speicherort zum Herunterladen zur Verfügung: [herunterladen Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span><span class="sxs-lookup"><span data-stu-id="500e5-112">The latest Wsusscn2.cab file is available for download at the following location: [Download Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span></span>

<span data-ttu-id="500e5-113">Nachdem Sie die aktuelle Wsusscn2.cab heruntergeladen haben, kann die Datei für die [**addscanpackageservice**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) -Methode bereitgestellt werden, und die WUA-API kann zum Durchsuchen des Offline Computers nach Sicherheitsupdates verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="500e5-113">After you download the latest Wsusscn2.cab, the file can be provided to the [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) method, and the WUA API can be used to search the offline computer for security updates.</span></span> <span data-ttu-id="500e5-114">WUA überprüft, ob die Wsusscn2.cab von einem gültigen Microsoft-Zertifikat signiert ist, bevor eine Offline Überprüfung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="500e5-114">WUA validates that the Wsusscn2.cab is signed by a valid Microsoft certificate before running an offline scan.</span></span>

> [!NOTE]
> <span data-ttu-id="500e5-115">In Übereinstimmung mit unserer " [SHA-1"-veralnungs Initiative](https://aka.ms/sha1deprecation)wird die Wsusscn2.cab Datei nicht mehr mit "SHA-1" und der SHA-2-Suite von Hash Algorithmen (insbesondere SHA-256) doppelt signiert.</span><span class="sxs-lookup"><span data-stu-id="500e5-115">In accordance with our [SHA-1 deprecation initiative](https://aka.ms/sha1deprecation), the Wsusscn2.cab file is no longer dual-signed using both SHA-1 and the SHA-2 suite of hash algorithms (specifically SHA-256).</span></span> <span data-ttu-id="500e5-116">Diese Datei wird jetzt nur mit SHA-256 signiert.</span><span class="sxs-lookup"><span data-stu-id="500e5-116">This file is now signed using only SHA-256.</span></span> <span data-ttu-id="500e5-117">Administratoren, die digitale Signaturen für diese Datei überprüfen, sollten jetzt nur einzelne SHA-256-Signaturen erwarten.</span><span class="sxs-lookup"><span data-stu-id="500e5-117">Administrators who verify digital signatures on this file should now expect only single SHA-256 signatures.</span></span>

## <a name="example"></a><span data-ttu-id="500e5-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="500e5-118">Example</span></span>

<span data-ttu-id="500e5-119">Im folgenden Beispiel wird die Wsusscn2.cab Datei zum Scannen eines Computers verwendet, und es werden fehlende Updates angezeigt.</span><span class="sxs-lookup"><span data-stu-id="500e5-119">The following example uses the Wsusscn2.cab file to scan a computer and displays updates that are missing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="500e5-120">Dieses Skript soll die Verwendung der Windows Update-Agent-APIs veranschaulichen und bietet ein Beispiel dafür, wie Entwickler diese APIs zum Lösen von Problemen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="500e5-120">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="500e5-121">Dieses Skript ist nicht als Produktionscode gedacht, und das Skript selbst wird nicht von Microsoft unterstützt (obwohl die zugrunde liegenden Windows Update-Agent-APIs unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="500e5-121">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set UpdateSession = CreateObject("Microsoft.Update.Session")
Set UpdateServiceManager = CreateObject("Microsoft.Update.ServiceManager")
Set UpdateService = UpdateServiceManager.AddScanPackageService("Offline Sync Service", "c:\wsusscn2.cab", 1)
Set UpdateSearcher = UpdateSession.CreateUpdateSearcher()

WScript.Echo "Searching for updates..." & vbCRLF

UpdateSearcher.ServerSelection = 3 ' ssOthers

UpdateSearcher.ServiceID = UpdateService.ServiceID

Set SearchResult = UpdateSearcher.Search("IsInstalled=0")

Set Updates = SearchResult.Updates

If searchResult.Updates.Count = 0 Then
    WScript.Echo "There are no applicable updates."
    WScript.Quit
End If

WScript.Echo "List of applicable items on the machine when using wssuscan.cab:" & vbCRLF

For I = 0 to searchResult.Updates.Count-1
    Set update = searchResult.Updates.Item(I)
    WScript.Echo I + 1 & "> " & update.Title
Next

WScript.Quit
```



 

 



