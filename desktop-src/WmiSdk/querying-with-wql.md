---
description: Der WMI Query Language (WQL) ist eine Teilmenge der Standard American National Standards Institute Structured Query Language (ANSI SQL) mit geringfügigen Semantik Änderungen, um WMI zu unterstützen.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Abfragen mit WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347071"
---
# <a name="querying-with-wql"></a><span data-ttu-id="7f3cf-103">Abfragen mit WQL</span><span class="sxs-lookup"><span data-stu-id="7f3cf-103">Querying with WQL</span></span>

<span data-ttu-id="7f3cf-104">Der WMI Query Language (WQL) ist eine Teilmenge der Standard American National Standards Institute Structured Query Language (ANSI SQL) mit geringfügigen Semantik Änderungen, um WMI zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-104">The WMI Query Language (WQL) is a subset of standard American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes to support WMI.</span></span>

<span data-ttu-id="7f3cf-105">Eine umfassende Liste der unterstützten WQL-Schlüsselwörter finden Sie unter [WQL (SQL für WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="7f3cf-105">For a complete list of supported WQL keywords, see [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span> <span data-ttu-id="7f3cf-106">Durch die Verwendung von SQL-Schlüsselwörtern für Objekt-oder Eigenschaftsnamen kann eine Abfrage möglicherweise nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-106">Using SQL keywords for object or property names may restrict a query from being parsed.</span></span> <span data-ttu-id="7f3cf-107">Die folgenden SQL-Schlüsselwörter sind eingeschränkt: **null**, **true** und **false**.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-107">The following SQL keywords are restricted: **NULL**, **TRUE**, and **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="7f3cf-108">Es gibt Einschränkungen für die Anzahl von-und-oder-Schlüsselwörtern, die in WQL-Abfragen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-108">There are limits to the number of AND and OR keywords that can be used in WQL queries.</span></span> <span data-ttu-id="7f3cf-109">Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann bewirken, dass WMI den Fehlercode der **WBEM \_ E- \_ Kontingent \_ Verletzung** als **HRESULT** -Wert zurückgibt</span><span class="sxs-lookup"><span data-stu-id="7f3cf-109">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="7f3cf-110">Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-110">The limit of WQL keywords depends on how complex the query is.</span></span>

 

<span data-ttu-id="7f3cf-111">Abfragen können die **Where** -Klausel für Erweiterung und Anpassung verwenden, obwohl Sie nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-111">Queries can use the **WHERE** clause for extension and customization, although it is not required.</span></span> <span data-ttu-id="7f3cf-112">Die **Where** -Klausel besteht aus einer Eigenschaft oder einem Schlüsselwort, einem Operator und einer Konstante.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-112">The **WHERE** clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="7f3cf-113">Alle **Where** -Klauseln müssen einen der vordefinierten Operatoren angeben, die in WQL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-113">All **WHERE** clauses must specify one of the predefined operators that are included in WQL.</span></span> <span data-ttu-id="7f3cf-114">Weitere Informationen zur Syntax finden Sie unter [WHERE-Klausel](where-clause.md).</span><span class="sxs-lookup"><span data-stu-id="7f3cf-114">For more information about syntax, see [WHERE Clause](where-clause.md).</span></span> <span data-ttu-id="7f3cf-115">Weitere Informationen zu gültigen WQL-Operatoren finden Sie unter [WQL-Operatoren](wql-operators.md).</span><span class="sxs-lookup"><span data-stu-id="7f3cf-115">For more information about valid WQL operators, see [WQL Operators](wql-operators.md).</span></span>

<span data-ttu-id="7f3cf-116">Wie bei anderen SQL-Abfrage Zeichenfolgen können Sie Ihre Abfragen mit Escapezeichen versehen.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-116">As with other SQL query strings, you can escape your queries.</span></span>

> [!Note]  
> <span data-ttu-id="7f3cf-117">WQL unterstützt keine Namespace übergreifende Abfragen oder Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-117">WQL does not support cross-namespace queries or associations.</span></span> <span data-ttu-id="7f3cf-118">Es ist nicht möglich, alle Instanzen einer bestimmten Klasse abzufragen, die sich in allen Namespaces auf dem Bereitstellungs Zielcomputer befinden.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-118">You cannot query for all instances of a specified class residing in all of the namespaces on the target computer.</span></span>

 

<span data-ttu-id="7f3cf-119">WQL unterstützt die folgenden Typen von Abfragen:</span><span class="sxs-lookup"><span data-stu-id="7f3cf-119">WQL supports the following types of queries:</span></span>

-   <span data-ttu-id="7f3cf-120">Daten Abfragen</span><span class="sxs-lookup"><span data-stu-id="7f3cf-120">Data queries</span></span>

    <span data-ttu-id="7f3cf-121">Daten Abfragen werden verwendet, um Klassen Instanzen und Daten Zuordnungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-121">Data queries are used to retrieve class instances and data associations.</span></span> <span data-ttu-id="7f3cf-122">Dabei handelt es sich um den am häufigsten verwendeten Abfragetyp in WMI-Skripts und-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-122">They are the most commonly used type of query in WMI scripts and applications.</span></span> <span data-ttu-id="7f3cf-123">Weitere Informationen zur Syntax von Daten Abfragen finden Sie unter [anfordern von klasseninstanzdaten](requesting-class-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="7f3cf-123">For more information about the syntax of data queries, see [Requesting Class Instance Data](requesting-class-instance-data.md).</span></span> <span data-ttu-id="7f3cf-124">Weitere Informationen zu Zuordnungen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="7f3cf-124">For more information about associations, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="7f3cf-125">WQL unterstützt keine Abfragen von Array Datatypes.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-125">WQL does not support queries of array datatypes.</span></span>

     

    <span data-ttu-id="7f3cf-126">Im folgenden Beispiel für eine Datenabfrage wird die Ereignisprotokoll Datei "Application" aus allen Instanzen von [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)angefordert.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-126">The following data query example requests the event log file named "Application" from all instances of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   <span data-ttu-id="7f3cf-127">Ereignis Abfragen</span><span class="sxs-lookup"><span data-stu-id="7f3cf-127">Event queries</span></span>

    <span data-ttu-id="7f3cf-128">Consumer verwenden Ereignis Abfragen, um sich für den Empfang von Benachrichtigungen über Ereignisse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-128">Consumers use event queries to register to receive notification of events.</span></span> <span data-ttu-id="7f3cf-129">Ereignis Anbieter verwenden Ereignis Abfragen zur Registrierung, um ein oder mehrere Ereignisse zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-129">Event providers use event queries to register to support one or more events.</span></span> <span data-ttu-id="7f3cf-130">Weitere Informationen zu Ereignis Abfragen finden Sie unter [empfangen von Ereignis Benachrichtigungen](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7f3cf-130">For more information about event queries, see [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

    <span data-ttu-id="7f3cf-131">Die folgende Beispiel Ereignis Abfrage durch einen temporären Ereignisconsumer fordert eine Benachrichtigung an, wenn eine neue Instanz einer Klasse erstellt wird, die von [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-131">The following example event query by a temporary event consumer requests notification when a new instance of a class derived from [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) is created.</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   <span data-ttu-id="7f3cf-132">Schema Abfragen</span><span class="sxs-lookup"><span data-stu-id="7f3cf-132">Schema queries</span></span>

    <span data-ttu-id="7f3cf-133">Schema Abfragen werden verwendet, um Klassendefinitionen (anstelle von Klassen Instanzen) und Schema Zuordnungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-133">Schema queries are used to retrieve class definitions (rather than class instances) and schema associations.</span></span> <span data-ttu-id="7f3cf-134">Klassen Anbieter verwenden Schema Abfragen, um die Klassen anzugeben, die Sie bei der Registrierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-134">Class providers use schema queries to specify the classes that they support when they register.</span></span> <span data-ttu-id="7f3cf-135">Weitere Informationen zu Schema Abfragen finden Sie unter [Abrufen von Klassendefinitionen](retrieving-class-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="7f3cf-135">For more information about schema queries, see [Retrieving Class Definitions](retrieving-class-definitions.md).</span></span>

    <span data-ttu-id="7f3cf-136">Die folgende Beispiel Schema Abfrage zeigt die spezielle Syntax.</span><span class="sxs-lookup"><span data-stu-id="7f3cf-136">The following example schema query shows the special syntax.</span></span>

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="7f3cf-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f3cf-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f3cf-138">WMI-Format für Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="7f3cf-138">WMI Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 
