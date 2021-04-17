---
title: Ändern der Größe des Dialog Felds zum Erwerb von Lizenzen
description: Ändern der Größe des Dialog Felds zum Erwerb von Lizenzen
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Windows Media Player, Ändern der Größe des Lizenz Erwerbs (Dialogfeld)
- Dialogfeld "Windows Media Player, Lizenzerwerb"
- Windows Media Player, DRM_LicenseAcqURL-Attribut
- Dialogfeld zum Ändern der Größe des Lizenz Erwerbs
- Dialogfeld "Lizenzerwerb"
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388509"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a>Ändern der Größe des Dialog Felds zum Erwerb von Lizenzen

Sie können Abfrage Zeichenfolgen-Parameter an die URL anfügen, die Sie für das DRM-Attribut " **\_ licenset URL** " bereitstellen, um eine Größe für das Dialogfeld "Lizenz Erfassung für Windows Media Player 10 oder höher" anzugeben. In der folgenden Tabelle sind die Parameter aufgeführt.



| Parameter | BESCHREIBUNG                                        |
|-----------|----------------------------------------------------|
| *Dlgx*    | Gibt die Breite des Dialog Felds in Pixel an.  |
| *Dlgy*    | Gibt die Höhe des Dialog Felds in Pixel an. |



 

Beispielsweise würde die folgende Lizenz Erwerbs-URL bewirken, dass das Dialogfeld für die Lizenz Erfassung mit einer Größe von 800 x 600 Pixel geöffnet wird:


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



Die maximale Größe für das Dialogfeld überschreitet niemals die aktuellen Bildschirm Abmessungen minus 20 Pixel. Die Mindestgröße beträgt 333 x 210 Pixel (Standardgröße).

Für dieses Feature ist Windows Media Player 10 oder höher erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




