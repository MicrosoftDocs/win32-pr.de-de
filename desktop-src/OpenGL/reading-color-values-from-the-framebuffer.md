---
title: Lesen von Farbwerten aus dem Framebuffer
description: Beachten Sie bei der Verwendung von Funktionen, mit denen Farbwerte aus dem Framebuffer gelesen werden, die Unterschiede zwischen dem Lesen von RGBA-Werten und Farb Indexwerten auf echten Farb Geräten und auf palettenbasierten Geräten.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL unter Windows, Lesen von Farbwerten aus framebuffers
- Lesen von Farbwerten aus Framebuffers OpenGL
- Framebuffers, Lesen von Farbwerten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709359"
---
# <a name="reading-color-values-from-the-framebuffer"></a><span data-ttu-id="e010e-106">Lesen von Farbwerten aus dem Framebuffer</span><span class="sxs-lookup"><span data-stu-id="e010e-106">Reading Color Values from the Framebuffer</span></span>

<span data-ttu-id="e010e-107">Beachten Sie bei der Verwendung von Funktionen, mit denen Farbwerte aus dem Framebuffer gelesen werden, die Unterschiede zwischen dem Lesen von RGBA-Werten und Farb Indexwerten auf echten Farb Geräten und auf palettenbasierten Geräten.</span><span class="sxs-lookup"><span data-stu-id="e010e-107">When using functions that read back color values from the framebuffer, be aware of the differences between reading RGBA values and color-index values on true-color devices and on palette-based devices.</span></span>

<span data-ttu-id="e010e-108">Auf einem echten Farbgerät:</span><span class="sxs-lookup"><span data-stu-id="e010e-108">On a true-color device:</span></span>

-   <span data-ttu-id="e010e-109">RGBA-Werte sind auf den Kanal im Gerät beschränkt.</span><span class="sxs-lookup"><span data-stu-id="e010e-109">RGBA values are limited to the channel in the device.</span></span>
-   <span data-ttu-id="e010e-110">Farb Indexwerte werden im Framebuffer als RGBA-Werte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e010e-110">Color-index values are stored as RGBA values in the framebuffer.</span></span> <span data-ttu-id="e010e-111">Wenn Sie diese Werte verwenden, müssen Sie eine umgekehrte Übersetzung von RGBA zum logischen Palettenindex durchführen.</span><span class="sxs-lookup"><span data-stu-id="e010e-111">When using these values, you must perform an inverse translation from RGBA to the logical palette index.</span></span> <span data-ttu-id="e010e-112">Wenn zwei logische Indizes die gleichen RGBA-Werte aufweisen, kann der falsche Index zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e010e-112">If two logical indexes have the same RGBA values, the wrong index can be returned.</span></span>

<span data-ttu-id="e010e-113">Auf einem palettenbasierten Gerät:</span><span class="sxs-lookup"><span data-stu-id="e010e-113">On a palette-based device:</span></span>

-   <span data-ttu-id="e010e-114">RGBA-Werte werden aus einem Index in der Systempalette gelesen.</span><span class="sxs-lookup"><span data-stu-id="e010e-114">RGBA values are read from an index in the system palette.</span></span> <span data-ttu-id="e010e-115">Der logische Index wird aus einer umgekehrten Tabelle abgerufen, und die RGBA-Komponenten werden extrahiert.</span><span class="sxs-lookup"><span data-stu-id="e010e-115">The logical index is obtained from an inverse table, and the RGBA components are extracted.</span></span>
-   <span data-ttu-id="e010e-116">Farb Indexwerte werden von einem Index in die Systempalette gelesen, und eine umgekehrte Tabelle wird verwendet, um den Index für die logische Palette zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e010e-116">Color-index values are read from an index into the system palette and an inverse table is used to get the logical palette index.</span></span>

 

 




