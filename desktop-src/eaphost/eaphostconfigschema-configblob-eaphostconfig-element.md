---
title: Configblob-Element (eaphostconfig)
description: Wird verwendet, wenn sich die Methoden Konfiguration im binären BLOB-Formular statt in Form einer Text Zeichenfolge befindet.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Configblob-Element EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739696"
---
# <a name="configblob-eaphostconfig-element"></a>Configblob-Element (eaphostconfig)

Das **configblob-Element (eaphostconfig)** wird verwendet, wenn sich die Methoden Konfiguration im binären BLOB-Formular statt in Form einer Text Zeichenfolge befindet.

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

Das **configblob** -Element wird durch das [**eaphostconfig**](eaphostconfigschema-eaphostconfig-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Die Elemente [**config**](eaphostconfigschema-config-eaphostconfig-element.md) und **configblob** können nicht gleichzeitig verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Eaphostconfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Eaphostconfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaphostconfig-Schema](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





