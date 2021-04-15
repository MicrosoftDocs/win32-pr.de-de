---
title: Befehlsmeldungen
description: Befehlsmeldungen
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- MCI-Befehls Meldungen, Informationen zu
- MCI-Befehls Meldungen, Syntax
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516715"
---
# <a name="command-messages"></a>Befehlsmeldungen

Die befehlsnachrichten Schnittstelle ist so konzipiert, dass Sie von Anwendungen verwendet wird, die eine Programmierschnittstelle in C-Sprache zum Steuern von Multimedia-Geräten benötigen. Es verwendet ein Nachrichten Übergabe Paradigma für die Kommunikation mit MCI-Geräten. Sie können einen Befehl mit der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion senden.

Die **mciSendCommand** -Funktion gibt bei Erfolg 0 zurück. Wenn die Funktion fehlschlägt, enthält das nieder wertige Wort des Rückgabewerts einen Fehlercode. Sie können diesen Fehlercode an die [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85)) -Funktion übergeben, um eine Textbeschreibung des Fehlers zu erhalten.

## <a name="syntax-of-command-messages"></a>Syntax von Befehls Meldungen

MCI-befehlsnachrichten bestehen aus den folgenden Elementen:

-   Ein konstanter Nachrichtenwert
-   Eine-Struktur, die Parameter für den Befehl enthält.
-   Ein Satz von Flags, die Optionen für den Befehl angeben und Felder im Parameter Block validieren.

Im folgenden Beispiel wird die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion verwendet, um den [**MCI- \_ Wiedergabe**](mci-play.md) Befehl an das Gerät zu senden, das durch einen Geräte Bezeichner identifiziert wird.


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



Der im ersten Parameter angegebene Geräte Bezeichner wird abgerufen, wenn das Gerät mit dem [**MCI-Befehl \_ Öffnen**](mci-open.md) geöffnet wird. Der letzte Parameter ist die Adresse einer [**MCI- \_ Wiedergabe \_**](mci-play-parms.md) -Parameter-Struktur, die möglicherweise Informationen darüber enthält, wo die Wiedergabe begonnen und beendet werden soll. Viele MCI-befehlsnachrichten verwenden eine-Struktur, um Parameter dieser Art zu enthalten. Der erste Member jeder dieser Strukturen gibt das Fenster an, das eine [**mm- \_ mcinotify**](mm-mcinotify.md) -Meldung empfängt, wenn der Vorgang abgeschlossen ist.

 

 