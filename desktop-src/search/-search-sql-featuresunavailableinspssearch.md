---
description: Die Microsoft Windows Search-Abfragesprache basiert auf Structured Query Language (SQL). Es wird jedoch nicht in einer relationalen Datenbank mit benutzerdefinierten Tabellen oder Indizes durchsucht.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: SQL-Funktionen sind in Microsoft Windows Search nicht verfügbar.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341188"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a><span data-ttu-id="0b1fe-103">SQL-Funktionen sind in Microsoft Windows Search nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0b1fe-103">SQL Features Unavailable in Microsoft Windows Search</span></span>

<span data-ttu-id="0b1fe-104">Die Microsoft Windows Search-Abfragesprache basiert auf Structured Query Language (SQL). Es wird jedoch nicht in einer relationalen Datenbank mit benutzerdefinierten Tabellen oder Indizes durchsucht.</span><span class="sxs-lookup"><span data-stu-id="0b1fe-104">Microsoft Windows Search query language is based on Structured Query Language (SQL); however, it does not search in a relational database with user-defined tables or indexes.</span></span> <span data-ttu-id="0b1fe-105">Aus diesem Grund sind viele Standard-SQL-Anweisungen und Syntax Funktionen nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="0b1fe-105">Because of this, many standard SQL statements and syntax features do not apply.</span></span> <span data-ttu-id="0b1fe-106">Im folgenden finden Sie eine Liste der signifikanteren SQL-Features, die in Windows Search nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0b1fe-106">The following is a list of the more significant SQL features that are not supported in Windows Search.</span></span>


-   <span data-ttu-id="0b1fe-107">Batch-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="0b1fe-107">BATCH statements</span></span>
-   <span data-ttu-id="0b1fe-108">COALESCE- \_ Tabellen Funktion</span><span class="sxs-lookup"><span data-stu-id="0b1fe-108">COALESCE\_TABLE function</span></span>
-   <span data-ttu-id="0b1fe-109">Convert-Funktion (verwenden Sie stattdessen die Cast Funktionen)</span><span class="sxs-lookup"><span data-stu-id="0b1fe-109">CONVERT function (use the CAST functions instead)</span></span>
-   <span data-ttu-id="0b1fe-110">CREATE VIEW-Anweisung</span><span class="sxs-lookup"><span data-stu-id="0b1fe-110">CREATE VIEW statement</span></span>
-   <span data-ttu-id="0b1fe-111">Datendefinitionssprache</span><span class="sxs-lookup"><span data-stu-id="0b1fe-111">Data definition language</span></span>
-   <span data-ttu-id="0b1fe-112">DataSource-Anweisung</span><span class="sxs-lookup"><span data-stu-id="0b1fe-112">DATASOURCE statement</span></span>
-   <span data-ttu-id="0b1fe-113">Datums-und Uhrzeit Formate außer ISO-Datums-und Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="0b1fe-113">Date and Time formats other than ISO date and time stamp</span></span>
-   <span data-ttu-id="0b1fe-114">DELETE-Anweisung</span><span class="sxs-lookup"><span data-stu-id="0b1fe-114">DELETE statement</span></span>
-   <span data-ttu-id="0b1fe-115">GRANT-Anweisung</span><span class="sxs-lookup"><span data-stu-id="0b1fe-115">GRANT statement</span></span>
-   <span data-ttu-id="0b1fe-116">Informations Schema</span><span class="sxs-lookup"><span data-stu-id="0b1fe-116">Information schema</span></span>
-   <span data-ttu-id="0b1fe-117">INSERT-Anweisung</span><span class="sxs-lookup"><span data-stu-id="0b1fe-117">INSERT statement</span></span>
-   <span data-ttu-id="0b1fe-118">Datentypen OLE DB</span><span class="sxs-lookup"><span data-stu-id="0b1fe-118">OLE DB data types</span></span>
-   <span data-ttu-id="0b1fe-119">Reguläre SQL-Standard Ausdrücke (verwenden Sie stattdessen "enthält" oder ähnliches)</span><span class="sxs-lookup"><span data-stu-id="0b1fe-119">SQL-standard regular expressions (use CONTAINS or LIKE instead)</span></span>
-   <span data-ttu-id="0b1fe-120">Parameter für SQL-Abfragen</span><span class="sxs-lookup"><span data-stu-id="0b1fe-120">Parameters to SQL queries</span></span>
-   <span data-ttu-id="0b1fe-121">Vergleich von relationalen Spalten</span><span class="sxs-lookup"><span data-stu-id="0b1fe-121">Relational column comparison</span></span>
-   <span data-ttu-id="0b1fe-122">Revision-ID-Header</span><span class="sxs-lookup"><span data-stu-id="0b1fe-122">Revision ID header</span></span>
-   <span data-ttu-id="0b1fe-123">REVOKE-Anweisung</span><span class="sxs-lookup"><span data-stu-id="0b1fe-123">REVOKE statement</span></span>
-   <span data-ttu-id="0b1fe-124">Bereichs Aliase oder Revisionsnummern</span><span class="sxs-lookup"><span data-stu-id="0b1fe-124">SCOPE aliases or revision numbers</span></span>
-   <span data-ttu-id="0b1fe-125">Alles auswählen (entfernt Duplikate automatisch)</span><span class="sxs-lookup"><span data-stu-id="0b1fe-125">SELECT ALL (removes duplicates automatically)</span></span>
-   <span data-ttu-id="0b1fe-126">Gespeicherte Prozeduren</span><span class="sxs-lookup"><span data-stu-id="0b1fe-126">Stored procedures</span></span>
-   <span data-ttu-id="0b1fe-127">Strukturierte Dokument Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0b1fe-127">Structured document expansion</span></span>
-   <span data-ttu-id="0b1fe-128">UNION ALL</span><span class="sxs-lookup"><span data-stu-id="0b1fe-128">UNION ALL</span></span>
-   <span data-ttu-id="0b1fe-129">Unbekanntes Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="0b1fe-129">UNKNOWN keyword</span></span>
-   <span data-ttu-id="0b1fe-130">UPDATE-Anweisung</span><span class="sxs-lookup"><span data-stu-id="0b1fe-130">UPDATE statement</span></span>

<span data-ttu-id="0b1fe-131">Windows Search unterstützt keine Thesaurus-und Füll Wörter.</span><span class="sxs-lookup"><span data-stu-id="0b1fe-131">Windows Search does not support Thesaurus and Noise Words.</span></span>

 

 



