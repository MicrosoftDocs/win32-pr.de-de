---
description: Definiert die hostingmetadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: hostmetadata-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359536"
---
# <a name="hostmetadata-element"></a>hostmetadata-Element

Definiert die hostingmetadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.

## <a name="usage"></a>Verbrauch

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Host**](host.md)<br/>     | Definiert die serviceid-und [**types**](types.md) -Elemente für den Dienst Host. Wenn Sie nicht explizit bereitgestellt werden, stellt WSDAPI keine Standarddaten als Antwort auf Metadatenanforderungen bereit.<br/> <br/>                                                                                                                                          |
| [**gehostet**](hosted.md)<br/> | Definiert die [**serviceid**](serviceid.md) -und [**types**](types.md) -Elemente für die Dienste, die von diesem Dienst Host bereitgestellt werden. Jeder von diesem Dienst Host bereitgestellte Dienst sollte über eigene [**gehostete**](hosted.md) Element Informationen verfügen, um sicherzustellen, dass der Dienst in Antworten auf Metadatenanforderungen ordnungsgemäß veröffentlicht wird.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                         | BESCHREIBUNG                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**relationshipmetadata**](relationshipmetadata.md)<br/> | Beschreibt den Host und die gehosteten Metadaten für das Gerät.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Die hostingmetadaten werden in diesem Element in einem Formular angezeigt, das dem im Geräte Profil angegebenen Formular ähnelt. **hostmetadata** unterscheiden sich geringfügig von dem im Geräte Profil beschriebenen Format, dass die einzige unterstützte Verweis Eigenschaft die Dienst-ID ist.

Anschließend wird das [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) -Element verwendet, um eine C-Konstante zu generieren, die diese Informationen enthält.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




