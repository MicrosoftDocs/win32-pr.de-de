---
title: EM_GETFIRSTVISIBLELINE Meldung (Winuser. h)
description: Ruft den NULL basierten Index der obersten sichtbaren Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- Windows-Steuerelemente für EM_GETFIRSTVISIBLELINE Meldung
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518302"
---
# <a name="em_getfirstvisibleline-message"></a>EM \_ getfirstvisibleline-Meldung

Ruft den NULL basierten Index der obersten sichtbaren Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Der Rückgabewert ist der null basierte Index der obersten sichtbaren Zeile in einem mehrzeiligen Bearbeitungs Steuerelement.

Steuer **Elemente bearbeiten:** Der Rückgabewert für einzeilige Bearbeitungs Steuerelemente ist der null basierte Index des ersten sichtbaren Zeichens.

**Rich Edit-Steuerelemente:** Für einzeilige Rich Edit-Steuerelemente ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Die Anzahl der Zeilen und die Länge der Zeilen in einem Bearbeitungs Steuerelement hängen von der Breite des Steuer Elements und der aktuellen WordWrap-Einstellung ab.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

 





