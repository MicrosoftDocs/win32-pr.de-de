---
title: Katalogbeispiel
description: Dieses Codebeispiel veranschaulicht das Markup und den Code, die erforderlich sind, um die verschiedenen Typen von Katalogsteuerelementen zu verwenden, die im Menübandframework Windows sind.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: ef776a8a1a8eadf9ee41cf9964066cc612a9f9a1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691749"
---
# <a name="gallery-sample"></a><span data-ttu-id="f1b92-103">Katalogbeispiel</span><span class="sxs-lookup"><span data-stu-id="f1b92-103">Gallery Sample</span></span>

<span data-ttu-id="f1b92-104">Dieses Codebeispiel veranschaulicht das Markup und den Code, die erforderlich sind, um die verschiedenen Typen von Katalogsteuerelementen zu verwenden, die im Menübandframework Windows sind.</span><span class="sxs-lookup"><span data-stu-id="f1b92-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="f1b92-105">Das Beispiel enthält Code, der verwendet werden kann, um Elemente dynamisch in die Kataloge zu füllen und spezielle Katalogvorschauereignisse zu behandeln, die eine ergebnisorientierte Benutzeroberfläche unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f1b92-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

- [<span data-ttu-id="f1b92-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="f1b92-106">Usage</span></span>](#usage)
  - [<span data-ttu-id="f1b92-107">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f1b92-107">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="f1b92-108">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f1b92-108">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="f1b92-109">Support</span><span class="sxs-lookup"><span data-stu-id="f1b92-109">Support</span></span>](#support)
- [<span data-ttu-id="f1b92-110">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="f1b92-110">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="f1b92-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f1b92-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="f1b92-112">Usage</span><span class="sxs-lookup"><span data-stu-id="f1b92-112">Usage</span></span>

<span data-ttu-id="f1b92-113">Die Windows Ribbon Framework-Beispiele können als eigenständige Microsoft Visual Studio-Projekte aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) heruntergeladen oder als Teil des Windows Software Development Kit [(SDK) installiert werden.](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="f1b92-113">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="f1b92-114">Windows Software Development Kit (SDK) (Standardinstallationspfad): %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ WindowsRibbon \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="f1b92-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="f1b92-115">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f1b92-115">Building the Sample</span></span>

<span data-ttu-id="f1b92-116">Laden Sie das Beispiel herunter.</span><span class="sxs-lookup"><span data-stu-id="f1b92-116">Download the sample.</span></span>

<span data-ttu-id="f1b92-117">Installieren Sie Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster der Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="f1b92-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="f1b92-118">Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="f1b92-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="f1b92-119">Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="f1b92-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="f1b92-120">Geben Sie an der Eingabeaufforderung MSBUILD ein.</span><span class="sxs-lookup"><span data-stu-id="f1b92-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="f1b92-121">Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.</span><span class="sxs-lookup"><span data-stu-id="f1b92-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="f1b92-122">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f1b92-122">Running the Sample</span></span>

<span data-ttu-id="f1b92-123">Um das Beispiel über das Befehlsfenster der Buildumgebung auszuführen, führen Sie die .exe-Dateien im Ordner Bin Debug oder Bin Release aus, der \\ im Beispielquellenordner \\ enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f1b92-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="f1b92-124">Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="f1b92-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="f1b92-125">Unterstützung</span><span class="sxs-lookup"><span data-stu-id="f1b92-125">Support</span></span>

<span data-ttu-id="f1b92-126">Das [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) steht zur Verfügung, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung Windows Menübandanwendungen zu stellen.</span><span class="sxs-lookup"><span data-stu-id="f1b92-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="f1b92-127">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="f1b92-127">Minimum Requirements</span></span>



| <span data-ttu-id="f1b92-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1b92-128">Requirement</span></span> | <span data-ttu-id="f1b92-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f1b92-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b92-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1b92-130">Minimum supported client</span></span> | <span data-ttu-id="f1b92-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f1b92-131">Windows 7</span></span><br/> <span data-ttu-id="f1b92-132">Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1b92-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="f1b92-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1b92-133">Minimum supported server</span></span> | <span data-ttu-id="f1b92-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1b92-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="f1b92-135">Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1b92-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="f1b92-136">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f1b92-136">Windows SDK</span></span>              | <span data-ttu-id="f1b92-137">7.0</span><span class="sxs-lookup"><span data-stu-id="f1b92-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="f1b92-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1b92-138">Visual Studio</span></span>            | <span data-ttu-id="f1b92-139">2008</span><span class="sxs-lookup"><span data-stu-id="f1b92-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="f1b92-140">Header- und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="f1b92-140">Header and IDL files</span></span>     | <span data-ttu-id="f1b92-141">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="f1b92-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="f1b92-142">Das [Plattformupdate](https://msdn.microsoft.com/library/dd378748.aspx) für Windows Vista und das Plattformupdate für [Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menübandanwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 als Ziel verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f1b92-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="f1b92-143">Die Plattformupdates sind für alle Windows Vista- und Windows Server 2008-Kunden über Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f1b92-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="f1b92-144">Bei Anwendungen von Drittanbietern, für die ein Plattformupdate für [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein Plattformupdate für Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erforderlich ist, kann Windows Update erkennen, ob das erforderliche Update installiert ist. Ist dies nicht der Windows Update wird es heruntergeladen und im Hintergrund installiert.</span><span class="sxs-lookup"><span data-stu-id="f1b92-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f1b92-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f1b92-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1b92-146">Arbeiten mit Katalogen</span><span class="sxs-lookup"><span data-stu-id="f1b92-146">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="f1b92-147">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="f1b92-147">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="f1b92-148">Dropdownkatalog</span><span class="sxs-lookup"><span data-stu-id="f1b92-148">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="f1b92-149">Katalog im Menüband</span><span class="sxs-lookup"><span data-stu-id="f1b92-149">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="f1b92-150">Katalog mit geteilten Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="f1b92-150">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="f1b92-151">Sammlungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1b92-151">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





