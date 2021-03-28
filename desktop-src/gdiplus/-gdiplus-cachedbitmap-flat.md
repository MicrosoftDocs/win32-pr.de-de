---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: CachedBitmap-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ebb19648e38425561d1a1609c5f71368718ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755761"
---
# <a name="cachedbitmap-functions"></a>CachedBitmap-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind. Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt. Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, sollten Sie dies tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird. Weitere Informationen zur Verwendung dieser Wrapper Methoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flatapi-Funktionen werden von der [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) C++-Klasse umschließt.

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>CachedBitmap-Funktionen und entsprechende Wrapper Methoden



| Flat-Funktion                                                                                                             | Wrapper Methode                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gpstatus wingdipapi gdipkreatecachedbitmap (gpbitmap- \* Bitmap, gpgrafik \* Grafiken, gpcachedbitmap \* \* CachedBitmap)   | [**CachedBitmap:: CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Erstellt ein [**CachedBitmap:: CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) -Objekt, das auf einem [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt und einem [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt basiert. Die zwischengespeicherte Bitmap übernimmt die Pixeldaten aus dem **Bitmap** -Objekt und speichert Sie in einem Format, das für das Anzeigegerät optimiert ist, das dem **Grafik** Objekt zugeordnet ist. |
| Gpstatus wingdipapi gdipdeletecachedbitmap (gpcachedbitmap \* CachedBitmap)<br/>                                      | ~ CachedBitmap ()                                                                                 | Bereinigt Ressourcen, die von einem [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) -Objekt verwendet werden.                                                                                                                                                                                                                                                                                                                                |
| Gpstatus wingdipapi gdipdrawcachedbitmap (gpgraphics- \* Grafiken, gpcachedbitmap \* CachedBitmap, int x, int y)            | [**Grafiken::D rawcachedbitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | Die [**Grafik::D rawcachedbitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) -Methode zeichnet das Bild, das in einem [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) -Objekt gespeichert ist.                                                                                                                                                                                                                                |
| Uint wingdipapi gdipemstowmlbits (HENHMETAFILE hemf, uint cbData16, LPBYTE pData16, int imapmode, int EFLAGS)<br/> | [**Metafile:: emltowmf**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Konvertiert eine Metadatei mit erweitertem Format in eine Windows Metafile-Format (WMF)-Metadatei und speichert die konvertierten Datensätze in einem angegebenen Puffer.                                                                                                                                                                                                                                                                                       |



 

 

