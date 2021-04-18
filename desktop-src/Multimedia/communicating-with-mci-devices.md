---
title: Kommunikation mit MCI-Geräten
description: Kommunikation mit MCI-Geräten
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- Mciwndsendstring-Makro
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341296"
---
# <a name="communicating-with-mci-devices"></a>Kommunikation mit MCI-Geräten

Der Treiber der einzelnen MCI-Geräte verwaltet eine Liste der aktuellen Einstellungen und Funktionen, sodass eine genaue Antwort ausgegeben werden kann, wenn nach Informationen abgefragt wird.

Wenn Sie mit einem MCI-Gerät kommunizieren möchten, können Sie mciwnd-Makros und-Funktionen verwenden. Viele der gängigsten MCI-Befehle und-Abfragen werden als Makros definiert. Wenn der Task, den Sie ausführen möchten, jedoch nicht als Funktion oder Makro verfügbar ist, können Sie MCI-Befehle direkt an den Gerätetreiber senden, indem Sie das [**mciwndsendstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) -Makro oder entweder das Nachrichten Formular oder die Zeichen folgen Form der MCI-Befehle verwenden. Die Verwendung des **mciwndsendstring** -Makros entspricht der Verwendung der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion wie folgt:


```C++
mciSendString(sz, Null, 0, Null) 
```



Die Parameter von [**mciwndsendstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) schließen nur das Fenster Handle und die Zeichen folgen Form des Befehls ein. Verwenden Sie zum Abrufen der Informationen, die von einem Zeichen folgen Befehl zurückgegeben werden, das [**mciwndreturnstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) -Makro.

Weitere Informationen zu MCI finden Sie unter [MCI](mci.md).

> [!Note]  
> Sie müssen den Gerätealias aus dem MCI-Befehl ausschließen, wenn Sie **mciwndsendstring** verwenden. Die mciwnd-Bibliothek fügt diesen Alias hinzu, wenn der Befehl an das MCI-Gerät gesendet wird.

 

 

 