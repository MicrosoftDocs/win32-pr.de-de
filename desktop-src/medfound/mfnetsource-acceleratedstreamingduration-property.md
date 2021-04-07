---
description: Dauer des beschleunigten Streamings für die Netzwerkquelle in Millisekunden.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: MFNETSOURCE_ACCELERATEDSTREAMINGDURATION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863167"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a>MF-Quelle \_ acceleratedstreamingduration (Eigenschaft)

Dauer des beschleunigten Streamings für die Netzwerkquelle in Millisekunden.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**DWORD** (als **Long** gespeichert)

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF-Quelle \_ acceleratedstreamingduration** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie ein **IPropertyStore** -Objekt an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Diese Eigenschaft gilt für das schnell Start Feature von Windows Media Services, das Inhalte schnell wieder gibt, ohne auf eine lange anfängliche Pufferung zu warten. Wenn Sie den schnell Start verwenden, sendet der Server, auf dem Windows Media Services ausgeführt wird, Daten am Anfang der Geschwindigkeit schneller als durch die Bitrate des Inhalts festgelegt.

Der Standardwert dieser Eigenschaft ist 10.000 Millisekunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk Quell Features](network-source-features.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




