---
title: Typdefinitionen, Konstruktdeklarationen und Importe
description: Typdefinitionen, Konstruktdeklarationen und Importe können außerhalb des Schnittstellentexts erfolgen.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- Schnittstellen MIDL , Typdefinitionen
- Schnittstellen MIDL , Konstruktdeklarationen
- Schnittstellen MIDL , Importe
- Typdefinitionen MIDL
- MIDL-Konstruktdeklarationen
- importiert MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1f80bca0a5d03ea0e935b05f973a6370c4180c9ce5c0fe7dea5d8f5c9c7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829220"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>Typdefinitionen, Konstruktdeklarationen und Importe

Typdefinitionen, Konstruktdeklarationen und Importe können außerhalb des Schnittstellentexts erfolgen. Alle Definitionen aus der IDL-Hauptdatei werden in der generierten Headerdatei angezeigt, und alle Prozeduren von allen Schnittstellen in der IDL-Hauptdatei generieren Stubroutinen. Dadurch können Anwendungen, die mehrere Schnittstellen unterstützen, IDL-Dateien in einer einzelnen, kombinierten IDL-Datei zusammenführen.

Daher ist weniger Zeit zum Kompilieren der Dateien erforderlich, und MIDL kann redundanzen in den generierten Stubs reduzieren. Dies kann [**Objektschnittstellen**](object.md) erheblich verbessern, indem sie gemeinsamen Code für Basisschnittstellen und abgeleitete Schnittstellen freigeben können. Bei **Nicht-Objektschnittstellen** müssen die Prozedurnamen für alle Schnittstellen eindeutig sein. Bei **Objektschnittstellen** müssen die Prozedurnamen nur innerhalb einer Schnittstelle eindeutig sein. Beachten Sie, dass mehrere Schnittstellen nicht zulässig sind, wenn Sie den Schalter [**/osf**](-osf.md) verwenden.

## <a name="declarative-constructs"></a>Deklarative Konstrukte

Die Syntax für deklarative Konstrukte in der IDL-Datei ähnelt der syntax für C. MIDL unterstützt alle deklarativen Microsoft C/C++-Konstrukte mit Ausnahme der folgenden:

-   Ältere Deklaratoren im Stil, mit denen ein Deklarator ohne Typspezifizierer angegeben werden kann, z. B.:

    ``` syntax
    x (y) 
    short x (y)
    ```

-   Deklarationen mit Initialisierern (MIDL akzeptiert nur Deklarationen, die der MIDL [**const-Syntax**](const.md) entsprechen).

Das [**Importschlüsselwort**](import.md) gibt die Namen einer oder mehrerer zu importierenden IDL-Dateien an. Die Importdirektive ähnelt [](include.md) der C include-Direktive, mit der Ausnahme, dass nur Datentypen in die importierende IDL-Datei aufgenommen werden.

## <a name="constant-declaration"></a>Konstantendeklaration

Die Konstantendeklaration gibt [**boolesche**](boolean.md), integer-, character-, wide-character-, string- und **\* void* _-Konstanten an. Weitere Informationen finden Sie unter [_ *const* *](const.md).

## <a name="general-declaration"></a>Allgemeine Deklaration

Eine allgemeine Deklaration ähnelt der [**C-Typedef-Anweisung**](typedef.md) mit dem Hinzufügen von IDL-Typattributen. Mit Ausnahme des [**Modus /osf**](-osf.md) lässt der MIDL-Compiler auch eine implizite Deklaration in Form einer Variablendefinition zu.

## <a name="function-declaration"></a>Funktionsdeklaration

Der Funktionsdeklarator ist ein Sonderfall der allgemeinen Deklaration. Sie können IDL-Attribute verwenden, um das Verhalten des Funktionsrückgabetyps und der einzelnen Parameter anzugeben.

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

 

 




