---
description: Gibt die maximale Anzahl von Authentifizierungsfehlern an, die für einen Satz von Anmeldeinformationen zulässig sind.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: maxAuthFailures (OneX)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9cb48479b2fe26ecb2667812cc6ee2048226c0665c25b12e25e8c7edbc35dac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800780"
---
# <a name="maxauthfailures-onex-element"></a>maxAuthFailures (OneX)-Element

Das Element maxAuthFailures (OneX) gibt die maximale Anzahl von Authentifizierungsfehlern an, die für einen Satz von Anmeldeinformationen zulässig sind.

Dieses Element ist optional. Wenn maxAuthFailures nicht in einem Profil angegeben ist, wird der Wert 1 verwendet.

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="maxAuthFailures">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **maxAuthFailures-Element** wird durch das [**OneX-Element**](onexschema-onex-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




