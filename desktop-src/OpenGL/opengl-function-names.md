---
title: OpenGL-Funktionsnamen
description: Viele OpenGL-Funktionen sind Variationen voneinander und unterscheiden sich hauptsächlich von den Datentypen ihrer Argumente.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, Funktionsnamen
- Funktionsnamen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710607"
---
# <a name="opengl-function-names"></a><span data-ttu-id="3c909-105">OpenGL-Funktionsnamen</span><span class="sxs-lookup"><span data-stu-id="3c909-105">OpenGL Function Names</span></span>

<span data-ttu-id="3c909-106">Viele OpenGL-Funktionen sind Variationen voneinander und unterscheiden sich hauptsächlich von den Datentypen ihrer Argumente.</span><span class="sxs-lookup"><span data-stu-id="3c909-106">Many OpenGL functions are variations of each other, differing mostly in the data types of their arguments.</span></span> <span data-ttu-id="3c909-107">Einige Funktionen unterscheiden sich in der Anzahl der verknüpften Argumente und ob diese Argumente als Vektor oder separat in einer Liste angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="3c909-107">Some functions differ in the number of related arguments and whether those arguments can be specified as a vector or must be specified separately in a list.</span></span> <span data-ttu-id="3c909-108">Wenn Sie z. b. die **glVertex2f** -Funktion verwenden, müssen Sie x-und y-Koordinaten als 32-Bit-Gleit Komma Zahlen angeben. mit **glVertex3sv** müssen Sie ein Array von drei kurzen (16-Bit-) ganzzahligen Werten für x, y und z angeben.</span><span class="sxs-lookup"><span data-stu-id="3c909-108">For example, if you use the **glVertex2f** function, you need to supply x- and y-coordinates as 32-bit floating-point numbers; with **glVertex3sv**, you must supply an array of three short (16-bit) integer values for x, y, and z.</span></span> <span data-ttu-id="3c909-109">In den folgenden Themen wird nur der Basisname der Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c909-109">Only the base name of the function is used in the topics that follow.</span></span> <span data-ttu-id="3c909-110">Ein Sternchen gibt an, dass möglicherweise mehr für den eigentlichen Funktionsnamen vorhanden ist, als angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3c909-110">An asterisk indicates that there may be more to the actual function name than is shown.</span></span> <span data-ttu-id="3c909-111">Beispielsweise steht ["glVertex \*](glvertex-functions.md) " für alle Variationen der Funktion, mit der Vertices angegeben werden: **glVertex2d**, **glVertex2f**, **glVertex2i** usw.</span><span class="sxs-lookup"><span data-stu-id="3c909-111">For example, [glVertex\*](glvertex-functions.md) stands for all the variations of the function you use to specify vertices: **glVertex2d**, **glVertex2f**, **glVertex2i**, and so on.</span></span>

<span data-ttu-id="3c909-112">Die Auswirkung einer OpenGL-Funktion kann variieren, je nachdem, ob bestimmte Modi aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="3c909-112">The effect of an OpenGL function can vary depending on whether certain modes are enabled.</span></span> <span data-ttu-id="3c909-113">Beispielsweise müssen Sie die Beleuchtung aktivieren, wenn die Beleuchtungs bezogenen Funktionen ein ordnungsgemäß beleuchtetes Objekt bilden.</span><span class="sxs-lookup"><span data-stu-id="3c909-113">For example, you need to enable lighting if the lighting-related functions are to produce a properly lit object.</span></span> <span data-ttu-id="3c909-114">Um einen bestimmten Modus zu aktivieren, verwenden Sie die Funktion [**glEnable**](glenable.md) , und geben Sie die entsprechende Konstante an, um den Modus zu identifizieren (z. b. gl- \_ Beleuchtung).</span><span class="sxs-lookup"><span data-stu-id="3c909-114">To enable a particular mode, use the [**glEnable**](glenable.md) function and supply the appropriate constant to identify the mode (for example, GL\_LIGHTING).</span></span> <span data-ttu-id="3c909-115">Um einen Modus zu deaktivieren, verwenden Sie [**gldeaktiviert**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="3c909-115">To disable a mode, use [**glDisable**](gldisable.md).</span></span> <span data-ttu-id="3c909-116">Eine komplette Liste der Modi, die aktiviert werden können, finden Sie unter **glEnable** .</span><span class="sxs-lookup"><span data-stu-id="3c909-116">See **glEnable** for a complete list of the modes that can be enabled.</span></span>

 

 




