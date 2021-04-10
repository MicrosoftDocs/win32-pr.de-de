---
title: Unterschiede zwischen "Mittel l" und "MkTypLib"
description: Unterschiede zwischen "Mittel l" und "MkTypLib"
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- Mittel l-und ODL-Mittell, Unterschiede zwischen der mittleren und der MkTypLib
- MkTypLib-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037603"
---
# <a name="differences-between-midl-and-mktyplib"></a>Unterschiede zwischen "Mittel l" und "MkTypLib"

> [!Note]  
> Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den Mittel l-Compiler.

 

Es gibt einige wichtige Bereiche, in denen der mittlerer l-Compiler von MkTypLib abweicht. Die meisten dieser Unterschiede treten auf, weil die mittlere Anzahl eher an die C-Syntax gerichtet ist als auf MkTypLib.

Im Allgemeinen empfiehlt es sich, die Syntax Syntax in ihren IDL-Dateien zu verwenden. Wenn Sie jedoch eine vorhandene ODL-Datei kompilieren oder auf andere Weise die Kompatibilität mit MkTypLib beibehalten müssen, verwenden Sie die compiler2,03 Mkktyplib.exe Option [**/mktyplib203**](-mktyplib203.md) . (Dies ist die letzte Version des MkTypLib-Tools.) Die Option **/mktyplib203** löst die folgenden Unterschiede aus:

-   typedef-Syntax für komplexe Datentypen

    In MkTypLib generieren beide der folgenden Definitionen einen tkind- \_ Datensatz für "This \_ struct" in der Typbibliothek. Das Tag "struct \_ Tag" ist optional und wird, falls verwendet, nicht in der Typbibliothek angezeigt.

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    Wenn ein optionales Tag fehlt, wird es von der Mittell generiert, wodurch der vom Benutzer bereitgestellten Definition ein Tag hinzugefügt wird. Da die erste Definition über ein Tag verfügt, generiert die mittlere l einen tkind \_ -Datensatz für "This \_ struct" und einen tkind- \_ Alias für "This \_ struct" ("This \_ struct" als Alias für "struct \_ Tag"). Da das-Tag in der zweiten Definition fehlt, generiert die Mittel-l einen tkind \_ -Datensatz für einen geschilderten Namen, der für den Benutzer und einen tkind- \_ Alias für "This struct" nicht aussagekräftig ist \_ .

    Dies hat potenzielle Auswirkungen auf Typbibliotheks Browser, die einfach den Namen eines Datensatzes in der Benutzeroberfläche anzeigen. Wenn Sie davon ausgehen, dass ein tkind- \_ Datensatz einen echten Namen hat, können nicht erkennbare Namen in der Benutzeroberfläche angezeigt werden. Dieses Verhalten gilt auch für [**Union**](union.md) -und [**Enumeration**](enum.md) -Definitionen, mit dem Mittelwert Compiler, der tkind \_ Unions \_ bzw. tkind-enums erzeugt.

    In der mittleren l sind auch [**Struktur**](struct.md)-, [**Union**](union.md) [**-und**](enum.md) Enumerationsdefinitionen im C-Stil zulässig. Beispielsweise ist die folgende Definition in der Mitte gültig:

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   Boolean-Datentypen

    In MkTypLib entsprechen der [**boolesche**](boolean.md) Basistyp und der MkTypLib-Datentyp bool dem Wert VT \_ bool, der Variant \_ bool zugeordnet und als [**kurz**](short.md)definiert ist. In der mittleren l entspricht der **boolesche** Basistyp VT \_ UI1, der als [**Ganzzahl ohne Vorzeichen char**](unsigned.md)definiert ist, und der boolesche Datentyp ist als [**Long**](long.md)definiert. Dies führt zu Problemen, wenn Sie die IDL-Syntax und die ODL-Syntax in derselben Datei mischen, während Sie trotzdem versuchen, die Kompatibilität mit MkTypLib aufrechtzuerhalten. Da die Datentypen unterschiedlich groß sind, entspricht der Marshallingcode nicht den Informationen, die in den Typinformationen beschrieben werden. Wenn Sie \_ in ihrer Typbibliothek einen VT-booleschen Wert verwenden möchten, sollten Sie den \_ Datentyp Variant bool verwenden.

