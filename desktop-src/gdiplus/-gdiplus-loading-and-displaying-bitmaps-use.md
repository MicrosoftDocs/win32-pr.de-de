---
description: Um ein Rasterbild (Bitmap) auf dem Bildschirm anzuzeigen, benötigen Sie ein Bildobjekt und ein Grafikobjekt.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Laden und Anzeigen von Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: db3ec9e1d586a585380123aa01d9553ad1f57f60efb93c28d2d974f54d56b249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115000"
---
# <a name="loading-and-displaying-bitmaps"></a>Laden und Anzeigen von Bitmaps

Weitere Informationen finden Sie auch im [WIC Viewer GDI+ Beispiel-App](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).

Um ein Rasterbild (Bitmap) auf dem Bildschirm anzuzeigen, benötigen Sie ein [**Bildobjekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) und ein [**Grafikobjekt.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Übergeben Sie den Namen einer Datei (oder eines  Zeigers auf einen Stream) an einen Imagekonstruktor. Nachdem Sie ein **Image-Objekt** erstellt haben, übergeben Sie die Adresse dieses **Image-Objekts** an die **DrawImage-Methode** eines **Graphics-Objekts.**

Im folgenden Beispiel wird ein [**Bildobjekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) aus einer JPEG-Datei erstellt und dann das Bild mit der oberen linken Ecke um (60, 10) zeichnet:

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

Die folgende Abbildung zeigt das Bild, das an der angegebenen Position gezeichnet wird.

![Screenshot eines Fensters, das ein Bild enthält, mit einer Ausrufezeichen für den Ursprungspunkt ](images/imageposition1.png)

Die [**Image-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) stellt grundlegende Methoden zum Laden und Anzeigen von Rasterbildern und Vektorbildern bereit. Die [](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) Bitmap-Klasse, die von der **Image-Klasse** erbt, stellt speziellere Methoden zum Laden, Anzeigen und Bearbeiten von Rasterbildern bereit. Beispielsweise können Sie ein **Bitmapobjekt** aus einem Symbolhandle (HICON) erstellen.

Das folgende Beispiel ruft ein Handle für ein Symbol ab und verwendet dieses Handle dann, um ein [**Bitmap-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) zu erstellen. Der Code zeigt das Symbol an, indem die Adresse des **Bitmap-Objekts** an die **DrawImage-Methode** eines [**Graphics-Objekts**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) übergeben wird.

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a>Siehe auch

[WIC Viewer GDI+-Beispiel-App](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
