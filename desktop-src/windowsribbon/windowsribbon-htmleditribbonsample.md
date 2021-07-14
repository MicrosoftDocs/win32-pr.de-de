---
title: HTMLEditRibbon-Beispiel
description: Dieses Codebeispiel zeigt Markup und Code, der zum Migrieren einer vorhandenen MFC-Anwendung (Microsoft Foundation Classes) zur Verwendung des Windows-Menübands erforderlich ist.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: cfe75d13a69e0122766e51a00bcb1b15d52eab4e
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691709"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="5871c-103">HTMLEditRibbon-Beispiel</span><span class="sxs-lookup"><span data-stu-id="5871c-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="5871c-104">Dieses Codebeispiel zeigt Markup und Code, der zum Migrieren einer vorhandenen MFC-Anwendung (Microsoft Foundation Classes) zur Verwendung des Windows-Menübands erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5871c-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="5871c-105">Sie wurde erstellt, indem die vorhandene MFC HTMLEdit-Beispielanwendung verwendet und deren Code und Ressourcen geändert wurden, um das Windows-Menüband zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5871c-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

- [<span data-ttu-id="5871c-106">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="5871c-106">Remarks</span></span>](#remarks)
- [<span data-ttu-id="5871c-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="5871c-107">Usage</span></span>](#usage)
  - [<span data-ttu-id="5871c-108">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5871c-108">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="5871c-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5871c-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="5871c-110">Support</span><span class="sxs-lookup"><span data-stu-id="5871c-110">Support</span></span>](#support)
- [<span data-ttu-id="5871c-111">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="5871c-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="5871c-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5871c-112">Remarks</span></span>

<span data-ttu-id="5871c-113">Das MFC-Beispiel finden Sie unter [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="5871c-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="5871c-114">Usage</span><span class="sxs-lookup"><span data-stu-id="5871c-114">Usage</span></span>

<span data-ttu-id="5871c-115">Die Windows Menüband-Frameworkbeispiele können als eigenständige Microsoft Visual Studio Projekte aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) heruntergeladen oder als Teil des Windows Software Development Kit [(SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/)installiert werden.</span><span class="sxs-lookup"><span data-stu-id="5871c-115">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="5871c-116">Windows Software Development Kit (SDK) (Standardinstallationspfad): %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="5871c-116">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="5871c-117">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5871c-117">Building the Sample</span></span>

<span data-ttu-id="5871c-118">Laden Sie das Beispiel herunter.</span><span class="sxs-lookup"><span data-stu-id="5871c-118">Download the sample.</span></span>

<span data-ttu-id="5871c-119">Installieren Sie das Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster der Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="5871c-119">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="5871c-120">Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="5871c-120">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="5871c-121">Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="5871c-121">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="5871c-122">Geben Sie an der Eingabeaufforderung MSBUILD ein.</span><span class="sxs-lookup"><span data-stu-id="5871c-122">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="5871c-123">Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.</span><span class="sxs-lookup"><span data-stu-id="5871c-123">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="5871c-124">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5871c-124">Running the Sample</span></span>

<span data-ttu-id="5871c-125">Um das Beispiel im Befehlsfenster der Buildumgebung auszuführen, führen Sie die .exe Dateien im Ordner Bin \\ Debug oder Bin Release \\ aus, der im Beispielquellordner enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5871c-125">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="5871c-126">Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="5871c-126">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="5871c-127">Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5871c-127">Support</span></span>

<span data-ttu-id="5871c-128">Das [Windows Menübandentwicklungsforum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) ist verfügbar, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung Windows Menübandanwendungen zu stellen.</span><span class="sxs-lookup"><span data-stu-id="5871c-128">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="5871c-129">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="5871c-129">Minimum Requirements</span></span>



| <span data-ttu-id="5871c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5871c-130">Requirement</span></span> | <span data-ttu-id="5871c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5871c-131">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5871c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5871c-132">Minimum supported client</span></span> | <span data-ttu-id="5871c-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5871c-133">Windows 7</span></span><br/> <span data-ttu-id="5871c-134">Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="5871c-134">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="5871c-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5871c-135">Minimum supported server</span></span> | <span data-ttu-id="5871c-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5871c-136">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="5871c-137">Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="5871c-137">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="5871c-138">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="5871c-138">Windows SDK</span></span>              | <span data-ttu-id="5871c-139">7.0</span><span class="sxs-lookup"><span data-stu-id="5871c-139">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="5871c-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5871c-140">Visual Studio</span></span>            | <span data-ttu-id="5871c-141">2008</span><span class="sxs-lookup"><span data-stu-id="5871c-141">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="5871c-142">Header- und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="5871c-142">Header and IDL files</span></span>     | <span data-ttu-id="5871c-143">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="5871c-143">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="5871c-144">Das [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und das [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows Menübandanwendungen auf Windows Vista und Windows Server 2008 ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="5871c-144">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="5871c-145">Die Plattformupdates sind über Windows Update für alle Kunden Windows Vista und Windows Server 2008 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5871c-145">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="5871c-146">Für Anwendungen von Drittanbietern, für die [ein Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erforderlich ist, kann Windows Update erkennen, ob das erforderliche Update installiert ist. Andernfalls wird Windows Update heruntergeladen und im Hintergrund installiert.</span><span class="sxs-lookup"><span data-stu-id="5871c-146">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





