---
title: Aufzählen von Gruppen, die viele Elemente enthalten
description: Erfahren Sie mehr über das Aufzählen Azure Active Directory Gruppen, die viele Elemente enthalten, indem Sie den inkrementellen Abruf von Daten (Bereichsabruf) verwenden.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Auflisten von Gruppen, die viele Active Directory-Mitglieder enthalten
- gruppen Active Directory , Auflisten von Gruppen mit vielen Mitgliedern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cab63b809fdbd2666f39a09d32f601346da00e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405153"
---
# <a name="enumerating-groups-that-contain-many-members"></a><span data-ttu-id="b2edc-105">Aufzählen von Gruppen, die viele Elemente enthalten</span><span class="sxs-lookup"><span data-stu-id="b2edc-105">Enumerating Groups That Contain Many Members</span></span>

<span data-ttu-id="b2edc-106">Die Mitglieder einer Gruppe werden in einem Mehrwertattribut namens **Member** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b2edc-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="b2edc-107">Das  Memberattribut kann eine große Anzahl von Werten enthalten.</span><span class="sxs-lookup"><span data-stu-id="b2edc-107">The **member** attribute can contain a large number of values.</span></span> <span data-ttu-id="b2edc-108">Das Auflisten von Membern kann ineffizient sein, wenn die Anzahl der Werte in einem mehrwertigen Attribut groß wird.</span><span class="sxs-lookup"><span data-stu-id="b2edc-108">Enumerating members can be inefficient when the number of values in a multi-valued attribute becomes large.</span></span> <span data-ttu-id="b2edc-109">Der Server begrenzt auch die maximale Anzahl von Werten, die in einer einzelnen Abfrage abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="b2edc-109">The server will also limit the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="b2edc-110">Dies bedeutet, dass, wenn eine Gruppe möglicherweise mehr Mitglieder hat, als vom Server bereitgestellt werden können, die einzige Möglichkeit zum Aufzählen aller Elemente der inkrementelle Abruf von Daten ist, die als *Bereichsabruf* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="b2edc-110">This means that if a group may have more members than can be supplied by the server, the only way to enumerate all members is to use incremental retrieval of data, known as *range retrieval*.</span></span>

<span data-ttu-id="b2edc-111">Der Bereichsabruf umfasst das Anfordern einer begrenzten Anzahl von Attributwerten in einer einzelnen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b2edc-111">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="b2edc-112">Die Anzahl der angeforderten Werte muss kleiner oder gleich der maximalen Anzahl von Werten sein, die vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b2edc-112">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="b2edc-113">Um zu reduzieren, wie oft die Abfrage den Server kontaktieren muss, sollte die Anzahl der angeforderten Werte so nahe wie möglich an diesem Maximum liegen.</span><span class="sxs-lookup"><span data-stu-id="b2edc-113">To reduce the number of times the query must contact the server, the number of values requested should be as close, as possible, to this maximum.</span></span> <span data-ttu-id="b2edc-114">Damit eine Anwendung ordnungsgemäß mit allen Servern funktioniert, sollte eine maximale Anzahl von 1.000 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2edc-114">To enable an application to work correctly with all servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="b2edc-115">Die Version des Servers, der die angeforderten Daten liefert, bestimmt die maximale Anzahl von Werten, die in einer einzelnen Abfrage abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="b2edc-115">The version of the server that supplies the requested data determines the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="b2edc-116">In der folgenden Tabelle sind die Serverversion und die maximale Anzahl von Werten aufgeführt, die in einer einzelnen Abfrage abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="b2edc-116">The following table lists the server version and the maximum number of values that can be retrieved in a single query.</span></span>



| <span data-ttu-id="b2edc-117">Version des Serverbetriebssystems</span><span class="sxs-lookup"><span data-stu-id="b2edc-117">Server operating system version</span></span> | <span data-ttu-id="b2edc-118">Abgerufene Höchstwerte</span><span class="sxs-lookup"><span data-stu-id="b2edc-118">Maximum values retrieved</span></span> |
|---------------------------------|--------------------------|
| <span data-ttu-id="b2edc-119">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b2edc-119">Windows 2000</span></span>                    | <span data-ttu-id="b2edc-120">1000</span><span class="sxs-lookup"><span data-stu-id="b2edc-120">1000</span></span>                     |
| <span data-ttu-id="b2edc-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2edc-121">Windows Server 2003</span></span>             | <span data-ttu-id="b2edc-122">1500</span><span class="sxs-lookup"><span data-stu-id="b2edc-122">1500</span></span>                     |



 

<span data-ttu-id="b2edc-123">Weitere Informationen zum Abrufen von Bereichen von Attributwerten mit ADSI finden Sie unter Abrufen von [Attributbereichen.](/windows/desktop/ADSI/attribute-range-retrieval)</span><span class="sxs-lookup"><span data-stu-id="b2edc-123">For more information about retrieving ranges of attribute values with ADSI, see [Attribute Range Retrieval](/windows/desktop/ADSI/attribute-range-retrieval).</span></span>

<span data-ttu-id="b2edc-124">Weitere Informationen zum Abrufen von Bereichen von Attributwerten mit [System.DirectoryServices](/dotnet/api/system.directoryservices)finden Sie unter [Auflisten von Membern in einer großen Gruppe.](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx)</span><span class="sxs-lookup"><span data-stu-id="b2edc-124">For more information about retrieving ranges of attribute values with [System.DirectoryServices](/dotnet/api/system.directoryservices), see [Enumerating Members in a Large Group](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span></span>

 

 