---
title: EM_GETPASSWORDCHAR Meldung (Winuser. h)
description: Ruft das Kenn Wort Zeichen ab, das ein Bearbeitungs Steuerelement anzeigt, wenn der Benutzer Text eingibt. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- Windows-Steuerelemente für EM_GETPASSWORDCHAR Meldung
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859175"
---
# <a name="em_getpasswordchar-message"></a>EM \_ getpasswordchar-Meldung

Ruft das Kenn Wort Zeichen ab, das ein Bearbeitungs Steuerelement anzeigt, wenn der Benutzer Text eingibt. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Der Rückgabewert gibt das Zeichen an, das anstelle von Zeichen, die vom Benutzer eingegeben werden, angezeigt werden soll. Wenn der Rückgabewert **null** ist, gibt es kein Kenn Wort Zeichen, und das Steuerelement zeigt die vom Benutzer eingegebenen Zeichen an.

## <a name="remarks"></a>Bemerkungen

Wenn ein Bearbeitungs Steuerelement mit dem es-Kenn [**\_ Wort**](edit-control-styles.md) Stil erstellt wird, wird das standardmäßige Kenn Wort Zeichen auf ein Sternchen () festgelegt \* . Wenn ein Bearbeitungs Steuerelement ohne den es-Kenn **\_ Wort** Stil erstellt wird, gibt es kein Kenn Wort Zeichen. Um das Kenn Wort Zeichen zu ändern, senden Sie die Nachricht [**EM \_ setpasswordchar**](em-setpasswordchar.md) .

Steuer **Elemente bearbeiten:** Mehrzeilige Bearbeitungs Steuerelemente unterstützen das Kenn Wort Format oder die Nachrichten nicht.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 2,0 und höher unterstützt. Sowohl einzeilige als auch mehrzeilige Bearbeitungs Steuerelemente unterstützen den Kenn Wort Stil und die Nachrichten. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ setpasswordchar**](em-setpasswordchar.md)
</dt> </dl>

 

 





