---
title: SimpleRibbon-Beispiel
description: In diesem Codebeispiel wird veranschaulicht, wie eine einfache Menübandanwendung Windows implementiert wird.
ms.assetid: 9196ae63-ca9e-43ae-8b4c-a30f1ef700f0
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: b2a7ab939239bd3c0017dfeeeab1487bcb1dce26
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691659"
---
# <a name="simpleribbon-sample"></a><span data-ttu-id="a07e0-103">SimpleRibbon-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a07e0-103">SimpleRibbon Sample</span></span>

<span data-ttu-id="a07e0-104">In diesem Codebeispiel wird veranschaulicht, wie eine einfache Menübandanwendung Windows implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="a07e0-104">This code sample demonstrates how to implement a simple Windows Ribbon application.</span></span>

- [<span data-ttu-id="a07e0-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="a07e0-105">Usage</span></span>](#usage)
  - [<span data-ttu-id="a07e0-106">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="a07e0-106">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="a07e0-107">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="a07e0-107">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="a07e0-108">Support</span><span class="sxs-lookup"><span data-stu-id="a07e0-108">Support</span></span>](#support)
- [<span data-ttu-id="a07e0-109">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="a07e0-109">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="usage"></a><span data-ttu-id="a07e0-110">Usage</span><span class="sxs-lookup"><span data-stu-id="a07e0-110">Usage</span></span>

<span data-ttu-id="a07e0-111">Die Windows Ribbon Framework-Beispiele können als eigenständige Microsoft Visual Studio-Projekte aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) heruntergeladen oder als Teil des Windows Software Development Kit [(SDK) installiert werden.](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="a07e0-111">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="a07e0-112">Windows Software Development Kit (SDK) (Standardinstallationspfad): %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ WindowsRibbon \\ SimpleRibbon</span><span class="sxs-lookup"><span data-stu-id="a07e0-112">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\SimpleRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="a07e0-113">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="a07e0-113">Building the Sample</span></span>

<span data-ttu-id="a07e0-114">Laden Sie das Beispiel herunter.</span><span class="sxs-lookup"><span data-stu-id="a07e0-114">Download the sample.</span></span>

<span data-ttu-id="a07e0-115">Installieren Sie Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster der Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="a07e0-115">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="a07e0-116">Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="a07e0-116">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="a07e0-117">Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="a07e0-117">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="a07e0-118">Geben Sie an der Eingabeaufforderung MSBUILD ein.</span><span class="sxs-lookup"><span data-stu-id="a07e0-118">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="a07e0-119">Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.</span><span class="sxs-lookup"><span data-stu-id="a07e0-119">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="a07e0-120">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="a07e0-120">Running the Sample</span></span>

<span data-ttu-id="a07e0-121">Um das Beispiel über das Befehlsfenster der Buildumgebung auszuführen, führen Sie die .exe-Dateien im Ordner Bin Debug oder Bin Release aus, der \\ im Beispielquellenordner \\ enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a07e0-121">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="a07e0-122">Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="a07e0-122">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="a07e0-123">Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a07e0-123">Support</span></span>

<span data-ttu-id="a07e0-124">Das [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) steht zur Verfügung, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung Windows Menübandanwendungen zu stellen.</span><span class="sxs-lookup"><span data-stu-id="a07e0-124">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="a07e0-125">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="a07e0-125">Minimum Requirements</span></span>



| <span data-ttu-id="a07e0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a07e0-126">Requirement</span></span> | <span data-ttu-id="a07e0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a07e0-127">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a07e0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a07e0-128">Minimum supported client</span></span> | <span data-ttu-id="a07e0-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a07e0-129">Windows 7</span></span><br/> <span data-ttu-id="a07e0-130">Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="a07e0-130">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="a07e0-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a07e0-131">Minimum supported server</span></span> | <span data-ttu-id="a07e0-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a07e0-132">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="a07e0-133">Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="a07e0-133">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="a07e0-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a07e0-134">Windows SDK</span></span>              | <span data-ttu-id="a07e0-135">7.0</span><span class="sxs-lookup"><span data-stu-id="a07e0-135">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="a07e0-136">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a07e0-136">Visual Studio</span></span>            | <span data-ttu-id="a07e0-137">2008</span><span class="sxs-lookup"><span data-stu-id="a07e0-137">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="a07e0-138">Header- und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="a07e0-138">Header and IDL files</span></span>     | <span data-ttu-id="a07e0-139">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="a07e0-139">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="a07e0-140">Das [Plattformupdate](https://msdn.microsoft.com/library/dd378748.aspx) für Windows Vista und das Plattformupdate für [Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menübandanwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 als Ziel verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a07e0-140">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a07e0-141">Die Plattformupdates sind für alle Windows Vista- und Windows Server 2008-Kunden über Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a07e0-141">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="a07e0-142">Bei Anwendungen von Drittanbietern, für die ein Plattformupdate für [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein Plattformupdate für Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erforderlich ist, kann Windows Update erkennen, ob das erforderliche Update installiert ist. Ist dies nicht der Windows Update wird es heruntergeladen und im Hintergrund installiert.</span><span class="sxs-lookup"><span data-stu-id="a07e0-142">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





