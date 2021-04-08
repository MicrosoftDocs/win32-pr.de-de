---
title: Yield-Rückruf Funktionen
description: Yield-Rückruf Funktionen
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Avicap-Rückruf Funktionen, Yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3666ea24a1d37402ffc13c09ca8ab95fcd19e1f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725856"
---
# <a name="yield-callback-functions"></a>Yield-Rückruf Funktionen

Anwendungen können Yield Callback-Funktionen während der streamingerfassung verwenden. (Eine Yield Callback-Funktion besteht in der Regel aus einer Nachrichten Schleife, die " [Peer Message](/windows/win32/api/winuser/nf-winuser-peekmessagea)", " [translatemess](/windows/win32/api/winuser/nf-winuser-translatemessage)" und " [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage)" aufruft.) Im Fenster erfassen wird die Yield Callback-Funktion für jeden aufgezeichneten Videoframe mindestens einmal aufgerufen, die genaue Rate hängt jedoch von der Framerate und dem Aufwand des Aufzeichnungs Treibers und des Datenträgers ab.

 

 