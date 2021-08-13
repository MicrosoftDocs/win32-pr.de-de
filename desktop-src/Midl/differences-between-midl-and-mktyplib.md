---
title: Unterschiede zwischen MIDL und MkTypLib
description: Unterschiede zwischen MIDL und MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL und ODL MIDL , Unterschiede zwischen MIDL und MkTypLib
- MkTypLib MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ae20e00dab492a140f48c9de683abeac04676824bd6513ccf086889b4460e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643624"
---
# <a name="differences-between-midl-and-mktyplib"></a>Unterschiede zwischen MIDL und MkTypLib

> [!Note]  
> Das Mktyplib.exe ist veraltet. Verwenden Sie stattdessen den MIDL-Compiler.

 

Es gibt einige wichtige Bereiche, in denen sich der MIDL-Compiler von MkTypLib unterscheidet. Die meisten dieser Unterschiede treten auf, da MIDL eher auf C-Syntax ausgerichtet ist als MkTypLib.

Im Allgemeinen sollten Sie die MIDL-Syntax in Ihren IDL-Dateien verwenden. Wenn Sie jedoch eine vorhandene ODL-Datei kompilieren oder auf andere Weise die Kompatibilität mit MkTypLib gewährleisten müssen, verwenden Sie die MIDL-Compileroption [**/mktyplib203,**](-mktyplib203.md) um das Verhalten von MIDL wie Mkktyplib.exe, Version 2.03, zu erzwingen. (Dies ist die letzte Version des MkTypLib-Tools.) Insbesondere die **Option /mktyplib203** löst diese Unterschiede auf:

-   typedef-Syntax für komplexe Datentypen

    In MkTypLib generieren beide der folgenden Definitionen einen TKIND \_ RECORD für "this \_ struct" in der Typbibliothek. Das Tag "struct tag" ist optional und wird bei Verwendung nicht \_ in der Typbibliothek angezeigt.

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    Wenn ein optionales Tag fehlt, generiert MIDL es und fügt der vom Benutzer bereitgestellten Definition effektiv ein Tag hinzu. Da die erste Definition über ein Tag verfügt, generiert MIDL einen TKIND RECORD für \_ "this struct" und einen \_ TKIND-ALIAS für \_ "this \_ struct" (definition "this struct" als Alias für \_ "struct \_ tag"). Da das Tag in der zweiten Definition fehlt, generiert MIDL einen TKIND RECORD für einen in MIDL internen, verfehlten Namen, der für den Benutzer nicht aussagekräftig ist, und einen \_ TKIND-ALIAS für \_ "diese \_ Struktur".

    Dies hat potenzielle Auswirkungen auf Typbibliotheksbrowser, die einfach den Namen eines Datensatzes auf ihrer Benutzeroberfläche anzeigen. Wenn Sie erwarten, dass ein TKIND RECORD einen echten Namen hat, können nicht erkennbare Namen \_ auf der Benutzeroberfläche angezeigt werden. Dieses Verhalten gilt auch für [**Union-**](union.md) und Enum-Definitionen, bei der der MIDL-Compiler TKIND-UNIONs bzw. [](enum.md) \_ TKIND-ENUMs \_ generiert.

    MIDL ermöglicht auch [**Struktur-,**](struct.md) [](union.md)Union- und [**Enumdefinitionen im C-Stil.**](enum.md) Die folgende Definition ist beispielsweise in MIDL legal:

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   Boolean-Datentypen

    In MkTypLib entspricht der [**boolesche**](boolean.md) Basistyp und der MkTypLib-Datentyp BOOL VT BOOL, der VARIANT BOOL entspricht und als kurze definiert \_ \_ [**ist.**](short.md) In MIDL entspricht der **boolesche** Basistyp VT UI1, das als zeichen ohne Vorzeichen definiert ist, und der BOOL-Datentyp wird als \_ long [**definiert.**](long.md) [](unsigned.md) Dies führt zu Schwierigkeiten, wenn Sie IDL-Syntax und ODL-Syntax in derselben Datei kombinieren, während Sie weiterhin versuchen, die Kompatibilität mit MkTypLib zu gewährleisten. Da die Datentypen unterschiedliche Größen haben, passt der Marshallingcode nicht zu dem, was in den Typinformationen beschrieben wird. Wenn Sie eine \_ VT-BOOL in Ihrer Typbibliothek verwenden möchten, sollten Sie den VARIANT \_ BOOL-Datentyp verwenden.

