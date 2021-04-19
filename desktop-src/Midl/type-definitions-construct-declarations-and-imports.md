---
title: Typdefinitionen, Konstruktordeklarationen und Importe
description: Typdefinitionen, Konstruktordeklarationen und Importe können außerhalb des Schnittstellen Texts auftreten.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- Schnittstellen-Mittell, Typdefinitionen
- Schnittstellen-Mittell, Konstruieren von Deklarationen
- Schnittstellen-Mittel l, Importe
- Typdefinitionen (Mittell)
- Konstruieren von Deklarationen in der Mitte
- importiert Mittel l
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342247"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>Typdefinitionen, Konstruktordeklarationen und Importe

Typdefinitionen, Konstruktordeklarationen und Importe können außerhalb des Schnittstellen Texts auftreten. Alle Definitionen aus der Haupt-IDL-Datei werden in der generierten Header Datei angezeigt, und alle Prozeduren aus allen Schnittstellen in der Haupt-IDL-Datei generieren stubroutinen. Dies ermöglicht es Anwendungen, die mehrere Schnittstellen unterstützen, IDL-Dateien in einer einzelnen, kombinierten IDL-Datei zusammenzuführen.

Daher ist es weniger Zeit, die Dateien zu kompilieren, und kann die Redundanz in den generierten Stubdaten auch durch die mittlere Größe verringern. Dadurch können [**Objekt**](object.md) Schnittstellen erheblich verbessert werden, indem allgemeiner Code für Basis Schnittstellen und abgeleitete Schnittstellen gemeinsam genutzt wird. Bei nicht- **Objekt** Schnittstellen müssen die Namen der Prozedur über alle Schnittstellen hinweg eindeutig sein. Bei **Objekt** Schnittstellen müssen die Namen der Prozedur nur innerhalb einer Schnittstelle eindeutig sein. Beachten Sie, dass mehrere Schnittstellen nicht zulässig sind, wenn Sie den Schalter [**/OSF**](-osf.md) verwenden.

## <a name="declarative-constructs"></a>Deklarative Konstrukte

Die Syntax für deklarative Konstrukte in der IDL-Datei ähnelt der Syntax für c. in der Mitte werden alle deklarativen Microsoft C/C++-Konstrukte unterstützt, mit Ausnahme der folgenden:

-   Ältere typdeklaratoren, die es ermöglichen, dass ein Deklarator ohne Typspezifizierer angegeben wird, z. b.:

    ``` syntax
    x (y) 
    short x (y)
    ```

-   Deklarationen mit Initialisierern (in der Mitte dürfen nur Deklarationen akzeptiert werden, die der Syntax der [**Konstanten Konstanten**](const.md) entsprechen).

Das [**Import**](import.md) -Schlüsselwort gibt die Namen von mindestens einer IDL-Datei an, die importiert werden soll. Die Import-Direktive ähnelt der C [**include**](include.md) -Direktive, mit dem Unterschied, dass nur Datentypen in die importierte IDL-Datei aufgenommen werden.

## <a name="constant-declaration"></a>Konstante Deklaration

Die Konstante Deklaration gibt [**boolesche**](boolean.md), ganzzahlige, Zeichen-, breit Zeichen-, Zeichen folgen-und **\* void** -Konstanten an. Weitere Informationen finden Sie unter [**konstant**](const.md).

## <a name="general-declaration"></a>Allgemeine Deklaration

Eine allgemeine Deklaration ähnelt der C- [**typedef**](typedef.md) -Anweisung mit dem Hinzufügen von IDL-Typattributen. Mit Ausnahme des [**/OSF**](-osf.md) -Modus ermöglicht der-Mittell-Compiler auch eine implizite Deklaration in Form einer Variablen Definition.

## <a name="function-declaration"></a>Funktionsdeklaration

Der funktionsdeklarator ist ein Sonderfall der allgemeinen Deklaration. Sie können IDL-Attribute verwenden, um das Verhalten des Funktions Rückgabe Typs und jedes Parameters anzugeben.

## <a name="examples"></a>Beispiele

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




