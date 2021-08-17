---
title: IPM_GETADDRESS Meldung (Commctrl.h)
description: Ruft die Adresswerte für alle vier Felder im IP-Adresssteuerelement ab.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- IPM_GETADDRESS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bcb35ed71532e815b33b45e1c15e9b82b75b5c87fac406b52de80670e3d72a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434511"
---
# <a name="ipm_getaddress-message"></a>IPM \_ GETADDRESS-Nachricht

Ruft die Adresswerte für alle vier Felder im IP-Adresssteuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen **DWORD-Wert,** der die Adresse empfängt. Der Wert von Feld 3 ist in den Bits 0 bis 7 enthalten. Der Wert von Feld 2 ist in den Bits 8 bis 15 enthalten. Der Wert von Feld 1 ist in den Bits 16 bis 23 enthalten. Der Wert von Feld 0 ist in den Bits 24 bis 31 enthalten. Die Makros [**FIRST \_ IPADDRESS,**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress) [**SECOND \_ IPADDRESS,**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) [**THIRD \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)und [**FOURTH \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) können auch verwendet werden, um die Adressinformationen zu extrahieren. 0 (null) wird als Adresse für alle leeren Felder zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl nicht leerer Felder zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





