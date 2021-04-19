---
description: 'Daten Abfragen sind WQL-Anweisungen, die Instanzen von Klassen anfordern. Zum Ausgeben einer Datenabfrage wird die IWbemServices:: ExecQuery-Methode oder die IWbemServices:: ExecQueryAsync-Methode aufgerufen.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Anfordern von klasseninstanzdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32df053ae1267f396978d98271f57f174ea6bf0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353973"
---
# <a name="requesting-class-instance-data"></a><span data-ttu-id="f6129-104">Anfordern von klasseninstanzdaten</span><span class="sxs-lookup"><span data-stu-id="f6129-104">Requesting Class Instance Data</span></span>

<span data-ttu-id="f6129-105">Daten Abfragen sind WQL-Anweisungen, die Instanzen von Klassen anfordern.</span><span class="sxs-lookup"><span data-stu-id="f6129-105">Data queries are WQL statements that request instances of classes.</span></span> <span data-ttu-id="f6129-106">Zum Ausgeben einer Datenabfrage wird die [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) -Methode oder die [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f6129-106">To issue a data query, applications call the [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) or [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method.</span></span>

<span data-ttu-id="f6129-107">Die folgenden Anweisungen werden verwendet, um Daten Abfragen durchführen zu können:</span><span class="sxs-lookup"><span data-stu-id="f6129-107">The following statements are used to make data queries:</span></span>

-   [<span data-ttu-id="f6129-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="f6129-108">SELECT</span></span>](select-statement-for-data-queries.md)
-   [<span data-ttu-id="f6129-109">assoziatoren von</span><span class="sxs-lookup"><span data-stu-id="f6129-109">ASSOCIATORS OF</span></span>](associators-of-statement.md)
-   [<span data-ttu-id="f6129-110">Verweise auf</span><span class="sxs-lookup"><span data-stu-id="f6129-110">REFERENCES OF</span></span>](references-of-statement.md)
-   [<span data-ttu-id="f6129-111">ISA</span><span class="sxs-lookup"><span data-stu-id="f6129-111">ISA</span></span>](isa-operator-for-data-queries.md)

<span data-ttu-id="f6129-112">Die WQL SELECT-Anweisung ist die Standard Structured Query Language (SQL)-Anweisung zum Abrufen von Informationen mit einigen Einschränkungen und Erweiterungen, die für WQL spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f6129-112">The WQL SELECT statement is the standard Structured Query Language (SQL) statement for retrieving information, with a few restrictions and extensions specific to WQL.</span></span> <span data-ttu-id="f6129-113">Obwohl die SQL-SELECT-Anweisung in der Regel in der Datenbankumgebung verwendet wird, um bestimmte Spalten aus Tabellen abzurufen, wird die WQL SELECT-Anweisung in WMI verwendet, um Instanzen einer einzelnen Klasse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f6129-113">Although the SQL SELECT statement is typically used in the database environment to retrieve particular columns from tables, the WQL SELECT statement is used in WMI to retrieve instances of a single class.</span></span> <span data-ttu-id="f6129-114">WQL unterstützt keine Abfragen über mehrere Klassen.</span><span class="sxs-lookup"><span data-stu-id="f6129-114">WQL does not support queries across multiple classes.</span></span>

<span data-ttu-id="f6129-115">Die assoziatoren von und verweisen auf-Anweisungen sind für WQL spezifisch und nicht Bestandteil von SQL Standard.</span><span class="sxs-lookup"><span data-stu-id="f6129-115">The ASSOCIATORS OF and REFERENCES OF statements are specific to WQL and are not part of standard SQL.</span></span> <span data-ttu-id="f6129-116">Die ASSOCIATORS of-Anweisung ruft alle Klassen Instanzen ab, die einer bestimmten Quell Klasseninstanz zugeordnet sind, und Verweise von Ruft alle-Instanzen ab, die auf eine bestimmte Quell Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="f6129-116">The ASSOCIATORS OF statement retrieves all class instances that are associated with a particular source class instance, and REFERENCES OF retrieves all instances that refer to a particular source instance.</span></span> <span data-ttu-id="f6129-117">Zuordnungen werden durch Instanzen einer [Association-Klasse](declaring-an-association-class.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f6129-117">Associations are represented by instances of an [association class](declaring-an-association-class.md).</span></span>

 

 



