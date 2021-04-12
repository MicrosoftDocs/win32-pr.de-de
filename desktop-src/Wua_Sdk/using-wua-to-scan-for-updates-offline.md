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
# <a name="using-wua-to-scan-for-updates-offline"></a>Verwenden von WUA, um Offline nach Updates zu suchen

Der Windows Update-Agent (WUA) kann verwendet werden, um Computer auf Sicherheitsupdates zu überprüfen, ohne eine Verbindung mit Windows Update oder einem WSUS-Server (Windows Server Update Services) herzustellen. Dadurch können Computer, die nicht mit dem Internet verbunden sind, auf Sicherheitsupdates überprüft werden.

Die Offline Überprüfung von Updates erfordert das Herunterladen einer signierten Datei (Wsusscn2.cab) von Windows Update.

Die Wsusscn2.cab-Datei ist eine CAB-Datei, die von Microsoft signiert wird. Diese Datei enthält Informationen zu sicherheitsbezogenen Updates, die von Microsoft veröffentlicht werden. Computer, die nicht mit dem Internet verbunden sind, können gescannt werden, um festzustellen, ob diese sicherheitsbezogenen Updates vorhanden oder erforderlich sind. Die Wsusscn2.cab Datei enthält die Sicherheitsupdates nicht selbst, sodass Sie erforderliche sicherheitsrelevante Updates auf andere Weise abrufen und installieren müssen. Neue Versionen der Wsusscn2.cab Datei werden regelmäßig freigegeben, wenn sicherheitsrelevante Updates auf der Windows Update Website veröffentlicht, entfernt oder überarbeitet werden. Die neueste Wsusscn2.cab Datei steht unter folgendem Speicherort zum Herunterladen zur Verfügung: [herunterladen Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)

Nachdem Sie die aktuelle Wsusscn2.cab heruntergeladen haben, kann die Datei für die [**addscanpackageservice**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) -Methode bereitgestellt werden, und die WUA-API kann zum Durchsuchen des Offline Computers nach Sicherheitsupdates verwendet werden. WUA überprüft, ob die Wsusscn2.cab von einem gültigen Microsoft-Zertifikat signiert ist, bevor eine Offline Überprüfung ausgeführt wird.

> [!NOTE]
> In Übereinstimmung mit unserer " [SHA-1"-veralnungs Initiative](https://aka.ms/sha1deprecation)wird die Wsusscn2.cab Datei nicht mehr mit "SHA-1" und der SHA-2-Suite von Hash Algorithmen (insbesondere SHA-256) doppelt signiert. Diese Datei wird jetzt nur mit SHA-256 signiert. Administratoren, die digitale Signaturen für diese Datei überprüfen, sollten jetzt nur einzelne SHA-256-Signaturen erwarten.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Wsusscn2.cab Datei zum Scannen eines Computers verwendet, und es werden fehlende Updates angezeigt.

> [!IMPORTANT]
> Dieses Skript soll die Verwendung der Windows Update-Agent-APIs veranschaulichen und bietet ein Beispiel dafür, wie Entwickler diese APIs zum Lösen von Problemen verwenden können. Dieses Skript ist nicht als Produktionscode gedacht, und das Skript selbst wird nicht von Microsoft unterstützt (obwohl die zugrunde liegenden Windows Update-Agent-APIs unterstützt werden).

 


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



 

 



