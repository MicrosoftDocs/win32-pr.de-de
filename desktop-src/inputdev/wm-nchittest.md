---
title: WM_NCHITTEST Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, um zu bestimmen, welcher Teil des Fensters einer bestimmten Bildschirm Koordinate entspricht.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- Tastatur-und Maus Eingaben für WM_NCHITTEST Nachricht
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
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337315"
---
# <a name="wm_nchittest-message"></a>WM- \_ nchittest-Nachricht

Wird an ein Fenster gesendet, um zu bestimmen, welcher Teil des Fensters einer bestimmten Bildschirm Koordinate entspricht. Dies kann z. b. der Fall sein, wenn der Cursor verschoben wird, wenn eine Maustaste gedrückt oder losgelassen wird, oder als Reaktion auf einen Aufrufen einer Funktion, wie z. b. [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint). Wenn die Maus nicht erfasst wird, wird die Nachricht an das Fenster unterhalb des Cursors gesendet. Andernfalls wird die Nachricht an das Fenster gesendet, das die Maus erfasst hat.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Das nieder wertige Wort gibt die x-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Bildschirms.

Das höchst wertige Wort gibt die y-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Bildschirms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion ist einer der folgenden Werte, der die Position des Cursor-Hot-Spot angibt.



| Rückgabecode/-wert                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Htborder**</dt> <dt>18</dt> </dl>      | Im Rahmen eines Fensters ohne Größen Anpassungsrahmen.<br/>                                                                                                                                           |
| <dl> <dt>**Htbottom**</dt> <dt>15</dt> </dl>      | Am unteren horizontalen Rand eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters vertikal zu ändern).<br/>                                                                                    |
| <dl> <dt>**Htbottomleft**</dt> <dt>16</dt> </dl>  | In der unteren linken Ecke eines Rahmens eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters diagonal zu ändern).<br/>                                                                              |
| <dl> <dt>**Htbottomright**</dt> <dt>17</dt> </dl> | In der unteren rechten Ecke eines Rahmens eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters diagonal zu ändern).<br/>                                                                             |
| <dl> <dt>**Htcaption**</dt> <dt>2</dt> </dl>      | In einer Titelleiste.<br/>                                                                                                                                                                                         |
| <dl> <dt>**Htclient**</dt> <dt>1</dt> </dl>       | In einem Client Bereich.<br/>                                                                                                                                                                                       |
| <dl> <dt>**Htclose**</dt> <dt>20</dt> </dl>       | In einer Schaltfläche **Schließen** .<br/>                                                                                                                                                                                  |
| <dl> <dt>**HTError**</dt> <dt>-2</dt> </dl>       | Auf dem Bildschirm Hintergrund oder in einer Trennlinie zwischen Fenstern (identisch mit " **htnirgendwo**", mit der Ausnahme, dass die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion ein Systemsignal erzeugt, um einen Fehler anzugeben).<br/> |
| <dl> <dt>**Htgrowbox**</dt> <dt>4</dt> </dl>      | In einem Größen Feld (identisch mit " **htsize**").<br/>                                                                                                                                                                     |
| <dl> <dt>**Hthelp**</dt> <dt>21</dt> </dl>        | In einer **Hilfe** Schaltfläche.<br/>                                                                                                                                                                                   |
| <dl> <dt>**Hthscroll**</dt> <dt>6</dt> </dl>      | In einer horizontalen Schiebe Leiste.<br/>                                                                                                                                                                             |
| <dl> <dt>**Htleft**</dt> <dt>10</dt> </dl>        | Am linken Rand eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters horizontal zu ändern).<br/>                                                                                              |
| <dl> <dt>**Htmenu**</dt> <dt>5</dt> </dl>         | In einem Menü.<br/>                                                                                                                                                                                              |
| <dl> <dt>**Htmaxbutton**</dt> <dt>9</dt> </dl>    | Auf der Schaltfläche **maximieren** .<br/>                                                                                                                                                                               |
| <dl> <dt>**Htminbutton**</dt> <dt>8</dt> </dl>    | Auf der Schaltfläche **minimieren** .<br/>                                                                                                                                                                               |
| <dl> <dt>**Htnirgendwo**</dt> <dt>0</dt> </dl>      | Auf dem Bildschirm Hintergrund oder auf einer Trennlinie zwischen Fenstern.<br/>                                                                                                                                         |
| <dl> <dt>**Htreduce**</dt> <dt>8</dt> </dl>       | Auf der Schaltfläche **minimieren** .<br/>                                                                                                                                                                               |
| <dl> <dt>**Htright**</dt> <dt>11</dt> </dl>       | Am rechten Rand eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters horizontal zu ändern).<br/>                                                                                             |
| <dl> <dt>**Htsize**</dt> <dt>4</dt> </dl>         | In einem Größen Feld (identisch mit " **htgrowbox**").<br/>                                                                                                                                                                  |
| <dl> " <dt>**Htsysmenu**</dt> <dt>3</dt> " </dl>      | In einem Fenstermenü oder in der Schaltfläche **Schließen** in einem untergeordneten Fenster.<br/>                                                                                                                                            |
| <dl> <dt>**Httop**</dt> <dt>12</dt> </dl>         | Am oberen horizontalen Rand eines Fensters.<br/>                                                                                                                                                             |
| <dl> <dt>**Httopleft**</dt> <dt>13</dt> </dl>     | In der oberen linken Ecke eines Fensterrahmens.<br/>                                                                                                                                                            |
| <dl> <dt>**Httopright**</dt> <dt>14</dt> </dl>    | In der oberen rechten Ecke eines Fensterrahmens.<br/>                                                                                                                                                           |
| <dl> <dt>**Httransparent**</dt> <dt>-1</dt> </dl> | In einem Fenster, das zurzeit von einem anderen Fenster im gleichen Thread abgedeckt wird (die Nachricht wird an die zugrunde liegenden Fenster im gleichen Thread gesendet, bis eine von Ihnen einen Code zurückgibt, der nicht " **httransparent**" ist).<br/>  |
| <dl> <dt>**Htvscroll**</dt> <dt>7</dt> </dl>      | Auf der vertikalen Schiebe Leiste.<br/>                                                                                                                                                                             |
| <dl> <dt>**Htzoom**</dt> <dt>9</dt> </dl>         | Auf der Schaltfläche **maximieren** .<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Position:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können). Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen. Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.

> [!IMPORTANT]
> Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.

 

**Windows Vista:** Wenn Sie benutzerdefinierte Frames erstellen, die die Standard Beschriftungs Schaltflächen enthalten, sollte diese Nachricht zuerst an die [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) -Funktion übermittelt werden. Dadurch kann der Desktopfenster-Manager (DWM) Treffer Tests für die Beschriftungen bereitstellen. Wenn **DwmDefWindowProc** die Nachricht nicht verarbeitet, ist möglicherweise eine weitere Verarbeitung von **WM \_ nchittest** erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser. h (Include WINDOWSX. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**\_Y- \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

**Licher**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkt**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

