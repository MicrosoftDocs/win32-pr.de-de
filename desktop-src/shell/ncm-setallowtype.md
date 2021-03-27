---
description: Legt die Netzwerk Adresstypen fest, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.
title: NCM_SETALLOWTYPE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753056"
---
# <a name="ncm_setallowtype-message"></a>NCM- \_ Nachricht vom Typ "logatlowtype"

Legt die Netzwerk Adresstypen fest, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*addrmask* \[ in\]
</dt> <dd>Gibt die Netzwerk Adresstypen als eine oder mehrere der <a href="net-string.md">**net \_ String**</a> -Konstanten an.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlerwert zurück.

## <a name="remarks"></a>Bemerkungen

Der Masken Satz ist das Kriterium, das verwendet wird, um eine Netzwerkadresse in der [**NCM- \_ GetAddress**](ncm-getaddress.md) -Nachricht zu überprüfen.

Verwenden Sie diese Meldung nur für ein Netzwerk Adress Steuerelement. Verwenden Sie zum Instanziieren die in shellapi. h definierte Klasse **msctls- \_ netaddress** . Ruft vor dem Senden dieser Nachricht [**initnetworkaddresscontrol**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) zur Laufzeit auf. Dadurch wird die Bibliothek der allgemeinen Steuerelemente initialisiert, die das Netzwerk Adress Steuerelement enthält.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NCM- \_ getallowtype**](ncm-getallowtype.md)
</dt> <dt>

[**NETADDR- \_ Typ**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




