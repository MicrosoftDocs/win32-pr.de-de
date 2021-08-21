---
description: Bild- und Bitmapobjekte speichern Bilder in einem geräteunabhängigen Format.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Verwenden einer zwischengespeicherten Bitmap zur Verbesserung der Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ffee17a2c8d564a38235cc83d204eacc9b4edf2e8070cb5971d55f1f991169f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036328"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Verwenden einer zwischengespeicherten Bitmap zur Verbesserung der Leistung

[**Bild-**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) und [**Bitmapobjekte**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) speichern Bilder in einem geräteunabhängigen Format. Ein [**CachedBitmap-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) speichert ein Bild im Format des aktuellen Anzeigegeräts. Das Rendern eines in einem **CachedBitmap-Objekt** gespeicherten Bilds ist schnell, da keine Verarbeitungszeit aufgewendet wird, um das Bild in das für das Anzeigegerät erforderliche Format zu konvertieren.

Im folgenden Beispiel werden ein [**Bitmap-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) und ein [**CachedBitmap-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) aus der Datei Texture.jpg erstellt. Bitmap  und **CachedBitmap** werden jeweils 30.000-mal gezeichnet. Wenn Sie den Code ausführen, sehen Sie, dass die **CachedBitmap-Bilder** wesentlich schneller gezeichnet werden als die **Bitmapbilder.**


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
> Ein [**CachedBitmap-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) entspricht dem Format des Anzeigegeräts zu dem Zeitpunkt, zu dem das **CachedBitmap-Objekt** erstellt wurde. Wenn der Benutzer des Programms die Anzeigeeinstellungen ändert, sollte Ihr Code ein neues **CachedBitmap-Objekt** erstellen. Die **DrawImage-Methode** schlägt fehl, wenn Sie ihr ein **CachedBitmap-Objekt** übergeben, das vor einer Änderung des Anzeigeformats erstellt wurde.

 

 

 



