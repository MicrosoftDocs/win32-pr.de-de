---
description: Gibt den PnP-X-Hardwarebezeichner des Diensts an.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: PnPXHardwareId-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d032974486d4bd43f0a699eba6b8f6b75598c49858eeedb09bae5d3e79b11e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311515"
---
# <a name="pnpxhardwareid-element"></a>PnPXHardwareId-Element

Gibt den PnP-X-Hardwarebezeichner des Diensts an. PnP gleicht dieses Element mit den Hardwarebeschreibungen ab, die im \[ Abschnitt PnpxDevice \] der INF-Datei des Geräts bereitgestellt werden. Basierend auf diesen Informationen wählt der PnP-Dienst den am besten geeigneten Gerätetreiber aus und lädt diesen.

## <a name="usage"></a>Verbrauch

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                             | Beschreibung                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [**Gehostet**](hosted.md)<br/> | Definiert Elemente für die vom Diensthost definierten Dienste. <br/> <br/> |



## <a name="remarks"></a>Hinweise

Um mehr als eine Hardware-ID anzugeben, trennen Sie die Bezeichner durch ein Leerzeichen, z.B. "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




