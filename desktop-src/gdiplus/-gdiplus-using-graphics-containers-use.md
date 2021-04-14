---
description: Ein Graphics-Objekt stellt Methoden wie DrawLine, DrawImage und DrawString zum Anzeigen von Vektorbildern, Rasterbildern und Text bereit.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Verwenden von Grafikcontainern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978905"
---
# <a name="using-graphics-containers"></a><span data-ttu-id="cde31-103">Verwenden von Grafikcontainern</span><span class="sxs-lookup"><span data-stu-id="cde31-103">Using Graphics Containers</span></span>

<span data-ttu-id="cde31-104">Ein [**graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) -Objekt stellt Methoden wie [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))und [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) zum Anzeigen von Vektorbildern, Rasterbildern und Text bereit.</span><span class="sxs-lookup"><span data-stu-id="cde31-104">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides methods such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), and [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) for displaying vector images, raster images, and text.</span></span> <span data-ttu-id="cde31-105">Ein **Grafik** Objekt verfügt auch über mehrere Eigenschaften, die die Qualität und Ausrichtung der Elemente beeinflussen, die gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="cde31-105">A **Graphics** object also has several properties that influence the quality and orientation of the items that are drawn.</span></span> <span data-ttu-id="cde31-106">Beispielsweise legt die Eigenschaft Glättungs Modus fest, ob Antialiasing auf Linien und Kurven angewendet wird, und die Welt Transformations Eigenschaft wirkt sich auf die Position und Drehung der Elemente aus, die gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="cde31-106">For example, the smoothing mode property determines whether antialiasing is applied to lines and curves, and the world transformation property influences the position and rotation of the items that are drawn.</span></span>

<span data-ttu-id="cde31-107">Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt ist oft einem bestimmten Anzeigegerät zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cde31-107">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object is often associated with a particular display device.</span></span> <span data-ttu-id="cde31-108">Wenn Sie ein **Grafik** Objekt zum Zeichnen in einem Fenster verwenden, wird das **Grafik** Objekt auch diesem bestimmten Fenster zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cde31-108">When you use a **Graphics** object to draw in a window, the **Graphics** object is also associated with that particular window.</span></span>

<span data-ttu-id="cde31-109">Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt kann als Container betrachtet werden, da es einen Satz von Eigenschaften enthält, die das Zeichnen beeinflussen und mit gerätespezifischen Informationen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cde31-109">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be thought of as a container because it holds a set of properties that influence drawing, and it is linked to device-specific information.</span></span> <span data-ttu-id="cde31-110">Sie können einen sekundären Container innerhalb eines vorhandenen **Grafik** Objekts erstellen, indem Sie die [BeginContainer](/previous-versions//ms535731(v=vs.85)) -Methode dieses **Grafik** Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cde31-110">You can create a secondary container within an existing **Graphics** object by calling the [BeginContainer](/previous-versions//ms535731(v=vs.85)) method of that **Graphics** object.</span></span>

<span data-ttu-id="cde31-111">In den folgenden Themen werden [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekte und schsted-Container ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="cde31-111">The following topics cover [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) objects and nested containers in more detail:</span></span>

-   [<span data-ttu-id="cde31-112">Status eines Grafikobjekts</span><span class="sxs-lookup"><span data-stu-id="cde31-112">The State of a Graphics Object</span></span>](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [<span data-ttu-id="cde31-113">Geschachtelte Grafikcontainer</span><span class="sxs-lookup"><span data-stu-id="cde31-113">Nested Graphics Containers</span></span>](-gdiplus-nested-graphics-containers-use.md)

 

 
