---
title: DM_SETDEFID (Winuser.h)
description: Ändert den Bezeichner der Standardschaltfläche für ein Dialogfeld.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- DM_SETDEFID meldungsdialogfelder
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92749cc7eca569b57d239a36bb6559e59a6a7ebc31c63787a93d0720b334d1ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741750"
---
# <a name="dm_setdefid-message"></a>DM \_ SETDEFID-Nachricht

Ändert den Bezeichner der Standardschaltfläche für ein Dialogfeld.


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner eines Schaltflächen-Steuerelements, das zum Standard wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist immer **TRUE.**

## <a name="remarks"></a>Hinweise

Diese Nachricht wird von der [**DefDlgProc-Funktion**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) verarbeitet. Zum Festlegen der Standardschaltfläche kann die Funktion [**WM \_ GETDLGCODE-**](wm-getdlgcode.md) und [**BM \_ SETSTYLE-Nachrichten**](../controls/bm-setstyle.md) an das angegebene Steuerelement und die aktuelle Standardschaltfläche senden.

Die Verwendung **der DM \_ SETDEFID-Nachricht** kann dazu führen, dass mehrere Schaltflächen den Standardzustand der Pushschaltfläche haben. Wenn das System einen Dialog öffnet, zeichnet es die erste Pushschaltfläche in der Dialogvorlage mit dem Standardzustands border. Wenn Sie eine **DM \_ SETDEFID-Nachricht** senden, um die Standardschaltfläche zu ändern, wird der Standardzustandsgrenzgrad nicht immer von der ersten Pushschaltfläche entfernt. In diesen Fällen sollte die Anwendung eine [**BM \_ SETSTYLE-Nachricht**](../controls/bm-setstyle.md) senden, um den Rahmenstil der ersten Schaltfläche zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ GETDEFID**](dm-getdefid.md)
</dt> <dt>

[**WM \_ GETDLGCODE**](wm-getdlgcode.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Dialogfelder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**BM \_ SETSTYLE**](../controls/bm-setstyle.md)
</dt> <dt>

[**EM \_ SETLIMITTEXT**](../controls/em-setlimittext.md)
</dt> </dl>

 