-   GUID-Definitionen in Headerdateien

    In MkTypLib werden GUIDs in der Headerdatei mit einem Makro definiert, das bedingt kompiliert werden kann, um entweder eine GUID-Vordefinition oder eine instanziierte GUID zu generieren. MIDL legt GUID-Vorabdefinitionen normalerweise nur in den generierten Headerdateien und GUID-Instanziierungen in der Datei ab, die vom [**Schalter /iid generiert**](-iid.md) wird.

Die folgenden Verhaltensunterschiede können nicht mithilfe des Schalters [**/mktyplib203 aufgelöst**](-mktyplib203.md) werden:

-   Groß- und Kleinschreibung

    Bei MIDL wird die Kleinschreibung beachtet, bei der OLE-Automatisierung nicht.

-   Bereich von Symbolen in einer Enum-Deklaration

    In MkTypLib ist der Gültigkeitsbereich von Symbolen in einer Enum "local". In MIDL ist der Gültigkeitsbereich von Symbolen in einer Enum global, wie er in C ist. Beispielsweise wird der folgende Code in MkTypLib kompiliert, generiert jedoch einen Fehler aufgrund doppelter Namen in MIDL:

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   Bereich des öffentlichen Attributs

    Wenn Sie das [**öffentliche Attribut**](public.md) auf einen Schnittstellenblock anwenden, behandelt MkTypLib jede Typedef innerhalb dieses Schnittstellenblocks als öffentlich. MIDL erfordert, dass Sie  das öffentliche Attribut explizit auf die Typedefs anwenden, die öffentlich sein sollten.

-   Importlib-Suchauftrag

    Wenn Sie mehrere Typbibliotheken importieren und diese Bibliotheken doppelte Verweise enthalten, löst MkTypLib dies mithilfe des ersten gefundenen Verweises auf. MIDL verwendet den letzten gefundenen Verweis. Bei der folgenden ODL-Syntax verwendet Bibliothek C beispielsweise die MOO-Typdefinition aus Bibliothek A, wenn Sie mit MkTypLib kompilieren, und die MOO-Typedef aus Bibliothek B, wenn Sie mit MIDL kompilieren:

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    Die geeignete Problemumgehung besteht in der Qualifizierung jedes solchen Verweises mit dem richtigen Importbibliotheksnamen wie dem folgenden:

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   VOID-Datentyp nicht erkannt

    MIDL erkennt den void-Datentyp [**der**](void.md) C-Sprache und den OLE Automation VOID-Datentyp nicht. Wenn Sie über eine ODL-Datei verfügen, die VOID verwendet, platzieren Sie diese Definition am Anfang der Datei:

    ``` syntax
#define VOID void
    ```

-   Exponentialschreibweise

    MIDL erfordert, dass Werte, die in exponentieller Notation ausgedrückt werden, in Anführungszeichen enthalten sind. Beispiel: "-2.5E+3"

-   LCID-Werte und -Konstanten

    Normalerweise wird die LCID bei der Analyse von Dateien von MIDL nicht verwendet. Um dieses Verhalten für einen Wert zu erzwingen, oder wenn Sie beim Definieren einer Konstante eine lokalspezifische Notation verwenden müssen, schließen Sie den Wert oder die Konstante in Anführungszeichen ein.

Weitere Informationen finden Sie unter [**/mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md)und [Marshalling OLE-Datentypen](marshaling-ole-data-types.md).

 

 




