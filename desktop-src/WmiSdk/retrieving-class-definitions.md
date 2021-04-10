---
description: Schema Abfragen sind WQL-Anweisungen, die Klassendefinitionen und Informationen zu Schema Zuordnungen anfordern.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Abrufen von Klassendefinitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131012"
---
# <a name="retrieving-class-definitions"></a><span data-ttu-id="7cc69-103">Abrufen von Klassendefinitionen</span><span class="sxs-lookup"><span data-stu-id="7cc69-103">Retrieving Class Definitions</span></span>

<span data-ttu-id="7cc69-104">Schema Abfragen sind WQL-Anweisungen, die Klassendefinitionen und Informationen zu [Schema Zuordnungen](schema-associations.md)anfordern.</span><span class="sxs-lookup"><span data-stu-id="7cc69-104">Schema queries are WQL statements that request class definitions and information about [schema associations](schema-associations.md).</span></span> <span data-ttu-id="7cc69-105">Klassen Anbieter verwenden Schema Abfragen in ihren Instanzen der [**\_ \_ classproviderregistration**](--classproviderregistration.md) -Klasse, um die Klassen anzugeben, die Sie unterstützen, wenn Sie sich bei WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="7cc69-105">Class providers use schema queries in their instances of the [**\_\_ClassProviderRegistration**](--classproviderregistration.md) class to specify the classes that they support when they register with WMI.</span></span> <span data-ttu-id="7cc69-106">Schema Abfragen werden in den Eigenschaften " **resultsetqueries**", " **referencedsetqueries**" und " **unsupportedqueries** " der **\_ \_ classproviderregistration** -Instanz abgelegt.</span><span class="sxs-lookup"><span data-stu-id="7cc69-106">Schema queries are placed in the **ResultSetQueries**, **ReferencedSetQueries**, and **UnsupportedQueries** properties of the **\_\_ClassProviderRegistration** instance.</span></span>

<span data-ttu-id="7cc69-107">Schema Abfragen ähneln Daten Abfragen darin, dass Sie die folgenden WQL-Anweisungen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="7cc69-107">Schema queries are similar to data queries in that they support the following WQL statements:</span></span>

-   [<span data-ttu-id="7cc69-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="7cc69-108">SELECT</span></span>](select-statement-for-schema-queries.md)
-   [<span data-ttu-id="7cc69-109">assoziatoren von</span><span class="sxs-lookup"><span data-stu-id="7cc69-109">ASSOCIATORS OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="7cc69-110">Verweise auf</span><span class="sxs-lookup"><span data-stu-id="7cc69-110">REFERENCES OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="7cc69-111">ISA</span><span class="sxs-lookup"><span data-stu-id="7cc69-111">ISA</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="7cc69-112">Eine Schema Abfrage ähnelt einem [Verweis](references-of-statement.md) auf die Datenabfrage, die das **classdefsonly** -Schlüsselwort angibt. Das heißt, dass ein Resultset von Klassen Definitions Objekten anstelle tatsächlicher Instanzen von Assoziations Klassen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7cc69-112">A schema query is similar to a [REFERENCES OF](references-of-statement.md) data query that specifies the **ClassDefsOnly** keyword; in other words, that returns a result set of class definition objects rather than actual instances of association classes.</span></span> <span data-ttu-id="7cc69-113">Allerdings gibt Verweise von nur Klassendefinitionen zurück, wenn Instanzen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7cc69-113">However, REFERENCES OF returns class definitions only if there are instances present.</span></span> <span data-ttu-id="7cc69-114">Eine Schema Abfrage gibt Klassendefinitionen zurück, unabhängig davon, ob Instanzen vorhanden sind oder nicht.</span><span class="sxs-lookup"><span data-stu-id="7cc69-114">A schema query returns class definitions whether or not instances are present.</span></span>

 

 



