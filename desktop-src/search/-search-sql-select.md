---
description: 'Im Folgenden wird die grundlegende Syntax der SELECT-Anweisung für eine lokale Abfrage veranschaulicht:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: SELECT-Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df8cc5f4b6bab673d20c981e44386d3fdbd651b5a2753d8c965ee55023a6562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227195"
---
# <a name="select-statement"></a>SELECT-Anweisung

Im Folgenden wird die grundlegende Syntax der SELECT-Anweisung für eine lokale Abfrage veranschaulicht:


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



Im Folgenden wird der Spaltenteil der SELECT-Anweisungssyntax dargestellt:


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



Die Spaltenspezifizierer müssen gültige Eigenschaftennamenspalten sein, die durch Kommas getrennt sind. Gültige Spaltennamen sind registrierte Eigenschaftenbeschreibungen oder werden durch das Eigenschaftensystemschema der Shell definiert. Sie können nur die Spalten auswählen, die im Eigenschaftensystemschema als abrufbar markiert sind. Wenn Sie mit gemischter Schreibung Eigenschaften identifizieren, bei denen es sich nicht um systemdefinierte Eigenschaften handelt, müssen Sie den Spaltenspezifizierer in doppelte Anführungszeichen einschließen. Systemdefinierte Eigenschaftennamen enthalten alle Eigenschaften, die mit "System" beginnen (z.B. System.Contact.FirstName), und erfordern keine Anführungszeichen.

> [!Note]  
> Sie können systemdefinierte Eigenschaftennamen aus Gründen der Lesbarkeit auch in doppelte Anführungszeichen einschließen. Dies wirkt sich nicht auf die Kompatibilität aus.

 

Wenn die Abfrage ein Dokument zurückgibt, das nicht über die angeforderte Spalte verfügt, ist der Wert dieser Spalte für das Dokument **NULL.**

Sie müssen mindestens einen Spaltennamen in einer SELECT-Anweisung angeben. In der abfrage strukturierte Abfragesprache (SQL) können Sie das Sternchen () verwenden, \* um anzugeben, dass alle Spalten in einer Tabelle zurückgegeben werden sollen. Es gelten jedoch keine definierten und festen Eigenschaften für alle Dokumente. Aus diesem Grund ist das SQL Sternchen im <columns> Spezifizierer der SELECT-Anweisung nicht zulässig.

## <a name="getting-the-top-n-results"></a>Abrufen der besten n Ergebnisse

Sie können eine maximale Anzahl von Ergebnissen angeben, die zurückgegeben werden sollen, indem Sie die TOP-Syntax verwenden:


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Datentypen von Umwandlungsspalten

Manchmal müssen Sie möglicherweise Zeichenfolgendaten, die aus Dokumenten extrahiert wurden, in einen anderen Datentyp umformen, damit ein entsprechender Vergleich durchgeführt werden kann. Weitere Informationen finden Sie unter [Umwandeln des Datentyps einer Spalte.](-search-sql-castingdatacolumntype.md)

## <a name="examples"></a>Beispiele

In den folgenden Beispielen werden der Name und die URL übereinstimmender Dokumente zurückgegeben.


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Umwandeln des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Systemeigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



