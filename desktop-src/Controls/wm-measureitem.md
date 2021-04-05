---
title: WM_MEASUREITEM Meldung (Winuser. h)
description: Wird an das Besitzer Fenster eines Kombinations Felds, eines Listen Felds, eines Listenansicht-Steuer Elements oder eines Menü Elements gesendet, wenn das Steuerelement oder das Menü erstellt wird.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- Windows-Steuerelemente für WM_MEASUREITEM Meldung
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859046"
---
# <a name="wm_measureitem-message"></a>WM \_ MeasureItem-Meldung

Wird an das Besitzer Fenster eines Kombinations Felds, eines Listen Felds, eines Listenansicht-Steuer Elements oder eines Menü Elements gesendet, wenn das Steuerelement oder das Menü erstellt wird.

Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Wert des **ctlid** -Members der [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, auf die durch den *LPARAM* -Parameter verwiesen wird. Dieser Wert identifiziert das Steuerelement, das die **WM \_ MeasureItem** -Nachricht gesendet hat. Wenn der Wert 0 (null) ist, wurde die Nachricht von einem Menü gesendet. Wenn der Wert ungleich 0 (null) ist, wurde die Nachricht von einem Kombinations Feld oder einem Listenfeld gesendet. Wenn der Wert ungleich 0 (null) ist und der Wert des **ItemID** -Members der **measureitemstruct** , auf den *LPARAM* zeigt, (uint) 1 ist, wurde die Nachricht von einem Kombinations Feld für die Bearbeitung gesendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, die die Dimensionen des vom Besitzer gezeichneten Steuer Elements oder Menü Elements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn das Besitzer Fenster die " **WM \_ MeasureItem** "-Meldung empfängt, füllt der Besitzer die [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur aus, auf die der *LPARAM* -Parameter der Nachricht verweist, und gibt zurück. Dadurch wird das System über die Abmessungen des Steuer Elements informiert. Wenn ein Listenfeld oder Kombinations Feld mit der lbs- [**Besitzer \_ drawvariable**](list-box-styles.md) oder dem [**CBS \_**](combo-box-styles.md) -Besitzer der Eigenschaft "Besitzer" erstellt wird, wird diese Nachricht an den Besitzer für jedes Element im Steuerelement gesendet. andernfalls wird diese Nachricht einmal gesendet.

Das System sendet die **WM- \_ Datei "MeasureItem** " an das Fenster "Besitzer" der Kombinations Felder und Listenfelder, die mit der "besitzdrawfixed"-Formatvorlage erstellt werden, bevor die " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) Wenn der Besitzer diese Nachricht empfängt, hat das System die Höhe und Breite der im Steuerelement verwendeten Schriftart noch nicht bestimmt. Funktionsaufrufe und Berechnungen, die diese Werte erfordern, sollten in der Hauptfunktion der Anwendung oder der Bibliothek auftreten.

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

[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

