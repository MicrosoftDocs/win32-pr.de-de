---
title: Umgang mit Definitionen in IDL-Dateien
description: Auf dieser Seite wird beschrieben, warum Symbole, die mit "\ define" definiert sind, aus den von dem Mittelwert generierten H-Dateien verschwinden und welche Aktionen damit durchgeführt werden können. Diese Erläuterung gilt für alle Dateien, die von der mittleren l verarbeitet werden, z. b. \. idl, \. ACF, \. h-Dateien.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- Mittlerer l-compilermittell, Umgang mit Definitionen
- definiert die mittlere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036918"
---
# <a name="dealing-with-defines-in-idl-files"></a>Umgang mit \# Definitionen in IDL-Dateien

Auf dieser Seite wird beschrieben, warum Symbole, die mit einer **\# Definition** definiert sind, aus den von dem Mittelwert generierten H-Dateien verschwinden und welche Aktionen damit durchgeführt werden können. Diese Erläuterung gilt für alle Dateien, die von der mittleren l verarbeitet werden, z. b. \* IDL-, \* ACF-und \* h-Dateien.

Das Verschwinden von **\# definierenden** Symbolen ist das Ergebnis der Mittell, die die Vorverarbeitung von Eingabedateien an einen Präprozessor delegiert. Standardmäßig ist der Präprozessor ein C/C++-Präprozessor aus der Buildumgebung. Nach der Vorverarbeitung weist der Eingabestream-Mittell-Empfang nur \# Zeilen Präprozessordirektiven auf. Insbesondere wird der Präprozessor alle Makro Definitionen in Eingabedateien aufhebt, sodass die Anwesenheit von der mittleren l nicht erkannt werden kann. Folglich werden die Definitionen nicht repliziert, wenn die-Klasse Typdefinitionen aus einer Eingabedatei in die generierte H-Datei repliziert \# . Verwenden Sie daher keine \# direkt in IDL-Dateien definierten Definitionen, wenn diese später aus der generierten H-Datei verwendet werden sollen.

Die folgenden vier Problem Umgehungen werden empfohlen:

-   Verwenden Sie [**die Konstante**](const.md) Deklaration.
-   Verwenden Sie separate Header Dateien, die importiert oder in die IDL-Datei eingeschlossen werden und später in den C-Quellcode eingefügt werden.
-   Verwenden Sie Enumerationskonstanten in der IDL-Datei.
-   Verwenden Sie das [**cpp- \_ Zitat**](cpp-quote.md) , um die **\# Definition** in der generierten Header Datei zu reproduzieren.

Sie können manifestresskonstanten mithilfe der **IDL-Konstante Deklaration** reproduzieren. Beachten Sie, dass die [**Konstante in der**](const.md) IDL-Konstantendeklaration von der C **/C++-Konstanten** Semantik abweicht und einfach eine benannte Konstante für eine IDL-Kompilierung einführt. Beispiel:

``` syntax
const short ARRSIZE = 10
```

In diesem Beispiel wird angegeben, dass " **arrsize** " eine Konstante mit dem Wert "10" ist. Benannte Konstanten können in IDL-Array Deklaratoren und an anderen Stellen verwendet werden, an denen ein C-Programmierer ein Manifest definiert. Außerdem führt diese Syntax dazu, dass die folgende Zeile in der Header Datei generiert wird:

``` syntax
#define ARRSIZE 10
```

Eine andere Möglichkeit zur Behandlung von **\#** define-Anweisungen besteht darin, Sie in einer separaten Header Datei zu packen, entweder in einer Datei, **\#** die zum Definieren von Anweisungen oder in einer Datei mit nur Typdefinitionen verwendet wird. Eine Datei, die nur Präprozessordirektiven enthält, kann sowohl von der IDL-Datei als auch von den C-Quelldateien sicher eingeschlossen werden. Obwohl die-Direktiven nicht in der vom Mittel l-Compiler generierten Header Datei verfügbar sind, kann das C-Source-Programm die separate Header Datei enthalten. Auf ähnliche Weise kann eine Header Datei mit **\#** define-Anweisungen und regulären Typdefinitionen aus der IDL-Datei importiert werden. Bei diesem Ansatz werden die **\#** define-und typedef-Anweisungen in einer H-Datei eingeschlossen, sodass die **\#** definierenden Symbole nicht direkt in der importierten IDL-Datei verwendet werden. Durch das Importieren einer Header-oder IDL-Datei in eine andere IDL-Datei wird verhindert, dass die typedef-Anweisungen in die von "Mittel l" generierte H-Datei repliziert werden (im Gegensatz zu **\#** include-Anweisungen). Dieser Ansatz ermöglicht, dass die ursprüngliche Header Datei auf sichere Weise aus dem C-Code entlang der generierten H-Datei referenziert werden kann, ohne dass ein Problem mit duplizierten Definitionen vorliegt.

Die Verwendung von Enumerationskonstanten in der IDL-Datei ist ebenfalls effektiv. Diese Konstanten können in konstanten Ausdrücken in IDL verwendet werden, z. b. in arraydeklaratoren. Enumerationskonstanten werden in den frühen Phasen der mittleren Kompilierung durch den C-Compiler-Präprozessor nicht entfernt, sodass Enumerationskonstanten in der vom Mittelwert Compiler generierten Header Datei verfügbar sind. Betrachten Sie folgende Anweisung:

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

Diese Anweisung wird nicht während der Kompilierungs Kompilierung durch den C-Präprozessor entfernt, und die typedef wird in die generierte H-Datei repliziert. Die Konstante maxstringcount ist für C-Quell Programme verfügbar, die die vom Mittelwert Compiler generierte Header Datei enthalten.

Schließlich kann die [**cpp- \_ Zitat**](cpp-quote.md) Anweisung von "Mittel l" verwendet werden, um eine beliebige Zeichenfolge direkt in die generierte H-Datei zu schreiben. Um beispielsweise die Manifestressource zu erhalten, die zuvor auf dieser Seite mit **cpp- \_ Anführungs** Zeichen verwendet wurde, kann die folgende Anweisung verwendet werden:

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

Diese Anweisung führt dazu, dass die folgende Zeile in der Header Datei generiert wird:

``` syntax
#define ARRSIZE 10
```

 

 




