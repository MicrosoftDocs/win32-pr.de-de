---
title: Befehlsmeldungen
description: Befehlsmeldungen
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- MCI-Befehlsmeldungen, Informationen
- MCI-Befehlsmeldungen, Syntax
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428c89f610f204cfeb75a6c23309c8f3f9846d3136ffac4dbcf0959c5bc4add3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807940"
---
# <a name="command-messages"></a>Befehlsmeldungen

Die Befehlsmeldungsschnittstelle ist für anwendungen konzipiert, die eine C-Sprachschnittstelle zum Steuern von Multimediageräten benötigen. Es verwendet ein Nachrichtenübergabeparadigma für die Kommunikation mit MCI-Geräten. Sie können einen Befehl mithilfe der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) senden.

Die **mciSendCommand-Funktion** gibt bei Erfolg 0 (null) zurück. Wenn die Funktion fehlschlägt, enthält das Wort mit niedriger Reihenfolge des Rückgabewerts einen Fehlercode. Sie können diesen Fehlercode an die [**mciGetErrorString-Funktion**](/previous-versions//dd757158(v=vs.85)) übergeben, um eine Textbeschreibung des Fehlers abzurufen.

## <a name="syntax-of-command-messages"></a>Syntax von Befehlsmeldungen

MCI-Befehlsmeldungen bestehen aus den folgenden Elementen:

-   Ein konstanter Nachrichtenwert
-   Eine -Struktur mit Parametern für den Befehl
-   Eine Gruppe von Flags, die Optionen für den Befehl und das Überprüfen von Feldern im Parameterblock angeben

Im folgenden Beispiel wird die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) verwendet, um den [**MCI \_ PLAY-Befehl**](mci-play.md) an das Gerät zu senden, das durch einen Gerätebezeichner identifiziert wird.


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



Der im ersten Parameter angegebene Gerätebezeichner wird abgerufen, wenn das Gerät mit dem [**MCI \_ OPEN-Befehl**](mci-open.md) geöffnet wird. Der letzte Parameter ist die Adresse einer [**MCI \_ PLAY \_ PARMS-Struktur,**](mci-play-parms.md) die Informationen darüber enthalten kann, wo die Wiedergabe beginnen und beenden soll. Viele MCI-Befehlsmeldungen verwenden eine -Struktur, um Parameter dieser Art zu enthalten. Der erste Member jeder dieser Strukturen identifiziert das Fenster, das nach Abschluss des Vorgangs eine [**MM \_ MCINOTIFY-Nachricht empfängt.**](mm-mcinotify.md)

 

 