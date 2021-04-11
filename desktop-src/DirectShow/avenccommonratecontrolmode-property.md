---
description: Gibt den Raten Steuerungs Modus an.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Avenccommonratecontrolmode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213985"
---
# <a name="avenccommonratecontrolmode-property"></a>Avenccommonratecontrolmode (Eigenschaft)

Gibt den Raten Steuerungs Modus an.

Anwendungen können diese Eigenschaft festlegen, um den Raten Steuerungs Modus anzugeben. Encoder können diese Eigenschaft auch als Funktion zurückgeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonratecontrolmode**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eavenccommonratecontrolmode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) -Enumeration.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.

[Codecapi \_ Avencvideotemporallayercount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [codecapi \_ avencvideousage](/windows/desktop/medfound/codecapi-avencvideousage)und codecapi \_ avenccommonratecontrolmode sind statische Codierungs Eigenschaften. Nachdem Sie festgelegt wurden, werden diese nur wirksam, nachdem ein Set Media Type auf der Ausgabe-PIN der Kamera aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

