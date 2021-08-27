---
description: Zeigt eine Fehlermeldung in der Sprechblasenspitze an, die dem Netzwerkadressen-Steuerelement zugeordnet ist.
title: NCM_DISPLAYERRORTIP (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 046119c93ec6a80fcfcedbd562d04665d5642fd832f2385bab914cc732499e5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111470"
---
# <a name="ncm_displayerrortip-message"></a>NCM \_ DISPLAYERRORTIP-Meldung

Zeigt eine Fehlermeldung in der Sprechblasenspitze an, die dem Netzwerkadressen-Steuerelement zugeordnet ist.


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Meldung erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Senden Sie diese Meldung, um eine Fehlermeldung anzuzeigen, wenn eine in das Steuerelement typifizierte Adresse nicht anhand der zulässigen Netzwerkadressentypen überprüft wird, die mit der [**NCM \_ SETALLOWTYPE-Meldung festgelegt**](ncm-setallowtype.md) wurden. Verwenden Sie die [**NCM \_ GETADDRESS-Nachricht,**](ncm-getaddress.md) um die Adresse zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**NetAddr \_ DisplayErrorTip**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




