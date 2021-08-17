---
description: Gibt die maximale Anzahl von Bildern von einer Gruppe von Bildern (GOP) bis zum nächsten GOP-Header an.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: AVEncMPVGOPSize-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7c82ae5c613bb3e78069be3f39f652d840e19c5d62d095fe020f4186bf975f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119258450"
---
# <a name="avencmpvgopsize-property"></a>AVEncMPVGOPSize-Eigenschaft

Gibt die maximale Anzahl von Bildern von einer Gruppe von Bildern (GOP) bis zum nächsten GOP-Header an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMPVGOPSize**

## <a name="property-value"></a>Eigenschaftswert

Encoder können diese Eigenschaft als aufzählten Satz oder als linearen Bereich implementieren.

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft fest, bevor Sie eine Aufzeichnung starten.

**Gilt für Windows 8:** Die codierte GOP-Größe muss kleiner oder gleich der angegebenen Zahl über diese Eigenschaft sein, um das gleiche B-Framemuster beizubehalten, das von [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) während des gesamten GOP oder aufgrund von Szenenänderungen festgelegt wird. Wenn z. B. die Anzahl der B-Frames in einem GOP auf 2 und die GOP-Größe 11 festgelegt ist, muss der Encoder eine GOP-Größe von mindestens 10 Frames erzeugen. Wenn sich die Szene in der Mitte eines GOP ändert, kann der Encoder auch einen Keyframe einfügen und kleinere GOP-Dateien erzeugen.

GOP-Größe 0 ist encoderabhängig, und Encoder können je nach Implementierung/Qualität/Leistung unterschiedliche GOP-Größen auswählen. Encoder sollten die GOP-Größe berücksichtigen und in diesem Fall B-Frames abschneiden.

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

 

 




