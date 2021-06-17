---
description: Erfahren Sie mehr über das Rendern eines Effekts für Direct3D 10. Ein Effekt kann verwendet werden, um Informationen zu speichern oder mit einer Gruppe von Status zu rendern.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendern eines Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262572"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="857bf-104">Rendern eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="857bf-104">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="857bf-105">Ein Effekt kann verwendet werden, um Informationen zu speichern oder mit einer Gruppe von Status zu rendern.</span><span class="sxs-lookup"><span data-stu-id="857bf-105">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="857bf-106">Jede Technik gibt Vertex-Shader, Geometrie-Shader, Pixel-Shader, Shaderzustand, Sampler- und Texturzustand und anderen Pipelinezustand an.</span><span class="sxs-lookup"><span data-stu-id="857bf-106">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="857bf-107">Nachdem Sie den Zustand in einem Effekt organisiert haben, können Sie den Renderingeffekt, der sich aus diesem Zustand ergibt, kapseln, indem Sie den Effekt erstellen und rendern.</span><span class="sxs-lookup"><span data-stu-id="857bf-107">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="857bf-108">Es gibt einige Schritte zum Vorbereiten eines Effekts für das Rendering.</span><span class="sxs-lookup"><span data-stu-id="857bf-108">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="857bf-109">Die erste ist die Kompilierung, bei der HLSL wie Code mit der HLSL-Sprachsyntax und den Auswirkungsframeworkregeln überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="857bf-109">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="857bf-110">Sie können einen Effekt aus Ihrer Anwendung mithilfe von API-Aufrufen kompilieren, oder Sie können einen Effekt offline mithilfe des Effektcompiler-Hilfsprogramms kompilieren.</span><span class="sxs-lookup"><span data-stu-id="857bf-110">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="857bf-111">Nachdem Der Effekt erfolgreich kompiliert wurde, erstellen Sie ihn, indem Sie einen anderen (aber sehr ähnlichen) Satz von APIs aufrufen.</span><span class="sxs-lookup"><span data-stu-id="857bf-111">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="857bf-112">Nachdem der Effekt erstellt wurde, gibt es zwei verbleibende Schritte für die Verwendung.</span><span class="sxs-lookup"><span data-stu-id="857bf-112">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="857bf-113">Zunächst müssen Sie die Effektzustandswerte (die Werte der Effektvariablen) mithilfe einer Reihe von Methoden zum Festlegen des Zustands initialisieren.</span><span class="sxs-lookup"><span data-stu-id="857bf-113">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="857bf-114">Bei einigen Variablen kann dies einmal erfolgen, wenn ein Effekt erstellt wird. andere müssen jedes Mal aktualisiert werden, wenn ihre Anwendung die Renderschleife aufruft.</span><span class="sxs-lookup"><span data-stu-id="857bf-114">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="857bf-115">Nachdem die Effektvariablen festgelegt wurden, teilen Sie der Laufzeit mit, die Auswirkung durch Anwenden einer Technik zu rendern.</span><span class="sxs-lookup"><span data-stu-id="857bf-115">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="857bf-116">Diese Themen werden weiter unten ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="857bf-116">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="857bf-117">Kompilieren eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="857bf-117">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="857bf-118">Erstellen eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="857bf-118">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="857bf-119">Festlegen des Effektzustands (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="857bf-119">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="857bf-120">Anwenden einer Technik (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="857bf-120">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="857bf-121">Natürlich gibt es [Überlegungen zur Leistung bei](d3d10-graphics-programming-guide-effects-performance.md) der Verwendung von Effekten.</span><span class="sxs-lookup"><span data-stu-id="857bf-121">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="857bf-122">Diese Überlegungen sind größtenteils identisch, wenn Sie keinen Effekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="857bf-122">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="857bf-123">Dies kann beispielsweise das Minimieren der Menge an Zustandsänderungen oder das Organisieren der Variablen sein, die nach Häufigkeit aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="857bf-123">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="857bf-124">Diese Taktiken werden verwendet, um die Menge der Daten zu minimieren, die von der CPU an die GPU gesendet werden müssen, und daher potenzielle Synchronisierungsprobleme zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="857bf-124">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="857bf-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="857bf-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="857bf-126">Effekte (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="857bf-126">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



