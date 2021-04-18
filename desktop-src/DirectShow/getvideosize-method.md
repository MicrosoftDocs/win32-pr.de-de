---
description: Die getvideosize-Methode ruft die nativen Video Dimensionen ab.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Getvideosize-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340098"
---
# <a name="getvideosize-method"></a><span data-ttu-id="f2790-103">Getvideosize-Methode</span><span class="sxs-lookup"><span data-stu-id="f2790-103">GetVideoSize Method</span></span>

> [!Note]  
> <span data-ttu-id="f2790-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2790-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f2790-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f2790-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f2790-106">Die- `GetVideoSize` Methode ruft die nativen Video Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="f2790-106">The `GetVideoSize` method retrieves the native video dimensions.</span></span>

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a><span data-ttu-id="f2790-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2790-107">Return Value</span></span>

<span data-ttu-id="f2790-108">Gibt ein [dvdrect](dvdrect-object.md) -Objekt zurück, das vier Lese-/Schreibeigenschaften enthält: (oben links) x; (oben links) y, Breite und Höhe.</span><span class="sxs-lookup"><span data-stu-id="f2790-108">Returns a [DVDRect](dvdrect-object.md) object containing four read/write properties: (top left) x; (top left) y, Width, and Height.</span></span> <span data-ttu-id="f2790-109">Die **x** -und **y** -Eigenschaften werden auf 0 (null) festgelegt, und die anderen beiden Eigenschaften reflektieren die Breite und Höhe des Video Rechtecks, das auf der Festplatte erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="f2790-109">The **x** and **y** properties are set to zero and the other two properties reflect the width and height of the video rectangle as authored on the disc.</span></span>

 

 



