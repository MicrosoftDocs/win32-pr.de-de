---
title: WM_NCHITTEST Meldung (Winuser.h)
description: Wird an ein Fenster gesendet, um zu bestimmen, welcher Teil des Fensters einer bestimmten Bildschirmkoordinate entspricht.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- WM_NCHITTEST Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f54c397db10e8ecd6b2ed3c67a73affde4507ea59a265d502f28ada97b8a68e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778640"
---
# <a name="wm_nchittest-message"></a>WM \_ NCHITTEST-Nachricht

Wird an ein Fenster gesendet, um zu bestimmen, welcher Teil des Fensters einer bestimmten Bildschirmkoordinate entspricht. Dies kann z. B. auftreten, wenn der Cursor bewegt wird, wenn eine Maustaste gedrückt oder losgelassen wird oder als Reaktion auf einen Aufruf einer Funktion wie [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint). Wenn die Maus nicht erfasst wird, wird die Nachricht an das Fenster unterhalb des Cursors gesendet. Andernfalls wird die Nachricht an das Fenster gesendet, das die Maus erfasst hat.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt die x-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Bildschirms.

Das Wort in hoher Reihenfolge gibt die y-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Bildschirms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert der [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ist einer der folgenden Werte, der die Position des Cursor-Hotspots angibt.



| Rückgabecode/-wert                                                                                                                                    | Beschreibung                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**HTBORDER**</dt> <dt>18</dt> </dl>      | Im Rahmen eines Fensters, das keinen Größenrahmen besitzt.<br/>                                                                                                                                           |
| <dl> <dt>**HTBOTTOM**</dt> <dt>15</dt> </dl>      | Im unteren horizontalen Rahmen eines Fensters, in dem die Größe geändert werden kann (der Benutzer kann mit der Maus darauf klicken, um die Größe des Fensters vertikal zu ändern).<br/>                                                                                    |
| <dl> <dt>**HTBOTTOMLEFT**</dt> <dt>16</dt> </dl>  | In der unteren linken Ecke eines Rahmens eines fensters mit Größenänderung (der Benutzer kann mit der Maus klicken, um die Größe des Fensters diagonal zu ändern).<br/>                                                                              |
| <dl> <dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt> </dl> | In der unteren rechten Ecke eines Rahmens eines Fensters mit Größenänderung (der Benutzer kann mit der Maus klicken, um die Größe des Fensters diagonal zu ändern).<br/>                                                                             |
| <dl> <dt>**ICEAPTION**</dt> <dt>2</dt> </dl>      | In einer Titelleiste.<br/>                                                                                                                                                                                         |
| <dl> <dt>**HTCLIENT**</dt> <dt>1</dt> </dl>       | In einem Clientbereich.<br/>                                                                                                                                                                                       |
| <dl> <dt>**NOKIALOSE**</dt> <dt>20</dt> </dl>       | In einer Schaltfläche **Schließen.**<br/>                                                                                                                                                                                  |
| <dl> <dt>**HTERROR**</dt> <dt>-2</dt> </dl>       | Auf dem Bildschirmhintergrund oder auf einer Trennlinie zwischen Fenstern (identisch mit **HTNOWHERE,** mit der Ausnahme, dass die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) einen Systemsignal erzeugt, um auf einen Fehler hinzuweisen).<br/> |
| <dl> <dt>**HTGROWBOX**</dt> <dt>4</dt> </dl>      | In einem Größenfeld (identisch mit **HTSIZE**).<br/>                                                                                                                                                                     |
| <dl> <dt>**HTHELP**</dt> <dt>21</dt> </dl>        | In  einer Hilfeschaltfläche.<br/>                                                                                                                                                                                   |
| <dl> <dt>**HTHSCROLL**</dt> <dt>6</dt> </dl>      | In einer horizontalen Bildlaufleiste.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTLEFT**</dt> <dt>10</dt> </dl>        | Im linken Rahmen eines Fensters, in dem die Größe geändert werden kann (der Benutzer kann mit der Maus darauf klicken, um die Größe des Fensters horizontal zu ändern).<br/>                                                                                              |
| <dl> <dt>**HTMENU**</dt> <dt>5</dt> </dl>         | In einem Menü.<br/>                                                                                                                                                                                              |
| <dl> <dt>**HTMAXBUTTON**</dt> <dt>9</dt> </dl>    | In einer Schaltfläche **Maximieren.**<br/>                                                                                                                                                                               |
| <dl> <dt>**HTMINBUTTON**</dt> <dt>8</dt> </dl>    | In einer Schaltfläche **Minimieren.**<br/>                                                                                                                                                                               |
| <dl> <dt>**HTNOWHERE**</dt> <dt>0</dt> </dl>      | Auf dem Bildschirmhintergrund oder auf einer Trennlinie zwischen Fenstern.<br/>                                                                                                                                         |
| <dl> <dt>**HTREDUCE**</dt> <dt>8</dt> </dl>       | In einer Schaltfläche **Minimieren.**<br/>                                                                                                                                                                               |
| <dl> <dt>**HTRIGHT**</dt> <dt>11</dt> </dl>       | Im rechten Rahmen eines fenstergrößerbaren Fensters (der Benutzer kann mit der Maus darauf klicken, um die Größe des Fensters horizontal zu ändern).<br/>                                                                                             |
| <dl> <dt>**HTSIZE**</dt> <dt>4</dt> </dl>         | In einem Größenfeld (identisch mit **HTGROWBOX**).<br/>                                                                                                                                                                  |
| <dl> <dt>**HTSYSMENU**</dt> <dt>3</dt> </dl>      | In einem Fenstermenü oder in einer Schaltfläche **Schließen** in einem untergeordneten Fenster.<br/>                                                                                                                                            |
| <dl> <dt>**HTTOP**</dt> <dt>12</dt> </dl>         | Im oberen horizontalen Rahmen eines Fensters.<br/>                                                                                                                                                             |
| <dl> <dt>**HTTOPLEFT**</dt> <dt>13</dt> </dl>     | In der oberen linken Ecke eines Fensterrahmens.<br/>                                                                                                                                                            |
| <dl> <dt>**HTTOPRIGHT**</dt> <dt>14</dt> </dl>    | In der oberen rechten Ecke eines Fensterrahmens.<br/>                                                                                                                                                           |
| <dl> <dt>**HTTRANSPARENT**</dt> <dt>-1</dt> </dl> | In einem Fenster, das derzeit von einem anderen Fenster im gleichen Thread abgedeckt wird (die Nachricht wird an zugrunde liegende Fenster im gleichen Thread gesendet, bis einer von ihnen einen Code zurückgibt, der nicht **HTTRANSPARENT** ist).<br/>  |
| <dl> <dt>**HTVSCROLL**</dt> <dt>7</dt> </dl>      | In der vertikalen Bildlaufleiste.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTZOOM**</dt> <dt>9</dt> </dl>         | In einer Schaltfläche **Maximieren.**<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie den folgenden Code, um die horizontale und vertikale Position abzurufen:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Wie oben erwähnt, befindet sich die x-Koordinate in der unteren Reihenfolge **unter** dem Rückgabewert. Die y-Koordinate befindet sich in der hohen **Kurzreihenfolge** (beide stellen *signierte* Werte dar, da sie negative Werte auf Systemen mit mehreren Monitoren annehmen können). Wenn der Rückgabewert einer Variablen zugewiesen wird, können Sie das [**MAKEPOINTS-Makro**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) verwenden, um eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) aus dem Rückgabewert abzurufen. Sie können auch das [**MAKRO GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) oder [**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die x- oder y-Koordinate zu extrahieren.

> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten aufweisen, und **LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

**Windows Vista:** Wenn Sie benutzerdefinierte Frames erstellen, die die Standardbeschriftungsschaltflächen enthalten, sollte diese Meldung zuerst an die [**DwmDefWindowProc-Funktion**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) übergeben werden. Dadurch kann der Desktopfenster-Manager (DWM) Treffertests für die Schaltflächen für Beschriftungen bereitstellen. Wenn **DwmDefWindowProc** die Nachricht nicht verarbeitet, ist möglicherweise eine weitere Verarbeitung von **WM \_ NCHITTEST** erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (windowsx.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkte**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

