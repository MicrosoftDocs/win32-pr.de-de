---
description: Wie ein Ausschneidebereich ist ein Clippfad ein weiteres Grafikobjekt, das eine Anwendung in einem Gerätekontext auswählen kann.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Clippfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91e77e3867951d09f464393fde6b416b9319f9ab914bcc393448d2b01a1eb24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038148"
---
# <a name="clip-paths"></a>Clippfade

Wie ein Ausschneidebereich ist ein Clippfad ein weiteres Grafikobjekt, das eine Anwendung in einem Gerätekontext auswählen kann. Im Gegensatz zu einem Ausschneidebereich wird ein Clippfad immer von einer Anwendung erstellt und zum Abschneiden auf eine oder mehrere unregelmäßige Formen verwendet. Beispielsweise kann eine Anwendung die Linien und Kurven verwenden, die die Konturen von Zeichen in einer Textzeichenfolge bilden, um einen Clippfad zu definieren.

Um einen Clippfad zu erstellen, müssen Sie zunächst einen Pfad erstellen, der die erforderliche unregelmäßige Form beschreibt. Pfade werden erstellt, indem die entsprechenden GDI-Zeichenfunktionen (Graphics Device Interface) nach dem Aufruf der [**BeginPath-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) und vor dem Aufruf der [**EndPath-Funktion aufruft**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) werden. Diese Auflistung von Funktionen wird als Pfadklammer bezeichnet. Weitere Informationen zu Pfaden und Pfadklammern finden Sie unter [Pfade](paths.md).

Nachdem der Pfad erstellt wurde, kann er durch Aufrufen der [**SelectClipPath-Funktion,**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) Identifizieren eines Gerätekontexts und Angeben eines Verwendungsmodus in einen Clippfad konvertiert werden. Der Verwendungsmodus bestimmt, wie das System den neuen Clippfad mit dem ursprünglichen Ausschneidebereich des Gerätekontexts kombiniert. In der folgenden Tabelle werden die Verwendungsmodi beschrieben.



| Mode      | BESCHREIBUNG                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| RGN \_ UND  | Der Clippfad enthält die Schnittmenge (überlappende Bereiche) des Ausschneidebereichs des Gerätekontexts und den aktuellen Pfad.    |
| RGN \_ COPY | Der Clippfad ist der aktuelle Pfad.                                                                                           |
| RGN \_ DIFF | Der Clippfad schließt den Ausschneidebereich des Gerätekontexts mit allen sich überschneidenden Teilen des aktuellen Pfads ein.        |
| RGN \_ ODER   | Der Clippfad enthält die Vereinigung (kombinierte Bereiche) des Ausschneidebereichs des Gerätekontexts und den aktuellen Pfad.              |
| RGN \_ XOR  | Der Clippfad enthält die Vereinigung des Ausschneidebereichs des Gerätekontexts und des aktuellen Pfads, schließt jedoch die Schnittmenge aus. |



 

 

 



