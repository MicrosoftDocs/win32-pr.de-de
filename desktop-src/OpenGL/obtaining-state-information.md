---
title: Abrufen von Zustandsinformationen
description: Abrufen von Zustandsinformationen
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, Zustandsinformationen
- OpenGL, Zustandsvariablen
- Zustandsinformationen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709719"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="bcd2b-106">Abrufen von Zustandsinformationen</span><span class="sxs-lookup"><span data-stu-id="bcd2b-106">Obtaining State Information</span></span>

<span data-ttu-id="bcd2b-107">OpenGL verwaltet viele Zustandsvariablen, die sich auf das Verhalten vieler Funktionen auswirken.</span><span class="sxs-lookup"><span data-stu-id="bcd2b-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="bcd2b-108">Einige dieser Variablen verfügen über spezialisierte Abfragefunktionen.</span><span class="sxs-lookup"><span data-stu-id="bcd2b-108">Some of these variables have specialized query functions.</span></span>



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="bcd2b-109">**glgetclipplane**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-109">**glGetClipPlane**</span></span>](glgetclipplane.md) | [<span data-ttu-id="bcd2b-110">**glgetpixelmap**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)             | [<span data-ttu-id="bcd2b-111">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-111">**glGetTexImage**</span></span>](glgetteximage.md)                   |
| [<span data-ttu-id="bcd2b-112">**glgetlight**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-112">**glGetLight**</span></span>](glgetlight.md)         | [<span data-ttu-id="bcd2b-113">**glgetpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | [<span data-ttu-id="bcd2b-114">**glgettexlevelparameter**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |
| [<span data-ttu-id="bcd2b-115">**glgetmap**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-115">**glGetMap**</span></span>](glgetmap.md)             | [<span data-ttu-id="bcd2b-116">**glgettex-v**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-116">**glGetTexEnv**</span></span>](glgettexenv.md)                 | [<span data-ttu-id="bcd2b-117">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-117">**glGetTexParameter**</span></span>](glgettexparameter.md)           |
| [<span data-ttu-id="bcd2b-118">**glgetmaterial**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-118">**glGetMaterial**</span></span>](glgetmaterial.md)   | [<span data-ttu-id="bcd2b-119">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="bcd2b-119">**glGetTexGen**</span></span>](glgettexgen.md)                 |                                                          |



 

<span data-ttu-id="bcd2b-120">Um den Wert anderer Zustandsvariablen zu erhalten, verwenden Sie je nach Bedarf " [**glgetbooleanv**](glgetbooleanv.md)", " [**glgetdoublev**](glgetdoublev.md)", " [**glgetfloatv**](glgetfloatv.md)" oder " [**glgetintegerv**](glgetintegerv.md)".</span><span class="sxs-lookup"><span data-stu-id="bcd2b-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="bcd2b-121">Weitere Informationen zur Verwendung dieser Funktionen finden Sie unter [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="bcd2b-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="bcd2b-122">Andere Abfragefunktionen, die Sie verwenden möchten, sind " [**glgeterror**](glgeterror.md)", " [**glgetstring**](glgetstring.md)" und " [**glisenabled**](glisenabled.md)".</span><span class="sxs-lookup"><span data-stu-id="bcd2b-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="bcd2b-123">(Weitere Informationen zu Funktionen im Zusammenhang mit der Fehlerbehandlung finden Sie unter [Behandeln von Fehlern](handling-errors.md) ). Verwenden Sie zum Speichern und Wiederherstellen von Gruppen von Zustandsvariablen [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="bcd2b-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="bcd2b-124">Verwenden der Abfragefunktionen</span><span class="sxs-lookup"><span data-stu-id="bcd2b-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="bcd2b-125">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="bcd2b-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="bcd2b-126">OpenGL-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="bcd2b-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="bcd2b-127">Speichern und Wiederherstellen von Sätzen von Zustandsvariablen</span><span class="sxs-lookup"><span data-stu-id="bcd2b-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="bcd2b-128">OpenGL-Zustandsvariablen</span><span class="sxs-lookup"><span data-stu-id="bcd2b-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="bcd2b-129">Referenz zu Zustandsinformationen</span><span class="sxs-lookup"><span data-stu-id="bcd2b-129">State Information Reference</span></span>](state-information-reference.md)

 

 




