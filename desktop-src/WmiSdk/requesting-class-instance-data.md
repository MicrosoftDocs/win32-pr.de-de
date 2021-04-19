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
# <a name="requesting-class-instance-data"></a>Anfordern von klasseninstanzdaten

Daten Abfragen sind WQL-Anweisungen, die Instanzen von Klassen anfordern. Zum Ausgeben einer Datenabfrage wird die [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) -Methode oder die [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode aufgerufen.

Die folgenden Anweisungen werden verwendet, um Daten Abfragen durchführen zu können:

-   [SELECT](select-statement-for-data-queries.md)
-   [assoziatoren von](associators-of-statement.md)
-   [Verweise auf](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

Die WQL SELECT-Anweisung ist die Standard Structured Query Language (SQL)-Anweisung zum Abrufen von Informationen mit einigen Einschränkungen und Erweiterungen, die für WQL spezifisch sind. Obwohl die SQL-SELECT-Anweisung in der Regel in der Datenbankumgebung verwendet wird, um bestimmte Spalten aus Tabellen abzurufen, wird die WQL SELECT-Anweisung in WMI verwendet, um Instanzen einer einzelnen Klasse abzurufen. WQL unterstützt keine Abfragen über mehrere Klassen.

Die assoziatoren von und verweisen auf-Anweisungen sind für WQL spezifisch und nicht Bestandteil von SQL Standard. Die ASSOCIATORS of-Anweisung ruft alle Klassen Instanzen ab, die einer bestimmten Quell Klasseninstanz zugeordnet sind, und Verweise von Ruft alle-Instanzen ab, die auf eine bestimmte Quell Instanz verweisen. Zuordnungen werden durch Instanzen einer [Association-Klasse](declaring-an-association-class.md)dargestellt.

 

 



