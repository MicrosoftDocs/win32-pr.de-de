---
description: Ein -Wert, der die Einheiten für einen Tiefenwert in einem Videoframe definiert.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: MF_MT_DEPTH_VALUE_UNIT -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca57fa5cf72be266ac58ee504b1d4b7c4f2506646f33295e468d2ed0781ab8d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060640"
---
# <a name="mf_mt_depth_value_unit-attribute"></a>MF \_ MT DEPTH VALUE \_ \_ \_ UNIT-Attribut

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ein -Wert, der die Einheiten für einen Tiefenwert in einem Videoframe definiert.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Der Einheitenwert ist ein UINT64-Wert in "1e" und "9 Meter". Wenn dieser Wert nicht vorhanden ist, ist der Standardwert der Einheit 1e-3, was angibt, dass jede Pixelebene im physischen Raum in 1 Millimeter gemessen wird.

Tiefenkameras können die Tiefe aller Pixel nicht ermitteln. Wenn die Konfidenz eines Pixels aufgrund von Material, Okklusion oder nicht dem zulässigen Bereich usw. niedrig ist, kann der Tiefenwert dieses Pixels ungültig sein.

Wenn ein Tiefenpixelwert 0 ist, ist das Pixel ungültig.

Einige Tiefenkameras fügen Bitmaskenmetadaten für jedes Pixel zusätzlich zum Tiefenwert an, um den Grund dafür zu darstellen, warum die Tiefe des Pixels ungültig ist, aufgrund von Material, Okklusion oder Nicht-Bereich usw. Es wird empfohlen, das Anfügen solcher Metadaten als Tiefenwertbits zu vermeiden, da dies in der Regel zu Schwierigkeiten bei der Verwendung solcher Werte im Pixel-Shader führt. Statt. Es wird empfohlen, einen separaten 8-Bit-Bildpuffer mit der gleichen Auflösung zu verwenden und ihn als Attribut des [**8-Bit-Bildpuffers zu anfügen.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) Diese Metadaten variieren für jeden Kameraanbieter und werden nicht von der Plattform standardisiert. Es wird empfohlen, vollständige 16 Bits für den Tiefenwert zu verwenden, um die Verarbeitung nachgelagert zu vereinfachen, und einen festen Wert wie 0 für die Invalidierung zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




