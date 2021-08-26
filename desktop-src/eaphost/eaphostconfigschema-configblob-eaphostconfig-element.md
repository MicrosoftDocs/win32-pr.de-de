---
title: ConfigBlob (EapHostConfig)-Element
description: Wird verwendet, wenn die Methodenkonfiguration in binärer BLOB-Form und nicht in Textzeichenfolgenform vorliegt.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- ConfigBlob-Element EAPHost
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
ms.openlocfilehash: 8f0d3b928ebc6cd24a6d7102ea37a8d0ae980c54499f568d25ca224b1121a20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021640"
---
# <a name="configblob-eaphostconfig-element"></a>ConfigBlob (EapHostConfig)-Element

Das **ConfigBlob -Element (EapHostConfig)** wird verwendet, wenn die Methodenkonfiguration in binärer BLOB-Form und nicht in Textzeichenfolgenform vorliegt.

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

Das **ConfigBlob-Element** wird durch das [**EapHostConfig-Element**](eaphostconfigschema-eaphostconfig-element.md) definiert.

## <a name="remarks"></a>Hinweise

Die [**Elemente Config**](eaphostconfigschema-config-eaphostconfig-element.md) und **ConfigBlob** können nicht gleichzeitig verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaphostconfig-Schema](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





