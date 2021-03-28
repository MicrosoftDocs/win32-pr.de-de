---
description: Image-und Bitmap-Objekte speichern Bilder in einem geräteunabhängigen Format.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Verwenden einer zwischengespeicherten Bitmap zum Verbessern der Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8e546460741342bcac8f1633e21d104984af9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994174"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Verwenden einer zwischengespeicherten Bitmap zum Verbessern der Leistung

[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -und [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekte speichern Bilder in einem geräteunabhängigen Format. Ein [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) -Objekt speichert ein Bild im Format des aktuellen Anzeige Geräts. Das Rendern eines in einem **CachedBitmap** -Objekt gespeicherten Bilds ist schnell, da keine Verarbeitungszeit aufgewendet wird, um das Abbild in das vom Anzeigegerät benötigte Format zu wandeln.

Im folgenden Beispiel werden ein [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt und ein [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) -Objekt aus dem Datei Texture.jpg erstellt. Die **Bitmap** und die **CachedBitmap** werden jeweils 30.000-Mal gezeichnet. Wenn Sie den Code ausführen, werden Sie feststellen, dass die **CachedBitmap** -Bilder wesentlich schneller gezeichnet werden als die **Bitmap** -Bilder.


```
Bitmap        bitmap(L"Texture.jpg");
UINT          width = bitmap.GetWidth();
UINT          height = bitmap.GetHeight();
CachedBitmap  cBitmap(&bitmap, &graphics);
int           j, k;
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
     graphics.DrawImage(&bitmap, j, j / 2, width, height);
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
      graphics.DrawCachedBitmap(&cBitmap, j, 150 + j / 2 );
```



> [!Note]  
> Ein [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) -Objekt entspricht dem Format des Anzeige Geräts zu dem Zeitpunkt, zu dem das **CachedBitmap** -Objekt erstellt wurde. Wenn der Benutzer des Programms die Anzeigeeinstellungen ändert, sollte der Code ein neues **CachedBitmap** -Objekt erstellen. Bei der **DrawImage** -Methode tritt ein Fehler auf, wenn Sie ein **CachedBitmap** -Objekt übergeben, das vor einer Änderung im Anzeige Format erstellt wurde.

 

 

 



