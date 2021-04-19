---
description: Gibt den Containertyp einer codierten Datei an.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: MF_TRANSCODE_CONTAINERTYPE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f86b8d5890a771200feda265c3878b6eb7030b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359905"
---
# <a name="mf_transcode_containertype-attribute"></a>MF- \_ transcode- \_ ContainerType-Attribut

Gibt den Containertyp einer codierten Datei an. Die Containertypen werden von Media Foundation unterstützt.

## <a name="data-type"></a>Datentyp

**GUID**

Mögliche Werte für die Containertypen, die von Media Foundation bereitgestellt werden, werden in der folgenden Tabelle beschrieben.



| Wert                                                                                                                                                                                                                                                                 | Bedeutung                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <dt>**MF transcodecontainertype- \_ ASF**</dt> </dl>             | Der ASF-Datei Container.<br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <dt>**MF transcodecontainertype \_ MPEG4**</dt> </dl>     | MP4-Datei Container.<br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <dt>**MF transcodecontainertype \_ MP3**</dt> </dl>             | Der MP3-Datei Container.<br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <dt>**MF transcodecontainertype \_ 3GP**</dt> </dl>             | 3GP-Datei Container. <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <dt>**MF transcodecontainertype \_ AC3**</dt> </dl>             | AC3-Datei Container. <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <dt>**MF transcodecontainertype- \_ ADTs**</dt> </dl>         | ADTS-Datei Container. <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <dt>**MF transcodecontainertype ( \_ MPEG2)**</dt> </dl>     | MPEG2-Datei Container. <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <dt>**MF transcodecontainertype \_ FMPEG4**</dt> </dl> | FMPEG4-Datei Container. <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <dt>**MF transcodecontainertype- \_ Wave**</dt> </dl>         | Wave File-Container.<br/> Wird in Windows 8.1 und höher unterstützt.<br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <dt>**MF transcodecontainertype \_ AVI**</dt> </dl>             | AVI-Datei Container.<br/> Wird in Windows 8.1 und höher unterstützt.<br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <dt>**MF transcodecontainertype \_ AMR**</dt> </dl>             | AMR-Datei Container. <br/>                                                    |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, wenden Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)an.

Um dieses Attribut festzulegen, wenden Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)an.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird sowohl für die Funktion "schnelles transcode" als auch für das Objekt "Sink Writer" verwendet.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

### <a name="fast-transcode"></a>Schnelles transcode

Die Anwendung muss das Container-Attribut im transcodieren-Profil vor dem Erstellen der transcodieren-Topologie festlegen. Der topologiebuilder analysiert dieses Attribut und lädt die entsprechende Medien Senke in der Pipeline. Weitere Informationen finden Sie unter den folgenden Themen:

-   [**IMF transcodeprofile:: getcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [**IMF transcodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a>Senke-Writer

Dieses Attribut kann verwendet werden, um den dateicontainertyp für den senkwriter zu konfigurieren. Weitere Informationen finden Sie unter [senkenwriter-Attribute](sink-writer-attributes.md).

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
</dt> </dl>

 

 




