---
description: Gibt an, wie der decodierte Videostream mit Zeilen Sprung verknüpft ist.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Avdecvideoinputscantype-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860383"
---
# <a name="avdecvideoinputscantype-property"></a>Avdecvideoinputscantype (Eigenschaft)

Gibt an, wie der decodierte Videostream mit Zeilen Sprung verknüpft ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecvideoinputscantype**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eavdecvideoinputscantype**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) -Enumeration.

## <a name="remarks"></a>Bemerkungen

Die oberen 16 Bits des Werts enthalten die Breite, und die unteren 16 Bits enthalten die Höhe.

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

 

