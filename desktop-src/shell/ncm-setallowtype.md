---
description: Legt die Netzwerkadressentypen fest, die ein angegebenes Netzwerkadressen-Steuerelement akzeptiert.
title: NCM_SETALLOWTYPE (Shellapi.h)
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
ms.openlocfilehash: d3fc6b8ceb848d4738ff2d77b4441a29354bf09248e0de88008072dbf867e8a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719924"
---
# <a name="ncm_setallowtype-message"></a>NCM \_ SETALLOWTYPE-Meldung

Legt die Netzwerkadressentypen fest, die ein angegebenes Netzwerkadressen-Steuerelement akzeptiert.


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*addrMask* \[ In\]
</dt> <dd>Gibt die Netzwerkadressentypen als eine oder mehrere der <a href="net-string.md">**NET \_ STRING-Konstanten**</a> an.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder andernfalls einen Fehlerwert.

## <a name="remarks"></a>Hinweise

Der Maskensatz ist das Kriterium, mit dem eine Netzwerkadresse in der [**NCM \_ GETADDRESS-Nachricht überprüft**](ncm-getaddress.md) wird.

Verwenden Sie diese Meldung nur für ein Netzwerkadressen-Steuerelement. Verwenden Sie zum Instanziieren die in Shellapi.h definierte Klasse **msctls \_ netaddress.** Rufen [**Sie InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) zur Laufzeit auf, bevor Sie diese Nachricht senden. Dadurch wird die allgemeine Steuerelementbibliothek initialisiert, die das Netzwerkadressensteuerelemente enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




