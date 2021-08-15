---
title: Yield-Rückruffunktionen
description: Yield-Rückruffunktionen
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- AVICap-Rückruffunktionen, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e87a3c986378bee05078b8cab28a0647827a1102ef1809558a47dcd5123af2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369134"
---
# <a name="yield-callback-functions"></a>Yield-Rückruffunktionen

Anwendungen können während der Streamingerfassung Yield-Rückruffunktionen verwenden. (Eine Yield-Rückruffunktion besteht in der Regel aus einer Nachrichtenschleife, die [PeekMessage,](/windows/win32/api/winuser/nf-winuser-peekmessagea) [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)und [DispatchMessage aufruft.)](/windows/win32/api/winuser/nf-winuser-dispatchmessage) Das Erfassungsfenster ruft die Yield-Rückruffunktion mindestens einmal für jeden erfassten Videoframe auf. Die genaue Rate hängt jedoch von der Bildfrequenz und dem Mehraufwand des Erfassungstreibers und des Datenträgers ab.

 

 