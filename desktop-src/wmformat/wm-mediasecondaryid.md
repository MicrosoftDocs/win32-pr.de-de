---
title: WM/MediaClassSecondaryID
description: Das WM/MediaClassSecondaryID-Attribut enthält die GUID der sekundären Medienklasse.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- WM/MediaClassSecondaryID windows Media Format
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a37c0b4314a518132d08454ef2cf7472273795cbb0b50f98d22b800e06cc1b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431644"
---
# <a name="wmmediaclasssecondaryid"></a>WM/MediaClassSecondaryID

Das **WM/MediaClassSecondaryID-Attribut** enthält die GUID der sekundären Medienklasse.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMMediaClassSecondaryID

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYP-GUID**

## <a name="remarks"></a>Hinweise

Dieses Attribut sollte auf einen der Werte in der folgenden Tabelle festgelegt werden.



| GUID der sekundären Klasse                   | BESCHREIBUNG                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "E0236BEB-C281-4EDE-A36D-7AF76A3D45B5" | Verwenden Sie für Audiobuchdateien.                                                                                                                                                               |
| "3A172A13-2BD9-4831-835B-114F6A95943F" | Wird für Audiodateien verwendet, die gesprochenes Wort enthalten, aber keine Audiobücher sind. Beispiel: Stand-Up-Routinen.                                                                           |
| "6677DB9B-E5A0-4063-A1AD-ACEB52840CF1" | Verwenden Sie für Audiodateien im Zusammenhang mit Nachrichten.                                                                                                                                                    |
| "1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B" | Verwenden Sie für Audiodateien mit Talk show-Inhalten.                                                                                                                                             |
| "1FE2E091-4E1E-40CE-B22D-348C732E0B10" | Verwenden Sie für Videodateien im Zusammenhang mit Nachrichten.                                                                                                                                                    |
| "D6DE1D88-C77C-4593-BFBC-9C61E8C373E3" | Verwenden Sie für Videodateien, die webbasierte Shows, kurze Filme, Filmtrailer usw. enthalten. Dies ist der allgemeine Bezeichner für Videounterhaltung, der nicht in eine andere Kategorie passt. |
| "00033368-5009-4AC3-A820-5D2D09A4E7C1" | Wird für Audiodateien verwendet, die Soundclips von Spielen enthalten.                                                                                                                                  |
| "F24FF731-96FC-4D0F-A2F5-5A3483682B1A" | Wird für Audiodateien verwendet, die vollständige Titel aus Spielsoundspuren enthalten. Wenn nur ein Teil eines Titels in der Datei codiert ist, verwenden Sie stattdessen den Bezeichner für Spielsoundclips.                   |
| "E3E689E2-BA8C-4330-96DF-A0EEEFFA6876" | Verwenden Sie für Videodateien, die Musikvideos enthalten.                                                                                                                                            |
| "B76628F4-300D-443D-9CB5-01C285109DAF" | Wird für Videodateien verwendet, die allgemeine Startvideos enthalten.                                                                                                                                      |
| "A9B87FC9-BD47-4BF0-AC4F-655B89F7D868" | Wird für Videodateien verwendet, die Featurevideos enthalten.                                                                                                                                           |
| "BA7F258A-62F7-47A9-B21F-4651C42A000E" | Verwenden Sie für Videodateien, die Fernsehsendungen enthalten. Verwenden Sie für webbasierte Shows den generischeren Bezeichner.                                                                                  |
| "44051B5B-B103-4B5C-92AB-93060A9463F0" | Wird für Videodateien verwendet, die Unternehmensvideos enthalten. Beispielsweise aufgezeichnete Besprechungen oder Trainingsvideos.                                                                                      |
| "0B710218-8C0C-475E-AF73-4C41C0C8F8CE" | Wird für Videodateien verwendet, die Heimvideos enthalten, die von Fotos erstellt wurden.                                                                                                                        |



 

Wenn Sie einen bezeichner der sekundären Klasse angeben, sollte die Datei auch ein Primäres Klassenbezeichnerattribut enthalten.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)
</dt> </dl>

 

 




