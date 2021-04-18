---
description: Gibt das Geräte Konformitäts Profil für die Codierung von ASF-Dateien (Advanced Streaming Format) an.
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: MF_TRANSCODE_ENCODINGPROFILE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527407"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>MF- \_ transcode- \_ encodingprofile-Attribut

Gibt das Geräte Konformitäts Profil für die Codierung von ASF-Dateien (Advanced Streaming Format) an.

## <a name="data-type"></a>Datentyp

**LPWSTR**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getalloeredstring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Attribut bei der Transcodierung auf ein Gerät, das Windows-Medien unterstützt. Wenn dieses Attribut festgelegt ist, verwendet der Encoder das Geräte Konformitäts Profil bzw. die Vorlage für Windows Media Codecs. Legen Sie das-Attribut für das transcodieren-Profil fest, bevor Sie die transcodieren-Topologie erstellen.

Der Wert dieses Attributs kann eine der in den folgenden Themen aufgeführten Konformitäts Vorlagen Zeichenfolgen sein:

-   [Konformitäts Vorlagen für Audiogeräte](../wmformat/audio-device-conformance-templates.md)
-   [Vorlagen für die Konformitäts Konformität von Video Geräten](../wmformat/video-device-conformance-templates.md)

Bei Windows Media Video Codierung verwendet der topologiebuilder dieses Attribut, um die [**mfpkey- \_ decodercomplexityangeforderten**](mfpkey-decodercomplexityrequestedproperty.md) -Eigenschaft für den Encoder festzulegen. Der Encoder versucht, die angegebene Vorlage zu verwenden, um den Inhalt zu codieren. Um die tatsächliche Vorlage zu erhalten, Durchsuchen Sie die Knoten der transcodieren-Topologie, um einen Zeiger auf den encoderknoten zu erhalten. Dann erhalten Sie den Wert der Eigenschaft [**mfpkey \_ decodercomplexityprofile**](mfpkey-decodercomplexityprofileproperty.md) aus dem Encoder.

Der Topologiegenerator verwendet auch den Wert dieses Attributs, um die Eigenschaft "opviceconformancetemplate" in der ASF-Medien Senke festzulegen.

Wenn dieses Attribut festgelegt ist, wird das Metadatenobjekt der ASF-Datei immer generiert, unabhängig davon, welcher Wert von [der Anwendung \_ \_ \_ \_ ](mf-transcode-skip-metadata-transfer.md) angegeben wurde.

Die folgenden Werte sind für dieses Attribut typisch:



| Wert   | BESCHREIBUNG                      |
|---------|----------------------------------|
| Unglücks    | Video zum erweiterten Profil           |
| Schlanken    | Video zum Hauptprofil               |
| El    | Video zu einfachem Profil             |
| "MP@LL" | Hauptprofil, Video auf mittlerer Ebene |
| L2    | Audioprofil, <= 160 KBit/s    |



 

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcode-API](transcode-api.md)
</dt> <dt>

[**IMF transcodeprofile:: getaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**IMF transcodeprofile:: setaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**IMF transcodeprofile:: setvideoattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**IMF transcodeprofile:: getvideoattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
