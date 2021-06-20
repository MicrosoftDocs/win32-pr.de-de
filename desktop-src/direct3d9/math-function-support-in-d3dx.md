---
description: Erfahren Sie mehr über die Unterstützung mathematischer Funktionen in D3DX. D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28c32b13d185694e4ffa41c314cf9f77cbb18b7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407523"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="c1a70-105">Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c1a70-105">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="c1a70-106">D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c1a70-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="c1a70-107">Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.</span><span class="sxs-lookup"><span data-stu-id="c1a70-107">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="c1a70-108">Mathematik</span><span class="sxs-lookup"><span data-stu-id="c1a70-108">Math</span></span>

<span data-ttu-id="c1a70-109">Mathematische Unterstützung, die in einer Reihe von Funktionen enthalten ist, wird für:</span><span class="sxs-lookup"><span data-stu-id="c1a70-109">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="c1a70-110">Farbberechnungen</span><span class="sxs-lookup"><span data-stu-id="c1a70-110">Color calculations</span></span>
-   <span data-ttu-id="c1a70-111">Flugzeuge</span><span class="sxs-lookup"><span data-stu-id="c1a70-111">Planes</span></span>
-   <span data-ttu-id="c1a70-112">Matrixbearbeitung</span><span class="sxs-lookup"><span data-stu-id="c1a70-112">Matrix manipulation</span></span>
-   <span data-ttu-id="c1a70-113">Quaternionen</span><span class="sxs-lookup"><span data-stu-id="c1a70-113">Quaternions</span></span>
-   <span data-ttu-id="c1a70-114">2D-Vektoren</span><span class="sxs-lookup"><span data-stu-id="c1a70-114">2D vectors</span></span>
-   <span data-ttu-id="c1a70-115">3D-Vektoren</span><span class="sxs-lookup"><span data-stu-id="c1a70-115">3D vectors</span></span>
-   <span data-ttu-id="c1a70-116">4D-Vektoren</span><span class="sxs-lookup"><span data-stu-id="c1a70-116">4D vectors</span></span>

<span data-ttu-id="c1a70-117">Beachten Sie, dass in Verbindung mit den C++-Überladungen die Unterstützung für grundlegende 3D-Mathematische Typen umfangreich ist.</span><span class="sxs-lookup"><span data-stu-id="c1a70-117">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="c1a70-118">Weitere Informationen zu diesen Funktionen finden Sie unter [D3DX-Funktionen.](dx9-graphics-reference-d3dx-functions.md)</span><span class="sxs-lookup"><span data-stu-id="c1a70-118">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="c1a70-119">Um die benötigte Funktion zu finden, werden sie in mehrere Ordner aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="c1a70-119">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="c1a70-120">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c1a70-120">FLOAT16</span></span>

<span data-ttu-id="c1a70-121">Wenn Sie den FLOAT16-Datentyp verwenden, achten Sie darauf, die Werte auf ein Maximum von D3DX \_ 16F MAX zu \_ beschränken.</span><span class="sxs-lookup"><span data-stu-id="c1a70-121">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="c1a70-122">Jeder FLOAT16-Wert, der diesen wert überschreitet, führt zu einem nicht definierten Verhalten in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1a70-122">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="c1a70-123">Weitere Informationen finden Sie unter [Andere D3DX-Konstanten.](other-d3dx-constants.md)</span><span class="sxs-lookup"><span data-stu-id="c1a70-123">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1a70-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1a70-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1a70-125">D3dx</span><span class="sxs-lookup"><span data-stu-id="c1a70-125">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



