---
description: Die \_ SummaryInformation-Tabelle ist eine spezielle Tabelle, die mit dem Zusammenfassungsinformationsdatenstrom verwendet wird. Sie können den Zusammenfassungsinformationsdatenstrom einer Windows Installer-Datenbank abrufen oder festlegen, indem Sie eine Textarchivdatei mit dem Namen \_ SummaryInformation.idt exportieren oder importieren.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3824ceb9b3ad12338d84dfeea016a3c7e4404c274543cc691dc6ea0fb121bd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805736"
---
# <a name="_summaryinformation"></a>\_SummaryInformation

Die \_ SummaryInformation-Tabelle ist eine spezielle Tabelle, die mit dem [Zusammenfassungsinformationsdatenstrom](summary-information-stream.md)verwendet wird. Sie können den Zusammenfassungsinformationsdatenstrom einer Windows Installer-Datenbank abrufen oder festlegen, indem Sie eine [Textarchivdatei](text-archive-files.md) namens \_ SummaryInformation.idt exportieren oder importieren.

Die IDT-Datei einer exportierten \_ SummaryInformation-Tabelle hat das folgende Format.

-   Die erste Zeile enthält die Tabellenspaltennamen, die durch Registerkarten getrennt sind: PropertyId und Value. Eine Liste der Eigenschaften und deren IDs (PID) finden Sie im Thema [Stream-Eigenschaftensatz](summary-information-stream-property-set.md) mit Zusammenfassungsinformationen.
-   Die zweite Zeile enthält die Spaltendefinitionen, die durch Registerkarten getrennt sind. Die Spaltendefinitionen werden auf die gleiche Weise wie im grundlegenden [IDT-Archivdateiformat](archive-file-format.md)angegeben. Die PropertyId-Spalte kann eine kurze ganze Zahl sein, die keine NULL-Werte zugibt. Die Value-Spalte kann eine lokalisierbare Zeichenfolge ohne NULL-Werte sein, die 255 Zeichen lang ist.
-   Die dritte Zeile ist der Tabellenname und der Name der Primärschlüsselspalte durch Registerkarten getrennt: \_ SummaryInformation und PropertyId.
-   Die verbleibenden Zeilen in der Datei stellen die PID und den zugeordneten Wert dar, getrennt durch Registerkarten. Datum und Uhrzeit in \_ SummaryInformation haben das folgende Format: YYYY/MM/DD hh::mm::ss. Beispiel: 1999/03/22 15:25:45.

Im Folgenden finden Sie ein Beispiel für den [Zusammenfassungsinformationsdatenstrom](summary-information-stream.md) einer Datenbank im IDT-Format.

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

Wenn Sie [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) oder die [Import-Methode](database-import.md) des [**Datenbankobjekts**](database-object.md) verwenden, um eine Textarchivtabelle mit dem Namen \_ SummaryInformation in eine Installerdatenbank zu importieren, schreiben Sie den Stream "05SummaryInformation" in die Datenbank.

 

 



