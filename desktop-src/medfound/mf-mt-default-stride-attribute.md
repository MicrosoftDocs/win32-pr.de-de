---
description: Standardoberflächenschritt für einen nicht komprimierten Videomedientyp. Stride ist die Anzahl der Bytes, die von einer Pixelzeile zur nächsten gesendet werden müssen.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: MF_MT_DEFAULT_STRIDE -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e130918f62d6ff986ced7dd6449dcc2d381a00fc0d7c0342eeb4afcc03833bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035238"
---
# <a name="mf_mt_default_stride-attribute"></a>MF \_ MT \_ DEFAULT \_ STRIDE-Attribut

Standardoberflächenschritt für einen nicht komprimierten Videomedientyp. Stride ist die Anzahl der Bytes, die von einer Pixelzeile zur nächsten gesendet werden müssen.

## <a name="data-type"></a>Datentyp

**UINT32**

Als **INT32-Wert** behandeln.

## <a name="remarks"></a>Hinweise

Der Attributwert wird als **UINT32 gespeichert,** sollte jedoch in einen 32-Bit-Ganzzahlwert mit Vorzeichen konvertiert werden. Stride kann negativ sein.

Stride ist für Bilder von oben nach unten positiv und für Bilder von unten nach oben negativ.

Dieses Attribut gibt den Schritt für eine *zusammenhängende* Darstellung des Bilds im Arbeitsspeicher an. das heißt, eine Darstellung ohne zusätzliche Auf padding bytes nach jeder Zeile. Wenn ein Medienpuffer die [**BERD2DBuffer-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) unterstützt, verwenden Sie die [**METHODE DERT2DBuffer::Lock2D,**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) um den tatsächlichen Schritt der Oberfläche zu erhalten. Dies kann zusätzliche Bytes enthalten.

Weitere Informationen zum Oberflächenschritt finden Sie unter [Image Stride](image-stride.md).

Ein Beispiel zum Berechnen des Standardschritts finden Sie unter [Unkomprimierte Videopuffer.](uncompressed-video-buffers.md)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Bild-Stride](image-stride.md)
</dt> </dl>

 

 




