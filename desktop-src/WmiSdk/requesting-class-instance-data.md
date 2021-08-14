---
description: Datenabfragen sind WQL-Anweisungen, die Instanzen von Klassen anfordern. Zum Ausführen einer Datenabfrage rufen Anwendungen die IWbemServices::ExecQuery- oder IWbemServices::ExecQueryAsync-Methode auf.
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Anfordern von Klasseninstanzdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332ff8b5ba0aae7d1ac33fb8faba6340bbd795401fa81a52ea9c21abc4fde2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316287"
---
# <a name="requesting-class-instance-data"></a>Anfordern von Klasseninstanzdaten

Datenabfragen sind WQL-Anweisungen, die Instanzen von Klassen anfordern. Zum Ausführen einer Datenabfrage rufen Anwendungen die [**IWbemServices::ExecQuery-**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) oder [**IWbemServices::ExecQueryAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) auf.

Die folgenden Anweisungen werden verwendet, um Datenabfragen zu erstellen:

-   [SELECT](select-statement-for-data-queries.md)
-   [ASSOZIATOREN VON](associators-of-statement.md)
-   [VERWEISE VON](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

Die WQL SELECT-Anweisung ist die standardmäßige strukturierte Abfragesprache -Anweisung (SQL) zum Abrufen von Informationen mit einigen Einschränkungen und Erweiterungen speziell für WQL. Obwohl die SQL SELECT-Anweisung in der Regel in der Datenbankumgebung verwendet wird, um bestimmte Spalten aus Tabellen abzurufen, wird die WQL SELECT-Anweisung in WMI verwendet, um Instanzen einer einzelnen Klasse abzurufen. WQL unterstützt keine Abfragen über mehrere Klassen hinweg.

Die ASSOCIATORS OF- und REFERENCES OF-Anweisungen sind spezifisch für WQL und nicht Teil der Standard-SQL. Die ASSOCIATORS OF-Anweisung ruft alle Klasseninstanzen ab, die einer bestimmten Quellklasseninstanz zugeordnet sind, und REFERENCES OF ruft alle Instanzen ab, die auf eine bestimmte Quellinstanz verweisen. Zuordnungen werden durch Instanzen einer [Zuordnungsklasse dargestellt.](declaring-an-association-class.md)

 

 



