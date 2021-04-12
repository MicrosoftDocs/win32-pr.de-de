---
title: RPC-Puffer Zuordnungs Fehler
description: Da die RPC-Lauf Zeit Bibliothek Speicher für Sende-und Empfangs Puffer zuordnet, sollte die Funktion RPC-Zuordnungs Fehler erwarten.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309967"
---
# <a name="rpc-buffer-allocation-errors"></a><span data-ttu-id="e9e76-103">RPC-Puffer Zuordnungs Fehler</span><span class="sxs-lookup"><span data-stu-id="e9e76-103">RPC Buffer Allocation Errors</span></span>

<span data-ttu-id="e9e76-104">Da die RPC-Lauf Zeit Bibliothek Speicher für Sende-und Empfangs Puffer zuordnet, sollte die Funktion RPC-Zuordnungs Fehler erwarten.</span><span class="sxs-lookup"><span data-stu-id="e9e76-104">Because the RPC run-time library allocates memory for send and receive buffers, the function should expect RPC allocation errors.</span></span> <span data-ttu-id="e9e76-105">Im Fall eines RPC-Zuordnungs Fehlers wird ein fort Setz bares Handle für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="e9e76-105">In the event of an RPC allocation error, a resumable handle is invalidated.</span></span> <span data-ttu-id="e9e76-106">Dies ist eine Voraussetzung, weil fort Setz Bare Funktionen nicht wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="e9e76-106">This is a requirement because resumable functions are not rewindable.</span></span>

 

 




