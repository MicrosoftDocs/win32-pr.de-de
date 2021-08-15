---
description: Gibt an, ob ein Stream in einer Videoaufnahmequelle ein Noch-Bild-Datenstrom ist.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: MF_DEVICESTREAM_IMAGE_STREAM-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a42ec0ea6ac8f89c7b35e5ae137c92aaf62006b9b06be689bb7203626f36b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244763"
---
# <a name="mf_devicestream_image_stream-attribute"></a>MF \_ DEVICESTREAM \_ IMAGE \_ STREAM-Attribut

Gibt an, ob ein Stream in einer Videoaufnahmequelle ein Noch-Bild-Datenstrom ist.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Einige Videokameras machen einen Nochbildstream verfügbar, der Bilder mit hoher Auflösung erzeugt. Der Bildstream erzeugt möglicherweise unkomprimierte Bilder oder JPEG-Bilder. Wenn die Kamera über einen Bilddatenstrom verfügt, legt die Medienquelle für das Erfassungsgerät dieses Attribut im Bilddatenstrom auf **TRUE** fest.

Gehen Sie wie folgt vor, um dieses Attribut abzurufen:

1.  Fragen Sie die Medienquelle nach der [**SCHNITTSTELLE "CSVMediaSourceEx"**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) ab.
2.  Rufen Sie [**DEN CURSORMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) auf, um einen [**POINTERAttributes-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) für den Stream abzurufen.
3.  Rufen Sie [**DIE ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) auf, um das Attribut abzurufen.

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

 

 




