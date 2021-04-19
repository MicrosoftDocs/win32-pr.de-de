---
title: Windows-Codierungs Konventionen
description: Wenn Sie mit der Windows-Programmierung noch nicht vertraut sind, kann es zu einer displanung kommen, wenn ein Windows-Programm angezeigt wird.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341925"
---
# <a name="windows-coding-conventions"></a>Windows-Codierungs Konventionen

Wenn Sie mit der Windows-Programmierung noch nicht vertraut sind, kann es zu einer displanung kommen, wenn ein Windows-Programm angezeigt wird. Der Code wird mit seltsamen Typdefinitionen wie **DWORD \_ ptr** und **lprect** gefüllt, und Variablen haben Namen wie *HWND* und *Pwsz* (als ungarische Notation bezeichnet). Es lohnt sich, einige der Windows-Codierungs Konventionen kennenzulernen.

Die meisten Windows-APIs bestehen aus Funktionen oder Component Object Model (com)-Schnittstellen. Nur wenige Windows-APIs werden als C++-Klassen bereitgestellt. (Eine wichtige Ausnahme ist GDI+, eine der 2D-Grafik-APIs.)

## <a name="typedefs"></a>TypeDefs

Die Windows-Header enthalten zahlreiche Typedefs. Viele davon sind in der Header Datei WINDEF. h definiert. Im folgenden finden Sie einige, auf die Sie häufig stoßen werden.

### <a name="integer-types"></a>Ganzzahltypen



| Datentyp     | Size    | Ebenes?  |
|---------------|---------|----------|
| **BYTE**      | 8 Bit  | Ohne Vorzeichen |
| **DWORD**     | 32 Bit | Ohne Vorzeichen |
| **INT32**     | 32 Bit | Signiert   |
| **INT64**     | 64 Bit | Signiert   |
| **LONG**      | 32 Bit | Signiert   |
| **LONGLONG**  | 64 Bit | Signiert   |
| **UINT32**    | 32 Bit | Ohne Vorzeichen |
| **UINT64**    | 64 Bit | Ohne Vorzeichen |
| **ULONG**     | 32 Bit | Ohne Vorzeichen |
| **ULONGLONG** | 64 Bit | Ohne Vorzeichen |
| **WORD**      | 16 Bit | Ohne Vorzeichen |



 

Wie Sie sehen können, gibt es eine gewisse Redundanz in diesen Typedefs. Einige dieser Überschneidungen sind lediglich auf den Verlauf der Windows-APIs zurückzuführen. Die hier aufgeführten Typen haben eine fester Größe, und die Größen sind in 32-Bit-und 64-Anwendungen identisch. Beispielsweise ist der **DWORD** -Typ immer 32 Bits breit.

### <a name="boolean-type"></a>Boolescher Typ

**Bool** ist eine typedef für einen ganzzahligen Wert, der in einem booleschen Kontext verwendet wird. Die Header Datei WINDEF. h definiert auch zwei Werte für die Verwendung mit **bool**.


```C++
#define FALSE    0 
#define TRUE     1
```



Trotz dieser Definition von **true** können die meisten Funktionen, die einen **booleschen** Typ zurückgeben, einen Wert ungleich 0 (null) zurückgeben, um die boolesche Wahrheit anzugeben. Daher sollten Sie immer Folgendes schreiben:


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



und nicht:


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



Beachten Sie, dass **bool** ein ganzzahliger Typ ist und nicht mit dem C++ **bool** -Typ austauschbar ist.

### <a name="pointer-types"></a>Zeiger Typen

Windows definiert viele Datentypen des Formular *Zeigers auf X*. Diese haben in der Regel das Präfix *P-* oder *LP-* in den Namen. Beispielsweise ist **lprect** ein Zeiger auf ein [**Rect**](/previous-versions//dd162897(v=vs.85)), wobei **Rect** eine Struktur ist, die ein Rechteck beschreibt. Die folgenden Variablen Deklarationen sind gleichwertig.


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



In der Vergangenheit steht *P* für "Zeiger" und " *LP* " für "Long-Zeiger". Lange Zeiger (auch als " *weite Zeiger*" bezeichnet) sind eine Holdover von 16-Bit-Fenstern, wenn Sie benötigt werden, um Speicherbereiche außerhalb des aktuellen Segments zu beheben. Das *LP* -Präfix wurde beibehalten, um das Portieren von 16-Bit-Code auf 32-Bit-Windows zu vereinfachen. Heute gibt es keinen Unterschied – ein Zeiger ist ein Zeiger.

### <a name="pointer-precision-types"></a>Zeiger Genauigkeits Typen

Die folgenden Datentypen sind immer die Größe eines Zeigers – d. h. 32 Bits Wide in 32-Bit-Anwendungen und 64 Bits Wide in 64-Bit-Anwendungen. Die Größe wird zur Kompilierzeit bestimmt. Wenn eine 32-Bit-Anwendung auf 64-Bit-Windows ausgeführt wird, sind diese Datentypen weiterhin 4 Bytes breit. (Eine 64-Bit-Anwendung kann nicht auf 32-Bit-Fenstern ausgeführt werden, sodass keine umgekehrte Situation auftritt.)

-   **DWORD \_ ptr**
-   **INT \_ ptr**
-   **Long- \_ ptr**
-   **ULONG \_ ptr**
-   **uint \_ ptr**

Diese Typen werden in Situationen verwendet, in denen eine Ganzzahl in einen-Zeiger umgewandelt werden kann. Sie werden auch verwendet, um Variablen für Zeigerarithmetik zu definieren und Schleifen Zähler zu definieren, die den gesamten Bereich von Bytes in Speicher Puffern durchlaufen. Im Allgemeinen werden Sie an Stellen angezeigt, an denen ein vorhandener 32-Bit-Wert auf 64 Bits auf 64-Bit-Fenstern erweitert wurde.

## <a name="hungarian-notation"></a>Ungarische Notation

In der *ungarischen Schreib* Weise werden den Namen von Variablen Präfixe hinzugefügt, um zusätzliche Informationen zur Variablen zu erhalten. (Der Erfinder der Notation, Charles Simonyi, war Ungarisch und daher sein Name).

In der ursprünglichen Form gibt die ungarische Notation *semantische* Informationen zu einer Variablen an und gibt Ihnen die beabsichtigte Verwendung. Beispiels *Weise bedeutet dies* , dass ein Index, *CB* , eine Größe in Byte ("count of bytes") und die Zeilen-und Spalten Nummern von *RW* und *Col* bedeuten. Diese Präfixe sind so konzipiert, dass die versehentliche Verwendung einer Variablen im falschen Kontext vermieden wird. Wenn Sie z. b. den Ausdruck gesehen haben `rwPosition +  cbTable` , wissen Sie, dass eine Zeilennummer zu einer Größe hinzugefügt wird, was fast sicherlich ein Fehler im Code ist.

Eine allgemeinere Form der ungarischen Notation verwendet Präfixe, um *Typinformationen* anzugeben – beispielsweise *DW* für **DWORD** und *w* für **Word**.

Wenn Sie im Web nach "ungarischer Notation" suchen, finden Sie viele Meinungen darüber, ob die ungarische Notation gut oder schlecht ist. Einige Programmierer haben eine sehr hohe Abneigung gegen die ungarische Notation. Andere finden es hilfreich. Unabhängig davon verwenden viele der Codebeispiele auf MSDN die ungarische Notation, aber Sie müssen nicht die Präfixe beachten, um den Code zu verstehen.

## <a name="next"></a>Nächste

[Arbeiten mit Zeichen folgen](working-with-strings.md)

 

 