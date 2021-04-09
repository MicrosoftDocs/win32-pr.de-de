---
title: Auflisten von Gruppen, die viele Member enthalten
description: Die Mitglieder einer Gruppe werden in einem mehrwertigen Attribut mit dem Namen "Member" gespeichert.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Auflisten von Gruppen, die viele Member enthalten Active Directory
- Gruppen Active Directory, Auflisten von Gruppen mit vielen Membern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2d9a5c9abc6e77ac72672379789d1028f92c3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101454"
---
# <a name="enumerating-groups-that-contain-many-members"></a><span data-ttu-id="f031b-105">Auflisten von Gruppen, die viele Member enthalten</span><span class="sxs-lookup"><span data-stu-id="f031b-105">Enumerating Groups That Contain Many Members</span></span>

<span data-ttu-id="f031b-106">Die Mitglieder einer Gruppe werden in einem mehrwertigen Attribut mit dem Namen " **Member**" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f031b-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="f031b-107">Das **Member** -Attribut kann eine große Anzahl von Werten enthalten.</span><span class="sxs-lookup"><span data-stu-id="f031b-107">The **member** attribute can contain a large number of values.</span></span> <span data-ttu-id="f031b-108">Das Auflisten von Membern kann ineffizient sein, wenn die Anzahl von Werten in einem mehrwertigen Attribut groß wird.</span><span class="sxs-lookup"><span data-stu-id="f031b-108">Enumerating members can be inefficient when the number of values in a multi-valued attribute becomes large.</span></span> <span data-ttu-id="f031b-109">Der Server schränkt außerdem die maximale Anzahl der Werte ein, die in einer einzelnen Abfrage abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="f031b-109">The server will also limit the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="f031b-110">Dies bedeutet, dass eine Gruppe, die möglicherweise mehr Mitglieder hat, als vom Server bereitgestellt werden kann, nur das inkrementelle Abrufen von Daten verwendet, die als *Bereichs Abruf* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f031b-110">This means that if a group may have more members than can be supplied by the server, the only way to enumerate all members is to use incremental retrieval of data, known as *range retrieval*.</span></span>

<span data-ttu-id="f031b-111">Der Bereichs Abruf umfasst das Anfordern einer begrenzten Anzahl von Attributwerten in einer einzelnen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f031b-111">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="f031b-112">Die Anzahl der angeforderten Werte muss kleiner oder gleich der maximalen Anzahl von Werten sein, die vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f031b-112">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="f031b-113">Um die Häufigkeit zu verringern, mit der die Abfrage den Server kontaktieren muss, sollte die Anzahl der angeforderten Werte so nah wie möglich auf diesen Höchstwert liegen.</span><span class="sxs-lookup"><span data-stu-id="f031b-113">To reduce the number of times the query must contact the server, the number of values requested should be as close, as possible, to this maximum.</span></span> <span data-ttu-id="f031b-114">Damit eine Anwendung ordnungsgemäß mit allen Servern funktioniert, sollte eine maximale Anzahl von 1000 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f031b-114">To enable an application to work correctly with all servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="f031b-115">Die Version des Servers, der die angeforderten Daten bereitstellt, bestimmt die maximale Anzahl von Werten, die in einer einzelnen Abfrage abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="f031b-115">The version of the server that supplies the requested data determines the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="f031b-116">In der folgenden Tabelle werden die Server Version und die maximale Anzahl von Werten aufgelistet, die in einer einzelnen Abfrage abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="f031b-116">The following table lists the server version and the maximum number of values that can be retrieved in a single query.</span></span>



| <span data-ttu-id="f031b-117">Server-Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="f031b-117">Server operating system version</span></span> | <span data-ttu-id="f031b-118">Maximal abgerufene Werte</span><span class="sxs-lookup"><span data-stu-id="f031b-118">Maximum values retrieved</span></span> |
|---------------------------------|--------------------------|
| <span data-ttu-id="f031b-119">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f031b-119">Windows 2000</span></span>                    | <span data-ttu-id="f031b-120">1000</span><span class="sxs-lookup"><span data-stu-id="f031b-120">1000</span></span>                     |
| <span data-ttu-id="f031b-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f031b-121">Windows Server 2003</span></span>             | <span data-ttu-id="f031b-122">1500</span><span class="sxs-lookup"><span data-stu-id="f031b-122">1500</span></span>                     |



 

<span data-ttu-id="f031b-123">Weitere Informationen zum Abrufen von Bereichen mit Attributwerten mit ADSI finden Sie unter [Attribut Bereichs Abruf](/windows/desktop/ADSI/attribute-range-retrieval).</span><span class="sxs-lookup"><span data-stu-id="f031b-123">For more information about retrieving ranges of attribute values with ADSI, see [Attribute Range Retrieval](/windows/desktop/ADSI/attribute-range-retrieval).</span></span>

<span data-ttu-id="f031b-124">Weitere Informationen zum Abrufen von Bereichen mit Attributwerten mit [System. DirectoryServices](/dotnet/api/system.directoryservices)finden Sie unter Auflisten von Membern [in einer großen Gruppe](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="f031b-124">For more information about retrieving ranges of attribute values with [System.DirectoryServices](/dotnet/api/system.directoryservices), see [Enumerating Members in a Large Group](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span></span>

 

 