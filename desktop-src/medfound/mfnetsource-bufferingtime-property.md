---
description: Anzahl der Daten in Sekunden, die die Netzwerkquelle beim Start puffert.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: MFNETSOURCE_BUFFERINGTIME-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6de79344913d77a30dc05dcad4e4f8dd3608e0d35009b1d8e5254e08790993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243807"
---
# <a name="mfnetsource_bufferingtime-property"></a>MFNETSOURCE \_ BUFFERINGTIME-Eigenschaft

Anzahl der Daten in Sekunden, die die Netzwerkquelle beim Start puffert.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**DWORD** (gespeichert als **LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ BUFFERINGTIME** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore-Zeiger** an den Quell resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Der Standardwert dieser Eigenschaft ist 5 Sekunden.

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

 

 




