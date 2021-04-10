---
title: Verwenden des/robust-Flags
description: Kompilieren Sie IDL-Dateien immer mithilfe des/robust-Schalters.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948880"
---
# <a name="use-the-robust-flag"></a><span data-ttu-id="6b349-103">Verwenden des/robust-Flags</span><span class="sxs-lookup"><span data-stu-id="6b349-103">Use the /robust Flag</span></span>

<span data-ttu-id="6b349-104">Kompilieren Sie IDL-Dateien immer mithilfe des [**/robust**](/windows/desktop/Midl/-robust) -Schalters.</span><span class="sxs-lookup"><span data-stu-id="6b349-104">Always compile .idl files using the [**/robust**](/windows/desktop/Midl/-robust) switch.</span></span> <span data-ttu-id="6b349-105">Durch die Verwendung des **/robust** -Schalters werden zusätzliche Informationen generiert, mit denen die Engine für die Netzwerkdaten Darstellung die Lauf Zeit Fehlerüberprüfung für korrelierte Argumente in dynamischen Arrays, Unions und in out-Schnittstellen Zeigern in com-und RPC-Anwendungen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="6b349-105">Using the **/robust** switch generates additional information that enables the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in out interface pointers in COM and RPC applications.</span></span> <span data-ttu-id="6b349-106">Wenn die Kompilierung von Software mit diesem Flag nicht möglich ist, ist die Software so verfügbar, dass Sie nicht durch Aktivitäten in einem anderen Bereich geschützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b349-106">If software fails to compile with this flag, the software is so exposed to attacks that no efforts in any other area can protect it.</span></span>

 

 