---
description: Für DV-Videos sind eine Reihe von Untertypen definiert. Jeder verfügt über einen FOURCC-Code und einen entsprechenden GUID-Wert. Nicht alle diese Formate werden unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise".
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: DV Video-Untertypen (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ee08bad5970d016ada2bf129132bf34261be9ba856071d9f90f1e73de91978
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102950"
---
# <a name="dv-video-subtypes"></a>DV-Videountertypen

Für DV-Videos sind eine Reihe von Untertypen definiert. Jeder verfügt über einen FOURCC-Code und einen entsprechenden GUID-Wert. Nicht alle diese Formate werden unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise".

## <a name="consumer-formats"></a>Consumerformate



| FOURCC | GUID               | Datenrate | BESCHREIBUNG                  |
|--------|--------------------|-----------|------------------------------|
| 'dvsl' | MEDIASUBTYPE \_ dvsl | 12,5 MBit/s | SD-DVCR (525-60 oder 625-50)   |
| "dvsd" | MEDIASUBTYPE \_ dvsd | 25 MBit/s   | SDL-DVCR (525-60 oder 625-50)  |
| "dvhd" | MEDIASUBTYPE \_ dvhd | 50 MBit/s   | HD-DVCR (1125-60 oder 1250-50) |



 

Weitere Informationen zu diesen Formaten finden Sie unter IEC-61834.

## <a name="professional-formats"></a>Professional Formate



| FOURCC | GUID               | Datenrate | BESCHREIBUNG                                 |
|--------|--------------------|-----------|---------------------------------------------|
| "dv25" | MEDIASUBTYPE \_ dv25 | 25 MBit/s   | DVCPRO 25 (525-60 oder 625-50).               |
| "dv50" | MEDIASUBTYPE \_ dv50 | 50 MBit/s   | DVCPRO 50 (525-60 oder 625-50)                |
| "dvh1" | MEDIASUBTYPE \_ dvh1 | 100 MBit/s  | DVCPRO 100 (1080/60i, 1080/50i oder 720/60P) |



 

Weitere Informationen zu dv25 und dv50 finden Sie unter SMPTE 314M und SMPTE 370M für weitere Informationen zu dvh1.

## <a name="miscellaneous"></a>verschiedene gefährliche Stoffe

In der Headerdatei Uuids.h sind zwei zusätzliche DV-Untertypen definiert. Diese entsprechen FOURCC-Codes, die von bestimmten DV-Codecs erzeugt werden. sie entsprechen keinen definierten DV-Standards. Diese Untertypen sind veraltet und sollten nicht verwendet werden.



| FOURCC | GUID               |
|--------|--------------------|
| "DVCS" | MEDIASUBTYPE \_ DVCS |
| 'DVSD' | MEDIASUBTYPE \_ DVSD |



 

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die unterstützten Datenraten (in Megabits pro Sekunde (MBit/s) für die MSDV- und UVC-Treiber.



| Betriebssystem                                                                 | MSDV-Treiber (IEEE 1394) | UVC-Treiber    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| Windows XP Service Pack 1 oder früher                                             | 12.5, 25                | Nicht verfügbar |
| Windows XP Service Pack 2 oder höher, Windows Server 2003 Service Pack 1 oder höher. | 12.5, 25, 50, 100       | 12.5, 25      |



 

Bei Streams mit 25 MBit/s hat sich das Verhalten des MSDV-Treibers in Windows Vista vor Windows Vista geändert. Der MSDV-Treiber hat den Medientyp immer auf MEDIASUBTYPE dvsd für Streams mit 25 MBit/s festgelegt, unabhängig davon, ob die Quelle \_ SDL-DVCR oder DVCPRO 25 war. Der Medientyp "dv25" wurde nicht verwendet. Ab Windows Vista unterscheidet der MSDV-Treiber zwischen diesen beiden Formaten. Für SDL-DVCR wird weiterhin der Untertyp "dvsd" verwendet. Für DVCPRO 25 wird nun der Untertyp "dv25" verwendet.

Die Filter DirectShow [DV Splitter](dv-splitter-filter.md) und [DV Video Decoder](dv-video-decoder-filter.md) unterstützen nur SDL-DVCR-Formate. Die Daten können PAL oder NTSC sein. Möglicherweise sind Filter oder Codecs von Drittanbietern verfügbar, die andere DV-Formate analysieren können, solange die Datenrate vom MSDV- oder UVC-Treiber unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[MSDV-Treiber](msdv-driver.md)
</dt> <dt>

[Videountertypen](video-subtypes.md)
</dt> </dl>

 

 




