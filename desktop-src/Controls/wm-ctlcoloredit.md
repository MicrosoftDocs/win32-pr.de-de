---
title: WM_CTLCOLOREDIT Meldung (Winuser. h)
description: Ein Bearbeitungs Steuerelement, das nicht schreibgeschützt oder deaktiviert ist, sendet die WM \_ ctlcoloredit-Nachricht an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- Windows-Steuerelemente für WM_CTLCOLOREDIT Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475111"
---
# <a name="wm_ctlcoloredit-message"></a>\_Ctlcoloredit-Meldung von WM

Ein Bearbeitungs Steuerelement, das nicht schreibgeschützt oder deaktiviert ist, sendet die **WM \_ ctlcoloredit** -Nachricht an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll. Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster den angegebenen Gerätekontext Handle verwenden, um die Text-und Hintergrundfarben des Bearbeitungs Steuer Elements festzulegen.


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext für das Bearbeitungs Steuerelement Fenster.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Bearbeitungs Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie das Handle eines Pinsels zurückgeben. Das System verwendet den Pinsel zum Zeichnen des Hintergrunds des Bearbeitungs Steuer Elements.

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung einen Pinsel zurückgibt, den Sie erstellt hat (z. b. durch die Verwendung [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) [**kreatesolidbrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) " oder "-Funktion"), muss die Anwendung den Pinsel freigeben. Wenn die Anwendung einen System Pinsel zurückgibt (z. b. einen, der von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion oder der [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) -Funktion abgerufen wurde), muss die Anwendung den Pinsel nicht freigeben.

Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für das Bearbeitungs Steuerelement aus.

Schreibgeschützte oder deaktivierte Bearbeitungs Steuerelemente senden die **WM- \_ ctlcoloredit** -Nachricht nicht, sondern senden die " [**WM \_ ctlcolorstatic**](wm-ctlcolorstatic.md) "-Nachricht.

Die **WM- \_ ctlcoloredit** -Nachricht wird nie zwischen Threads gesendet, sondern nur innerhalb desselben Threads.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben. Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt. Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.

Umfassende **Bearbeitung:** Diese Meldung wird nicht unterstützt. Um die Hintergrundfarbe für ein Rich-Edit-Steuerelement festzulegen, verwenden Sie die Nachricht [**EM \_ setbkgndcolor**](em-setbkgndcolor.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ setbkgndcolor**](em-setbkgndcolor.md)
</dt> <dt>

[**WM \_ ctlcolorstatic**](wm-ctlcolorstatic.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

