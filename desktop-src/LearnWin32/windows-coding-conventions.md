---
title: Windows Codierungskonventionen
description: Wenn Sie noch nicht mit Windows arbeiten, kann es versirrend sein, wenn Sie zum ersten Mal ein Windows sehen.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78c24f38f9f2f410c044637ca3aa59d4baa39e9b671b3485c5b85899b69c2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387395"
---
# <a name="windows-coding-conventions"></a>Windows Codierungskonventionen

Wenn Sie noch nicht mit Windows arbeiten, kann es versirrend sein, wenn Sie zum ersten Mal ein Windows sehen. Der Code ist mit ungewöhnlichen Typdefinitionen wie **DWORD \_ PTR** und **LPRECT** gefüllt, und Variablen verfügen über Namen wie *hWnd* und *pwsz* (als "Ink malische Notation" bezeichnet). Es lohnt sich, sich einen Moment Zeit zu nehmen, um einige der Windows programmieren zu lernen.

Die überwiegende Mehrheit Windows APIs besteht entweder aus Funktionen oder Component Object Model (COM)-Schnittstellen. Nur sehr wenige Windows-APIs werden als C++-Klassen bereitgestellt. (Eine wichtige Ausnahme ist GDI+, eine der 2D-Grafik-APIs.)

## <a name="typedefs"></a>TypeDefs

Die Windows-Header enthalten viele Typedefs. Viele davon sind in der Headerdatei WinDef.h definiert. Hier sind einige, auf die Sie häufig stoßen werden.

### <a name="integer-types"></a>Ganzzahltypen



| Datentyp     | Size    | Unterzeichnet?  |
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



 

Wie Sie sehen können, gibt es eine gewisse Redundanz in diesen Typedefs. Ein Teil dieser Überlappung ist einfach auf den Verlauf der Windows-APIs zurück. Die hier aufgeführten Typen haben eine feste Größe, und die Größen sind in 32-Bit- und 64-Anwendungen identisch. Der **DWORD-Typ** ist beispielsweise immer 32 Bit breit.

### <a name="boolean-type"></a>Boolescher Typ

**BOOL** ist eine Typedef für einen ganzzahligen Wert, der in einem booleschen Kontext verwendet wird. Die Headerdatei WinDef.h definiert außerdem zwei Werte für die Verwendung mit **BOOL.**


```C++
#define FALSE    0 
#define TRUE     1
```



Trotz dieser Definition von **TRUE** können die meisten Funktionen, die einen **BOOL-Typ** zurückgeben, jeden Wert zurückgeben, der nicht 0 (null) ist, um die boolesche Wahrheit anzugeben. Daher sollten Sie immer dies schreiben:


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



und nicht dies:


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



Beachten Sie, dass **BOOL** ein ganzzahliger Typ ist und nicht mit dem **bool-Typ** C++ austauschbar ist.

### <a name="pointer-types"></a>Zeigertypen

Windows definiert viele Datentypen des *Formularzeigers auf X.* Diese haben in der Regel *das Präfix P-* *oder LP-* im Namen. **LPRECT** ist beispielsweise ein Zeiger auf ein [**RECT,**](/previous-versions//dd162897(v=vs.85))wobei **RECT** eine Struktur ist, die ein Rechteck beschreibt. Die folgenden Variablendeklarationen sind gleichwertig.


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



In der Vergangenheit *steht P* für "zeiger" und *LP* für "long pointer". Lange Zeiger (auch als Far-Zeiger *bezeichnet)* sind ein Holdover von 16-Bit-Windows, wenn sie benötigt wurden, um Speicherbereiche außerhalb des aktuellen Segments zu adressieren. Das *LP-Präfix* wurde beibehalten, um das Portieren von 16-Bit-Code auf 32-Bit-Windows. Heute gibt es keinen Unterschied– ein Zeiger ist ein Zeiger.

### <a name="pointer-precision-types"></a>Zeigergenauigkeitstypen

Die folgenden Datentypen weisen immer die Größe eines Zeigers auf, d. &a. 32 Bit Breite in 32-Bit-Anwendungen und 64 Bit Breite in 64-Bit-Anwendungen. Die Größe wird zur Kompilierzeit bestimmt. Wenn eine 32-Bit-Anwendung auf 64-Bit-Windows ausgeführt wird, sind diese Datentypen immer noch 4 Byte breit. (Eine 64-Bit-Anwendung kann nicht auf 32-Bit-Windows ausgeführt werden, sodass die umgekehrte Situation nicht eintritt.)

-   **DWORD \_ PTR**
-   **INT \_ PTR**
-   **LONG \_ PTR**
-   **ULONG \_ PTR**
-   **UINT \_ PTR**

Diese Typen werden in Situationen verwendet, in denen eine ganze Zahl in einen Zeiger konvertiert werden kann. Sie werden auch verwendet, um Variablen für Zeigerarithmetik zu definieren und Schleifenzähler zu definieren, die den gesamten Bytebereich in Speicherpuffern durchlaufen. Im Allgemeinen werden sie an Stellen angezeigt, an denen ein vorhandener 32-Bit-Wert auf 64 Bit auf 64 Bit erweitert Windows.

## <a name="hungarian-notation"></a>Notation (Deutsch)

*Bei der notieren Notation* handelt es sich um das Hinzufügen von Präfixen zu den Namen von Variablen, um zusätzliche Informationen über die Variable zu erhalten. (Der Rausch der Notation, Charles Simonyi, war", daher der Name".

In der ursprünglichen Form liefert die notation -Notation *semantische* Informationen zu einer Variablen, die Ihnen die beabsichtigte Verwendung angibt. Beispielsweise bedeutet *"i"* einen Index, *"cb"* eine Größe in Bytes ("Anzahl von Bytes") und *"rw"* und *"col"* die mittleren Zeilen- und Spaltennummern. Diese Präfixe sind so konzipiert, dass die versehentliche Verwendung einer Variablen im falschen Kontext vermieden wird. Wenn Sie beispielsweise den Ausdruck gesehen haben, wissen Sie, dass einer Größe eine Zeilennummer hinzugefügt wird. Dies ist mit sicherheit ein `rwPosition +  cbTable` Fehler im Code.

In einer gängigeren Form der notation -Notation werden Präfixe verwendet, um Typinformationen zu geben, z. B. *dw* für **DWORD** und *w* für **WORD**. 

Wenn Sie im Web nach "Inkungszeichen" suchen, finden Sie viele Meinung darüber, ob die notation-Notation gut oder schlecht ist. Einige Programmierer haben eine intensive Abneigung gegen die Notation "Deutsch". Andere finden es hilfreich. Unabhängig davon verwenden viele der Codebeispiele auf MSDN die notation -Notation, aber Sie müssen sich die Präfixe nicht merken, um den Code zu verstehen.

## <a name="next"></a>Nächste

[Arbeiten mit Zeichenfolgen](working-with-strings.md)

 

 