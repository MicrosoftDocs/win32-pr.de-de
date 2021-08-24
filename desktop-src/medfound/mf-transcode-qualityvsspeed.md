---
description: Gibt eine Zahl zwischen 0 und 100 an, die den Kompromiss zwischen Codierungsqualität und Codierungsgeschwindigkeit angibt.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: MF_TRANSCODE_QUALITYVSSPEED -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7498cd319f347d8509f42e1713e1b2e267b32406eceb073ea9ca1e4cb4ea8d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604670"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a>MF \_ TRANSCODE \_ QUALITYVSSPEED-Attribut

Gibt eine Zahl zwischen 0 und 100 an, die den Kompromiss zwischen Codierungsqualität und Codierungsgeschwindigkeit angibt.

## <a name="data-type"></a>Datentyp

**UINT32**

Der Wert dieser Eigenschaft hat den folgenden Bereich.



| Wert                                                                          | Bedeutung                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>0</dt> </dl>   | Niedrigere Qualität, schnellere Codierung.<br/>  |
| <dl> <dt>100</dt> </dl> | Höhere Qualität, langsamere Codierung.<br/> |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Dieses Attribut verfügt über den gleichen GUID-Wert wie die [avencCommonQualityVsSpeed-Eigenschaft,](../directshow/avenccommonqualityvsspeed-property.md) die für [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)definiert ist, und hat die gleiche Interpretation.

Die Anwendung kann dieses Attribut für das Transcodierungsprofil festlegen, bevor die Transcodierungstopologie für Windows Mediencodecs erstellt wird. Der Wert muss im Bereich von 0 bis 100 liegen. Bei Videostreams ordnet der Transcodierungstopologie-Generator dem von der Anwendung angegebenen Wert einen Wert zu und stellt den zugeordneten Wert der **MFPKEY \_ COMPLEXITYEX-Eigenschaft** des Encoders zur Verfügung. Niedrigere Werte ermöglichen es dem Encoder, weniger komplizierte Codierungsalgorithmen zu verwenden. Durch die Verwendung einfacherer Algorithmen wird eine Ausgabe mit geringerer Qualität erzeugt, der Codierungsprozess ist jedoch schneller und erfordert weniger Verarbeitungsleistung.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcodierungs-API](transcode-api.md)
</dt> <dt>

[**CODIERUNGTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
