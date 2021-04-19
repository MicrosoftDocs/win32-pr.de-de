---
title: Verwenden der Abfragefunktionen
description: Verwenden der Abfragefunktionen
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, Abfragefunktionen
- Abfragefunktionen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341859"
---
# <a name="using-the-query-functions"></a><span data-ttu-id="f890d-105">Verwenden der Abfragefunktionen</span><span class="sxs-lookup"><span data-stu-id="f890d-105">Using the Query Functions</span></span>

<span data-ttu-id="f890d-106">Es gibt vier Abfragefunktionen zum Abrufen einfacher Zustandsvariablen und eine zum bestimmen, ob ein bestimmter Zustand aktiviert oder deaktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="f890d-106">There are four query functions for obtaining simple state variables and one for determining whether a particular state is enabled or disabled:</span></span>

-   [<span data-ttu-id="f890d-107">**glgetbooleanv**</span><span class="sxs-lookup"><span data-stu-id="f890d-107">**glGetBooleanv**</span></span>](glgetbooleanv.md)
-   [<span data-ttu-id="f890d-108">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="f890d-108">**glGetIntegerv**</span></span>](glgetintegerv.md)
-   [<span data-ttu-id="f890d-109">**glgetfloatv**</span><span class="sxs-lookup"><span data-stu-id="f890d-109">**glGetFloatv**</span></span>](glgetfloatv.md)
-   [<span data-ttu-id="f890d-110">**glgetdoublev**</span><span class="sxs-lookup"><span data-stu-id="f890d-110">**glGetDoublev**</span></span>](glgetdoublev.md)
-   [<span data-ttu-id="f890d-111">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="f890d-111">**glIsEnabled**</span></span>](glisenabled.md)

<span data-ttu-id="f890d-112">Die Prototypen für die Abfragefunktionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f890d-112">The prototypes for the query functions are:</span></span>

<span data-ttu-id="f890d-113">**void** **glgetbooleanv**(**GLenum** *PName* , **glboolean \*** *para* Metern);</span><span class="sxs-lookup"><span data-stu-id="f890d-113">**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );</span></span>

<span data-ttu-id="f890d-114">**void** **glgetintegerv**(**GLenum** *PName* , **glint \*** *para* Metern);</span><span class="sxs-lookup"><span data-stu-id="f890d-114">**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \*** *params* );</span></span>

<span data-ttu-id="f890d-115">**void** **glgetfloatv**(**GLenum** *PName* , **glfloat \*** *para* Metern);</span><span class="sxs-lookup"><span data-stu-id="f890d-115">**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );</span></span>

<span data-ttu-id="f890d-116">**void** **glgetdoublev**(**GLenum** *PName* , **gldouble \*** *para* );</span><span class="sxs-lookup"><span data-stu-id="f890d-116">**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );</span></span>

<span data-ttu-id="f890d-117">Die Abfragefunktionen erhalten die Statusvariablen "Boolean", "Integer", "Floating-Point" oder "Double Precision".</span><span class="sxs-lookup"><span data-stu-id="f890d-117">Respectively, the query functions obtain Boolean, integer, floating-point, or double-precision state variables.</span></span> <span data-ttu-id="f890d-118">Der *PName* -Parameter ist eine symbolische Konstante, die die zurück zugebende Zustands Variable angibt, und *params* ist ein Zeiger auf ein Array vom Typ, in dem die zurückgegebenen Daten abgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f890d-118">The *pname* parameter is a symbolic constant indicating the state variable to return, and *params* is a pointer to an array of the indicated type in which to place the returned data.</span></span> <span data-ttu-id="f890d-119">Die möglichen Werte für " *PName* " sind in den [OpenGL-Zustandsvariablen](opengl-state-variables.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f890d-119">The possible values for *pname* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span> <span data-ttu-id="f890d-120">Eine Typkonvertierung wird ausgeführt, wenn die gewünschte Variable als angeforderter Datentyp zurückgegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="f890d-120">A type conversion is performed if necessary to return the desired variable as the requested data type.</span></span>

<span data-ttu-id="f890d-121">Der Prototyp für " [**glisenabled**](glisenabled.md) " ist:</span><span class="sxs-lookup"><span data-stu-id="f890d-121">The prototype for [**glIsEnabled**](glisenabled.md) is:</span></span>

