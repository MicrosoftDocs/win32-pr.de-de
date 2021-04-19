---
title: Fehlerbehandlung (OpenGL)
description: Wenn OpenGL einen Fehler erkennt, wird ein aktueller Fehlercode aufgezeichnet.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- Fehlerbehandlung bei OpenGL
- OpenGL-Fehlerbehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337699"
---
# <a name="error-handling-opengl"></a><span data-ttu-id="5dded-105">Fehlerbehandlung (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="5dded-105">Error Handling (OpenGL)</span></span>

<span data-ttu-id="5dded-106">Wenn OpenGL einen Fehler erkennt, wird ein aktueller Fehlercode aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5dded-106">When OpenGL detects an error, it records a current error code.</span></span> <span data-ttu-id="5dded-107">Die Funktion, die den Fehler verursacht hat, wird ignoriert und hat daher keine Auswirkung auf den OpenGL-Zustand oder den Frame Puffer-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="5dded-107">The function that caused the error is ignored, so it has no effect on the OpenGL state or on the framebuffer contents.</span></span> <span data-ttu-id="5dded-108">(Wenn der aufgezeichnete Fehler "GL \_ " war Nicht genügend Arbeits \_ \_ Speicher, die Ergebnisse der Funktion sind jedoch nicht definiert.) Nachdem Sie aufgezeichnet wurde, wird der aktuelle Fehlercode erst gelöscht, wenn Sie die Abfragefunktion " [**glgeterror**](glgeterror.md) " aufrufen, die den aktuellen Fehlercode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5dded-108">(If the error recorded was GL\_OUT\_OF\_MEMORY, however, the results of the function are undefined.) Once recorded, the current error code isn't cleared until you call the [**glGetError**](glgeterror.md) query function, which returns the current error code.</span></span>

<span data-ttu-id="5dded-109">Implementierungen von OpenGL können mehrere aktuelle Fehlercodes zurückgeben, die jeweils so lange festgelegt bleiben, bis Sie abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="5dded-109">Implementations of OpenGL may return multiple current error codes, each of which remains set until queried.</span></span> <span data-ttu-id="5dded-110">Die **glgeterror** -Funktion gibt den Fehler "GL No error" zurück, wenn \_ \_ Sie alle aktuellen Fehlercodes abgefragt haben oder wenn kein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="5dded-110">The **glGetError** function returns GL\_NO\_ERROR once you've queried all the current error codes or if there is no error.</span></span> <span data-ttu-id="5dded-111">Wenn Sie also einen Fehlercode erhalten, rufen Sie **glgeterror** auf, bis GL \_ kein \_ Fehler zurückgegeben wird, um sicherzustellen, dass Sie alle Fehler ermittelt haben.</span><span class="sxs-lookup"><span data-stu-id="5dded-111">Therefore, if you obtain an error code, call **glGetError** until GL\_NO\_ERROR is returned to be sure you've discovered all the errors.</span></span> <span data-ttu-id="5dded-112">Eine Liste der Fehlercodes finden Sie unter [OpenGL-Fehlercodes](opengl-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5dded-112">For the list of error codes, see [OpenGL error codes](opengl-error-codes.md).</span></span>

<span data-ttu-id="5dded-113">Sie können die Funktion " [**gluerrorstring**](gluerrorstring.md) glu" verwenden, um eine beschreibende Zeichenfolge zu erhalten, die dem Fehlercode entspricht, der in der Übergabe</span><span class="sxs-lookup"><span data-stu-id="5dded-113">You can use the [**gluErrorString**](gluerrorstring.md) GLU function to obtain a descriptive string corresponding to the error code passed in.</span></span> <span data-ttu-id="5dded-114">Weitere Informationen zu " **gluerrorstring**" finden Sie unter [Behandeln von Fehlern](handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="5dded-114">For more information on **gluErrorString**, see [Handling Errors](handling-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="5dded-115">Die glu-Funktionen geben häufig Fehler Werte zurück, wenn ein Fehler erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="5dded-115">GLU functions often return error values if an error is detected.</span></span> <span data-ttu-id="5dded-116">Die OpenGL Utility Library definiert außerdem die Fehlercodes glu \_ invalid \_ enum, Glu \_ invalid \_ Value und glu \_ out \_ of \_ Memory, die dieselbe Bedeutung wie die zugehörigen OpenGL-Fehlercodes haben.</span><span class="sxs-lookup"><span data-stu-id="5dded-116">Also, the OpenGL Utility library defines the error codes GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY, which have the same meaning as the related OpenGL error codes.</span></span>

 

 

 




