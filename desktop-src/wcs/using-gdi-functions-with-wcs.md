---
title: Verwenden von GDI-Funktionen mit WCS
description: Es gibt verschiedene Funktionen in der Grafischen Geräteschnittstelle (GDI), die Farbdaten verwenden oder verarbeiten.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- Windows Color System (WCS), Grafikgeräteschnittstelle (GDI)
- WCS (Windows Color System), Grafikgeräteschnittstelle (GDI)
- Bildfarbverwaltung, Grafische Geräteschnittstelle (GDI)
- Farbverwaltung, Grafische Geräteschnittstelle (GDI)
- Farben, Grafische Geräteschnittstelle (GDI)
- Grafikgeräteschnittstelle (GDI)
- GDI (Grafikgeräteschnittstelle)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a104378ae46e6b9519d6f795d280d45c28c8fa3fdc7d1e34aae609bcdbd195d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444677"
---
# <a name="using-gdi-functions-with-wcs"></a>Verwenden von GDI-Funktionen mit WCS

Es gibt verschiedene Funktionen in der Grafischen Geräteschnittstelle (GDI), die Farbdaten verwenden oder verarbeiten. Einige sind für die Verwendung mit WCS aktiviert, andere nicht. Die folgenden GDI-Funktionen sind für ICM relevant:

