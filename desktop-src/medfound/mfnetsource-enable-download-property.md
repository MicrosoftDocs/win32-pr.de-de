---
description: Gibt an, ob alle Downloadprotokolle aktiviert sind.
ms.assetid: c178693f-44ea-481e-b7f2-2ec94eea1994
title: MFNETSOURCE_ENABLE_DOWNLOAD -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7749dcdf15c099284a73cf6c55c1d753825230126e77a972e906b280a0b09a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738979"
---
# <a name="mfnetsource_enable_download-property"></a>MFNETSOURCE \_ ENABLE \_ DOWNLOAD (Eigenschaft)

Gibt an, ob alle Downloadprotokolle aktiviert sind.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Boolescher Wert (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ ENABLE \_ DOWNLOAD** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an [das -Objekt Configuring a Media Source](configuring-a-media-source.md)(Konfigurieren einer Medienquelle).

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

 

 




