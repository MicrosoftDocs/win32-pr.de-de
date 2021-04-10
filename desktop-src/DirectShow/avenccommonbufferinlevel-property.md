---
description: Gibt die anfängliche Ebene des Codierungs Puffers in Bits an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Avenccommonbufferinlevel-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125252"
---
# <a name="avenccommonbufferinlevel-property"></a>Avenccommonbufferinlevel (Eigenschaft)

Gibt die anfängliche Ebene des Codierungs Puffers in Bits an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonbufferinlevel**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Bemerkungen

Bei MPEG-Videos definiert diese Eigenschaft die anfängliche VBV-Auslastung (Video Buffer Verifier). Die Verkettung von Streams während der Codierung wird unterstützt.

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

 

 




