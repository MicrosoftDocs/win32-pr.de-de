---
title: EM_SETREADONLY Meldung (Winuser. h)
description: Legt den schreibgeschützten Stil (es ist schreibgeschützt \_ ) eines Bearbeitungs Steuer Elements fest oder entfernt diesen. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Windows-Steuerelemente für EM_SETREADONLY Meldung
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
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103554"
---
# <a name="em_setreadonly-message"></a>EM- \_ Nachricht

Legt den schreibgeschützten Stil (es ist Schreib [**geschützt \_**](edit-control-styles.md)) eines Bearbeitungs Steuer Elements fest oder entfernt diesen. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob der es- [**Schreib \_**](edit-control-styles.md) geschützte Stil festgelegt oder entfernt werden soll. Mit dem Wert **true** wird der schreibgeschützte Stil ' es ' festgelegt; mit dem Wert ' **false** ' wird der schreibgeschützte Stil ' **es \_** ' entfernt **\_**

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn ein Bearbeitungs Steuerelement den [**Stil \_ "es**](edit-control-styles.md) schreibgeschützt" aufweist, kann der Benutzer den Text im Bearbeitungs Steuerelement nicht ändern.

Verwenden Sie die [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) -Funktion mit dem GWL-Style-Flag, um zu bestimmen, ob ein Bearbeitungs Steuer [**Element den schreibgeschützten \_ Schreib**](edit-control-styles.md) Stil hat \_ .

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

