---
description: Gibt die PnP-X-Kategorie an, zu der das Gerät gehört. Es können mehrere Kategorien angegeben werden.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: PnPXDeviceCategory-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08084d780c26d2f7fab902156939fd14a3e60c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996587"
---
# <a name="pnpxdevicecategory-element"></a>PnPXDeviceCategory-Element

Gibt die PnP-X-Kategorie an, zu der das Gerät gehört. Es können mehrere Kategorien angegeben werden.

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
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Definiert die Hersteller- und Modellmetadaten für das zu implementierende Gerät.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Geräte können auch eine Geräteunterkategorie für eine beschreibendere Gerätekategorie angeben. Beispielsweise identifiziert "Phones.WindowsMobile Cameras.DigitalZooCamera MediaDevices.MusicPlayer" ein Gerät, bei dem es sich um ein Microsoft Windows Mobile-Gerät mit einer Kamera und einem Musikplayer handelt. Die primäre Gerätekategorie für dieses Gerät wäre "Phones".

Um mehr als eine Gerätekategorie anzugeben, trennen Sie die Kategorien durch ein Leerzeichen. Beispielsweise identifiziert "Druckerspeicher" ein Gerät mit der primären Kategorie "Drucker" und der sekundären Kategorie "Speicher".

Wenn ein **PnPXDeviceCategory-Element** vorhanden ist, sollte mindestens ein [**gehostetes**](hosted.md) Element sowohl [**PnPXHardwareId-**](pnpxhardwareid.md) als auch [**PnPXCompatibleId-Elemente**](pnpxcompatibleid.md) enthalten. Wenn **PnPXHardwareId-** und **PnPXCompatibleId-Elemente** in einem **gehosteten** Element vorhanden sind, sollte mindestens ein **PnPXDeviceCategory-Element** innerhalb des [**thisModelMetadata-Elements**](thismodelmetadata.md) vorhanden sein.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




