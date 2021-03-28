---
title: " if-, elif-, else-und endif-Direktiven"
description: Präprozessordirektiven, die die Kompilierung von Teilen einer Quelldatei steuern.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- if-, elif-, else-und endif-Direktive HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101659"
---
# <a name="if-elif-else-and-endif-directives"></a>\#If \# -, elif \# -, else-und \# EndIf-Direktiven

Präprozessordirektiven, die die Kompilierung von Teilen einer Quelldatei steuern.



| \#Wenn *ifcondition* ...         |
|--------------------------------|
| \[\#Elif *elif Condition* ...\] |
| \[\#else...\]                 |
| \#endif                        |



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifcondition*<br/>                                                                                   | Die auszuwertende primäre Bedingung. Wenn dieser Parameter zu einem Wert ungleich 0 (null) ausgewertet wird, wird der gesamte Text zwischen dieser \# if-Direktive und der nächsten Instanz der \# elif-, \# else-oder \# endif-Direktive in der Übersetzungseinheit beibehalten. andernfalls wird der nachfolgende Quellcode nicht beibehalten. <br/> Mit der Bedingung kann der Präprozessoroperator definiert werden, um zu bestimmen, ob eine bestimmte präprozessorkonstante oder ein bestimmtes Makro definiert ist. Diese Verwendung entspricht der Verwendung der [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) -Direktive. <br/> Weitere Informationen zu den Werten des Parameters " *ifcondition* " finden Sie im Abschnitt "Hinweise". <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elif Condition* \[ optionale\] <br/> | Andere auszuwertende Bedingung. Wenn der *ifcondition* -Parameter und alle vorherigen \# elif-Direktiven NULL ergeben und dieser Parameter zu einem Wert ungleich 0 (null) ausgewertet wird, wird der gesamte Text zwischen dieser \# elif-Direktive und der nächsten Instanz der \# elif-, \# else-oder \# endif-Direktive in der Übersetzungseinheit beibehalten. andernfalls wird der nachfolgende Quellcode nicht beibehalten. <br/> Mit der Bedingung kann der Präprozessoroperator definiert werden, um zu bestimmen, ob eine bestimmte präprozessorkonstante oder ein bestimmtes Makro definiert ist. Diese Verwendung entspricht der Verwendung der [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) -Direktive. <br/> Im Abschnitt "Hinweise" finden Sie Einschränkungen für den Wert des *elilarcondition* -Parameters. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Jede \# if-Direktive in einer Quelldatei muss mit einer abschließenden \# endif-Direktive übereinstimmen. Eine beliebige Anzahl von \# elif-Direktiven kann zwischen der \# if-und der \# endif-Direktive auftreten, aber \# es ist höchstens eine Else-Direktive zulässig. Die \# else-Direktive muss, falls vorhanden, die letzte Direktive vor \# EndIf sein. Bedingte Kompilierungs Direktiven, die in include-Dateien enthalten sind, müssen die gleichen Bedingungen erfüllen.

Die \# if-, \# elif \# -, else-und \# EndIf-Direktiven können in den Textteilen anderer \# if-Direktiven geschachtelt werden. Jede geschsted \# else-, \# elif-oder \# endif-Direktive gehört der nächstgelegenen vorangehenden \# if-Direktive an.

Wenn keine Bedingungen zu einem Wert ungleich 0 (null) ausgewertet werden, wählt der Präprozessor den TextBlock nach der \# else-Direktive aus. Wenn die \# else-Klausel ausgelassen wird und keine Bedingungen zu einem Wert ungleich 0 (null) ausgewertet werden, wird kein TextBlock ausgewählt.

Die Parameter " *ifcondition* " und " *elimode Condition* " erfüllen viele der folgenden Anforderungen:

-   Ausdrücke für die bedingte Kompilierung werden als [**signierte lange**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) Werte behandelt, und diese Ausdrücke werden mit denselben Regeln wie Ausdrücke in C++ ausgewertet.
-   Ausdrücke müssen einen ganzzahligen Typ aufweisen und können nur ganzzahlige Konstanten und Zeichenkonstanten und den defined -Operator umfassen.
-   Ausdrücke können nicht **sizeof** oder einen Typumwandlungs Operator verwenden.
-   Die Zielumgebung ist möglicherweise nicht in der Lage, alle Bereiche von ganzen Zahlen darzustellen.
-   Die Übersetzung stellt den Typ " [**int**](/windows/desktop/WinProg/windows-data-types) " mit dem Typ " **Long**" und " [**Ganzzahl ohne Vorzeichen int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) " gleich " **Ganzzahl ohne Vorzeichen long**" dar.
-   Das Konvertierungsprogramm kann Zeichenkonstanten in einen Satz von Codewerten übersetzen, die sich vom Satz für die Zielumgebung unterscheiden. Um die Eigenschaften der Zielumgebung zu bestimmen, überprüfen Sie die Werte der Makros von LIMITS.H in einer für die Zielumgebung erstellten Anwendung.
-   Der Ausdruck darf keine Umgebungsabfragen durchführen und muss von Implementierungsdetails auf dem Zielcomputer isoliert bleiben.

## <a name="examples"></a>Beispiele

Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie Präprozessordirektiven für die bedingte Kompilierung verwendet werden.

### <a name="use-of-the-defined-operator"></a>Verwendung des definierten Operators

Das folgende Beispiel zeigt die Verwendung des definierten-Operators. Wenn das bezeichnerguthaben definiert ist, wird der-Befehl der **Credit** -Funktion kompiliert. Wenn der bezeichnerkennung definiert ist, wird der aufrufswert der **debitfunktion** kompiliert. Wenn kein Bezeichner definiert ist, wird der-Befehl der **Printerror** -Funktion kompiliert. Beachten Sie, dass "Guthaben" und "Guthaben" unterschiedliche Bezeichner in C und C++ sind, da sich ihre Fälle unterscheiden.


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>Verwendung von nsted \# if-Direktiven

Das folgende Beispiel zeigt, wie if-Direktiven geschachtelt \# werden. In diesem Beispiel wird davon ausgegangen, dass bereits eine symbolische Konstante mit dem Namen "DLEVEL" definiert wurde. Die \# elif-und \# else-Direktiven werden verwendet, um eine von vier Optionen basierend auf dem Wert von DLEVEL zu treffen. Der Konstante Stapel ist abhängig von der Definition von DLEVEL auf 0, 100 oder 200 festgelegt. Wenn DLEVEL größer als 5 ist, wird der Stapel nicht definiert.


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



### <a name="use-for-including-header-files"></a>Verwenden zum Einschließen von Header Dateien

Eine übliche Verwendung für die bedingte Kompilierung besteht darin, mehrere Inklusionen derselben Headerdatei zu verhindern. In C++, in denen Klassen häufig in Header Dateien definiert werden, können Konstrukte für die bedingte Kompilierung verwendet werden, um mehrere Definitionen zu verhindern. Im folgenden Beispiel wird bestimmt, ob das symbolische Konstante Beispiel \_ H definiert ist. Wenn dies der Fall ist, wurde die Datei bereits eingeschlossen und muss nicht erneut verarbeitet werden. Wenn dies nicht der Wert ist, wird das Konstante Beispiel \_ H definiert, um das Beispiel anzuzeigen. H wurde bereits verarbeitet.


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

 

