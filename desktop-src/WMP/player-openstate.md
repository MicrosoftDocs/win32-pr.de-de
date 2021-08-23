---
title: Player.openState
description: Die openState-Eigenschaft ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player.openState-Windows Media Player
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7c0b88d3cab5d5bae4efb1e9a2a5032709943d82484b073302bf0b45a6f5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995980"
---
# <a name="playeropenstate"></a>Player.openState

Die **openState-Eigenschaft** ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.

## <a name="syntax"></a>Syntax

*Player* . **openState**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**). Die Enumerationskonst constant im C-Stil kann abgeleitet werden, indem dem Zustandswert "wmpos" vorangestellt wird. Die Konstante für den PlaylistOpening-Zustand ist beispielsweise **wmposPlaylistOpening.**



| Wert | State                   | BESCHREIBUNG                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nicht definiert               | Windows Media Player befindet sich in einem nicht definierten Zustand.                                                                                                         |
| 1     | PlaylistChangeing        | Eine neue Wiedergabeliste wird geladen.                                                                                                                    |
| 2     | PlaylistLocating        | Windows Media Player versucht, die Wiedergabeliste zu finden. Die Wiedergabeliste kann lokal (Bibliothek oder Metadatei mit der Dateierweiterung .asx) oder remote sein. |
| 3     | Wiedergabeliste: Herstellen einer Verbindung      | Herstellen einer Verbindung mit der Wiedergabeliste.                                                                                                                            |
| 4     | PlaylistLoading         | Die Wiedergabeliste wurde gefunden und wird jetzt abgerufen.                                                                                                    |
| 5     | WiedergabelisteOpening         | Die Wiedergabeliste wurde abgerufen und wird jetzt analysiert und geladen.                                                                                        |
| 6     | PlaylistOpenNoMedia     | Die Wiedergabeliste ist geöffnet.                                                                                                                                      |
| 7     | PlaylistChanged         | CurrentPlaylist wurde eine neue **Wiedergabeliste zugewiesen.**                                                                                               |
| 8     | MediaChanging           | Ein neues Medienelement wird geladen.                                                                                                                |
| 9     | MediaLocating           | Windows Media Player wird das Medienelement durch suchen. Die Datei kann lokal oder remote sein.                                                                      |
| 10    | Medienverbindung         | Herstellen einer Verbindung mit dem Server, der das Medienelement enthält.                                                                                                    |
| 11    | MediaLoading            | Das Medienelement wurde gefunden und wird jetzt abgerufen.                                                                                                |
| 12    | MediaOpening            | Das Medienelement wurde abgerufen und wird jetzt geöffnet.                                                                                                 |
| 13    | MediaOpen               | Das Medienelement ist jetzt geöffnet.                                                                                                                                |
| 14    | BeginCodecAcquisition   | Starten des Codec-Kaufs.                                                                                                                            |
| 15    | EndCodecAcquisition     | Die Codec-Übernahme ist abgeschlossen.                                                                                                                         |
| 16    | BeginLicenseAcquisition | Erwerben einer Lizenz für die Wiedergabe von DRM-geschützten Inhalten.                                                                                                     |
| 17    | EndLicenseAcquisition   | Die Lizenz zur Wiedergabe von DRM-geschützten Inhalten wurde erworben.                                                                                               |
| 18    | BeginIndividualization  | Beginnen Sie mit der DRM-Individualisierung.                                                                                                                           |
| 19    | EndIndividualization    | Die DRM-Individualisierung wurde abgeschlossen.                                                                                                              |
| 20    | MediaWaiting            | Warten auf Medienelement.                                                                                                                                |
| 21    | OpeningUnknownURL       | Öffnen einer URL mit einem unbekannten Typ.                                                                                                                    |



 

## <a name="remarks"></a>Hinweise

Windows Media Player, dass Zustände nicht in einer bestimmten Reihenfolge auftreten. Darüber hinaus tritt nicht jeder Zustand notwendigerweise während einer Abfolge von Ereignissen auf. Sie sollten keinen Code schreiben, der von der Zustandsordnung abhängig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.OpenStateChange-Ereignis**](player-player-openstatechange.md)
</dt> </dl>

 

 





