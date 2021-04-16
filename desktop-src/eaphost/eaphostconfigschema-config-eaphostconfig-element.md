---
title: Config-Element (eaphostconfig)
description: Wird verwendet, wenn die Methoden Konfiguration im XML-Textformular statt in einem binären BLOB erfolgt.
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
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477169"
---
# <a name="config-eaphostconfig-element"></a>Config-Element (eaphostconfig)

Das Element **config (eaphostconfig)** wird verwendet, wenn die Methoden Konfiguration im XML-Textformular statt in einem binären BLOB erfolgt.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

Das **config** -Element wird durch das [**eaphostconfig**](eaphostconfigschema-eaphostconfig-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Die Elemente **config** und [**configblob**](eaphostconfigschema-configblob-eaphostconfig-element.md) können nicht gleichzeitig verwendet werden.

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

 

 





