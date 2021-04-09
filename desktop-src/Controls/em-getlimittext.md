---
title: EM_GETLIMITTEXT Meldung (Winuser. h)
description: Ruft den aktuellen Text Grenzwert für ein Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- Windows-Steuerelemente für EM_GETLIMITTEXT Meldung
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858688"
---
# <a name="em_getlimittext-message"></a>EM \_ getlimittext-Nachricht

Ruft den aktuellen Text Grenzwert für ein Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist das Text Limit.

## <a name="remarks"></a>Bemerkungen

**Bearbeitungs Steuerelemente, umfassende Bearbeitung 2,0 und höher:** Das Text Limit ist die maximale Text Menge in **TCHAR** s, die das Steuerelement enthalten kann. Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen. Zwei Dokumente mit der gleichen Zeichen Beschränkung führen zu demselben Text Limit, auch wenn "ANSI" und das andere "Unicode" sind.

**Rich Edit 1,0:** Das Text Limit ist die maximale Menge an Text (in Bytes), die das Rich Edit-Steuerelement enthalten kann.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ SetLimitText**](em-setlimittext.md)
</dt> </dl>

 

 





