---
description: ICE32 überprüft, ob die Schlüssel und Fremdschlüssel in der MSI-Datei denselben Größen-und Spalten Definitions Typen entsprechen.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362324"
---
# <a name="ice32"></a>ICE32

ICE32 überprüft, ob die Schlüssel und Fremdschlüssel in der MSI-Datei denselben Größen-und Spalten Definitions Typen entsprechen. Diese benutzerdefinierte Ice-Aktion führt den Vergleich mithilfe der [ \_ Validierungs Tabelle](-validation-table.md) durch und verwendet die Definitions Typen, die von " [**msiviewgetcolumninfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)" zurückgegeben werden. Weitere Informationen finden Sie unter [Column Definition Format](column-definition-format.md).

## <a name="result"></a>Ergebnis

ICE32 gibt Fehler aus, wenn die MSI-Datei Fremdschlüssel für Schlüssel mit einer anderen Spaltenlänge oder einem anderen Spaltendatentyp enthält.

## <a name="example"></a>Beispiel

ICE32 gibt zwei Fehler für das folgende Beispiel aus:

-   Es ist ein Fremdschlüssel und ein Schlüssel definiert, die sich von der Größe unterscheiden.
-   Es ist ein Fremdschlüssel und ein Schlüssel definiert, die sich in Ihrem Definitionstyp unterscheiden.

[ \_ Validierungs Tabelle](-validation-table.md) (partiell)



| Tabelle | Spalte  | KeyTable | KeyColumn |
|-------|---------|----------|-----------|
| File  | Version | Datei     | 1         |
| Klapp  | Column8 | Klapp     | 1         |



 

Spaltendefinitionen (partiell)



| Tabelle | Spalte  | type | Size |
|-------|---------|------|------|
| File  | File    | s    | 72   |
| File  | Version | E    | 32   |
| Klapp  | Column1 | i    | 2    |
| Klapp  | Column8 | E    | 32   |



 

In der Spalte Version der Dateitabelle kann es sich um einen Fremdschlüssel für eine andere Datei in der Dateitabelle handeln. Dies tritt bei Begleit Dateien auf. In der Spalte Version ist jedoch nur eine Zeichen folgen Länge von 32 zulässig, während die Spalte Datei eine Zeichen folgen Länge von 72 zulässt. Um diesen Fehler zu beheben, ändern Sie die Länge der Zeichenfolge entsprechend.

Es sind ein Fremdschlüssel und ein Schlüssel definiert, die sich in ihren Definitions Typen unterscheiden. Column8 der Flap-Tabelle wird als Fremdschlüssel für column1 aufgeführt. Column8 ist eine Zeichen folgen Spalte und column1 eine ganzzahlige Spalte. Die Fremdschlüssel-und Schlüsselpaare müssen so definiert sein, dass Ihre Datentypen stimmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



