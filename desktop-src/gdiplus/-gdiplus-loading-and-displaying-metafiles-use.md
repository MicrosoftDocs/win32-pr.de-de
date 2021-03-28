---
description: Die Image-Klasse stellt grundlegende Methoden zum Laden und Anzeigen von Rasterbildern und Vektorbildern bereit. Die Metafile-Klasse, die von der Image-Klasse erbt, bietet speziellere Methoden zum Aufzeichnen, anzeigen und untersuchen von Vektorbildern.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Laden und Anzeigen von Metadateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041714"
---
# <a name="loading-and-displaying-metafiles"></a>Laden und Anzeigen von Metadateien

Die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse stellt grundlegende Methoden zum Laden und Anzeigen von Rasterbildern und Vektorbildern bereit. Die [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Klasse, die von der **Image** -Klasse erbt, bietet speziellere Methoden zum Aufzeichnen, anzeigen und untersuchen von Vektorbildern.

Zum Anzeigen eines Vektor Bilds (Metadatei) auf dem Bildschirm benötigen Sie ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt und ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt. Übergeben Sie den Namen einer Datei (oder eines Zeigers an einen Stream) an einen **bildkonstruktor** . Nachdem Sie ein **Image** -Objekt erstellt haben, übergeben Sie die Adresse dieses **Bild** Objekts an die **DrawImage** -Methode eines **Grafik** Objekts.

Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus einer EMF-Datei (Enhanced Metafile) erstellt. Anschließend wird das Bild mit der linken oberen Ecke bei (60, 10) gezeichnet:


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



Die folgende Abbildung zeigt das an der angegebenen Position gezeichnete Bild.

![Screenshot eines Fensters, das ein Bild enthält und den Ursprungs Punkt angibt](images/imageposition2.png)

 

 



