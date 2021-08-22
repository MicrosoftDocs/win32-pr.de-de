---
description: Legt den SPS-Bezeichner (Sequence Parameter Set) in der SPS-NAL-Einheit (Network Abstraction Layer) des H.264-Bitstreams fest.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: CODECAPI_AVEncH264SPSID-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da06e431a3747e676e3934ac9a261e1d0e1ec37e18bacf01f8a3e623c4257488
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664660"
---
# <a name="codecapi_avench264spsid-property"></a>CODECAPI \_ AVEncH264SPSID-Eigenschaft

Legt den SPS-Bezeichner (Sequence Parameter Set) in der SPS-NAL-Einheit (Network Abstraction Layer) des H.264-Bitstreams fest.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncH264SPSID**

## <a name="property-value"></a>Eigenschaftswert

Gibt den Wert der **seq-Parametersatz-ID \_ \_ \_** in der SPS-NAL-Einheit an. Das **Syntaxelement seq \_ parameter set \_ \_ id** identifiziert den Sequenzparametersatz. Der resultierende Bitstream kann mit anderen Bitstreams verkettet werden, um einen längeren Bitstream zu erzeugen, der mehrere Sequenzparametersätze mit unterschiedlichen SPS-Bezeichnern enthält.

Der gültige Bereich ist 0 31, wie in der H.264/AVC-Spezifikation angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

