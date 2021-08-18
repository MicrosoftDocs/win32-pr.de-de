---
title: WM_DELETEITEM (Winuser.h)
description: Wird an den Besitzer eines Listen- oder Kombinationsfelds gesendet, wenn das Listenfeld oder Kombinationsfeld zerstört wird oder wenn Elemente von der LB \_ DELETESTRING-, LB \_ RESETCONTENT-, CB \_ DELETESTRING- oder CB RESETCONTENT-Meldung entfernt \_ werden.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f461b63d751822d9a4c602993314bf0677cff754881269ab44458ab17f3a439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018538"
---
# <a name="wm_deleteitem-message"></a>WM \_ DELETEITEM-Nachricht

Wird an den Besitzer eines Listen- oder Kombinationsfelds gesendet, wenn das Listenfeld oder Kombinationsfeld zerstört wird oder wenn Elemente von der [**LB \_ DELETESTRING-,**](lb-deletestring.md) [**LB \_ RESETCONTENT-,**](lb-resetcontent.md) [**CB \_ DELETESTRING-**](cb-deletestring.md)oder [**CB \_ RESETCONTENT-Meldung**](cb-resetcontent.md) entfernt werden. Das System sendet für jedes gelöschte Element eine **WM \_ DELETEITEM-Nachricht.** Das System sendet die **WM \_ DELETEITEM-Nachricht** für jedes gelöschte Listenfeld oder Kombinationsfeldelement mit Elementdaten ungleich 0 (null).


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Bezeichner des Steuerelements an, das die **WM \_ DELETEITEM-Nachricht gesendet** hat.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**DELETEITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) die Informationen über das aus einem Listenfeld gelöschte Element enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte **TRUE zurückgeben,** wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Microsoft Windows NT und höher: Windows sendet eine **WM \_ DELETEITEM-Nachricht** nur für Elemente, die aus einem vom Besitzer gezeichneten Listenfeld (mit dem [**LBS \_ OWNERDRAWFIXED-**](list-box-styles.md) oder [**LBS \_ OWNERDRAWVARIABLE-Stil)**](list-box-styles.md) oder einem vom Besitzer gezeichneten Kombinationsfeld (mit dem [**CBS \_ OWNERDRAWFIXED-**](combo-box-styles.md) oder [**CBS \_ OWNERDRAWVARIABLE-Stil)**](combo-box-styles.md) gelöscht wurden.

Windows 95: Windows sendet die **WM \_ DELETEITEM-Nachricht** für jedes gelöschte Listenfeld oder Kombinationsfeldelement mit Elementdaten ungleich null.

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

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ RESETCONTENT**](lb-resetcontent.md)
</dt> </dl>

 

 





