---
title: Funktionsattribute
description: Die Attribute \ Callback \ und \ local \ können als Funktions Attribute angewendet werden.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729641"
---
# <a name="function-attributes"></a><span data-ttu-id="6d3dc-103">Funktionsattribute</span><span class="sxs-lookup"><span data-stu-id="6d3dc-103">Function Attributes</span></span>

<span data-ttu-id="6d3dc-104">Die **\[** Attribute [**Callback**](/windows/desktop/Midl/callback) **\]** und **\[** [**local**](/windows/desktop/Midl/local) **\]** können als Funktions Attribute angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d3dc-104">The **\[**[**callback**](/windows/desktop/Midl/callback)**\]** and **\[**[**local**](/windows/desktop/Midl/local)**\]** attributes can be applied as function attributes.</span></span>

<span data-ttu-id="6d3dc-105">Ein Rückruf ist ein Remote-Aufrufe von Server zu Client, der als Teil eines konzeptionellen Single-Execution-Threads ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d3dc-105">A callback is a remote call from server to client that executes as part of a conceptual single-execution thread.</span></span> <span data-ttu-id="6d3dc-106">Ein Rückruf wird immer im Kontext eines Remote Aufrufs (oder eines Rückrufs) ausgegeben und von dem Thread ausgeführt, der den ursprünglichen Remote Rückruf (oder Rückruf) ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="6d3dc-106">A callback is always issued in the context of a remote call (or callback) and is executed by the thread that issued the original remote call (or callback).</span></span>

<span data-ttu-id="6d3dc-107">Häufig ist es wünschenswert, eine lokale Prozedur Deklaration in der IDL-Datei zu platzieren, da dies die logische Stelle ist, um Schnittstellen zu einem Paket zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6d3dc-107">It is often desirable to place a local procedure declaration in the IDL file, since this is the logical place to describe interfaces to a package.</span></span> <span data-ttu-id="6d3dc-108">Das **\[** [**local**](/windows/desktop/Midl/local) - **\]** Attribut gibt an, dass eine Prozedur Deklaration nicht tatsächlich eine Remote Funktion, sondern eine lokale Prozedur ist.</span><span class="sxs-lookup"><span data-stu-id="6d3dc-108">The **\[**[**local**](/windows/desktop/Midl/local)**\]** attribute indicates that a procedure declaration is not actually a remote function, but a local procedure.</span></span> <span data-ttu-id="6d3dc-109">Der mittlerer l-Compiler generiert keine stubfunktionen für Funktionen mit dem **\[ lokalen \]** Attribut.</span><span class="sxs-lookup"><span data-stu-id="6d3dc-109">The MIDL compiler does not generate any stubs for functions with the **\[local\]** attribute.</span></span>

<span data-ttu-id="6d3dc-110">Beachten Sie, dass die Verwendung von **\[** [**Callback**](/windows/desktop/Midl/callback) **\]** bei der Multithreadprogrammierung nicht empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="6d3dc-110">It is important to note that the use of **\[**[**callback**](/windows/desktop/Midl/callback)**\]** is not recommended in multi-thread programming.</span></span> <span data-ttu-id="6d3dc-111">Als Single Thread-Programmierfunktion ist Sie nicht für die Unterstützung der Sicherheitsanforderungen, die eine Multithreadumgebung bereitstellt, bereit.</span><span class="sxs-lookup"><span data-stu-id="6d3dc-111">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

 

 