---
description: Gibt an, ob der Encoder offene Gruppen von Bildern (GOPs) oder geschlossene GOPs erzeugt. Diese Eigenschaft gilt für MPEG-Video Encoder.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Avencmpvgopopen-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746928"
---
# <a name="avencmpvgopopen-property"></a>Avencmpvgopopen (Eigenschaft)

Gibt an, ob der Encoder offene Gruppen von Bildern (GOPs) oder geschlossene GOPs erzeugt. Diese Eigenschaft gilt für MPEG-Video Encoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**Variant \_ bool** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencmpvgopopen**

## <a name="property-value"></a>Eigenschaftswert



| Wert          | BESCHREIBUNG |
|----------------|-------------|
| Variant \_ false | Geschlossene GOPs |
| Variant \_ true  | Open-GOPs   |



 

## <a name="remarks"></a>Bemerkungen

Ein geöffnetes GOP enthält Delta Frames, die auf Frames aus dem vorherigen GOP verweisen. Ein geschlossenes GOP enthält keine Delta Frames, die auf das vorherige GOP verweisen.

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

 

 




