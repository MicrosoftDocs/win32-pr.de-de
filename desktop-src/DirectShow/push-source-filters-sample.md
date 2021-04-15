---
description: Beispiel für Push-Quell Filter
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Beispiel für Push-Quell Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521331"
---
# <a name="push-source-filters-sample"></a>Beispiel für Push-Quell Filter

## <a name="description"></a>BESCHREIBUNG

Dieses Beispiel besteht aus einem Satz von drei Quell filtern, die die folgenden Quelldaten als Videostream bereitstellen:

-   Cpushsourcebitmap: Single Bitmap (aus aktuellem Verzeichnis geladen)
-   Cpushsourcebitmapset: Satz von Bitmaps (aus aktuellem Verzeichnis geladen)
-   Cpushsourcedesktop: Kopie des aktuellen Desktop Abbilds (nur GDI)

## <a name="usage"></a>Verbrauch

Wenn Sie einen Filter verwenden möchten, laden Sie ihn in GraphEdit, und rendieren Sie seine Ausgabe-PIN. Dadurch wird eine Verbindung mit einem Videorenderer (und möglicherweise mit einem Farb Raum Konverter-Filter) hergestellt, und Sie können die Ausgabe anzeigen. Wenn Sie die Ausgabe in eine AVI-Datei renderten möchten, laden Sie die Datei "AVI MUX", laden Sie einen Datei Schreiber Filter, geben Sie einen Ausgabe Namen an den dateiwriter an, und renderten Sie die Ausgabe-PIN des pushsource Sie können auch Video Kompressoren, Video Effekte usw. Laden und verbinden.

> [!Note]  
> Der Desktop Erfassungs Filter bietet keine Unterstützung für Hardware Überlagerungen, sodass das Video, das auf einer über Lagerungs Oberfläche gerendert wird, oder Cursor, die über die Hardware über Er verwendet GDI zum Konvertieren des aktuellen Desktop Bilds in eine Bitmap, die als Beispiel für ein Medium an die Ausgabe-PIN übergeben wird.

 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ pushsource.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



