---
description: Definiert die Hostingmetadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: hostMetadata-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994797"
---
# <a name="hostmetadata-element"></a>hostMetadata-Element

Definiert die Hostingmetadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.

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
| [**Host**](host.md)<br/>     | Definiert die Elemente ServiceID und [**Types**](types.md) für den Diensthost. Wenn sie nicht explizit angegeben wird, stellt WSDAPI als Reaktion auf Metadatenanforderungen keine Standarddaten bereit.<br/> <br/>                                                                                                                                          |
| [**Gehostet**](hosted.md)<br/> | Definiert die [**Elemente ServiceID**](serviceid.md) und [**Types**](types.md) für die von diesem Diensthost bereitgestellten Dienste. Jeder von diesem Diensthost bereitgestellte Dienst sollte über eigene [**Gehostete**](hosted.md) Elementinformationen verfügen, um sicherzustellen, dass der Dienst ordnungsgemäß als Antwort auf Metadatenanforderungen veröffentlicht wird.<br/> <br/> |



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
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Beschreibt die Host- und gehosteten Metadaten für das Gerät.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Die Hostingmetadaten werden in diesem Element in einer Form angezeigt, die der im Geräteprofil angegebenen ähnelt. **hostMetadata** unterscheidet sich geringfügig vom im Geräteprofil beschriebenen Format, da die einzige referenz-Eigenschaft, die sie unterstützt, die Dienst-ID ist.

Das [**relationshipMetadataDefinition-Element**](relationshipmetadatadefinition.md) wird anschließend verwendet, um eine C-Konstante zu generieren, die diese Informationen enthält.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




