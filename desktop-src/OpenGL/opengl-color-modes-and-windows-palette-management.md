---
title: OpenGL-Farbmodi und Windows-Palettenverwaltung
description: Die Microsoft-Implementierung von OpenGL in Windows unterstützt zwei Farbpixel-Daten Modi RGBA und Color-Index-Modi. Windows bietet zwei analoge Möglichkeiten, Farben und Palettenverwaltung Farben zu verarbeiten.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL unter Windows, Farbmodi
- OpenGL unter Windows, Palettenverwaltung
- Palette Management OpenGL
- Farbmodi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309788"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a><span data-ttu-id="eda98-108">OpenGL-Farbmodi und Windows-Palettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="eda98-108">OpenGL Color Modes and Windows Palette Management</span></span>

<span data-ttu-id="eda98-109">Die Microsoft-Implementierung von OpenGL in Windows unterstützt zwei Farbpixel-Daten Modi: RGBA und Color-Index-Modi.</span><span class="sxs-lookup"><span data-stu-id="eda98-109">The Microsoft implementation of OpenGL in Windows supports two color pixel data modes: RGBA and color-index modes.</span></span> <span data-ttu-id="eda98-110">Windows bietet zwei analoge Methoden zur Handhabung von Farben: echte Farb-und Palettenverwaltung.</span><span class="sxs-lookup"><span data-stu-id="eda98-110">Windows provide two analogous ways of handling color: true color and palette management.</span></span>

<span data-ttu-id="eda98-111">Echte Farben Geräte, die in der Lage sind, 16, 24 oder mehr Bits von Farbinformationen pro Pixel zu akzeptieren, können Zehntausende, zehn Millionen oder mehr Farben gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="eda98-111">True-color devices, able to accept 16, 24, or more bits of color information per pixel, can display tens of thousands, tens of millions, or more colors simultaneously.</span></span> <span data-ttu-id="eda98-112">Komplexität entstehen jedoch, wenn eine Anwendung den RGBA-oder Farb Index Modus auf einem palettengerät verwalten muss.</span><span class="sxs-lookup"><span data-stu-id="eda98-112">Complexities arise, however, when an application has to manage RGBA or color-index mode on a palette-type device.</span></span> <span data-ttu-id="eda98-113">Palettengeräte, wie z. b. eine 256-farbige VGA-Anzeige, sind in der Anzahl von Farben, die Sie gleichzeitig anzeigen können, beschränkt.</span><span class="sxs-lookup"><span data-stu-id="eda98-113">Palette-type devices, such as a 256-color VGA display, are limited in the number of colors they can display simultaneously.</span></span> <span data-ttu-id="eda98-114">Anwendungen müssen eine Reihe komplizierter Details verarbeiten, um Geräte mit Palettentyp erfolgreich verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="eda98-114">Applications must handle a number of tricky details to successfully use palette-type devices.</span></span> <span data-ttu-id="eda98-115">Da im farbindexmodusprogramm keine Hardware Palette verwendet wird, ist die Verwendung mit echten Farb Geräten schwieriger als Programme, die den RGBA-Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="eda98-115">Because color-index mode programs don't use a hardware palette, they are more difficult to use with true-color devices than programs using the RGBA mode.</span></span>

 

 




