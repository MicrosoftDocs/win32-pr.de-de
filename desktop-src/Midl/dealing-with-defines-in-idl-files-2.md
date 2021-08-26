---
title: Umgang mit Definitionen in IDL-Dateien
description: Auf dieser Seite wird beschrieben, warum Symbole, die mit \define definiert sind, aus den vom MIDL-Compiler generierten H-Dateien nicht mehr angezeigt werden und was sie tun können. Diese Erklärung gilt für alle dateien, die von MIDL verarbeitet werden, z. B. \.idl,\ .acf, \ .h-Dateien.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL-Compiler MIDL , der mit definiert
- definiert MIDL.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c8a63423943d72326b16d53272f63d6efbe7d614661990560b00989be04cf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979701"
---
# <a name="dealing-with-defines-in-idl-files"></a>Umgang mit \# Definitionen in IDL-Dateien

Auf dieser Seite wird beschrieben, warum symbole, die mit einer Definition definiert sind, aus den vom MIDL-Compiler generierten H-Dateien nicht mehr angezeigt werden und was damit zu tun ist. **\#** Diese Erklärung gilt für alle dateien, die von MIDL verarbeitet werden, z. B. \* IDL-, \* ACF- \* und H-Dateien.

Die **\# Nichtbewegung von definierenden** Symbolen ist das Ergebnis der MIDL-Delegierung der Vorverarbeitung von Eingabedateien an einen Präprozessor. Standardmäßig ist der Präprozessor ein C/C++-Präprozessor aus der Buildumgebung. Nach der Vorverarbeitung verfügt die EINGABESTREAM-MIDL nur über \# Zeilenvorprozessordirektiven. Insbesondere entrollt der Präprozessor alle Makrodefinitionen in Eingabedateien, und daher kann MIDL deren Vorhandensein nicht erkennen. Wenn MIDL also Typdefinitionen aus einer Eingabedatei in die generierte H-Datei repliziert, werden die \# Definitionen nicht repliziert. Verwenden Sie daher definition nicht direkt in IDL-Dateien, wenn sie später aus \# der generierten H-Datei verwendet werden sollen.

Die folgenden vier Problemumgehungen werden empfohlen:

-   Verwenden [](const.md) Sie die const-Deklarationsspezifikation.
-   Verwenden Sie separate Headerdateien, die importiert oder in die IDL-Datei eingeschlossen und später im C-Quellcode enthalten sind.
-   Verwenden Sie Enumerationskonst constants in der IDL-Datei.
-   Verwenden Sie [**\_ CPP-Anführungszeichen,**](cpp-quote.md) um **\# die Definition** in der generierten Headerdatei zu reproduzieren.

Sie können Manifestkonst constants mithilfe der **Syntax der IDL-Konstantendeklaration reproduzieren.** Beachten Sie, [**dass sich const**](const.md) in der IDL-Konstantendeklaration von der konstanten C/C++-Semantik ab unterscheiden und einfach eine benannte Konstante für eine IDL-Kompilierung ein führt.  Beispiel:

``` syntax
const short ARRSIZE = 10
```

In diesem Beispiel wird angegeben, **dass ARRSIZE** eine Konstante mit dem Wert 10 ist. Benannte Konstanten können in IDL-Arraydeklaratoren und an anderen Stellen verwendet werden, an denen ein C-Programmierer ein Manifest definiert. Darüber hinaus führt diese Syntax dazu, dass die folgende Zeile in der Headerdatei generiert wird:

``` syntax
#define ARRSIZE 10
```

Eine andere Möglichkeit zum Behandeln von define-Anweisungen besteht in der Gepackt in einer separaten Headerdatei, entweder in eine Datei, die anweisungen definiert, oder in eine Datei, die nur **\#** **\#** Typdefinitionen enthält. Eine Datei, die nur Präprozessordirektiven enthält, kann sowohl in der IDL-Datei als auch in den C-Quelldateien sicher enthalten sein. Obwohl die -Anweisungen nicht in der vom MIDL-Compiler generierten Headerdatei verfügbar sind, kann das C-Quellprogramm die separate Headerdatei enthalten. Auf ähnliche Weise kann eine Headerdatei mit define-Anweisungen und regulären Typdefinitionen **\#** aus Ihrer IDL-Datei importiert werden. Dieser Ansatz kapselt die define- und typedef-Anweisungen, indem sie in einer H-Datei verwendet werden, damit die definierenden Symbole nicht direkt in der importierenden **\#** **\#** IDL-Datei verwendet werden. Durch das Importieren eines Headers oder einer IDL-Datei in eine andere IDL-Datei wird verhindert, dass die typedef-Anweisungen in die von MIDL generierte H-Datei repliziert werden (im Gegensatz zu **\#** include-Anweisungen). Bei diesem Ansatz kann aus dem C-Code entlang der generierten H-Datei sicher auf die ursprüngliche Headerdatei verwiesen werden, ohne dass ein Problem mit doppelten Definitionen besteht.

Die Verwendung von Enumerationskonst constants in der IDL-Datei ist ebenfalls wirksam. Diese Konstanten können in konstanten Ausdrücken in IDL verwendet werden, z. B. in Arraydeklaratoren. Enumerationskonstationen werden in den frühen Phasen der MIDL-Kompilierung durch den C-Compiler-Präprozessor nicht entfernt, sodass Enumerationskonstationen in der vom MIDL-Compiler generierten Headerdatei verfügbar sind. Betrachten Sie folgende Anweisung:

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

Diese Anweisung wird während der MIDL-Kompilierung durch den C-Präprozessor nicht entfernt, und die TypeDef wird in die generierte H-Datei repliziert. Die Konstante MAXSTRINGCOUNT ist für C-Quellprogramme verfügbar, die die vom MIDL-Compiler generierte Headerdatei enthalten.

Schließlich kann die [**cpp \_ quote-Direktive**](cpp-quote.md) von MIDL verwendet werden, um eine beliebige Zeichenfolge direkt in die generierte H-Datei zu schreiben. Um beispielsweise die manifest-Konstante, die zuvor auf dieser Seite verwendet wurde, mit CPP-Anführungszeichen zu erhalten, kann die folgende Anweisung verwendet werden: **\_**

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

Diese Anweisung führt dazu, dass die folgende Zeile in der Headerdatei generiert wird:

``` syntax
#define ARRSIZE 10
```

 

 




