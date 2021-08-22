---
description: Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an. Diese Eigenschaft ist in allen Geschwindigkeitskontrollmodi gültig.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: AVEncCommonQualityVsSpeed-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9def8fc53a6cf88384a42870ef695294a0117ab3bfdd26ba69c95bd2b02a63b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540880"
---
# <a name="avenccommonqualityvsspeed-property"></a>AVEncCommonQualityVsSpeed (Eigenschaft)

Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an. Diese Eigenschaft ist in allen Geschwindigkeitskontrollmodi gültig.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonQualityVsSpeed**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft hat den folgenden Bereich.



| Wert | Beschreibung                      |
|-------|----------------------------------|
| 0     | Niedrigere Qualität, schnellere Codierung.  |
| 100   | Höhere Qualität, langsamere Codierung. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




