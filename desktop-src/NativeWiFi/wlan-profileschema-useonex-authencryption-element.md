---
description: Gibt an, ob die 802.1X-Authentifizierung verwendet wird.
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: useOneX-Element (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 961f1b6be52da97ada2c230579ac281652a07fcbae67ac32d2399eb2968b1946
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912570"
---
# <a name="useonex-authencryption-element"></a>useOneX-Element (authEncryption)

Das useOneX-Element (authEncryption) gibt an, ob die 802.1X-Authentifizierung verwendet wird.

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

Das -Element wird durch das [**authEncryption-Element**](wlan-profileschema-authencryption-security-element.md) definiert.

## <a name="examples"></a>Beispiele

Beispielprofile, die das **useOneX-Element** verwenden, finden Sie unter [Beispiele für Funkprofile.](wireless-profile-samples.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**authEncryption (Sicherheit)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




