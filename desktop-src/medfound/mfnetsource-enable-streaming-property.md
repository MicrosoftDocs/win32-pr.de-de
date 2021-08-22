---
description: Gibt an, ob alle Streamingprotokolle aktiviert sind.
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: MFNETSOURCE_ENABLE_STREAMING -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fae2b127a52bbea9e8d122ec9ad219c61010068b07696b44cce49cc7546c9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463700"
---
# <a name="mfnetsource_enable_streaming-property"></a>MFNETSOURCE \_ ENABLE \_ STREAMING (Eigenschaft)

Gibt an, ob alle Streamingprotokolle aktiviert sind.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Boolescher Wert (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ ENABLE \_ STREAMING** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** auf [das -Objekt Configuring a Media Source](configuring-a-media-source.md)(Konfigurieren einer Medienquelle).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Unterstützte Protokolle](supported-protocols.md)
</dt> </dl>

 

 




