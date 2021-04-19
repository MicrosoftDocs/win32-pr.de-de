---
description: Ein-Wert, der die Einheiten für einen tiefen Wert in einem Videoframe definiert.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: MF_MT_DEPTH_VALUE_UNIT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356602"
---
# <a name="mf_mt_depth_value_unit-attribute"></a>Einheiten Attribut des MF- \_ MT- \_ tiefen \_ Werts \_

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ein-Wert, der die Einheiten für einen tiefen Wert in einem Videoframe definiert.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Der Einheits Wert ist ein UINT64-Wert in Nanometer im Bereich von 1E-9-Meter. Wenn dieser Wert nicht vorhanden ist, ist der Standardwert der Einheit 1E-3, was bedeutet, dass jede Pixelebene in einem physischen Raum in 1 Millimeter gemessen wird.

Tiefen Kameras können die Tiefe aller Pixel nicht verstehen. Wenn die Zuverlässigkeit eines Pixels aufgrund von Material, Okklusion, außerhalb des gültigen Bereichs usw. gering ist, kann der tiefen Wert dieses Pixels ungültig sein.

Wenn ein tiefen Pixel Wert 0 ist, ist das Pixel ungültig.

Bei einigen tiefen Kameras werden Bitmasken Metadaten für jedes Pixel zusätzlich zum tiefen Wert anfügen, um den Grund für die Ungültigkeit der Pixel Tiefe aufgrund von Material, Okklusion oder außerhalb des gültigen Bereichs usw. darzustellen. Es wird empfohlen, solche Metadaten nicht als Bits im tiefen Wert anzufügen, da dies in der Regel zu Schwierigkeiten führt, wenn Sie solche Werte in Pixel-Shader verwenden. Stattdessen. Es wird empfohlen, dass Sie einen separaten 8-Bit-Image Puffer mit derselben Auflösung verwenden und ihn als Attribut von [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)anfügen. Diese Metadaten sind für jeden Hersteller der Kamera unterschiedlich und werden nicht von der Plattform standardisiert. Wir empfehlen die Verwendung von vollständigen 16 Bits für den Tiefen Wert zur einfacheren Verarbeitung von downstreamvorgängen und die Verwendung eines Fixed-Werts wie 0 für die Invalidierung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




