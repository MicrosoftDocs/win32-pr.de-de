---
description: Gibt die Kategorie PnP-X an, zu der das Gerät gehört. Es können mehrere Kategorien angegeben werden.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: PnPXDeviceCategory-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42a34a3f63333a2d33266991c0e028e7d42a7244c962617974c9cc15e290d03c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897360"
---
# <a name="pnpxdevicecategory-element"></a>PnPXDeviceCategory-Element

Gibt die Kategorie PnP-X an, zu der das Gerät gehört. Es können mehrere Kategorien angegeben werden.

## <a name="usage"></a>Verbrauch

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   | BESCHREIBUNG                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Definiert die Hersteller- und Modellmetadaten für das zu implementierte Gerät.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Geräte können auch eine Geräteunterkategorie für eine aussagekräftigere Gerätekategorie angeben. Beispielsweise identifiziert "Phones.WindowsMobile Cameras.DigitalCamera MediaDevices.MusicPlayer" ein Gerät, bei dem es sich um ein Microsoft Windows Mobile-Gerät mit einer Kamera und einem Musikplayer handelt. Die primäre Gerätekategorie für dieses Gerät wäre "Phones".

Um mehr als eine Gerätekategorie anzugeben, trennen Sie die Kategorien durch einen Bereich. Beispielsweise identifiziert "Drucker Storage" ein Gerät mit der primären Kategorie "Drucker" und der sekundären Kategorie "Storage".

Wenn ein **PnPXDeviceCategory-Element** vorhanden ist, [](hosted.md) sollte mindestens ein gehostetes Element sowohl [**PnPXHardwareId-**](pnpxhardwareid.md) als auch [**PnPXCompatibleId-Elemente**](pnpxcompatibleid.md) enthalten. Wenn **PnPXHardwareId-** und **PnPXCompatibleId-Elemente** in  einem gehosteten Element vorhanden sind, sollte im [**thisModelMetadata-Element**](thismodelmetadata.md) mindestens ein **PnPXDeviceCategory-Element** vorhanden sein.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




