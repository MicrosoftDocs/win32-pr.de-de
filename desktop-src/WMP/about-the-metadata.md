---
title: Informationen zu den Metadaten
description: Informationen zu den Metadaten
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Windows Media Player,Metadaten
- metadata,about
- Metadaten, Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcccda2af46e60e4bb0733d17e35e1a50d1fe923e9775fa6b10d2c06e3a972a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865360"
---
# <a name="about-the-metadata"></a>Informationen zu den Metadaten

Windows Media Player 10 oder höher versucht, die folgenden Metadatenattribute zu synchronisieren.



| Player-Attribut | Globale WMDM-Konstante  | BESCHREIBUNG                                                                                                 | Erforderliche Version                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| AlbumArtist      | g \_ wszWMDMWeisArtist | Auf NULL endende **Zeichenfolge,** die den Namen des primären Interpreten für das Album enthält.                         | Windows Media Player 11 oder höher. |
| Album            | g \_ wszWMDMWeissTitle  | Auf NULL endende **Zeichenfolge,** die den Titel des Albums enthält, auf dem der Inhalt ursprünglich veröffentlicht wurde.  | Windows Media Player 11 oder höher. |
| Autor           | g \_ wszWMDMAuthor      | Auf NULL endende **Zeichenfolge,** die den Namen des Medienautors oder Akteurs enthält, der dem Inhalt zugeordnet ist.    | Windows Media Player 11 oder höher. |
| BuyNow           | g \_ wszWMDMBuyNow      | **Boolescher Wert,** der angibt, ob der Benutzer den Inhalt erworben hat.                                 | Windows Media Player 10 oder höher. |
| WM/Genre         | g \_ wszWMDMGenre       | Auf NULL endende **Zeichenfolge,** die das Genre des Inhalts enthält.                                             | Windows Media Player 11 oder höher. |
| UserPlayCount    | g \_ wszWMDMPlayCount   | **DWORD,** das die Anzahl der Wiedergaben der digitalen Mediendatei durch den Benutzer enthält.                        | Windows Media Player 10 oder höher. |
| Released      | g \_ wszWMDMYear        | Das Datum der ursprünglichen Freigabe des Elements.                                                               | Windows Media Player 11 oder höher. |
| Titel            | g \_ wszWMDMTitle       | Auf NULL endende **Zeichenfolge,** die den Titel enthält.                                                            | Windows Media Player 11 oder höher. |
| WM/TrackNumber   | g \_ wszWMDMTrack       | **DWORD** mit der Titelnummer des Elements auf dem Album, auf dem es ursprünglich veröffentlicht wurde.         | Windows Media Player 11 oder höher. |
| UserRating       | g \_ wszWMDMUserRating  | **DWORD** mit einem Wert, der die Sternbewertung darstellt, die der Benutzer für die digitale Mediendatei angegeben hat. | Windows Media Player 10 oder höher. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geräteerweiterungen für die beschleunigte Metadatenübertragung**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




