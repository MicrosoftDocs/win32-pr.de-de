---
description: Zeigt eine Fehlermeldung in der Sprechblasen Info an, die dem Netzwerk Adress Steuerelement zugeordnet ist.
title: NCM_DISPLAYERRORTIP Meldung (shellapi. h)
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
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993775"
---
# <a name="ncm_displayerrortip-message"></a>NCM- \_ displayerrortip-Meldung

Zeigt eine Fehlermeldung in der Sprechblasen Info an, die dem Netzwerk Adress Steuerelement zugeordnet ist.


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

Wenn diese Nachricht erfolgreich ist, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Senden Sie diese Meldung, um eine Fehlermeldung anzuzeigen, wenn eine Adresse, die in das Steuerelement eingegeben wird, nicht anhand der zulässigen Netzwerk Adresstypen überprüft wird, die mit der [**NCM \_ setallowtype**](ncm-setallowtype.md) -Nachricht festgelegt Verwenden Sie die [**NCM \_ GetAddress**](ncm-getaddress.md) -Nachricht, um die Adresse zu überprüfen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NETADDR \_ displayerrortip**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




