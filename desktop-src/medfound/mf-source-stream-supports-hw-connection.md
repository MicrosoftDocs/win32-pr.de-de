---
description: Gibt an, ob eine Medienquelle den Hardwaredatenfluss unterstützt.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659672b11cbcaa51f543eec8239f56ba792584a4b1ac44af25ed76016cdeb2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955145"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a>MF \_ SOURCE STREAM SUPPORTS HW CONNECTION attribute (MF-QUELLSTREAM \_ UNTERSTÜTZT \_ \_ \_ HW-VERBINDUNGSattribut)

Gibt an, ob eine Medienquelle den Hardwaredatenfluss unterstützt.

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="remarks"></a>Hinweise

Dieses Attribut wird verwendet, wenn eine Medienquelle einen Proxy an ein Hardwaregerät sendet und Daten nachgeschaltet über einen Hardwarebus übertragen kann, ohne Daten an die CPU zu senden. Beispielsweise kann eine Webcam H.264-codiertes Video direkt an einen integrierten Hardwaredecoder senden.

In diesem Szenario werden Quelle und Decoder weiterhin in [](media-sources.md) der Microsoft Media Foundation medienquellenobjekt und einer Media Foundation Transform (MFT) dargestellt. [](media-foundation-transforms.md) Allerdings fließen keine Daten zwischen diesen beiden Objekten auf der Pipelineebene, sondern nur auf der Hardwareebene, wie im folgenden Diagramm dargestellt.

![Ein Diagramm, das eine Hardwareproxyquelle zeigt.](images/proxy-mft3.png)

Die Verbindung zwischen der Medienquelle und MFT wird wie folgt ausgehandelt.

1.  Die Pipeline fragt die Medienquelle für die [**BENUTZEROBERFLÄCHEMediaSourceEx-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) ab. (Diese Schnittstelle ist optional, damit Medienquellen unterstützt werden.)
2.  Die Pipeline ruft [**DEN TYPSMEDIASourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) auf, um einen [**ATTRIBUTATTRIBUTEs-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) zu erhalten.
3.  Die Pipelineabfragen für das MF \_ SOURCE \_ STREAM SUPPORTS \_ \_ HW \_ CONNECTION-Attribut. Wenn das Attribut vorhanden und gleich **TRUE** ist, unterstützt die Medienquelle Hardwareverbindungen.
4.  Die Pipeline überprüft, ob MFT auch ein Hardwareproxy ist, indem sie auf das [Attribut MFT \_ ENUM HARDWARE URL Attribute (MFT-ENUM-HARDWARE-URL-Attribut) \_ \_ \_ ](mft-enum-hardware-url-attribute.md) im MFT überprüft. Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).
5.  Die Pipeline legt das [Attribut MFT \_ CONNECTED STREAM \_ \_ ATTRIBUTE](mft-connected-stream-attribute.md) auf dem MFT fest. Der Wert dieses Attributs ist der VON der Medienquelle in Schritt 2 abgerufene [**ATTRIBUTEAttribute-Zeiger.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
6.  Die Pipeline legt das [MFT \_ CONNECTED TO \_ \_ HW \_ STREAM-Attribut](mft-connected-to-hw-stream.md) sowohl für die Medienquelle als auch für MFT auf TRUE fest. 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Hardware-MFTs](hardware-mfts.md)
</dt> </dl>

 

 




