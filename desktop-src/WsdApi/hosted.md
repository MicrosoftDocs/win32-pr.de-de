---
description: Definiert die Elemente ServiceID, Types, PnPXHardwareId und PnPXCompatibleId für die vom Diensthost definierten Dienste.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: Gehostetes Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afc3ea8dae3e705800cb4a1d2733bc86bcd491a25f2888ca258a47d6e765b796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738420"
---
# <a name="hosted-element"></a>Gehostetes Element

Definiert die Elemente [**ServiceID,**](serviceid.md) [**Types,**](types.md)[**PnPXHardwareId**](pnpxhardwareid.md)und [**PnPXCompatibleId**](pnpxcompatibleid.md) für die vom Diensthost definierten Dienste.

## <a name="usage"></a>Verbrauch

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                 | Beschreibung                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [**PnPXCompatibleId**](pnpxcompatibleid.md)<br/> | Gibt den PnP-X-kompatiblen Bezeichner des Diensts an.<br/> <br/> |
| [**PnPXHardwareId**](pnpxhardwareid.md)<br/>     | Gibt den PnP-X-Hardwarebezeichner des Diensts an.<br/> <br/>   |
| [**ServiceID**](serviceid.md)<br/>               | Definiert einen Dienstbezeichner für den Diensthost.<br/> <br/>        |
| [**Typen**](types.md)<br/>                       | Definiert eine Liste der qualifizierten XSD-Namen.<br/> <br/>                    |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                         | Beschreibung                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Die Hostingmetadaten für das zu implementierende Gerät.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Jeder von einem Diensthost bereitgestellte Dienst sollte über eigene **Gehostete** Elementinformationen verfügen, um sicherzustellen, dass der Dienst ordnungsgemäß als Antwort auf Metadatenanforderungen veröffentlicht wird.

Die [**Elemente PnPXHardwareId**](pnpxhardwareid.md) und [**PnPXCompatibleId**](pnpxcompatibleid.md) sind optional, müssen jedoch zusammen verwendet werden. Wenn eine vorhanden ist, muss auch die andere vorhanden sein.

Wenn ein [**PnPXDeviceCategory-Element**](pnpxdevicecategory.md) vorhanden ist, muss mindestens ein **gehostetes** Element sowohl [**PnPXHardwareId-**](pnpxhardwareid.md) als auch [**PnPXCompatibleId-Elemente**](pnpxcompatibleid.md) enthalten. Wenn **PnPXHardwareId-** und **PnPXCompatibleId-Elemente** in einem **gehosteten** Element vorhanden sind, muss mindestens ein **PnPXDeviceCategory-Element** innerhalb des [**thisModelMetadata-Elements**](thismodelmetadata.md) vorhanden sein.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




