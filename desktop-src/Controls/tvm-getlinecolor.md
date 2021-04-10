---
title: TVM_GETLINECOLOR Meldung (kommstrg. h)
description: Die TVM \_ getLineColor-Meldung Ruft die aktuelle Linien Farbe ab.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- Windows-Steuerelemente für TVM_GETLINECOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040757"
---
# <a name="tvm_getlinecolor-message"></a>TVM \_ getLineColor-Meldung

Die **TVM \_ getLineColor** -Meldung Ruft die aktuelle Linien Farbe ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die aktuelle Linien Farbe oder den CLR- \_ Standardwert zurück, wenn kein Wert angegeben wurde.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ruft nur Linien Farben ab. Um die Farben von "+" und "-" in den Schaltflächen abzurufen, verwenden Sie die [**TVM \_ gettextcolor**](tvm-gettextcolor.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ setlinecolor**](tvm-setlinecolor.md)
</dt> </dl>

 

 





