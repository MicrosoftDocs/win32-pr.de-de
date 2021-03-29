---
description: Die Funktionen getupdatur und getupdatergn rufen den aktuellen Aktualisierungs Bereich für das Fenster ab.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Der Aktualisierungs Bereich wird abgerufen.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215172"
---
# <a name="retrieving-the-update-region"></a><span data-ttu-id="0f1f2-103">Der Aktualisierungs Bereich wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-103">Retrieving the Update Region</span></span>

<span data-ttu-id="0f1f2-104">Die Funktionen [**getupdatur**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) und [**getupdatergn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) rufen den aktuellen Aktualisierungs Bereich für das Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-104">The [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) functions retrieve the current update region for the window.</span></span> <span data-ttu-id="0f1f2-105">Getupdatter Ruft das kleinste Rechteck (in logischen Koordinaten) ab, das den gesamten Update Bereich einschließt.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-105">GetUpdateRect retrieves the smallest rectangle (in logical coordinates) that encloses the entire update region.</span></span> <span data-ttu-id="0f1f2-106">Getupdatergn Ruft den Update Bereich selbst ab.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-106">GetUpdateRgn retrieves the update region itself.</span></span> <span data-ttu-id="0f1f2-107">Diese Funktionen können verwendet werden, um die aktuelle Größe des Aktualisierungs Bereichs zu berechnen und zu bestimmen, wo ein Zeichnungs Vorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-107">These functions can be used to calculate the current size of the update region to determine where to carry out a drawing operation.</span></span>

<span data-ttu-id="0f1f2-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ruft auch die Dimensionen des kleinsten Rechtecks ab, das den aktuellen Aktualisierungs Bereich einschließt, wobei die Dimensionen in den **rcpaint** -Member in der [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) also retrieves the dimensions of the smallest rectangle enclosing the current update region, copying the dimensions to the **rcPaint** member in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="0f1f2-109">Da **BeginPaint** den Update Bereich überprüft, gibt jeder Aufrufe von [**getupdatergn**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) und [**getupdatergn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) unmittelbar nach einem Aufrufen von **BeginPaint** einen leeren Update Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-109">Because **BeginPaint** validates the update region, any call to [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediately after a call to **BeginPaint** returns an empty update region.</span></span>

 

 



