---
description: Gibt den PnP-X-Hardwarebezeichner des Diensts an.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: PnPXHardwareId-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996527"
---
# <a name="pnpxhardwareid-element"></a>PnPXHardwareId-Element

Gibt den PnP-X-Hardwarebezeichner des Diensts an. PnP gleicht dieses Element mit den Hardwarebeschreibungen ab, die im \[ Abschnitt PnpxDevice \] der INF-Datei des Geräts angegeben sind. Basierend auf diesen Informationen wählt der PnP-Dienst den am besten geeigneten Gerätetreiber aus und lädt diesen.

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
| [**Gehostet**](hosted.md)<br/> | Definiert Elemente für die vom Diensthost definierten Dienste. <br/> <br/> |



## <a name="remarks"></a>Hinweise

Um mehr als eine Hardware-ID anzugeben, trennen Sie die Bezeichner durch ein Leerzeichen, z.B. "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




