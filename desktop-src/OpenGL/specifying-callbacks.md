---
title: Angeben von Rückrufen
description: Sie können bis zu fünf Rückruf Funktionen für ein Mosaik angeben.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- OpenGL-Hilfsprogramm (GLU), angeben von Rückruf Funktionen
- GLU (OpenGL-Hilfsprogramm), angeben von Rückruf Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516029"
---
# <a name="specifying-callbacks"></a><span data-ttu-id="c235f-105">Angeben von Rückrufen</span><span class="sxs-lookup"><span data-stu-id="c235f-105">Specifying Callbacks</span></span>

<span data-ttu-id="c235f-106">Sie können bis zu fünf Rückruf Funktionen für ein Mosaik angeben.</span><span class="sxs-lookup"><span data-stu-id="c235f-106">You can specify up to five callback functions for a tessellation.</span></span> <span data-ttu-id="c235f-107">Alle Funktionen, die Sie nicht angeben, werden im Mosaik Prozess nicht aufgerufen, und Sie erhalten keine Informationen, die Sie möglicherweise zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="c235f-107">Any functions that you do not specify are not called during the tessellation, and you do not get any information they might have returned.</span></span> <span data-ttu-id="c235f-108">Sie geben die Rückruf Funktionen mit " [*glutesscallback*](glutess.md)" an.</span><span class="sxs-lookup"><span data-stu-id="c235f-108">You specify the callback functions with [*gluTessCallback*](glutess.md).</span></span>

<span data-ttu-id="c235f-109">Die Funktion " **glutesscallback** " verknüpft die Rückruffunktion " *FN* " mit dem Mosaik Objekt " *tessobj*".</span><span class="sxs-lookup"><span data-stu-id="c235f-109">The **gluTessCallback** function associates the callback function *fn* with the tessellation object *tessobj*.</span></span> <span data-ttu-id="c235f-110">Der Typ des Rückrufs wird durch den *Parametertyp* bestimmt, der z. b. " **glu \_ Begin**", " **glu \_ Edge \_ Flag** **", " \_** **glu \_ Scheitel** Punkt" oder " **glu- \_ Fehler**" sein kann.</span><span class="sxs-lookup"><span data-stu-id="c235f-110">The type of the callback is determined by the parameter *type*, which can be **GLU\_BEGIN**, **GLU\_EDGE\_FLAG**, **GLU\_VERTEX**, **GLU\_END**, or **GLU\_ERROR**.</span></span> <span data-ttu-id="c235f-111">Die fünf möglichen Rückruf Funktionen verfügen über die folgenden Prototypen.</span><span class="sxs-lookup"><span data-stu-id="c235f-111">The five possible callback functions have the following prototypes.</span></span>



| <span data-ttu-id="c235f-112">Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="c235f-112">Callback function</span></span>   | <span data-ttu-id="c235f-113">Prototyp</span><span class="sxs-lookup"><span data-stu-id="c235f-113">Prototype</span></span>                                    |
|---------------------|----------------------------------------------|
| <span data-ttu-id="c235f-114">**Glu \_ Anfang**</span><span class="sxs-lookup"><span data-stu-id="c235f-114">**GLU\_BEGIN**</span></span>      | <span data-ttu-id="c235f-115">**void** **Begin**(\*\*GLenum \* \* *-Typ* );</span><span class="sxs-lookup"><span data-stu-id="c235f-115">**void** **begin**(\**GLenum\*\*\*type* );</span></span>       |
| <span data-ttu-id="c235f-116">**Glu \_ Edge- \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="c235f-116">**GLU\_EDGE\_FLAG**</span></span> | <span data-ttu-id="c235f-117">**void** **edgeflag**(\*\*glboolean \* \* *-Flag* );</span><span class="sxs-lookup"><span data-stu-id="c235f-117">**void** **edgeFlag**(\**GLboolean\*\*\*flag* );</span></span> |
| <span data-ttu-id="c235f-118">**Glu- \_ Scheitelpunkt**</span><span class="sxs-lookup"><span data-stu-id="c235f-118">**GLU\_VERTEX**</span></span>     | <span data-ttu-id="c235f-119">**void** **Scheitel** Punkt (\*\*void \* \* \* *-Daten* );</span><span class="sxs-lookup"><span data-stu-id="c235f-119">**void** **vertex**(\**void \*\*\*\*data* );</span></span>     |
| <span data-ttu-id="c235f-120">**Glu \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="c235f-120">**GLU\_END**</span></span>        | <span data-ttu-id="c235f-121"> **Ende beenden**( *void* );</span><span class="sxs-lookup"><span data-stu-id="c235f-121">**void** **end**( *void* );</span></span>                  |
| <span data-ttu-id="c235f-122">**Glu- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="c235f-122">**GLU\_ERROR**</span></span>      | <span data-ttu-id="c235f-123">**void** - **Fehler**(\**GLenum \* \* \* errno* );</span><span class="sxs-lookup"><span data-stu-id="c235f-123">**void** **error**(\**GLenum\*\*\*errno* );</span></span>      |



 

