---
description: Gibt die Länge von nalus in der Stichprobe an. Hierbei handelt es sich um ein MF-BLOB, das auf komprimierte Eingabe Beispiele für den H. 264-Decoder festgelegt ist.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: MF_NALU_LENGTH_INFORMATION-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347936"
---
# <a name="mf_nalu_length_information-attribute"></a>MF \_ Nalu- \_ Längen \_ Informations Attribut

Gibt die Länge von nalus in der Stichprobe an. Hierbei handelt es sich um ein MF- **BLOB** , das auf komprimierte Eingabe Beispiele für den H. 264-Decoder festgelegt ist.

## <a name="data-type"></a>Datentyp

**BLOB**

## <a name="remarks"></a>Bemerkungen

Damit dieses Attribut festgelegt werden kann, muss das Medium den Typ "mediasubtype H264" aufweisen, \_ und das Attribut " [MF \_ Nalu \_ length \_ Set](mf-nalu-length-set.md) " muss für den Eingabe Medientyp von mediasubtype H264 festgelegt werden \_ .

Legen Sie \_ \_ \_ für das Eingabe Beispiel die Informationen der MF-Nalu-Länge als **BLOB** fest, mit einem DWORD für jede Nalu im Beispiel. Wenn z. b. AUD (9 Bytes), SPS (25 Bytes), PPS (10 Bytes), IDR slice1 (50 k), IDR Slice 2 (60 k) vorhanden sind, sollten 5 DWords mit den Werten 9, 25, 10, 50 k, 60 k im **BLOB** vorhanden sein.

Hier finden Sie Code, in dem das **BLOB** festgelegt wird. **rgdwnalulengthinfo** ist ein Array vom Typ DWORD und **uinalulengthidx** ist die gültige Nalu-Länge, die auf das **BLOB** festgelegt ist.


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



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

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




