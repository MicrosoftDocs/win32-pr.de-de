---
title: Avicap-Rückruf Funktionen
description: Avicap-Rückruf Funktionen
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Avicap-Klasse, Rückruf Funktionen
- Avicap-Rückruf Funktionen, Informationen zu
- WM_CAP_SET_CALLBACK_CAPCONTROL Meldung
- WM_CAP_SET_CALLBACK_ERROR Meldung
- WM_CAP_SET_CALLBACK_FRAME Meldung
- WM_CAP_SET_CALLBACK_STATUS Meldung
- WM_CAP_SET_CALLBACK_VIDEOSTREAM Meldung
- WM_CAP_SET_CALLBACK_WAVESTREAM Meldung
- WM_CAP_SET_CALLBACK_YIELD Meldung
- capsetcallbackoncapcontrol-Makro
- capsetcallbackonerrormacro
- capsetcallbackonframe-Makro
- capsetcallbackonstatus-Makro
- capsetcallbackonvideostream-Makro
- capsetcallbackonwavestream-Makro
- capsetcallbackonyield-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948049"
---
# <a name="avicap-callback-functions"></a>Avicap-Rückruf Funktionen

Die Anwendung kann Rückruf Funktionen mit einem Aufzeichnungs Fenster registrieren, damit die Anwendung benachrichtigt wird, wenn sich der Status ändert, wenn Fehler auftreten, wenn Video Frame-und Audiopuffer verfügbar werden und während der streamingerfassung eine Rendite erzielt wird. Die Rückruffunktion wird in den folgenden Meldungen festgelegt.



| `Message`                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ Cap- \_ Satz Rückruf ( \_ \_ capcontrol)**](wm-cap-set-callback-capcontrol.md)   | Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, um das Starten und Beenden der Erfassung präzise zu steuern. Sie können auch das " [**capsetcallbackoncapcontrol**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) "-Makro verwenden, um diese Nachricht zu senden.                   |
| [**Rückruf Fehler bei WM-Abdeckung \_ \_ festgelegt \_ \_**](wm-cap-set-callback-error.md)             | Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn ein Fehler auftritt. Sie können auch das [**capsetcallbackonerror**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) -Makro verwenden, um diese Nachricht zu senden.                                                           |
| [**\_ \_ \_ Rückruf \_ Rahmen für WM-Cap-Satz**](wm-cap-set-callback-frame.md)             | Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn Vorschau Rahmen aufgezeichnet werden. Sie können auch das " [**capsetcallbackonframe**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) "-Makro verwenden, um diese Nachricht zu senden.                                               |
| [**Rückruf Status der WM- \_ Obergrenze \_ festlegen \_ \_**](wm-cap-set-callback-status.md)           | Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn sich der Status ändert. Sie können auch das " [**capsetcallbackonstatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) "-Makro verwenden, um diese Nachricht zu senden.                                                      |
| [**WM- \_ Abdeckungs \_ Satz \_ Rückruf \_ Videostream**](wm-cap-set-callback-videostream.md) | Gibt die Rückruffunktion in der Anwendung an, die während der streamingerfassung aufgerufen wird, wenn ein neuer Video Puffer verfügbar wird. Sie können auch das " [**capsetcallbackonvideostream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) "-Makro verwenden, um diese Nachricht zu senden. |
| [**WM- \_ Cap- \_ Satz \_ Rückruf \_ WaveStream**](wm-cap-set-callback-wavestream.md)   | Gibt die Rückruffunktion in der Anwendung an, die während der streamingerfassung aufgerufen wird, wenn ein neuer Audiopuffer verfügbar wird. Sie können auch das " [**capsetcallbackonwavestream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) "-Makro verwenden, um diese Nachricht zu senden.   |
| [**\_ \_ \_ Rückruf \_ Rendite für WM-Cap-Satz**](wm-cap-set-callback-yield.md)             | Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn Sie während der streamingerfassung Sie können auch das [**capsetcallbackonyield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) -Makro verwenden, um diese Nachricht zu senden.                                         |



 

In den folgenden Themen werden die verschiedenen Rückruf Funktionen, die an die Funktionen gesendeten Benachrichtigungen und deren Verwendungszwecke beschrieben.

 

 




