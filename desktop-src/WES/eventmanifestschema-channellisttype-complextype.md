---
title: Komplexer ChannelListType-Typ
description: Definiert eine Liste von Kanälen, an die Anbieter Ereignisse protokollieren können. | Komplexer ChannelListType-Typ
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- Komplexer ChannelListType-Typ EventLog
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8602594bdbdf6d39532213b0be660b5b3cfb6a90cd8281d9555ed2ff3a9d401
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121050"
---
# <a name="channellisttype-complex-type"></a>Komplexer ChannelListType-Typ

Definiert eine Liste von Kanälen, an die Anbieter Ereignisse protokollieren können.

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | Typ                                                                           | Beschreibung                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Kanal**](eventmanifestschema-channel-channellisttype-element.md)             | [**Channeltype**](eventmanifestschema-channeltype-complextype.md)             | Definiert einen Kanal, in dem Ereignisse protokolliert werden können.<br/>                                                                  |
| [**importChannel**](eventmanifestschema-importchannel-channellisttype-element.md) | [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md) | Identifiziert einen Kanal, der von einem anderen Anbieter oder in einem Manifest definiert wurde, das einen Metadatenabschnitt enthält.<br/> |



## <a name="remarks"></a>Hinweise

Sie können bis zu acht Kanäle angeben (eine beliebige Kombination aus importierten Kanälen oder Kanälen, die Sie definieren).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





