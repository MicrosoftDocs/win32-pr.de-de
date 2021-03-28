---
title: Initialisieren der Mosaik Phase
description: In diesem Thema wird gezeigt, wie die Mosaik Stufe initialisiert wird.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992742"
---
# <a name="how-to-initialize-the-tessellator-stage"></a><span data-ttu-id="a8059-103">Gewusst wie: Initialisieren der Mosaik Phase</span><span class="sxs-lookup"><span data-stu-id="a8059-103">How To: Initialize the Tessellator Stage</span></span>

<span data-ttu-id="a8059-104">Im Allgemeinen erweitert das Mosaik Modell das kompakte, benutzerdefinierte Modell eines Patches in Geometry, das eine programmierbare Menge von Details enthält.</span><span class="sxs-lookup"><span data-stu-id="a8059-104">In general, tessellation expands the compact, user-defined, model of a patch into geometry that contains a programmable amount of detail.</span></span> <span data-ttu-id="a8059-105">Die Geometrie ist in der Regel eine Gruppe von Dreiecken, die eine detaillierte Oberflächengeometrie darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8059-105">The geometry is typically a set of triangles that represents detailed surface geometry.</span></span> <span data-ttu-id="a8059-106">In diesem Thema wird gezeigt, wie die Mosaik Stufe initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a8059-106">This topic shows how to initialize the tessellator stage.</span></span>

<span data-ttu-id="a8059-107">Die Mosaik Phase ist die zweite von drei Phasen, die zusammenarbeiten, um eine Oberfläche zu Mosaik oder zu Kacheln.</span><span class="sxs-lookup"><span data-stu-id="a8059-107">The tessellator stage is the second of three stages that work together to tessellate or tile a surface.</span></span> <span data-ttu-id="a8059-108">Die erste Phase ist die Hull-Shader-Stufe. Es wird einmal pro Patch betrieben und konfiguriert, wie sich die nächste Stufe (der Mosaik-Mosaik Prozess) verhält.</span><span class="sxs-lookup"><span data-stu-id="a8059-108">The first stage is the hull-shader stage; it operates once per patch and configures how the next stage (the fixed function tessellator) behaves.</span></span> <span data-ttu-id="a8059-109">Ein Hull-Shader generiert auch benutzerdefinierte Ausgaben, wie z. b. Ausgabe Steuerungs Punkte und Patch-Konstanten, die über den Mosaik Prozess direkt an die dritte Phase gesendet werden, die Domäne-Shader-Stufe.</span><span class="sxs-lookup"><span data-stu-id="a8059-109">A hull shader also generates user-defined outputs such as output-control points and patch constants that are sent past the tessellator directly to the third stage, the domain-shader stage.</span></span> <span data-ttu-id="a8059-110">Ein Domänen-Shader wird einmal pro Mosaik-Stagingpunkt aufgerufen und wertet Oberflächen Positionen aus.</span><span class="sxs-lookup"><span data-stu-id="a8059-110">A domain shader is invoked once per tessellator-stage point and evaluates surface positions.</span></span>

<span data-ttu-id="a8059-111">Die Mosaik Phase ist eine fixierte Funktions Phase, es ist kein Shader vorhanden, der generiert werden kann, und es kann kein Zustand festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a8059-111">The tessellator stage is a fixed function stage, there is no shader to generate, and no state to set.</span></span> <span data-ttu-id="a8059-112">Er empfängt seinen gesamten Setup Status aus der Hull-Shader-Stufe. Nachdem die Hülle-Shader-Stufe initialisiert wurde, wird die Mosaik Phase automatisch initialisiert.</span><span class="sxs-lookup"><span data-stu-id="a8059-112">It receives all of its setup state from the hull-shader stage; once the hull-shader stage has been initialized, the tessellator stage is automatically initialized.</span></span>

<span data-ttu-id="a8059-113">**So initialisieren Sie die Mosaik Phase**</span><span class="sxs-lookup"><span data-stu-id="a8059-113">**To initialize the tessellator stage**</span></span>

-   <span data-ttu-id="a8059-114">Initialisieren Sie die Hull-Shader-Phase mit [**Verknüpfung id3d11devicecontext aus:: hssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="a8059-114">Initialize the hull-shader stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    <span data-ttu-id="a8059-115">*ppclassinhaltungen* ist ein Zeiger auf ein Array von shaderschnittstellen, dargestellt durch [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) -Zeiger und die Anzahl der Schnittstellen, die durch *numclassinhaltungen* dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a8059-115">*ppClassInstances* is a pointer to an array of shader interfaces, represented by [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointers and the number of interfaces, represented by *NumClassInstances*.</span></span> <span data-ttu-id="a8059-116">Wenn Sie nicht verwendet werden, können diese Parameter auf **null** bzw. 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a8059-116">If not used, these parameters can be set to **NULL** and 0 respectively.</span></span>

<span data-ttu-id="a8059-117">Nachdem die Hull-Shader-Stufe initialisiert wurde, sollten Sie auch die Domäne-Shader-Stufe initialisieren.</span><span class="sxs-lookup"><span data-stu-id="a8059-117">After the hull-shader stage is initialized, you should also initialize the domain-shader stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8059-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8059-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8059-119">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a8059-119">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="a8059-120">Mosaik Übersicht</span><span class="sxs-lookup"><span data-stu-id="a8059-120">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




