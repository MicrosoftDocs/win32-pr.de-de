---
description: Gibt den Wert des Drop Frame-Flags im Group of Pictures (GOP)-Header an.
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Avencvideoheaderdropframe-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860477"
---
# <a name="avencvideoheaderdropframe-property"></a>Avencvideoheaderdropframe (Eigenschaft)

Gibt den Wert des Drop Frame-Flags im Group of Pictures (GOP)-Header an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideoheaderdropframe**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft kann 0 oder 1 sein.

## <a name="remarks"></a>Bemerkungen

Der Ablage Frame Modus wird in einem NTSC-Video verwendet, um die Diskrepanz zwischen dem Video, das 29,97 Frames pro Sekunde ist, und der Zeit Code Anzeige (30 Frames pro Sekunde) zu korrigieren. Im Ablage Frame Modus werden die Frame Nummern 00 und 01 am Anfang jeder Minute übersprungen. ausgenommen sind Minuten, bei denen es sich um ein Vielfaches von zehn (00, 10, 20 usw.) handelt. Nur die Frame Nummern im Zeit Code werden gelöscht. Es werden keine eigentlichen Frames gelöscht.

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

 

 




