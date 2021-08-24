---
title: Kommunizieren mit MCI-Geräten
description: Kommunizieren mit MCI-Geräten
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- MCIWndSendString-Makro
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3def53cda9374ba50dfea8252918f073d961410092a977c8779f3a29d6b36204
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807840"
---
# <a name="communicating-with-mci-devices"></a>Kommunizieren mit MCI-Geräten

Der Treiber jedes MCI-Geräts verwaltet eine Liste der aktuellen Einstellungen und Funktionen, sodass er eine genaue Antwort ausstellen kann, wenn informationen abgefragt werden.

Wenn Sie mit einem MCI-Gerät kommunizieren möchten, können Sie MCIWnd-Makros und -Funktionen verwenden. Viele der gängigsten MCI-Befehle und -Abfragen werden als Makros definiert. Wenn die Aufgabe, die Sie ausführen möchten, jedoch nicht als Funktion oder Makro verfügbar ist, können Sie MCI-Befehle direkt an den Gerätetreiber senden, indem Sie das [**MCIWndSendString-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) oder das Nachrichtenformular oder die Zeichenfolgenform der MCI-Befehle verwenden. Die Verwendung des **MCIWndSendString-Makros** entspricht der Verwendung der [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) wie folgt:


```C++
mciSendString(sz, Null, 0, Null) 
```



Die Parameter von [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) enthalten nur das Fensterhandle und die Zeichenfolgenform des Befehls. Verwenden Sie das [**MCIWndReturnString-Makro,**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) um die von einem Zeichenfolgenbefehl zurückgegebenen Informationen abzurufen.

Weitere Informationen zu MCI finden Sie unter [MCI](mci.md).

> [!Note]  
> Sie müssen den Gerätealias aus dem MCI-Befehl ausschließen, wenn Sie **MCIWndSendString** verwenden. Die MCIWnd-Bibliothek fügt diesen Alias hinzu, wenn der Befehl an das MCI-Gerät gesendet wird.

 

 

 