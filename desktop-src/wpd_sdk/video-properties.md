---
description: Windows Portable Geräte unterstützen die folgenden Videoeigenschaften.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Videoeigenschaften (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6e7bbab3416f50a95d2ae29e2be0ef5ecdcad6eed0112f940e5c34b593f2b79a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083384"
---
# <a name="video-properties"></a>Videoeigenschaften

Windows Portable Geräte unterstützen die folgenden Videoeigenschaften.



| Eigenschaft                                         | VarType        | Beschreibung                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ VIDEO \_ AUTHOR**                           | **VT \_ LPWSTR** | Der Autor der Videodatei.                                                                                                                                                                                                                           |
| **WPD \_ VIDEO \_ BITRATE**                          | **VT \_ UI4**    | Die Bitrate der Videodatei.                                                                                                                                                                                                                         |
| **\_ \_ WPD-VIDEOPUFFERGRÖßE \_**                     | **VT \_ UI4**    | Ein -Wert, der die erforderliche Videopuffergröße zum Rendern dieser Datei angibt.                                                                                                                                                                              |
| **\_WPD-VIDEOGUTHABEN \_**                          | **VT \_ LPWSTR** | Das Guthaben, in dem die Umwandlung und das Team für das Video aufgeführt sind.                                                                                                                                                                                                    |
| **WPD \_ VIDEO \_ FOURCC \_ CODE**                     | **VT \_ DWORD**  | Der registrierte FourCC-Code, der den Codec angibt, der für die Videodatei verwendet wurde. Eine Liste der FourCC-Formate finden Sie im Artikel [Registered FOURCC Codes and WAVE Formats (Registrierte FOURCC-Codes und WAVE-Formate)](https://msdn2.microsoft.com/library/ms867195.aspx) auf der MSDN-Website. |
| **WPD \_ VIDEO \_ FRAMERATE**                        | **VT \_ UI4**    | Die Bildfrequenz der Videodatei in Frames/Sekunde x 1.000. Beispielsweise wird eine Bildfrequenz von 29,97 als 29970 dargestellt.                                                                                                                                 |
| **WPD \_ VIDEO \_ GENRE**                            | **VT \_ LPWSTR** | Das Genre dieser Videodatei. Es gibt keine Standardgenredefinitionen.                                                                                                                                                                                  |
| **WPD \_ VIDEO \_ KEY \_ FRAME \_ DISTANCE**             | **VT \_ UI4**    | Das Intervall zwischen Keyframes in Millisekunden.                                                                                                                                                                                                       |
| **EINSTELLUNG \_ FÜR WPD-VIDEOQUALITÄT \_ \_**                 | **VT \_ UI4**    | Die Qualitätseinstellung für die Videodatei. Dies ist codecabhängig.                                                                                                                                                                                        |
| **\_WPD-VIDEO \_ \_ AUFGEZEICHNETTV-KANALNUMMER \_**      | **VT \_ UI4**    | Die Nummer des Fernsehkanals, von dem das Video aufgezeichnet wurde.                                                                                                                                                                                              |
| **WPD \_ VIDEO \_ RECORDEDTV \_ PROGRAM \_ DESCRIPTION** | **VT \_ LPWSTR** | Eine Beschreibung des aufgezeichneten Fernsehprogramms.                                                                                                                                                                                                       |
| **WPD \_ VIDEO \_ RECORDEDTV \_ REPEAT**               | **VT \_ BOOL**   | Ein boolescher Wert, der angibt, ob das Fernsehprogramm eine Wiederholungsshow war.                                                                                                                                                                     |
| **WPD \_ VIDEO \_ RECORDEDTV \_ STATION \_ NAME**        | **VT \_ LPWSTR** | Die Fernsehstation, von der das Video aufgezeichnet wurde.                                                                                                                                                                                                |
| **WPD \_ VIDEO \_ SCAN \_ TYPE**                       | **VT \_ UI4**    | Ein [**WPD \_ VIDEO SCAN \_ TYPES-Enumerator, \_**](wpd-video-scan-types.md) der das Interlacing der Videodatei angibt.                                                                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




