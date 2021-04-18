---
description: Die \_ Tabelle SummaryInformation ist eine spezielle Tabelle, die zusammen mit dem Zusammenfassungs Informationsdaten Strom verwendet wird. Sie können den Zusammenfassungs Informationsdaten Strom einer Windows Installer Datenbank durch Exportieren oder Importieren einer Textarchiv Datei mit dem Namen " \_ SummaryInformation. IDT" erhalten oder festlegen.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368709"
---
# <a name="_summaryinformation"></a>\_SummaryInformation

Die \_ Tabelle SummaryInformation ist eine spezielle Tabelle, die zusammen mit dem [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md)verwendet wird. Sie können den Zusammenfassungs Informationsdaten Strom einer Windows Installer Datenbank durch Exportieren oder Importieren einer [Textarchiv Datei](text-archive-files.md) mit dem Namen " \_ SummaryInformation. IDT" erhalten oder festlegen.

Die IDT-Datei einer exportierten \_ SummaryInformation-Tabelle weist das folgende Format auf.

-   Die erste Zeile enthält die durch Tabstopps getrennten Tabellen Spaltennamen: PropertyId und Value. Eine Liste der Eigenschaften und deren IDs (PID) finden Sie im Abschnitt " [zusammenfassende Informationsstrom](summary-information-stream-property-set.md) -Eigenschaften Satz".
-   Die zweite Zeile enthält die Spaltendefinitionen, die durch Registerkarten getrennt sind. Die Spaltendefinitionen werden auf die gleiche Weise wie im grundlegenden IDT- [Archivdatei Format](archive-file-format.md)angegeben. Die PropertyId-Spalte kann eine kurze Ganzzahl sein, die keine NULL-Werte zulässt. Die Value-Spalte kann eine lokalisierbare Zeichenfolge von 255 Zeichen sein, die keine NULL-Werte zulässt.
-   Die dritte Zeile ist der Tabellenname und der Name der Primärschlüssel Spalte, die durch Registerkarten getrennt sind: \_ SummaryInformation und PropertyId.
-   Die verbleibenden Zeilen in der Datei stellen die PID und den zugeordneten Wert dar, getrennt durch Registerkarten. Datum und Uhrzeit in \_ SummaryInformation weisen folgendes Format auf: yyyy/mm/dd hh:: mm:: SS. Beispiel: 1999/03/22 15:25:45.

Im folgenden finden Sie ein Beispiel für den [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) einer Datenbank im IDT-Format.

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

Wenn Sie [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) oder die [Import](database-import.md) -Methode des [**Database**](database-object.md) -Objekts verwenden, um eine Textarchiv Tabelle mit dem Namen \_ "SummaryInformation" in eine Installerdatenbank zu importieren, schreiben Sie den Datenstrom "05summaryinformation" in die Datenbank.

 

 



