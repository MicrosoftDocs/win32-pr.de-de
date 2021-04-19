---
description: Eines der wichtigsten Tools von Windows-Verwaltungsinstrumentation (WMI) ist die Möglichkeit, das WMI-Repository nach Klassen-und Instanzinformationen abzufragen.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: WMI-Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354607"
---
# <a name="querying-wmi"></a><span data-ttu-id="f2474-103">WMI-Abfrage</span><span class="sxs-lookup"><span data-stu-id="f2474-103">Querying WMI</span></span>

<span data-ttu-id="f2474-104">Eines der wichtigsten Tools von Windows-Verwaltungsinstrumentation (WMI) ist die Möglichkeit, das WMI-Repository nach Klassen-und Instanzinformationen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="f2474-104">One of the main tools of Windows Management Instrumentation (WMI) is the ability to query the WMI repository for class and instance information.</span></span> <span data-ttu-id="f2474-105">Beispielsweise können Sie anfordern, dass WMI alle Objekte zurückgibt, die das Herunterfahren von Ereignissen des Desktop Systems darstellen.</span><span class="sxs-lookup"><span data-stu-id="f2474-105">For example, you can request that WMI return all the objects representing shut-down events from your desktop system.</span></span> <span data-ttu-id="f2474-106">Sie können auch Klassen-, Instanz-oder Schema Daten abrufen.</span><span class="sxs-lookup"><span data-stu-id="f2474-106">You can also retrieve class, instance, or schema data.</span></span> <span data-ttu-id="f2474-107">In der folgenden Tabelle sind die verschiedenen Typen von Abfragen aufgelistet, die Sie vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="f2474-107">The following table lists the different types of queries you can make.</span></span>



| <span data-ttu-id="f2474-108">Thema</span><span class="sxs-lookup"><span data-stu-id="f2474-108">Topic</span></span>                                                                | <span data-ttu-id="f2474-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2474-109">Description</span></span>                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2474-110">Aufrufen einer synchronen Abfrage</span><span class="sxs-lookup"><span data-stu-id="f2474-110">Invoking a Synchronous Query</span></span>](invoking-a-synchronous-query.md)     | <span data-ttu-id="f2474-111">Hier wird beschrieben, wie im gesamten Abfrageprozess eine Verknüpfung mit WMI beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="f2474-111">Describes how to maintain a link with WMI throughout the query process.</span></span> <span data-ttu-id="f2474-112">Synchrone Abfragen eignen sich gut für kleine Abfragen oder Abfragen an ein lokales System.</span><span class="sxs-lookup"><span data-stu-id="f2474-112">Synchronous queries are good for small queries or queries to a local system.</span></span><br/>                                  |
| [<span data-ttu-id="f2474-113">Aufrufen einer asynchronen Abfrage</span><span class="sxs-lookup"><span data-stu-id="f2474-113">Invoking an Asynchronous Query</span></span>](invoking-an-asynchronous-query.md) | <span data-ttu-id="f2474-114">Beschreibt das Einrichten eines separaten Prozesses zum Empfangen von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="f2474-114">Describes how to set up a separate process to receive queries.</span></span> <span data-ttu-id="f2474-115">Asynchrone Abfragen sind komplexer und bieten ein niedrigeres Maß an Sicherheit, verbessern jedoch im Allgemeinen die Systemleistung.</span><span class="sxs-lookup"><span data-stu-id="f2474-115">Asynchronous queries are more complex and provide a lower level of security, but generally improve system performance.</span></span><br/> |



 

<span data-ttu-id="f2474-116">Zusätzlich zum Abfragen des WMI-Repository können Sie auch den [*WMI Query Language (WQL)*](gloss-w.md) verwenden, um Benachrichtigungs Ereignisse an die Anwendung weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="f2474-116">In addition to querying the WMI repository, you can also use the [*WMI Query Language (WQL)*](gloss-w.md) to route notification events to your application.</span></span> <span data-ttu-id="f2474-117">Weitere Informationen finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="f2474-117">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

> [!Note]
>
> <span data-ttu-id="f2474-118">Zum ordnungsgemäßen Abfragen von WMI müssen Sie über ein gutes Verständnis der WQL verfügen.</span><span class="sxs-lookup"><span data-stu-id="f2474-118">To properly query WMI, you must have a good understanding of WQL.</span></span> <span data-ttu-id="f2474-119">Eine Abfrage, die falsch, zu komplex oder ungeeignet ist, kann dazu führen, dass der Abfrage Prozessor einen Fehler oder unerwartete Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f2474-119">A query that is incorrect, too complex, or inappropriate can cause the query processor to return an error or unexpected results.</span></span> <span data-ttu-id="f2474-120">Eine umfassende Anleitung zu WQL finden Sie unter [Querying with WQL (Abfragen mit WQL](querying-with-wql.md)).</span><span class="sxs-lookup"><span data-stu-id="f2474-120">For a comprehensive guide to WQL, see [Querying with WQL](querying-with-wql.md).</span></span>
>
> <span data-ttu-id="f2474-121">Es gibt Einschränkungen für die Anzahl von **-** und- **oder** -Schlüsselwörtern, die in WQL-Abfragen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f2474-121">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="f2474-122">Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann bewirken, dass WMI den Fehlercode der **WBEM \_ E- \_ Kontingent \_ Verletzung** als **HRESULT** -Wert zurückgibt</span><span class="sxs-lookup"><span data-stu-id="f2474-122">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="f2474-123">Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="f2474-123">The limit of WQL keywords depends on how complex the query is.</span></span>
>
> <span data-ttu-id="f2474-124">Beim Abfragen von Eigenschafts Werten mit einem **UInt64** -oder **sint64** -Datentyp in einer Skriptsprache wie VBScript gibt WMI Zeichen folgen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f2474-124">When querying for property values with a **uint64** or **sint64** data type in a scripting language like VBScript, WMI returns string values.</span></span> <span data-ttu-id="f2474-125">Beim Vergleichen dieser Werte können unerwartete Ergebnisse auftreten, da das Vergleichen von Zeichen folgen andere Ergebnisse als das Vergleichen von Zahlen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f2474-125">Unexpected results can occur when comparing these values, because comparing strings returns different results than comparing numbers.</span></span> <span data-ttu-id="f2474-126">Beispielsweise ist "10 Milliarden" kleiner als "9" beim Vergleichen von Zeichen folgen, und 9 ist kleiner als 10 Milliarden beim Vergleich von Zahlen.</span><span class="sxs-lookup"><span data-stu-id="f2474-126">For example, "10000000000" is less than "9" when comparing strings, and 9 is less than 10000000000 when comparing numbers.</span></span> <span data-ttu-id="f2474-127">Um Verwirrung zu vermeiden, sollten Sie die [CDbl](/previous-versions//ftekwwt0(v=vs.85)) -Methode in VBScript verwenden, wenn Eigenschaften vom Typ **UInt64** oder **sint64** aus WMI abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f2474-127">To avoid confusion you should use the [CDbl](/previous-versions//ftekwwt0(v=vs.85)) method in VBScript when properties of type **uint64** or **sint64** are retrieved from WMI.</span></span>

 

> [!Note]  

 

<span data-ttu-id="f2474-128">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="f2474-128">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

