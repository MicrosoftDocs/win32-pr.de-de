---
description: 'Im Folgenden wird die grundlegende Syntax der SELECT-Anweisung für eine lokale Abfrage veranschaulicht:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: SELECT-Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3655f279a149017da841f296ad29c18518bc96
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883441"
---
# <a name="select-statement"></a>SELECT-Anweisung

Im Folgenden wird die grundlegende Syntax der SELECT-Anweisung für eine lokale Abfrage veranschaulicht:


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



Im Folgenden wird der Spaltenteil der SELECT-Anweisungssyntax veranschaulicht:


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



Die Spaltenspezifizierer müssen gültige Eigenschaftsnamenspalten sein, die durch Kommas getrennt sind. Gültige Spaltennamen sind registrierte Eigenschaftenbeschreibungen oder werden durch das Eigenschaftensystemschema der Shell definiert. Sie können nur die Spalten auswählen, die im Eigenschaftensystemschema als abrufbar gekennzeichnet sind. Wenn Sie eigenschaften, die keine systemdefinierten Eigenschaften sind, mit gemischter Case-Eigenschaft identifizieren, müssen Sie den Spaltenspezifizierer in doppelte Anführungszeichen setzen. Systemdefinierte Eigenschaftennamen enthalten alle Eigenschaften, die mit "System" beginnen (z. B. System.Contact.FirstName), und erfordern keine Anführungszeichen.

> [!Note]  
> Sie können systemdefinierte Eigenschaftsnamen auch in doppelte Anführungszeichen umschließen, um lesbar zu sein. Dies wirkt sich nicht auf die Kompatibilität aus.

 

Wenn die Abfrage ein Dokument zurückgibt, das nicht über die angeforderte Spalte verfügt, ist der Wert dieser Spalte für das Dokument **NULL.**

Sie müssen mindestens einen Spaltennamen in einer SELECT-Anweisung angeben. In der strukturierte Abfragesprache -Abfrage (SQL) können Sie das Sternchen ( ) verwenden, um anzugeben, dass alle Spalten in einer Tabelle \* zurückgegeben werden sollen. Es gilt jedoch kein definierter und fester Satz von Eigenschaften für alle Dokumente. Aus diesem Grund ist das SQL sternchen im Spaltenspezifizierer der &lt; &gt; SELECT-Anweisung nicht zulässig.

## <a name="getting-the-top-n-results"></a>Abrufen der ersten n Ergebnisse

Sie können eine maximale Anzahl von Ergebnissen angeben, die mithilfe der TOP-Syntax zurückgeben werden:


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Typumformung von Spaltendatentypen

Manchmal müssen Sie möglicherweise aus Dokumenten extrahierte Zeichenfolgendaten in einen anderen Datentyp casten, damit ein entsprechender Vergleich vorgenommen werden kann. Weitere Informationen finden Sie unter [Umwandlung des Datentyps einer Spalte.](-search-sql-castingdatacolumntype.md)

## <a name="examples"></a>Beispiele

In den folgenden Beispielen werden der Name und die URL der übereinstimmenden Dokumente angegeben.


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Umwandlung des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Systemeigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



