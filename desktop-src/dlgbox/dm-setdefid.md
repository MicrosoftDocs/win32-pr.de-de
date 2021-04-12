---
title: DM_SETDEFID Meldung (Winuser. h)
description: Ändert den Bezeichner der Standard-pushschaltfläche für ein Dialogfeld.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- Dialog Felder DM_SETDEFID Meldung
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
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518878"
---
# <a name="dm_setdefid-message"></a>DM \_ -setdefid-Meldung

Ändert den Bezeichner der Standard-pushschaltfläche für ein Dialogfeld.


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner eines Push Button-Steuer Elements, das zum Standard wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist immer " **true**".

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird von der [**defdlgproc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) -Funktion verarbeitet. Um die Standard Schaltfläche Push festzulegen, kann die Funktion die Nachrichten [**WM \_ getdlgcode**](wm-getdlgcode.md) und [**BM \_ SetStyle**](../controls/bm-setstyle.md) an das angegebene Steuerelement und die aktuelle Standard-Schaltfläche Push senden.

Die Verwendung der **DM \_ setdefid-** Nachricht kann dazu führen, dass mehr als eine Schaltfläche den Standardzustand der pushschaltfläche aufweist. Wenn das System ein Dialogfeld öffnet, wird die erste Schaltfläche "Push" in der Dialogfeld Vorlage mit dem standardmäßigen Zustands Rahmen gezeichnet. Durch das Senden einer **DM \_ setdefid-** Meldung zum Ändern der Standard Schaltfläche wird nicht immer der standardmäßige Zustands Rahmen aus der ersten Schaltfläche "Push" entfernt. In diesen Fällen sollte die Anwendung eine BM- [**\_ SetStyle**](../controls/bm-setstyle.md) -Nachricht senden, um die Rahmenart der ersten pushschaltfläche zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Defdlgproc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ getdefid**](dm-getdefid.md)
</dt> <dt>

[**WM \_ getdlgcode**](wm-getdlgcode.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Dialog Felder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**BM- \_ SetStyle**](../controls/bm-setstyle.md)
</dt> <dt>

[**EM \_ SetLimitText**](../controls/em-setlimittext.md)
</dt> </dl>

 

