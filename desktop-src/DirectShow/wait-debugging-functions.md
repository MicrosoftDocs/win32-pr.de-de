---
description: Wait-Debugging-Funktionen
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Wait-Debugging-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345811"
---
# <a name="wait-debugging-functions"></a><span data-ttu-id="df738-103">Wait-Debugging-Funktionen</span><span class="sxs-lookup"><span data-stu-id="df738-103">Wait Debugging Functions</span></span>

<span data-ttu-id="df738-104">Microsoft DirectShow stellt mehrere Funktionen zum Debuggen von unendlichen warte Vorgängen bereit.</span><span class="sxs-lookup"><span data-stu-id="df738-104">Microsoft DirectShow provides several functions for debugging infinite waits.</span></span>

<span data-ttu-id="df738-105">In Einzelhandels Builds funktionieren die [**dbgwaitformultipleobjects**](dbgwaitformultipleobjects.md) -und [**dbgwaitforsingleobject**](dbgwaitforsingleobject.md) -Funktionen wie Ihre Windows-API-Entsprechungen, **WaitForMultipleObjects** und **WaitForSingleObject**, mit unendlichen Timeout Intervallen.</span><span class="sxs-lookup"><span data-stu-id="df738-105">In retail builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions work like their Windows API counterparts, **WaitForMultipleObjects** and **WaitForSingleObject**, with infinite time-out intervals.</span></span>

<span data-ttu-id="df738-106">In Debugbuilds verwenden diese Funktionen einen globalen Timeout Wert.</span><span class="sxs-lookup"><span data-stu-id="df738-106">In debug builds, these functions use a global time-out value.</span></span> <span data-ttu-id="df738-107">Wenn das Timeout abgelaufen ist, löst die Funktion eine Assert-Funktion aus.</span><span class="sxs-lookup"><span data-stu-id="df738-107">If the time-out expires, the function triggers an assert.</span></span> <span data-ttu-id="df738-108">Der folgende Registrierungsschlüssel gibt den Timeout Wert (in Millisekunden) an:</span><span class="sxs-lookup"><span data-stu-id="df738-108">The following registry key specifies the time-out value, in milliseconds:</span></span>

<span data-ttu-id="df738-109">**Timeout für lokalen HKEY- \_ \_ Computer \\ <DebugRoot> \\ <Module Name> \\**</span><span class="sxs-lookup"><span data-stu-id="df738-109">**HKEY\_LOCAL\_MACHINE\\<DebugRoot>\\<Module Name>\\TIMEOUT**</span></span>

<span data-ttu-id="df738-110">*<DebugRoot>* dabei ist der Registrierungs Pfad, der im Thema [Debug Output Functions](debug-output-functions.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="df738-110">where *<DebugRoot>* is the registry path described in the topic [Debug Output Functions](debug-output-functions.md).</span></span>

<span data-ttu-id="df738-111">Wenn der Schlüssel nicht vorhanden ist, ist der Timeout Wert standardmäßig unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="df738-111">If the key does not exist, the time-out value defaults to INFINITE.</span></span> <span data-ttu-id="df738-112">Sie können die [**dbgsetwaittimeout**](dbgsetwaittimeout.md) -Funktion verwenden, um den Registrierungs Eintrag zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="df738-112">You can use the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function to override the registry entry.</span></span>



| <span data-ttu-id="df738-113">Funktion</span><span class="sxs-lookup"><span data-stu-id="df738-113">Function</span></span>                                                       | <span data-ttu-id="df738-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df738-114">Description</span></span>                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="df738-115">**Dbgsetwaittimeout**</span><span class="sxs-lookup"><span data-stu-id="df738-115">**DbgSetWaitTimeout**</span></span>](dbgsetwaittimeout.md)                 | <span data-ttu-id="df738-116">Legt den Timeout Wert für das Debuggen fest.</span><span class="sxs-lookup"><span data-stu-id="df738-116">Sets the debugging time-out value.</span></span>                              |
| [<span data-ttu-id="df738-117">**Dbgwaitformultipleobjects**</span><span class="sxs-lookup"><span data-stu-id="df738-117">**DbgWaitForMultipleObjects**</span></span>](dbgwaitformultipleobjects.md) | <span data-ttu-id="df738-118">Wartet darauf, dass alle (oder alle) der angegebenen Objekte signalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="df738-118">Waits for any (or all) of the specified objects to be signaled.</span></span> |
| [<span data-ttu-id="df738-119">**Dbgwaitforsingleobject**</span><span class="sxs-lookup"><span data-stu-id="df738-119">**DbgWaitForSingleObject**</span></span>](dbgwaitforsingleobject.md)       | <span data-ttu-id="df738-120">Wartet darauf, dass ein Objekt signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="df738-120">Waits for an object to become signaled.</span></span>                         |



 

 

 



