---
title: EM_SETREADONLY (Winuser.h)
description: Legt den schreibgeschützten Stil (ES READONLY) eines Bearbeitungssteuer steuerelements fest \_ oder entfernt ihn. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETREADONLY meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d46726c1247f7ef93c00e495ca77ad3d337253705bd3018a0480fc9588c22f8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437510"
---
# <a name="em_setreadonly-message"></a>EM \_ SETREADONLY-Nachricht

Legt den schreibgeschützten Stil [**(ES \_ READONLY)**](edit-control-styles.md)eines Bearbeitungssteuersets fest oder entfernt ihn. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob der [**ES \_ READONLY-Stil festgelegt oder entfernt werden**](edit-control-styles.md) soll. Der Wert **TRUE legt** den ES **\_ READONLY-Stil** fest. Der Wert **FALSE** entfernt den **ES \_ READONLY-Stil.**

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ungleich null.

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Wenn ein Bearbeitungssteuerfeld über [**den STIL ES \_ READONLY**](edit-control-styles.md) verfügt, kann der Benutzer den Text innerhalb des Bearbeitungssteuerfelds nicht ändern.

Verwenden Sie die [**GetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) mit dem GWL STYLE-Flag, um zu bestimmen, ob ein Bearbeitungssteuerzeichen den [**STIL ES \_ READONLY**](edit-control-styles.md) \_ aufweise.

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

