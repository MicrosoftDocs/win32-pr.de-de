---
description: Gibt eine Zahl zwischen 0 und 100 an, die den Kompromiss zwischen Codierungsqualität und Codierungs Geschwindigkeit angibt.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: MF_TRANSCODE_QUALITYVSSPEED-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371476"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a>MF- \_ transcode \_ qualityvsspeed-Attribut

Gibt eine Zahl zwischen 0 und 100 an, die den Kompromiss zwischen Codierungsqualität und Codierungs Geschwindigkeit angibt.

## <a name="data-type"></a>Datentyp

**UINT32**

Der Wert dieser Eigenschaft hat den folgenden Bereich.



| Wert                                                                          | Bedeutung                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>0</dt> </dl>   | Niedrigere Qualität, schnellere Codierung.<br/>  |
| <dl> <dt>100</dt> </dl> | Höhere Qualität, langsamere Codierung.<br/> |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut hat denselben GUID-Wert wie die Eigenschaft " [avenccommonqualityvsspeed](../directshow/avenccommonqualityvsspeed-property.md) ", die für [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi)definiert ist, und hat dieselbe Interpretation.

Die Anwendung kann dieses Attribut für das transcodieren-Profil festlegen, bevor die transcodieren-Topologie für Windows Media Codecs zu erstellen ist. Der Wert muss zwischen 0 und 100 liegen. Für den Videostream ordnet der transcodieren-Topologiegenerator dem von der Anwendung angegebenen Wert einen Wert zu und gibt den zugeordneten Wert an die **\_ complexityex-Eigenschaft von mfpkey** des Encoders an. Niedrigere Werte ermöglichen es dem Encoder, weniger komplizierte Codierungs Algorithmen zu verwenden. Die Verwendung einfacherer Algorithmen erzeugt eine Ausgabe mit geringerer Qualität, aber der Codierungsprozess ist schneller und erfordert weniger Verarbeitungsleistung.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcode-API](transcode-api.md)
</dt> <dt>

[**IMF transcodeprofile:: setvideoattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
