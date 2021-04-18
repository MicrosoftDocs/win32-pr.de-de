---
title: Portieren von IRIS GL Get-Funktionen
description: 'IRIS GL \ 0034; Get \ 0034; Funktionen haben folgende Form:'
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- IRIS GL Porting, Get Functions
- Portieren von IRIS GL, Get Functions
- Portieren auf OpenGL von IRIS GL, Get Functions
- OpenGL-Portierung von IRIS GL, Get Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340436"
---
# <a name="porting-iris-gl-get-functions"></a><span data-ttu-id="c734b-107">Portieren von IRIS GL Get-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c734b-107">Porting IRIS GL Get Functions</span></span>

<span data-ttu-id="c734b-108">Die "Get"-Funktionen von IRIS GL haben folgende Form:</span><span class="sxs-lookup"><span data-stu-id="c734b-108">IRIS GL "get" functions take the following form:</span></span>

``` syntax
int getthing();
```

<span data-ttu-id="c734b-109">und</span><span class="sxs-lookup"><span data-stu-id="c734b-109">and</span></span>

``` syntax
int getthings( int *a, int *b);
```

<span data-ttu-id="c734b-110">Der Iris GL-Code umfasst wahrscheinlich Get-Funktionsaufrufe, die etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="c734b-110">Your IRIS GL code probably includes get function calls that look something like:</span></span>

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

<span data-ttu-id="c734b-111">In OpenGL verwenden Sie einen der folgenden vier Arten von [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) -Funktionen anstelle der entsprechenden IRIS GL Get-Funktionen:</span><span class="sxs-lookup"><span data-stu-id="c734b-111">In OpenGL you use one of the following four types of [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) functions in place of equivalent IRIS GL get functions:</span></span>

-   <span data-ttu-id="c734b-112">**glgetbooleanv**</span><span class="sxs-lookup"><span data-stu-id="c734b-112">**glGetBooleanv**</span></span>
-   <span data-ttu-id="c734b-113">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="c734b-113">**glGetIntegerv**</span></span>
-   <span data-ttu-id="c734b-114">**glgetfloatv**</span><span class="sxs-lookup"><span data-stu-id="c734b-114">**glGetFloatv**</span></span>
-   <span data-ttu-id="c734b-115">**glgetdoublev**</span><span class="sxs-lookup"><span data-stu-id="c734b-115">**glGetDoublev**</span></span>

<span data-ttu-id="c734b-116">Die Funktionen haben die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="c734b-116">The functions have the following syntax:</span></span>

``` syntax
glGet<Datatype>v( value, *data );
```

<span data-ttu-id="c734b-117">der *Wert* ist vom Typ " **GLenum** ", und die Daten sind vom Typ " **gldatatype**".</span><span class="sxs-lookup"><span data-stu-id="c734b-117">where *value* is of type **GLenum** and data is of type **GLdatatype**.</span></span> <span data-ttu-id="c734b-118">Wenn Sie " **glget** " und einen anderen Typ als den erwarteten Typ zurückgeben, wird der Typ entsprechend konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c734b-118">When you call **glGet** and it returns a type different from the type expected, the type is converted appropriately.</span></span> <span data-ttu-id="c734b-119">Eine umfassende Liste der Parameter für **glget** finden Sie unter [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="c734b-119">For a complete list of **glGet** parameters, see [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span></span>

 

 




