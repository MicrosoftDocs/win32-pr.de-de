---
title: AVICap-Rückruffunktionen
description: AVICap-Rückruffunktionen
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- AVICap-Klasse, Rückruffunktionen
- AVICap-Rückruffunktionen, Informationen
- WM_CAP_SET_CALLBACK_CAPCONTROL Meldung
- WM_CAP_SET_CALLBACK_ERROR Meldung
- WM_CAP_SET_CALLBACK_FRAME Meldung
- WM_CAP_SET_CALLBACK_STATUS Meldung
- WM_CAP_SET_CALLBACK_VIDEOSTREAM Meldung
- WM_CAP_SET_CALLBACK_WAVESTREAM Meldung
- WM_CAP_SET_CALLBACK_YIELD Meldung
- capSetCallbackOnCapControl-Makro
- capSetCallbackOnErrormacro
- capSetCallbackOnFrame-Makro
- capSetCallbackOnStatus-Makro
- capSetCallbackOnVideoStream-Makro
- capSetCallbackOnWaveStream-Makro
- capSetCallbackOnYield-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee000f03df5bb23ed46f3692ded692630c85a292dfe3dccfcd24a8867849d5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691960"
---
# <a name="avicap-callback-functions"></a>AVICap-Rückruffunktionen

Ihre Anwendung kann Rückruffunktionen mit einem Erfassungsfenster registrieren, damit ihre Anwendung benachrichtigt wird, wenn sich der Status ändert, wenn Fehler auftreten, wenn Videoframe- und Audiopuffer verfügbar werden und während der Streamingerfassung ergebnisse. Die folgenden Meldungen legen die Rückruffunktion fest.



| `Message`                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAP \_ SET \_ CALLBACK \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)   | Gibt die Rückruffunktion in der aufgerufenen Anwendung an, um eine präzise Steuerung des Erfassungsstarts und -endes zu ermöglichen. Sie können auch das [**CapSetCallbackOnCapControl-Makro**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) verwenden, um diese Nachricht zu senden.                   |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md)             | Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn ein Fehler auftritt. Sie können auch das [**CapSetCallbackOnError-Makro**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) verwenden, um diese Nachricht zu senden.                                                           |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ FRAME**](wm-cap-set-callback-frame.md)             | Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn Vorschauframes erfasst werden. Sie können auch das [**CapSetCallbackOnFrame-Makro**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) verwenden, um diese Nachricht zu senden.                                               |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ STATUS**](wm-cap-set-callback-status.md)           | Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn sich der Status ändert. Sie können auch das [**CapSetCallbackOnStatus-Makro**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) verwenden, um diese Nachricht zu senden.                                                      |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md) | Gibt die Rückruffunktion in der Anwendung an, die während der Streamingerfassung aufgerufen wird, wenn ein neuer Videopuffer verfügbar wird. Sie können auch das [**CapSetCallbackOnVideoStream-Makro**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) verwenden, um diese Nachricht zu senden. |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)   | Gibt die Rückruffunktion in der Anwendung an, die während der Streamingerfassung aufgerufen wird, wenn ein neuer Audiopuffer verfügbar wird. Sie können auch das [**CapSetCallbackOnWaveStream-Makro**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) verwenden, um diese Nachricht zu senden.   |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ YIELD**](wm-cap-set-callback-yield.md)             | Gibt die Rückruffunktion in der Anwendung an, die bei der Streamingerfassung aufgerufen wird. Sie können auch das [**CapSetCallbackOnYield-Makro**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) verwenden, um diese Nachricht zu senden.                                         |



 

In den folgenden Themen werden die verschiedenen Rückruffunktionen, die an die Funktionen gesendeten Benachrichtigungen und deren Verwendung beschrieben.

 

 




