---
title: Config-Element (EapHostConfig)
description: Wird verwendet, wenn die Methodenkonfiguration in XML-Textform und nicht in einem binären BLOB vor sich geht.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Config-Element EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba798afaa418e5de49c48abdc8dac242a300a7228ffe27a76241f4cbabed5833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739080"
---
# <a name="config-eaphostconfig-element"></a>Config-Element (EapHostConfig)

Das **Config-Element (EapHostConfig)** wird verwendet, wenn die Methodenkonfiguration in XML-Textform und nicht in einem binären BLOB vor sich geht.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

Das **Config-Element** wird durch das [**EapHostConfig-Element**](eaphostconfigschema-eaphostconfig-element.md) definiert.

## <a name="remarks"></a>Hinweise

Die **Elemente Config** und [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) können nicht gleichzeitig verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

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

 

 





