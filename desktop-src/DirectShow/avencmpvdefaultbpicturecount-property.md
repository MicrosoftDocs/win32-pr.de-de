---
description: Gibt die Standard Anzahl von aufeinander folgenden B-Frames zwischen I-und P-Frames an.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Avencmpvdefaultbpicturecount-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041269"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>Avencmpvdefaultbpicturecount (Eigenschaft)

Gibt die Standard Anzahl von aufeinander folgenden B-Frames zwischen I-und P-Frames an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencmpvdefaultbpicturecount**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Bemerkungen

Vor Windows 8 gilt diese Eigenschaft für MPEG-Video Encoder. Ab Windows 8 wird diese Eigenschaft von MPEG-, WMV-und H. 264-Video Encodern verwendet.

Wenn der Encoder diese Eigenschaft unterstützt, kann er zum Steuern der GOP-Struktur (Group of Pictures) verwendet werden.

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

 

 




