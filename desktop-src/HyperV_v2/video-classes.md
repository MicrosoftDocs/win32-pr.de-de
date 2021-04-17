---
description: Alle virtuellen Computer spiegeln das vorhanden sein eines emulierten S3-Video Controllers und eines beschleunigten, synthetischen Video Controllers wider.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Video Klassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485694"
---
# <a name="video-classes"></a>Video Klassen

Alle virtuellen Computer spiegeln das vorhanden sein eines emulierten S3-Video Controllers und eines beschleunigten, synthetischen Video Controllers wider.

Jedem Anzeige Controller ist ein Video Head-Objekt zugeordnet. Auf einem virtuellen Computer kann zu einem beliebigen Zeitpunkt nur ein Anzeige Controller aktiv sein.

Für jede aktive Remote Sitzung, die mit einem virtuellen Computer verbunden ist, ist eine Terminal Verbindung vorhanden.

Im folgenden finden Sie WMI-Klassen für die Virtualisierung im Zusammenhang mit Videos.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                  | BESCHREIBUNG                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ S3DisplayController**](msvm-s3displaycontroller.md)<br/>               | Stellt den Zustand des emulierten S3-Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist.<br/>       |
| [**MSVM \_ syntheticdisplaycontroller**](msvm-syntheticdisplaycontroller.md)<br/> | Stellt den Status des synthetischen Anzeige Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist.<br/> |
| [**MSVM \_ systemterminalconnection**](msvm-systemterminalconnection.md)<br/>     | Ordnet eine virtuelle Maschine einer Terminal Verbindung zu.<br/>                                                        |
| [**MSVM \_ terminalconnection**](msvm-terminalconnection.md)<br/>                 | Gibt den Status einer aktiven Remote Sitzung an, die mit einer virtuellen Maschine interagiert.<br/>                             |
| [**MSVM- \_ videohead**](msvm-videohead.md)<br/>                                   | Beschreibt die primäre Zeichen Oberfläche auf einem Anzeige Controller.<br/>                                                  |
| [**MSVM \_ videoheadoncontroller**](msvm-videoheadoncontroller.md)<br/>           | Ordnet einen Video Kopf dem Videocontroller zu, der ihn enthält.<br/>                                             |



 

 

 




