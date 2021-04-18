---
description: Die Datenebene enthält häufig überwiegend statische Informationen&\# 8212; Informationen, die auf permanenten Medien beibehalten werden.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Optimieren von Aufrufen zwischen der com+-Geschäftslogik und den Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345434"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a><span data-ttu-id="cf0a3-103">Optimieren von Interaktionen zwischen der com+-Geschäftslogik Ebene und der Datenebene</span><span class="sxs-lookup"><span data-stu-id="cf0a3-103">Optimizing Interactions Between the COM+ Business Logic Tier and the Data Tier</span></span>

<span data-ttu-id="cf0a3-104">Die Datenebene enthält häufig überwiegend statische Informationen – Informationen, die auf permanenten Medien beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-104">The data tier often contains mostly static information—information persisted on durable media.</span></span> <span data-ttu-id="cf0a3-105">Da diese Ebene Informationen umfasst, die überwiegend statisch sind, ist eine gründliche Analyse von möglichen Engpässen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-105">Because this tier encompasses information that is mostly static, it requires a thorough analysis for potential bottlenecks.</span></span> <span data-ttu-id="cf0a3-106">Neben der offensichtlichen Möglichkeit von Verbindungs Engpässen können auch Hotspots durch häufig verwendete Datensätze, ineffiziente Datenzugriffs Methoden und die Notwendigkeit, den Zugriff auf Legacy Systeme zu koordinieren, verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-106">In addition to the obvious possibility for connection bottlenecks, hot spots can be caused by frequently accessed records, inefficient data access methods, and the need to coordinate access to legacy systems.</span></span>

## <a name="connecting-to-the-data-tier"></a><span data-ttu-id="cf0a3-107">Herstellen einer Verbindung mit der Datenebene</span><span class="sxs-lookup"><span data-stu-id="cf0a3-107">Connecting to the Data Tier</span></span>

<span data-ttu-id="cf0a3-108">Zwei Aspekte spielen eine wichtige Rolle beim Entwerfen einer Datenebene für eine COM+-Anwendung: Verbindungspooling und [com+-Just-in-time (JIT)-Aktivierung](com--just-in-time-activation.md)und die Verwendung von DSNs.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-108">Two considerations play an important role in designing a data tier for a COM+ application: connection pooling and [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md), and the use of DSNs.</span></span> <span data-ttu-id="cf0a3-109">Komponenten, die Verbindungen mit der Datenebene herstellen, sollten das [com+-Objekt Pooling](com--object-pooling.md) verwenden, das für die Komponente festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-109">Components that make connections to the data tier should use [COM+ object pooling](com--object-pooling.md) set on the component.</span></span>

<span data-ttu-id="cf0a3-110">Verwenden Sie beim Erstellen von DSNs für die Komponente angegebene objektkonstruktorzeichenfolgen, anstatt einen Datei-DSN zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-110">When creating DSNs, use object constructor strings specified on the component instead of creating a File DSN.</span></span> <span data-ttu-id="cf0a3-111">Datei-DSNs sind langsamer als eine Verbindung mithilfe einer Objektkonstruktorzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-111">File DSNs are slower than a connection using an object constructor string.</span></span> <span data-ttu-id="cf0a3-112">Objektkonstruktorzeichenfolgen können auf dem Eigenschaften Blatt der Komponente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-112">Object constructor strings can be specified on the component property sheet.</span></span> <span data-ttu-id="cf0a3-113">Weitere Informationen finden Sie unter [com+-objektkonstruktorzeichenfolgen](com--object-constructor-strings.md).</span><span class="sxs-lookup"><span data-stu-id="cf0a3-113">For more information, see [COM+ Object Constructor Strings](com--object-constructor-strings.md).</span></span>

<span data-ttu-id="cf0a3-114">Wenn Sie Komponenten verwenden, um auf eine SQL Server Datenbank zuzugreifen, verwenden Sie das COM+-Objekt Pooling anstelle von SQL-Verbindungspooling.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-114">If you are using components to access a SQL Server database, use COM+ object pooling instead of SQL connection pooling.</span></span>

<span data-ttu-id="cf0a3-115">Wenn die Komponente ADO zum Abrufen mehrerer Recordsets verwendet, richten Sie mehrere Verbindungen für die Komponente ein.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-115">If your component is using ADO to fetch multiple recordsets, establish multiple connections for the component.</span></span> <span data-ttu-id="cf0a3-116">Wenn ADO mehrere Recordsets abruft, werden mehrere Verbindungen im Hintergrund erstellt, wenn Sie nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-116">When ADO retrieves multiple recordsets, it creates multiple connections in the background if you do not create them.</span></span> <span data-ttu-id="cf0a3-117">Wenn Sie Sie erstellen, können Sie Sie in einem Pool zusammenführen und mehr Kontrolle über die Anzahl der verwendeten Verbindungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf0a3-117">If you create them, you can pool them and have more control over the number of the connections used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf0a3-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf0a3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf0a3-119">Optimieren von Interaktionen zwischen der com+-Geschäftslogik Ebene und der Präsentationsebene</span><span class="sxs-lookup"><span data-stu-id="cf0a3-119">Optimizing Interactions Between the COM+ Business Logic Tier and the Presentation Tier</span></span>](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



