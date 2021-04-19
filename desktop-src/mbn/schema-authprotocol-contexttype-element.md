---
description: Gibt das Authentifizierungsprotokoll an, das zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden soll.
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Authprotocol-Element (ContextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348768"
---
# <a name="authprotocol-contexttype-element"></a>Authprotocol-Element (ContextType)

Das **authprotocol (ContextType)** -Element gibt das Authentifizierungsprotokoll an, das zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden soll.

Das-Element kann einen der folgenden Werte aufweisen.

| Wert      | Bedeutung                                                                 |
|------------|-------------------------------------------------------------------------|
| Gar     | Kein Authentifizierungsprotokoll.                                             |
| PAP      | Unverschlüsselte Kenn Wort Authentifizierung.                                    |
| CHAP     | Challenge Handshake Authentication-Protokoll (CHAP).                      |
|  MsCHAPV2 | Verwenden Sie das Microsoft s Challenge Handshake Authentication-Protokoll (CHAP) v 2.0. |



 

Dieses Element ist optional und wird nur für GSM-Profile verwendet. Wenn das Element nicht angegeben und das Profil für ein GSM-Gerät verwendet wird, verwendet der Mobile Breitbanddienst den Wert **"None"**.

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **authprotocol** -Element wird durch den komplexen [**ContextType**](schema-contexttype-complextype.md) -Typ definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Kontext (mbnprofile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




