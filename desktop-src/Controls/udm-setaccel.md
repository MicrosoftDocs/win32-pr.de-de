---
title: UDM_SETACCEL Meldung (kommstrg. h)
description: Legt die Beschleunigung für ein auf-ab-Steuerelement fest.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- Windows-Steuerelemente für UDM_SETACCEL Meldung
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041005"
---
# <a name="udm_setaccel-message"></a>UDM- \_ SetAccel-Meldung

Legt die Beschleunigung für ein auf-ab-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl der von *aaccels* angegebenen [**udaccel**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) -Strukturen.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array von [**udaccel**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) -Strukturen, die Beschleunigungs Informationen enthalten. Elemente müssen in aufsteigender Reihenfolge basierend auf dem **nsec** -Member sortiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**UDM \_ GetAccel**](udm-getaccel.md)
</dt> </dl>

 

 





