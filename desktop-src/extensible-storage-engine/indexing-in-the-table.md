---
description: 'Weitere Informationen: Indizierung in der Tabelle'
title: Indizierung in der Tabelle
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041855"
---
# <a name="indexing-in-the-table"></a><span data-ttu-id="1df06-103">Indizierung in der Tabelle</span><span class="sxs-lookup"><span data-stu-id="1df06-103">Indexing in the Table</span></span>


<span data-ttu-id="1df06-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1df06-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="indexing-in-the-table"></a><span data-ttu-id="1df06-105">Indizierung in der Tabelle</span><span class="sxs-lookup"><span data-stu-id="1df06-105">Indexing in the Table</span></span>

<span data-ttu-id="1df06-106">Ein Index ist ein Satz von Schlüssel Spalten, die eine persistente Reihenfolge von Datensätzen in einer Tabelle definieren.</span><span class="sxs-lookup"><span data-stu-id="1df06-106">An index is a set of key columns that define a persistent ordering of records in a table.</span></span> <span data-ttu-id="1df06-107">Datensätze sind Indexeinträge im primären Index.</span><span class="sxs-lookup"><span data-stu-id="1df06-107">Records are index entries in the primary index.</span></span> <span data-ttu-id="1df06-108">Ein primärer Index und mehrere sekundäre Indizes können definiert werden, um unterschiedliche Datenreihen in der Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1df06-108">One primary index and multiple secondary indexes can be defined to create different orders of data in the table.</span></span>

<span data-ttu-id="1df06-109">Obwohl mehrere Indizes definiert werden können, werden die Datensätze physisch in B +-Bäumen in der vom primären Index angegebenen Reihenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1df06-109">Although multiple indices can be defined, the records are physically stored in B+ trees in the order specified by the primary index.</span></span> <span data-ttu-id="1df06-110">Der primäre Index ist immer ein gruppierter Index und muss auch eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="1df06-110">The primary index is always a clustered index, and must also be unique.</span></span> <span data-ttu-id="1df06-111">Der primäre Index muss vor der ersten Tabellen Aktualisierung deklariert werden, um die Index Reihenfolge beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="1df06-111">The primary index must be declared before the first table update to preserve the index ordering.</span></span> <span data-ttu-id="1df06-112">Wenn kein primärer Index von der Anwendung definiert wird, werden die Daten in der Reihenfolge gespeichert, in der die Datensätze der Tabelle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1df06-112">When no primary index is defined by the application, the data is stored in the order in which records are added to the table.</span></span> <span data-ttu-id="1df06-113">Dieser spezielle Index wird als sequenzieller Index bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1df06-113">This special index is referred to as a sequential index.</span></span>

<span data-ttu-id="1df06-114">Separate B +-Strukturen werden verwendet, um Datensätze entsprechend dem sekundären Index zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="1df06-114">Separate B+ trees are used to order records according to the secondary index.</span></span> <span data-ttu-id="1df06-115">Index Einträge im sekundären Index enthalten Zeiger auf die Daten, die gemäß dem primären Index gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1df06-115">Index entries in the secondary index contain pointers to the data stored according to the primary index.</span></span> <span data-ttu-id="1df06-116">Die Indexeinträge für Datensätze im primären Index müssen eindeutig sein, da der sekundäre Index mit dem Primärschlüssel des Datensatzes auf den Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="1df06-116">The index entries for records in the primary index must be unique because the secondary index points to the record using the primary key of the record.</span></span> <span data-ttu-id="1df06-117">Sekundäre Indizes verfügen möglicherweise über eine Eindeutigkeits Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="1df06-117">Secondary indices may or may not have a uniqueness constraint.</span></span> <span data-ttu-id="1df06-118">Weitere Informationen finden Sie im Thema [Übersicht über die Datenbank](./database-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="1df06-118">For more information, see the [Database Overview](./database-overview.md) topic.</span></span>
