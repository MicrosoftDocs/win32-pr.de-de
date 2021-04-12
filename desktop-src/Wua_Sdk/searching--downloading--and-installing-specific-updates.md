---
description: Das Skript Beispiel in diesem Thema veranschaulicht, wie Sie den Windows Update-Agent (WUA) verwenden, um ein bestimmtes Update zu scannen, herunterzuladen und zu installieren. Das Update kann anhand seines Titels angegeben werden.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Suchen, herunterladen und installieren spezifischer Updates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadd7903303356c3937f41e44aa7a47e71192409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343808"
---
# <a name="searching-downloading-and-installing-specific-updates"></a>Suchen, herunterladen und installieren spezifischer Updates

Das Skript Beispiel in diesem Thema veranschaulicht, wie Sie den Windows Update-Agent (WUA) verwenden, um ein bestimmtes Update zu scannen, herunterzuladen und zu installieren. Das Update kann anhand seines Titels angegeben werden.

Das Beispiel sucht nach einem bestimmten Software Update, lädt das Update herunter und installiert dann das Update. Beispielsweise kann ein Benutzer mit dieser Methode ermitteln, ob ein kritisches Sicherheitsupdate auf einem Computer installiert ist. Wenn das Update nicht installiert ist, kann der Benutzer sicherstellen, dass das Update heruntergeladen und installiert wird. Der Benutzer kann außerdem sicherstellen, dass er über den Status der Installation benachrichtigt wird.

Das Beispiel Update wird durch den Update Titel in der [**Title-Eigenschaft von iupdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)identifiziert. Der Titel des Updates, das in diesem Beispiel empfohlen wird, ist "Update for Windows Rights Management Client 1,0."

> [!Note]  
> Informationen zum Suchen, herunterladen und Installieren aller Updates, die für eine bestimmte Anwendung gelten, finden Sie unter [suchen, herunterladen und Installieren von Updates](searching--downloading--and-installing-updates.md).

 

Beachten Sie Folgendes, bevor Sie versuchen, dieses Beispiel auszuführen:

-   WUA muss auf dem Computer installiert sein. Weitere Informationen zum Ermitteln der installierten Version von WUA finden Sie unter [bestimmen der aktuellen WUA](determining-the-current-version-of-wua.md)-Version.
-   Das Beispiel bietet keine eigene Benutzeroberfläche. WUA fordert den Benutzer auf, den Computer neu zu starten, wenn ein Update einen Neustart erfordert.
-   Das Beispiel kann nur Updates von WUA herunterladen. Updates können nicht von einem Server mit der Software Update Services (SUS) 1,0 heruntergeladen werden.
-   Das Ausführen dieses Beispiels erfordert Windows Script Host (WSH). Weitere Informationen zu WSH finden Sie im Abschnitt "WSH" des Platform Software Development Kit (SDK). Wenn das Beispiel in eine Datei mit dem Namen WUA \_SpecificUpdate.vbs kopiert wird, können Sie es ausführen, indem Sie ein Eingabe Aufforderungs Fenster öffnen und den folgenden Befehl eingeben: **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>Beispiel

> [!IMPORTANT]
> Dieses Skript soll die Verwendung der Windows Update-Agent-APIs veranschaulichen und bietet ein Beispiel dafür, wie Entwickler diese APIs zum Lösen von Problemen verwenden können. Dieses Skript ist nicht als Produktionscode gedacht, und das Skript selbst wird nicht von Microsoft unterstützt (obwohl die zugrunde liegenden Windows Update-Agent-APIs unterstützt werden).

 


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



 

 



