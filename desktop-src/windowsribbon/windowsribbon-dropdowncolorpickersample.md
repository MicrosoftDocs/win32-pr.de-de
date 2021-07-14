---
title: DropDownColorPicker-Beispiel
description: Dieses Codebeispiel veranschaulicht das Markup und den Code, die für die Verwendung eines Windows DropDownColorPicker-Steuerelements erforderlich sind.
ms.assetid: cc8e18a6-9ed5-47ca-a807-f50838821f14
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 0bb4cb91fdcd5450bd9be5ee70a8ca6c0fe253f6
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691689"
---
# <a name="dropdowncolorpicker-sample"></a><span data-ttu-id="fe927-103">DropDownColorPicker-Beispiel</span><span class="sxs-lookup"><span data-stu-id="fe927-103">DropDownColorPicker Sample</span></span>

<span data-ttu-id="fe927-104">Dieses Codebeispiel veranschaulicht das Markup und den Code, die für die Verwendung eines Windows DropDownColorPicker-Steuerelements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fe927-104">This code sample demonstrates the markup and code required to use a Windows Ribbon DropDownColorPicker control.</span></span>

- [<span data-ttu-id="fe927-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="fe927-105">Usage</span></span>](#usage)
  - [<span data-ttu-id="fe927-106">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="fe927-106">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="fe927-107">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="fe927-107">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="fe927-108">Support</span><span class="sxs-lookup"><span data-stu-id="fe927-108">Support</span></span>](#support)
- [<span data-ttu-id="fe927-109">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="fe927-109">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="fe927-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe927-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="fe927-111">Usage</span><span class="sxs-lookup"><span data-stu-id="fe927-111">Usage</span></span>

<span data-ttu-id="fe927-112">Die Windows Ribbon Framework-Beispiele können als eigenständige Microsoft Visual Studio-Projekte aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) heruntergeladen oder als Teil des Windows Software Development Kit [(SDK) installiert werden.](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="fe927-112">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="fe927-113">Windows Software Development Kit (SDK) (Standardinstallationspfad): %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ WindowsRibbon \\ DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="fe927-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\DropDownColorPicker</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="fe927-114">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="fe927-114">Building the Sample</span></span>

<span data-ttu-id="fe927-115">Laden Sie das Beispiel herunter.</span><span class="sxs-lookup"><span data-stu-id="fe927-115">Download the sample.</span></span>

<span data-ttu-id="fe927-116">Installieren Sie Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster der Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="fe927-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="fe927-117">Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="fe927-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="fe927-118">Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="fe927-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="fe927-119">Geben Sie an der Eingabeaufforderung MSBUILD ein.</span><span class="sxs-lookup"><span data-stu-id="fe927-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="fe927-120">Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.</span><span class="sxs-lookup"><span data-stu-id="fe927-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="fe927-121">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="fe927-121">Running the Sample</span></span>

<span data-ttu-id="fe927-122">Um das Beispiel über das Befehlsfenster der Buildumgebung auszuführen, führen Sie die .exe-Dateien im Ordner Bin Debug oder Bin Release aus, der \\ im Beispielquellenordner \\ enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fe927-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="fe927-123">Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="fe927-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="fe927-124">Unterstützung</span><span class="sxs-lookup"><span data-stu-id="fe927-124">Support</span></span>

<span data-ttu-id="fe927-125">Das [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) steht zur Verfügung, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung Windows Menübandanwendungen zu stellen.</span><span class="sxs-lookup"><span data-stu-id="fe927-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="fe927-126">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="fe927-126">Minimum Requirements</span></span>



| <span data-ttu-id="fe927-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe927-127">Requirement</span></span> | <span data-ttu-id="fe927-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fe927-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe927-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe927-129">Minimum supported client</span></span> | <span data-ttu-id="fe927-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe927-130">Windows 7</span></span><br/> <span data-ttu-id="fe927-131">Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe927-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="fe927-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe927-132">Minimum supported server</span></span> | <span data-ttu-id="fe927-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe927-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="fe927-134">Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe927-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="fe927-135">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="fe927-135">Windows SDK</span></span>              | <span data-ttu-id="fe927-136">7.0</span><span class="sxs-lookup"><span data-stu-id="fe927-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="fe927-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fe927-137">Visual Studio</span></span>            | <span data-ttu-id="fe927-138">2008</span><span class="sxs-lookup"><span data-stu-id="fe927-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="fe927-139">Header- und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="fe927-139">Header and IDL files</span></span>     | <span data-ttu-id="fe927-140">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="fe927-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="fe927-141">Das [Plattformupdate](https://msdn.microsoft.com/library/dd378748.aspx) für Windows Vista und das Plattformupdate für [Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menübandanwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 als Ziel verwenden können.</span><span class="sxs-lookup"><span data-stu-id="fe927-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="fe927-142">Die Plattformupdates sind für alle Windows Vista- und Windows Server 2008-Kunden über Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe927-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="fe927-143">Anwendungen von Drittanbietern, die ein Plattformupdate für [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein Plattformupdate für Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen lassen, ob die erforderliche Aktualisierung installiert ist. Ist dies nicht der Windows Update, wird es im Hintergrund heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="fe927-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fe927-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe927-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe927-145">Dropdownliste Farbwähler</span><span class="sxs-lookup"><span data-stu-id="fe927-145">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="fe927-146">Farbwähler Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe927-146">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 





