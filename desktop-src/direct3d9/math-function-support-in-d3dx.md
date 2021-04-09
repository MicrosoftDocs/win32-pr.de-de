---
description: D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124477"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="15a86-104">Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="15a86-104">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="15a86-105">D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="15a86-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="15a86-106">Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.</span><span class="sxs-lookup"><span data-stu-id="15a86-106">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="15a86-107">Mathematik</span><span class="sxs-lookup"><span data-stu-id="15a86-107">Math</span></span>

<span data-ttu-id="15a86-108">Mathematische Unterstützung, die in einer Reihe von Funktionen enthalten ist, wird für Folgendes bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="15a86-108">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="15a86-109">Farb Berechnungen</span><span class="sxs-lookup"><span data-stu-id="15a86-109">Color calculations</span></span>
-   <span data-ttu-id="15a86-110">Back</span><span class="sxs-lookup"><span data-stu-id="15a86-110">Planes</span></span>
-   <span data-ttu-id="15a86-111">Matrix Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="15a86-111">Matrix manipulation</span></span>
-   <span data-ttu-id="15a86-112">Quaternionen</span><span class="sxs-lookup"><span data-stu-id="15a86-112">Quaternions</span></span>
-   <span data-ttu-id="15a86-113">2D-Vektoren</span><span class="sxs-lookup"><span data-stu-id="15a86-113">2D vectors</span></span>
-   <span data-ttu-id="15a86-114">3D-Vektoren</span><span class="sxs-lookup"><span data-stu-id="15a86-114">3D vectors</span></span>
-   <span data-ttu-id="15a86-115">4D-Vektoren</span><span class="sxs-lookup"><span data-stu-id="15a86-115">4D vectors</span></span>

<span data-ttu-id="15a86-116">Beachten Sie, dass bei einer Verbindung mit den C++-über Ladungen die Unterstützung für grundlegende 3D-mathematische Typen sehr umfangreich ist.</span><span class="sxs-lookup"><span data-stu-id="15a86-116">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="15a86-117">Weitere Informationen zu diesen Funktionen finden Sie unter [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="15a86-117">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="15a86-118">Um die benötigte Funktion zu finden, werden Sie in mehreren Ordnern untergliedert.</span><span class="sxs-lookup"><span data-stu-id="15a86-118">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="15a86-119">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="15a86-119">FLOAT16</span></span>

<span data-ttu-id="15a86-120">Bei Verwendung des FLOAT16-Datentyps sollten Sie die Werte auf maximal D3DX \_ 16f begrenzen \_ .</span><span class="sxs-lookup"><span data-stu-id="15a86-120">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="15a86-121">Alle FLOAT16-Werte, die diesen Wert überschreiten, führen zu einem nicht definierten Verhalten in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="15a86-121">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="15a86-122">Siehe [andere D3DX-Konstanten](other-d3dx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="15a86-122">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="15a86-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15a86-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15a86-124">D3DX</span><span class="sxs-lookup"><span data-stu-id="15a86-124">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



