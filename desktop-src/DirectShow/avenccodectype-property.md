---
description: Gibt das Codierungsschema an.
ms.assetid: a26951d6-67fb-43fb-849f-331416e9d7c2
title: Avenccodectype-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8643c0624b7d82381e2008f2adbd6804e9af9881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341998"
---
# <a name="avenccodectype-property"></a>Avenccodectype (Eigenschaft)

Gibt das Codierungsschema an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi- \_ avenccodectype**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein **BSTR** -Wert, der die Zeichen folgen Darstellung einer GUID enthält. Die folgenden GUIDs sind definiert.



| GUID                                      | Beschreibung                                        |
|-------------------------------------------|----------------------------------------------------|
| Codecapi \_ GUID \_ avencdolbydigitalconsumer | Dolby Digital Consumer-Audiodatei                       |
| Codecapi \_ GUID \_ avencdolbydigitalplus     | Dolby Digital Plus-Audiodatei                           |
| Codecapi \_ GUID \_ avencdolbydigitalpro      | Dolby Digital pro-Audiodatei                            |
| Codecapi \_ GUID \_ avencdts                  | DTS-Audiodaten                                          |
| Codecapi \_ GUID \_ avencdtshd                | DTS-HD-Audiodaten                                       |
| Codecapi \_ GUID \_ avencdv                   | DV-Video                                           |
| Codecapi- \_ GUID \_ AVEncH264Video            | H. 264-Video                                        |
| Codecapi \_ GUID \_ avencmlp                  | Datei für das Verlust lose packen (MLP) des Meridian              |
| Codecapi- \_ GUID \_ AVEncMPEG1Audio           | MPEG-1-Audiodatei                                       |
| Codecapi- \_ GUID \_ AVEncMPEG1Video           | MPEG-1-Video                                       |
| Codecapi- \_ GUID \_ AVEncMPEG2Audio           | MPEG-2-Audiodatei                                       |
| Codecapi- \_ GUID \_ AVEncMPEG2Video           | MPEG-2-Video                                       |
| Codecapi \_ GUID \_ avencpcm                  | PCM-Audiodatei                                          |
| Codecapi \_ GUID \_ avencsdds                 | Audio (Dynamic Digital Sound, SDDS) für Sony            |
| Codecapi \_ GUID \_ avencwmalossless          | Windows Media Audio 9, verlustloses Audiodaten               |
| Codecapi \_ GUID \_ avencwmapro               | Windows Media Audio 9 Professional-Audiodatei (WMA Pro) |
| Codecapi \_ GUID \_ avencwmavoice             | Windows Media Audio 9-Audiosprache                  |
| Codecapi \_ GUID \_ avencwmv                  | Windows Media Video                                |
| Codecapi- \_ GUID \_ AVEndMPEG4Video           | MPEG-4-Video                                       |



 

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Eigenschaft festlegen, um anzugeben, welches Codierungsschema verwendet werden soll. Codecs können diese Eigenschaft auch als Funktion zurückgeben.

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

 

 




