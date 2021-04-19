---
description: Eine Reihe von Untertypen sind für das DV-Video definiert. Jede verfügt über einen FourCC-Code und einen entsprechenden GUID-Wert. Nicht alle diese Formate werden unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise".
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: DV-Video Untertypen (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356003"
---
# <a name="dv-video-subtypes"></a>DV-Video Untertypen

Eine Reihe von Untertypen sind für das DV-Video definiert. Jede verfügt über einen FourCC-Code und einen entsprechenden GUID-Wert. Nicht alle diese Formate werden unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise".

## <a name="consumer-formats"></a>Consumerformate



| FOURCC | GUID               | Datenrate | BESCHREIBUNG                  |
|--------|--------------------|-----------|------------------------------|
| "dvsl" | Mediasubtype \_ dvsl | 12,5 MBit/s | SD-dvcr (525-60 oder 625-50)   |
| "DVSD" | Mediasubtype \_ DVSD | 25 Mbit/s   | SDL-dvcr (525-60 oder 625-50)  |
| "dvhd" | Mediasubtype \_ dvhd | 50 MBit/s   | HD-dvcr (1125-60 oder 1250-50) |



 

Weitere Informationen zu diesen Formaten finden Sie unter IEC-61834.

## <a name="professional-formats"></a>Professionelle Formate



| FOURCC | GUID               | Datenrate | BESCHREIBUNG                                 |
|--------|--------------------|-----------|---------------------------------------------|
| 'dv25' | Mediasubtype \_ DV25 | 25 Mbit/s   | DVCPro 25 (525-60 oder 625-50).               |
| 'dv50' | Mediasubtype \_ DV50 | 50 MBit/s   | DVCPRO 50 (525-60 oder 625-50)                |
| 'dvh1' | Mediasubtype \_ dvh1 | 100 MBit/s  | DVCPRO 100 (1080/60i, 1080/50i oder 720/60p) |



 

Weitere Informationen zu DV25 und DV50 sowie zu SMPTE 370m finden Sie unter SMPTE 314m.

## <a name="miscellaneous"></a>Verschiedenes

Zwei weitere DV-Untertypen sind in der Header Datei "UUIDs. h" definiert. Diese entsprechen den FourCC-Codes, die von bestimmten DV-Codecs erstellt werden. Sie entsprechen keinen definierten DV-Standards. Diese Untertypen sind veraltet und sollten nicht verwendet werden.



| FOURCC | GUID               |
|--------|--------------------|
| DVCS | mediasubtype- \_ dvcs |
| "DVSD" | mediasubtype \_ DVSD |



 

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden die unterstützten Datenraten für die msdv-und UVC-Treiber in meits pro Sekunde (Mbit/s) angezeigt.



| Betriebssystem                                                                 | Msdv-Treiber (IEEE 1394) | UVC-Treiber    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| Windows XP Service Pack 1 oder früher                                             | 12,5, 25                | Nicht verfügbar |
| Windows XP Service Pack 2 oder höher, Windows Server 2003 Service Pack 1 oder höher. | 12,5, 25, 50, 100       | 12,5, 25      |



 

Für Datenströme mit 25 Mbit/s hat sich das Verhalten des msdv-Treibers in Windows Vista vor Windows Vista geändert. der msdv-Treiber hat den Medientyp immer auf mediasubtype \_ DVSD für 25 Mbit/s-Streams festgelegt, unabhängig davon, ob die Quelle SDL-dvcr oder DVCPro 25 war. Der Medientyp ' DV25 ' wurde nicht verwendet. Ab Windows Vista unterscheidet der msdv-Treiber nun zwischen diesen beiden Formaten. Für SDL-dvcr wird weiterhin der "DVSD"-Untertyp verwendet. Bei DVCPro 25 wird nun der Untertyp "DV25" verwendet.

Die Filter "DirectShow [DV Splitter](dv-splitter-filter.md) " und " [DV Video Decoder](dv-video-decoder-filter.md) " unterstützen nur SDL-dvcr-Formate. Die Daten können PAL oder NTSC sein. Möglicherweise sind Filter oder Codecs von Drittanbietern verfügbar, mit denen andere DV-Formate analysiert werden können, solange die Datenmenge vom msdv-oder UVC-Treiber unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Msdv-Treiber](msdv-driver.md)
</dt> <dt>

[Video Untertypen](video-subtypes.md)
</dt> </dl>

 

 




