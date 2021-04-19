---
description: Anwendungen können PDH zum Extrahieren von Leistungsindikatoren aus SQL-Protokollen verwenden, oder Sie können formatierte oder unformatierte Leistungsindikatoren direkt aus der Datenbank mithilfe von SQL-Abfragen extrahieren.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL-Protokolldatei Schema
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357752"
---
# <a name="sql-log-file-schema"></a><span data-ttu-id="2556a-103">SQL-Protokolldatei Schema</span><span class="sxs-lookup"><span data-stu-id="2556a-103">SQL Log File Schema</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2556a-104">PDH-Unterstützung für ODBC-SQL-Datenbanken kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="2556a-104">PDH support for ODBC SQL databases may be altered or unavailable in the future.</span></span>

<span data-ttu-id="2556a-105">Anwendungen können PDH-APIs für Lese-und Schreibvorgänge von Leistungsdaten in kompatiblen ODBC-SQL-Datenbanken verwenden und dann mithilfe von SQL-Abfragen weitere Verarbeitung ausführen.</span><span class="sxs-lookup"><span data-stu-id="2556a-105">Applications can use PDH APIs read and write performance counter data in compatible ODBC SQL databases and then perform further processing through SQL queries.</span></span> <span data-ttu-id="2556a-106">In diesem Abschnitt wird das SQL-Schema zum Speichern von Leistungsindikatoren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2556a-106">This section describes the SQL schema used to store performance counters.</span></span> <span data-ttu-id="2556a-107">Sie können diese Informationen zum Erstellen von benutzerdefinierten Ansichten und Berichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="2556a-107">You can use this information to create custom views and reports.</span></span> <span data-ttu-id="2556a-108">Das Schema besteht aus den folgenden drei Tabellen:</span><span class="sxs-lookup"><span data-stu-id="2556a-108">The schema consists of the following three tables:</span></span>

- [<span data-ttu-id="2556a-109">**Gegen Daten**</span><span class="sxs-lookup"><span data-stu-id="2556a-109">**CounterData**</span></span>](counterdata.md)
- [<span data-ttu-id="2556a-110">**Counter Details**</span><span class="sxs-lookup"><span data-stu-id="2556a-110">**CounterDetails**</span></span>](counterdetails.md)
- [<span data-ttu-id="2556a-111">**Display toid**</span><span class="sxs-lookup"><span data-stu-id="2556a-111">**DisplayToID**</span></span>](displaytoid.md)

> [!NOTE]
> <span data-ttu-id="2556a-112">PDH-Unterstützung für ODBC-SQL-Datenbanken funktioniert nur mit ODBC-SQL-Treibern, die [Massen Kopier Erweiterungen (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2556a-112">PDH support for ODBC SQL databases only works with ODBC SQL drivers that support [Bulk Copy (BCP) Extensions](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span></span>
