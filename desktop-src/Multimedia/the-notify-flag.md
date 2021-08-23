---
title: Das Benachrichtigungsflag
description: Das Benachrichtigungsflag
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- MCI_NOTIFY-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbec671a9810d31078eedf9b8557bcdc4fa7c3e82f688b7fd005f85cb4127476
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688270"
---
# <a name="the-notify-flag"></a>Das Benachrichtigungsflag

Das Flag "notify" (MCI \_ NOTIFY) weist das Gerät an, eine [**MM MCINOTIFY-Nachricht**](mm-mcinotify.md) zu senden, wenn das Gerät eine Aktion abschließt. Ihre Anwendung muss über eine Fensterprozedur verfügen, um die MM \_ MCINOTIFY-Nachricht zu verarbeiten, damit die Benachrichtigung auswirkungen kann. Eine MM \_ MCINOTIFY-Meldung gibt an, dass die Verarbeitung eines Befehls abgeschlossen wurde, gibt jedoch nicht an, ob der Befehl erfolgreich abgeschlossen wurde, fehlgeschlagen ist oder abgelöst oder abgebrochen wurde.

Die Anwendung gibt das Handle für das Zielfenster für die Nachricht an, wenn sie einen Befehl ausgibt. In der Befehlszeichenfolgen-Schnittstelle ist dieses Handle der letzte Parameter der [**mciSendString-Funktion.**](/previous-versions//dd757161(v=vs.85)) In der Befehlsmeldungsschnittstelle wird das Handle im Wort mit niedriger Reihenfolge des **dwCallBack-Members** der -Struktur angegeben, die mit der Befehlsmeldung gesendet wird. (Jede Struktur, die einer Befehlsmeldung zugeordnet ist, enthält diesen Member.)

 

 