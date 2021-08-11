---
description: Dauer des beschleunigten Streamings für die Netzwerkquelle in Millisekunden.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: MFNETSOURCE_ACCELERATEDSTREAMINGDURATION-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ec37cfd7dd0aa8d60c3e192ae0f445f8a121e9e3cd3f85d46e8c18b21fc2b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243864"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a>MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION-Eigenschaft

Dauer des beschleunigten Streamings für die Netzwerkquelle in Millisekunden.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**DWORD** (gespeichert als **LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie ein **IPropertyStore-Objekt** an den Quell resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Diese Eigenschaft gilt für das Fast Start-Feature von Windows Media-Dienste, das Inhalte schnell wiedergibt, ohne auf eine lange anfängliche Pufferung warten zu müssen. Bei Verwendung von Fast Start sendet der Server, auf dem Windows Media-Dienste ausgeführt wird, einige Daten am Anfang des Inhalts schneller als die durch die Bitrate des Inhalts angegebene Rate.

Der Standardwert dieser Eigenschaft ist 10.000 Millisekunden.

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

 

 




