---
description: Gibt an, ob der Encoder offene Gruppen von Bildern (GOPs) oder geschlossene GOPs erzeugt. Diese Eigenschaft gilt für MPEG-Videoencoder.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: AVEncMPVGOPOpen-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6be085bde5588fecd5a2274d442f38d4198702475f3ed13c7bb3a5569687375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540900"
---
# <a name="avencmpvgopopen-property"></a>AVEncMPVGOPOpen (Eigenschaft)

Gibt an, ob der Encoder offene Gruppen von Bildern (GOPs) oder geschlossene GOPs erzeugt. Diese Eigenschaft gilt für MPEG-Videoencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMPVGOPOpen**

## <a name="property-value"></a>Eigenschaftswert



| Wert          | Beschreibung |
|----------------|-------------|
| VARIANT \_ FALSE | Geschlossene GOPs |
| VARIANT \_ TRUE  | Öffnen von GOPs   |



 

## <a name="remarks"></a>Hinweise

Ein geöffneter GOP enthält Deltaframes, die auf Frames aus dem vorherigen GOP verweisen. Ein geschlossener GOP enthält keine Deltaframes, die auf den vorherigen GOP verweisen.

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

 

 




