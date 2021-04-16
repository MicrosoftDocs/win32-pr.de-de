---
description: Ein-Wert, der das Messsystem für einen tiefen Wert in einem Videoframe definiert.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: MF_MT_DEPTH_MEASUREMENT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567857"
---
# <a name="mf_mt_depth_measurement-attribute"></a>MF \_ - \_ Attribut "Tiefe \_ Messung"

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ein-Wert, der das Messsystem für einen tiefen Wert in einem Videoframe definiert.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieser Wert ist ein Member der [**\_ mfdepthmeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement) -Enumeration.

Wenn dieses Attribut nicht vorhanden ist, wird davon ausgegangen, dass es sich um **distanceyfocalplane** handelt. Die Entfernung zur Fokusebene ist in der Regel einfacher in einem 3D-euklidischen Koordinatensystem zu verarbeiten.

![Abbildung von distancedefocalplane](images/distance-to-focal-plane.png)

Der Abstand zum Fokus Center-Format ist in der Regel Rohdaten des Sensors, wie z. b. Zeit von Flug Kameras.

![Abbildung von distancegeopticalcenter](images/distance-to-optical-center.png)

Tiefen Kameras können die Tiefe aller Pixel nicht verstehen. Wenn die Zuverlässigkeit eines Pixels aufgrund von Material, Okklusion, außerhalb des gültigen Bereichs usw. gering ist, kann der tiefen Wert dieses Pixels ungültig sein.

Wenn ein tiefen Pixel Wert 0 ist, ist das Pixel ungültig.

Bei einigen tiefen Kameras werden Bitmasken Metadaten für jedes Pixel zusätzlich zum tiefen Wert anfügen, um den Grund für die Ungültigkeit der Pixel Tiefe aufgrund von Material, Okklusion oder außerhalb des gültigen Bereichs usw. darzustellen. Es wird empfohlen, solche Metadaten nicht als Bits im tiefen Wert anzufügen, da dies in der Regel zu Schwierigkeiten führt, wenn Sie solche Werte in Pixel-Shader verwenden. Stattdessen. Es wird empfohlen, dass Sie einen separaten 8-Bit-Image Puffer mit derselben Auflösung verwenden und ihn als Attribut von [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)anfügen. Diese Metadaten sind für jeden Hersteller der Kamera unterschiedlich und werden nicht von der Plattform standardisiert. Wir empfehlen die Verwendung von vollständigen 16 Bits für den Tiefen Wert zur einfacheren Verarbeitung von downstreamvorgängen und die Verwendung eines Fixed-Werts wie 0 für die Invalidierung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




