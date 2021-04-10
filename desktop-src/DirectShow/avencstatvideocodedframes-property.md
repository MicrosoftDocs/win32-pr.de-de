---
description: Gibt die Anzahl der codierten Video Frames zurück.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Avencstatus videocodedframes-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124807"
---
# <a name="avencstatvideocodedframes-property"></a>Avencstatus videocodedframes (Eigenschaft)

Gibt die Anzahl der codierten Video Frames zurück.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencstatus videocodedframes**

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nach Abschluss der Codierung verfügbar.

Der Wert dieser Eigenschaft entspricht der Eigenschaft " [**avencstatus videototalframes**](avencstatvideototalframes-property.md) " abzüglich der Anzahl der gelöschten Frames. Der Encoder kann Frames ablegen, um innerhalb der angegebenen Bitrate Einschränkungen zu bleiben. Möglicherweise werden auch Frames am Ende des Streams abgelegt (siehe Eigenschaft " [**avenccommonstreamendhandling**](avenccommonstreamendhandling-property.md) ").

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

 

 




