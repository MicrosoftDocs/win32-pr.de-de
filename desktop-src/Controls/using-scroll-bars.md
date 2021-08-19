---
title: Verwenden von Bildlaufleisten
description: Dieser Abschnitt enthält Themen, die veranschaulichen, wie Scrollleisten erstellt werden.
ms.assetid: 45ffb56f-f567-40d7-8172-e64e26744ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96b1341e76b80e4ba5bf45df3dcfee03db87bb82adb4ba50273edbac6db4ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957589"
---
# <a name="using-scroll-bars"></a>Verwenden von Bildlaufleisten

Dieser Abschnitt enthält Themen, die veranschaulichen, wie Scrollleisten erstellt werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen von Bildlaufleisten](create-scroll-bars.md)<br/>                                                                     | Beim Erstellen eines überlappenden, Popup- oder untergeordneten Fensters können Sie Standardscrollleisten hinzufügen, indem Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden und WS \_ HSCROLL, WS VSCROLL oder beide Stile \_ angeben. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Scrollen von Text](scroll-text-in-scroll-bars.md)<br/>                                                                    | In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfensterprozedur einer Anwendung vornehmen können, um einem Benutzer das Scrollen von Text zu ermöglichen. Das Beispiel in diesem Abschnitt erstellt und zeigt ein Array von Textzeichenfolgen an und verarbeitet Meldungen der Bildlaufleiste von [**WM \_ HSCROLL**](wm-hscroll.md) und [**WM \_ VSCROLL,**](wm-vscroll.md) sodass der Benutzer text vertikal und horizontal scrollen kann. <br/>                                                                                                                                                                                                                                                                 |
| [Scrollen einer Bitmap](scroll-a-bitmap-in-scroll-bars.md)<br/>                                                            | In diesem Abschnitt werden Änderungen beschrieben, die Sie an der Hauptfensterprozedur einer Anwendung vornehmen können, um dem Benutzer das Scrollen in einer Bitmap zu ermöglichen. <br/> Das Beispiel enthält ein Menüelement, das den Bildschirminhalt in eine Bitmap kopiert und die Bitmap im Clientbereich anzeigt. Im Beispiel werden auch die [**WM \_ HSCROLL-**](wm-hscroll.md) und [**WM \_ VSCROLL-Meldungen**](wm-vscroll.md) verarbeitet, die von den Scrollleisten generiert werden, sodass der Benutzer die Bitmap horizontal und vertikal scrollen kann. Im Gegensatz zum Beispiel für gescrollten Text verwendet das Bitmapbeispiel die [**BitBlt-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) um den ungültigen Teil des Clientbereichs zu zeichnen. <br/> |
| [Erstellen einer Tastaturschnittstelle für Standard-Bildlaufleisten](create-a-keyboard-interface-for-standard-scroll-bars.md)<br/> | Obwohl ein Bildlaufleisten-Steuerelement eine integrierte Tastaturoberfläche bietet, ist dies bei einer Standard-Bildlaufleiste nicht der Reihe. Um eine Tastaturschnittstelle für eine Standardscrollleiste zu implementieren, muss eine Fensterprozedur die [**WM \_ KEYDOWN-Nachricht**](/windows/desktop/inputdev/wm-keydown) verarbeiten und den durch den wParam-Parameter angegebenen *virtuellen Tastencode* untersuchen. Wenn der Code des virtuellen Schlüssels einer Pfeiltaste entspricht, sendet sich die Fensterprozedur selbst eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht,**](wm-vscroll.md) bei der das niedrige Wort des *wParam-Parameters* auf den entsprechenden Anforderungscode der Scrollleiste festgelegt ist. <br/>                                              |



 

 

