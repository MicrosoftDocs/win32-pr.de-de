---
description: Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht. Diese flachen API-Funktionen werden von der C++-Klasse CachedBitmap umschlossen.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: CachedBitmap-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce265592ad8aa10744ed124d246be69e258773f5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396196"
---
# <a name="cachedbitmap-functions"></a>CachedBitmap-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden. Die Funktionen in der flachen GDI+-API werden von einer Sammlung von etwa 40 C++-Klassen umschlossen. Es wird empfohlen, die Funktionen in der flachen API nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Microsoft Product Support Services bietet keine Unterstützung für Code, der die flache API direkt aufruft. Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flachen API-Funktionen werden von der C++-Klasse [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) umschlossen.

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>CachedBitmap-Funktionen und entsprechende Wrappermethoden



| Flat-Funktion                                                                                                             | Wrappermethode                                                                                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap( GpBitmap \* bitmap, GpGraphics \* graphics, GpCachedBitmap \* \* cachedBitmap )   | [**CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Erstellt ein [**CachedBitmap::CachedBitmap-Objekt**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) basierend auf einem [**Bitmap-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) und einem [**Graphics-Objekt.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Die zwischengespeicherte Bitmap verwendet die Pixeldaten aus dem **Bitmap-Objekt** und speichert sie in einem Format, das für das Anzeigegerät optimiert ist, das dem **Grafikobjekt** zugeordnet ist. |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap(GpCachedBitmap \* cachedBitmap)<br/>                                      | ~CachedBitmap()                                                                                 | Bereinigt ressourcen, die von einem [**CachedBitmap-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) verwendet werden.                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap( GpGraphics \* graphics, GpCachedBitmap \* cachedBitmap, INT x, INT y )            | [**Graphics::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | Die [**Graphics::D rawCachedBitmap-Methode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) zeichnet das in einem [**CachedBitmap-Objekt gespeicherte**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) Bild.                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits( HENHMETAFILE hemf, UINT cbData16, LPBYTE pData16, INT iMapMode, INT eFlags )<br/> | [**Metafile::EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Konvertiert eine Metadatei im erweiterten Format in eine WMF-Metadatei (Windows Metafile-Format) und speichert die konvertierten Datensätze in einem angegebenen Puffer.                                                                                                                                                                                                                                                                                       |



 

 

