---
title: Eingabedaten
description: Die OpenGL-Pipeline erfordert, dass Sie mehrere Datentypen eingeben.
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- OpenGL-Verarbeitungs Pipeline, Eingabedaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337569"
---
# <a name="input-data"></a><span data-ttu-id="74ed1-104">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="74ed1-104">Input Data</span></span>

<span data-ttu-id="74ed1-105">Die OpenGL-Pipeline erfordert, dass Sie mehrere Datentypen eingeben:</span><span class="sxs-lookup"><span data-stu-id="74ed1-105">The OpenGL pipeline requires you to input several types of data:</span></span>

-   <span data-ttu-id="74ed1-106">**Vertices**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-106">**Vertices**.</span></span> <span data-ttu-id="74ed1-107">Vertices beschreiben die Form des gewünschten geometrischen Objekts.</span><span class="sxs-lookup"><span data-stu-id="74ed1-107">Vertices describe the shape of the desired geometric object.</span></span> <span data-ttu-id="74ed1-108">Um Vertices anzugeben, verwenden Sie die [**glVertex \***](glvertex-functions.md) -Funktionen in Verbindung mit [**glBegin**](glbegin.md) und [**glEnd**](glend.md) , um einen Punkt, eine Linie oder ein Polygon zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="74ed1-108">To specify vertices, use [**glVertex\***](glvertex-functions.md) functions in conjunction with [**glBegin**](glbegin.md) and [**glEnd**](glend.md) to create a point, line, or polygon.</span></span> <span data-ttu-id="74ed1-109">Sie können auch [**glrect**](glrect-functions.md) verwenden, um ein gesamtes Rechteck gleichzeitig zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="74ed1-109">You can also use [**glRect**](glrect-functions.md) to describe an entire rectangle at one time.</span></span>
-   <span data-ttu-id="74ed1-110">**Edge-Flag**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-110">**Edge flag**.</span></span> <span data-ttu-id="74ed1-111">Standardmäßig sind alle Ränder von Polygonen Begrenzungs Kanten.</span><span class="sxs-lookup"><span data-stu-id="74ed1-111">By default, all edges of polygons are boundary edges.</span></span> <span data-ttu-id="74ed1-112">Verwenden Sie [**gledgeflag \***](gledgeflag-functions.md) , um das Edge-Flag explizit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="74ed1-112">Use [**glEdgeFlag\***](gledgeflag-functions.md) to explicitly set the edge flag.</span></span>
-   <span data-ttu-id="74ed1-113">**Aktuelle Raster Position**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-113">**Current raster position**.</span></span> <span data-ttu-id="74ed1-114">Mit [**glRasterPos \***](glrasterpos-functions.md)angegeben, wird die aktuelle Raster Position verwendet, um Raster Koordinaten für Pixel-und Bitmap-Zeichnungsvorgänge zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="74ed1-114">Specified with [**glRasterPos\***](glrasterpos-functions.md), the current raster position is used to determine raster coordinates for pixel- and bitmap-drawing operations.</span></span>
-   <span data-ttu-id="74ed1-115">**Aktuelle normal**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-115">**Current normal**.</span></span> <span data-ttu-id="74ed1-116">Ein normaler Vektor, der einem bestimmten Scheitelpunkt zugeordnet ist, bestimmt, wie eine Oberfläche an diesem Scheitelpunkt im dreidimensionalen Raum ausgerichtet wird. Dies wirkt sich wiederum darauf aus, wie viel Licht der jeweilige Scheitelpunkt empfängt.</span><span class="sxs-lookup"><span data-stu-id="74ed1-116">A normal vector associated with a particular vertex determines how a surface at that vertex is oriented in three-dimensional space; this in turn affects how much light that particular vertex receives.</span></span> <span data-ttu-id="74ed1-117">Verwenden Sie [**glnormal \***](glnormal-functions.md) , um einen normalen Vektor anzugeben.</span><span class="sxs-lookup"><span data-stu-id="74ed1-117">Use [**glNormal\***](glnormal-functions.md) to specify a normal vector.</span></span>
-   <span data-ttu-id="74ed1-118">**Aktuelle Farbe**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-118">**Current color**.</span></span> <span data-ttu-id="74ed1-119">Die Farbe eines Scheitel Punkts und die Beleuchtungsbedingungen bestimmen die endgültige, Leuchtende Farbe.</span><span class="sxs-lookup"><span data-stu-id="74ed1-119">The color of a vertex, together with the lighting conditions, determine the final, lit color.</span></span> <span data-ttu-id="74ed1-120">Die Farbe wird mit " [**glcolor \***](glcolor-functions.md) " angegeben, wenn im RGBA-Modus angegeben ist, oder mit " [**glindex \***](glindex-functions.md) ", wenn im Farb Index Modus</span><span class="sxs-lookup"><span data-stu-id="74ed1-120">Color is specified with [**glColor\***](glcolor-functions.md) if in RGBA mode, or with [**glIndex\***](glindex-functions.md) if in color-index mode.</span></span>
-   <span data-ttu-id="74ed1-121">**Aktuelle Texturkoordinaten**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-121">**Current texture coordinates**.</span></span> <span data-ttu-id="74ed1-122">Mit " [**gltexcoord \***](gltexcoord-functions.md)" angegeben, bestimmen Texturkoordinaten die Position in einer Textur Zuordnung, die einem Scheitelpunkt eines Objekts zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="74ed1-122">Specified with [**glTexCoord\***](gltexcoord-functions.md), texture coordinates determine the location in a texture map to associate with a vertex of an object.</span></span>

> [!Note]  
> <span data-ttu-id="74ed1-123">Wenn " **glVertex \*** " aufgerufen wird, erbt der resultierende Scheitelpunkt die aktuellen Edge-Flag-, normal-, Farb-und Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="74ed1-123">When **glVertex\*** is called, the resulting vertex inherits the current edge flag, normal, color, and texture coordinates.</span></span> <span data-ttu-id="74ed1-124">Daher muss " **gledgeflag \***", " **glnormal \***", " **glcolor \***" und " **gltexcoord \*** " vor " **glVertex \***" aufgerufen werden, wenn Sie sich auf den resultierenden Scheitelpunkt auswirken.</span><span class="sxs-lookup"><span data-stu-id="74ed1-124">Therefore, **glEdgeFlag\***, **glNormal\***, **glColor\***, and **glTexCoord\*** must be called before **glVertex\***, if they are to affect the resulting vertex.</span></span>

 

 

 




