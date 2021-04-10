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
# <a name="retrieving-class-definitions"></a>Abrufen von Klassendefinitionen

Schema Abfragen sind WQL-Anweisungen, die Klassendefinitionen und Informationen zu [Schema Zuordnungen](schema-associations.md)anfordern. Klassen Anbieter verwenden Schema Abfragen in ihren Instanzen der [**\_ \_ classproviderregistration**](--classproviderregistration.md) -Klasse, um die Klassen anzugeben, die Sie unterstützen, wenn Sie sich bei WMI registrieren. Schema Abfragen werden in den Eigenschaften " **resultsetqueries**", " **referencedsetqueries**" und " **unsupportedqueries** " der **\_ \_ classproviderregistration** -Instanz abgelegt.

Schema Abfragen ähneln Daten Abfragen darin, dass Sie die folgenden WQL-Anweisungen unterstützen:

-   [SELECT](select-statement-for-schema-queries.md)
-   [assoziatoren von](schema-associations.md)
-   [Verweise auf](schema-associations.md)
-   [ISA](isa-operator-for-schema-queries.md)

Eine Schema Abfrage ähnelt einem [Verweis](references-of-statement.md) auf die Datenabfrage, die das **classdefsonly** -Schlüsselwort angibt. Das heißt, dass ein Resultset von Klassen Definitions Objekten anstelle tatsächlicher Instanzen von Assoziations Klassen zurückgibt. Allerdings gibt Verweise von nur Klassendefinitionen zurück, wenn Instanzen vorhanden sind. Eine Schema Abfrage gibt Klassendefinitionen zurück, unabhängig davon, ob Instanzen vorhanden sind oder nicht.

 

 



