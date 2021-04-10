---
description: Maximale Dauer des beschleunigten Streamings in Millisekunden, wenn die Netzwerkquelle UDP-Transport verwendet.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050457"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a>MF NetSource \_ maxudpacceleratedstreamingduration (Eigenschaft)

Maximale Dauer des beschleunigten Streamings in Millisekunden, wenn die Netzwerkquelle UDP-Transport verwendet.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**DWORD** (als **Long** gespeichert)

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource \_ maxudpacceleratedstreamingduration** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Für den UDP-Transport überschreibt diese Eigenschaft die Eigenschaft [**msnetsource \_ acceleratedstreamingduration**](mfnetsource-acceleratedstreamingduration-property.md) , wenn der Wert dieser Eigenschaft niedriger ist.

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Der Standardwert dieser Eigenschaft ist 8.000 Millisekunden.

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

 

 




