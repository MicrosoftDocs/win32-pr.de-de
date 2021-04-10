---
title: IPM_SETRANGE Meldung (kommstrg. h)
description: Legt den gültigen Bereich für das angegebene Feld im IP-Adress Steuerelement fest.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- Windows-Steuerelemente für IPM_SETRANGE Meldung
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
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040856"
---
# <a name="ipm_setrange-message"></a>IPM- \_ Nachricht

Legt den gültigen Bereich für das angegebene Feld im IP-Adress Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein NULL basierter Feld Index, auf den der Bereich angewendet wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **Word** -Wert, der die untere Grenze des Bereichs in dem nieder wertigen Byte und die Obergrenze im höherwertigen Byte enthält. Beide Werte sind inklusiv. Das [**makeiprange**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) -Makro kann auch verwendet werden, um den Bereich zu erstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer einen Wert in das Feld eingibt, der außerhalb dieses Bereichs liegt, sendet das Steuerelement die [IPN \_ FieldChanged](ipn-fieldchanged.md) -Benachrichtigung mit dem eingegebenen Wert. Wenn der Wert nach dem Senden der Benachrichtigung noch außerhalb des Bereichs liegt, versucht das Steuerelement, den eingegebenen Wert in den nächstgelegenen Bereichs Grenzwert zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





