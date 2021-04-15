---
description: Gibt an, ob eine Medien Senke den Hardware Datenfluss unterstützt.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: MF_STREAM_SINK_SUPPORTS_HW_CONNECTION-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485206"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>Daten \_ Strom- \_ Senke \_ unterstützt das \_ HW- \_ Verbindungs Attribut

Gibt an, ob eine Medien Senke den Hardware Datenfluss unterstützt.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird verwendet, wenn eine Medien Senke ein Hardware Gerät als Proxy verwendet und Daten über einen Hardwarebus empfangen kann. Beispielsweise kann ein Hardware-Audiodecoder Audiodaten direkt an die audiorenderinghardware senden.

In diesem Szenario werden der Decoder und die Senke weiterhin in der Microsoft Media Foundation durch eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT) und eine Medien Senke dargestellt. Zwischen diesen beiden Objekten auf der Pipeline Ebene werden jedoch keine Daten übertragen, sondern nur auf der Hardwareebene, wie in der folgenden Abbildung dargestellt.

![ein Diagramm, das eine Hardware Proxy Quelle anzeigt.](images/proxy-mft4.png)

Die Verbindung zwischen dem MFT und der Medien Senke wird wie folgt ausgehandelt.

1.  Die Pipeline prüft, ob es sich bei der MFT um einen Hardware Proxy handelt, indem auf der MFT das Attribut Attribut für die MFT-Aufzählung der [ \_ Hardware- \_ \_ URL \_ ](mft-enum-hardware-url-attribute.md) überprüft wird. Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).
2.  Die Pipeline erhält einen Zeiger auf die [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle der Stream-Senke in der Medien Senke.
3.  Die Pipeline verwendet den [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger zum Abfragen der MF-Daten \_ Strom- \_ Senke \_ unterstützt das \_ HW- \_ Verbindungs Attribut. Wenn dieses Attribut vorhanden und gleich **true** ist, unterstützt die Medienquelle Hardware Verbindungen.
4.  Die Pipeline legt das [Attribut Attribut des verbundenen MFT- \_ \_ Streams \_ ](mft-connected-stream-attribute.md) in der streamsenke fest. Der Wert dieses Attributs ist der [**imfattribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger aus dem MFT.
5.  Die Pipeline legt die mit dem [ \_ HW- \_ \_ \_ streamattribut verbundene MFT](mft-connected-to-hw-stream.md) für die streamsenke und die MFT auf " **true** " fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




