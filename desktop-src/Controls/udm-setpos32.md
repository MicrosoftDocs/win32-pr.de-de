---
title: UDM_SETPOS32 Meldung (kommstrg. h)
description: Legt die Position eines auf-ab-Steuer Elements mit 32-Bit-Genauigkeit fest.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- Windows-Steuerelemente für UDM_SETPOS32 Meldung
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956791"
---
# <a name="udm_setpos32-message"></a>UDM \_ SETPOS32 Meldung

Legt die Position eines auf-ab-Steuer Elements mit 32-Bit-Genauigkeit fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Eine Variable vom Typ Integer, die die neue Position für das auf-ab-Steuerelement angibt. Wenn der-Parameter außerhalb des angegebenen Bereichs des Steuer Elements liegt, wird *LPARAM* auf den nächstgelegenen gültigen Wert festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Position zurück.

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

[**UDM- \_ GetPos**](udm-getpos.md)
</dt> <dt>

[**UDM- \_ SetPos**](udm-setpos.md)
</dt> <dt>

[**UDM \_ GETPOS32**](udm-getpos32.md)
</dt> </dl>

 

 





