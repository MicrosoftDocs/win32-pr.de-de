---
description: Gibt an, ob der Bilddatenstrom in einer Videoaufnahmequelle unabhängig vom Videostream ist.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52392839c5f196159692bc9c4624cbda67b869471d6737c4cff60c847f890e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956680"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>MF \_ DEVICESTREAM \_ INDEPENDENT IMAGE \_ \_ STREAM-Attribut

Gibt an, ob der Bilddatenstrom in einer Videoaufnahmequelle unabhängig vom Videostream ist.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Einige USB-Videokameras machen einen Stream verfügbar, der Standbilder erzeugt. Bei einigen Kameras gibt der Bildstream einfach den nächsten Frame aus dem Videostream zurück. In anderen Kameras funktioniert der Bildstream unabhängig vom Videostream. Wenn die Kamera über einen unabhängigen Bilddatenstrom verfügt, legt die Medienquelle für das Erfassungsgerät dieses Attribut im Bilddatenstrom auf **TRUE** fest.

Gehen Sie wie folgt vor, um dieses Attribut abzurufen:

1.  Fragen Sie die Medienquelle nach der [**SCHNITTSTELLE "CSVMediaSourceEx"**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) ab.
2.  Rufen Sie [**DEN CURSORMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) auf, um einen [**POINTERAttributes-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) für den Stream abzurufen.
3.  Rufen Sie [**DIE ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) auf, um das Attribut abzurufen.

Dieses Attribut gilt nur, wenn das [MF \_ DEVICESTREAM \_ IMAGE \_ STREAM-Attribut](mf-devicestream-image-stream.md) **TRUE** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




