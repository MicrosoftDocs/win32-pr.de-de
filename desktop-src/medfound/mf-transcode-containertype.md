---
description: Gibt den Containertyp einer codierten Datei an.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: MF_TRANSCODE_CONTAINERTYPE-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c56b0332c43f10fa61b34f47191e3946a4813b3670249a8d858317067c38d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604690"
---
# <a name="mf_transcode_containertype-attribute"></a>MF \_ TRANSCODE \_ CONTAINERTYPE-Attribut

Gibt den Containertyp einer codierten Datei an. Die Containertypen werden von Media Foundation unterstützt.

## <a name="data-type"></a>Datentyp

**GUID**

Mögliche Werte für die von Media Foundation bereitgestellten Containertypen werden in der folgenden Tabelle beschrieben.



| Wert                                                                                                                                                                                                                                                                 | Bedeutung                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <dt>**MFTranscodeContainerType \_ ASF**</dt> </dl>             | ASF-Dateicontainer.<br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG4**</dt> </dl>     | MP4-Dateicontainer.<br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <dt>**MFTranscodeContainerType \_ MP3**</dt> </dl>             | MP3-Dateicontainer.<br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <dt>**MFTranscodeContainerType \_ 3GP**</dt> </dl>             | 3GP-Dateicontainer. <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <dt>**MFTranscodeContainerType \_ AC3**</dt> </dl>             | AC3-Dateicontainer. <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <dt>**MFTranscodeContainerType \_ ADTS**</dt> </dl>         | ADTS-Dateicontainer. <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG2**</dt> </dl>     | MPEG2-Dateicontainer. <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ FMPEG4**</dt> </dl> | FMPEG4-Dateicontainer. <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <dt>**MFTranscodeContainerType \_ WAVE**</dt> </dl>         | WAVE-Dateicontainer.<br/> Wird in Windows 8.1 und höher unterstützt.<br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <dt>**MFTranscodeContainerType \_ AVI**</dt> </dl>             | AVI-Dateicontainer.<br/> Wird in Windows 8.1 und höher unterstützt.<br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <dt>**MFTranscodeContainerType \_ AMR**</dt> </dl>             | AMR-Dateicontainer. <br/>                                                    |



 

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetGUID auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetGUID auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl mit dem Fast Transcode-Feature als auch mit dem Sink Writer-Objekt verwendet.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

### <a name="fast-transcode"></a>Schnelle Transcodierung

Die Anwendung muss das Containerattribut für das Transcodierungsprofil festlegen, bevor die Transcodierungstopologie erstellt wird. Der Topologie-Generator analysiert dieses Attribut und lädt die entsprechende Mediensenke in die Pipeline. Weitere Informationen finden Sie in den folgenden Themen:

-   [**CODTRANSCODEProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [**ÜBERTRANSCODEProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a>Sink Writer

Dieses Attribut kann verwendet werden, um den Dateicontainertyp für den Senkenwriter zu konfigurieren. Weitere Informationen finden Sie unter [Sink Writer Attributes](sink-writer-attributes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcodieren der API](transcode-api.md)
</dt> </dl>

 

 




