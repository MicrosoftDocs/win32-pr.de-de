---
description: Gibt die minimale Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: Avenccommonminbitrate-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c9b6e84675994d2aca7548f6c13d6558ebc020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343948"
---
# <a name="avenccommonminbitrate-property"></a>Avenccommonminbitrate (Eigenschaft)

Gibt die minimale Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonminbitrate**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Bemerkungen

Der Encoder erzwingt die minimale Bitrate durch Erhöhen der Codierungsqualität nach Bedarf.

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

 

 




