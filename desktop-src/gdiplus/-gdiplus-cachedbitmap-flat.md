---
description: Windows GDI+ macht eine flache API verfügbar, die aus ca. 600 Funktionen besteht. Diese flachen API-Funktionen werden von der CachedBitmap C++-Klasse umschlossen.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: CachedBitmap-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1835cd668df90a7703a4aebdd60d37d877fe571f376d440080f5668ec3926a26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888330"
---
# <a name="cachedbitmap-functions"></a>CachedBitmap-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus ca. 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden. Die Funktionen in der GDI+-API werden von einer Sammlung von ca. 40 C++-Klassen umschlossen. Es wird empfohlen, die Funktionen in der flachen API nicht direkt auf aufruft. Wenn Sie Aufrufe von GDI+, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, der die flache API direkt aufruft. Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter GDI+ [Flat-API](-gdiplus-flatapi-flat.md).

Die folgenden flachen API-Funktionen werden von der [**CachedBitmap-C++-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) umschlossen.

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>CachedBitmap-Funktionen und entsprechende Wrappermethoden



| Flat-Funktion                                                                                                             | Wrappermethode                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap( GpBitmap \* bitmap, GpGraphics \* graphics, GpCachedBitmap \* \* cachedBitmap )   | [**CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Erstellt ein [**CachedBitmap::CachedBitmap-Objekt**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) basierend auf einem [**Bitmap-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) und einem [**Graphics-Objekt.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Die zwischengespeicherte Bitmap verwendet die Pixeldaten aus dem **Bitmap-Objekt** und speichert sie in einem Format, das für das Anzeigegerät optimiert ist, das dem **Grafikobjekt zugeordnet** ist. |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap(GpCachedBitmap \* cachedBitmap)<br/>                                      | ~CachedBitmap()                                                                                 | Bereinigt ressourcen, die von einem [**CachedBitmap-Objekt verwendet**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) werden.                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap( \* GpGraphics-Grafiken, GpCachedBitmap \* cachedBitmap, INT x, INT y )            | [**Graphics::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | Die [**Graphics::D rawCachedBitmap-Methode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) zeichnet das in einem [**CachedBitmap-Objekt gespeicherte**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) Bild.                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits( HENHMETAFILE hemf, UINT cbData16, LPBYTE pData16, INT iMapMode, INT eFlags )<br/> | [**Metafile::EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Konvertiert eine Metadatei im erweiterten Format in eine METAF-Metadatei (Windows Metafile Format) und speichert die konvertierten Datensätze in einem angegebenen Puffer.                                                                                                                                                                                                                                                                                       |



 

 

