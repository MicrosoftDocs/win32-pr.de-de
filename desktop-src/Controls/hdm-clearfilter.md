---
title: HDM_CLEARFILTER Meldung (kommstrg. h)
description: Löscht den Filter für ein bestimmtes Header-Steuerelement. Sie können diese Nachricht explizit senden oder das Header \_ ClearFilter-Makro verwenden.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- Windows-Steuerelemente für HDM_CLEARFILTER Meldung
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104492"
---
# <a name="hdm_clearfilter-message"></a>HDM \_ ClearFilter-Meldung

Löscht den Filter für ein bestimmtes Header-Steuerelement. Sie können diese Nachricht explizit senden oder das [**Header \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Spaltenwert, der angibt, welcher Filter gelöscht werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück. Das **LRESULT** wird in eine ganze Zahl umgewandelt, die **true**(1) oder **false**(0) angibt.

## <a name="remarks"></a>Bemerkungen

Wenn der Spaltenwert als-1 angegeben wird, werden alle Filter gelöscht, und die [Hdn-Filter \_ Änderungs](hdn-filterchange.md) Benachrichtigung wird nur einmal gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_ClearAllFilters-Header**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





