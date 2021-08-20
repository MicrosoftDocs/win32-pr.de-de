---
title: Makros und Meldungen für MCI-Funktionen
description: Makros und Meldungen für MCI-Funktionen
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- MCI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b411c018c55254658972d3cdc21a9d721334d5e78635b38f636892e2c80797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784320"
---
# <a name="mci-functions-macros-and-messages"></a>Makros und Meldungen für MCI-Funktionen

Die meisten MCI-Anwendungen verwenden [**die Funktionen mciSendString**](/previous-versions//dd757161(v=vs.85)) und [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) dutzendfach. MCI bietet einige weitere nützliche Funktionen, die Ihre Anwendung seltener verwenden wird.

Die für die meisten MCI-Befehle erforderliche Geräte-ID [](open.md) wird in der Regel in einem Aufruf des open-Befehls [**(MCI \_ OPEN**](mci-open.md)) abgerufen. Wenn Sie eine Geräte-ID benötigen, das Gerät jedoch nicht öffnen möchten , z. B. wenn Sie die Funktionen des Geräts abfragen möchten, bevor Sie eine andere Aktion ausführen, können Sie die [**mciGetDeviceID-Funktion**](/previous-versions//dd757156(v=vs.85)) aufrufen.

Mit [**der mciGetCreatorTask-Funktion**](/previous-versions//dd757155(v=vs.85)) kann Ihre Anwendung einen Gerätebezeichner verwenden, um ein Handle für den Task abzurufen, der diesen Bezeichner erstellt hat.

Sie können die [**Funktionen mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) und [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) verwenden, um die Adresse der Rückruffunktion zu zuweisen und abzurufen, die dem Wait-Flag (MCI WAIT) zugeordnet \_ ist.

Die [**mciGetErrorString-Funktion**](/previous-versions//dd757158(v=vs.85)) ruft eine Zeichenfolge ab, die einen MCI-Fehlerwert beschreibt. Jede Zeichenfolge, die MCI zurückgibt, ob Daten oder eine Fehlerbeschreibung, ist maximal 128 Zeichen lang. Dialogfeldfelder, die kleiner als 128 Zeichen sind, schneiden die längeren Zeichenfolgen ab, die von MCI zurückgegeben werden. Weitere Informationen zu diesen Zeichenfolgen finden Sie unter [MCIERR-Rückgabewerte.](mcierr-return-values.md)

Die MCI-Makros sind Tools, mit denen Sie Werte erstellen und disassemblieren können, die Zeitformate angeben. Diese Zeitformate werden in vielen MCI-Befehlen verwendet. Die Von den Makros umgesetzten Formate sind Stunden/Minuten/Sekunden (HMS), Minuten/Sekunden/Frames (MSF) und Tracks/Minuten/Sekunden/Frames (TMSF). In der folgenden Tabelle sind die Makros und ihre Beschreibungen aufgeführt.



| Makro                                        | Beschreibung                                        |
|----------------------------------------------|----------------------------------------------------|
| [**MCI \_ HMS \_ HOUR**](mci-hms-hour.md)       | Ruft die Stundenkomponente aus einem HMS-Wert ab.   |
| [**MCI \_ HMS \_ MINUTE**](mci-hms-minute.md)   | Ruft die Minutenkomponente aus einem HMS-Wert ab. |
| [**MCI \_ HMS \_ SECOND**](mci-hms-second.md)   | Ruft die Sekundenkomponente aus einem HMS-Wert ab. |
| [**MCI \_ MAKE \_ HMS**](mci-make-hms.md)       | Erstellt einen HMS-Wert.                              |
| [**MCI \_ MAKE \_ MSF**](mci-make-msf.md)       | Erstellt einen MSF-Wert.                              |
| [**MCI \_ MAKE \_ TMSF**](mci-make-tmsf.md)     | Erstellt einen TMSF-Wert.                              |
| [**\_MCI-MSF-FRAME \_**](/previous-versions//dd743438(v=vs.85))     | Ruft die Frameskomponente aus einem MSF-Wert ab.  |
| [**MCI \_ MSF \_ MINUTE**](mci-msf-minute.md)   | Ruft die Minutenkomponente aus einem MSF-Wert ab. |
| [**MCI \_ MSF \_ SECOND**](mci-msf-second.md)   | Ruft die Sekundenkomponente aus einem MSF-Wert ab. |
| [**MCI \_ TMSF \_ FRAME**](mci-tmsf-frame.md)   | Ruft die Frameskomponente aus einem TMSF-Wert ab.  |
| [**MCI \_ TMSF \_ MINUTE**](mci-tmsf-minute.md) | Ruft die Minutenkomponente aus einem TMSF-Wert ab. |
| [**MCI \_ TMSF \_ SECOND**](mci-tmsf-second.md) | Ruft die Sekundenkomponente aus einem TMSF-Wert ab. |
| [**MCI \_ TMSF \_ TRACK**](mci-tmsf-track.md)   | Ruft die Tracks-Komponente aus einem TMSF-Wert ab.  |



 

MCI stellt außerdem zwei Nachrichten zur Verfügung: [**MM \_ MCINOTIFY**](mm-mcinotify.md) und [**MM \_ MCISIGNAL**](mm-mcisignal.md). Die MM MCINOTIFY-Nachricht benachrichtigt eine Anwendung über das Ergebnis eines MCI-Befehls, wenn dieser Befehl das \_ Flag "notify" (MCI \_ NOTIFY) angibt. Die MM \_ MCISIGNAL-Nachricht ist spezifisch für Digitalvideogeräte. Sie benachrichtigt die Anwendung, wenn eine angegebene Position erreicht wird.

 

 