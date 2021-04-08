---
title: WM_DRAWITEM Meldung (Winuser. h)
description: Wird an das übergeordnete Fenster einer vom Besitzer gezeichneten Schaltfläche, einem Kombinations Feld, einem Listenfeld oder einem Menü gesendet, wenn sich ein visueller Aspekt der Schaltfläche, des Kombinations Felds, des Listen Felds oder des Menüs geändert hat.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- Windows-Steuerelemente für WM_DRAWITEM Meldung
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741361"
---
# <a name="wm_drawitem-message"></a>WM- \_ DrawItem-Nachricht

Wird an das übergeordnete Fenster einer vom Besitzer gezeichneten Schaltfläche, einem Kombinations Feld, einem Listenfeld oder einem Menü gesendet, wenn sich ein visueller Aspekt der Schaltfläche, des Kombinations Felds, des Listen Felds oder des Menüs geändert hat.

Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Bezeichner des Steuer Elements an, das die **WM- \_ DrawItem** -Nachricht gesendet hat. Wenn die Nachricht von einem Menü gesendet wurde, ist dieser Parameter gleich 0 (null).

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur, die Informationen über das zu zeichende Element und den Typ der erforderlichen Zeichnung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.

## <a name="remarks"></a>Bemerkungen

Standardmäßig zeichnet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion das Fokus Rechteck für ein vom Besitzer gezeichnetes Listenfeld Element.

Der *itemaction* -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur gibt den Zeichnungs Vorgang an, den eine Anwendung ausführen soll.

Vor der Rückgabe aus der Verarbeitung dieser Nachricht muss eine Anwendung sicherstellen, dass der vom *hdc* -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur identifizierte Gerätekontext den Standardstatus aufweist.

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

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

