---
title: MCI-Funktionen Makros und Meldungen
description: MCI-Funktionen Makros und Meldungen
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- MCI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade9ac3ea5c2a3c74f94bab899305cdae7ec51c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726993"
---
# <a name="mci-functions-macros-and-messages"></a>MCI-Funktionen Makros und Meldungen

Die meisten MCI-Anwendungen verwenden die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -und [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktionen Dutzende Male. MCI bietet einige weitere nützliche Funktionen, die von Ihrer Anwendung seltener verwendet werden.

Der für die meisten MCI-Befehle erforderliche Geräte Bezeichner wird in der Regel in [**einem aufgerufenen Befehl (**](open.md) [**MCI \_ Open**](mci-open.md)) abgerufen. Wenn Sie einen Geräte Bezeichner benötigen, aber das Gerät nicht öffnen möchten – beispielsweise, wenn Sie die Funktionen des Geräts Abfragen möchten, bevor Sie eine andere Aktion ausführen – können Sie die [**mcigetdeviceid**](/previous-versions//dd757156(v=vs.85)) -Funktion aufrufen.

Die [**mcigetkreatortask**](/previous-versions//dd757155(v=vs.85)) -Funktion ermöglicht der Anwendung die Verwendung eines Geräte Bezeichners zum Abrufen eines Handles für den Task, der diesen Bezeichner erstellt hat.

Sie können die Funktionen [**mcigetyieldproc**](/previous-versions//dd757159(v=vs.85)) und [**mcisetyieldproc**](/previous-versions//dd757163(v=vs.85)) zum Zuweisen und Abrufen der Adresse der Rückruffunktion verwenden, die dem Flag "wait" (MCI \_ Wait) zugeordnet ist.

Die [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85)) -Funktion Ruft eine Zeichenfolge ab, die einen MCI-Fehlerwert beschreibt. Jede von MCI zurückgegebene Zeichenfolge, ob Daten oder eine Fehlerbeschreibung, ist maximal 128 Zeichen lang. Dialog Feld Felder, die kleiner als 128 Zeichen sind, schneiden die von MCI zurückgegebenen längeren Zeichen folgen ab. Weitere Informationen zu diesen Zeichen folgen finden Sie unter [mcierr-Rückgabewerte](mcierr-return-values.md).

Die MCI-Makros sind Tools, mit denen Sie Werte zum Angeben von Zeitformaten erstellen und disassemblieren können. Diese Zeitformate werden in vielen MCI-Befehlen verwendet. Die von den Makros durchgeführten Formate sind Stunden/Minuten/Sekunden (HMS), minutes/seconds/Frames (MSF) und Tracks/Minutes/seconds/Frames (TMSF). In der folgenden Tabelle sind die Makros und ihre Beschreibungen aufgeführt.



| Makro                                        | Beschreibung                                        |
|----------------------------------------------|----------------------------------------------------|
| [**MCI-Dauer- \_ \_ Stunde**](mci-hms-hour.md)       | Ruft die Stunden Komponente von einem "HMS"-Wert ab.   |
| [**MCI- \_ HMS- \_ Minute**](mci-hms-minute.md)   | Ruft die Minuten Komponente von einem "HMS"-Wert ab. |
| [**MCI- \_ HMS- \_ Sekunde**](mci-hms-second.md)   | Ruft die Sekunden Komponente von einem "HMS"-Wert ab. |
| [**MCI \_ machen von \_ HMS**](mci-make-hms.md)       | Erstellt einen HMS-Wert.                              |
| [**MCI \_ make \_ MSF**](mci-make-msf.md)       | Erstellt einen MSF-Wert.                              |
| [**MCI \_ make \_ TMSF**](mci-make-tmsf.md)     | Erstellt einen TMSF-Wert.                              |
| [**MCI \_ MSF- \_ Frame**](/previous-versions//dd743438(v=vs.85))     | Ruft die Frames-Komponente von einem MSF-Wert ab.  |
| [**MCI \_ MSF- \_ Minute**](mci-msf-minute.md)   | Ruft die Minuten Komponente von einem MSF-Wert ab. |
| [**MCI \_ MSF ( \_ Sekunde)**](mci-msf-second.md)   | Ruft die Sekunden Komponente von einem MSF-Wert ab. |
| [**MCI \_ TMSF- \_ Frame**](mci-tmsf-frame.md)   | Ruft die Frames-Komponente von einem TMSF-Wert ab.  |
| [**MCI \_ TMSF- \_ Minute**](mci-tmsf-minute.md) | Ruft die Minuten Komponente von einem TMSF-Wert ab. |
| [**MCI \_ TMSF ( \_ Sekunde)**](mci-tmsf-second.md) | Ruft die Sekunden Komponente aus einem TMSF-Wert ab. |
| [**MCI \_ TMSF- \_ Track**](mci-tmsf-track.md)   | Ruft die Spuren Komponente aus einem TMSF-Wert ab.  |



 

MCI bietet auch zwei Nachrichten: [**mm \_ mcinotify**](mm-mcinotify.md) und [**mm \_ mcisignal**](mm-mcisignal.md). Die \_ Meldung mm mcinotify benachrichtigt eine Anwendung über das Ergebnis eines MCI-Befehls, wenn dieser Befehl das Flag "Benachrichtigen" (MCI \_ Notify) angibt. Die \_ mcisignal-Nachricht von mm ist für Digital Video-gerätespezifisch und benachrichtigt die Anwendung, wenn eine bestimmte Position erreicht ist.

 

 