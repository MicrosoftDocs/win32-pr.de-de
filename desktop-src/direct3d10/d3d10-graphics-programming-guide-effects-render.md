---
description: Ein Effekt kann zum Speichern von Informationen oder zum Rendering mithilfe einer Zustands Gruppe verwendet werden.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendern eines Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214083"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="d0a64-103">Rendern eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0a64-103">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="d0a64-104">Ein Effekt kann zum Speichern von Informationen oder zum Rendering mithilfe einer Zustands Gruppe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0a64-104">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="d0a64-105">Jede Technik gibt Scheitelpunkt-Shader, Geometry-Shader, Pixel-Shader, shaderzustand, Sampler und Textur Zustand und anderen Pipeline Zustand an.</span><span class="sxs-lookup"><span data-stu-id="d0a64-105">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="d0a64-106">Nachdem Sie den Status in einem Effekt organisiert haben, können Sie den renderingeffekt Kapseln, der sich aus diesem Zustand ergibt, indem Sie den Effekt erstellen und rendern.</span><span class="sxs-lookup"><span data-stu-id="d0a64-106">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="d0a64-107">Es gibt einige Schritte zum Vorbereiten eines Effekts für das Rendering.</span><span class="sxs-lookup"><span data-stu-id="d0a64-107">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="d0a64-108">Der erste ist die Kompilierung, die den HLSL-Code auf die HLSL-Sprachsyntax und die Effekt Framework-Regeln überprüft.</span><span class="sxs-lookup"><span data-stu-id="d0a64-108">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="d0a64-109">Sie können einen Effekt von Ihrer Anwendung mithilfe von API-aufrufen kompilieren, oder Sie können einen Effekt offline mit dem Effekt-Compilerdienstprogramm kompilieren.</span><span class="sxs-lookup"><span data-stu-id="d0a64-109">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="d0a64-110">Nachdem ihre Wirkung erfolgreich kompiliert wurde, erstellen Sie Sie durch Aufrufen eines anderen (aber sehr ähnlichen) Satzes von APIs.</span><span class="sxs-lookup"><span data-stu-id="d0a64-110">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="d0a64-111">Nachdem der Effekt erstellt wurde, gibt es zwei verbleibende Schritte für die Verwendung.</span><span class="sxs-lookup"><span data-stu-id="d0a64-111">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="d0a64-112">Zunächst müssen Sie die Werte des Wirkungs Zustands (die Werte der Effekt Variablen) mit einer Reihe von Methoden zum Festlegen des Zustands initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d0a64-112">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="d0a64-113">Bei einigen Variablen kann dies einmalig erfolgen, wenn ein Effekt erstellt wird. andere müssen jedes Mal aktualisiert werden, wenn die Anwendung die Renderschleife aufruft.</span><span class="sxs-lookup"><span data-stu-id="d0a64-113">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="d0a64-114">Nachdem die Effekt Variablen festgelegt wurden, weisen Sie die Laufzeit an, die Auswirkung durch Anwenden einer Technik zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="d0a64-114">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="d0a64-115">Diese Themen werden im folgenden ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0a64-115">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="d0a64-116">Kompilieren eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0a64-116">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="d0a64-117">Erstellen eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0a64-117">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="d0a64-118">Status des festgelegten Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0a64-118">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="d0a64-119">Anwenden einer Technik (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0a64-119">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="d0a64-120">Natürlich sind bei der Verwendung von Effekten [Leistungsaspekte zu berücksichtigen](d3d10-graphics-programming-guide-effects-performance.md) .</span><span class="sxs-lookup"><span data-stu-id="d0a64-120">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="d0a64-121">Diese Überlegungen sind größtenteils identisch, wenn Sie keinen Effekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="d0a64-121">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="d0a64-122">Dinge wie das Minimieren der Menge der Zustandsänderungen oder das Organisieren der Variablen, die nach Häufigkeit aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d0a64-122">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="d0a64-123">Diese Taktiken werden verwendet, um die Datenmenge zu minimieren, die von der CPU an die GPU gesendet werden muss, und damit potenzielle Synchronisierungs Probleme zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="d0a64-123">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0a64-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0a64-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0a64-125">Effekte (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0a64-125">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



