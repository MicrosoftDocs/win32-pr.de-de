---
description: Diese Konstanten gelten für Auswirkung-Variablen.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE Konstanten
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343965"
---
# <a name="d3d10_effect_variable-constants"></a><span data-ttu-id="48d38-103">D3d10 \_ Effect- \_ Variablen Konstanten</span><span class="sxs-lookup"><span data-stu-id="48d38-103">D3D10\_EFFECT\_VARIABLE Constants</span></span>

<span data-ttu-id="48d38-104">Diese Konstanten gelten für Auswirkung-Variablen.</span><span class="sxs-lookup"><span data-stu-id="48d38-104">These constants apply to effect variables.</span></span>



| <span data-ttu-id="48d38-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="48d38-105">\#define</span></span>                                       | <span data-ttu-id="48d38-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48d38-106">Description</span></span>  | <span data-ttu-id="48d38-107">Wert</span><span class="sxs-lookup"><span data-stu-id="48d38-107">Value</span></span>                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d38-108">D3d10 \_ Effect- \_ Variablen \_ Anmerkung</span><span class="sxs-lookup"><span data-stu-id="48d38-108">D3D10\_EFFECT\_VARIABLE\_ANNOTATION</span></span>            | <span data-ttu-id="48d38-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="48d38-109">1 << 0</span></span> | <span data-ttu-id="48d38-110">Gibt an, dass dies eine Anmerkung oder eine globale Variable ist.</span><span class="sxs-lookup"><span data-stu-id="48d38-110">Indicates that this is an annotation or a global variable.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="48d38-111">D3d10 \_ Effect- \_ Variable in \_ Pooled</span><span class="sxs-lookup"><span data-stu-id="48d38-111">D3D10\_EFFECT\_VARIABLE\_POOLED</span></span>                | <span data-ttu-id="48d38-112">1 << 1</span><span class="sxs-lookup"><span data-stu-id="48d38-112">1 << 1</span></span> | <span data-ttu-id="48d38-113">Gibt an, dass sich diese Variable oder der Konstantenpuffer in einem Effekt Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="48d38-113">Indicates that this variable or constant buffer resides in an effect pool.</span></span> <span data-ttu-id="48d38-114">Wenn dieses Flag nicht festgelegt ist, befindet sich die Variable in einem eigenständigen Effekt oder einem untergeordneten Effekt (eigenständige Effekte geben false aus [**ID3D10Effect:: ispool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool)zurück.</span><span class="sxs-lookup"><span data-stu-id="48d38-114">If this flag is not set, then the variable resides in a standalone effect or a child effect (standalone effects return false from [**ID3D10Effect::IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span></span> |
| <span data-ttu-id="48d38-115">D3d10 \_ - \_ Variable ( \_ expliziter \_ Bindungs \_ Punkt)</span><span class="sxs-lookup"><span data-stu-id="48d38-115">D3D10\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT</span></span> | <span data-ttu-id="48d38-116">1 << 2</span><span class="sxs-lookup"><span data-stu-id="48d38-116">1 << 2</span></span> | <span data-ttu-id="48d38-117">Gibt an, dass die Variable mithilfe des Register-Schlüssel Worts explizit gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="48d38-117">Indicates that the variable has been explicitly bound using the register keyword.</span></span>                                                                                                                                                                                 |



 

<span data-ttu-id="48d38-118">Diese Flags sind in d3d10effect. h als Makros definiert.</span><span class="sxs-lookup"><span data-stu-id="48d38-118">These flags are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48d38-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48d38-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48d38-120">Effekt Konstanten (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="48d38-120">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



