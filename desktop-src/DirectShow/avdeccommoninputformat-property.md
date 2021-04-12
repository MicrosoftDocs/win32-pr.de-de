---
description: Gibt das aktuelle Eingabeformat für den Decoder an.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Avdeccommoninputformat-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482283"
---
# <a name="avdeccommoninputformat-property"></a>Avdeccommoninputformat (Eigenschaft)

Gibt das aktuelle Eingabeformat für den Decoder an.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdeccommoninputformat**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein **BSTR** -Wert, der die Zeichen folgen Darstellung einer GUID enthält. Die folgenden GUIDs sind definiert.



| **GUID**                                            | BESCHREIBUNG                                    |
|-----------------------------------------------------|------------------------------------------------|
| **Codecapi- \_ GUID \_ avdecaudioinputaac**              | "Advanced audiocoding" (AAC)                    |
| **Codecapi- \_ GUID \_ avdecaudioinputdolbydigitalplus** | Dolby Digital Plus-Audiodatei                       |
| **Codecapi- \_ GUID \_ avdecaudioinputdolby**            | Dolby-Audiodatei                                    |
| **Codecapi- \_ GUID \_ avdecaudioinputdts**              | DTS-Audiodaten                                      |
| **Codecapi \_ GUID \_ avdecaudioinpuderaac**            | High-Efficiency erweiterte Audiocodierung (HE-AAC) |
| **Codecapi- \_ GUID \_ avdecaudioinputmpeg**             | MPEG-Audiodatei                                     |
| **Codecapi- \_ GUID \_ avdecaudioinputpcm**              | PCM-Audiodatei                                      |
| **Codecapi- \_ GUID \_ avdecaudioinputwma**              | Windows Media Audio                            |
| **Codecapi- \_ GUID \_ avdecaudioinputwmapro**           | Windows Media Audio 9 Professional (WMA Pro)   |



 

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

 

 




