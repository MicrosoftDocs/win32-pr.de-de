---
title: Galerie Beispiel
description: Dieses Codebeispiel veranschaulicht das Markup und den Code, die erforderlich sind, um die unterschiedlichen Typen von Katalog Steuerelementen zu verwenden, die im Windows-Menü Band Framework
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aacc52081fbcd2b6b58fd4c2439894705880d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103142"
---
# <a name="gallery-sample"></a><span data-ttu-id="83324-103">Galerie Beispiel</span><span class="sxs-lookup"><span data-stu-id="83324-103">Gallery Sample</span></span>

<span data-ttu-id="83324-104">Dieses Codebeispiel veranschaulicht das Markup und den Code, die erforderlich sind, um die unterschiedlichen Typen von Katalog Steuerelementen zu verwenden, die im Windows-Menü Band Framework</span><span class="sxs-lookup"><span data-stu-id="83324-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="83324-105">Das Beispiel enthält Code, der zum dynamischen Auffüllen von Elementen in den Galerien und zum Behandeln spezieller Katalog-Vorschau Ereignisse verwendet werden kann, die die ergebnisorientierte Benutzeroberfläche unterstützen.</span><span class="sxs-lookup"><span data-stu-id="83324-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

-   [<span data-ttu-id="83324-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="83324-106">Usage</span></span>](#usage)
    -   [<span data-ttu-id="83324-107">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="83324-107">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="83324-108">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="83324-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="83324-109">Unterstützung</span><span class="sxs-lookup"><span data-stu-id="83324-109">Support</span></span>](#support)
-   [<span data-ttu-id="83324-110">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="83324-110">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="83324-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83324-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="83324-112">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="83324-112">Usage</span></span>

<span data-ttu-id="83324-113">Das Galerie Beispiel kann als eigenständiges Microsoft Visual Studio Projekt aus dem [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) heruntergeladen oder als Teil des [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx)installiert werden.</span><span class="sxs-lookup"><span data-stu-id="83324-113">The Gallery Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="83324-114">Microsoft Download Center: [Beispiele für Windows-Menü Bänder](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="83324-114">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="83324-115">Windows Software Development Kit (SDK) (Standard Installationspfad):% Program Files% \\ Microsoft SDKs \\ Windows- \\ \[ Versionsnummer \] \\ Beispiele \\ WinUI \\ windowsribbon \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="83324-115">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="83324-116">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="83324-116">Building the Sample</span></span>

<span data-ttu-id="83324-117">Laden Sie das Beispiel auf Ihre Festplatte herunter.</span><span class="sxs-lookup"><span data-stu-id="83324-117">Download the sample to your hard disk.</span></span>

<span data-ttu-id="83324-118">Installieren Sie den Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="83324-118">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="83324-119">Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="83324-119">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="83324-120">Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="83324-120">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="83324-121">Geben Sie an der Eingabeaufforderung MSBUILD ein.</span><span class="sxs-lookup"><span data-stu-id="83324-121">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="83324-122">Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.</span><span class="sxs-lookup"><span data-stu-id="83324-122">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="83324-123">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="83324-123">Running the Sample</span></span>

<span data-ttu-id="83324-124">Um das Beispiel im Befehlsfenster der Buildumgebung auszuführen, führen Sie die exe-Dateien im \\ Ordner bin Debug oder bin Release aus, \\ der im Beispiel Quellordner enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="83324-124">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="83324-125">Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="83324-125">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="83324-126">Support</span><span class="sxs-lookup"><span data-stu-id="83324-126">Support</span></span>

<span data-ttu-id="83324-127">Das [Windows-Menüband-Entwicklungs Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) steht zur Erörterung von Themen und zum stellen von Fragen im Zusammenhang mit der Entwicklung von Windows-</span><span class="sxs-lookup"><span data-stu-id="83324-127">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="83324-128">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="83324-128">Minimum Requirements</span></span>



| <span data-ttu-id="83324-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83324-129">Requirement</span></span> | <span data-ttu-id="83324-130">Wert</span><span class="sxs-lookup"><span data-stu-id="83324-130">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83324-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83324-131">Minimum supported client</span></span> | <span data-ttu-id="83324-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="83324-132">Windows 7</span></span><br/> <span data-ttu-id="83324-133">Windows Vista mit Service Pack 2 (SP2) und [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="83324-133">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="83324-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83324-134">Minimum supported server</span></span> | <span data-ttu-id="83324-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="83324-135">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="83324-136">Windows Server 2008 mit SP2 und [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="83324-136">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="83324-137">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="83324-137">Windows SDK</span></span>              | <span data-ttu-id="83324-138">7.0</span><span class="sxs-lookup"><span data-stu-id="83324-138">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="83324-139">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="83324-139">Visual Studio</span></span>            | <span data-ttu-id="83324-140">2008</span><span class="sxs-lookup"><span data-stu-id="83324-140">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="83324-141">Header-und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="83324-141">Header and IDL files</span></span>     | <span data-ttu-id="83324-142">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="83324-142">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="83324-143">Das [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und das [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menü Band Anwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="83324-143">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="83324-144">Die Platt Form Updates werden für alle Windows Vista-und Windows Server 2008-Kunden über Windows Update verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="83324-144">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="83324-145">Anwendungen von Drittanbietern, die ein [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen, ob das erforderliche aktualisierte installiert ist. Wenn dies nicht der Fall ist, wird Windows Update im Hintergrund heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="83324-145">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="83324-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83324-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83324-147">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="83324-147">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="83324-148">Kombinations Feld</span><span class="sxs-lookup"><span data-stu-id="83324-148">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="83324-149">Dropdown-Katalog</span><span class="sxs-lookup"><span data-stu-id="83324-149">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="83324-150">In-Ribbon-Katalog</span><span class="sxs-lookup"><span data-stu-id="83324-150">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="83324-151">Split Button-Katalog</span><span class="sxs-lookup"><span data-stu-id="83324-151">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="83324-152">Sammlungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="83324-152">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





