---
title: Simpleribbon-Beispiel
description: Dieses Codebeispiel veranschaulicht, wie eine einfache Windows-Menü Bandanwendung implementiert wird.
ms.assetid: 9196ae63-ca9e-43ae-8b4c-a30f1ef700f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5055d47db2d947778699d55bbae96649b9b45ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478603"
---
# <a name="simpleribbon-sample"></a><span data-ttu-id="c6e37-103">Simpleribbon-Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6e37-103">SimpleRibbon Sample</span></span>

<span data-ttu-id="c6e37-104">Dieses Codebeispiel veranschaulicht, wie eine einfache Windows-Menü Bandanwendung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="c6e37-104">This code sample demonstrates how to implement a simple Windows Ribbon application.</span></span>

-   [<span data-ttu-id="c6e37-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="c6e37-105">Usage</span></span>](#usage)
    -   [<span data-ttu-id="c6e37-106">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="c6e37-106">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="c6e37-107">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c6e37-107">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="c6e37-108">Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c6e37-108">Support</span></span>](#support)
-   [<span data-ttu-id="c6e37-109">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="c6e37-109">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="usage"></a><span data-ttu-id="c6e37-110">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c6e37-110">Usage</span></span>

<span data-ttu-id="c6e37-111">Das simpleribbon-Beispiel kann als eigenständiges Microsoft Visual Studio Projekt aus dem [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) heruntergeladen oder als Teil des [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx)installiert werden.</span><span class="sxs-lookup"><span data-stu-id="c6e37-111">The SimpleRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="c6e37-112">Microsoft Download Center: [Beispiele für Windows-Menü Bänder](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="c6e37-112">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="c6e37-113">Windows Software Development Kit (SDK) (Standard Installationspfad):% Program Files% \\ Microsoft SDKs \\ Windows- \\ \[ Versionsnummer \] \\ Beispiele \\ WinUI \\ windowsribbon \\ simpleribbon</span><span class="sxs-lookup"><span data-stu-id="c6e37-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\SimpleRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="c6e37-114">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c6e37-114">Building the Sample</span></span>

<span data-ttu-id="c6e37-115">Laden Sie das Beispiel auf Ihre Festplatte herunter.</span><span class="sxs-lookup"><span data-stu-id="c6e37-115">Download the sample to your hard disk.</span></span>

<span data-ttu-id="c6e37-116">Installieren Sie den Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="c6e37-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="c6e37-117">Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="c6e37-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="c6e37-118">Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="c6e37-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="c6e37-119">Geben Sie an der Eingabeaufforderung MSBUILD ein.</span><span class="sxs-lookup"><span data-stu-id="c6e37-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="c6e37-120">Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.</span><span class="sxs-lookup"><span data-stu-id="c6e37-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="c6e37-121">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c6e37-121">Running the Sample</span></span>

<span data-ttu-id="c6e37-122">Um das Beispiel im Befehlsfenster der Buildumgebung auszuführen, führen Sie die exe-Dateien im \\ Ordner bin Debug oder bin Release aus, \\ der im Beispiel Quellordner enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c6e37-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="c6e37-123">Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="c6e37-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="c6e37-124">Support</span><span class="sxs-lookup"><span data-stu-id="c6e37-124">Support</span></span>

<span data-ttu-id="c6e37-125">Das [Windows-Menüband-Entwicklungs Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) steht zur Erörterung von Themen und zum stellen von Fragen im Zusammenhang mit der Entwicklung von Windows-</span><span class="sxs-lookup"><span data-stu-id="c6e37-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="c6e37-126">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="c6e37-126">Minimum Requirements</span></span>



| <span data-ttu-id="c6e37-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6e37-127">Requirement</span></span> | <span data-ttu-id="c6e37-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c6e37-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e37-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6e37-129">Minimum supported client</span></span> | <span data-ttu-id="c6e37-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6e37-130">Windows 7</span></span><br/> <span data-ttu-id="c6e37-131">Windows Vista mit Service Pack 2 (SP2) und [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6e37-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="c6e37-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6e37-132">Minimum supported server</span></span> | <span data-ttu-id="c6e37-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6e37-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="c6e37-134">Windows Server 2008 mit SP2 und [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6e37-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="c6e37-135">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c6e37-135">Windows SDK</span></span>              | <span data-ttu-id="c6e37-136">7.0</span><span class="sxs-lookup"><span data-stu-id="c6e37-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="c6e37-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c6e37-137">Visual Studio</span></span>            | <span data-ttu-id="c6e37-138">2008</span><span class="sxs-lookup"><span data-stu-id="c6e37-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="c6e37-139">Header-und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="c6e37-139">Header and IDL files</span></span>     | <span data-ttu-id="c6e37-140">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="c6e37-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="c6e37-141">Das [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und das [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menü Band Anwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="c6e37-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="c6e37-142">Die Platt Form Updates werden für alle Windows Vista-und Windows Server 2008-Kunden über Windows Update verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="c6e37-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="c6e37-143">Anwendungen von Drittanbietern, die ein [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen, ob das erforderliche aktualisierte installiert ist. Wenn dies nicht der Fall ist, wird Windows Update im Hintergrund heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="c6e37-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





