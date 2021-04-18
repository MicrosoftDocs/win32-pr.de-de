---
description: Gibt den PnP-X-Hardware Bezeichner des Dienstanbieter an.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Pnpxhardwareid-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347910"
---
# <a name="pnpxhardwareid-element"></a>Pnpxhardwareid-Element

Gibt den PnP-X-Hardware Bezeichner des Dienstanbieter an. PNP stimmt mit diesem Element mit den Hardware Beschreibungen überein, die im \[ Abschnitt "pnpxdevice" \] der INF-Datei des Geräts bereitgestellt werden. Basierend auf diesen Informationen wählt der PnP-Dienst den am besten geeigneten Gerätetreiber aus und lädt ihn.

## <a name="usage"></a>Verbrauch

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                             | BESCHREIBUNG                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [**gehostet**](hosted.md)<br/> | Definiert die Elemente für die Dienste, die vom Dienst Host definiert werden. <br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Wenn Sie mehr als eine Hardware-ID angeben möchten, trennen Sie die Bezeichner durch ein Leerzeichen, z. b. "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




