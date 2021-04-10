---
description: Gibt die maximale Anzahl von Bildern eines GOP-Headers (Group of Pictures) zum nächsten GOP-Header an.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Avencmpvgopsize-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041266"
---
# <a name="avencmpvgopsize-property"></a>Avencmpvgopsize (Eigenschaft)

Gibt die maximale Anzahl von Bildern eines GOP-Headers (Group of Pictures) zum nächsten GOP-Header an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencmpvgopsize**

## <a name="property-value"></a>Eigenschaftswert

Encoder können diese Eigenschaft als enumerationsset oder als linearen Bereich implementieren.

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft fest, bevor Sie eine Aufzeichnung starten.

**Gilt für Windows 8:** Die codierte GOP-Größe muss mit dieser Eigenschaft kleiner oder gleich der angegebenen Zahl sein, um das gleiche B-Frame-Muster im gesamten GOP oder aufgrund von Szenen Änderungen durch [codecapi \_ avencmpvdefaultbpicturecount](avencmpvdefaultbpicturecount-property.md) festzulegen. Wenn z. B. die Anzahl der B-Frames in einem GOP als 2 angegeben wird und die GOP-Größe 11 beträgt, erzeugt der Encoder eine GOP-Größe von 10 Frames oder weniger. Wenn Szenen Änderungen in der Mitte eines GOP stattfinden, fügt der Encoder möglicherweise auch einen Keyframe ein und erzeugt kleinere GOP.

GOP size 0 ist Codierungs abhängig, und Encoder können basierend auf Ihrer Implementierung/Qualität/Leistung verschiedene GOP-Größen auswählen. Encoder sollten die GOP-Größe berücksichtigen und in diesem Fall B-Frames kürzen.

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

 

 