-   [Gerätekontextfunktionen mit WCS](#device-context-functions-with-wcs)
-   [Stift- und Pinselfunktionen mit WCS](#pen-and-brush-functions-with-wcs)
-   [Textausgabefunktionen mit WCS](#text-output-functions-with-wcs)
-   [Bitmapfunktionen mit WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Gerätekontextfunktionen mit WCS



|    Funktion                |   BESCHREIBUNG                                                                                                                                                                                                                              |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateCompatibleDC | Wenn der Gerätekontext (DC), der über den hdc-Parameter an diese Funktion übergeben wird, für ICM aktiviert ist, ist der dc, den die Funktion erstellt, ebenfalls ICM aktiviert. Die Quell- und Zielfarbräume werden im DC angegeben. |
| CreateDC           | ICM können aktiviert werden, indem Sie den dmICMMethod-Member der DEVMODE-Struktur, auf den der pInitData-Parameter zeigt, auf den entsprechenden Wert festlegen. Weitere Informationen finden Sie in der Dokumentation im Plattform-SDK zur DEVMODE-Struktur.  |
| ResetDC            | Das Farbprofil des vom hdc-Parameter angegebenen Gerätekontexts wird basierend auf den Informationen in der DEVMODE-Struktur zurückgesetzt, die durch den lpInitData-Parameter angegeben wird.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Stift- und Pinselfunktionen mit WCS



|    Funktion                |   BESCHREIBUNG                                                                                                                                                                                                                              |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Pinselfunktionen | Bei der Pinselerstellung erfolgt keine Farbverwaltung. Die Farbverwaltung wird jedoch durchgeführt, wenn der Pinsel in einem ICM aktivierten DC ausgewählt wird. |
| CreatePen       | Bei der Stifterstellung erfolgt keine Farbverwaltung. Die Farbverwaltung wird jedoch durchgeführt, wenn der Pinsel in einem ICM aktivierten DC ausgewählt wird.   |
| ExtCreatePen    | Bei der Stifterstellung erfolgt keine Farbverwaltung. Die Farbverwaltung wird jedoch durchgeführt, wenn der Pinsel in einem ICM aktivierten DC ausgewählt wird.   |
| SelectObject    | Wenn das ausgewählte Objekt ein Pinsel oder Stift ist, wird die Farbverwaltung durchgeführt.                                                              |
| SetDCBrushColor | Die Farbverwaltung wird ausgeführt, wenn WCS aktiviert ist.                                                                                              |
| SetDCPenColor   | Die Farbverwaltung wird ausgeführt, wenn WCS aktiviert ist.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Textausgabefunktionen mit WCS



|    Funktion                |   BESCHREIBUNG                                                                                                                                                                                                                              |
|--------------|--------------------------------------------------|
| SetBkColor   | Die Farbverwaltung wird ausgeführt, wenn WCS aktiviert ist. |
| SetTextColor | Die Farbverwaltung wird ausgeführt, wenn WCS aktiviert ist. |



 

## <a name="bitmap-functions-with-wcs"></a>Bitmapfunktionen mit WCS



|    Funktion                |   BESCHREIBUNG                                                                                                                                                                                                                              |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitblt            | Wenn Blits auftreten, wird keine Farbverwaltung durchgeführt.                                                                                                                                                                                                                                                                                                                                                                                             |
| CreateDIBitmap    | Der fuUsage-Parameter gibt an, dass der bmiColors-Member der BITMAPINFO-Struktur, auf die der lpbmi-Parameter zeigt, Farbinformationen enthält oder nicht. Wenn dies nicht dere ist, wird keine Farbverwaltung für diese Bitmap ausgeführt. Die Bitmap muss Version 4 oder Version 5 der BITMAPINFO-Struktur verwenden, damit die Farbverwaltung aktiviert wird. Der Inhalt der resultierenden Bitmap ist nach dem Erstellen der Bitmap nicht farbgleich. |
| CreateDIBSection  | Wenn die bitmapinfo-Struktur, die über den pbmi-Parameter übergeben wird, nicht Version 4 oder Version 5 ist, erfolgt keine Farbverwaltung. Wenn es sich um Version 4 oder 5 handelt, ist die Farbverwaltung aktiviert, und der angegebene Farbraum wird der Bitmap zugeordnet.                                                                                                                                                                                                   |
| MaskBlt           | Wenn Blits auftreten, wird keine Farbverwaltung durchgeführt.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Wenn es sich bei dem Objekt um eine Bitmap handelt, die mit CreateDIBSection erstellt wurde, wird die Farbverwaltung durchgeführt. Der Farbraum der Bitmap wird als Zielfarbraum verwendet.                                                                                                                                                                                                                                                                                       |
| SetDIBits         | Die Farbverwaltung wird ausgeführt. Wenn die angegebene BITMAPINFO-Struktur nicht Version 4 oder Version 5 ist, wird das Farbprofil des aktuellen Domänencontrollers als Quellfarbraumprofil verwendet. Wenn es keins besitzt, wird der sRGB-Speicherplatz verwendet. Wenn die angegebene BITMAPINFO-Struktur Version 4 oder Version 5 ist, wird das im Bitmapheader angegebene Farbraumprofil als Quellfarbraumprofil verwendet.                                         |
| SetDIBitsToDevice | Die Farbverwaltung wird ausgeführt. Wenn die angegebene BITMAPINFO-Struktur nicht Version 4 oder Version 5 ist, wird das Farbprofil des aktuellen Gerätekontexts als Quellfarbraumprofil verwendet. Wenn kein Farbraum verwendet wird, wird der sRGB-Farbraum verwendet. Wenn die angegebene BITMAPINFO-Struktur Version 4 oder Version 5 ist, wird das der Bitmap zugeordnete Farbraumprofil als Quellfarbraum verwendet.                                    |
| SetDIBColorTable  | Es wird keine Farbverwaltung durchgeführt.                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | Wenn Blits auftreten, wird keine Farbverwaltung durchgeführt.                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | Die Farbverwaltung wird ausgeführt. Wenn die angegebene BITMAPINFO-Struktur nicht Version 4 oder Version 5 ist, wird das Farbprofil des aktuellen Domänencontrollers als Quellfarbraumprofil verwendet. Wenn es keins besitzt, wird der sRGB-Speicherplatz verwendet. Wenn die angegebene BITMAPINFO-Struktur Version 4 oder Version 5 ist, wird das im Bitmapheader angegebene Farbraumprofil als Quellfarbraumprofil verwendet.                                         |



 

 

 




