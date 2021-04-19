---
description: Gibt an, ob eine Medienquelle den Hardware Datenfluss unterstützt.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362875"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a>Der MF- \_ \_ Quellstream \_ unterstützt das \_ HW- \_ Verbindungs Attribut

Gibt an, ob eine Medienquelle den Hardware Datenfluss unterstützt.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird verwendet, wenn eine Medienquelle einen Proxy für ein Hardware Gerät verwendet und Daten nach unten über einen Hardwarebus übertragen kann, ohne dass Daten an die CPU gesendet werden. Beispielsweise kann eine Webcam H. 264-codiertes Video direkt an einen integrierten Hardware Decoder übermitteln.

In diesem Szenario werden Quelle und Decoder weiterhin in der Microsoft Media Foundation durch ein [Medienquellen](media-sources.md) Objekt und eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT) dargestellt. Zwischen diesen beiden Objekten auf der Pipeline Ebene werden jedoch keine Daten übertragen, sondern nur auf der Hardwareebene, wie in der folgenden Abbildung dargestellt.

![ein Diagramm, das eine Hardware Proxy Quelle anzeigt.](images/proxy-mft3.png)

Die Verbindung zwischen der Medienquelle und der MFT wird wie folgt ausgehandelt.

1.  Die Pipeline fragt die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab. (Diese Schnittstelle ist für Medienquellen optional, die unterstützt.)
2.  Die Pipeline ruft [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) auf, um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger zu erhalten.
3.  Die Pipeline Abfragen für den MF- \_ Quelldaten \_ Strom \_ unterstützen das HW- \_ \_ Verbindungs Attribut. Wenn das Attribut vorhanden und gleich **true** ist, unterstützt die Medienquelle Hardware Verbindungen.
4.  Die Pipeline prüft, ob es sich bei der MFT auch um einen Hardware Proxy handelt, indem auf der MFT das Attribut Attribut für die MFT-Aufzählung der [ \_ Hardware- \_ \_ URL \_ ](mft-enum-hardware-url-attribute.md) überprüft wird. Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).
5.  Die Pipeline legt das [Attribut Attribut des verbundenen MFT- \_ \_ Streams \_ ](mft-connected-stream-attribute.md) auf dem MFT fest. Der Wert dieses Attributs ist der [**imfattribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger, der aus der Medienquelle in Schritt 2 abgerufen wurde.
6.  Die Pipeline legt die mit dem [ \_ HW- \_ \_ \_ streamattribut verbundene MFT](mft-connected-to-hw-stream.md) für die Medienquelle und die MFT auf " **true** " fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Hardware-MFTs](hardware-mfts.md)
</dt> </dl>

 

 




