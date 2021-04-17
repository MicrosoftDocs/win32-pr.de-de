---
description: Windows Search stellt Content-crawlen und Suchfunktionen bereit, die die Volltextsuche unterstützen. Die von Windows Search verwendete Abfragesprache erweitert die standardmäßige SQL-92-und SQL-99-Datenbankabfrage Syntax, um die Nützlichkeit durch textbasierte Suchvorgänge zu verbessern.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Abfragen des Indexes mit der SQL-Syntax von Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484411"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a><span data-ttu-id="0006d-104">Abfragen des Indexes mit der SQL-Syntax von Windows Search</span><span class="sxs-lookup"><span data-stu-id="0006d-104">Querying the Index with Windows Search SQL Syntax</span></span>

<span data-ttu-id="0006d-105">Windows Search stellt Content-crawlen und Suchfunktionen bereit, die die Volltextsuche unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0006d-105">Windows Search provides content crawling and search features that support full-text searching.</span></span> <span data-ttu-id="0006d-106">Die von Windows Search verwendete Abfragesprache erweitert die standardmäßige SQL-92-und SQL-99-Datenbankabfrage Syntax, um die Nützlichkeit durch textbasierte Suchvorgänge zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="0006d-106">The query language used by Windows Search extends the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span>

<span data-ttu-id="0006d-107">Alle Features von Windows Search Structured Query Language (SQL) sind mit Windows Search unter Windows Vista und höher kompatibel, einschließlich aller Versionen von Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0006d-107">All features of Windows Search Structured Query Language (SQL) are compatible with Windows Search on Windows Vista, and later, including all versions of Windows 10.</span></span>

<span data-ttu-id="0006d-108">Dieser Abschnitt enthält eine Übersicht über die SQL-Syntax in Windows Search und enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0006d-108">This section provides an overview of SQL syntax in Windows Search, and includes the following topics:</span></span>

- [<span data-ttu-id="0006d-109">Übersicht über die SQL-Syntax von Windows Search</span><span class="sxs-lookup"><span data-stu-id="0006d-109">Overview of Windows Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
- [<span data-ttu-id="0006d-110">Allgemeine Informationen zur Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="0006d-110">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)
- [<span data-ttu-id="0006d-111">Gruppieren nach... Über... An</span><span class="sxs-lookup"><span data-stu-id="0006d-111">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
- [<span data-ttu-id="0006d-112">SELECT-Anweisung</span><span class="sxs-lookup"><span data-stu-id="0006d-112">SELECT Statement</span></span>](-search-sql-select.md)
- [<span data-ttu-id="0006d-113">FROM-Klausel</span><span class="sxs-lookup"><span data-stu-id="0006d-113">FROM Clause</span></span>](-search-sql-from.md)
- [<span data-ttu-id="0006d-114">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="0006d-114">WHERE Clause</span></span>](-search-sql-where.md)
- [<span data-ttu-id="0006d-115">Order By-Klausel</span><span class="sxs-lookup"><span data-stu-id="0006d-115">ORDER BY Clause</span></span>](-search-sql-orderby.md)
- [<span data-ttu-id="0006d-116">Rank by-Klausel</span><span class="sxs-lookup"><span data-stu-id="0006d-116">RANK BY Clause</span></span>](-search-sql-rankby.md)
- [<span data-ttu-id="0006d-117">Set-Anweisung</span><span class="sxs-lookup"><span data-stu-id="0006d-117">SET Statement</span></span>](-search-sql-set.md)
- [<span data-ttu-id="0006d-118">Rowset-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0006d-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)

<span data-ttu-id="0006d-119">In dieser Dokumentation wird davon ausgegangen, dass Sie mit dem Objekt Verknüpfungs-und Einbetten von Datenbanken (OLE DB)</span><span class="sxs-lookup"><span data-stu-id="0006d-119">This documentation assumes familiarity with Object Linking and Embedding Database (OLE DB), and SQL.</span></span>

## <a name="code-samples"></a><span data-ttu-id="0006d-120">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="0006d-120">Code samples</span></span>

<span data-ttu-id="0006d-121">Das wssql-Codebeispiel veranschaulicht die Kommunikation zwischen Microsoft OLE DB und Windows Search über SQL.</span><span class="sxs-lookup"><span data-stu-id="0006d-121">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="0006d-122">Das wsoledb-Codebeispiel veranschaulicht Active Template Library (ATL)-OLE DB Zugriff auf Windows Search-Anwendungen und zwei zusätzliche Methoden zum Abrufen von Ergebnissen aus Windows Search.</span><span class="sxs-lookup"><span data-stu-id="0006d-122">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="0006d-123">Beide Beispiele sind in den [Windows-Such Beispielen](-search-samples-ovw.md) und im [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0006d-123">Both samples are available in the [Windows Search Samples](-search-samples-ovw.md) and the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0006d-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0006d-124">Related topics</span></span>

[<span data-ttu-id="0006d-125">Programm gesteuertes Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="0006d-125">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="0006d-126">Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="0006d-126">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="0006d-127">Abfragen des Indexes mit isearchqueryhelper</span><span class="sxs-lookup"><span data-stu-id="0006d-127">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)

[<span data-ttu-id="0006d-128">Abfragen des Indexes mit dem Search-MS-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0006d-128">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)

[<span data-ttu-id="0006d-129">Abfragen des Indexes mit der SQL-Syntax von Windows Search</span><span class="sxs-lookup"><span data-stu-id="0006d-129">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="0006d-130">Programm gesteuertes verwenden der erweiterten Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="0006d-130">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
