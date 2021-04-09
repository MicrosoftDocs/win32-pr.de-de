---
title: Verwenden von Scrollleisten
description: Dieser Abschnitt enthält Themen, die veranschaulichen, wie Schiebe leisten erstellt werden.
ms.assetid: 45ffb56f-f567-40d7-8172-e64e26744ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d602426bd5f716a380d43104046f330d3240d516
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039700"
---
# <a name="using-scroll-bars"></a>Verwenden von Scrollleisten

Dieser Abschnitt enthält Themen, die veranschaulichen, wie Schiebe leisten erstellt werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen von Scrollleisten](create-scroll-bars.md)<br/>                                                                     | Beim Erstellen eines überlappenden, Popup-oder untergeordneten Fensters können Sie Standard Scrollleisten hinzufügen, indem Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden und "WS \_ HScroll", "WS \_ VScroll" oder beide Stile angeben. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Vorgehensweise beim Scrollen von Text](scroll-text-in-scroll-bars.md)<br/>                                                                    | In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfenster Prozedur einer Anwendung vornehmen können, damit ein Benutzer einen Bildlauf durchführen kann. Im Beispiel in diesem Abschnitt wird ein Array von Text Zeichenfolgen erstellt und angezeigt. Außerdem werden die Bild Lauf leisten Meldungen [**WM \_ HScroll**](wm-hscroll.md) und [**WM \_ VScroll**](wm-vscroll.md) verarbeitet, sodass der Benutzer sowohl vertikal als auch horizontal einen Bildlauf durchführen kann. <br/>                                                                                                                                                                                                                                                                 |
| [Vorgehensweise beim Scrollen einer Bitmap](scroll-a-bitmap-in-scroll-bars.md)<br/>                                                            | In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfenster Prozedur einer Anwendung vornehmen können, damit der Benutzer einen Bildlauf in einer Bitmap ausführen kann. <br/> Das Beispiel enthält ein Menü Element, mit dem der Bildschirminhalt in eine Bitmap kopiert und die Bitmap im Client Bereich angezeigt wird. Im Beispiel werden auch die von den Schiebe leisten generierten " [**WM \_ HScroll**](wm-hscroll.md) "-und " [**WM \_ VScroll**](wm-vscroll.md) "-Meldungen verarbeitet, sodass der Benutzer die Bitmap horizontal und vertikal scrollen kann. Im Gegensatz zum Beispiel für Text mit Text wird mit dem Bitmap-Beispiel die [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) -Funktion verwendet, um den ungültigen Teil des Client Bereichs zu zeichnen. <br/> |
| [Erstellen einer Tastaturschnittstelle für Standard Scrollleisten](create-a-keyboard-interface-for-standard-scroll-bars.md)<br/> | Obwohl ein Schiebe leisten-Steuerelement eine integrierte Tastaturschnittstelle bereitstellt, ist dies für eine Standard Scrollleiste nicht der Standard. Um eine Tastaturschnittstelle für eine Standard Scrollleiste zu implementieren, muss eine Fenster Prozedur die [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht verarbeiten und den durch den *wParam* -Parameter angegebenen Code des virtuellen Schlüssels überprüfen. Wenn der Code des virtuellen Schlüssels einer Pfeiltaste entspricht, sendet die Fenster Prozedur selbst eine [**WM \_ HScroll**](wm-hscroll.md) -oder [**WM \_ VScroll**](wm-vscroll.md) -Nachricht, bei der das nieder wertige Wort des *wParam* -Parameters auf den entsprechenden Anforderungs Code der Schiebe Leiste festgelegt ist. <br/>                                              |



 

 

