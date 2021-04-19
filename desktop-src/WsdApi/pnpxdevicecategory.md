---
description: Gibt die PnP-X-Kategorie an, zu der das Gerät gehört. Es können mehr als eine Kategorie angegeben werden.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Pnpxdebug-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363495"
---
# <a name="pnpxdevicecategory-element"></a>Pnpxdebug-Element

Gibt die PnP-X-Kategorie an, zu der das Gerät gehört. Es können mehr als eine Kategorie angegeben werden.

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
| [**thismodelmetadata**](thismodelmetadata.md)<br/> | Definiert die Hersteller-und Modell Metadaten für das zu implementierende Gerät.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Geräte können auch eine Geräte Unterkategorie für eine beschreibende Gerätekategorie angeben. Beispielsweise identifiziert "Phones. WindowsMobile Kameras. digitalstillcamera mediadevices. Musicplayer" ein Gerät, das ein Microsoft Windows Mobile-Gerät mit einer Kamera und einem Musikplayer ist. Die primäre Gerätekategorie für dieses Gerät wäre "Smartphones".

Wenn Sie mehr als eine Gerätekategorie angeben möchten, trennen Sie die Kategorien durch ein Leerzeichen. Beispielsweise identifiziert "Drucker Speicher" ein Gerät mit der primär Kategorie "Drucker" und der sekundären Kategorie "Speicher".

Wenn ein **pnpxenvicecategory** -Element vorhanden ist, sollte mindestens ein [**gehosteter**](hosted.md) -Element sowohl [**pnpxhardwareid**](pnpxhardwareid.md) -als auch [**pnpxcompatibleid-**](pnpxcompatibleid.md) Elemente enthalten. Ebenso muss, wenn **pnpxhardwareid** -und **pnpxcompatibleid-** Elemente in einem **gehosteten** Element vorhanden sind, mindestens ein **pnpxenvicecategory** -Element im [**thismodelmetadata**](thismodelmetadata.md) -Element vorhanden sein.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




