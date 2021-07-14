---
title: FontControl-Beispiel
description: Dieses Codebeispiel veranschaulicht das Markup und den Code, die zum Implementieren eines FontControl-Ausdrucks innerhalb einer Windows Ribbon-Anwendung erforderlich sind.
ms.assetid: 8fb84bd1-5e63-447c-b7a0-b3d7cb8c3be7
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 52a81a1a1950305437a7bbc68aab95876b3a6374
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691759"
---
# <a name="fontcontrol-sample"></a><span data-ttu-id="ac4e5-103">FontControl-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ac4e5-103">FontControl Sample</span></span>

<span data-ttu-id="ac4e5-104">Dieses Codebeispiel veranschaulicht das Markup und den Code, die zum Implementieren eines FontControl-Ausdrucks innerhalb einer Windows Ribbon-Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-104">This code sample demonstrates the markup and code required to implement a FontControl within a Windows Ribbon application.</span></span>

- [<span data-ttu-id="ac4e5-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="ac4e5-105">Usage</span></span>](#usage)
  - [<span data-ttu-id="ac4e5-106">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ac4e5-106">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="ac4e5-107">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ac4e5-107">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="ac4e5-108">Support</span><span class="sxs-lookup"><span data-stu-id="ac4e5-108">Support</span></span>](#support)
- [<span data-ttu-id="ac4e5-109">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="ac4e5-109">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="ac4e5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac4e5-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="ac4e5-111">Usage</span><span class="sxs-lookup"><span data-stu-id="ac4e5-111">Usage</span></span>

<span data-ttu-id="ac4e5-112">Die Windows Menüband-Frameworkbeispiele können als eigenständige Microsoft Visual Studio Projekte aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) heruntergeladen oder als Teil des Windows Software Development Kit [(SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/)installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-112">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="ac4e5-113">Windows Software Development Kit (SDK) (Standardinstallationspfad): %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ WindowsRibbon \\ FontControl</span><span class="sxs-lookup"><span data-stu-id="ac4e5-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\FontControl</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="ac4e5-114">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ac4e5-114">Building the Sample</span></span>

<span data-ttu-id="ac4e5-115">Laden Sie das Beispiel herunter.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-115">Download the sample.</span></span>

<span data-ttu-id="ac4e5-116">Installieren Sie das Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster der Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="ac4e5-117">Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="ac4e5-118">Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="ac4e5-119">Geben Sie an der Eingabeaufforderung MSBUILD ein.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="ac4e5-120">Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="ac4e5-121">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ac4e5-121">Running the Sample</span></span>

<span data-ttu-id="ac4e5-122">Um das Beispiel im Befehlsfenster der Buildumgebung auszuführen, führen Sie die .exe Dateien im Ordner Bin \\ Debug oder Bin Release \\ aus, der im Beispielquellordner enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="ac4e5-123">Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="ac4e5-124">Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ac4e5-124">Support</span></span>

<span data-ttu-id="ac4e5-125">Das [Windows Menübandentwicklungsforum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) ist verfügbar, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung Windows Menübandanwendungen zu stellen.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="ac4e5-126">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="ac4e5-126">Minimum Requirements</span></span>



| <span data-ttu-id="ac4e5-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac4e5-127">Requirement</span></span> | <span data-ttu-id="ac4e5-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ac4e5-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4e5-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac4e5-129">Minimum supported client</span></span> | <span data-ttu-id="ac4e5-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ac4e5-130">Windows 7</span></span><br/> <span data-ttu-id="ac4e5-131">Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac4e5-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="ac4e5-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac4e5-132">Minimum supported server</span></span> | <span data-ttu-id="ac4e5-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac4e5-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="ac4e5-134">Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac4e5-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="ac4e5-135">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="ac4e5-135">Windows SDK</span></span>              | <span data-ttu-id="ac4e5-136">7.0</span><span class="sxs-lookup"><span data-stu-id="ac4e5-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="ac4e5-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ac4e5-137">Visual Studio</span></span>            | <span data-ttu-id="ac4e5-138">2008</span><span class="sxs-lookup"><span data-stu-id="ac4e5-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="ac4e5-139">Header- und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="ac4e5-139">Header and IDL files</span></span>     | <span data-ttu-id="ac4e5-140">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="ac4e5-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="ac4e5-141">Das [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und das [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows Menübandanwendungen auf Windows Vista und Windows Server 2008 ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="ac4e5-142">Die Plattformupdates sind über Windows Update für alle Kunden von Windows Vista und Windows Server 2008 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="ac4e5-143">Drittanbieteranwendungen, die [Plattformupdates für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen, ob das erforderliche Update installiert ist. Andernfalls wird Windows Update heruntergeladen und im Hintergrund installiert.</span><span class="sxs-lookup"><span data-stu-id="ac4e5-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ac4e5-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac4e5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac4e5-145">Schriftartsteuerelement</span><span class="sxs-lookup"><span data-stu-id="ac4e5-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="ac4e5-146">Eigenschaften des Schriftartsteuerelements</span><span class="sxs-lookup"><span data-stu-id="ac4e5-146">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> </dl>

 

 





