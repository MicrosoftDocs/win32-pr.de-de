---
description: Gibt an, ob der Decoder innerhalb von Frames mit fehlenden Verweis Rahmen löscht.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Avdecvideodroppicwithmissingref-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213884"
---
# <a name="avdecvideodroppicwithmissingref-property"></a>Avdecvideodroppicwithmissingref (Eigenschaft)

Gibt an, ob der Decoder innerhalb von Frames mit fehlenden Verweis Rahmen löscht.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**Variant \_ bool** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecvideodroppicwithmissingref**

## <a name="remarks"></a>Bemerkungen

Wenn der Bitstrom beschädigt ist, weist ein Frame möglicherweise fehlende Verweis Rahmen auf. Wenn der Wert dieser Eigenschaft **Variant \_ true** ist, löscht der Decoder den Frame. Wenn der Wert **Variant \_ false** ist, versucht der Decoder, den Frame zu decodieren, wobei ein oder mehrere nahe gelegene Frames als Bezugsrahmen verwendet werden. Der sich ergebende decodierte Frame verfügt über blockierende Artefakte.

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

 

 




