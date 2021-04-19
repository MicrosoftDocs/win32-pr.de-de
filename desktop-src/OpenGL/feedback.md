---
title: Feedback
description: Im Feedback Modus generiert jedes primitive, das rasterisiert werden soll, einen Block von Werten, die in das Feedback Array kopiert werden.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- Feedback Modus, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106373426"
---
# <a name="feedback-mode"></a><span data-ttu-id="fa8fb-104">Feedback Modus</span><span class="sxs-lookup"><span data-stu-id="fa8fb-104">Feedback mode</span></span>

<span data-ttu-id="fa8fb-105">Im Feedback Modus generiert jedes primitive, das rasterisiert werden soll, einen Block von Werten, die in das Feedback Array kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="fa8fb-105">In feedback mode, each primitive to be rasterized generates a block of values that is copied into the feedback array.</span></span> <span data-ttu-id="fa8fb-106">Geben Sie dieses Array mit [**glfeedbackbuffer**](glfeedbackbuffer.md)an, das aufgerufen werden muss, bevor OpenGL in den Feedback Modus versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fa8fb-106">Supply this array with [**glFeedbackBuffer**](glfeedbackbuffer.md), which you must call before putting OpenGL into feedback mode.</span></span> <span data-ttu-id="fa8fb-107">Jeder Block von Werten beginnt mit einem Code, der den primitiven Typ anzeigt, gefolgt von Werten, die die Scheitel Punkte und zugeordneten Daten des primitiven beschreiben.</span><span class="sxs-lookup"><span data-stu-id="fa8fb-107">Each block of values begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="fa8fb-108">Einträge werden auch für Bitmaps und Pixel Rechtecke geschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa8fb-108">Entries are also written for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="fa8fb-109">Es ist nicht garantiert, dass die Werte in das Feedback Array geschrieben werden, bis Sie " [**glrendermode**](glrendermode.md) " aufgerufen haben, um OpenGL aus dem Feedback Modus zu nehmen.</span><span class="sxs-lookup"><span data-stu-id="fa8fb-109">Values are not guaranteed to be written into the feedback array until you call [**glRenderMode**](glrendermode.md) to take OpenGL out of feedback mode.</span></span> <span data-ttu-id="fa8fb-110">Sie können mit [**glpassthrough**](glpassthrough.md) einen Marker angeben, der im Feedback Modus zurückgegeben wird, als ob es sich um einen primitiven handelt.</span><span class="sxs-lookup"><span data-stu-id="fa8fb-110">You can use [**glPassThrough**](glpassthrough.md) to supply a marker that is returned in feedback mode as if it were a primitive.</span></span>

 

 




