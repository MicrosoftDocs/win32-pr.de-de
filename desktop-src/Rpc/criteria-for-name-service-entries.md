---
title: Kriterien für Namensdienst Einträge
description: Kriterien für Namensdienst Einträge mit Remote Prozedur Aufruf (RPC).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471453"
---
# <a name="criteria-for-name-service-entries"></a><span data-ttu-id="5fcf3-103">Kriterien für Namensdienst Einträge</span><span class="sxs-lookup"><span data-stu-id="5fcf3-103">Criteria for Name Service Entries</span></span>

<span data-ttu-id="5fcf3-104">Beim Verarbeiten von Namensdienst Einträgen werden folgende Kriterien verwendet:</span><span class="sxs-lookup"><span data-stu-id="5fcf3-104">The following criteria are used when processing name service entries:</span></span>

-   <span data-ttu-id="5fcf3-105">Wenn Sie für [**rpcnsbindinglookupbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)einen nicht-**null** -Eingabe Namen angeben, ist dieser Eintrag der einzige Eintrag, der nach Bindungs Handles durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-105">If you provide a non-**NULL** entry name for [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), that entry will be the only entry searched for binding handles.</span></span> <span data-ttu-id="5fcf3-106">Wenn Sie **null** übergeben, werden alle Einträge in der Anmelde Domäne durchsucht.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-106">If you pass **NULL**, all entries in your logon domain will be searched.</span></span> <span data-ttu-id="5fcf3-107">Beachten Sie, dass dies keine vertrauenswürdigen Domänen umfasst.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-107">Note that this does not include trusted domains.</span></span>
-   <span data-ttu-id="5fcf3-108">Wenn Sie ein Schnittstellen handle bereitstellen, werden Bindungs Handles nur von einem Eintrag zurückgegeben, wenn der Schnittstellen Abschnitt des Eintrags eine kompatible Version der Schnittstelle uuid enthält.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-108">If you provide an interface handle, binding handles are returned from an entry only if the interface section of the entry contains a compatible version of that interface UUID.</span></span> <span data-ttu-id="5fcf3-109">Das heißt, die Hauptversionsnummer muss mit der UUID der Schnittstelle identisch sein, während die neben Versionsnummer größer oder gleich ihrem Wert sein muss.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-109">That is, the major version number must be the same as your interface UUID, while the minor version number must be equal to or greater than yours.</span></span>
-   <span data-ttu-id="5fcf3-110">Wenn Sie eine Objekt-UUID angeben, werden Bindungs Handles nur von einem Eintrag zurückgegeben, wenn der Objekt-UUID-Abschnitt des Eintrags dieses bestimmte Objekt "uuid" enthält.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-110">If you provide an object UUID, binding handles are returned from an entry only if the object UUID section of the entry contains that particular object UUID.</span></span>

<span data-ttu-id="5fcf3-111">Wenn ein Name-Dienst Eintrag die oben beschriebenen Kriterien überschreitet, werden alle Bindungs Handles aus diesen Einträgen gesammelt.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-111">If a name service entry survives the criteria described above, all the binding handles from those entries are gathered.</span></span> <span data-ttu-id="5fcf3-112">Handles mit einer Protokoll Sequenz, die vom Client nicht unterstützt wird, werden verworfen, und die restlichen Handles werden als Ausgabe von [**rpcnsbindinglookupnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-112">Handles with a protocol sequence that is unsupported by the client are discarded and the remaining handles are returned to you as the output from [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span></span>

 

 




