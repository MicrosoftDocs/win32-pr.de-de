---
description: Definiert die Elemente serviceid, types, pnpxhardwareid und pnpxcompatibleid für die Dienste, die vom Dienst Host definiert werden.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: Hosted-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352502"
---
# <a name="hosted-element"></a>Hosted-Element

Definiert die Elemente [**serviceid**](serviceid.md), [**types**](types.md),[**pnpxhardwareid**](pnpxhardwareid.md)und [**pnpxcompatibleid**](pnpxcompatibleid.md) für die Dienste, die vom Dienst Host definiert werden.

## <a name="usage"></a>Verbrauch

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                 | BESCHREIBUNG                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [**Pnpxcompatibleid**](pnpxcompatibleid.md)<br/> | Gibt den mit PnP-X kompatiblen Bezeichner des Dienstanbieter an.<br/> <br/> |
| [**Pnpxhardwareid**](pnpxhardwareid.md)<br/>     | Gibt den PnP-X-Hardware Bezeichner des Dienstanbieter an.<br/> <br/>   |
| [**ServiceID**](serviceid.md)<br/>               | Definiert einen Dienst Bezeichner für den Dienst Host.<br/> <br/>        |
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



| Element                                         | BESCHREIBUNG                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostmetadata**](hostmetadata.md)<br/> | Die hostingmetadaten für das Gerät, das implementiert werden soll.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Jeder von einem Dienst Host bereitgestellte Dienst sollte über eigene **gehostete** Element Informationen verfügen, um sicherzustellen, dass der Dienst in Antworten auf Metadatenanforderungen ordnungsgemäß veröffentlicht wird.

Die [**pnpxhardwareid**](pnpxhardwareid.md) -und [**pnpxcompatibleid-**](pnpxcompatibleid.md) Elemente sind optional, aber wenn Sie verwendet werden, müssen Sie miteinander verwendet werden. Wenn eine solche vorhanden ist, muss auch die andere vorhanden sein.

Wenn ein [**pnpxenvicecategory**](pnpxdevicecategory.md) -Element vorhanden ist, muss mindestens ein **gehosteter** -Element sowohl [**pnpxhardwareid**](pnpxhardwareid.md) -als auch [**pnpxcompatibleid-**](pnpxcompatibleid.md) Elemente enthalten. Ebenso muss, wenn **pnpxhardwareid** -und **pnpxcompatibleid-** Elemente in einem **gehosteten** Element vorhanden sind, mindestens ein **pnpxenvicecategory** -Element im [**thismodelmetadata**](thismodelmetadata.md) -Element vorhanden sein.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




