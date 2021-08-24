---
description: Gibt an, wie oft die Netzwerkquelle versucht, erneut eine Verbindung mit dem Server herzustellen und das Streaming fortzusetzen, wenn die Verbindung unterbrochen wird.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: MFNETSOURCE_AUTORECONNECTLIMIT-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f526e9ff0274438b696996c1143620ec367fa7b086a479a066d0ba9c283f95a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604540"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a>MFNETSOURCE \_ AUTORECONNECTLIMIT-Eigenschaft

Gibt an, wie oft die Netzwerkquelle versucht, erneut eine Verbindung mit dem Server herzustellen und das Streaming fortzusetzen, wenn die Verbindung unterbrochen wird.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**DWORD** (gespeichert als **LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ AUTORECONNECTLIMIT** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie ein **IPropertyStore-Objekt** an den Quell resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerkquellfeatures](network-source-features.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




