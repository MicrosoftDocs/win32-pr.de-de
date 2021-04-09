---
title: UDM_SETPOS Meldung (kommstrg. h)
description: Legt die aktuelle Position für ein auf-ab-Steuerelement mit 16-Bit-Genauigkeit fest.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- Windows-Steuerelemente für UDM_SETPOS Meldung
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104762"
---
# <a name="udm_setpos-message"></a>UDM- \_ SetPos-Nachricht

Legt die aktuelle Position für ein auf-ab-Steuerelement mit 16-Bit-Genauigkeit fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Neue Position für das auf-ab-Steuerelement. Wenn der Parameter außerhalb des angegebenen Bereichs des Steuer Elements liegt, wird *LPARAM* auf den nächstgelegenen gültigen Wert festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die vorherige Position.

## <a name="remarks"></a>Bemerkungen

Diese Meldung unterstützt nur 16-Bit-Positionen. Wenn 32-Bit-Werte für ein auf-ab-Steuerelement mit [**UDM- \_ SETRANGE32**](udm-setrange32.md)aktiviert wurden, verwenden Sie [**UDM \_ SETPOS32**](udm-setpos32.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**UDM- \_ GetRange**](udm-getrange.md)
</dt> <dt>

[**UDM- \_ GetPos**](udm-getpos.md)
</dt> </dl>

 

 





