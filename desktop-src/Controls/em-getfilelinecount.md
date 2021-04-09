---
title: EM_GETFILELINECOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungs Steuerelement ab, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Windows-Steuerelemente für EM_GETFILELINECOUNT Meldung
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104834"
---
# <a name="em_getfilelinecount-message-commctrlh"></a>EM_GETFILELINECOUNT Meldung (kommstrg. h)

Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungs Steuerelement ab, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.

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

Der Rückgabewert ist eine ganze Zahl, die die Gesamtzahl der Textzeilen im mehrzeiligen Bearbeitungs Steuerelement angibt, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden. Wenn das Steuerelement keinen Text hat, ist der Rückgabewert 1. Der Rückgabewert ist nie kleiner als 1.

## <a name="remarks"></a>Bemerkungen

Die **EM \_ getfilelinecount** -Nachricht Ruft die Gesamtanzahl von Textzeilen ab, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden, nicht nur die Anzahl der zurzeit sichtbaren Zeilen.

Der Zeilenumbruch ändert nicht die Anzahl der Zeilen, die von dieser Nachricht zurückgegeben werden, da diese Nachricht unabhängig davon funktioniert, wie Zeilen auf dem Bildschirm angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ getfileline**](em-getfileline.md)
</dt> <dt>

[**EM \_ filelinelength**](em-filelinelength.md)
</dt> <dt>

[**" \_ Getfilelinecount" Bearbeiten**](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





