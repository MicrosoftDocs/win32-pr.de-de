---
title: OpenGL-Zustandsvariablen
description: In den folgenden Themen werden die Namen von Zustandsvariablen aufgelistet, die abgefragt werden können.
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- OpenGL-Zustandsvariablen
- Zustandsvariablen, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342266"
---
# <a name="opengl-state-variables"></a><span data-ttu-id="832a5-105">OpenGL-Zustandsvariablen</span><span class="sxs-lookup"><span data-stu-id="832a5-105">OpenGL State Variables</span></span>

<span data-ttu-id="832a5-106">In den folgenden Themen werden die Namen von Zustandsvariablen aufgelistet, die abgefragt werden können:</span><span class="sxs-lookup"><span data-stu-id="832a5-106">The following topics list the names of state variables that can be queried:</span></span>

-   [<span data-ttu-id="832a5-107">**Zustandsvariablen für aktuelle Werte und zugehörige Daten**</span><span class="sxs-lookup"><span data-stu-id="832a5-107">**State Variables for Current Values and Associated Data**</span></span>](state-variables-for-current-values-and-associated-data.md)
-   [<span data-ttu-id="832a5-108">**Transformations Zustandsvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-108">**Transformation State Variables**</span></span>](transformation-state-variables.md)
-   [<span data-ttu-id="832a5-109">**Farb Statusvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-109">**Coloring State Variables**</span></span>](coloring-state-variables.md)
-   [<span data-ttu-id="832a5-110">**Beleuchtungs Zustandsvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-110">**Lighting State Variables**</span></span>](lighting-state-variables.md)
-   [<span data-ttu-id="832a5-111">**Rasterization-Zustandsvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-111">**Rasterization State Variables**</span></span>](rasterization-state-variables.md)
-   [<span data-ttu-id="832a5-112">**Texturierungsstatusvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-112">**Texturing State Variables**</span></span>](texturing-state-variables.md)
-   [<span data-ttu-id="832a5-113">**Pixel Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="832a5-113">**Pixel Operations**</span></span>](pixel-operations.md)
-   [<span data-ttu-id="832a5-114">**Statusvariablen des Framebuffer-Steuer Elements**</span><span class="sxs-lookup"><span data-stu-id="832a5-114">**Framebuffer Control State Variables**</span></span>](framebuffer-control-state-variables.md)
-   [<span data-ttu-id="832a5-115">**Pixel Zustandsvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-115">**Pixel State Variables**</span></span>](pixel-state-variables.md)
-   [<span data-ttu-id="832a5-116">**Evaluatorstatusvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-116">**Evaluator State Variables**</span></span>](evaluator-state-variables.md)
-   [<span data-ttu-id="832a5-117">**Hinweis Zustandsvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-117">**Hint State Variables**</span></span>](hint-state-variables.md)
-   [<span data-ttu-id="832a5-118">**Implementierungs abhängige Zustandsvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-118">**Implementation-Dependent State Variables**</span></span>](implementation-dependent-state-variables.md)
-   [<span data-ttu-id="832a5-119">**Von der Implementierung abhängige Pixel-Depth Zustandsvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-119">**Implementation-Dependent Pixel-Depth State Variables**</span></span>](implementation-dependent-pixel-depth-state-variables.md)
-   [<span data-ttu-id="832a5-120">**Diverse Zustandsvariablen**</span><span class="sxs-lookup"><span data-stu-id="832a5-120">**Miscellaneous State Variables**</span></span>](miscellaneous-state-variables.md)

<span data-ttu-id="832a5-121">Für jede Variable werden im Thema eine Beschreibung, eine Attribut Gruppe, ein ursprünglicher oder ein Minimalwert sowie die vorgeschlagene Funktion " [**glget \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) " aufgeführt, die für die Beschaffung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="832a5-121">For each variable, the topic lists a description, attribute group, initial or minimum value, and the suggested [**glGet\***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) function to use for obtaining it.</span></span>

<span data-ttu-id="832a5-122">Zustandsvariablen, die Sie mit " [**glgetbooleanv**](glgetbooleanv.md)", " [**glgetintegerv**](glgetintegerv.md)", " [**glgetfloatv**](glgetfloatv.md)" oder " [**glgetdoublev**](glgetdoublev.md) " abrufen können, werden mit nur einer dieser Funktionalitäten aufgelistet, die am besten für den Typ der zurück zugegenden Daten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="832a5-122">State variables that you can obtain using [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetDoublev**](glgetdoublev.md) are listed with just one of these functionsthe one that is most appropriate for the type of data to be returned.</span></span> <span data-ttu-id="832a5-123">Diese Zustandsvariablen können nicht mithilfe von " [**glisenabled**](glisenabled.md)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="832a5-123">You cannot obtain these state variables using [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="832a5-124">Sie können jedoch Zustandsvariablen abrufen, für die " **glisenabled** " als Abfragefunktion mit " **glgetbooleanv**", " **glgetintegerv**", " **glgetfloatv**" und " **glgetdoublev**" aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="832a5-124">However, you can obtain state variables for which **glIsEnabled** is listed as the query function with **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv**, and **glGetDoublev**.</span></span> <span data-ttu-id="832a5-125">Mit dieser Funktion können Sie Zustandsvariablen abrufen, für die eine andere Funktion als Abfragefunktion aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="832a5-125">You can obtain state variables for which any other function is listed as the query function only by using that function.</span></span> <span data-ttu-id="832a5-126">Wenn keine Attribut Gruppe aufgeführt ist, gehört die Variable keiner Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="832a5-126">If no attribute group is listed, the variable doesn't belong to any group.</span></span> <span data-ttu-id="832a5-127">Alle Zustandsvariablen, die Sie Abfragen können, mit Ausnahme derjenigen, die von der Implementierung abhängen, haben Anfangswerte.</span><span class="sxs-lookup"><span data-stu-id="832a5-127">All state variables that you can query, except those that are implementation dependent, have initial values.</span></span> <span data-ttu-id="832a5-128">Um den Anfangswert einer Variablen zu ermitteln, für die kein Anfangswert aufgelistet ist, lesen Sie den Verweis der Variablen oder den</span><span class="sxs-lookup"><span data-stu-id="832a5-128">To determine the initial value of a variable for which no initial value is listed, see that variable's reference or the</span></span>

<span data-ttu-id="832a5-129">*OpenGL-Referenzhandbuch*.</span><span class="sxs-lookup"><span data-stu-id="832a5-129">*OpenGL Reference Manual*.</span></span>

 

 




