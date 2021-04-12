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
# <a name="searching-downloading-and-installing-specific-updates"></a><span data-ttu-id="7078e-104">Suchen, herunterladen und installieren spezifischer Updates</span><span class="sxs-lookup"><span data-stu-id="7078e-104">Searching, Downloading, and Installing Specific Updates</span></span>

<span data-ttu-id="7078e-105">Das Skript Beispiel in diesem Thema veranschaulicht, wie Sie den Windows Update-Agent (WUA) verwenden, um ein bestimmtes Update zu scannen, herunterzuladen und zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7078e-105">The scripting sample in this topic shows you how to use the Windows Update Agent (WUA) to scan, download, and install a specific update.</span></span> <span data-ttu-id="7078e-106">Das Update kann anhand seines Titels angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7078e-106">The update can be specified by its title.</span></span>

<span data-ttu-id="7078e-107">Das Beispiel sucht nach einem bestimmten Software Update, lädt das Update herunter und installiert dann das Update.</span><span class="sxs-lookup"><span data-stu-id="7078e-107">The sample searches for a specific software update, downloads the update, and then installs the update.</span></span> <span data-ttu-id="7078e-108">Beispielsweise kann ein Benutzer mit dieser Methode ermitteln, ob ein kritisches Sicherheitsupdate auf einem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7078e-108">For example, a user can use this method to determine if a critical security update is installed on a computer.</span></span> <span data-ttu-id="7078e-109">Wenn das Update nicht installiert ist, kann der Benutzer sicherstellen, dass das Update heruntergeladen und installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7078e-109">If the update isn't installed, the user can ensure that the update is downloaded and installed.</span></span> <span data-ttu-id="7078e-110">Der Benutzer kann außerdem sicherstellen, dass er über den Status der Installation benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="7078e-110">The user can also ensure that they are notified about the status of the installation.</span></span>

<span data-ttu-id="7078e-111">Das Beispiel Update wird durch den Update Titel in der [**Title-Eigenschaft von iupdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7078e-111">The sample update is identified by the update title in [**Title Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span></span> <span data-ttu-id="7078e-112">Der Titel des Updates, das in diesem Beispiel empfohlen wird, ist "Update for Windows Rights Management Client 1,0."</span><span class="sxs-lookup"><span data-stu-id="7078e-112">The title of the update that is suggested in this sample is "Update for Windows Rights Management client 1.0."</span></span>

> [!Note]  
> <span data-ttu-id="7078e-113">Informationen zum Suchen, herunterladen und Installieren aller Updates, die für eine bestimmte Anwendung gelten, finden Sie unter [suchen, herunterladen und Installieren von Updates](searching--downloading--and-installing-updates.md).</span><span class="sxs-lookup"><span data-stu-id="7078e-113">For info about how to search, download, and install all the updates that apply to a specific application, see [Searching, Downloading, and Installing Updates](searching--downloading--and-installing-updates.md).</span></span>

 

<span data-ttu-id="7078e-114">Beachten Sie Folgendes, bevor Sie versuchen, dieses Beispiel auszuführen:</span><span class="sxs-lookup"><span data-stu-id="7078e-114">Before you attempt to run this sample, note the following:</span></span>

-   <span data-ttu-id="7078e-115">WUA muss auf dem Computer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="7078e-115">WUA must be installed on the computer.</span></span> <span data-ttu-id="7078e-116">Weitere Informationen zum Ermitteln der installierten Version von WUA finden Sie unter [bestimmen der aktuellen WUA](determining-the-current-version-of-wua.md)-Version.</span><span class="sxs-lookup"><span data-stu-id="7078e-116">For more info about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>
-   <span data-ttu-id="7078e-117">Das Beispiel bietet keine eigene Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="7078e-117">The sample doesn't provide its own user interface.</span></span> <span data-ttu-id="7078e-118">WUA fordert den Benutzer auf, den Computer neu zu starten, wenn ein Update einen Neustart erfordert.</span><span class="sxs-lookup"><span data-stu-id="7078e-118">WUA prompts the user to restart the computer if an update requires a restart.</span></span>
-   <span data-ttu-id="7078e-119">Das Beispiel kann nur Updates von WUA herunterladen.</span><span class="sxs-lookup"><span data-stu-id="7078e-119">The sample can download updates only from WUA.</span></span> <span data-ttu-id="7078e-120">Updates können nicht von einem Server mit der Software Update Services (SUS) 1,0 heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="7078e-120">It can't download updates from a Software Update Services (SUS) 1.0 server.</span></span>
-   <span data-ttu-id="7078e-121">Das Ausführen dieses Beispiels erfordert Windows Script Host (WSH).</span><span class="sxs-lookup"><span data-stu-id="7078e-121">Running this sample requires Windows Script Host (WSH).</span></span> <span data-ttu-id="7078e-122">Weitere Informationen zu WSH finden Sie im Abschnitt "WSH" des Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="7078e-122">For more info about WSH, see the WSH section of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="7078e-123">Wenn das Beispiel in eine Datei mit dem Namen WUA \_SpecificUpdate.vbs kopiert wird, können Sie es ausführen, indem Sie ein Eingabe Aufforderungs Fenster öffnen und den folgenden Befehl eingeben: **cscript WUA \_SpecificUpdate.vbs**</span><span class="sxs-lookup"><span data-stu-id="7078e-123">If the sample is copied to a file named WUA\_SpecificUpdate.vbs, you can run it by opening a Command Prompt window and by typing this command: **cscript WUA\_SpecificUpdate.vbs**</span></span>  
    

## <a name="example"></a><span data-ttu-id="7078e-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7078e-124">Example</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7078e-125">Dieses Skript soll die Verwendung der Windows Update-Agent-APIs veranschaulichen und bietet ein Beispiel dafür, wie Entwickler diese APIs zum Lösen von Problemen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7078e-125">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="7078e-126">Dieses Skript ist nicht als Produktionscode gedacht, und das Skript selbst wird nicht von Microsoft unterstützt (obwohl die zugrunde liegenden Windows Update-Agent-APIs unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="7078e-126">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


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



 

 



