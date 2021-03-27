---
title: Verwenden der Shader-Verknüpfung
description: Wir zeigen, wie vorkompilierte HLSL-Funktionen erstellt, in Bibliotheken Verpacken und zur Laufzeit mit vollständigen Shadern verknüpft werden.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729913"
---
# <a name="using-shader-linking"></a><span data-ttu-id="d8152-103">Verwenden der Shader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="d8152-103">Using shader linking</span></span>

<span data-ttu-id="d8152-104">Wir zeigen, wie vorkompilierte HLSL-Funktionen erstellt, in Bibliotheken Verpacken und zur Laufzeit mit vollständigen Shadern verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="d8152-104">We show how to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run-time.</span></span> <span data-ttu-id="d8152-105">Das Verknüpfen von Shader wird beginnend mit Windows 8.1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8152-105">Shader linking is supported starting with Windows 8.1.</span></span>

<span data-ttu-id="d8152-106">**Ziel:** Erfahren Sie, wie Sie Shader-Verknüpfung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8152-106">**Objective:** Learn how to use shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d8152-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d8152-107">Prerequisites</span></span>

<span data-ttu-id="d8152-108">Es wird davon ausgegangen, dass Sie mit C+ vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="d8152-108">We assume that you are familiar with C++.</span></span> <span data-ttu-id="d8152-109">Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="d8152-109">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="d8152-110">**Gesamtzeit bis zum Abschluss:** 60 Minuten.</span><span class="sxs-lookup"><span data-stu-id="d8152-110">**Total time to complete:** 60 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="d8152-111">Weiterführende Informationen</span><span class="sxs-lookup"><span data-stu-id="d8152-111">Where to go from here</span></span>

<span data-ttu-id="d8152-112">Siehe auch [HLSL-compilerapis](dx-graphics-d3dcompiler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d8152-112">Also see [HLSL compiler APIs](dx-graphics-d3dcompiler-reference.md).</span></span>

<span data-ttu-id="d8152-113">Folgende Inhalte werden behandelt:</span><span class="sxs-lookup"><span data-stu-id="d8152-113">We show you how to:</span></span>

-   <span data-ttu-id="d8152-114">Kompilieren Sie den Shader-Code.</span><span class="sxs-lookup"><span data-stu-id="d8152-114">Compile your shader code</span></span>
-   <span data-ttu-id="d8152-115">Laden des kompilierten Codes in eine Shader-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d8152-115">Load the compiled code into a shader library</span></span>
-   <span data-ttu-id="d8152-116">Binden der Ressourcen von Quell Slots an Ziel Slots</span><span class="sxs-lookup"><span data-stu-id="d8152-116">Bind the resources from source slots to destination slots</span></span>
-   <span data-ttu-id="d8152-117">Erstellen von funktionsverknüpfungs Diagrammen (FLGS) für Shader</span><span class="sxs-lookup"><span data-stu-id="d8152-117">Construct function-linking-graphs (FLGs) for shaders</span></span>
-   <span data-ttu-id="d8152-118">Verknüpfen von shaderdiagrammen mit einer shaderbibliothek, um ein Shader-BLOB zu erzeugen, das von der Direct3D-Laufzeit verwendet werden kann</span><span class="sxs-lookup"><span data-stu-id="d8152-118">Link shader graphs with a shader library to produce a shader blob that the Direct3D runtime can use</span></span>

<span data-ttu-id="d8152-119">Als Nächstes erstellen wir eine shaderbibliothek und binden Ressourcen von Quell Slots an Ziel Slots.</span><span class="sxs-lookup"><span data-stu-id="d8152-119">Next we make a shader library and bind resources from source slots to destination slots.</span></span>

[<span data-ttu-id="d8152-120">Verpacken einer shaderbibliothek</span><span class="sxs-lookup"><span data-stu-id="d8152-120">Packaging a shader library</span></span>](pachaging-a-shader-library.md)

## <a name="related-topics"></a><span data-ttu-id="d8152-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8152-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8152-122">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="d8152-122">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="d8152-123">Direct3D 11-Grafik</span><span class="sxs-lookup"><span data-stu-id="d8152-123">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[<span data-ttu-id="d8152-124">DXGI</span><span class="sxs-lookup"><span data-stu-id="d8152-124">DXGI</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 