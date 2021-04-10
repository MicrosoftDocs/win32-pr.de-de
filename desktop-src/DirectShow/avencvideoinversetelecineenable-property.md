---
description: Gibt an, ob der Encoder Inverse Telecine ausführt.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Avencvideoinverabtelecineenable-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124994"
---
# <a name="avencvideoinversetelecineenable-property"></a>Avencvideoinverabtelecineenable (Eigenschaft)

Gibt an, ob der Encoder Inverse Telecine ausführt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**Variant \_ bool** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideoinverabtelecineenable**

## <a name="remarks"></a>Bemerkungen

Wenn der Wert **Variant \_ true** ist, führt der Encoder Inverse Telecine aus. Wenn Inverse Telecine nicht erforderlich ist, legen Sie diese Eigenschaft auf **Variant \_ false** fest. Wenn Sie Inverse Telecine außerhalb des Encoders ausführen möchten, legen Sie diese Eigenschaft auf **Variant \_ false** fest, und legen Sie die Eigenschaft [**avencvideooutputscantype**](avencvideooutputscantype-property.md) auf eavencvideooutputscan \_ sameasinput fest.

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

 

 




