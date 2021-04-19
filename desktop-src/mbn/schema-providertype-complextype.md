---
description: Gibt Informationen über ein Mobilfunknetz an.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: komplexer ProviderType-Typ (mobiles Breitband)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356783"
---
# <a name="providertype-complex-type"></a>komplexer ProviderType-Typ

Der komplexe Typ **ProviderType** gibt Informationen zu einem Mobilfunknetz an.

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                          | type                                                           | BESCHREIBUNG               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [**ProviderID**](schema-providerid-providertype-element.md)     | [**provideridtype**](schema-provideridtype-simpletype.md)     | Anbieter-ID.<br/>   |
| [**ProviderName**](schema-providername-providertype-element.md) | [**providernametype**](schema-providernametype-simpletype.md) | Der Anbieter Name.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




