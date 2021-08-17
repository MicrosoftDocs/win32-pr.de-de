---
description: Das System sendet eine WM \_ NCPAINT-Nachricht an das Fenster, wenn ein Teil des Nichtclientbereichs des Fensters, z. B. die Titelleiste, die Menüleiste oder der Fensterrahmen, aktualisiert werden muss.
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: Nichtclientbereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a20593063af4382e79697b249324ba0fd6fe2782d903b645a2b80c25c63c436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698739"
---
# <a name="nonclient-area"></a>Nichtclientbereich

Das System sendet immer dann eine [**WM \_ NCPAINT-Nachricht**](wm-ncpaint.md) an das Fenster, wenn ein Teil des Nichtclientbereichs des Fensters, z. B. die Titelleiste, die Menüleiste oder der Fensterrahmen, aktualisiert werden muss. Das System kann auch andere Nachrichten senden, um ein Fenster anweisen, einen Teil des Clientbereichs zu aktualisieren. Wenn beispielsweise ein Fenster aktiv oder inaktiv wird, sendet es die [**WM \_ NCACTIVATE-Nachricht,**](../winmsg/wm-ncactivate.md) um die Titelleiste zu aktualisieren. Im Allgemeinen wird die Verarbeitung dieser Meldungen für Standardfenster nicht empfohlen, da die Anwendung in der Lage sein muss, alle erforderlichen Teile des Nichtclientbereichs für das Fenster zu zeichnen. Aus diesem Grund übergeben die meisten Anwendungen diese Nachrichten zur Standardverarbeitung an [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Eine Anwendung, die benutzerdefinierte Nichtclientbereiche für ihre Fenster erstellt, muss diese Meldungen verarbeiten. Dabei muss die Anwendung einen Fenstergerätekontext zum Zeichnen im Fenster verwenden. Der *Fenstergerätekontext* ermöglicht der Anwendung das Zeichnen in allen Teilen des Fensters, einschließlich des Nicht-Clientbereichs. Eine Anwendung ruft einen Fenstergerätekontext mithilfe der [**GetWindowDC-**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) oder [**GetDCEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdcex) ab und muss nach Abschluss des Zeichnens den Fenstergerätekontext mithilfe der [**ReleaseDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-releasedc) freigeben.

Das System verwaltet einen Updatebereich für den Nichtclientbereich. Wenn eine Anwendung eine [**WM \_ NCPAINT-Nachricht**](wm-ncpaint.md) empfängt, enthält der *wParam-Parameter* ein Handle für einen Bereich, der die Dimensionen des Updatebereichs definiert. Die Anwendung kann das Handle verwenden, um den Updatebereich mit dem Clippingbereich für den Gerätekontext des Fensters zu kombinieren. Das System kombiniert den Updatebereich beim Abrufen des Fenstergerätekontexts nicht automatisch, es sei denn, die Anwendung verwendet [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) und gibt sowohl das Regionshandle als auch das DCX \_ INTERSECTRGN-Flag an. Wenn die Anwendung den Updatebereich nicht kombiniert, werden nur Zeichnungsvorgänge abgeschnitten, die sich andernfalls außerhalb des Fensters erstrecken würden. Die Anwendung ist nicht für das Löschen der Updateregion verantwortlich, unabhängig davon, ob sie die Region verwendet.

Wenn eine Anwendung die [**WM \_ NCACTIVATE-Nachricht**](../winmsg/wm-ncactivate.md) verarbeitet, muss sie nach der Verarbeitung **TRUE** zurückgeben, um das System anzuweisen, die Änderung des aktiven Fensters abzuschließen. Wenn das Fenster minimiert wird, wenn die Anwendung die **WM \_ NCACTIVATE-Nachricht** empfängt, sollte die Meldung an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben werden. In solchen Fällen wird die Bezeichnung für das Symbol von der Standardfunktion neu gezeichnet.

 

 
