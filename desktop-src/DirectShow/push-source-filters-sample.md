---
description: Beispiel für Pushquellenfilter
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Beispiel für Pushquellenfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e72a9be7e5fa81d4fe2dc006c6d12e42f4f94d91561823b7f26a8400bbddda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747790"
---
# <a name="push-source-filters-sample"></a>Beispiel für Pushquellenfilter

## <a name="description"></a>Beschreibung

Dieses Beispiel besteht aus drei Quellfiltern, die die folgenden Quelldaten als Videostream bereitstellen:

-   CPushSourceBitmap: Einzelne Bitmap (aus aktuellem Verzeichnis geladen)
-   CPushSourceBitmapSet: Satz von Bitmaps (aus dem aktuellen Verzeichnis geladen)
-   CPushSourceDesktop: Kopie des aktuellen Desktopimages (nur GDI)

## <a name="usage"></a>Verbrauch

Um einen Filter zu verwenden, laden Sie ihn in GraphEdit, und rendern Sie dessen Ausgabepin. Dadurch wird ein Videorenderer (und möglicherweise ein Farbraumkonverterfilter) verbunden, und Sie können die Ausgabe anzeigen. Wenn Sie die Ausgabe in einer AVI-Datei rendern möchten, laden Sie den AVI Mux, laden Sie einen Dateiwriterfilter, geben Sie dem Dateiwriter einen Ausgabenamen an, und rendern Sie den Ausgabepin des PushSource-Filters. Sie können auch Videointeressierer, Videoeffekte usw. laden und verbinden.

> [!Note]  
> Der Desktoperfassungsfilter unterstützt keine Hardwareüberlagerungen und erfasst daher keine Videos, die auf einer Überlagerungsoberfläche gerendert werden, oder Cursor, die über Hardwareüberlagerungen angezeigt werden. GDI wird verwendet, um das aktuelle Desktopbild in eine Bitmap zu konvertieren, die als Medienbeispiel an den Ausgabepin übergeben wird.

 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version des [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ \] SDK-Stammbeispiele* \\ Multimedia \\ \\ DirectShow Filters \\ \\ PushSource.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



