---
description: Wird vom Compiler aufgerufen, wenn Sie über mehr als eine Seite lokaler Variablen in der Funktion verfügen.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk-Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a58b31836947dfb1816bea72a54f820354c792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958127"
---
# <a name="_chkstk-routine"></a><span data-ttu-id="55e96-103">\_chkstk-Routine</span><span class="sxs-lookup"><span data-stu-id="55e96-103">\_chkstk Routine</span></span>

<span data-ttu-id="55e96-104">Wird vom Compiler aufgerufen, wenn Sie über mehr als eine Seite lokaler Variablen in der Funktion verfügen.</span><span class="sxs-lookup"><span data-stu-id="55e96-104">Called by the compiler when you have more than one page of local variables in your function.</span></span>

## <a name="remarks"></a><span data-ttu-id="55e96-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55e96-105">Remarks</span></span>

<span data-ttu-id="55e96-106">\_die chkstk-Routine ist eine Hilfsroutine für den C-Compiler.</span><span class="sxs-lookup"><span data-stu-id="55e96-106">\_chkstk Routine is a helper routine for the C compiler.</span></span> <span data-ttu-id="55e96-107">Bei x86-Compilern \_ wird die chkstk-Routine aufgerufen, wenn die lokalen Variablen 4 KB überschreiten. für x64-Compiler beträgt der Wert 8K.</span><span class="sxs-lookup"><span data-stu-id="55e96-107">For x86 compilers, \_chkstk Routine is called when the local variables exceed 4K bytes; for x64 compilers it is 8K.</span></span>

 

 



