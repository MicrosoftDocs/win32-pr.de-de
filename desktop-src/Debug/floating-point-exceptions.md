---
description: Standardmäßig sind alle FP-Ausnahmen im System deaktiviert.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Gleitkommaausnahmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342572"
---
# <a name="floating-point-exceptions"></a><span data-ttu-id="d1b97-103">Gleitkommaausnahmen</span><span class="sxs-lookup"><span data-stu-id="d1b97-103">Floating-Point Exceptions</span></span>

<span data-ttu-id="d1b97-104">Standardmäßig sind alle FP-Ausnahmen im System deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d1b97-104">By default, the system has all FP exceptions turned off.</span></span> <span data-ttu-id="d1b97-105">Daher führen Berechnungen in Nan oder Infinity anstelle einer Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="d1b97-105">Therefore, computations result in NAN or INFINITY, rather than an exception.</span></span> <span data-ttu-id="d1b97-106">Bevor Sie Gleit Komma Ausnahmen (FP) mithilfe der strukturierten Ausnahmebehandlung abfangen können, müssen Sie die [ \_ controlfp \_ s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C-Lauf Zeit Bibliotheksfunktion zum Aktivieren aller möglichen FP-Ausnahmen aufruft.</span><span class="sxs-lookup"><span data-stu-id="d1b97-106">Before you can trap floating-point (FP) exceptions using structured exception handling, you must call the [\_controlfp\_s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C run-time library function to turn on all possible FP exceptions.</span></span> <span data-ttu-id="d1b97-107">Wenn nur bestimmte Ausnahmen abgefangen werden sollen, verwenden Sie nur die Flags, die den zu erfassenden Ausnahmen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d1b97-107">To trap only particular exceptions, use only the flags that correspond to the exceptions to be trapped.</span></span> <span data-ttu-id="d1b97-108">Beachten Sie, dass jeder Handler für FP-Fehler [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) als erste FP-Anweisung aufrufen sollte.</span><span class="sxs-lookup"><span data-stu-id="d1b97-108">Note that any handler for FP errors should call [\_clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) as its first FP instruction.</span></span> <span data-ttu-id="d1b97-109">Diese Funktion löscht Gleit Komma Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="d1b97-109">This function clears floating-point exceptions.</span></span>

 

 
