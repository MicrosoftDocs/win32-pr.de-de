---
title: Installieren von Visualisierungen
description: Installieren von Visualisierungen
ms.assetid: ca391e38-def5-47da-81f7-94aa96530387
keywords:
- Windows Media Player-Plug-ins, Visualisierungen
- Plug-ins, Visualisierungen
- Visualisierungen, installieren
- benutzerdefinierte Visualisierungen, installieren
- Installieren von Visualisierungen
- Visualisierungen, registrieren
- benutzerdefinierte Visualisierungen, registrieren
- Registrierung, Visualisierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1dc8f33d7b5f5b938bee6c89d946955509ab34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337992"
---
# <a name="installing-visualizations"></a><span data-ttu-id="f9215-111">Installieren von Visualisierungen</span><span class="sxs-lookup"><span data-stu-id="f9215-111">Installing Visualizations</span></span>

<span data-ttu-id="f9215-112">Sie müssen einen Installationsvorgang für den Benutzer Ihrer Visualisierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f9215-112">You must provide an installation process for the user of your visualization.</span></span> <span data-ttu-id="f9215-113">Außerdem müssen Sie einen Deinstallations Vorgang für den Benutzer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f9215-113">You must also provide an uninstall process for the user.</span></span> <span data-ttu-id="f9215-114">Von der aktuellen Version von Windows Media Player werden keine Visualisierungen von der Benutzeroberfläche installiert.</span><span class="sxs-lookup"><span data-stu-id="f9215-114">The current version of Windows Media Player does not install visualizations from the user interface.</span></span>

## <a name="installing-to-the-visualization-folder"></a><span data-ttu-id="f9215-115">Installieren im Ordner "Visualisierung"</span><span class="sxs-lookup"><span data-stu-id="f9215-115">Installing to the Visualization Folder</span></span>

<span data-ttu-id="f9215-116">Es wird empfohlen, dass Sie alle Visualisierungen im Unterordner Visualisierungen des Ordners installieren, in dem Windows Media Player installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9215-116">It is recommended that you install all visualizations in the Visualizations subfolder of the folder where Windows Media Player is installed.</span></span>

## <a name="registering-your-visualization"></a><span data-ttu-id="f9215-117">Registrieren der Visualisierung</span><span class="sxs-lookup"><span data-stu-id="f9215-117">Registering Your Visualization</span></span>

<span data-ttu-id="f9215-118">Visualisierungen sind COM-DLLs und befolgen alle normalen Installations-und Entfernungs Regeln.</span><span class="sxs-lookup"><span data-stu-id="f9215-118">Visualizations are COM DLLs and follow all the normal rules of installation and removal.</span></span> <span data-ttu-id="f9215-119">Sie können regsvr32.exe oder andere Installations Tools verwenden, um die Visualisierung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="f9215-119">You can use regsvr32.exe or other installation tools to register your visualization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9215-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9215-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9215-121">**Informationen zu benutzerdefinierten Visualisierungen**</span><span class="sxs-lookup"><span data-stu-id="f9215-121">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




