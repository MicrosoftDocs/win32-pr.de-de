---
description: Gibt das Gerätekonformitätsprofil für die Codierung von ASF-Dateien (Advanced Streaming Format) an.
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: MF_TRANSCODE_ENCODINGPROFILE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b44a923abc563a84f3536fd6353ac2a3dd2352e472344edf7053d647674908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244231"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>MF \_ TRANSCODE \_ ENCODINGPROFILE-Attribut

Gibt das Gerätekonformitätsprofil für die Codierung von ASF-Dateien (Advanced Streaming Format) an.

## <a name="data-type"></a>Datentyp

**Lpwstr**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetAllocatedString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Attribut beim Transcodieren auf ein Gerät, das Windows unterstützt. Wenn dieses Attribut festgelegt ist, verwendet der Encoder das Gerätekonformitätsprofil oder die Vorlage für Windows Mediencodecs. Legen Sie das -Attribut für das Transcodierungsprofil fest, bevor Sie die Transcodierungstopologie erstellen.

Der Wert dieses Attributs kann eine der Zeichenfolgen für Konformitätsvorlagen sein, die in den folgenden Themen aufgeführt sind:

-   [Vorlagen für die Konformität von Audio-Geräten](../wmformat/audio-device-conformance-templates.md)
-   [Vorlagen für gerätekonforme Videogeräte](../wmformat/video-device-conformance-templates.md)

Für Windows Media Video-Codierung verwendet der Topologie-Generator dieses Attribut, um die [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED-Eigenschaft**](mfpkey-decodercomplexityrequestedproperty.md) für den Encoder festlegen. Der Encoder versucht, den Inhalt mithilfe der angegebenen Vorlage zu codieren. Um die eigentliche Vorlage zu erhalten, durchlaufen Sie die Knoten der Transcodierungstopologie, um einen Zeiger auf den Encoderknoten zu erhalten. Anschließend wird der Wert der [**MFPKEY \_ DECODERCOMPLEXITYPROFILE-Eigenschaft**](mfpkey-decodercomplexityprofileproperty.md) vom Encoder empfangen.

Der Topologie-Generator verwendet auch den Wert dieses Attributs, um die Eigenschaft "DeviceConformanceTemplate" für die ASF-Mediensenke fest zu legen.

Wenn dieses Attribut festgelegt ist, wird das Metadatenobjekt der ASF-Datei immer unabhängig vom von der Anwendung angegebenen Wert des [MF \_ TRANSCODE \_ SKIP METADATA \_ \_ TRANSFER-Attributs](mf-transcode-skip-metadata-transfer.md) generiert.

Typische Werte für dieses Attribut sind:



| Wert   | BESCHREIBUNG                      |
|---------|----------------------------------|
| "AP"    | Video zu erweiterten Profilen           |
| "MP"    | Hauptprofilvideo               |
| "SP"    | Video zu einfachen Profilen             |
| "MP@LL" | Hauptprofil, Video auf mittlerer Ebene |
| "L2"    | Audioprofil, <= 160 KBit/s    |



 

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcodierungs-API](transcode-api.md)
</dt> <dt>

[**CODIERUNGTranscodeProfile::GetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**CODIERUNGTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**BESCHRIFTUNGTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**BESCHRIFTUNGTranscodeProfile::GetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
