---
description: Gibt an, ob das MsB-Multicastprotokoll (Media Stream Broadcast) in der Netzwerkquelle aktiviert ist.
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: MFNETSOURCE_ENABLE_MSB -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1054b4a94bf966457ddeccc606fbd2fd2c8a1d5b3978b830b5e3c48f0f93b5ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243817"
---
# <a name="mfnetsource_enable_msb-property"></a>MFNETSOURCE \_ ENABLE \_ MSB-Eigenschaft

Gibt an, ob das MsB-Multicastprotokoll (Media Stream Broadcast) in der Netzwerkquelle aktiviert ist.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ ENABLE \_ MSB** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Unterstützte Protokolle](supported-protocols.md)
</dt> </dl>

 

 




