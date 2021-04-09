---
title: Kombinieren von Pipe-und nonpipe-Parametern
description: Kombinieren von Pipe-und nonpipe-Parametern im Remote Prozedur Aufruf (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858401"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a><span data-ttu-id="ae8d2-103">Kombinieren von Pipe-und nonpipe-Parametern</span><span class="sxs-lookup"><span data-stu-id="ae8d2-103">Combining Pipe and Nonpipe Parameters</span></span>

<span data-ttu-id="ae8d2-104">Wenn Sie Pipetypen und andere Typen in einem Remote Prozedur aufrufsbefehl kombinieren, werden die Daten gemäß der Richtung des Parameters übertragen:</span><span class="sxs-lookup"><span data-stu-id="ae8d2-104">When you combine pipe types and other types in a remote procedure call, the data is transmitted according to the direction of the parameter:</span></span>

-   <span data-ttu-id="ae8d2-105">**In Richtung werden \[ die Daten für alle nonpipe-Argumente zuerst übertragen, gefolgt von pipedaten. \]**</span><span class="sxs-lookup"><span data-stu-id="ae8d2-105">In the **\[in\]** direction, the data for all nonpipe arguments is transmitted first, followed by pipe data.</span></span>
-   <span data-ttu-id="ae8d2-106">In der **\[ Ausrichtungs \]** Richtung sendet der Server zuerst die Pipe-Daten.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-106">In the **\[out\]** direction, the server sends the pipe data first.</span></span> <span data-ttu-id="ae8d2-107">Nachdem die Manager-Routine zurückgegeben wurde, überträgt der Server die nonpipe-Daten.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-107">After the manager routine returns, the server transmits the nonpipe data.</span></span>
-   <span data-ttu-id="ae8d2-108">Wenn **\[ in, out \]** -Pipe-Argumente in Kombination mit **\[ in \] -, out-, out** -, out-und over-Pipe-Argumenten vorhanden sind, werden zuerst die Eingabedaten wie zuvor beschrieben übertragen.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-108">When there are **\[in,out\]** pipe arguments combined with **\[in,out\]** non-pipe arguments, first the input data is transmitted in its entirety, as previously described.</span></span> <span data-ttu-id="ae8d2-109">Anschließend werden die Ausgabedaten wie zuvor beschrieben übertragen.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-109">Then, the output data is transmitted as previously described.</span></span>

<span data-ttu-id="ae8d2-110">Die folgende Einschränkung gilt für diese (Mittel l 3,0) Implementierung von Pipes: Wenn Sie Pipetypen und andere Typen in einem einzelnen Remote Prozedur aufzurufen kombinieren, müssen die nonpipe-Parameter über eine klar definierte Größe verfügen, damit der Mittelwert Compiler die benötigte Puffergröße berechnen kann.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-110">The following restriction applies to this (MIDL 3.0) implementation of pipes: When you combine pipe types and other types in a single remote procedure call, the nonpipe parameters must have a well-defined size in order to allow the MIDL compiler to calculate the buffer size needed.</span></span> <span data-ttu-id="ae8d2-111">Sie können z. b. keine pipenameter mit einem \[ [eindeutigen](/windows/desktop/Midl/unique) \] Zeiger oder einer konformen Struktur kombinieren, da ihre Größe zum Zeitpunkt der Kompilierung nicht bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-111">For example, you cannot combine pipe parameters with a \[ [unique](/windows/desktop/Midl/unique)\] pointer or a conformant structure, since their sizes cannot be determined at compile time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae8d2-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae8d2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae8d2-113">Kanal</span><span class="sxs-lookup"><span data-stu-id="ae8d2-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="ae8d2-114">/Oi</span><span class="sxs-lookup"><span data-stu-id="ae8d2-114">/Oi</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 