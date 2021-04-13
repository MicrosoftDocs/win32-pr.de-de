---
description: Eine Anwendung sendet die WM- \_ mdicascade-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle untergeordneten Fenster in einem kaskadierenden Format anzuordnen.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: WM_MDICASCADE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343199"
---
# <a name="wm_mdicascade-message"></a>WM- \_ mdicascade-Nachricht

Eine Anwendung sendet die **WM- \_ mdicascade** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle untergeordneten Fenster in einem kaskadierenden Format anzuordnen.


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Überlappungsverhalten. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <dt>**Mditile \_ Überspringen**</dt> von <dt>0x0002</dt> </dl> | Verhindert, dass deaktivierte untergeordnete MDI-Fenster kaskadiert werden. <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <dt>**Mditile \_ ZOrder**</dt> <dt>0x0004</dt> </dl>                   | Ordnet die Fenster in der Z-Reihenfolge an.<br/>                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert " **true**".

Wenn die Meldung fehlschlägt, ist der Rückgabewert **false**.

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

[**WM- \_ mdiiconarrange**](wm-mdiiconarrange.md)
</dt> <dt>

[**WM- \_ mditile**](wm-mditile.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




