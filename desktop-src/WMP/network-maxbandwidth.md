---
title: Network.maxBandwidth
description: Die maxBandwidth-Eigenschaft gibt die maximal zulässige Bandbreite an oder ruft sie ab.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Network.maxBandwidth Windows Media Player
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c06c84762cd0d68af8af1cc9405036c5aecce317a61dbf292d3213bed351e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574146"
---
# <a name="networkmaxbandwidth"></a>Network.maxBandwidth

Die **maxBandwidth-Eigenschaft** gibt die maximal zulässige Bandbreite an oder ruft sie ab.

## <a name="syntax"></a>Syntax

*Player*. *network*. **maxBandwidth**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/Schreibnummer (**long**). 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft hat keinen Standardwert. Der Wert kann angegeben werden, während Windows Media Player wiedergegeben wird. Die Änderung wird jedoch erst wirksam, wenn das aktuelle Medienelement durch Öffnen eines anderen Oder durch Aufrufen von *Player* freigegeben wird. **schließen Sie**. Windows Media Player versucht, die größtmögliche Bandbreite zu erreichen. Nur im Fall des festzulegenden Werts tritt eine Bandbreitenreduzierung auf.

Diese Einstellung ist nützlich, um die verwendete Bandbreite zu reduzieren, insbesondere bei einem MBR-Datenstrom (Multiple Bit Rate). Ein MBR-Stream enthält mehrere Datenströme mit unterschiedlichen Bitraten. In einigen Fällen kann es wünschenswert sein, einen Stream mit einer niedrigeren Bitrate zu verwenden, als der Client erfordert. In diesem Fall wählt das Festlegen der **maxBandwidth-Eigenschaft** einen Stream mit niedrigerer Bitrate aus.

Ein MBR-Datenstrom kann beispielsweise Streams enthalten, die mit 20 Kilobits pro Sekunde (KBit/s), 37 KBit/s und 200 KBit/s codiert sind. Wenn Sie die **maxBandwidth-Eigenschaft** auf 50.000 (50 KBit/s) festlegen, wird der Stream mit 37 KBit/s anstelle des Streams mit 200 KBit/s ausgewählt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> <dt>

[**Player.close**](player-close.md)
</dt> </dl>

 

 





