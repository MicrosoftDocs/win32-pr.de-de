---
description: Das System sendet eine WM \_ ncpaint-Meldung an das Fenster, wenn ein Teil des nicht-Client Bereichs des Fensters (z. b. die Titelleiste, die Menüleiste oder der Fensterrahmen) aktualisiert werden muss.
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: Nicht-Client Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51da31709f5bd9326cc0d05a9e37e2df78bfbb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215186"
---
# <a name="nonclient-area"></a>Nicht-Client Bereich

Das System sendet eine [**WM \_ ncpaint**](wm-ncpaint.md) -Meldung an das Fenster, wenn ein Teil des nicht-Client Bereichs des Fensters (z. b. die Titelleiste, die Menüleiste oder der Fensterrahmen) aktualisiert werden muss. Das System kann auch andere Nachrichten senden, um ein Fenster zu leiten, um einen Teil des Client Bereichs zu aktualisieren. Wenn ein Fenster z. b. aktiv oder inaktiv wird, sendet es die [**WM- \_ ncaktivierungs**](../winmsg/wm-ncactivate.md) Nachricht, um die zugehörige Titelleiste zu aktualisieren. Im Allgemeinen wird die Verarbeitung dieser Nachrichten für Standardfenster nicht empfohlen, da die Anwendung alle erforderlichen Teile des nicht-Client Bereichs für das Fenster zeichnen muss. Aus diesem Grund werden diese Nachrichten von den meisten Anwendungen zur Standard Verarbeitung an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben.

Eine Anwendung, die benutzerdefinierte nicht-Client Bereiche für Windows erstellt, muss diese Nachrichten verarbeiten. Wenn dies der Fall ist, muss die Anwendung einen Fenster Gerätekontext verwenden, um das Zeichnen im Fenster auszuführen. Der *Fenster Gerätekontext* ermöglicht der Anwendung das Zeichnen in allen Teilen des Fensters, einschließlich des nicht-Client Bereichs. Eine Anwendung ruft einen Fenster Gerätekontext mithilfe der [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) -Funktion oder der [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion ab und muss, wenn die Zeichnung beendet ist, den Fenster Gerätekontext mithilfe der [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion freigeben.

Das System verwaltet einen Update Bereich für den nicht-Client Bereich. Wenn eine Anwendung eine [**WM- \_ ncpaint**](wm-ncpaint.md) -Nachricht empfängt, enthält der *wParam* -Parameter ein Handle für einen Bereich, der die Dimensionen des Aktualisierungs Bereichs definiert. Die Anwendung kann das Handle verwenden, um den Aktualisierungs Bereich mit dem Clippingbereich für den Fenster Gerätekontext zu kombinieren. Das System kombiniert die Update Region nicht automatisch, wenn der Fenster Gerätekontext abgerufen wird, es sei denn, die Anwendung verwendet [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) und gibt sowohl das Regions Handle als auch das DCX- \_ intersectrgn-Flag an. Wenn die Anwendung den Update Bereich nicht kombiniert, werden nur Zeichnungsvorgänge abgeschnitten, die andernfalls außerhalb des Fensters erweitert werden. Die Anwendung ist nicht dafür verantwortlich, den Update Bereich zu löschen, unabhängig davon, ob Sie die Region verwendet.

Wenn eine Anwendung die [**WM- \_ ncaktivierungs**](../winmsg/wm-ncactivate.md) Nachricht verarbeitet, muss Sie nach der Verarbeitung " **true** " zurückgeben, um das System zum Abschluss der Änderung des aktiven Fensters zu leiten. Wenn das Fenster minimiert wird, wenn die Anwendung die **WM- \_ ncaktivierungs** Nachricht empfängt, sollte die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben werden. In solchen Fällen wird die Bezeichnung für das Symbol von der Standardfunktion neu gezeichnet.

 

 
