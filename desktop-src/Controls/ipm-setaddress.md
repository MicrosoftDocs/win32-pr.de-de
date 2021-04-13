---
title: IPM_SETADDRESS Meldung (kommstrg. h)
description: Legt die Adress Werte für alle vier Felder im IP-Adress Steuerelement fest.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- Windows-Steuerelemente für IPM_SETADDRESS Meldung
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104463"
---
# <a name="ipm_setaddress-message"></a>IPM- \_ setAddress-Nachricht

Legt die Adress Werte für alle vier Felder im IP-Adress Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein **DWORD** -Wert, der die neue Adresse enthält. Der Wert von Feld 3 ist in Bits 0 bis 7 enthalten. Der Wert für Feld 2 ist in Bits 8 bis 15 enthalten. Der Wert für Feld 1 ist in Bits 16 bis 23 enthalten. Der Wert Feld 0 ist in Bits 24 bis 31 enthalten. Das [**MakeIPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) -Makro kann auch zum Erstellen der Adressinformationen verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Diese Meldung generiert keine [**IPN \_ FieldChanged**](ipn-fieldchanged.md) -Benachrichtigung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





