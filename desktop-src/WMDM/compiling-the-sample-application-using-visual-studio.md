---
title: Kompilieren der Beispielanwendung mit Visual Studio
description: Kompilieren der Beispielanwendung mit Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Desktop Anwendungen, Beispiele
- Windows Media Device Manager, Beispiel für eine Desktop Anwendung
- Beispiel für Device Manager Desktop Anwendung
- Beispiele, Desktop Anwendungen
- Beispiele, Kompilieren mithilfe von Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036732"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a><span data-ttu-id="9ad26-110">Kompilieren der Beispielanwendung mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9ad26-110">Compiling the Sample Application Using Visual Studio</span></span>

<span data-ttu-id="9ad26-111">Das Windows Media Device Manager SDK enthält eine Visual Studio-Projekt Mappe, die mit Microsoft Visual Studio 2005 kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="9ad26-111">The Windows Media Device Manager SDK includes a Visual Studio solution that is compatible with Microsoft Visual Studio 2005.</span></span>

<span data-ttu-id="9ad26-112">Bevor Sie die Beispielanwendung kompilieren, müssen Sie die Header Datei "shtypes. h" umbenennen, um Konflikte mit einer Datei mit demselben Namen zu vermeiden, die im Microsoft Platform SDK zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="9ad26-112">Before you compile the sample application, you must rename the header file shtypes.h to prevent conflicts with a file of the same name that is found in the Microsoft Platform SDK.</span></span> <span data-ttu-id="9ad26-113">Beispielsweise können Sie <SDK- *Installationspfad* > \\ WMFSDK11 \\ include \\ shtypes. h in <*SDK-Installationspfad* > \\ WMFSDK11 \\ include \\ shtypes. h. Backup umbenennen.</span><span class="sxs-lookup"><span data-stu-id="9ad26-113">For example, you could rename <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h to <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h.backup.</span></span>

<span data-ttu-id="9ad26-114">Um die Anwendung zu erstellen, starten Sie eine Instanz von Visual Studio 2005, öffnen Sie die Projektmappendatei "wmdmapp. sln", die sich im Ordner <*SDK-Installationspfad* > \\ WMFSDK11 \\ apps \\ wmdmapp befindet, und wählen Sie die Option **Build/Build Solution** aus.</span><span class="sxs-lookup"><span data-stu-id="9ad26-114">To build the application, start an instance of Visual Studio 2005, open the solution file, wmdmapp.sln, which is found in the folder <*SDK installation path*>\\WMFSDK11\\apps\\wmdmapp and choose the **Build/Build Solution** option.</span></span> <span data-ttu-id="9ad26-115">Dadurch werden zwei Projektdateien erstellt: das Hilfsprojekt, proghelp. vcproj, und die Hauptanwendung wmdmapp. vcproj.</span><span class="sxs-lookup"><span data-stu-id="9ad26-115">This will create two project files: the helper project, proghelp.vcproj, as well as the main application wmdmapp.vcproj.</span></span> <span data-ttu-id="9ad26-116">Außerdem werden die Status-hilfsdll und die Hauptanwendung (WMDMApp.exe) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ad26-116">In addition, it will create the progress helper DLL and the main application (WMDMApp.exe).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ad26-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ad26-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ad26-118">**Beispiel für eine Desktop Anwendung**</span><span class="sxs-lookup"><span data-stu-id="9ad26-118">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




