---
title: Dropdowncolorpicker-Beispiel
description: Dieses Codebeispiel veranschaulicht das Markup und den Code, die für die Verwendung eines Windows-Menübands dropdowncolorpicker-Steuer Elements erforderlich sind
ms.assetid: cc8e18a6-9ed5-47ca-a807-f50838821f14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000db12fbc3b3f7ace679e4e8b1f4756d59f6e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103935"
---
# <a name="dropdowncolorpicker-sample"></a><span data-ttu-id="e7f02-103">Dropdowncolorpicker-Beispiel</span><span class="sxs-lookup"><span data-stu-id="e7f02-103">DropDownColorPicker Sample</span></span>

<span data-ttu-id="e7f02-104">Dieses Codebeispiel veranschaulicht das Markup und den Code, die für die Verwendung eines Windows-Menübands dropdowncolorpicker-Steuer Elements erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="e7f02-104">This code sample demonstrates the markup and code required to use a Windows Ribbon DropDownColorPicker control.</span></span>

-   [<span data-ttu-id="e7f02-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="e7f02-105">Usage</span></span>](#usage)
    -   [<span data-ttu-id="e7f02-106">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="e7f02-106">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="e7f02-107">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="e7f02-107">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="e7f02-108">Unterstützung</span><span class="sxs-lookup"><span data-stu-id="e7f02-108">Support</span></span>](#support)
-   [<span data-ttu-id="e7f02-109">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="e7f02-109">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="e7f02-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7f02-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="e7f02-111">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="e7f02-111">Usage</span></span>

<span data-ttu-id="e7f02-112">Das dropdowncolorpicker-Beispiel kann als eigenständiges Microsoft Visual Studio Projekt aus dem [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) heruntergeladen oder als Teil des [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx)installiert werden.</span><span class="sxs-lookup"><span data-stu-id="e7f02-112">The DropDownColorPicker Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="e7f02-113">Microsoft Download Center: [Beispiele für Windows-Menü Bänder](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="e7f02-113">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="e7f02-114">Windows Software Development Kit (SDK) (Standard Installationspfad):% Program Files% \\ Microsoft SDKs \\ Windows- \\ \[ Versionsnummer \] \\ Beispiele \\ WinUI \\ windowsribbon \\ dropdowncolorpicker</span><span class="sxs-lookup"><span data-stu-id="e7f02-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\DropDownColorPicker</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="e7f02-115">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="e7f02-115">Building the Sample</span></span>

<span data-ttu-id="e7f02-116">Laden Sie das Beispiel auf Ihre Festplatte herunter.</span><span class="sxs-lookup"><span data-stu-id="e7f02-116">Download the sample to your hard disk.</span></span>

<span data-ttu-id="e7f02-117">Installieren Sie den Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="e7f02-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="e7f02-118">Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="e7f02-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="e7f02-119">Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="e7f02-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="e7f02-120">Geben Sie an der Eingabeaufforderung MSBUILD ein.</span><span class="sxs-lookup"><span data-stu-id="e7f02-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="e7f02-121">Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.</span><span class="sxs-lookup"><span data-stu-id="e7f02-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="e7f02-122">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="e7f02-122">Running the Sample</span></span>

<span data-ttu-id="e7f02-123">Um das Beispiel im Befehlsfenster der Buildumgebung auszuführen, führen Sie die exe-Dateien im \\ Ordner bin Debug oder bin Release aus, \\ der im Beispiel Quellordner enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e7f02-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="e7f02-124">Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="e7f02-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="e7f02-125">Support</span><span class="sxs-lookup"><span data-stu-id="e7f02-125">Support</span></span>

<span data-ttu-id="e7f02-126">Das [Windows-Menüband-Entwicklungs Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) steht zur Erörterung von Themen und zum stellen von Fragen im Zusammenhang mit der Entwicklung von Windows-</span><span class="sxs-lookup"><span data-stu-id="e7f02-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="e7f02-127">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="e7f02-127">Minimum Requirements</span></span>



| <span data-ttu-id="e7f02-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7f02-128">Requirement</span></span> | <span data-ttu-id="e7f02-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e7f02-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f02-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7f02-130">Minimum supported client</span></span> | <span data-ttu-id="e7f02-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7f02-131">Windows 7</span></span><br/> <span data-ttu-id="e7f02-132">Windows Vista mit Service Pack 2 (SP2) und [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f02-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="e7f02-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7f02-133">Minimum supported server</span></span> | <span data-ttu-id="e7f02-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7f02-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="e7f02-135">Windows Server 2008 mit SP2 und [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f02-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="e7f02-136">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e7f02-136">Windows SDK</span></span>              | <span data-ttu-id="e7f02-137">7.0</span><span class="sxs-lookup"><span data-stu-id="e7f02-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="e7f02-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e7f02-138">Visual Studio</span></span>            | <span data-ttu-id="e7f02-139">2008</span><span class="sxs-lookup"><span data-stu-id="e7f02-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="e7f02-140">Header-und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="e7f02-140">Header and IDL files</span></span>     | <span data-ttu-id="e7f02-141">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="e7f02-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="e7f02-142">Das [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und das [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menü Band Anwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="e7f02-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="e7f02-143">Die Platt Form Updates werden für alle Windows Vista-und Windows Server 2008-Kunden über Windows Update verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="e7f02-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="e7f02-144">Anwendungen von Drittanbietern, die ein [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen, ob das erforderliche aktualisierte installiert ist. Wenn dies nicht der Fall ist, wird Windows Update im Hintergrund heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="e7f02-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e7f02-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7f02-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7f02-146">Dropdown-Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="e7f02-146">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="e7f02-147">Farbauswahl Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7f02-147">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 





