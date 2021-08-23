---
description: Ein -Wert, der das Messsystem für einen Tiefenwert in einem Videoframe definiert.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: MF_MT_DEPTH_MEASUREMENT -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a292e5a96cec7490917ef0bb897a9a7a67dd303d29692bf6db5ff58e1d4388c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605799"
---
# <a name="mf_mt_depth_measurement-attribute"></a>MF \_ MT \_ DEPTH \_ MEASUREMENT-Attribut

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ein -Wert, der das Messsystem für einen Tiefenwert in einem Videoframe definiert.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieser Wert ist ein Member der [**\_ MFDepthMeasurement-Enumeration.**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)

Wenn dieses Attribut nicht vorhanden ist, wird von **DistanceToFocalPlane ausgegangen.** Der Abstand zur Fokusebene ist in einem euklidischen 3D-Koordinatensystem in der Regel einfacher zu nutzen.

![Abbildung von distancetofocalplane](images/distance-to-focal-plane.png)

Der Abstand zum Fokuscenterformat ist in der Regel Rohdaten des Sensors, z. B. die Zeit von Flugkameras.

![Abbildung von distancetoopticalcenter](images/distance-to-optical-center.png)

Tiefenkameras können die Tiefe aller Pixel nicht ermitteln. Wenn die Konfidenz eines Pixels aufgrund von Material, Okklusion oder nicht dem zulässigen Bereich usw. niedrig ist, kann der Tiefenwert dieses Pixels ungültig sein.

Wenn ein Tiefenpixelwert 0 ist, ist das Pixel ungültig.

Einige Tiefenkameras fügen Bitmaskenmetadaten für jedes Pixel zusätzlich zum Tiefenwert an, um den Grund dafür zu darstellen, warum die Tiefe des Pixels ungültig ist, aufgrund von Material, Okklusion oder Nicht-Bereich usw. Es wird empfohlen, das Anfügen solcher Metadaten als Tiefenwertbits zu vermeiden, da dies in der Regel zu Schwierigkeiten bei der Verwendung solcher Werte im Pixel-Shader führt. Statt. Es wird empfohlen, einen separaten 8-Bit-Bildpuffer mit der gleichen Auflösung zu verwenden und ihn als Attribut des [**8-Bit-Bildpuffers zu anfügen.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) Diese Metadaten variieren für jeden Kameraanbieter und werden nicht von der Plattform standardisiert. Es wird empfohlen, vollständige 16 Bits für den Tiefenwert zu verwenden, um die Verarbeitung nachgelagert zu vereinfachen, und einen festen Wert wie 0 für die Invalidierung zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




