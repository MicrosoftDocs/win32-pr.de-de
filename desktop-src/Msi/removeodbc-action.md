---
description: Die removeodbc-Aktion entfernt die Datenquellen, Konvertierer und Treiber, die während der Installation zum Entfernen aufgeführt sind.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Removeodbc-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349866"
---
# <a name="removeodbc-action"></a><span data-ttu-id="86218-103">Removeodbc-Aktion</span><span class="sxs-lookup"><span data-stu-id="86218-103">RemoveODBC Action</span></span>

<span data-ttu-id="86218-104">Die removeodbc-Aktion entfernt die Datenquellen, Konvertierer und Treiber, die während der Installation zum Entfernen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="86218-104">The RemoveODBC action removes the data sources, translators, and drivers listed for removal during the installation.</span></span> <span data-ttu-id="86218-105">Mit dieser Aktion werden die [ODBCDatasource-Tabelle](odbcdatasource-table.md), die [odbctranslator-Tabelle](odbctranslator-table.md)und die [odbcdriver-Tabelle](odbcdriver-table.md) für jede Datenquelle, jeden Konvertierer oder Treiber, der zum Entfernen geplant ist, abgefragt.</span><span class="sxs-lookup"><span data-stu-id="86218-105">This action queries the [ODBCDataSource table](odbcdatasource-table.md), [ODBCTranslator table](odbctranslator-table.md), and [ODBCDriver table](odbcdriver-table.md) for each data source, translator, or driver scheduled for removal.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="86218-106">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="86218-106">Sequence Restrictions</span></span>

<span data-ttu-id="86218-107">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="86218-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="86218-108">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="86218-108">ActionData Messages</span></span>

<span data-ttu-id="86218-109">Für jeden installierten Treiber.</span><span class="sxs-lookup"><span data-stu-id="86218-109">For each driver installed.</span></span>



| <span data-ttu-id="86218-110">Feld</span><span class="sxs-lookup"><span data-stu-id="86218-110">Field</span></span> | <span data-ttu-id="86218-111">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="86218-111">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="86218-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="86218-112">\[1\]</span></span> | <span data-ttu-id="86218-113">Treiber Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="86218-113">Driver description.</span></span> <span data-ttu-id="86218-114">Der Schlüssel des ODBC-Treibers.</span><span class="sxs-lookup"><span data-stu-id="86218-114">The ODBC driver key.</span></span> |
| <span data-ttu-id="86218-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="86218-115">\[2\]</span></span> | <span data-ttu-id="86218-116">ComponentID</span><span class="sxs-lookup"><span data-stu-id="86218-116">ComponentId</span></span>                              |



 

<span data-ttu-id="86218-117">Für jeden installierten Konvertierer.</span><span class="sxs-lookup"><span data-stu-id="86218-117">For each translator installed.</span></span>



| <span data-ttu-id="86218-118">Feld</span><span class="sxs-lookup"><span data-stu-id="86218-118">Field</span></span> | <span data-ttu-id="86218-119">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="86218-119">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="86218-120">\[1\]</span><span class="sxs-lookup"><span data-stu-id="86218-120">\[1\]</span></span> | <span data-ttu-id="86218-121">Treiber Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="86218-121">Driver description.</span></span> <span data-ttu-id="86218-122">Der Schlüssel des ODBC-Treibers.</span><span class="sxs-lookup"><span data-stu-id="86218-122">The ODBC driver key.</span></span> |
| <span data-ttu-id="86218-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="86218-123">\[2\]</span></span> | <span data-ttu-id="86218-124">ComponentID</span><span class="sxs-lookup"><span data-stu-id="86218-124">ComponentId</span></span>                              |



 

<span data-ttu-id="86218-125">Für jede installierte Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="86218-125">For each data source installed.</span></span>



| <span data-ttu-id="86218-126">Feld</span><span class="sxs-lookup"><span data-stu-id="86218-126">Field</span></span> | <span data-ttu-id="86218-127">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="86218-127">Description of action data</span></span>                              |
|-------|---------------------------------------------------------|
| <span data-ttu-id="86218-128">\[1\]</span><span class="sxs-lookup"><span data-stu-id="86218-128">\[1\]</span></span> | <span data-ttu-id="86218-129">Treiber Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="86218-129">Driver description.</span></span> <span data-ttu-id="86218-130">Der Schlüssel des ODBC-Treibers.</span><span class="sxs-lookup"><span data-stu-id="86218-130">The ODBC driver key.</span></span>                |
| <span data-ttu-id="86218-131">\[2\]</span><span class="sxs-lookup"><span data-stu-id="86218-131">\[2\]</span></span> | <span data-ttu-id="86218-132">ComponentID</span><span class="sxs-lookup"><span data-stu-id="86218-132">ComponentId</span></span>                                             |
| <span data-ttu-id="86218-133">\[3\]</span><span class="sxs-lookup"><span data-stu-id="86218-133">\[3\]</span></span> | <span data-ttu-id="86218-134">Registrierung: SQL \_ Remove \_ DSN oder SQL \_ Remove \_ sys \_ DSN</span><span class="sxs-lookup"><span data-stu-id="86218-134">Registration: SQL\_REMOVE\_DSN or SQL\_REMOVE\_SYS\_DSN</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="86218-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86218-135">Remarks</span></span>

<span data-ttu-id="86218-136">Wenn sowohl die ODBC-Verwendungs Anzahl als auch die Datei Verwendungs Anzahl 0 (null) betragen, wird die Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="86218-136">If both the ODBC usage count and the file usage count become zero, the file is removed.</span></span> <span data-ttu-id="86218-137">Die Registrierung ist abhängig von der Verwendung von ODBC-Verwendungs Anzahlen, und das Entfernen von Dateien basiert auf freigegebenen DLLs-Schlüssel Verweis</span><span class="sxs-lookup"><span data-stu-id="86218-137">Registration is dependent on ODBC usage counts and file removal is based on shared DLLs key reference counts.</span></span>

 

 



