---
description: Eine Farbpalette ist ein Array, das Farb Werte enthält, die die Farben identifizieren, die derzeit auf dem Ausgabegerät angezeigt oder gezeichnet werden können.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Farbpaletten (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130812"
---
# <a name="color-palettes-windows-gdi"></a><span data-ttu-id="18dad-103">Farbpaletten (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="18dad-103">Color Palettes (Windows GDI)</span></span>

<span data-ttu-id="18dad-104">Eine Farbpalette ist ein Array, das Farb Werte enthält, die die Farben identifizieren, die derzeit auf dem Ausgabegerät angezeigt oder gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="18dad-104">A color palette is an array that contains color values identifying the colors that can currently be displayed or drawn on the output device.</span></span> <span data-ttu-id="18dad-105">Farbpaletten werden von Geräten verwendet, die viele Farben erzeugen können, jedoch nur eine Teilmenge dieser zu einem bestimmten Zeitpunkt anzeigen oder zeichnen können.</span><span class="sxs-lookup"><span data-stu-id="18dad-105">Color palettes are used by devices that are capable of generating many colors but that can only display or draw a subset of these at any given time.</span></span> <span data-ttu-id="18dad-106">Bei solchen Geräten verwaltet das System eine *Systempalette* , um die aktuellen Farben des Geräts zu verfolgen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="18dad-106">For such devices, the system maintains a *system palette* to track and manage the current colors of the device.</span></span> <span data-ttu-id="18dad-107">Anwendungen haben keinen direkten Zugriff auf die Systempalette.</span><span class="sxs-lookup"><span data-stu-id="18dad-107">Applications do not have direct access to the system palette.</span></span> <span data-ttu-id="18dad-108">Stattdessen ordnet das System den einzelnen Geräte Kontexten eine Standardpalette zu.</span><span class="sxs-lookup"><span data-stu-id="18dad-108">Instead, the system associates a default palette with each device context.</span></span> <span data-ttu-id="18dad-109">Anwendungen können die Farben in der Standardpalette verwenden oder Ihre eigenen Farben definieren, indem Sie *logische Paletten* erstellen und Sie einzelnen Geräte Kontexten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="18dad-109">Applications can use the colors in the default palette or define their own colors by creating *logical palettes* and associating them with individual device contexts.</span></span>

<span data-ttu-id="18dad-110">Eine Anwendung kann ermitteln, ob ein Gerät Farbpaletten unterstützt, indem das RC- \_ palettenbit im RasterCaps-Wert überprüft wird, der von der [**getdebug**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="18dad-110">An application can determine whether a device supports color palettes by checking for the RC\_PALETTE bit in the RASTERCAPS value returned by the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function.</span></span>

 

 



