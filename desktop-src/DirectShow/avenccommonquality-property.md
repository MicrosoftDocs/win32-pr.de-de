---
description: Gibt die Qualitätsstufe für die Codierung an.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Avenccommonquality-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482510"
---
# <a name="avenccommonquality-property"></a>Avenccommonquality (Eigenschaft)

Gibt die Qualitätsstufe für die Codierung an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonquality**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft hat den folgenden Bereich.



| Wert | BESCHREIBUNG                           |
|-------|---------------------------------------|
| 0     | Minimale Qualität, kleinere Ausgabegröße. |
| 100   | Maximale Qualität, größere Ausgabegröße.  |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft steuert die Qualitätsstufe, wenn der Encoder keine eingeschränkte Bitrate verwendet. Die Eigenschaft " [**avenccommonratecontrolmode**](avenccommonratecontrolmode-property.md) " bestimmt, ob die Bitrate eingeschränkt ist.

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

 

 




