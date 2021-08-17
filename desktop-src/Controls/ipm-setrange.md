---
title: IPM_SETRANGE (Commctrl.h)
description: Legt den gültigen Bereich für das angegebene Feld im IP-Adresssteuerfeld fest.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- IPM_SETRANGE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d599619fa9a065a27a9721b890f6d52c496bf646504009e1950b7ca1279f8a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434470"
---
# <a name="ipm_setrange-message"></a>IPM \_ SETRANGE-Nachricht

Legt den gültigen Bereich für das angegebene Feld im IP-Adresssteuerfeld fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein nullbasierter Feldindex, auf den der Bereich angewendet wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein  WORD-Wert, der die untere Grenze des Bereichs im niedrigen Byte und die Obergrenze im hohen Byte enthält. Beide Werte sind inklusiv. Das [**MAKEIPRANGE-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) kann auch zum Erstellen des Bereichs verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Wenn der Benutzer einen Wert in das Feld ein gibt, das sich außerhalb dieses Bereichs befindet, sendet das Steuerelement die [IPN \_ FIELDCHANGED-Benachrichtigung](ipn-fieldchanged.md) mit dem eingegebenen Wert. Wenn der Wert nach dem Senden der Benachrichtigung noch außerhalb des Bereichs liegt, versucht das Steuerelement, den eingegebenen Wert in den nächstgelegenen Bereichsgrenzwert zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





