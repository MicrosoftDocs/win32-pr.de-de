---
description: Die Anwendung kann mit dem Schablonen Puffer 2D-oder 3D-Bilder in eine 3D-Szene zusammensetzen.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Zusammensetzung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344229"
---
# <a name="compositing-direct3d-9"></a><span data-ttu-id="1a357-103">Zusammensetzung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1a357-103">Compositing (Direct3D 9)</span></span>

<span data-ttu-id="1a357-104">Die Anwendung kann mit dem Schablonen Puffer 2D-oder 3D-Bilder in eine 3D-Szene zusammensetzen.</span><span class="sxs-lookup"><span data-stu-id="1a357-104">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="1a357-105">Eine Maske im Schablone-Puffer wird verwendet, um einen Bereich der Renderingzieloberfläche zu okzieren.</span><span class="sxs-lookup"><span data-stu-id="1a357-105">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="1a357-106">Gespeicherte 2D-Informationen, wie z. b. Text oder Bitmaps, können dann in den Bereich "okded" geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1a357-106">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="1a357-107">Alternativ kann die Anwendung zusätzliche 3D-primitive in den mit der Schablone maskierten Bereich der Renderingzieloberfläche rendern.</span><span class="sxs-lookup"><span data-stu-id="1a357-107">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="1a357-108">Sie kann sogar eine ganze Szene darstellen.</span><span class="sxs-lookup"><span data-stu-id="1a357-108">It can even render an entire scene.</span></span>

<span data-ttu-id="1a357-109">Spiele sind häufig mehrere 3D-Szenen zusammengesetzt.</span><span class="sxs-lookup"><span data-stu-id="1a357-109">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="1a357-110">Beispielsweise wird bei Fahr spielen in der Regel eine Spiegelung der Rückseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1a357-110">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="1a357-111">Die Spiegel Datenbank enthält die Ansicht der 3D-Szene hinter dem Treiber.</span><span class="sxs-lookup"><span data-stu-id="1a357-111">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="1a357-112">Es handelt sich im Wesentlichen um eine zweite 3D-Szene, die mit der vorwärts Ansicht des Treibers zusammengesetzt wird</span><span class="sxs-lookup"><span data-stu-id="1a357-112">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a357-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a357-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a357-114">Techniken für Schablonen Puffer</span><span class="sxs-lookup"><span data-stu-id="1a357-114">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