<span data-ttu-id="c235f-124">Um eine Rückruffunktion zu ändern, rufen Sie mit der neuen Funktion " [*glutesscallback*](glutess.md) " auf.</span><span class="sxs-lookup"><span data-stu-id="c235f-124">To change a callback function, call [*gluTessCallback*](glutess.md) with the new function.</span></span> <span data-ttu-id="c235f-125">Um eine Rückruffunktion auszuschließen, ohne Sie durch eine neue zu ersetzen, **übergeben Sie** für die entsprechende Funktion einen NULL-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c235f-125">To eliminate a callback function without replacing it with a new one, pass **gluTessCallback** a null pointer for the appropriate function.</span></span>

<span data-ttu-id="c235f-126">Wenn das Mosaik Vorgang fortgesetzt wird, werden die Rückruf Funktionen ähnlich wie die OpenGL-Funktionen " [**glBegin**](glbegin.md)", " [gledgeflag](gledgeflag-functions.md)", " [glVertex](glvertex-functions.md)" und " [**glEnd**](glend.md)" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c235f-126">As tessellation proceeds, the callback functions are called in a manner similar to the way you would use the OpenGL functions [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md), and [**glEnd**](glend.md).</span></span>

<span data-ttu-id="c235f-127">Die **glu \_ Begin** -Rückruffunktion wird mit einem von drei möglichen Parametern aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="c235f-127">The **GLU\_BEGIN** callback function is invoked with one of three possible parameters:</span></span>

-   <span data-ttu-id="c235f-128">GL- \_ Dreiecks \_ Lüfter</span><span class="sxs-lookup"><span data-stu-id="c235f-128">GL\_TRIANGLE\_FAN</span></span>
-   <span data-ttu-id="c235f-129">GL- \_ Dreiecks \_ Streifen</span><span class="sxs-lookup"><span data-stu-id="c235f-129">GL\_TRIANGLE\_STRIP</span></span>
-   <span data-ttu-id="c235f-130">GL- \_ Dreiecke</span><span class="sxs-lookup"><span data-stu-id="c235f-130">GL\_TRIANGLES</span></span>

<span data-ttu-id="c235f-131">Nach dem Aufrufen der Funktion " **glu \_ Begin** Callback" und vor dem Aufrufen der mit dem " **glu \_ End**" verknüpften Rückruffunktion wird eine Kombination aus dem glu-edgeflag und dem **glu \_ Vertex** -Rückrufe aufgerufen. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="c235f-131">After calling the **GLU\_BEGIN** callback function, and before calling the callback function associated with **GLU\_END**, some combination of the **GLU\_EDGE\_FLAG** and **GLU\_VERTEX** callbacks is invoked.</span></span> <span data-ttu-id="c235f-132">Die zugeordneten Scheitel Punkte und edgeflags werden genau so interpretiert, wie Sie in OpenGL zwischen **glBegin**(GL- \_ Dreieck- \_ Lüfter), **glBegin**(GL- \_ Dreiecks \_ Streifen) oder **glBegin**(GL \_ -Dreiecke **)** und dem passenden **glEnd** liegen.</span><span class="sxs-lookup"><span data-stu-id="c235f-132">The associated vertices and edge flags are interpreted exactly as they are in OpenGL between **glBegin**(GL\_TRIANGLE\_FAN), **glBegin**(GL\_TRIANGLE\_STRIP), or **glBegin**(GL\_TRIANGLES **)** and the matching **glEnd**.</span></span>

<span data-ttu-id="c235f-133">Da edgeflags in einem Dreiecks Lüfter oder einem Dreiecks Streifen keinen Sinn ergeben, wird der **glu \_ Begin** -Rückruf nur mit **GL- \_ Dreiecke** aufgerufen, wenn eine Rückruffunktion mit einem glu-edgeflag verknüpft ist. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="c235f-133">Because edge flags make no sense in a triangle fan or triangle strip, if there is a callback function associated with **GLU\_EDGE\_FLAG**, the **GLU\_BEGIN** callback is called only with **GL\_TRIANGLES**.</span></span> <span data-ttu-id="c235f-134">Die Funktion " **glu \_ Edge \_ Flag** Callback" funktioniert analog zur OpenGL [gledgeflag](gledgeflag-functions.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c235f-134">The **GLU\_EDGE\_FLAG** callback function works analogously to the OpenGL [glEdgeFlag](gledgeflag-functions.md) function.</span></span>

<span data-ttu-id="c235f-135">Wenn während des Mosaik Fehlers ein Fehler auftritt, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c235f-135">If there is an error during the tessellation, the error callback function is invoked.</span></span> <span data-ttu-id="c235f-136">An die Fehler Rückruffunktion wird eine glu-Fehlernummer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c235f-136">The error callback function is passed a GLU error number.</span></span> <span data-ttu-id="c235f-137">Sie können eine Zeichenfolge abrufen, in der der Fehler mit der Funktion " [**gluerrorstring**](gluerrorstring.md) " beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c235f-137">You can obtain a character string describing the error with the [**gluErrorString**](gluerrorstring.md) function.</span></span>

 

 




