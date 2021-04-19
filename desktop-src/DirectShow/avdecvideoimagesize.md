---
description: Ruft die Größe des decodierten Bilds in Pixel ab.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Avdecvideoimagesize-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343146"
---
# <a name="avdecvideoimagesize-property"></a>Avdecvideoimagesize (Eigenschaft)

Ruft die Größe des decodierten Bilds in Pixel ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecvideoimagesize**

## <a name="property-value"></a>Eigenschaftswert

Die hohen 16 Bits enthalten die Breite, und die unteren 16 Bits enthalten die Höhe.

## <a name="remarks"></a>Bemerkungen

Die Anzahl der Kanäle umfasst den LFE-Kanal (Low Frequency Effect), falls vorhanden.

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

 

 




