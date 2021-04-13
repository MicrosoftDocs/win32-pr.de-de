---
title: WM/MediaClassSecondaryID
description: Das WM/MediaClassSecondaryID-Attribut enthält die GUID der sekundären Medienklasse.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- WM/MediaClassSecondaryID Windows Media-Format
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389270"
---
# <a name="wmmediaclasssecondaryid"></a>WM/MediaClassSecondaryID

Das **WM/MediaClassSecondaryID-** Attribut enthält die GUID der sekundären Medienklasse.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmmediaclasssecondaryid

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ- \_ GUID**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut sollte auf einen der Werte in der folgenden Tabelle festgelegt werden.



| GUID der sekundären Klasse                   | BESCHREIBUNG                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "E0236BEB-C281-4EDE-A36D-7AF76A3D45B5" | Verwenden Sie für audiobookdateien.                                                                                                                                                               |
| "3a172 A13-2bd9-4831-835b-114b f" | Verwendung für Audiodateien, die gesprochene Wörter enthalten, aber keine Audiobücher sind. Beispielsweise sind die-Beispiel-Comedy-Routinen.                                                                           |
| "6677db9b-e5a0-4063-a1ad-aceb52840cf1" | Verwenden Sie für Audiodateien, die sich auf Neuigkeiten beziehen.                                                                                                                                                    |
| "1b824a67-3s80-4e3e-9cde-f 7361b0s5f 1B" | Verwenden Sie für Audiodateien mit dem Inhalt von Talk anzeigen.                                                                                                                                             |
| "1fe2e091-4E1E-40ce-b22d-348c732e0b10" | Verwenden Sie dies für Videodateien im Zusammenhang mit Neuigkeiten.                                                                                                                                                    |
| "D6DE1D88-C77C-4593-BF-9c61e8c373e3" | Verwenden Sie dies für Videodateien mit webbasierten anzeigen, kurzen Filmen, Film Anhängern usw. Dies ist der allgemeine Bezeichner für Video Unterhaltung, der nicht in eine andere Kategorie passt. |
| "00033368-5009-4ac3-A820-5d2d09a4e7c1" | Verwenden Sie für Audiodateien, die Soundclips von spielen enthalten.                                                                                                                                  |
| "F24FF731-96FC-4D0F-A2F5-5A3483682B1A" | Verwenden Sie dies für Audiodateien, die vollständige Lieder aus Spiel Sound Spuren enthalten. Wenn nur ein Teil eines Liedes in der Datei codiert ist, verwenden Sie stattdessen den Bezeichner für Game Soundclips.                   |
| "E3E689E2-BA8C-4330-96DF-A0EEEFFA6876" | Verwenden Sie dies für Videodateien, die Musikvideos enthalten.                                                                                                                                            |
| "B76628F4-300D-443D-9CB5-01C285109DAF" | Verwenden Sie dies für Videodateien mit dem allgemeinen Home-Video.                                                                                                                                      |
| "A9B87FC9-BD47-4BF0-AC4F-655B89F7D868" | Verwenden Sie für Videodateien, die Featurefilme enthalten.                                                                                                                                           |
| "BA7F258A-62F7-47A9-B21F-4651C42A000E" | Verwendung für Videodateien, die Fernsehsendungen enthalten. Verwenden Sie für webbasiertes anzeigen den allgemeineren Bezeichner.                                                                                  |
| "44051b5b-B103-4b5c-92ab-93060a9463f" | Verwenden Sie dies für Videodateien, die Firmenvideos enthalten. Beispielsweise aufgezeichnete Besprechungen oder Schulungsvideos.                                                                                      |
| "0b710218-8c0c-475E-af73-4c41c0c8f" | Verwenden Sie dies für Videodateien mit Start Videos aus Fotos.                                                                                                                        |



 

Wenn Sie einen Bezeichner der sekundären Klasse angeben, sollte die Datei auch ein primäres klassenbezeichnerattribut enthalten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM/mediaclassprimaryid**](wm-mediaprimaryid.md)
</dt> </dl>

 

 




