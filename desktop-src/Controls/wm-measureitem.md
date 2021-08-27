---
title: WM_MEASUREITEM (Winuser.h)
description: Wird beim Erstellen des Steuerelements oder Menüs an das Besitzerfenster eines Kombinationsfelds, Listenfelds, Listenansicht-Steuerelements oder Menüelements gesendet.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- WM_MEASUREITEM von Windows-Steuerelementen
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
ms.openlocfilehash: 7eae57fc163f19edcef6dc924072cd3389146b66e614b61d6f121237e82e1344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957509"
---
# <a name="wm_measureitem-message"></a>WM \_ MEASUREITEM-Meldung

Wird beim Erstellen des Steuerelements oder Menüs an das Besitzerfenster eines Kombinationsfelds, Listenfelds, Listenansicht-Steuerelements oder Menüelements gesendet.

Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Wert des **CtlID-Members** der [**MEASUREITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) auf die der *lParam-Parameter* zeigt. Dieser Wert identifiziert das Steuerelement, das die **WM \_ MEASUREITEM-Nachricht gesendet** hat. Wenn der Wert 0 (null) ist, wurde die Nachricht von einem Menü gesendet. Wenn der Wert ungleich 0 (null) ist, wurde die Nachricht von einem Kombinationsfeld oder einem Listenfeld gesendet. Wenn der Wert ungleich 0 (null) ist und der Wert des **itemID-Elements** der **MEASUREITEMSTRUCT,** auf die *lParam* zeigt, (UINT) 1 ist, wurde die Nachricht durch ein Kombinationsfeld für die Bearbeitung gesendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**MEASUREITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) die die Dimensionen des vom Besitzer gezeichneten Steuerelements oder Menüelements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE zurückgeben.**

## <a name="remarks"></a>Hinweise

Wenn das Besitzerfenster die **WM \_ MEASUREITEM-Meldung** empfängt, füllt der Besitzer die [**MEASUREITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) aus, auf die der *lParam-Parameter* der Nachricht zeigt, und gibt zurück. Dadurch wird das System über die Dimensionen des Steuerelements informiert. Wenn ein Listen- oder Kombinationsfeld mit dem [**Format LBS \_ OWNERDRAWVARIABLE**](list-box-styles.md) oder [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) erstellt wird, wird diese Nachricht für jedes Element im Steuerelement an den Besitzer gesendet. Andernfalls wird diese Nachricht einmal gesendet.

Das System sendet die **WM \_ MEASUREITEM-Nachricht** an das Besitzerfenster von Kombinationsfeldern und Listenfeldern, die mit dem OWNERDRAWFIXED-Format erstellt wurden, bevor die [**WM \_ INITDIALOG-Nachricht gesendet**](/windows/desktop/dlgbox/wm-initdialog) wird. Wenn der Besitzer diese Nachricht empfängt, hat das System daher noch nicht die Höhe und Breite der im Steuerelement verwendeten Schriftart bestimmt. Funktionsaufrufe und Berechnungen, die diese Werte erfordern, sollten in der Hauptfunktion der Anwendung oder Bibliothek erfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

