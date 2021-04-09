---
description: Legt den Sequenz Parametersatz-Bezeichner (SPS) in der SPS-Einheit für die Netzwerk Abstraktionsschicht (NAL) des H. 264-Bit-Streams fest.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: CODECAPI_AVEncH264SPSID-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127981"
---
# <a name="codecapi_avench264spsid-property"></a>Codecapi \_ AVEncH264SPSID Eigenschaft

Legt den Sequenz Parametersatz-Bezeichner (SPS) in der SPS-Einheit für die Netzwerk Abstraktionsschicht (NAL) des H. 264-Bit-Streams fest.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ AVEncH264SPSID**

## <a name="property-value"></a>Eigenschaftswert

Gibt den Wert der **Seq- \_ Parameter \_ Satz- \_ ID** in der SPS-nal-Einheit an. Das **Seq- \_ Parameter \_ Satz- \_ ID** -Syntax Element identifiziert den Satz von Sequenz Parametern. Der resultierende Bitstream kann mit anderen Bitstreams verkettet werden, um einen längeren Bitstream zu schaffen, der mehrere Sequenz Parametersätze mit unterschiedlichen SPS-bezeichtern enthält.

Der gültige Bereich ist 0 31, wie in der H. 264/AVC-Spezifikation angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**Icodecapi**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

