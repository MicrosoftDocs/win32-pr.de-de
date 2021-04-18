---
description: Gibt das Zeitintervall an, für das die durchschnittliche Bitrate gilt. Diese Eigenschaft wird in Verbindung mit der Eigenschaft "avenccommonmeanbitrate" verwendet.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Avenccommonmeanbitrateingeterval-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482523"
---
# <a name="avenccommonmeanbitrateinterval-property"></a>Avenccommonmeanbitrateingeterval (Eigenschaft)

Gibt das Zeitintervall an, für das die durchschnittliche Bitrate gilt. Diese Eigenschaft wird in Verbindung mit der Eigenschaft " [**avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md) " verwendet.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonmeanbitrateingeterval**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Bemerkungen

Bei der bidirektionalen VBR-Codierung (Two-Pass Variable Bitrate) gibt der Wert 0 (null) an, dass das Zeitintervall die gesamte Dauer des Inhalts ist. Bei einer CBR-Codierung (Single-Pass Constant Bit Rate) gibt der Wert 0 (null) an, dass der Encoder das Intervall (in der Regel 0,5 Sekunden) auswählt.

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

 

 




