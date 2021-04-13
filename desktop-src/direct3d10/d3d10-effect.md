---
description: Diese Konstanten werden beim Erstellen eines Effekts verwendet, um entweder das Kompilierungs Verhalten oder das Lauf Zeit Effekt Verhalten zu definieren.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: D3D10_EFFECT Konstanten
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342159"
---
# <a name="d3d10_effect-constants"></a><span data-ttu-id="6bf77-103">D3d10 \_ Effect-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6bf77-103">D3D10\_EFFECT Constants</span></span>

<span data-ttu-id="6bf77-104">Diese Konstanten werden beim Erstellen eines Effekts verwendet, um entweder das Kompilierungs Verhalten oder das Lauf Zeit Effekt Verhalten zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6bf77-104">These constants used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span>



| <span data-ttu-id="6bf77-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="6bf77-105">\#define</span></span>                                 | <span data-ttu-id="6bf77-106">Wert</span><span class="sxs-lookup"><span data-stu-id="6bf77-106">Value</span></span>        | <span data-ttu-id="6bf77-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bf77-107">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf77-108">D3d10 \_ Effekt \_ Kompilieren des untergeordneten \_ \_ Effekts</span><span class="sxs-lookup"><span data-stu-id="6bf77-108">D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT</span></span>    | <span data-ttu-id="6bf77-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="6bf77-109">1 << 0</span></span> | <span data-ttu-id="6bf77-110">Kompilieren Sie die FX-Datei mit einem untergeordneten Effekt.</span><span class="sxs-lookup"><span data-stu-id="6bf77-110">Compile the .fx file to a child effect.</span></span> <span data-ttu-id="6bf77-111">Untergeordnete Effekte haben keine Initialisiert für freigegebene Werte, da diese im Effekt Pool initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6bf77-111">Child effects have no initializes for any shared values because these are initialized in the effect pool.</span></span>                                                                                                           |
| <span data-ttu-id="6bf77-112">D3d10 \_ Effekt- \_ Kompilierung \_ \_ langsame \_ Ops zulassen</span><span class="sxs-lookup"><span data-stu-id="6bf77-112">D3D10\_EFFECT\_COMPILE\_ALLOW\_SLOW\_OPS</span></span> | <span data-ttu-id="6bf77-113">1 << 1</span><span class="sxs-lookup"><span data-stu-id="6bf77-113">1 << 1</span></span> | <span data-ttu-id="6bf77-114">Standardmäßig ist der Leistungsmodus aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6bf77-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="6bf77-115">Der Leistungsmodus lässt änderbare Zustands Objekte nicht zu, indem verhindert wird, dass nicht literale Ausdrücke in Zustands Objekt Definitionen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6bf77-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span> <span data-ttu-id="6bf77-116">Wenn Sie dieses Flag angeben, wird der Modus deaktiviert, und es werden änderbare Zustands Objekte zugelassen.</span><span class="sxs-lookup"><span data-stu-id="6bf77-116">Specifying this flag will disable the mode and allow for mutable state objects.</span></span> |
| <span data-ttu-id="6bf77-117">D3d10 \_ Effect \_ Single \_ Thread</span><span class="sxs-lookup"><span data-stu-id="6bf77-117">D3D10\_EFFECT\_SINGLE\_THREADED</span></span>          | <span data-ttu-id="6bf77-118">1 << 3</span><span class="sxs-lookup"><span data-stu-id="6bf77-118">1 << 3</span></span> | <span data-ttu-id="6bf77-119">Versuchen Sie nicht, mit anderen Threads zu synchronisieren, die Auswirkungen in denselben Pool laden.</span><span class="sxs-lookup"><span data-stu-id="6bf77-119">Do not attempt to synchronize with other threads loading effects into the same pool.</span></span>                                                                                                                                                                        |



 

<span data-ttu-id="6bf77-120">Diese Konstanten werden in d3d10effect. h als Makros definiert.</span><span class="sxs-lookup"><span data-stu-id="6bf77-120">These constants are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bf77-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6bf77-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bf77-122">Effekt Konstanten (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="6bf77-122">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



