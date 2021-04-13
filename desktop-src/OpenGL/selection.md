---
title: Auswahl
description: Auswahl gibt den aktuellen Inhalt des Namens Stapels zurück, bei dem es sich um ein Array von Namen mit ganzzahligen Werten handelt.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- Auswahlmodus OpenGL
- Auswahl Treffer OpenGL
- Treffer Datensätze OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310376"
---
# <a name="selection"></a><span data-ttu-id="747e7-106">Auswahl</span><span class="sxs-lookup"><span data-stu-id="747e7-106">Selection</span></span>

<span data-ttu-id="747e7-107">Auswahl gibt den aktuellen Inhalt des Namens Stapels zurück, bei dem es sich um ein Array von Namen mit ganzzahligen Werten handelt.</span><span class="sxs-lookup"><span data-stu-id="747e7-107">Selection returns the current contents of the name stack, which is an array of names with integer values.</span></span> <span data-ttu-id="747e7-108">Sie weisen die Namen zu und erstellen den namens Stapel innerhalb des Modellierungs Codes, der die Geometrie von Objekten angibt, die Sie zeichnen möchten.</span><span class="sxs-lookup"><span data-stu-id="747e7-108">You assign the names and build the name stack within the modeling code that specifies the geometry of objects you want to draw.</span></span> <span data-ttu-id="747e7-109">Wenn dann im Auswahlmodus ein primitiv das Clip Volume überschneidet, tritt ein Auswahl Treffer auf.</span><span class="sxs-lookup"><span data-stu-id="747e7-109">Then, in selection mode, whenever a primitive intersects the clip volume, a selection hit occurs.</span></span> <span data-ttu-id="747e7-110">Der Treffer Daten Satz, der in das Auswahl Array geschrieben wird, das Sie mit [**glselectbuffer**](glselectbuffer.md)angegeben haben, enthält Informationen zum Inhalt des Namens Stapels zum Zeitpunkt des Treffer.</span><span class="sxs-lookup"><span data-stu-id="747e7-110">The hit record, which is written into the selection array you've supplied with [**glSelectBuffer**](glselectbuffer.md), contains information about the contents of the name stack at the time of the hit.</span></span>

> [!Note]  
> <span data-ttu-id="747e7-111">Nennen Sie [**glselectbuffer**](glselectbuffer.md) , bevor Sie OpenGL mit [**glrendermode**](glrendermode.md)in den Auswahlmodus versetzen.</span><span class="sxs-lookup"><span data-stu-id="747e7-111">Call [**glSelectBuffer**](glselectbuffer.md) before you put OpenGL into selection mode with [**glRenderMode**](glrendermode.md).</span></span> <span data-ttu-id="747e7-112">Es ist nicht garantiert, dass der gesamte Inhalt des Namens Stapels zurückgegeben wird, bis Sie **glrendermode** aufgerufen haben, um OpenGL aus dem Auswahlmodus zu nehmen.</span><span class="sxs-lookup"><span data-stu-id="747e7-112">The entire contents of the name stack aren't guaranteed to be returned until you call **glRenderMode** to take OpenGL out of selection mode.</span></span>

 

<span data-ttu-id="747e7-113">Ändern Sie den Namen Stapel mit " [**glinitnames**](glinitnames.md)", " [**glloadname**](glloadname.md)", " [**glpushname**](glpushname.md)" und " [**glpopname**](glpopname.md)".</span><span class="sxs-lookup"><span data-stu-id="747e7-113">Manipulate the name stack with [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md), and [**glPopName**](glpopname.md).</span></span> <span data-ttu-id="747e7-114">Sie können auch " [**glupickmatrix**](glupickmatrix.md) " zur Auswahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="747e7-114">You can also use [**gluPickMatrix**](glupickmatrix.md) for selection.</span></span>

 

 




