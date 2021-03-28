---
description: Benachrichtigungsfunktionen
ms.assetid: 44f69e05-1f08-48da-abb7-7e0a96c0cd26
title: Benachrichtigungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e5ca0bbcd9f2f184abd312fe15d4923e5cf14b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131333"
---
# <a name="notification-functions"></a>Benachrichtigungsfunktionen



| Flat-Funktion                                                                  | Wrapper Methode                            | Bemerkungen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gpstatus wingdipapi gdiplusnotificationhook (out ULONG \_ ptr \* Token)<br/> | Wird von Wrapper Methoden nicht aufgerufen.<br/> | Die [**gdiplstreamstartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) -Funktion gibt einen Zeiger auf eine [**gdipl-startupoutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) -Struktur (im Ausgabeparameter) zurück. Einer der Member der-Struktur ist ein Zeiger auf eine Benachrichtigungs Hook-Funktion, die dieselbe Signatur aufweist wie gdipl-notificationhook.<br/> Es gibt zwei Möglichkeiten, wie Sie die Benachrichtigungs-Hook-Funktion aufrufen können. Sie können den von [**gdiplstarstartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) zurückgegebenen Zeiger verwenden, oder Sie können gdipl"gdipl-notificationhook" aufzurufen. Tatsächlich überprüft "gdiplingnotificationhook" lediglich, ob Sie den Hintergrund Thread unterdrückt haben, und ruft dann die Benachrichtigungs-Hook-Funktion auf, die von " **gdiplstartstartup**" zurückgegeben wird.<br/> Der Token-Parameter empfängt einen Bezeichner, den Sie später an einen entsprechenden-aufrufunhook übergeben sollten.<br/>                                                                                                                                         |
| VOID wingdipapi gdipl-notificationunhook (ULONG \_ ptr-Token)<br/>         | Wird von Wrapper Methoden nicht aufgerufen.<br/> | Die [**gdiplstreamstartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) -Funktion gibt einen Zeiger auf eine [**gdipl-startupoutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) -Struktur (im Ausgabeparameter) zurück. Einer der Member der-Struktur ist ein Zeiger auf eine Benachrichtigungsfunktion, die die gleiche Signatur aufweist wie gdipl-notificationunhook.<br/> Es gibt zwei Möglichkeiten, wie Sie die aufzuheben-Benachrichtigungsfunktion aufrufen können. Sie können den von [**gdiplstarstartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) zurückgegebenen Zeiger verwenden, oder Sie können gdipl"gdipl-notificationunhook" abrufen. In der Tat überprüft "gdiplingnotificationunhook" lediglich, ob Sie den Hintergrund Thread unterdrückt haben, und ruft dann die Benachrichtigungsfunktion "aufzuheben" auf, die von " **gdiplupstartup**" zurückgegeben wird.<br/> Wenn Sie die aufzuheben-Benachrichtigungsfunktion aufzurufen, übergeben Sie das Token, das Sie zuvor erhalten haben, von einem entsprechenden-Rückruf an die Notification Hook-Funktion. Wenn Sie dies nicht tun, werden Ressourcen Lecks angezeigt, die nicht bereinigt werden, bis der Prozess beendet wird.<br/> |



 

 

 




