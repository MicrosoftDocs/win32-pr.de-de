---
title: Übersetzen in Visual Basic von C++
description: Übersetzen in Visual Basic von C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340216"
---
# <a name="translating-to-visual-basic-from-c"></a>Übersetzen in Visual Basic von C++

Mithilfe der Programmiersprache C++ können Entwickler direkt auf den Speicher zugreifen, in dem eine bestimmte Variable gespeichert wird. Speicher Zeiger bieten diesen direkten Zugriff. In Visual Basic werden Zeiger für Sie behandelt. Beispielsweise ist ein Parameter, der als Zeiger auf ein **int** in C++ deklariert ist, mit einem Parameter identisch, der in Visual Basic als **ByRef**- **Ganzzahl** deklariert wurde.

Ein Parameter, der in Visual Basic **als Zeichenfolge** deklariert ist, wird als Zeiger auf einen **BSTR** in C++ deklariert. Das Festlegen eines Zeichen folgen Zeigers auf **null** in C++ entspricht dem Festlegen der Zeichenfolge auf die **vbNullString** -Konstante in Visual Basic. Das übergeben einer Zeichenfolge der Länge 0 ("") an eine Funktion, die für den Empfang von **null** vorgesehen ist, funktioniert nicht, da dadurch ein Zeiger auf eine Zeichenfolge der Länge 0 (null) anstatt auf einen NULL-Zeiger übergeben wird.

C++ unterstützt Datencontainer, d.. Strukturen und Unions, die in den frühen Versionen von Visual Basic keine Entsprechungen aufweisen. Aus diesem Grund wrappen com-Objekte in der Regel Informationen, die normalerweise in Strukturen und Unions in Objektklassen gespeichert werden. Einige COM-Objekte enthalten jedoch möglicherweise Strukturen, die dazu führen, dass die Visual Basic auf Teile der Methoden oder Funktionen des Objekts nicht zugreifen können.

Einige C++-Datentypen werden in Visual Basic nicht unterstützt, z. b. unsignierte Typen und **HWND** -Typen. Methoden, die diese Datentypen akzeptieren oder zurückgeben, sind in Visual Basic nicht verfügbar.

In Visual Basic werden die mit Automation kompatiblen Datentypen als interne Datentypen verwendet. Daher sind C++-Datentypen, die Automatisierungs kompatibel sind, auch mit Visual Basic kompatibel. Datentypen, die nicht Automatisierungs kompatibel sind, können möglicherweise nicht in Visual Basic konvertiert werden.

In der folgenden Tabelle werden die Datentypen aufgelistet, die von Visual Basic und ihren **VarType** -Entsprechungen unterstützt werden. **VarType** ist eine Enumeration, die die Arten von Automatisierungs Varianten auflistet.



| Datentyp in Visual Basic  | VarType-Entsprechung                |
|-------------------------|-----------------------------------|
| **Integer**<br/>  | 16 Bit, signiert, VT \_ I2<br/> |
| **Long**<br/>     | 32 Bit, signiert, VT \_ I4<br/> |
| **Datum**<br/>     | VT- \_ Datum<br/>               |
| **Währung**<br/> | VT- \_ CY<br/>                 |
| **Object**<br/>   | \*VT \_ -Verteilung<br/>         |
| **String**<br/>   | VT \_ BSTR<br/>               |
| **Boolescher Wert**<br/>  | VT \_ bool<br/>               |
| **Währung**<br/> | VT ( \_ dezimal)<br/>            |
| **Single**<br/>   | VT \_ R4<br/>                 |
| **Double**<br/>   | VT \_ R8<br/>                 |
| **Dezimal**<br/>  | VT ( \_ dezimal)<br/>            |
| **Byte**<br/>     | VT ( \_ dezimal)<br/>            |
| **Konfigur**<br/>  | VT- \_ Variante<br/>            |



 

Alle Parameter in Visual Basic, sofern Sie nicht mit dem Schlüsselwort **ByVal** gekennzeichnet sind, werden als Verweis (als Zeiger) anstatt als Wert übermittelt.

C++ und Visual Basic unterscheiden sich geringfügig von der Darstellung von Eigenschaften. In C++ werden Eigenschaften als ein Satz von Accessorfunktionen dargestellt, der den Eigenschafts Wert festlegt und einen, der den Eigenschafts Wert abruft. In Visual Basic werden Eigenschaften als einzelnes Element dargestellt, das zum Abrufen oder Festlegen des Eigenschafts Werts verwendet werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 





