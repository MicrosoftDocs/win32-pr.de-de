---
description: Der Filename-Datentyp ist eine Textzeichenfolge, die einen Dateinamen oder Ordner enthält.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Dateiname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d125a1151520fb4d3b885bd815b0a5bf58d2b00ec61581fc7773f1da1bd29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636204"
---
# <a name="filename"></a>Dateiname

Der Filename-Datentyp ist eine Textzeichenfolge, die einen Dateinamen oder Ordner enthält. Standardmäßig wird davon ausgegangen, dass für den Dateinamen die Syntax für kurze Dateinamen verwendet wird. Das heißt, der Name aus acht Zeichen, der Zeitraum (.) und die 3-zeichenfolgen-Erweiterung. Es muss immer ein kurzer Dateiname angegeben werden, da die [**SHORTFILENAMES-Eigenschaft**](shortfilenames.md) festgelegt werden kann oder das Zielvolumen für die Installation nur kurze Dateinamen unterstützt.

Um einen langen Dateinamen mit dem kurzen Dateinamen einderherzustellen, trennen Sie ihn vom kurzen Dateinamen durch eine vertikale Leiste ( \| ).

Beispielsweise sind die folgenden beiden Zeichenfolgen gültig:

-   status.txt
-   projec~1.txt\| Project Status.txt

Kurze und lange Dateinamen dürfen nicht die folgenden Zeichen enthalten:

-   Schrägstrich (/) oder ( \\ )
-   Fragezeichen (?)
-   vertikaler Balken ( \| )
-   rechte eckige Klammer (>)
-   linke eckige Klammer (<)
-   Doppelpunkt (:)
-   Sternchen ( \* )
-   Anführungszeichen (")

Darüber hinaus dürfen kurze Dateinamen nicht die folgenden Zeichen enthalten:

-   Pluszeichen (+)
-   Komma (,)
-   Semikolon (;)
-   Gleichheitszeichen (=)
-   linke eckige Klammer ( \[ )
-   rechte eckige Klammer ( \] )

Es ist kein Leerzeichen vor dem vertikalen Balkentrennzeichen () für die Syntax für kurze \| Dateinamen/lange Dateinamen zulässig. Kurze Dateinamen enthalten möglicherweise kein Leerzeichen, obwohl ein langer Dateiname möglicherweise ist. Ein Leerzeichen kann nur nach dem Trennzeichen vorhanden sein, wenn der lange Dateiname des Dateinamens mit dem Leerzeichen beginnt. Es ist keine vollständige Pfadsyntax zulässig.

> [!Note]  
> Das Format der FileName -Spalte der [MsiEmbeddedUI-Tabelle](msiembeddedui-table.md) ist mit dem Format Filename-Datentyp, mit der Ausnahme, dass das senkrechte Balkentrennzeichen () für die Syntax für kurze dateiname/long-Dateinamen nicht \| verfügbar ist.

 

 

 



