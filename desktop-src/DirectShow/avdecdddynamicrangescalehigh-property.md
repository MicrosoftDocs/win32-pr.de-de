---
description: Gibt den auf hoher Ebene ausgeschnittenen Wert an, wenn der Decoder ein dynamisches Bereichs Steuerelement für einen Dolby AC-3-Audiodatenstrom ausführt.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Avdecdddynamicrangescalehigh-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482278"
---
# <a name="avdecdddynamicrangescalehigh-property"></a>Avdecdddynamicrangescalehigh (Eigenschaft)

Gibt den auf hoher Ebene ausgeschnittenen Wert an, wenn der Decoder ein dynamisches Bereichs Steuerelement für einen Dolby AC-3-Audiodatenstrom ausführt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecdddynamicrangescalehigh**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft hat den folgenden Bereich.



| Wert | BESCHREIBUNG                                                    |
|-------|----------------------------------------------------------------|
| 0     | Keine dynamische Bereichs Komprimierung. Bewahren Sie den gesamten dynamischen Bereich auf. |
| 100   | Vollständige dynamische Bereichs Komprimierung anwenden.                          |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt nur, wenn der Wert der [**avdecddoperationalmode**](avdecddoperationalmode-property.md) -Eigenschaft die Zeile eavdecddoperationalmode ist \_ .

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

 

 




