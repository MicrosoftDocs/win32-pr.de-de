---
description: Die folgenden GUIDs definieren Kategorien für Media Foundation Transformationen (MFTs). Diese Kategorien werden verwendet, um MFTs zu registrieren und aufzuzählen.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7bc74054ad9f201b1f2ca53b526826d34c510d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863964"
---
# <a name="mft_category"></a>MFT- \_ Kategorie

Die folgenden GUIDs definieren Kategorien für Media Foundation Transformationen (MFTs). Diese Kategorien werden verwendet, um MFTs zu registrieren und aufzuzählen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </dl></td>
<td style="text-align: left;">Audiodecoder.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">Audioeffekte.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </dl></td>
<td style="text-align: left;">Audioencoder.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl> <dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </dl></td>
<td style="text-align: left;">Demultiplexer.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl> <dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </dl></td>
<td style="text-align: left;">Multiplexers (.<br/>
<blockquote>
[!Note]<br />
In Windows Vista unterstützt die Media Foundation Pipeline keine MFTs mit mehr als einer Eingabe. MFTs mit mehreren Eingaben werden in Windows 7 unterstützt.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl> <dt><strong>MFT_CATEGORY_OTHER</strong></dt> </dl></td>
<td style="text-align: left;">Verschiedene MFTs.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </dl></td>
<td style="text-align: left;">Video-Decoders.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">Video Effekte.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">Effekte der Videorenderer.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </dl></td>
<td style="text-align: left;">Video Encoder.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Eingeführt in Windows 7.
</blockquote>
<br/> Video Prozessoren. <br/> Diese Kategorie ist auf MFTs beschränkt, die Formatkonvertierungen für unkomprimierte Videos ausführen, einschließlich Farb Raum Konvertierungen. Verwenden Sie für Video Effekte, die die Darstellung des Bilds ändern (z. b. einen Weichzeichnereffekt oder eine Farb-zu-Graustufen Transformation) die <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> Kategorie.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> <dt>

[**MF-Wert**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[**MF-Datei**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[**MF-tregiester**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




