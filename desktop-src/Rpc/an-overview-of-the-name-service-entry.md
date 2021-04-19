---
title: Übersicht über den Eintrag "Name Service"
description: Der Name-Dienst Eintrag besteht aus drei unterschiedlichen Abschnitten.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338414"
---
# <a name="an-overview-of-the-name-service-entry"></a><span data-ttu-id="dd3b6-103">Übersicht über den Eintrag "Name Service"</span><span class="sxs-lookup"><span data-stu-id="dd3b6-103">An Overview of the Name Service Entry</span></span>

<span data-ttu-id="dd3b6-104">Der Name-Dienst Eintrag besteht aus drei unterschiedlichen Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-104">The name service entry consists of three distinct sections.</span></span> <span data-ttu-id="dd3b6-105">Der erste Abschnitt ist für Schnittstellen (UUID + Version), der zweite Abschnitt enthält die Objekt-UUIDs und der dritte Abschnitt für Bindungs Handles.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-105">The first section is for interfaces (UUID + version), the second section contains the object UUIDs, and the third section is for binding handles.</span></span> <span data-ttu-id="dd3b6-106">Sie geben einen Namen für den Eintrag an, der als Möglichkeit dient, ihn zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-106">You provide a name for the entry that will serve as a way to identify it.</span></span>

<span data-ttu-id="dd3b6-107">Beim Aufrufen von [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)gibt der Server den Namen des Eintrags an, in den die exportierten Informationen platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-107">When calling [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), the server specifies the name of the entry in which to place the exported information.</span></span> <span data-ttu-id="dd3b6-108">Diese neu exportierte Schnittstelle wird dann dem Schnittstellen Abschnitt des Namensdienst Eintrags hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-108">This newly exported interface is then added to the interface section of the name service entry.</span></span> <span data-ttu-id="dd3b6-109">Alle Schnittstellen, die bereits im Namen Dienst Eintrag vorhanden sind, bleiben ebenfalls erhalten.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-109">Any interfaces that are already present in the name service entry remain as well.</span></span> <span data-ttu-id="dd3b6-110">Der gleiche Vorgang wird für Objekt-UUIDs und Bindungs Handles befolgt.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-110">This same process is followed for object UUIDs and binding handles.</span></span>

<span data-ttu-id="dd3b6-111">Der Client ruft [**rpcnsbindinglookupbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (oder [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) auf, um nach einem entsprechenden Bindungs Handle zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-111">The client calls [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (or [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) to search for an appropriate binding handle.</span></span> <span data-ttu-id="dd3b6-112">Der Eintrags Name, das Schnittstellen Handle und eine Objekt-UUID werden extrahiert.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-112">The entry name, interface handle, and an object UUID are extracted.</span></span> <span data-ttu-id="dd3b6-113">Diese schränken die Einträge ein, von denen Bindungs Handles zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-113">These restrict the entries from which binding handles are returned.</span></span> <span data-ttu-id="dd3b6-114">Wenn ein Eintrag mit den Suchkriterien übereinstimmt, werden alle Bindungs Handles in diesem Eintrag von [**rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd3b6-114">If an entry matches the search criteria, all the binding handles in that entry are returned from [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span>

 

 




