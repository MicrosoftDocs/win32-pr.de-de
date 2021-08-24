---
description: Gibt an, ob eine Mediensenke den Hardwaredatenfluss unterstützt.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: MF_STREAM_SINK_SUPPORTS_HW_CONNECTION-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9f663c492e5ae15590cc9240762e90298122790fa350fae51d09dd1199f6d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714375"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>MF STREAM SINK SUPPORTS HW CONNECTION attribute (MF \_ \_ STREAM-SENKE \_ UNTERSTÜTZT \_ \_ HW-VERBINDUNGSattribut)

Gibt an, ob eine Mediensenke den Hardwaredatenfluss unterstützt.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Dieses Attribut wird verwendet, wenn eine Mediensenke ein Hardwaregerät proxt und Daten über einen Hardwarebus empfangen kann. Beispielsweise kann ein Hardwareaudiodecoder Audiodaten direkt an die Audiorenderinghardware senden.

In diesem Szenario werden der Decoder und die Senke weiterhin im Microsoft Media Foundation durch eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT) und eine Mediensenke dargestellt. Allerdings fließen keine Daten zwischen diesen beiden Objekten auf der Pipelineebene, sondern nur auf der Hardwareebene, wie im folgenden Diagramm dargestellt.

![Ein Diagramm, das eine Hardwareproxyquelle zeigt.](images/proxy-mft4.png)

Die Verbindung zwischen MFT und der Mediensenke wird wie folgt ausgehandelt.

1.  Die Pipeline überprüft, ob der MFT ein Hardwareproxy ist, indem das [Attribut MFT \_ ENUM HARDWARE URL Attribute (MFT-ENUM-HARDWARE-URL-Attribut) \_ \_ \_ ](mft-enum-hardware-url-attribute.md) auf dem MFT überprüft wird. Weitere Informationen finden Sie unter [Hardware-MFTs.](hardware-mfts.md)
2.  Die Pipeline ruft einen Zeiger auf die [**INTERFACESStreamSink-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) der Streamsenke auf der Mediensenke ab.
3.  Die Pipeline verwendet den [**POINTERStreamSink-Zeiger,**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) um das MF \_ STREAM SINK SUPPORTS \_ \_ \_ HW \_ CONNECTION-Attribut abzufragen. Wenn dieses Attribut vorhanden und **gleich TRUE** ist, unterstützt die Medienquelle Hardwareverbindungen.
4.  Die Pipeline legt das [Attribut MFT \_ CONNECTED STREAM \_ \_ ATTRIBUTE](mft-connected-stream-attribute.md) für die Streamsenke fest. Der Wert dieses Attributs ist der [**POINTERAttribute-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) aus dem MFT.
5.  Die Pipeline legt das [MFT \_ CONNECTED TO \_ \_ HW \_ STREAM-Attribut](mft-connected-to-hw-stream.md) sowohl in der Streamsenke als auch im MFT auf **TRUE** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




