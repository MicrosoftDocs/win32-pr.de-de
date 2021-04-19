---
description: Gibt an, ob die 802.1 x-Authentifizierung verwendet wird.
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: useonex-Element (authencryption)
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
ms.openlocfilehash: cb327be4006e8da0074815a74e49d3ccdc5d3c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363538"
---
# <a name="useonex-authencryption-element"></a>useonex-Element (authencryption)

Das useonex-Element (authencryption) gibt an, ob die 802.1 x-Authentifizierung verwendet wird.

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

Das-Element wird durch das [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element definiert.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **useonex** -Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**authencryption (Sicherheit)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




