---
title: Htmleditribbon-Beispiel
description: Dieses Codebeispiel zeigt Markup und Code, die erforderlich sind, um eine vorhandene MFC-Anwendung (Microsoft Foundation Classes) zur Verwendung des Windows-Menübands zu migrieren.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98d4d76508b812d86a4dab38f8dcec96dadc52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040321"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="6c5fd-103">Htmleditribbon-Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c5fd-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="6c5fd-104">Dieses Codebeispiel zeigt Markup und Code, die erforderlich sind, um eine vorhandene MFC-Anwendung (Microsoft Foundation Classes) zur Verwendung des Windows-Menübands zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="6c5fd-105">Es wurde erstellt, indem die vorhandene MFC-HTMLEdit-Beispielanwendung erstellt und der Code und die Ressourcen für die Verwendung des Windows-Menübands geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

-   [<span data-ttu-id="6c5fd-106">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="6c5fd-106">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="6c5fd-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="6c5fd-107">Usage</span></span>](#usage)
    -   [<span data-ttu-id="6c5fd-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="6c5fd-108">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="6c5fd-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6c5fd-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="6c5fd-110">Unterstützung</span><span class="sxs-lookup"><span data-stu-id="6c5fd-110">Support</span></span>](#support)
-   [<span data-ttu-id="6c5fd-111">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="6c5fd-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="6c5fd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c5fd-112">Remarks</span></span>

<span data-ttu-id="6c5fd-113">Das MFC-Beispiel finden Sie unter [HTMLEdit Sample: umschließt das Internet Explorer-Steuerelement für die MSHTML-Bearbeitung](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="6c5fd-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="6c5fd-114">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="6c5fd-114">Usage</span></span>

<span data-ttu-id="6c5fd-115">Das htmleditribbon-Beispiel kann als eigenständiges Microsoft Visual Studio Projekt aus dem [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) heruntergeladen oder als Teil des [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx)installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-115">The HTMLEditRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="6c5fd-116">Microsoft Download Center: [Beispiele für Windows-Menü Bänder](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="6c5fd-116">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="6c5fd-117">Windows Software Development Kit (SDK) (Standard Installationspfad):% Program Files% \\ Microsoft SDKs \\ Windows- \\ \[ Versionsnummer \] \\ Samples \\ WinUI \\ windowsribbon \\ htmleditribbon</span><span class="sxs-lookup"><span data-stu-id="6c5fd-117">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="6c5fd-118">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6c5fd-118">Building the Sample</span></span>

<span data-ttu-id="6c5fd-119">Laden Sie das Beispiel auf Ihre Festplatte herunter.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-119">Download the sample to your hard disk.</span></span>

<span data-ttu-id="6c5fd-120">Installieren Sie den Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-120">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="6c5fd-121">Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-121">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="6c5fd-122">Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-122">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="6c5fd-123">Geben Sie an der Eingabeaufforderung MSBUILD ein.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-123">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="6c5fd-124">Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-124">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="6c5fd-125">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6c5fd-125">Running the Sample</span></span>

<span data-ttu-id="6c5fd-126">Um das Beispiel im Befehlsfenster der Buildumgebung auszuführen, führen Sie die exe-Dateien im \\ Ordner bin Debug oder bin Release aus, \\ der im Beispiel Quellordner enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-126">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="6c5fd-127">Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-127">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="6c5fd-128">Support</span><span class="sxs-lookup"><span data-stu-id="6c5fd-128">Support</span></span>

<span data-ttu-id="6c5fd-129">Das [Windows-Menüband-Entwicklungs Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) steht zur Erörterung von Themen und zum stellen von Fragen im Zusammenhang mit der Entwicklung von Windows-</span><span class="sxs-lookup"><span data-stu-id="6c5fd-129">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="6c5fd-130">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="6c5fd-130">Minimum Requirements</span></span>



| <span data-ttu-id="6c5fd-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c5fd-131">Requirement</span></span> | <span data-ttu-id="6c5fd-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6c5fd-132">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5fd-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c5fd-133">Minimum supported client</span></span> | <span data-ttu-id="6c5fd-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c5fd-134">Windows 7</span></span><br/> <span data-ttu-id="6c5fd-135">Windows Vista mit Service Pack 2 (SP2) und [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c5fd-135">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="6c5fd-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c5fd-136">Minimum supported server</span></span> | <span data-ttu-id="6c5fd-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c5fd-137">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="6c5fd-138">Windows Server 2008 mit SP2 und [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c5fd-138">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="6c5fd-139">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6c5fd-139">Windows SDK</span></span>              | <span data-ttu-id="6c5fd-140">7.0</span><span class="sxs-lookup"><span data-stu-id="6c5fd-140">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="6c5fd-141">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6c5fd-141">Visual Studio</span></span>            | <span data-ttu-id="6c5fd-142">2008</span><span class="sxs-lookup"><span data-stu-id="6c5fd-142">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="6c5fd-143">Header-und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="6c5fd-143">Header and IDL files</span></span>     | <span data-ttu-id="6c5fd-144">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="6c5fd-144">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="6c5fd-145">Das [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und das [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menü Band Anwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-145">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="6c5fd-146">Die Platt Form Updates werden für alle Windows Vista-und Windows Server 2008-Kunden über Windows Update verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-146">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="6c5fd-147">Anwendungen von Drittanbietern, die ein [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen, ob das erforderliche aktualisierte installiert ist. Wenn dies nicht der Fall ist, wird Windows Update im Hintergrund heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-147">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





