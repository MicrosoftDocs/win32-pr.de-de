---
title: Beispiel für eine Desktop Anwendung
description: Beispiel für eine Desktop Anwendung
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Desktop Anwendungen, Beispiele
- Windows Media Device Manager, Beispiel für eine Desktop Anwendung
- Beispiel für Device Manager Desktop Anwendung
- wmdmapp-Beispielanwendung
- Beispiele, Desktop Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388361"
---
# <a name="sample-desktop-application"></a><span data-ttu-id="135d4-110">Beispiel für eine Desktop Anwendung</span><span class="sxs-lookup"><span data-stu-id="135d4-110">Sample Desktop Application</span></span>

<span data-ttu-id="135d4-111">Der Windows Media Device Manager wird mit einer Beispiel-Desktop Anwendung namens wmdmapp ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="135d4-111">The Windows Media Device Manager ships with a sample desktop application called wmdmapp.</span></span> <span data-ttu-id="135d4-112">Diese Anwendung verfügt über eine grafische Benutzeroberfläche, die Ihnen das Durchsuchen verbundener Geräte, das Erstellen von Wiedergabelisten auf dem Gerät und das Ziehen von Mediendateien auf das Gerät ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="135d4-112">This application has a graphical user interface that allows you to browse connected devices, create playlists on the device, and drag media files to the device.</span></span>

<span data-ttu-id="135d4-113">Diese Beispielanwendung besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="135d4-113">This sample application consists of two pieces:</span></span>

-   <span data-ttu-id="135d4-114">wmdapp.exe, eine ausführbare Datei, die ein Fenster anzeigt und die meisten Benutzeroberflächen und grundlegenden Funktionen des Programms ausführt, und</span><span class="sxs-lookup"><span data-stu-id="135d4-114">wmdapp.exe, an executable that displays a window and performs most of the user interface and basic functionality of the program, and</span></span>
-   <span data-ttu-id="135d4-115">proghelp.dll, eine Hilfs-DLL, die Hilfsprogrammfunktionen für die Anwendung ausführt.</span><span class="sxs-lookup"><span data-stu-id="135d4-115">proghelp.dll, a helper DLL that performs utility functions for the application.</span></span> <span data-ttu-id="135d4-116">Sie müssen diese DLL nach der Projekt Erstellung registrieren.</span><span class="sxs-lookup"><span data-stu-id="135d4-116">You must register this DLL after building the project.</span></span>

<span data-ttu-id="135d4-117">Sie können Visual Studio verwenden, um die Beispielanwendung zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="135d4-117">To compile the sample application, you can use Visual Studio.</span></span> <span data-ttu-id="135d4-118">Im folgenden Abschnitt wird beschrieben, wie dies geschieht:</span><span class="sxs-lookup"><span data-stu-id="135d4-118">The following section describes how this is done:</span></span>

-   [<span data-ttu-id="135d4-119">Kompilieren der Beispielanwendung mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="135d4-119">Compiling the Sample Application Using Visual Studio</span></span>](compiling-the-sample-application-using-visual-studio.md)

<span data-ttu-id="135d4-120">Nachdem Sie das Projekt kompiliert haben, registrieren Sie die proghelp.dll Datei.</span><span class="sxs-lookup"><span data-stu-id="135d4-120">After compiling the project, register the proghelp.dll file.</span></span> <span data-ttu-id="135d4-121">Um diese DLL zu registrieren, öffnen Sie eine Eingabeaufforderung, navigieren Sie zu dem Verzeichnis, das diese DLL enthält, und geben Sie ein `regsvr32 proghelp.dll` .</span><span class="sxs-lookup"><span data-stu-id="135d4-121">To register this DLL, open a command prompt and browse to the directory containing this DLL and type `regsvr32 proghelp.dll`.</span></span>

 

 