<span data-ttu-id="f890d-122">**Glboolean** - **glisenabled**(GLenum- *Cap* );</span><span class="sxs-lookup"><span data-stu-id="f890d-122">**GLboolean** **glIsEnabled**(GLenum *cap* );</span></span>

<span data-ttu-id="f890d-123">Wenn der durch *Cap* angegebene Modus aktiviert ist, gibt " **glisenabled** " den Wert "GL true" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="f890d-123">If the mode specified by *cap* is enabled, **glIsEnabled** returns GL\_TRUE.</span></span> <span data-ttu-id="f890d-124">Wenn der durch *Cap* angegebene Modus deaktiviert ist, gibt " **glisenabled** " den Wert "GL false" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="f890d-124">If the mode specified by *cap* is disabled, **glIsEnabled** returns GL\_FALSE.</span></span> <span data-ttu-id="f890d-125">Die möglichen Werte für *Cap* sind unter [OpenGL-Zustandsvariablen](opengl-state-variables.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f890d-125">The possible values for *cap* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span>

<span data-ttu-id="f890d-126">Bei anderen spezialisierten Funktionen werden bestimmte Zustandsvariablen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f890d-126">Other specialized functions return specific state variables.</span></span> <span data-ttu-id="f890d-127">Informationen dazu, wann diese Funktionen verwendet werden sollten, finden Sie unter OpenGL-Zustandsvariablen und im *OpenGL-Referenzhandbuch*.</span><span class="sxs-lookup"><span data-stu-id="f890d-127">To find out when to use these functions, see OpenGL State Variables and the *OpenGL Reference Manual*.</span></span> <span data-ttu-id="f890d-128">Weitere Informationen zur Fehlerbehandlung von OpenGL und zur Funktion " **glgeterror** " finden Sie unter [Fehlerbehandlung](error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="f890d-128">For more information on OpenGL's error handling facility and the **glGetError** function, see [Error Handling](error-handling.md).</span></span>

<span data-ttu-id="f890d-129">Die Funktionen, die bestimmte Zustandsvariablen zurückgeben, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f890d-129">The functions that return specific state variables are:</span></span>

-   [<span data-ttu-id="f890d-130">**glgetclipplane**</span><span class="sxs-lookup"><span data-stu-id="f890d-130">**glGetClipPlane**</span></span>](glgetclipplane.md)
-   [<span data-ttu-id="f890d-131">**glgeterror**</span><span class="sxs-lookup"><span data-stu-id="f890d-131">**glGetError**</span></span>](glgeterror.md)
-   [<span data-ttu-id="f890d-132">**glgetlight**</span><span class="sxs-lookup"><span data-stu-id="f890d-132">**glGetLight**</span></span>](glgetlight.md)
-   [<span data-ttu-id="f890d-133">**glgetmap**</span><span class="sxs-lookup"><span data-stu-id="f890d-133">**glGetMap**</span></span>](glgetmap.md)
-   [<span data-ttu-id="f890d-134">**glgetmaterial**</span><span class="sxs-lookup"><span data-stu-id="f890d-134">**glGetMaterial**</span></span>](glgetmaterial.md)
-   [<span data-ttu-id="f890d-135">**glgetpixelmap**</span><span class="sxs-lookup"><span data-stu-id="f890d-135">**glGetPixelMap**</span></span>](glgetpixelmap.md)
-   [<span data-ttu-id="f890d-136">**glgetpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="f890d-136">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
-   [<span data-ttu-id="f890d-137">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="f890d-137">**glGetString**</span></span>](glgetstring.md)
-   [<span data-ttu-id="f890d-138">**glgettex-v**</span><span class="sxs-lookup"><span data-stu-id="f890d-138">**glGetTexEnv**</span></span>](glgettexenv.md)
-   [<span data-ttu-id="f890d-139">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="f890d-139">**glGetTexGen**</span></span>](glgettexgen.md)
-   [<span data-ttu-id="f890d-140">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="f890d-140">**glGetTexImage**</span></span>](glgetteximage.md)
-   [<span data-ttu-id="f890d-141">**glgettexlevelparameter**</span><span class="sxs-lookup"><span data-stu-id="f890d-141">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
-   [<span data-ttu-id="f890d-142">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="f890d-142">**glGetTexParameter**</span></span>](glgettexparameter.md)

 

 




