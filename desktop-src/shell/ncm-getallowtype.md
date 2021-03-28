---
description: Ruft die Netzwerk Adresstypen ab, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.
title: NCM_GETALLOWTYPE Meldung (shellapi. h)
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
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041845"
---
# <a name="ncm_getallowtype-message"></a>NCM- \_ getallowtype-Nachricht

Ruft die Netzwerk Adresstypen ab, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.


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

Gibt die zulässigen Netzwerk Adresstypen als eine oder mehrere der [**net \_ String**](net-string.md) -Konstanten zurück.

## <a name="remarks"></a>Bemerkungen

Die zurückgegebene Maske ist das Kriterium, das verwendet wird, um eine Netzwerkadresse in der [**NCM \_ GetAddress**](ncm-getaddress.md) -Nachricht zu überprüfen.

Verwenden Sie diese Meldung nur für ein Netzwerk Adress Steuerelement. Verwenden Sie zum Instanziieren die in shellapi. h definierte Klasse **msctls- \_ netaddress** . Ruft vor dem Senden dieser Nachricht [**initnetworkaddresscontrol**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) zur Laufzeit auf. Dadurch wird die Bibliothek der allgemeinen Steuerelemente initialisiert, die das Netzwerk Adress Steuerelement enthält.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NCM- \_ Typ "Typ"**](ncm-setallowtype.md)
</dt> <dt>

[**NETADDR- \_ getallowtype**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




