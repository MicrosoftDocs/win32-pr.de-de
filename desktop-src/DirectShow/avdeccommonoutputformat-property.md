---
description: Gibt das Ausgabeformat für den Decoder an.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Avdeccommonoutputformat-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522480"
---
# <a name="avdeccommonoutputformat-property"></a>Avdeccommonoutputformat (Eigenschaft)

Gibt das Ausgabeformat für den Decoder an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdeccommonoutputformat**

## <a name="property-value"></a>Eigenschaftswert



| GUID                                                               | Beschreibung                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Codecapi \_ GUID \_ avdecaudiooutputformat \_ PCM                        | PCM-Audiodaten mit beliebig vielen Kanälen                                                                                                                                                                             |
| Codecapi \_ GUID \_ avdecaudiooutputformat \_ PCM- \_ Kopfhörer            | Stereo-PCM-Audiodaten, verwenden von left-only/Right (LO/RO)-Downmix                                                                                                                                                        |
| Codecapi \_ GUID \_ avdecaudiooutputformat \_ PCM \_ Stereo \_ Auto          | Stereo PCM-Audiodatei mit automatischer Auswahl des Stereo-downmischmodus (LO/RO oder lt/RT). Sie können diesen Wert für Audioformate verwenden, in denen der Eingabestream den bevorzugten downmischungs Modus definiert, z. b. Dolby AC-3. |
| Codecapi \_ GUID \_ avdecaudiooutputformat \_ PCM \_ Stereo \_ matrixencoded | Stereo PCM-Audiodatei mit Matrix codiertem Stereo Downmix (LT/RT)                                                                                                                                                       |
| Codecapi \_ GUID \_ avdecaudiooutputformat \_ SPDIF \_ Bitstream           | S/PDIF (Sony/Philips Digital Interface Format) komprimierter Bitstream, wie von IEC-60958 definiert                                                                                                                        |
| Codecapi \_ GUID \_ avdecaudiooutputformat \_ SPDIF \_ PCM                 | E/a PDIF PCM Stereo, gemäß IEC-60958                                                                                                                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




