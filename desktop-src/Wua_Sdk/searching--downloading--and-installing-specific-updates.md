---
description: Das Skriptbeispiel in diesem Thema zeigt, wie Sie den Windows Update-Agent (WUA) verwenden, um ein bestimmtes Update zu überprüfen, herunterzuladen und zu installieren. Das Update kann anhand des Titels angegeben werden.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Suchen, Herunterladen und Installieren bestimmter Updates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c2da9569ed6fe34b18264ee59e91965877d63e422ae20e25fc27fbc025e812
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071284"
---
# <a name="searching-downloading-and-installing-specific-updates"></a>Suchen, Herunterladen und Installieren bestimmter Updates

Das Skriptbeispiel in diesem Thema zeigt, wie Sie den Windows Update-Agent (WUA) verwenden, um ein bestimmtes Update zu überprüfen, herunterzuladen und zu installieren. Das Update kann anhand des Titels angegeben werden.

Im Beispiel wird nach einem bestimmten Softwareupdate gesucht, das Update heruntergeladen und dann das Update installiert. Beispielsweise kann ein Benutzer diese Methode verwenden, um zu bestimmen, ob ein kritisches Sicherheitsupdate auf einem Computer installiert ist. Wenn das Update nicht installiert ist, kann der Benutzer sicherstellen, dass das Update heruntergeladen und installiert wird. Der Benutzer kann auch sicherstellen, dass er über den Status der Installation benachrichtigt wird.

Das Beispielupdate wird durch den Updatetitel in [**der Titeleigenschaft von IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)identifiziert. Der Titel des Updates, das in diesem Beispiel vorgeschlagen wird, lautet "Update für Windows Rights Management Client 1.0".

> [!Note]  
> Informationen zum Suchen, Herunterladen und Installieren aller Updates, die für eine bestimmte Anwendung gelten, finden Sie unter [Suchen, Herunterladen und Installieren von Updates.](searching--downloading--and-installing-updates.md)

 

Beachten Sie Folgendes, bevor Sie versuchen, dieses Beispiel auszuführen:

-   WUA muss auf dem Computer installiert sein. Weitere Informationen zum Ermitteln der installierten WUA-Version finden Sie unter [Bestimmen der aktuellen Version von WUA.](determining-the-current-version-of-wua.md)
-   Das Beispiel bietet keine eigene Benutzeroberfläche. WUA fordert den Benutzer auf, den Computer neu zu starten, wenn ein Update einen Neustart erfordert.
-   Das Beispiel kann Updates nur von WUA herunterladen. Updates können nicht von einem SOFTWARE UPDATE SERVICES-Server (SUS) 1.0-Server heruntergeladen werden.
-   Zum Ausführen dieses Beispiels ist Windows Script Host (WSH) erforderlich. Weitere Informationen zu WSH finden Sie im WSH-Abschnitt des Platform Software Development Kit (SDK). Wenn das Beispiel in eine Datei mit dem Namen WUASpecificUpdate.vbs kopiert \_ wird, können Sie es ausführen, indem Sie ein Eingabeaufforderungsfenster öffnen und den folgenden Befehl eingeben: **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>Beispiel

> [!IMPORTANT]
> Dieses Skript soll die Verwendung der Windows Update-Agent-APIs veranschaulichen und ein Beispiel dafür bereitstellen, wie Entwickler diese APIs zum Lösen von Problemen verwenden können. Dieses Skript ist nicht als Produktionscode vorgesehen, und das Skript selbst wird von Microsoft nicht unterstützt (obwohl die zugrunde liegenden Windows Update-Agent-APIs unterstützt werden).

 


```VB
Set updateSession = CreateObject("Microsoft.Update.Session")
updateSession.ClientApplicationID = "MSDN Sample Script"

'Get update title to search for
WScript.Echo "Enter the title of the update: " & _
"(for example, Update for Windows Rights Management client 1.0)"
updateTitle = WScript.StdIn.Readline

WScript.Echo vbCRLF & "Searching for: " & updateTitle & "..."

Set updateSearcher = updateSession.CreateupdateSearcher()

'Search for all software updates, already installed and not installed
Set searchResult = _
updateSearcher.Search("Type='Software'")

Set updateToInstall = CreateObject("Microsoft.Update.UpdateColl")

updateIsApplicable = False

'Cycle through search results to look for the update title
For i = 0 To searchResult.Updates.Count-1
   Set update = searchResult.Updates.Item(i)
   If UCase(update.Title) = UCase(updateTitle) Then
   'Update in list of applicable updates 
   'Determine if it is already installed or not
      If update.IsInstalled = False Then
         WScript.Echo vbCRLF & _
         "Result: Update applicable, not installed."
         updateIsApplicable = True
         updateToInstall.Add(update)
      Else 
         'Update is installed so notify user and quit
         WScript.Echo vbCRLF & _
         "Result: Update applicable, already installed."
         updateIsApplicable = True
         WScript.Quit 
      End If
   End If 
Next

If updateIsApplicable = False Then
   WScript.Echo "Result: Update is not applicable to this machine."
   WScript.Quit
End If

WScript.Echo vbCRLF & "Would you like to install now? (Y/N)"
stdInput = WScript.StdIn.Readline
 
If (strInput = "N" or strInput = "n") Then 
   WScript.Quit
ElseIf  (stdInput = "Y" OR stdInput = "y") Then
   'Download update
   Set downloader = updateSession.CreateUpdateDownloader() 
   downloader.Updates = updateToInstall
   WScript.Echo vbCRLF & "Downloading..."
   Set downloadResult = downloader.Download()
   WScript.Echo "Download Result: " & downloadResult.ResultCode
  
   'Install Update
   Set installer = updateSession.CreateUpdateInstaller()
   WScript.Echo vbCRLF & "Installing..."
   installer.Updates = updateToInstall
   Set installationResult = installer.Install()
  
   'Output the result of the installation
   WScript.Echo "Installation Result: " & _
   installationResult.ResultCode
   WScript.Echo "Reboot Required: " & _
   installationResult.RebootRequired 
End If
```



 

 



