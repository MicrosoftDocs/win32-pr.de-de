---
description: Ruft die Netzwerkadressentypen ab, die ein angegebenes Netzwerkadressen-Steuerelement akzeptiert.
title: NCM_GETALLOWTYPE (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11b937ca851f00c51090683db4aebfc3db63cbf83efc95bad7a6f456d8f58988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858809"
---
# <a name="ncm_getallowtype-message"></a>NCM \_ GETALLOWTYPE-Nachricht

Ruft die Netzwerkadressentypen ab, die ein angegebenes Netzwerkadressen-Steuerelement akzeptiert.


```C++
NCM_GETALLOWTYPE

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

Gibt die zulässigen Netzwerkadressentypen als eine oder mehrere der [**NET \_ STRING-Konstanten**](net-string.md) zurück.

## <a name="remarks"></a>Hinweise

Die zurückgegebene Maske ist das Kriterium, mit dem eine Netzwerkadresse in der [**NCM \_ GETADDRESS-Nachricht überprüft**](ncm-getaddress.md) wird.

Verwenden Sie diese Meldung nur für ein Netzwerkadressen-Steuerelement. Verwenden Sie zum Instanziieren die in Shellapi.h definierte Klasse **msctls \_ netaddress.** Rufen [**Sie InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) zur Laufzeit auf, bevor Sie diese Nachricht senden. Dadurch wird die allgemeine Steuerelementbibliothek initialisiert, die das Netzwerkadressensteuerelemente enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




