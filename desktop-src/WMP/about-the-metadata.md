---
title: Informationen zu den Metadaten
description: Informationen zu den Metadaten
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Windows-Media Player, Metadaten
- Metadaten, Informationen zu
- Metadaten, Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309300"
---
# <a name="about-the-metadata"></a>Informationen zu den Metadaten

Windows Media Player 10 oder höher versucht, die folgenden Metadatenattribute zu synchronisieren.



| Player-Attribut | Globale WMDM-Konstante  | BESCHREIBUNG                                                                                                 | Erforderliche Version                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Albumartist      | g \_ wszwmdmalbumartist | NULL-terminierte **Zeichenfolge** , die den Namen des primären Künstlers für das Album enthält.                         | Windows Media Player 11 oder höher. |
| Aufzunehmen            | g \_ wszwmdmalbumtitle  | NULL-terminierte **Zeichenfolge** , die den Titel des Albums enthält, auf dem der Inhalt ursprünglich freigegeben wurde.  | Windows Media Player 11 oder höher. |
| Autor           | g \_ wszwmdmauthor      | NULL-terminierte **Zeichenfolge** mit dem Namen des Medienkünstlers oder des Actors, der dem Inhalt zugeordnet ist.    | Windows Media Player 11 oder höher. |
| Jetzt in Kauf           | g \_ wszwmdmbuynow      | **Boolescher** Wert, der angibt, ob der Benutzer den Inhalt kaufen möchte.                                 | Windows Media Player 10 oder höher. |
| WM/Genre         | g \_ wszwmdmgenre       | NULL-terminierte **Zeichenfolge** , die das Genre des Inhalts enthält.                                             | Windows Media Player 11 oder höher. |
| Userplaycount    | g \_ wszwmdmplaycount   | **DWORD** , das die Häufigkeit enthält, mit der der Benutzer die digitale Mediendatei wiedergegeben hat.                        | Windows Media Player 10 oder höher. |
| ReleaseDate      | g \_ wszwmdmyear        | Das Datum der ursprünglichen Version des Elements.                                                               | Windows Media Player 11 oder höher. |
| Titel            | g \_ wszwmdmtitle       | Mit NULL beendete **Zeichenfolge** , die den Titel enthält.                                                            | Windows Media Player 11 oder höher. |
| WM/tracknumber   | g \_ wszwmdmtrack       | **DWORD** , das die Nachverfolgung des Elements auf dem Album enthält, auf dem es ursprünglich veröffentlicht wurde.         | Windows Media Player 11 oder höher. |
| UserRating       | g \_ wszwmdmuserrating  | **DWORD** mit einem Wert, der die Stern Bewertung darstellt, die der Benutzer für die digitale Mediendatei angegeben hat. | Windows Media Player 10 oder höher. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geräte Erweiterungen für die beschleunigte metadatenübertragung**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




