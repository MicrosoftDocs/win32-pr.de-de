---
title: Windows Hallo Welt-Beispiel
description: Diese Beispielanwendung zeigt, wie ein minimales Windows-Programm erstellt wird.
ms.assetid: ec316ad8-d01d-4558-91b6-19fdbba3d520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932d3b0c524c643022904b08402507d4a603adb
ms.sourcegitcommit: e084958628fb997e9e11fe08574d82edbba07dbf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2019
ms.locfileid: "104311675"
---
# <a name="windows-hello-world-sample"></a><span data-ttu-id="9c2fa-103">Windows Hallo Welt-Beispiel</span><span class="sxs-lookup"><span data-stu-id="9c2fa-103">Windows Hello World Sample</span></span>

<span data-ttu-id="9c2fa-104">Diese Beispielanwendung zeigt, wie ein minimales Windows-Programm erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-104">This sample application shows how to create a minimal Windows program.</span></span>

## <a name="description"></a><span data-ttu-id="9c2fa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c2fa-105">Description</span></span>

<span data-ttu-id="9c2fa-106">Die Beispielanwendung Windows Hallo Welt erstellt und zeigt ein leeres Fenster an, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-106">The Windows Hello World sample application creates and shows an empty window, as shown in the screen shot that follows.</span></span> <span data-ttu-id="9c2fa-107">Dieses Beispiel wird in [Modul 1 erläutert. Ihr erstes Windows-Programm](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="9c2fa-107">This sample is discussed in [Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

![Screenshot des Beispiel Programms](images/window01.png)

## <a name="downloading-the-sample"></a><span data-ttu-id="9c2fa-109">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9c2fa-109">Downloading the Sample</span></span>

<span data-ttu-id="9c2fa-110">Dieses Beispiel ist [hier](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/HelloWorld)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-110">This sample is available [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/HelloWorld).</span></span>

<span data-ttu-id="9c2fa-111">Um es herunterzuladen, navigieren Sie zum Stamm des beispielrepository auf GitHub ([Microsoft/Windows-Classic-Samples](https://github.com/microsoft/Windows-classic-samples/)), und klicken Sie auf die Schaltfläche **Klonen oder herunterladen** , um die ZIP-Datei aller Beispiele auf Ihren Computer herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-111">To download it, go to the root of the sample repo on GitHub ([microsoft/Windows-classic-samples](https://github.com/microsoft/Windows-classic-samples/)) and click the **Clone or download** button to download the zip file of all the samples to your computer.</span></span> <span data-ttu-id="9c2fa-112">Entzippen Sie dann den Ordner.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-112">Then unzip the folder.</span></span>

<span data-ttu-id="9c2fa-113">Um das Beispiel in Visual Studio zu öffnen, wählen Sie Datei > Öffnen > Projekt > **Projekt** Mappe aus, und navigieren Sie zu dem Speicherort, an dem Sie den Ordner entzippt haben, und **Windows-Classic-Samples-Master/Samples/Win7Samples/BEGIN/LearnWin32/Hello**</span><span class="sxs-lookup"><span data-stu-id="9c2fa-113">To open the sample in Visual Studio, select **File / Open / Project/Solution**, and navigate to the location you unzipped the folder and **Windows-classic-samples-master / Samples / Win7Samples / begin / LearnWin32 / HelloWorld / cpp**.</span></span> <span data-ttu-id="9c2fa-114">Öffnen Sie die Datei " **HelloWorld. sln**".</span><span class="sxs-lookup"><span data-stu-id="9c2fa-114">Open the file **HelloWorld.sln**.</span></span>

<span data-ttu-id="9c2fa-115">Nachdem das Beispiel geladen wurde, müssen Sie es aktualisieren, damit es mit Windows 10 funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-115">Once the sample has loaded, you will need to update it to work with Windows 10.</span></span> <span data-ttu-id="9c2fa-116">Wählen Sie im Menü **Projekt** in Visual Studio die Option **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-116">From the **Project** menu in Visual Studio, select **Properties**.</span></span> <span data-ttu-id="9c2fa-117">Aktualisieren Sie die **Windows SDK Version** in ein Windows 10 SDK, z. b. 10.0.17763.0 oder eine bessere Version.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-117">Update the **Windows SDK Version** to a Windows 10 SDK, such as 10.0.17763.0 or better.</span></span> <span data-ttu-id="9c2fa-118">Ändern Sie dann das **Platt Form Toolset** in Visual Studio 2017 oder höher.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-118">Then change **Platform Toolset** to Visual Studio 2017 or better.</span></span> <span data-ttu-id="9c2fa-119">Nun können Sie das Beispiel ausführen, indem Sie F5 drücken.</span><span class="sxs-lookup"><span data-stu-id="9c2fa-119">Now you can run the sample by pressing F5!</span></span>


## <a name="related-topics"></a><span data-ttu-id="9c2fa-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c2fa-120">Related topics</span></span>

* [<span data-ttu-id="9c2fa-121">Erlernen Sie das Program mieren für Windows: Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="9c2fa-121">Learn to Program for Windows: Sample Code</span></span>](learn-to-program-for-windows--sample-code.md)
* [<span data-ttu-id="9c2fa-122">Modul 1. Ihr erstes Windows-Programm</span><span class="sxs-lookup"><span data-stu-id="9c2fa-122">Module 1. Your First Windows Program</span></span>](your-first-windows-program.md)
