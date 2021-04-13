---
description: Legt die Video-Temporale Ebenenanzahl für einen Video Encoder fest.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: CODECAPI_AVEncVideoTemporalLayerCount-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484115"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a>Codecapi \_ avencvideotemporallayercount (Eigenschaft)

Legt die Video-Temporale Ebenenanzahl für einen Video Encoder fest.

## <a name="data-type"></a>Datentyp

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideotemporallayercount**

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.

Codecapi \_ avencvideotemporallayercount, [codecapi \_ avencvideousage](codecapi-avencvideousage.md)und [codecapi \_ avenccommonratecontrolmode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sind statische Codierungs Eigenschaften. Nachdem Sie festgelegt wurden, werden diese nur wirksam, nachdem ein Set Media Type auf der Kamera-s-Ausgabe-PIN aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

