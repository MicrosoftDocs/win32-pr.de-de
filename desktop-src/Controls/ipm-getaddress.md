---
title: IPM_GETADDRESS Meldung (kommstrg. h)
description: Ruft die Adress Werte für alle vier Felder im IP-Adress Steuerelement ab.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- Windows-Steuerelemente für IPM_GETADDRESS Meldung
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
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956724"
---
# <a name="ipm_getaddress-message"></a>IPM- \_ GetAddress-Nachricht

Ruft die Adress Werte für alle vier Felder im IP-Adress Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die Adresse empfängt. Der Wert für Feld 3 ist in Bits 0 bis 7 enthalten. Der Wert für Feld 2 ist in Bits 8 bis 15 enthalten. Der Wert für Feld 1 ist in Bits 16 bis 23 enthalten. Der Wert Feld 0 ist in Bits 24 bis 31 enthalten. Die [**erste \_ IP-Adresse**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), die [**zweite \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress)-, [**dritte \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)-und [**vierte \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) -Makros können auch zum Extrahieren der Adressinformationen verwendet werden. NULL wird als Adresse für alle leeren Felder zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der nicht leeren Felder zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





