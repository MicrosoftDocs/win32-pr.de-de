---
description: Standard Oberflächen Stride für einen unkomprimierten Video Medientyp. Stride ist die Anzahl der Bytes, die erforderlich sind, um von einer Zeile aus Pixel zum nächsten zu wechseln.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: MF_MT_DEFAULT_STRIDE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215142"
---
# <a name="mf_mt_default_stride-attribute"></a>MF \_ MT- \_ Standard-Stride- \_ Attribut

Standard Oberflächen Stride für einen unkomprimierten Video Medientyp. Stride ist die Anzahl der Bytes, die erforderlich sind, um von einer Zeile aus Pixel zum nächsten zu wechseln.

## <a name="data-type"></a>Datentyp

**UINT32**

Als **Int32** -Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Der Attribut Wert wird als **UInt32** gespeichert, sollte jedoch in einen ganzzahligen Wert von 32-Bit-Ganzzahl umgewandelt werden. Stride kann negativ sein.

Stride ist für Top-Down-Bilder positiv und negativ für Bild von unten nach oben.

Dieses Attribut liefert den Schritt für eine zusammen *hängende* Darstellung des Bilds im Arbeitsspeicher. Das heißt, eine Darstellung ohne zusätzliche Auffüll Bytes nach jeder Zeile. Wenn ein Medien Puffer die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle unterstützt, verwenden Sie die [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) -Methode, um den tatsächlichen Schritt der Oberfläche zu erhalten, der möglicherweise zusätzliche Leerzeichen enthält.

Weitere Informationen zu Surface Stride finden Sie unter [Image Stride](image-stride.md).

Ein Beispiel für die Berechnung des Standard Schrittes finden Sie unter [nicht komprimierte Video Puffer](uncompressed-video-buffers.md).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[Bild Schritt](image-stride.md)
</dt> </dl>

 

 




