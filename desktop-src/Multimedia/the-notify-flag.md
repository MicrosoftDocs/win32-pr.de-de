---
title: Das Benachrichtigungs Kennzeichen
description: Das Benachrichtigungs Kennzeichen
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- MCI_NOTIFY-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390276"
---
# <a name="the-notify-flag"></a>Das Benachrichtigungs Kennzeichen

Das Flag "Benachrichtigen" (MCI \_ Notify) weist das Gerät an, eine [**mm-mcinotify**](mm-mcinotify.md) -Nachricht zu senden, wenn das Gerät eine Aktion abschließt. Die Anwendung muss über eine Fenster Prozedur verfügen, um die mm-Meldung zu verarbeiten, \_ dass die Benachrichtigung eine beliebige Auswirkung hat. Eine mm- \_ mcinotifizierungsmeldung gibt an, dass die Verarbeitung eines Befehls abgeschlossen wurde. es wird jedoch nicht angegeben, ob der Befehl erfolgreich ausgeführt wurde, fehlgeschlagen ist oder ersetzt oder abgebrochen wurde.

Die Anwendung gibt das Handle für das Zielfenster der Nachricht an, wenn ein Befehl ausgegeben wird. In der Befehls Zeichenfolgen-Schnittstelle ist dieses Handle der letzte Parameter der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion. In der befehlsnachrichten Schnittstelle wird das Handle in dem nieder wertigen Wort des **dwcallback** -Members der Struktur angegeben, die mit der Befehls Meldung gesendet wird. (Jede Struktur, die einer Befehls Meldung zugeordnet ist, enthält diesen Member.)

 

 