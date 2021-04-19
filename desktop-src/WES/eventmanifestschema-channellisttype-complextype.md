---
title: Komplexer channelellisttype-Typ
description: Definiert eine Liste von Kanälen, zu denen Anbieter Ereignisse protokollieren können. | Komplexer channelellisttype-Typ
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- Das Ereignisprotokoll des komplexen channelellisttype-Typs.
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361832"
---
# <a name="channellisttype-complex-type"></a>Komplexer channelellisttype-Typ

Definiert eine Liste von Kanälen, zu denen Anbieter Ereignisse protokollieren können.

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



| Element                                                                            | type                                                                           | BESCHREIBUNG                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Kanals**](eventmanifestschema-channel-channellisttype-element.md)             | [**ChannelType**](eventmanifestschema-channeltype-complextype.md)             | Definiert einen Kanal, zu dem Ereignisse protokolliert werden können.<br/>                                                                  |
| [**importchannel**](eventmanifestschema-importchannel-channellisttype-element.md) | [**Importchanneltype**](eventmanifestschema-importchanneltype-complextype.md) | Identifiziert einen Kanal, der von einem anderen Anbieter oder einem Manifest definiert wurde, das einen Metadatenabschnitt enthält.<br/> |



## <a name="remarks"></a>Bemerkungen

Sie können bis zu acht Kanäle angeben (eine beliebige Kombination aus importierten Kanälen oder Kanälen, die Sie definieren).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





