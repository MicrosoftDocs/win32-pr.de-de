---
title: EM_GETFILELINECOUNT (CommCtrl.h)
description: Ruft die Anzahl der Zeilen in einem mehrzeilenigen Bearbeitungssteuerzeichen unabhängig davon ab, wie Zeilen auf dem Bildschirm angezeigt werden.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT meldungssteuerelemente Windows
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
ms.openlocfilehash: 28539af32212a699e12d2cf1d1787fa2e7aaa224f374eb6a63717279fcad16b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019678"
---
# <a name="em_getfilelinecount-message-commctrlh"></a>EM_GETFILELINECOUNT (CommCtrl.h)

Ruft die Anzahl der Zeilen in einem mehrzeilenigen Bearbeitungssteuerzeichen unabhängig davon ab, wie Zeilen auf dem Bildschirm angezeigt werden.

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

Der Rückgabewert ist eine ganze Zahl, die die Gesamtzahl der Textzeilen im mehrzeilenigen Bearbeitungssteuerfeld angibt, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden. Wenn das Steuerelement keinen Text enthält, ist der Rückgabewert 1. Der Rückgabewert ist nie kleiner als 1.

## <a name="remarks"></a>Hinweise

Die **MELDUNG \_ EM GETFILELINECOUNT** ruft die Gesamtzahl der Textzeilen ab, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden, und nicht nur die Anzahl der derzeit sichtbaren Zeilen.

Der Zeilenumbruch ändert nicht die Anzahl der Zeilen, die von dieser Meldung zurückgegeben werden, da diese Meldung unabhängig davon funktioniert, wie Zeilen auf dem Bildschirm angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETFILELINE**](em-getfileline.md)
</dt> <dt>

[**EM \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**Bearbeiten \_ von GetFileLineCount**](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





