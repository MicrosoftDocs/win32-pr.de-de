---
description: Ein GraphicsPath-Objekt speichert eine Sequenz von Linien und B&\# 233; Zier-Splines.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Vereinfachen von Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987901"
---
# <a name="flattening-paths"></a><span data-ttu-id="0ee74-103">Vereinfachen von Pfaden</span><span class="sxs-lookup"><span data-stu-id="0ee74-103">Flattening Paths</span></span>

<span data-ttu-id="0ee74-104">Ein [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt speichert eine Sequenz von Linien und Bézier-Splines.</span><span class="sxs-lookup"><span data-stu-id="0ee74-104">A [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object stores a sequence of lines and Bézier splines.</span></span> <span data-ttu-id="0ee74-105">Sie können einem Pfad mehrere Arten von Kurven (Ellipsen, Arcs, kardinale Splines) hinzufügen, aber jede Kurve wird in eine Bézier-Spline konvertiert, bevor Sie im Pfad gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ee74-105">You can add several types of curves (ellipses, arcs, cardinal splines) to a path, but each curve is converted to a Bézier spline before it is stored in the path.</span></span> <span data-ttu-id="0ee74-106">Das Vereinfachen eines Pfads besteht darin, jede Bézier-Spline im Pfad in eine Sequenz von geraden Zeilen umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="0ee74-106">Flattening a path consists of converting each Bézier spline in the path to a sequence of straight lines.</span></span>

<span data-ttu-id="0ee74-107">Um einen Pfad zu vereinfachen, nennen Sie die [**GraphicsPath:: vereinfachen**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) -Methode eines [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0ee74-107">To flatten a path, call the [**GraphicsPath::Flatten**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="0ee74-108">Die **GraphicsPath:: Flatten** -Methode empfängt ein flatdo-Argument, das den maximalen Abstand zwischen dem vereinfachten Pfad und dem ursprünglichen Pfad angibt.</span><span class="sxs-lookup"><span data-stu-id="0ee74-108">The **GraphicsPath::Flatten** method receives a flatness argument that specifies the maximum distance between the flattened path and the original path.</span></span> <span data-ttu-id="0ee74-109">Die folgende Abbildung zeigt einen Pfad vor und nach der Vereinfachung.</span><span class="sxs-lookup"><span data-stu-id="0ee74-109">The following illustration shows a path before and after flattening.</span></span>

![Abbildung, die eine Sequenz von verbundenen Bézier-Splines in blau und den entsprechenden roten Zeilen anzeigt](images/aboutgdip02-art32a.png)

 

 



