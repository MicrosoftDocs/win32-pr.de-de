---
title: IPM_SETADDRESS Meldung (Commctrl.h)
description: Legt die Adresswerte für alle vier Felder im IP-Adresssteuerelement fest.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 54817d2206295432e9b477532268a000fc43047ae928ab02224d668912474519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434490"
---
# <a name="ipm_setaddress-message"></a>IPM \_ SETADDRESS-Nachricht

Legt die Adresswerte für alle vier Felder im IP-Adresssteuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein **DWORD-Wert,** der die neue Adresse enthält. Der Wert von Feld 3 ist in den Bits 0 bis 7 enthalten. Der Wert von Feld 2 ist in den Bits 8 bis 15 enthalten. Der Wert von Feld 1 ist in den Bits 16 bis 23 enthalten. Der Wert des Felds 0 ist in den Bits 24 bis 31 enthalten. Das [**MAKEIPADDRESS-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) kann auch zum Erstellen der Adressinformationen verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Diese Meldung generiert keine [**IPN \_ FIELDCHANGED-Benachrichtigung.**](ipn-fieldchanged.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





