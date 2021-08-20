---
description: Enhanced-Format Metadateien
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Enhanced-Format Metadateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f28a1b14d226fb3ae60dd7b620e3e04565d9c5c05f84704570bda267ca6ced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118068167"
---
# <a name="enhanced-format-metafiles"></a>Enhanced-Format Metadateien

Die Metadatei im *erweiterten Format* besteht aus den folgenden Elementen:

-   Ein Header
-   Eine Tabelle mit Handles für GDI-Objekte
-   Eine private Palette
-   Ein Array von Metadateidatensätzen

Erweiterte Metadateien bieten echte Geräteunabhängigkeit. Sie können sich das in einer erweiterten Metadatei gespeicherte Bild als "Momentaufnahme" der Videoanzeige vorstellen, die zu einem bestimmten Zeitpunkt erstellt wurde. Diese "Momentaufnahme" behält ihre Dimensionen unabhängig davon bei, wo sie auf einem Drucker, einem Plotter, dem Desktop oder im Clientbereich einer beliebigen Anwendung angezeigt wird.

Sie können erweiterte Metadateien verwenden, um ein Bild zu speichern, das mithilfe der GDI-Funktionen (einschließlich neuer Pfad- und Transformationsfunktionen) erstellt wurde. Da das erweiterte Metadateiformat standardisiert ist, können Bilder, die in diesem Format gespeichert sind, von einer Anwendung in eine andere kopiert werden. Und da die Bilder wirklich geräteunabhängig sind, behalten sie garantiert ihre Form und ihren Anteil auf jedem Ausgabegerät bei.

-   [Erweiterte Metadateidatensätze](enhanced-metafile-records.md)
-   [Erweiterte Metadateierstellung](enhanced-metafile-creation.md)
-   [Erweiterte Metadateivorgänge](enhanced-metafile-operations.md)

 

 