-   GUID-Definitionen in Header Dateien

    In MkTypLib werden GUIDs in der Header Datei mit einem Makro definiert, das bedingt kompiliert werden kann, um entweder eine GUID-prädefinition oder eine instanziierte GUID zu generieren. In der Regel werden GUID-prädefinitionen in den generierten Header Dateien und GUID-Instanziierungen nur in der vom [**/IID**](-iid.md) -Schalter generierten Datei abgelegt.

Die folgenden Unterschiede im Verhalten können nicht mithilfe des [**/mktyplib203**](-mktyplib203.md) -Schalters aufgelöst werden:

-   Groß- und Kleinschreibung

    Bei der Groß-/Kleinschreibung wird die Groß-/Kleinschreibung beachtet.

-   Bereich von Symbolen in einer Aufzählungs Deklaration

    In MkTypLib ist der Gültigkeitsbereich von Symbolen in einer Aufzählung lokal. In der mittleren l ist der Gültigkeitsbereich von Symbolen in einer-Aufzählung Global, wie er in C ist. Der folgende Code wird z. b. in MkTypLib kompiliert, generiert jedoch einen doppelten Namensfehler in der mittleren l:

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   Bereich des öffentlichen Attributs

    Wenn Sie das [**Public**](public.md) -Attribut auf einen Schnittstellen Block anwenden, behandelt MkTypLib jede typedef in diesem Schnittstellen Block als Public. Bei der mittleren l ist es erforderlich, dass Sie das **öffentliche** Attribut explizit auf die Typedefs anwenden, die öffentlich sein sollen.

-   Importlib-Such Reihenfolge

    Wenn Sie mehr als eine Typbibliothek importieren und diese Bibliotheken doppelte Verweise enthalten, löst MkTypLib dies mithilfe des ersten gefundenen Verweises auf. In der Mitte wird der letzte Verweis verwendet, den er findet. Mit der folgenden ODL-Syntax verwendet Library C z. b. die MOO-typedef von Bibliothek A, wenn Sie mit MkTypLib kompilieren, und die MOO-Typdefinition aus Bibliothek B, wenn Sie mit der mittleren l kompilieren:

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

    Die entsprechende Problem Umgehung hierfür besteht darin, jeden Verweis auf diesen Verweis mit dem richtigen Import Bibliotheksnamen zu qualifizieren, wie im folgenden Beispiel:

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   VOID-Datentyp wurde nicht erkannt.

    Der Datentyp " [**void**](void.md) " der C-Sprache wird von der mittleren l erkannt, und der Datentyp "OLE Automation void" wird nicht erkannt Wenn Sie über eine ODL-Datei verfügen, die void verwendet, platzieren Sie diese Definition am Anfang der Datei:

    ``` syntax
#define VOID void
    ```

-   Exponentialschreibweise

    Die in der Exponentialnotation ausgedrückte Werte müssen in Anführungszeichen enthalten sein. Beispiel: "-2.5 e + 3"

-   LCID-Werte und-Konstanten

    Normalerweise wird die LCID beim Auswerten von Dateien in der Mitte nicht berücksichtigt. Um dieses Verhalten für einen Wert zu erzwingen, oder wenn Sie beim Definieren einer Konstante eine Gebiets Schema spezifische Notation verwenden müssen, müssen Sie den Wert oder die Konstante in Anführungszeichen einschließen.

Weitere Informationen finden Sie unter [**/mktyplib203**](-mktyplib203.md), [**/IID**](-iid.md)und Marshalling von [OLE-Datentypen](marshaling-ole-data-types.md).

 

 




