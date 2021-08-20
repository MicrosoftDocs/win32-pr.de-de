---
title: Suchen und Öffnen von Ausstellern und Dekomprimierern
description: Suchen und Öffnen von Ausstellern und Dekomprimierern
ms.assetid: ed931f01-dbfc-4fdc-b725-c062302b037b
keywords:
- Videokomprimierungs-Manager (VCM), Öffnen von Klappen
- VCM (Videokomprimierungs-Manager),Öffnen von Klappen
- ICLocate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c861c9fb5c317b6b0fc3a48552db200389739ebd8a53dbf15fbdbd0564ba8f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139301"
---
# <a name="locating-and-opening-compressors-and-decompressors"></a>Suchen und Öffnen von Ausstellern und Dekomprimierern

Im folgenden Beispiel wird die [**ICLocate-Funktion**](/windows/desktop/api/Vfw/nf-vfw-iclocate) verwendet, um eine 8-Bit-Pro-Pixel-Bitmap zu komprimieren.


```C++
BITMAPINFOHEADER bih; 
HIC              hIC 
 
// Initialize the bitmap structure. 
bih.biSize = sizeof(BITMAPINFOHEADER); 
bih.biWidth = bih.biHeight = 0; 
bih.biPlanes = 1; 
bih.biCompression = BI_RGB;      // standard RGB bitmap 
bih.biBitcount = 8;              // 8 bits-per-pixel format 
bih.biSizeImage = 0; 
bih.biXPelsPerMeter = bih.biYPelsPerMeter = 0; 
bih.biClrUsed = bih.biClrImportant = 256; 
 
hIC = ICLocate (ICTYPE_VIDEO, 0L, (LPBITMAPINFOHEADER) &bih, 
    NULL, ICMODE_COMPRESS); 
 
```



Im folgenden Beispiel werden die Dekomprimierer im System aufzählt, um einen zu finden, der das Format seiner Bilder verarbeiten kann. In diesem Beispiel werden **ICTYPE \_ VIDEO** (entspricht dem vierstelligen "VIDC"-Code) und das [**ICDecompressQuery-Makro**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) verwendet, um zu bestimmen, ob ein Strich oder Dekomprimierer das Bildformat unterstützt.


```C++
for (i=0; ICInfo(fccType, i, &icinfo); i++) 
{ 
    hic = ICOpen(icinfo.fccType, icinfo.fccHandler, ICMODE_QUERY); 
    if (hic) 
    { 
        // Skip this compressor if it can't handle the format. 
        if (fccType == ICTYPE_VIDEO && pvIn != NULL && 
            ICDecompressQuery(hic, pvIn, NULL) != ICERR_OK) 
        { 
            ICClose(hic); 
            continue; 
        } 
 
        // Find out the compressor name. 
        ICGetInfo(hic, &icinfo, sizeof(icinfo)); 
 
        // Add it to the combo box. 
        n = ComboBox_AddString(hwndC,icinfo.szDescription); 
        ComboBox_SetItemData(hwndC, n, hic); 
    } 
} 
 
```



Im folgenden Beispiel wird versucht, eine bestimmte Komprimierung zu finden, um das 8-Bit-RGB-Format in ein 8-Bit-RLE-Format zu komprimieren.


```C++
BITMAPINFOHEADER    bihIn, bihOut; 
HIC                 hIC 
 
// Initialize the bitmap structure. 

biSize = bihOut.biSize = sizeof(BITMAPINFOHEADER); 
bihIn.biWidth = bihIn.biHeight = bihOut.biWidth = bihOut.biHeight = 0; 
bihIn.biPlanes = bihOut.biPlanes= 1; 
bihIn.biCompression = BI_RGB;        // standard RGB bitmap for input 
bihOut.biCompression = BI_RLE8;      // 8-bit RLE for output format 
bihIn.biBitcount = bihOut.biBitCount = 8;  // 8 bits-per-pixel format 
bihIn.biSizeImage = bihOut.biSizeImage = 0; 
bihIn.biXPelsPerMeter = bih.biYPelsPerMeter = 
    bihOut.biXPelsPerMeter = bihOut.biYPelsPerMeter = 0; 
bihIn.biClrUsed = bih.biClrImportant = 
    bihOut.biClrUsed = bihOut.biClrImportant = 256; 

hIC = ICLocate (ICTYPE_VIDEO, 0L, 
    (LPBITMAPINFOHEADER)&bihIn, 
    (LPBITMAPINFOHEADER)&bihOut, ICMODE_COMPRESS); 
 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Videokomprimierungs-Managers](using-the-video-compression-manager.md)
</dt> </dl>

 

 




