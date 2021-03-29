---
description: Durch Farbmischung können Anwendungen neue Farben erstellen, indem Sie den Stift oder die Pinsel Farbe mit Farben im vorhandenen Bild kombinieren.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Farbmischung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130813"
---
# <a name="color-mixing"></a><span data-ttu-id="843cc-103">Farbmischung</span><span class="sxs-lookup"><span data-stu-id="843cc-103">Color Mixing</span></span>

<span data-ttu-id="843cc-104">Durch Farbmischung können Anwendungen neue Farben erstellen, indem Sie den Stift oder die Pinsel Farbe mit Farben im vorhandenen Bild kombinieren.</span><span class="sxs-lookup"><span data-stu-id="843cc-104">Color mixing lets an application create new colors by combining the pen or brush color with colors in the existing image.</span></span> <span data-ttu-id="843cc-105">Die Anwendung kann auswählen, ob der Stift oder die Pinsel Farbe unverändert gezeichnet werden soll (wodurch ein vorhandenes Bild tatsächlich gezeichnet wird) oder die Farbe mit den bereits vorhandenen Farben gemischt werden soll.</span><span class="sxs-lookup"><span data-stu-id="843cc-105">The application can choose either to draw the pen or brush color as is (effectively drawing over any existing image) or to mix the color with the colors already present.</span></span>

<span data-ttu-id="843cc-106">Der Vordergrund Mischungs Modus, der manchmal als binärer Raster Vorgang bezeichnet wird, bestimmt, wie diese Farben gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="843cc-106">The foreground mix mode, sometimes called the binary raster operation, determines how these colors are mixed.</span></span> <span data-ttu-id="843cc-107">Eine Anwendung kann Farben zusammenführen, wobei alle Komponenten beider Farben beibehalten werden. Masken Farben, entfernen oder moderieren von Komponenten, die nicht häufig vorkommen; oder exklusiv Masken Farben, entfernen oder moderieren allgemeiner Komponenten.</span><span class="sxs-lookup"><span data-stu-id="843cc-107">An application can merge colors, preserving all components of both colors; mask colors, removing or moderating components that are not common; or exclusively mask colors, removing or moderating components that are common.</span></span> <span data-ttu-id="843cc-108">Es gibt mehrere Variationen dieser grundlegenden Mischungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="843cc-108">There are several variations on these basic mixing operations.</span></span>

<span data-ttu-id="843cc-109">Farbmischung unterliegt der Farb Näherung.</span><span class="sxs-lookup"><span data-stu-id="843cc-109">Color mixing is subject to color approximation.</span></span> <span data-ttu-id="843cc-110">Wenn das Ergebnis der Farbmischung eine Farbe ist, die das Gerät nicht generieren kann, gleicht das System das Ergebnis mithilfe einer Farbe, die es generieren kann.</span><span class="sxs-lookup"><span data-stu-id="843cc-110">If the result of color mixing is a color that the device cannot generate, the system approximates the result, using a color it can generate.</span></span> <span data-ttu-id="843cc-111">Wenn eine Anwendung Dithering-Farben vermischt, werden die einzelnen Farben, die zum Erstellen der Dithering-Farbe verwendet werden, gemischt, und die Ergebnisse unterliegen der Farb Näherung.</span><span class="sxs-lookup"><span data-stu-id="843cc-111">If an application mixes dithered colors, the individual colors used to create the dithered color are mixed, and the results are subject to color approximation.</span></span>

<span data-ttu-id="843cc-112">Eine Anwendung legt den Vordergrund Mischungs Modus mithilfe der [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) -Funktion fest und ruft den aktuellen Modus mithilfe der [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) -Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="843cc-112">An application sets the foreground mix mode by using the [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) function and retrieves the current mode by using the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) function.</span></span>

<span data-ttu-id="843cc-113">Obwohl es einen Hintergrund Mischungs Modus gibt, steuert dieser Modus nicht die Mischung von Farben.</span><span class="sxs-lookup"><span data-stu-id="843cc-113">Although there is a background mix mode, that mode does not control the mixing of colors.</span></span> <span data-ttu-id="843cc-114">Stattdessen wird angegeben, ob eine Hintergrundfarbe beim Zeichnen von formatierten Linien, ausstrichen und Text verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="843cc-114">Instead, it specifies whether a background color is used when drawing styled lines, hatched brushes, and text.</span></span>

 

 



