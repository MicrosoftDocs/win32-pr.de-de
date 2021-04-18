---
description: 'Das folgende Beispiel zeigt die grundlegende Syntax der SELECT-Anweisung für eine lokale Abfrage:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: SELECT-Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344263"
---
# <a name="select-statement"></a>SELECT-Anweisung

Das folgende Beispiel zeigt die grundlegende Syntax der SELECT-Anweisung für eine lokale Abfrage:


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



Das folgende Beispiel zeigt den Spalten Teil der Syntax der SELECT-Anweisung:


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



Die Spalten Spezifizierer müssen gültige Eigenschaftsnamen Spalten sein, die durch Kommas getrennt sind. Gültige Spaltennamen sind registrierte Eigenschafts Beschreibungen oder werden durch das Eigenschafts System Schema der Shell definiert. Sie können nur die Spalten auswählen, die im Schema des Eigenschaften Systems als abrufbar gekennzeichnet sind. Wenn Sie gemischte Schreibweise verwenden, um Eigenschaften zu identifizieren, bei denen es sich nicht um System definierte Eigenschaften handelt, müssen Sie den Spaltenspezifizierer in doppelte Anführungszeichen einschließen. System definierte Eigenschaftsnamen enthalten alle Eigenschaften, die mit "System" beginnen (z. b. System. Contact. FirstName), und erfordern keine Anführungszeichen.

> [!Note]  
> Sie können für die Lesbarkeit auch System definierte Eigenschaftsnamen in doppelte Anführungszeichen einschließen. Dies hat keine Auswirkung auf die Kompatibilität.

 

Wenn die Abfrage ein Dokument zurückgibt, das nicht die angeforderte Spalte enthält, ist der Wert dieser Spalte für das Dokument **null**.

Sie müssen mindestens einen Spaltennamen in einer SELECT-Anweisung angeben. In der Structured Query Language (SQL)-Abfrage dürfen Sie das Sternchen () verwenden, \* um anzugeben, dass alle Spalten in einer Tabelle zurückgegeben werden sollen. Allerdings gelten für alle Dokumente keine definierten und festgelegten Eigenschaften. Aus diesem Grund ist das SQL-Sternchen im <columns> Spezifizierer der SELECT-Anweisung nicht zulässig.

## <a name="getting-the-top-n-results"></a>Erzielen der Top-n-Ergebnisse

Sie können mit der Top-Syntax eine maximale Anzahl von Ergebnissen angeben, die zurückgegeben werden sollen:


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Umwandeln von Spaltendatentypen

Manchmal müssen Sie Zeichen folgen Daten, die aus Dokumenten extrahiert werden, als einen anderen Datentyp umwandeln, damit ein entsprechender Vergleich erfolgen kann. Weitere Informationen finden Sie unter umwandeln [des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md).

## <a name="examples"></a>Beispiele

In den folgenden Beispielen werden der Name und die URL der übereinstimmenden Dokumente zurückgegeben.


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Umwandeln des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[System Eigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



