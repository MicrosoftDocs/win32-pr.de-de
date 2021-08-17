---
description: Für mehrere MPEG-2-Medientyp-GUIDs definiert das Windows DDK Namen, die sich von den in DirectShow verwendeten Namen unterscheiden. Die folgende Tabelle zeigt die DirectShow-Namen (definiert in Ksuuids.h) und die entsprechenden Kernelmodusnamen (definiert in Ksmedia.h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: MPEG-2-Kernelmedientypen (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cfbbd93bfb4d9c21a7ab2b496e69458e2754d95ae4427ad163c4f2a06e4165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952259"
---
# <a name="mpeg-2-kernel-media-types"></a>MPEG-2-Kernelmedientypen

Für mehrere MPEG-2-Medientyp-GUIDs definiert das Windows DDK Namen, die sich von den in DirectShow verwendeten Namen unterscheiden. Die folgende Tabelle zeigt die DirectShow-Namen (definiert in Ksuuids.h) und die entsprechenden Kernelmodusnamen (definiert in Ksmedia.h).



| Name in "Ksuuids.h"              | Name in Ksmedia.h                          |
|--------------------------------|--------------------------------------------|
| FORMAT \_ WaveFormatEx           | \_KSDATAFORMAT-SPEZIFIZIERER \_ WAVEFORMATEX      |
| FORMAT \_ MPEG2Video             | \_KSDATAFORMAT-BEZEICHNER \_ MPEG2 \_ VIDEO      |
| MEDIASUBTYPE \_ ATSC \_ SI         | \_KSDATAFORMAT-UNTERTYP \_ ATSC \_ SI            |
| MEDIASUBTYPE \_ DOLBY \_ AC3       | KSDATAFORMAT \_ SUBTYPE \_ AC3 \_ AUDIO          |
| MEDIASUBTYPE \_ DVB \_ SI          | \_KSDATAFORMAT-UNTERTYP \_ : SI \_             |
| MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO | KSDATAFORMAT \_ SUBTYPE \_ LPCM \_ AUDIO         |
| MEDIASUBTYPE \_ \_ MPEG2-AUDIO     | KSDATAFORMAT \_ SUBTYPE \_ MPEG2 \_ AUDIO        |
| MEDIASUBTYPE \_ \_ MPEG2-PROGRAMM   | STATIC \_ KSDATAFORMAT \_ TYPE \_ MPEG2 \_ PROGRAM |
| MEDIASUBTYPE \_ \_ MPEG2-TRANSPORT | KSDATAFORMAT-TYP \_ \_ \_ MPEG2-TRANSPORT       |
| MEDIASUBTYPE \_ MPEG2 \_ VIDEO     | KSDATAFORMAT \_ SUBTYPE \_ MPEG2 \_ VIDEO        |
| MEDIATYPE \_ \_ MPEG2-ABSCHNITTE     | \_MPEG2-ABSCHNITTE DES KSDATAFORMAT-TYPS \_ \_        |
| MEDIATYPE \_ Audio               | KSDATAFORMAT-AUDIO \_ \_                  |
| MEDIATYPE \_ MPEG2 \_ PES          | KSDATAFORMAT-TYP \_ \_ MPEG2 \_ PES             |
| \_MEDIATYPE-Video               | KSDATAFORMAT-TYP \_ \_ VIDEO                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MPEG-2-Medientypen](mpeg-2-media-types.md)
</dt> </dl>

 

 




