---
title: " if-, elif-, else- und endif-Direktiven"
description: Präprozessordirektiven, die die Kompilierung von Teilen einer Quelldatei steuern.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- if-, elif-, else- und endif-Direktiven HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb5f4716509905d4ce800abbe4cb11b85d116d7a5afd5a56301b1ecb5ce0724b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726450"
---
# <a name="if-elif-else-and-endif-directives"></a>\#if-, \# \# elif-, else- und \# endif-Direktiven

Präprozessordirektiven, die die Kompilierung von Teilen einer Quelldatei steuern.



| \#*, wenn ifCondition* ...         |
|--------------------------------|
| \[\#elif *elifCondition* ...\] |
| \[\#oder...\]                 |
| \#endif                        |



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                                                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*<br/>                                                                                   | Die primäre auszuwertende Bedingung. Wenn dieser Parameter zu einem Wert ungleich 0 (null) ausgewertet wird, wird der gesamte Text zwischen dieser \# if-Direktive und der nächsten Instanz der \# elif-, \# else- oder \# endif-Direktive in der Übersetzungseinheit beibehalten. Andernfalls wird der nachfolgende Quellcode nicht beibehalten. <br/> Die Bedingung kann den definierten Präprozessoroperator verwenden, um zu bestimmen, ob eine bestimmte Präprozessorkonstante oder ein bestimmtes Makro definiert ist. Diese Verwendung entspricht der Verwendung der [ \# ifdef-Direktive.](dx-graphics-hlsl-appendix-pre-ifdef.md) <br/> Einschränkungen für den Wert des *ifCondition-Parameters* finden Sie im Abschnitt Hinweise. <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ Optional\] <br/> | Andere auszuwertende Bedingung. Wenn der *ifCondition-Parameter* und alle vorherigen \# elif-Direktiven zu 0 (null) ausgewertet werden und dieser Parameter einen Wert ungleich 0 ergibt, wird der gesamte Text zwischen dieser \# elif-Direktive und der nächsten Instanz der \# elif-, \# else- oder \# endif-Direktive in der Übersetzungseinheit beibehalten. Andernfalls wird der nachfolgende Quellcode nicht beibehalten. <br/> Die Bedingung kann den definierten Präprozessoroperator verwenden, um zu bestimmen, ob eine bestimmte Präprozessorkonstante oder ein bestimmtes Makro definiert ist. Diese Verwendung entspricht der Verwendung der [ \# ifdef-Direktive.](dx-graphics-hlsl-appendix-pre-ifdef.md) <br/> Einschränkungen für den Wert des *elifCondition-Parameters* finden Sie im Abschnitt Hinweise. <br/> |



 

## <a name="remarks"></a>Hinweise

Jede \# if-Direktive in einer Quelldatei muss mit einer schließenden \# endif-Direktive abgegleichen werden. Eine beliebige Anzahl von \# Elifdirektiven kann zwischen der \# if- und \# endif-Direktive angezeigt werden, aber höchstens eine \# andere Direktive ist zulässig. Falls \# vorhanden, muss die else-Direktive die letzte Direktive vor \# endif sein. Anweisungen für die bedingte Kompilierung, die in Includedateien enthalten sind, müssen dieselben Bedingungen erfüllen.

Die \# \# if-, \# elif-, else- und \# endif-Direktiven können in den Textabschnitten anderer if-Direktiven geschachtelt \# werden. Jede geschachtelte \# \# else-, elif- oder \# endif-Direktive gehört zur nächstgelegenen vorangehenden \# if-Direktive.

Wenn keine Bedingungen zu einem Wert ungleich 0 (null) ausgewertet werden, wählt der Präprozessor den Textblock nach der \# else-Anweisung aus. Wenn die \# else-Klausel ausgelassen wird und keine Bedingungen zu einem Wert ungleich 0 (null) ausgewertet werden, wird kein Textblock ausgewählt.

Die Parameter *ifCondition* und *elifCondition* erfüllen die folgenden Anforderungen:

-   Ausdrücke für die bedingte Kompilierung werden als lange Werte mit [**Vorzeichen**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) behandelt, und diese Ausdrücke werden mit den gleichen Regeln wie Ausdrücke in C++ ausgewertet.
-   Ausdrücke müssen einen ganzzahligen Typ aufweisen und können nur ganzzahlige Konstanten und Zeichenkonstanten und den defined -Operator umfassen.
-   Ausdrücke können **sizeof** oder einen Typcastoperator nicht verwenden.
-   Die Zielumgebung ist möglicherweise nicht in der Lage, alle Bereiche von ganzen Zahlen darzustellen.
-   Die Übersetzung stellt den Typ [**int**](/windows/desktop/WinProg/windows-data-types) wie den Typ **long** und [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) den gleichen typ wie **unsigned long** dar.
-   Das Konvertierungsprogramm kann Zeichenkonstanten in einen Satz von Codewerten übersetzen, die sich vom Satz für die Zielumgebung unterscheiden. Um die Eigenschaften der Zielumgebung zu bestimmen, überprüfen Sie die Werte der Makros von LIMITS.H in einer für die Zielumgebung erstellten Anwendung.
-   Der Ausdruck darf keine Umgebungsabfragen durchführen und muss von Implementierungsdetails auf dem Zielcomputer isoliert bleiben.

## <a name="examples"></a>Beispiele

Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie Präprozessordirektiven für die bedingte Kompilierung verwendet werden.

### <a name="use-of-the-defined-operator"></a>Verwendung des definierten Operators

Das folgende Beispiel zeigt die Verwendung des definierten Operators. Wenn der Bezeichner CREDIT definiert ist, wird der Aufruf der **Credit-Funktion** kompiliert. Wenn der Bezeichner DEBIT definiert ist, wird der Aufruf der **Debitfunktion** kompiliert. Wenn keiner der Bezeichner definiert ist, wird der Aufruf der **printerror-Funktion** kompiliert. Beachten Sie, dass "CREDIT" und "credit" unterschiedliche Bezeichner in C und C++ sind, da ihre Fälle unterschiedlich sind.


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>Verwenden von geschachtelten \# if-Anweisungen

Das folgende Beispiel zeigt, wie if-Anweisungen geschachtelt \# werden. In diesem Beispiel wird davon ausgegangen, dass zuvor eine symbolische Konstante namens DLEVEL definiert wurde. Die \# Elif- und \# else-Direktiven werden verwendet, um basierend auf dem Wert von DLEVEL eine von vier Optionen zu treffen. Die Konstante STACK ist abhängig von der Definition von DLEVEL auf 0, 100 oder 200 festgelegt. Wenn DLEVEL größer als 5 ist, ist STACK nicht definiert.


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a>Verwenden zum Einschließen von Headerdateien

Eine übliche Verwendung für die bedingte Kompilierung besteht darin, mehrere Inklusionen derselben Headerdatei zu verhindern. In C++, wo Klassen häufig in Headerdateien definiert werden, können Konstrukte für die bedingte Kompilierung verwendet werden, um mehrere Definitionen zu verhindern. Im folgenden Beispiel wird bestimmt, ob die symbolische Konstante EXAMPLE \_ H definiert ist. Wenn ja, wurde die Datei bereits eingeschlossen und muss nicht erneut verarbeitet werden. Andernfalls wird die Konstante EXAMPLE \_ H definiert, um dieses BEISPIEL anzugeben. H wurde bereits verarbeitet.


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

