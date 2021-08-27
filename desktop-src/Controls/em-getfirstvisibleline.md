---
title: EM_GETFIRSTVISIBLELINE (Winuser.h)
description: Ruft den nullbasierten Index der obersten sichtbaren Zeile in einem mehrzeilenbasierten Bearbeitungssteuerteil ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- EM_GETFIRSTVISIBLELINE meldungssteuerelemente Windows
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
ms.openlocfilehash: 11eb93c1c7dcce7f502945df4e063b22c29514bc79fe7310875e9de055e1d745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049210"
---
# <a name="em_getfirstvisibleline-message"></a>EM \_ GETFIRSTVISIBLELINE-Nachricht

Ruft den nullbasierten Index der obersten sichtbaren Zeile in einem mehrzeilenbasierten Bearbeitungssteuerteil ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

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

Der Rückgabewert ist der nullbasierte Index der obersten sichtbaren Zeile in einem mehrzeilenbasierten Bearbeitungssteuerteil.

**Steuerelemente bearbeiten:** Bei einzeilenbasierten Bearbeitungssteuerelementen ist der Rückgabewert der nullbasierte Index des ersten sichtbaren Zeichens.

**Umfangreiche Bearbeitungssteuerelemente:** Bei einzeilenbasierten Rich-Edit-Steuerelementen ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Die Anzahl der Zeilen und die Länge der Zeilen in einem Bearbeitungssteuerzeichen hängen von der Breite des Steuerelements und der aktuellen Wordwrap-Einstellung ab.

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

 





