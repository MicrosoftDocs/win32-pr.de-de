---
title: Zähler, Abfragen und prädikations
description: Stream Output-und UAV-Leistungsindikatoren werden in Direct3D 12 in einer ähnlichen Methode wie Direct3D 11 verwendet, obwohl der Arbeitsspeicher für die Leistungsindikatoren nun von der APP zugeordnet werden muss.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548738"
---
# <a name="counters-queries-and-predication"></a><span data-ttu-id="c2826-103">Zähler, Abfragen und prädikations</span><span class="sxs-lookup"><span data-stu-id="c2826-103">Counters, queries, and predication</span></span>

<span data-ttu-id="c2826-104">In diesem Thema werden Datenstrom Ausgabe-Leistungsindikatoren, UAV-Leistungsindikatoren, Abfragen und das Prädikat behandelt.</span><span class="sxs-lookup"><span data-stu-id="c2826-104">This topic covers stream-output counters, UAV counters, queries, and predication.</span></span>

<span data-ttu-id="c2826-105">Stream Output-und UAV-Leistungsindikatoren werden in Direct3D 12 in einer ähnlichen Methode wie Direct3D 11 verwendet, obwohl der Arbeitsspeicher für die Leistungsindikatoren nun von der APP zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c2826-105">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="c2826-106">Abfragen in Direct3D 12 unterscheiden sich eher von denen in Direct3D 11, mit dem Hinzufügen von Zäunen und anderen Prozessen, die die Notwendigkeit einiger Abfrage Typen entfernen.</span><span class="sxs-lookup"><span data-stu-id="c2826-106">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c2826-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c2826-107">In this section</span></span>



| <span data-ttu-id="c2826-108">Thema</span><span class="sxs-lookup"><span data-stu-id="c2826-108">Topic</span></span>                                                           | <span data-ttu-id="c2826-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2826-109">Description</span></span>                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2826-110">Stream-ausgabezähler</span><span class="sxs-lookup"><span data-stu-id="c2826-110">Stream Output Counters</span></span>](stream-output-counters.md)<br/> | <span data-ttu-id="c2826-111">Die Streamausgabe ist die Fähigkeit der GPU, Vertices in einen Puffer zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c2826-111">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="c2826-112">Der Status der Datenstrom-ausgabezähler Monitor.</span><span class="sxs-lookup"><span data-stu-id="c2826-112">The stream output counters monitor progress.</span></span><br/>                                                               |
| [<span data-ttu-id="c2826-113">UAV-Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="c2826-113">UAV Counters</span></span>](uav-counters.md)<br/>                     | <span data-ttu-id="c2826-114">UAV-Leistungsindikatoren können verwendet werden, um einen atomaren 32-Bit-Zähler mit einer nicht geordneten Zugriffs Ansicht (UAV) zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c2826-114">UAV counters can be used to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span><br/>                                                                                |
| [<span data-ttu-id="c2826-115">Abfragen</span><span class="sxs-lookup"><span data-stu-id="c2826-115">Queries</span></span>](queries.md)<br/>                               | <span data-ttu-id="c2826-116">In Direct3D 12 werden Abfragen in Arrays von Abfragen gruppiert, die als Abfrage Heap bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="c2826-116">In Direct3D 12, queries are grouped into arrays of queries called a query heap.</span></span> <span data-ttu-id="c2826-117">Ein Abfrage Heap weist einen Typ auf, der die gültigen Abfrage Typen definiert, die mit diesem Heap verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c2826-117">A query heap has a type which defines the valid types of queries that can be used with that heap.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c2826-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c2826-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2826-119">Leistungsmessung</span><span class="sxs-lookup"><span data-stu-id="c2826-119">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>

 

 





