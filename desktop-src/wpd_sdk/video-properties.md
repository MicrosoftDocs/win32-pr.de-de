---
description: Tragbare Windows-Geräte unterstützen die folgenden Videoeigenschaften.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Video Eigenschaften (portabledevice. h)
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
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358015"
---
# <a name="video-properties"></a>Video Eigenschaften

Tragbare Windows-Geräte unterstützen die folgenden Videoeigenschaften.



| Eigenschaft                                         | VarType        | BESCHREIBUNG                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Video \_ Autor**                           | **VT \_ LPWSTR** | Der Autor der Videodatei.                                                                                                                                                                                                                           |
| **WPD- \_ Video \_ Bitrate**                          | **VT \_ UI4**    | Die Bitrate der Videodatei.                                                                                                                                                                                                                         |
| **WPD- \_ Video \_ Puffer \_ Größe**                     | **VT \_ UI4**    | Ein-Wert, der die erforderliche Video Puffergröße zum Rendering dieser Datei angibt.                                                                                                                                                                              |
| **WPD- \_ Video \_ Gutschriften**                          | **VT \_ LPWSTR** | Das Guthaben, das die Umwandlung und die Gruppe für das Video auflistet.                                                                                                                                                                                                    |
| **WPD- \_ Video- \_ FourCC- \_ Code**                     | **VT \_ DWORD**  | Der registrierte FourCC-Code, der den Codec angibt, der für die Videodatei verwendet wurde. Eine Auflistung von FourCC-Formaten finden Sie im Artikel [registrierte FOURCC Codes und Wave Formats](https://msdn2.microsoft.com/library/ms867195.aspx) auf der MSDN-Website. |
| **WPD- \_ Video \_ Framerate**                        | **VT \_ UI4**    | Die Frame Rate der Videodatei in Frames/Sekunde x 1.000. Beispielsweise wird eine Frame Rate von 29,97 als 29970 dargestellt.                                                                                                                                 |
| **WPD- \_ Video \_ Genre**                            | **VT \_ LPWSTR** | Das Genre dieser Videodatei. Es sind keine Standard Genre Definitionen vorhanden.                                                                                                                                                                                  |
| **WPD \_ - \_ Video \_ schlüsselframe- \_ Abstand**             | **VT \_ UI4**    | Das Intervall zwischen Keyframes in Millisekunden.                                                                                                                                                                                                       |
| **WPD- \_ Video \_ Qualitäts \_ Einstellung**                 | **VT \_ UI4**    | Die Qualitätseinstellung für die Videodatei. Dies ist Codec-abhängig.                                                                                                                                                                                        |
| **WPD-Video recorddebug- \_ \_ \_ Kanal \_ Nummer**      | **VT \_ UI4**    | Die Nummer des Fernsehkanals, von dem das Video aufgezeichnet wurde.                                                                                                                                                                                              |
| **WPD-Video recorddebug- \_ \_ \_ Programm \_ Beschreibung** | **VT \_ LPWSTR** | Eine Beschreibung des aufgezeichneten Fernsehprogramms.                                                                                                                                                                                                       |
| **WPD- \_ Video \_ recordebug \_ Wiederholen**               | **VT \_ bool**   | Ein boolescher Wert, der angibt, ob das Fernsehprogramm eine Wiederholung anzeigt.                                                                                                                                                                     |
| **WPD-Video recorddebug- \_ \_ \_ Stations \_ Name**        | **VT \_ LPWSTR** | Die Fernsehstation, von der das Video aufgezeichnet wurde.                                                                                                                                                                                                |
| **WPD- \_ Video \_ Überprüfungstyp \_**                       | **VT \_ UI4**    | Ein [**WPD \_ - \_ \_ videoscantypes**](wpd-video-scan-types.md) -Enumerator, der das Zeilen Sprung der Video Datei angibt.                                                                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




