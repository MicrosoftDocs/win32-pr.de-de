---
description: ICE32 überprüft, ob Schlüssel und Fremdschlüssel in der .msi datei die gleichen Größen- und Spaltendefinitionstypen haben.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e9361cd091afea3444858e64e043b87b779c2313f0ba16bb0ec6cf58fad265
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528620"
---
# <a name="ice32"></a>ICE32

ICE32 überprüft, ob Schlüssel und Fremdschlüssel in der .msi datei die gleichen Größen- und Spaltendefinitionstypen haben. Diese benutzerdefinierte ICE-Aktion vergleicht den Vergleich mithilfe der [ \_ Validation-Tabelle](-validation-table.md) und der Definitionstypen, die von [**MsiViewGetColumnInfo zurückgegeben werden.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) Weitere Informationen finden Sie unter [Spaltendefinitionsformat](column-definition-format.md).

## <a name="result"></a>Ergebnis

ICE32 gibt Fehler aus, wenn .msi-Datei Fremdschlüssel für Schlüssel mit einer anderen Spaltenlänge oder einem anderen Spaltendatentyp enthält.

## <a name="example"></a>Beispiel

ICE32 veröffentlicht zwei Fehler für das gezeigte Beispiel:

-   Es sind ein Fremdschlüssel und ein Fremdschlüssel definiert, die sich in der Größe unterscheiden.
-   Es sind ein Fremdschlüssel und ein Fremdschlüssel definiert, die sich in ihrem Definitionstyp unterscheiden.

[ \_ Validierungstabelle](-validation-table.md) (partiell)



| Tabelle | Spalte  | KeyTable | KeyColumn |
|-------|---------|----------|-----------|
| Datei  | Version | Datei     | 1         |
| Klappe  | Column8 | Klappe     | 1         |



 

Spaltendefinitionen (partiell)



| Tabelle | Spalte  | Typ | Size |
|-------|---------|------|------|
| Datei  | Datei    | s    | 72   |
| Datei  | Version | E    | 32   |
| Klappe  | Column1 | i    | 2    |
| Klappe  | Column8 | E    | 32   |



 

Die Spalte Version der Tabelle Datei kann ein Fremdschlüssel für eine andere Datei in der Tabelle Datei sein. Dies tritt bei Begleitdateien auf. Die Spalte Version lässt jedoch nur eine Zeichenfolgenlänge von 32 zu, während die Spalte Datei eine Zeichenfolgenlänge von 72 zulässt. Um diesen Fehler zu beheben, ändern Sie die Zeichenfolgenlängen, die übereinstimmen.

Es sind ein Fremdschlüssel und ein Fremdschlüssel definiert, die sich in ihren Definitionstypen unterscheiden. Column8 der Flap-Tabelle wird als Fremdschlüssel für Column1 aufgeführt. Column8 ist eine Zeichenfolgenspalte und Column1 eine ganzzahlige Spalte. Die Fremdschlüssel- und Schlüsselpaare müssen so definiert werden, dass ihre Datentypen übereinstimmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



