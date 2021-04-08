---
description: 'Wenn die setupcommitfilequeue-Funktion einen Commit für die Datei Warteschlange ausführt, werden die Datei Vorgänge in der folgenden Reihenfolge verarbeitet: Datei Löschvorgänge, Datei Umbenennungs Vorgänge und schließlich Datei Kopiervorgänge.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Reihenfolge der Warteschlangen Verpflichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865716"
---
# <a name="order-of-queue-commitment"></a>Reihenfolge der Warteschlangen Verpflichtung

Wenn die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion einen Commit für die Datei Warteschlange ausführt, werden die Datei Vorgänge in der folgenden Reihenfolge verarbeitet: Datei Löschvorgänge, Datei Umbenennungs Vorgänge und schließlich Datei Kopiervorgänge. Die folgende Gliederung zeigt den Lebenszyklus des Verpflichtungs Prozesses einer Warteschlange.

 

-   unter Warteschlange löschen starten
    -   Vorgang zum Löschen einer Datei starten <--Wiederholung für jeden
    -   beendet einen Datei Löschvorgang < Datei Löschung in der Warteschlange.
-   Fertigstellen der unter Warteschlange löschen

<!-- -->

-   unter Warteschlange umbenennen starten
    -   startet einen Vorgang zum Umbenennen von Dateien <--Wiederholung für jeden
    -   beendet einen Datei Löschvorgang < Datei umbenennen in der Warteschlange.
-   Schließen Sie die unter Warteschlange Rename

<!-- -->

-   Kopieren der subque
    -   Starten eines Datei Kopiervorgangs <--Wiederholung für jeden
    -   beendet einen Datei Kopiervorgang < Datei Kopiervorgang in der Warteschlange.
    -   Kopieren der unter Warteschlange
-   Fertigstellen der Warteschlange

 

Bei jedem Schritt oder wenn ein Fehler auftritt, sendet die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion eine Benachrichtigung an die Rückruf Routine. Die Rückruf Routine kann die von der Warteschlange gesendeten Informationen verwenden, um den Installationsfortschritt zu verfolgen und ggf. mit dem Benutzer zu interagieren.

Wenn z. b. für einen Datei Kopiervorgang eine Quelldatei erforderlich ist, die im aktuellen Pfad nicht verfügbar war, sendet [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) eine spfilenotify- \_ needmedia-Benachrichtigung an die Rückruf Routine sowie Informationen über die erforderliche Datei und das erforderliche Medium. Die Rückruf Routine könnte diese Informationen verwenden, um ein Dialogfeld zu generieren, das den Benutzer auffordert, den nächsten Datenträger durch Aufrufen von [ **setuppromptfordisk** einzufügen.](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)

Die Setup-API enthält eine standardmäßige Warteschlangen Rückruf Routine, [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka). Diese Routine verarbeitet Warteschlangen Benachrichtigungen und generiert Fehler Dialogfelder und Status anzeigen für die Installation. Sie können die standardmäßige Warteschlangen Rückruf Routine verwenden, oder Sie können eine Filter Rückruf Routine schreiben, um eine Teilmenge der Benachrichtigungen zu verarbeiten und die anderen an die standardmäßige Warteschlangen Rückruf Routine zu übergeben.

Wenn keine der Funktionen der Rückruf Routine Ihren Anforderungen entspricht, können Sie eine eigenständige benutzerdefinierte Rückruf Routine schreiben, die nicht die standardmäßige Warteschlangen Rückruf Routine aufruft.

Weitere Informationen zu Warteschlangen Rückruf Routinen finden Sie unter [Standard Warteschlangen-Rückruf Routine](default-queue-callback-routine.md)und [Erstellen einer benutzerdefinierten Warteschlangen Rückruf-Routine](creating-a-custom-queue-callback-routine.md).

 

 



