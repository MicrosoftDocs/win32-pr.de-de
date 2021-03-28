---
description: Wenn Sie ein Rasterbild (Bitmap) auf dem Bildschirm anzeigen möchten, benötigen Sie ein Bild Objekt und ein Grafik Objekt.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Laden und Anzeigen von Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "104982844"
---
# <a name="loading-and-displaying-bitmaps"></a>Laden und Anzeigen von Bitmaps

Weitere Informationen finden Sie auch in der [WIC-Viewer-Beispiel-App](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).

Wenn Sie ein Rasterbild (Bitmap) auf dem Bildschirm anzeigen möchten, benötigen Sie ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt und ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt. Übergeben Sie den Namen einer Datei (oder eines Zeigers an einen Stream) an einen **bildkonstruktor** . Nachdem Sie ein **Image** -Objekt erstellt haben, übergeben Sie die Adresse dieses **Bild** Objekts an die **DrawImage** -Methode eines **Grafik** Objekts.

Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus einer JPEG-Datei erstellt, und anschließend wird das Bild mit der linken oberen Ecke bei (60, 10) gezeichnet:

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

Die folgende Abbildung zeigt das an der angegebenen Position gezeichnete Bild.

![Screenshot eines Fensters, das ein Bild enthält, mit einer Legende für den Ursprungs Punkt ](images/imageposition1.png)

Die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse stellt grundlegende Methoden zum Laden und Anzeigen von Rasterbildern und Vektorbildern bereit. Die [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klasse, die von der **Image** -Klasse erbt, bietet speziellere Methoden zum Laden, anzeigen und Bearbeiten von Rasterbildern. Beispielsweise können Sie ein **Bitmap** -Objekt aus einem Symbol Handle (HICON) erstellen.

Im folgenden Beispiel wird ein Handle für ein Symbol abgerufen, und anschließend wird dieses Handle zum Erstellen eines [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekts verwendet. Im Code wird das Symbol angezeigt, indem die Adresse des **Bitmap** -Objekts an die **DrawImage** -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts übergeben wird.

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a>Weitere Informationen

[WIC-Viewer-GDI+-Beispiel-App](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
