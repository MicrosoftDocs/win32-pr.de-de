---
title: Mittelgroße Arrays
description: Mittel l-Arrays.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- Datentypen mittlerer l, Arrays
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038935"
---
# <a name="midl-arrays"></a>Mittelgroße Arrays

Arraydeklaratoren werden im Schnittstellen Text der IDL-Datei als einer der folgenden Zeichen folgen angezeigt:

-   Teil einer allgemeinen Deklaration
-   Ein Member einer Struktur oder eines Union-Deklarators.
-   Ein Parameter für einen Remote Prozedur aufrufen

Die Begrenzungen der einzelnen Dimensionen des Arrays werden innerhalb eines separaten Paars von eckigen Klammern ausgedrückt. Ein Ausdruck, der zu *n* ausgewertet wird, steht für eine untere Grenze von 0 (null) und eine obere Grenze von *n-1*. Wenn die eckigen Klammern leer sind oder ein einzelnes Sternchen ( \* ) enthalten, ist die untere Grenze NULL, und die obere Grenze wird zur Laufzeit bestimmt.

Das Array kann auch zwei durch ein Auslassungs Zeichen getrennte Werte enthalten, die die unteren und oberen Begrenzungen des Arrays darstellen, wie in \[ *niedriger*... *oben* \] . Microsoft RPC erfordert eine untere Grenze von NULL. Der mittlerer l-Compiler erkennt keine Konstrukte, die niedrigere Grenzen ungleich NULL angeben.

Arrays können den Feld Attributen "size", " [**Max \_ is**](max-is.md)", " [**length \_ is**](length-is.md)", " [**First \_ is**](first-is.md)" und " [**Last" \_ ist**](last-is.md) die Angabe der Größe des Arrays oder des Teils des Arrays, das gültige Daten enthält. [**\_**](size-is.md) Diese Feld Attribute identifizieren den Parameter, das Strukturfeld oder die Konstante, die die Array Dimension oder den Index angibt.

Das Array muss mit dem Bezeichner verknüpft werden, der vom Feld Attribut auf folgende Weise angegeben wird: Wenn das Array ein Parameter ist, muss der Bezeichner auch ein Parameter für dieselbe Funktion sein. Wenn das Array ein Strukturfeld ist, muss der Bezeichner ein weiteres Strukturfeld derselben Struktur sein.

Ein Array wird als "konform" bezeichnet, wenn die obere Grenze einer Dimension zur Laufzeit bestimmt wird. (Nur obere Begrenzungen können zur Laufzeit bestimmt werden.) Um die obere Grenze zu ermitteln, muss die Array Deklaration [**eine \_ Größe**](size-is.md) oder ein [**Maximales \_ is**](max-is.md) -Attribut enthalten.

Ein Array wird als "Variation" bezeichnet, wenn seine Begrenzungen zur Kompilierzeit bestimmt werden, der Bereich der übertragenen Elemente jedoch zur Laufzeit bestimmt wird. Um den Bereich der übertragenen Elemente zu ermitteln, muss die Array Deklaration [**eine \_ Länge**](length-is.md)von, [**First \_ ist**](first-is.md)oder das [**Letzte \_ is**](last-is.md) -Attribut enthalten.

Ein Übereinstimmung unterschiedliches Array (auch als "Open" bezeichnet) ist ein Array, dessen obere Grenze und der Bereich der übertragenen Elemente zur Laufzeit bestimmt werden. Höchstens ein konformes oder konform veränderliches Array kann in eine C-Struktur eingefügt werden und muss das letzte Element der Struktur sein. Im Gegensatz dazu können nicht konforme Arrays an beliebiger Stelle in einer Struktur vorkommen.

## <a name="examples"></a>Beispiele

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

Weitere Informationen finden Sie unter [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).

## <a name="multidimensional-arrays"></a>Mehrdimensionale Arrays

Der Benutzer kann Typen deklarieren, die Arrays sind, und dann Arrays von Objekten dieser Typen deklarieren. Die Semantik von *m*-dimensionalen Arrays von *n*-dimensionalen Array Typen ist mit der Semantik von *m* + *n*-dimensionalen Arrays identisch.

Beispielsweise kann der Typ "Rect" \_ als zweidimensionales Array definiert werden, und die Variable " *Rect* " kann als ein Array vom Typ "Rect" definiert werden \_ . Dies entspricht dem dreidimensionalen Array *Äquivalent " \_ Rect*":

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

Microsoft RPC ist C-orientiert. Gemäß den Konventionen der C-Sprache kann nur die erste Dimension eines mehrdimensionalen Arrays zur Laufzeit bestimmt werden. Die Interoperation mit DCE-IDL-Arrays, die andere Sprachen unterstützen, ist auf Folgendes beschränkt:

-   Mehrdimensionale Arrays mit Konstanten (Kompilierzeit festgelegten) Begrenzungen.
-   Mehrdimensionale Arrays mit allen Konstanten Begrenzungen außer der ersten Dimension. Die obere Grenze und der Bereich der übertragenen Elemente der ersten Dimension sind von der Laufzeit abhängig.
-   Alle eindimensionalen Arrays mit einer unteren Grenze von 0 (null).

Wenn das **\[** [**String**](string.md) - **\]** Attribut für mehrdimensionale Arrays verwendet wird, gilt das-Attribut für das äußteste ganz rechts.

## <a name="arrays-of-pointers"></a>Arrays von Zeigern

Verweis Zeiger müssen auf gültige Daten zeigen. Die Client Anwendung muss den gesamten Arbeitsspeicher für ein **\[** [**in**](in.md) - **\]** oder **\[** **in-,**[**out**](out-idl.md) - **\]** Array von Verweis Zeigern zuordnen, insbesondere wenn das Array mit den Werten **\[ in \]**, oder **\[** **in, out \]**, **\[** [**length \_ is**](length-is.md) **\]** oder **\[** [**Last \_ is**](last-is.md) **\]** zugeordnet ist. Die Client Anwendung muss auch alle Array Elemente vor dem-Befehl initialisieren. Vor der Rückgabe an den Client muss die Serveranwendung überprüfen, ob alle Array Elemente im übertragenen Bereich auf einen gültigen Speicher zeigen.

Auf der Serverseite ordnet der Stub Speicher für alle Array Elemente zu, unabhängig davon, wie **\[** [**lange \_**](length-is.md) der **\]** Wert ist oder der **\[** letzte Wert zum Zeitpunkt des [**\_ Aufrufes ist**](last-is.md) **\]** . Diese Funktion kann sich auf die Leistung Ihrer Anwendung auswirken.

Es gelten keine Einschränkungen für Arrays eindeutiger Zeiger. Sowohl auf dem Client als auch auf dem Server wird der Speicher für NULL-Zeiger zugeordnet. Wenn Zeiger ungleich NULL sind, werden die Daten in einem vorab zugeordneten Speicher abgelegt.

Ein optionaler zeigerdeklarator kann dem Arraydeklarator vorangestellt werden.

Wenn eingebettete Verweis Zeiger reine **\[** [**out**](out-idl.md) **\]** -Parameter sind, muss der Server-Manager-Code dem Array von Verweis Zeigern gültige Werte zuweisen. Beispiel:

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

Die generierten stubwerte ordnen das Array zu und weisen allen in das Array eingebetteten Zeigern NULL-Werte zu.

 

 