---
description: Gibt die endgültige Ebene des Codierungs Puffers am Ende des Codierungs Prozesses in Bits an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Avenccommonbufferoutlevel-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346202"
---
# <a name="avenccommonbufferoutlevel-property"></a>Avenccommonbufferoutlevel (Eigenschaft)

Gibt die endgültige Ebene des Codierungs Puffers am Ende des Codierungs Prozesses in Bits an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonbufferoutlevel**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Bemerkungen

Die-Eigenschaft ist nur verfügbar, wenn die Codierungs Dauer im Voraus mithilfe der Eigenschaft " [**avencvideonooffieldstoencode**](avencvideonooffieldstoencode-property.md) " oder der Eigenschaft " [**avencaudiointervaltoencode**](avencaudiointervaltoencode-property.md) " definiert wird.

Bei MPEG-Videos definiert diese Eigenschaft am Ende des Codierungs Prozesses den VBV-Füllungs Bereich (Video Buffer Verifier). Die Verkettung von Streams während der Codierung wird unterstützt.

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

 

 




