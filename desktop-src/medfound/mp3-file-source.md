---
description: Die MP3-Datei Quelle analysiert MP3-Dateien.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: MP3-Datei Quelle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130497"
---
# <a name="mp3-file-source"></a>MP3-Datei Quelle

Die MP3-Datei Quelle analysiert MP3-Dateien.

Die MP3-Datei Quelle gibt Puffer aus, die MPEG-1-Audioframes enthalten. Die Audiocodierung wird nicht decodiert.

## <a name="file-extensions-and-mime-types"></a>Dateierweiterungen und MIME-Typen

Die MP3-Datei Quelle ist die Standard Medienquelle für die folgende Dateinamenerweiterung:

-   .mp3

Es ist auch die Standard Medienquelle für die folgenden MIME-Typen.

-   Audiodatei/MPEG
-   Audiodatei/x-MP3
-   Audiodatei/x-MPEG

## <a name="media-types"></a>Medientypen

Der von der MP3-Datei Quelle angebotene Medientyp enthält die folgenden Attribute.



| Attribut                                                                                    | BESCHREIBUNG                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                                    | Gleich **mfmediatype \_ -Audiodatei**.                                                                                                                   |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                           | Entspricht **mfaudioformat \_ MP3** oder **mfaudioformat \_ MPEG**.                                                                                        |
| [**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Die durchschnittliche Anzahl von Bytes pro Sekunde.                                                                                                                |
| [**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md)             | Gleich 1.                                                                                                                                        |
| [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)                   | Anzahl der Audiokanäle.                                                                                                                          |
| [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md)      | Anzahl von Audiobeispielen pro Sekunde.                                                                                                                |
| [**\_ \_ Benutzer \_ Daten für MF-MT**](mf-mt-user-data-attribute.md)                                      | Enthält den Teil einer [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) -Struktur, der nach dem **wfx** -Member der-Struktur angezeigt wird. |



 

## <a name="interfaces"></a>Schnittstellen

Die MP3-Datei Quelle macht die folgenden Schnittstellen über [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))verfügbar:

-   [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMF Media Event Generator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Außerdem werden die folgenden Schnittstellen über [**IMF-Service**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)verfügbar gemacht:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Dienst-GUID</th>
<th>Schnittstelle</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MF_METADATA_PROVIDER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_PROPERTY_HANDLER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
<blockquote>
[!Note]<br />
Siehe <a href="shell-metadata-providers.md">shellmetadatenanbieter</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>Imfratecontrol</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>Imfratesupport</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                           |
| DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Medienquellen und senken](media-sources-and-sinks.md)
</dt> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[Quellresolver](source-resolver.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
