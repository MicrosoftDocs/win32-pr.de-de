---
description: Metadatendateien Enhanced-Format
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Metadatendateien Enhanced-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978625"
---
# <a name="enhanced-format-metafiles"></a>Metadatendateien Enhanced-Format

Die *Metadatei mit erweitertem Format* besteht aus den folgenden Elementen:

-   Ein-Header
-   Eine Tabelle mit Handles für GDI-Objekte
-   Eine private Palette
-   Ein Array von Metadatei-Datensätzen.

Erweiterte Metadatendateien bieten echte Geräteunabhängigkeit. Sie können sich das Bild, das in einer erweiterten Metadatei gespeichert ist, als "Momentaufnahme" der Videoanzeige vorstellen, die zu einem bestimmten Zeitpunkt erstellt wurde. Diese "Momentaufnahme" behält die Dimensionen unabhängig davon bei, wo Sie auf einem Drucker, einem Plotter, dem Desktop oder im Client Bereich einer beliebigen Anwendung angezeigt werden.

Sie können Erweiterte Metadateien zum Speichern eines Bilds verwenden, das mit den GDI-Funktionen (einschließlich neuer Pfad-und Transformations Funktionen) erstellt wurde. Da das erweiterte Metadatei-Format standardisiert ist, können Bilder, die in diesem Format gespeichert sind, aus einer Anwendung in eine andere kopiert werden. und da die Bilder wirklich Geräte unabhängig sind, gewährleisten Sie, dass Sie Ihre Form und den Anteil an allen Ausgabegeräten beibehalten.

-   [Erweiterte Metafile-Datensätze](enhanced-metafile-records.md)
-   [Erweiterte metadateierstellung](enhanced-metafile-creation.md)
-   [Erweiterte metadateivorgänge](enhanced-metafile-operations.md)

 

 



