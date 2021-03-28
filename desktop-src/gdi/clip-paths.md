---
description: Wie bei einem Clippingbereich ist ein Clip Pfad ein weiteres Grafik Objekt, das von einer Anwendung in einen Gerätekontext ausgewählt werden kann.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Clip Pfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978769"
---
# <a name="clip-paths"></a>Clip Pfade

Wie bei einem Clippingbereich ist ein Clip Pfad ein weiteres Grafik Objekt, das von einer Anwendung in einen Gerätekontext ausgewählt werden kann. Anders als bei einem Clippingbereich wird ein Clip Pfad immer von einer Anwendung erstellt und für das Clipping auf eine oder mehrere unregelmäßige Formen verwendet. Beispielsweise kann eine Anwendung die Linien und Kurven verwenden, die die Darstellung von Zeichen in einer Text Zeichenfolge bilden, um einen Clip Pfad zu definieren.

Zum Erstellen eines Clip Pfades muss zunächst ein Pfad erstellt werden, der die erforderliche unregelmäßige Form beschreibt. Pfade werden erstellt, indem nach dem Aufrufen der [**beginpath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) -Funktion und vor dem Aufrufen der [**endpath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) -Funktion die entsprechenden GDI-Zeichnungsfunktionen (Graphics Device Interface) aufgerufen werden. Diese Auflistung von Funktionen wird als Pfad Klammer bezeichnet. Weitere Informationen zu Pfaden und Pfad Klammern finden Sie unter [Pfade](paths.md).

Nachdem der Pfad erstellt wurde, kann er in einen Clip Pfad konvertiert werden, indem die [**selectclippath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) -Funktion aufgerufen, ein Gerätekontext identifiziert und ein Verwendungs Modus angegeben wird. Der Verwendungs Modus bestimmt, wie das System den neuen Clip Pfad mit dem ursprünglichen Clippingbereich des Geräte Kontexts kombiniert. In der folgenden Tabelle werden die Verwendungs Modi beschrieben.



| Mode      | BESCHREIBUNG                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| RGN \_ und  | Der Clip Pfad enthält die Schnittmenge (überlappende Bereiche) des Clippingbereichs des Geräte Kontexts und den aktuellen Pfad.    |
| RGN- \_ Kopie | Der Clip Pfad ist der aktuelle Pfad.                                                                                           |
| RGN- \_ diff | Der Clip Pfad schließt den Clippingbereich des Geräte Kontexts ein, der überschneidende Teile des aktuellen Pfads ausgeschlossen ist.        |
| RGN \_ oder   | Der Clip Pfad enthält die Union (kombinierte Bereiche) des Clippingbereichs des Geräte Kontexts und den aktuellen Pfad.              |
| RGN- \_ Xor  | Der Clip Pfad umfasst die Vereinigung des Clippingbereichs des Geräte Kontexts und des aktuellen Pfads, schließt jedoch die Schnittmenge aus. |



 

 

 



