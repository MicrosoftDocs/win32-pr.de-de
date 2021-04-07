---
title: Interoperabilität mit GDI
description: DirectWrite bietet einen Migrationspfad von und einige Interoperabilität mit, dem GDI-Schriftart Modell sowie Schnittstellen zum Rendern von Text in eine Bitmap, die dann in einem Fenster gezeichnet werden kann.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite, GDI-Interoperation
- DirectWrite, Interoperabilität
- Interoperabilität
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039032"
---
# <a name="interoperating-with-gdi"></a>Interoperabilität mit GDI

[DirectWrite](direct-write-portal.md) bietet einen Migrationspfad von und einige Interoperabilität mit, dem GDI-Schriftart Modell sowie Schnittstellen zum Rendern von Text in eine Bitmap, die dann in einem Fenster gezeichnet werden kann.

Diese Übersicht enthält die folgenden Teile:

-   [Introduction (Einführung)](#introduction)
-   [Teil 1: idschreitegdiinterop](#part-1-idwritegdiinterop)
-   [Teil 2: Schriftart Objekte](#part-2-font-objects)
-   [Teil 3: Rendering](#part-3-rendering)

## <a name="introduction"></a>Einführung

[DirectWrite](direct-write-portal.md) bietet Methoden für die Typumwandlung zwischen der GDI-LOGFONT-Struktur und den DirectWrite-Schriftart Schnittstellen. Dies ermöglicht es Ihnen, GDI für einige oder alle der Schriftart Enumeration und-Auswahl zu verwenden, während gleichzeitig die verbesserte Funktionalität und Leistung von DirectWrite genutzt wird. DirectWrite verfügt auch über Schnittstellen zum Rendern in eine Bitmap, wenn Sie Text auf einer GDI-Oberfläche anzeigen möchten.

## <a name="part-1-idwritegdiinterop"></a>Teil 1: idschreitegdiinterop

Die [**idschreitegdiinterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) -Schnittstelle wird verwendet, um zwischen GDI-Schriftart Strukturen und [DirectWrite](direct-write-portal.md) -Schriftart Schnittstellen zu konvertieren und ein [**idwrite-bitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Objekt zu erstellen. Zum Aufrufen eines **idschreitegdiinterop** -Objekts verwenden Sie die [**idschreitefactory:: getgdiinterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) -Methode, wie im folgenden Code gezeigt.


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a>Teil 2: Schriftart Objekte

GDI verwendet die LogFont-Struktur zum Speichern von Informationen über die Schriftart und den Text Stil. Die [**idwrite-gdiinterop:: kreatefontfromlogfont**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) -Methode konvertiert eine LOGFONT-Struktur in ein [**idschreitefont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) -Objekt, wie im folgenden Code gezeigt.


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



Allerdings werden von [**idwrite-Font**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) nicht alle Informationen in einer LogFont-Datei eingeschlossen. Eine LOGFONT-Struktur enthält die Schriftgröße, die Gewichtung, den Stil, die Unterstreichung, das stricken, den Namen der Schriftart und einige andere Informationen. **Idwrite-Font** -Objekte enthalten Informationen zu einer Schriftart und ihrer Gewichtung und Art, aber nicht zur Schriftart Größe, Unterstreichung usw. Mit [DirectWrite](direct-write-portal.md)werden Formatierungs Informationselemente wie diese durch ein [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt oder für bestimmte Textbereiche ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt gekapselt.

Sie haben die Möglichkeit, [**idschreibschriftart**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) mithilfe von [**idschreitegdiinterop:: convertfonttologfont**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)in eine LogFont-Datei zu konvertieren.

## <a name="part-3-rendering"></a>Teil 3: Rendering

Um DirectWrite-Text auf einer GDI-Oberfläche zu Renderen, verwenden Sie einen benutzerdefinierten TextRenderer. Weitere Informationen finden Sie im Thema [Rendering zu einer GDI-Oberfläche](render-to-a-gdi-surface.md) .

 

 