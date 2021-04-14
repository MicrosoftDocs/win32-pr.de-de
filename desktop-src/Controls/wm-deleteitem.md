---
title: WM_DELETEITEM Meldung (Winuser. h)
description: Wird an den Besitzer eines Listen Felds oder Kombinations Felds gesendet, wenn das Listenfeld oder Kombinations Feld zerstört wird oder wenn Elemente von der LB- \_ deletestring-, lb \_ resetcontent-, CB \_ deletestring-oder CB \_ resetcontent-Nachricht entfernt werden.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- Windows-Steuerelemente für WM_DELETEITEM Meldung
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
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476473"
---
# <a name="wm_deleteitem-message"></a>WM \_ DeleteItem-Meldung

Wird an den Besitzer eines Listen Felds oder Kombinations Felds gesendet, wenn das Listenfeld oder Kombinations Feld zerstört wird oder wenn Elemente von der [**lb- \_ deletestring**](lb-deletestring.md)- [**, lb \_ resetcontent**](lb-resetcontent.md)-, [**CB \_ deletestring**](cb-deletestring.md)-oder [**CB \_ resetcontent**](cb-resetcontent.md) -Nachricht entfernt werden. Das System sendet eine " **WM \_ DeleteItem** "-Meldung für jedes gelöschte Element. Das System sendet die " **WM \_ DeleteItem** "-Meldung für ein beliebiges gelöschtes Listenfeld oder Kombinations Feld Element mit Elementdaten, die nicht NULL sind.


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Bezeichner des Steuer Elements an, das die **WM- \_ DeleteItem** -Nachricht gesendet hat.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**deleteitemstruct**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) -Struktur, die Informationen über das Element enthält, das aus einem Listenfeld gelöscht wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte **true** zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Microsoft Windows NT und höher: Windows sendet eine **WM \_ DeleteItem** -Nachricht nur für Elemente, die aus einem von einem Besitzer gezeichneten Listenfeld (mit dem "lbs-Besitzer" oder "lbs-Besitzer"-Stil) oder dem vom Besitzer gezeichneten Kombinations Feld (mit dem [**CBS \_**](combo-box-styles.md) -Besitzer-oder [**CBS \_**](combo-box-styles.md) -Besitzer-Stil) gelöscht wurden. [**\_**](list-box-styles.md) [**\_**](list-box-styles.md)

Windows 95: Windows sendet die " **WM \_ DeleteItem** "-Meldung für ein beliebiges gelöschtes Listenfeld oder Kombinations Feld Element mit Elementdaten, die nicht NULL sind.

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

[**CB \_ deletestring**](cb-deletestring.md)
</dt> <dt>

[**CB \_ resetcontent**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**LB- \_ deletestring**](lb-deletestring.md)
</dt> <dt>

[**LB- \_ resetcontent**](lb-resetcontent.md)
</dt> </dl>

 

 





