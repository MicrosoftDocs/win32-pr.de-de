---
title: Abrufen von Zustandsinformationen
description: Abrufen von Zustandsinformationen
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL,Zustandsinformationen
- OpenGL,Zustandsvariablen
- 'Zustandsinformationen: OpenGL'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120685"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="9d904-106">Abrufen von Zustandsinformationen</span><span class="sxs-lookup"><span data-stu-id="9d904-106">Obtaining State Information</span></span>

<span data-ttu-id="9d904-107">OpenGL verwaltet viele Zustandsvariablen, die sich auf das Verhalten vieler Funktionen auswirken.</span><span class="sxs-lookup"><span data-stu-id="9d904-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="9d904-108">Einige dieser Variablen verfügen über spezielle Abfragefunktionen.</span><span class="sxs-lookup"><span data-stu-id="9d904-108">Some of these variables have specialized query functions.</span></span>

:::row:::
    :::column:::
        [<span data-ttu-id="9d904-109">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="9d904-109">**glGetClipPlane**</span></span>](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="9d904-110">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="9d904-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="9d904-111">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="9d904-111">**glGetTexImage**</span></span>](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="9d904-112">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="9d904-112">**glGetLight**</span></span>](glgetlight.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="9d904-113">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="9d904-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="9d904-114">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="9d904-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="9d904-115">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="9d904-115">**glGetMap**</span></span>](glgetmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="9d904-116">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="9d904-116">**glGetTexEnv**</span></span>](glgettexenv.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="9d904-117">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="9d904-117">**glGetTexParameter**</span></span>](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="9d904-118">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="9d904-118">**glGetMaterial**</span></span>](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="9d904-119">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="9d904-119">**glGetTexGen**</span></span>](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

<span data-ttu-id="9d904-120">Verwenden Sie [**glGetBooleanv,**](glgetbooleanv.md) [**glGetDoublev,**](glgetdoublev.md) [**glGetFloatv**](glgetfloatv.md)oder [**glGetIntegerv,**](glgetintegerv.md)um den Wert anderer Zustandsvariablen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9d904-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="9d904-121">Informationen zur Verwendung dieser Funktionen finden Sie unter [**glGet.**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)</span><span class="sxs-lookup"><span data-stu-id="9d904-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="9d904-122">Weitere Abfragefunktionen, die Sie möglicherweise verwenden möchten, sind [**glGetError,**](glgeterror.md) [**glGetString**](glgetstring.md)und [**glIsEnabled.**](glisenabled.md)</span><span class="sxs-lookup"><span data-stu-id="9d904-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="9d904-123">(Weitere [Informationen zu Funktionen im Zusammenhang](handling-errors.md) mit der Fehlerbehandlung finden Sie unter Behandeln von Fehlern.) Verwenden Sie [**glPushAttrib**](glpushattrib.md) und [**glPopAttrib,**](glpopattrib.md)um Sätze von Zustandsvariablen zu speichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d904-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="9d904-124">Verwenden der Abfragefunktionen</span><span class="sxs-lookup"><span data-stu-id="9d904-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="9d904-125">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="9d904-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="9d904-126">OpenGL-Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9d904-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="9d904-127">Speichern und Wiederherstellen von Sätzen von Zustandsvariablen</span><span class="sxs-lookup"><span data-stu-id="9d904-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="9d904-128">OpenGL-Zustandsvariablen</span><span class="sxs-lookup"><span data-stu-id="9d904-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="9d904-129">Referenz zu Zustandsinformationen</span><span class="sxs-lookup"><span data-stu-id="9d904-129">State Information Reference</span></span>](state-information-reference.md)

 

 




