---
description: Gibt die Größe der Videozugriffseinheiten in Bytes an. Diese Eigenschaft gilt nur für vbr-Steuerungsmodi (Variable Bit Rate).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: AVEncVideoCodedVideoAccessUnitSize-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce45dbd232226aa5e0013cbead8e4ff2d8d82b5362d1d6a43cf45c2d030407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663165"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a>AVEncVideoCodedVideoAccessUnitSize-Eigenschaft

Gibt die Größe der Videozugriffseinheiten in Bytes an. Diese Eigenschaft gilt nur für vbr-Steuerungsmodi (Variable Bit Rate).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird als Wertebereich zurückgegeben. Rufen Sie [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)auf, um den unterstützten Bereich abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




