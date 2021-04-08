---
title: Verwenden von anzeigen Listen
description: Verwenden von anzeigen Listen
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, Anzeigen von Listen
- Anzeigelisten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855816"
---
# <a name="using-display-lists"></a><span data-ttu-id="f08b2-105">Verwenden von anzeigen Listen</span><span class="sxs-lookup"><span data-stu-id="f08b2-105">Using Display Lists</span></span>

<span data-ttu-id="f08b2-106">Eine Anzeigeliste ist eine Gruppe von OpenGL-Funktionen, die für die nachfolgende Ausführung gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="f08b2-106">A display list is a group of OpenGL functions that has been stored for subsequent execution.</span></span> <span data-ttu-id="f08b2-107">Die Funktion " [**glnewlist**](glnewlist.md) " beginnt mit der Erstellung einer Anzeigeliste, und mit " [**glendlist**](glendlist.md) " wird Sie beendet.</span><span class="sxs-lookup"><span data-stu-id="f08b2-107">The [**glNewList**](glnewlist.md) function begins the creation of a display list, and [**glEndList**](glendlist.md) ends it.</span></span> <span data-ttu-id="f08b2-108">Mit wenigen Ausnahmen werden OpenGL-Funktionen, die zwischen **glnewlist** und **glendlist** aufgerufen werden, an die Anzeigeliste angehängt.</span><span class="sxs-lookup"><span data-stu-id="f08b2-108">With few exceptions, OpenGL functions called between **glNewList** and **glEndList** are appended to the display list.</span></span> <span data-ttu-id="f08b2-109">(Eine Liste der Funktionen, die Sie in einer Anzeigeliste nicht speichern und ausführen können, finden Sie in der Liste mit den Funktionen von **glnewlist** .) Wenn Sie die Ausführung einer Liste oder einer Gruppe von Listen aufrufen möchten, verwenden Sie " [**glCallList**](glcalllist.md) " oder " [**glcalllists**](glcalllists.md) ", und geben Sie die identifizierende Anzahl einer bestimmten Liste oder Listen an.</span><span class="sxs-lookup"><span data-stu-id="f08b2-109">(See **glNewList** for a list of the functions that you can't store and execute from within a display list.) To trigger the execution of a list or set of lists, use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) and supply the identifying number of a particular list or lists.</span></span> <span data-ttu-id="f08b2-110">Sie verwalten die Indizes, die zum Identifizieren von anzeigen Listen mit " [**glgenlists**](glgenlists.md)", " [**gllistbase**](gllistbase.md)" und " [**glislist**](glislist.md)" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f08b2-110">You manage the indexes used to identify display lists with [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md), and [**glIsList**](glislist.md).</span></span> <span data-ttu-id="f08b2-111">Verwenden Sie zum Löschen eines Satzes von Anzeigelisten " [**gldelta etelists**](gldeletelists.md)".</span><span class="sxs-lookup"><span data-stu-id="f08b2-111">To delete a set of display lists, use [**glDeleteLists**](gldeletelists.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f08b2-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f08b2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f08b2-113">Anzeigen von Listen verweisen</span><span class="sxs-lookup"><span data-stu-id="f08b2-113">Display Lists Reference</span></span>](display-lists-reference.md)
</dt> </dl>

 

 




