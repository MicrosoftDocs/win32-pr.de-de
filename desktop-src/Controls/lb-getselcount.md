---
title: LB_GETSELCOUNT Meldung (Winuser.h)
description: Ruft die Gesamtzahl der ausgewählten Elemente in einem Listenfeld mit mehrfacher Auswahl ab.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- LB_GETSELCOUNT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8cacbf266931daaeba4a98c95c7c428630708d833af7603b0be09cef3071212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434110"
---
# <a name="lb_getselcount-message"></a>LB \_ GETSELCOUNT-Nachricht

Ruft die Gesamtzahl der ausgewählten Elemente in einem Listenfeld mit mehrfacher Auswahl ab.

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

Der Rückgabewert ist die Anzahl der ausgewählten Elemente im Listenfeld. Wenn das Listenfeld ein Listenfeld mit nur einer Auswahl ist, lautet der Rückgabewert LB \_ ERR.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





