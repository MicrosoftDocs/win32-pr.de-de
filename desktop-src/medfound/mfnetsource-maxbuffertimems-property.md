---
description: Maximale Datenmenge in Millisekunden, die von der Netzwerkquelle gepuffert wird.
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: MFNETSOURCE_MAXBUFFERTIMEMS -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99d0bf07da8b931ee5487715a4b4430e5ed4384142fc69678a075275d9c7757b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243432"
---
# <a name="mfnetsource_maxbuffertimems-property"></a>MFNETSOURCE \_ MAXBUFFERTIMEMS (Eigenschaft)

Maximale Datenmenge in Millisekunden, die von der Netzwerkquelle gepuffert wird.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**DWORD** (als **LONG gespeichert)**

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ MAXBUFFERTIMEMS** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Der Standardwert dieser Eigenschaft beträgt 40.000 Millisekunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerkquellenfeatures](network-source-features.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




