---
description: Die updateendpointproxysettings-Struktur definiert die Proxy Einstellungen, die beim Anfordern eines Tokens verwendet werden.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Updateendpointproxysettings-Struktur (updateendpointauth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041781"
---
# <a name="updateendpointproxysettings-structure"></a>Updateendpointproxysettings-Struktur

Die **updateendpointproxysettings** -Struktur definiert die Proxy Einstellungen, die beim Anfordern eines Tokens verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a>Member

<dl> <dt>

**szproxyaddr**
</dt> <dd>

Der DNS-Name oder die IP-Adresse des zu verwendenden Proxy Servers (z. b. "Proxy.somecorp.com" oder "192.168.0.4") oder eine leere Zeichenfolge, wenn kein Proxy verwendet werden soll.

</dd> <dt>

**szbypasslist**
</dt> <dd>

Eine Liste von Host Adressen, die den Proxy Server umgehen sollen, oder eine leere Zeichenfolge, wenn alle Host Adressen den Proxy Server verwenden sollen.

WUA verwendet diese Daten nicht, wenn **szproxyaddr** leer ist.

</dd> <dt>

**szusername**
</dt> <dd>

Der Benutzername, der zur Authentifizierung beim Proxy Server verwendet wird, oder die leere Zeichenfolge, wenn keine Authentifizierung erforderlich ist.

WUA verwendet diese Daten nicht, wenn **szproxyaddr** leer ist.

</dd> <dt>

**szPassword**
</dt> <dd>

Das Kennwort, das für die Authentifizierung beim Proxy Server verwendet wird, oder die leere Zeichenfolge, wenn keine Authentifizierung erforderlich ist.

WUA verwendet diese Daten nicht, wenn **szproxyaddr** leer ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Updateendpointauth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Updateendpointauth. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getendpointtoken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




