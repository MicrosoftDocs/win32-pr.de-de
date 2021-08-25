---
description: Gibt den Typ des Filters zum Deaktivieren der Hervorhebung an, der beim Decodieren verwendet werden soll. Diese Eigenschaft gilt für MPEG-Audioencoder.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: AVEncMPAEmphasisType-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3da73e2708acde7a5b388d229a3a82c50a2dff04c4f2873551a992fe738189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824230"
---
# <a name="avencmpaemphasistype-property"></a>AVEncMPAEmphasisType-Eigenschaft

Gibt den Typ des Filters zum Deaktivieren der Hervorhebung an, der beim Decodieren verwendet werden soll. Diese Eigenschaft gilt für MPEG-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMPAEmphasisType**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVEncMPAEmphasisType-Enumeration.**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)

## <a name="remarks"></a>Hinweise

Diese Eigenschaft legt die Hervorhebungsbits im Frameheader fest.

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

 

