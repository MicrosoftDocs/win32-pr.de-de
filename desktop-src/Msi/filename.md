---
description: Der Datentyp Dateiname ist eine Text Zeichenfolge, die einen Dateinamen oder einen Ordner enthält.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Dateiname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528190"
---
# <a name="filename"></a>Dateiname

Der Datentyp Dateiname ist eine Text Zeichenfolge, die einen Dateinamen oder einen Ordner enthält. Standardmäßig wird davon ausgegangen, dass der Dateiname eine kurze Dateiname-Syntax verwendet. Dabei handelt es sich um einen achtstelligen Namen, einen Zeitraum (.) und eine Erweiterung mit drei Zeichen. Ein kurzer Dateiname muss immer angegeben werden, da die Eigenschaft [**shortfileames**](shortfilenames.md) festgelegt werden kann oder das Zielvolume für die Installation nur kurze Dateinamen unterstützt.

Wenn Sie einen langen Dateinamen mit dem kurzen Dateinamen einschließen möchten, trennen Sie ihn vom kurzen Dateinamen mit einem senkrechten Strich ( \| ).

Die folgenden beiden Zeichen folgen sind z. b. gültig:

-   status.txt
-   PROJEC ~1.txt\| Projekt Status.txt

Kurze und lange Dateinamen dürfen die folgenden Zeichen nicht enthalten:

-   Schrägstrich (/) oder ( \\ )
-   Fragezeichen (?)
-   senkrechter Strich ( \| )
-   Rechte Spitze Klammer (>)
-   öffnende spitze Klammer (<)
-   Doppelpunkt (:)
-   Sternchen ( \* )
-   Anführungszeichen (")

Außerdem dürfen kurze Dateinamen die folgenden Zeichen nicht enthalten:

-   Pluszeichen (+)
-   Komma (,)
-   Semikolon (;)
-   Gleichheitszeichen (=)
-   linke eckige Klammer ( \[ )
-   rechte eckige Klammer ( \] )

Es ist kein Leerzeichen vor dem senkrechten Strich ( \| ) für die Syntax der kurzen Dateinamen/langen Dateinamen zulässig. Kurze Dateinamen dürfen keine Leerzeichen enthalten, obwohl ein langer Dateiname möglicherweise ist. Ein Leerzeichen kann nach dem Trennzeichen nur vorhanden sein, wenn der lange Dateiname mit dem Leerzeichen beginnt. Es ist keine vollständige Pfad Syntax zulässig.

> [!Note]  
> Das Format der Dateiname-Spalte der [msiembeddedui](msiembeddedui-table.md) -Tabelle entspricht dem Datentyp Datentyp Datentyp, mit dem Unterschied, dass das vertikale Balken \| Trennzeichen () für die Syntax kurzer Dateiname/langer Dateiname nicht verfügbar ist.

 

 

 



