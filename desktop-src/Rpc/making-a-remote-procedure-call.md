---
title: Ausführen eines Remote Prozedur Aufrufes
description: Sobald das Client Programm verteilter Anwendungen, die explizite Bindungs Handles verwenden, über ein Bindungs Handle verfügt, kann es Remote Prozeduren ausführen.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Anrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707182"
---
# <a name="making-a-remote-procedure-call"></a><span data-ttu-id="349e3-104">Ausführen eines Remote Prozedur Aufrufes</span><span class="sxs-lookup"><span data-stu-id="349e3-104">Making a Remote Procedure Call</span></span>

<span data-ttu-id="349e3-105">Sobald das Client Programm verteilter Anwendungen, die explizite Bindungs Handles verwenden, über ein Bindungs Handle verfügt, kann es Remote Prozeduren ausführen.</span><span class="sxs-lookup"><span data-stu-id="349e3-105">Once the client program of distributed applications that uses explicit binding handles has a binding handle, it can execute remote procedures.</span></span>

<span data-ttu-id="349e3-106">Microsoft RPC bietet auch benutzerdefinierte Bindungs Handles, implizite Bindungs Handles und automatische Bindungs Handles.</span><span class="sxs-lookup"><span data-stu-id="349e3-106">Microsoft RPC also offers custom binding handles, implicit binding handles, and automatic binding handles.</span></span> <span data-ttu-id="349e3-107">Diese Bindungs Handles bieten Client-und Serverprogrammen verschiedene Steuerungs Ebenen für das Ausführen von Remote Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="349e3-107">These binding handles offer client and server programs different levels of control over the process of executing remote procedures.</span></span> <span data-ttu-id="349e3-108">Ausführliche Informationen zu verschiedenen handle-Typen und der von Ihnen angebotenen Flexibilität finden Sie unter [Bindung und Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="349e3-108">For details on different handle types and the flexibility they offer, see [Binding and Handles](binding-and-handles.md).</span></span>

<span data-ttu-id="349e3-109">Um den Prozedur Aufruf Remote auszuführen, müssen Sie die Client seitige Stub-Funktion auf die gleiche Weise aufrufen, wie jede C-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="349e3-109">To execute the procedure call remotely, call the client-side stub function in the same manner any C function is called.</span></span>

 

 




