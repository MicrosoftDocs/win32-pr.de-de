---
description: In diesem Thema wird das Debuggen von Shell-und Namespace Erweiterungs-DLLs erläutert.
title: Debuggen mit der Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525379"
---
# <a name="debugging-with-the-shell"></a><span data-ttu-id="25e1d-103">Debuggen mit der Shell</span><span class="sxs-lookup"><span data-stu-id="25e1d-103">Debugging with the Shell</span></span>

<span data-ttu-id="25e1d-104">In diesem Thema wird das Debuggen von Shell-und Namespace Erweiterungs-DLLs erläutert.</span><span class="sxs-lookup"><span data-stu-id="25e1d-104">This topic explains how to debug Shell and namespace extension DLLs.</span></span>

-   [<span data-ttu-id="25e1d-105">Ausführen der Shell unter einem Debugger</span><span class="sxs-lookup"><span data-stu-id="25e1d-105">Running the Shell Under a Debugger</span></span>](#running-the-shell-under-a-debugger)
-   [<span data-ttu-id="25e1d-106">Ausführen und Testen von Shellerweiterungen</span><span class="sxs-lookup"><span data-stu-id="25e1d-106">Running and Testing Shell Extensions</span></span>](#running-and-testing-shell-extensions)
-   [<span data-ttu-id="25e1d-107">Entladen der dll</span><span class="sxs-lookup"><span data-stu-id="25e1d-107">Unloading the DLL</span></span>](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a><span data-ttu-id="25e1d-108">Ausführen der Shell unter einem Debugger</span><span class="sxs-lookup"><span data-stu-id="25e1d-108">Running the Shell Under a Debugger</span></span>

<span data-ttu-id="25e1d-109">Zum Debuggen der Erweiterung müssen Sie die Shell über den Debugger ausführen.</span><span class="sxs-lookup"><span data-stu-id="25e1d-109">To debug your extension, you need to run the Shell from the debugger.</span></span> <span data-ttu-id="25e1d-110">Folgen Sie diesen Schritten:</span><span class="sxs-lookup"><span data-stu-id="25e1d-110">Follow these steps:</span></span>

1.  <span data-ttu-id="25e1d-111">Laden Sie das Projekt der Erweiterung in den Debugger, führen Sie es jedoch nicht aus.</span><span class="sxs-lookup"><span data-stu-id="25e1d-111">Load the extension's project into the debugger, but do not run it.</span></span>
2.  <span data-ttu-id="25e1d-112">Beenden Sie die Shell.</span><span class="sxs-lookup"><span data-stu-id="25e1d-112">Shut down the Shell.</span></span>

    -   <span data-ttu-id="25e1d-113">Für Windows Vista und höher:</span><span class="sxs-lookup"><span data-stu-id="25e1d-113">For Windows Vista and later:</span></span>
        1.  <span data-ttu-id="25e1d-114">Zeigen Sie das **Startmenü** an.</span><span class="sxs-lookup"><span data-stu-id="25e1d-114">Display the **Start** menu.</span></span>
        2.  <span data-ttu-id="25e1d-115">Drücken Sie STRG + UMSCHALT und klicken Sie mit der rechten Maustaste auf den Hintergrund der rechten Hälfte des **Startmenü** .</span><span class="sxs-lookup"><span data-stu-id="25e1d-115">Press CTRL+SHIFT and right-click on the background of the right half of the **Start** menu.</span></span>
        3.  <span data-ttu-id="25e1d-116">Wählen Sie im angezeigten Menü die Option **Exit Explorer** aus.</span><span class="sxs-lookup"><span data-stu-id="25e1d-116">From the menu that appears, choose **Exit Explorer**.</span></span>
    -   <span data-ttu-id="25e1d-117">Für Windows XP:</span><span class="sxs-lookup"><span data-stu-id="25e1d-117">For Windows XP:</span></span>
        1.  <span data-ttu-id="25e1d-118">Wählen Sie im Menü **Start** die Option **herunter** fahren aus.</span><span class="sxs-lookup"><span data-stu-id="25e1d-118">From the **Start** menu, choose **Shut down**.</span></span>
        2.  <span data-ttu-id="25e1d-119">Drücken Sie Strg + Alt + Umschalttaste, und klicken Sie im Dialogfeld **Windows herunter** fahren auf **Nein** .</span><span class="sxs-lookup"><span data-stu-id="25e1d-119">Press CTRL+ALT+SHIFT, and click **No** in the **Shut Down Windows** dialog box.</span></span>

    <span data-ttu-id="25e1d-120">Die Shell ist nun heruntergefahren, aber alle anderen Anwendungen werden weiterhin ausgeführt, einschließlich des Debuggers.</span><span class="sxs-lookup"><span data-stu-id="25e1d-120">The Shell is now shut down, but all other applications are still running, including the debugger.</span></span>

3.  <span data-ttu-id="25e1d-121">Legen Sie den Debugger so fest, dass die Erweiterungs-DLL mit Explorer.exe aus dem **Windows** -Verzeichnis ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25e1d-121">Set the debugger to run the extension DLL with Explorer.exe from the **Windows** directory.</span></span>
4.  <span data-ttu-id="25e1d-122">Führen Sie das Projekt aus dem Debugger aus.</span><span class="sxs-lookup"><span data-stu-id="25e1d-122">Run the project from the debugger.</span></span> <span data-ttu-id="25e1d-123">Die Shell wird wie üblich gestartet, aber der Debugger wird an den Shellprozess angefügt.</span><span class="sxs-lookup"><span data-stu-id="25e1d-123">The Shell will launch as usual, but the debugger will be attached to the Shell's process.</span></span>

## <a name="running-and-testing-shell-extensions"></a><span data-ttu-id="25e1d-124">Ausführen und Testen von Shellerweiterungen</span><span class="sxs-lookup"><span data-stu-id="25e1d-124">Running and Testing Shell Extensions</span></span>

<span data-ttu-id="25e1d-125">Sie können Ihre Erweiterungen in einem separaten Windows Explorer-Prozess ausführen und testen, um das Beenden und Neustarten des Desktops und der Taskleiste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="25e1d-125">You can run and test your extensions in a separate Windows Explorer process to avoid stopping and restarting the desktop and taskbar.</span></span> <span data-ttu-id="25e1d-126">Der Desktop und die Taskleiste können weiterhin verwendet werden, während Sie die Erweiterungen ausführen und testen.</span><span class="sxs-lookup"><span data-stu-id="25e1d-126">Your desktop and taskbar can still be used while you run and test the extensions.</span></span>

<span data-ttu-id="25e1d-127">Fügen Sie der Registrierung den folgenden reg DWORD-Eintrag hinzu, um dieses Feature zu aktivieren \_ .</span><span class="sxs-lookup"><span data-stu-id="25e1d-127">To enable this feature, add the following REG\_DWORD entry to the registry.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

<span data-ttu-id="25e1d-128">Damit dieser Eintrag wirksam wird, müssen Sie sich ab-und wieder anmelden.</span><span class="sxs-lookup"><span data-stu-id="25e1d-128">For this entry to take effect, you must log off and log on again.</span></span> <span data-ttu-id="25e1d-129">Diese Einstellung bewirkt, dass die Fenster Desktop und Taskleiste in einem Explorer.exe Prozess erstellt werden und alle anderen Explorer-und Ordner Fenster in einem anderen Explorer.exe Prozess geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="25e1d-129">This setting causes the desktop and taskbar windows to be created in one Explorer.exe process and all other Explorer and folder windows to be opened in a different Explorer.exe process.</span></span>

<span data-ttu-id="25e1d-130">Mit dieser Einstellung können Sie nicht nur die Ausführung und das Testen der Erweiterungen vereinfachen, sondern auch den Desktop stabiler machen, da er sich auf Shellerweiterungen bezieht.</span><span class="sxs-lookup"><span data-stu-id="25e1d-130">In addition to making the running and testing of your extensions more convenient, this setting also makes the desktop more robust as it relates to Shell extensions.</span></span> <span data-ttu-id="25e1d-131">Viele solche Erweiterungen (z. b. Kontextmenü Erweiterungen) werden in den nicht-Desktop Explorer.exe Prozess geladen.</span><span class="sxs-lookup"><span data-stu-id="25e1d-131">Many such extensions (shortcut menu extensions, for example) will be loaded into the nondesktop Explorer.exe process.</span></span> <span data-ttu-id="25e1d-132">Wenn dieser Prozess beendet wird, sind der Desktop und die Taskleiste nicht betroffen, und im nächsten Explorer oder Ordner Fenster wird der beendete Prozess neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="25e1d-132">If this process terminates, the desktop and taskbar will be unaffected, and the next Explorer or folder window will re-create the terminated process.</span></span>

## <a name="unloading-the-dll"></a><span data-ttu-id="25e1d-133">Entladen der dll</span><span class="sxs-lookup"><span data-stu-id="25e1d-133">Unloading the DLL</span></span>

<span data-ttu-id="25e1d-134">Die Shell entlädt automatisch jede DLL, wenn Ihre Verwendungs Anzahl 0 (null) ist, aber erst, nachdem die DLL für einen bestimmten Zeitraum verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="25e1d-134">The Shell automatically unloads any DLL when its usage count is zero, but only after the DLL has not been used for a period of time.</span></span> <span data-ttu-id="25e1d-135">Dieser inaktive Zeitraum ist ggf. nicht akzeptabel, insbesondere dann, wenn eine Shellerweiterungs-dll gedeppt wird.</span><span class="sxs-lookup"><span data-stu-id="25e1d-135">This inactive period might be unacceptably long at times, especially when a Shell extension DLL is being debugged.</span></span> <span data-ttu-id="25e1d-136">Sie können den inaktiven Zeitraum verkürzen, indem Sie der Registrierung die folgenden Informationen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="25e1d-136">You can shorten the inactive period by adding the following information to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



