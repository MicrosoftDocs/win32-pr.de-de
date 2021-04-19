---
title: Verwenden von GDI-Funktionen mit WCS
description: Es gibt verschiedene Funktionen in der Graphics Device Interface (GDI), die Farbdaten verwenden oder verwenden.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- Windows Color System (WCS), Graphics Device Interface (GDI)
- WCS (Windows Color System), Graphics Device Interface (GDI)
- Bild Farbverwaltung, Grafikgeräte Schnittstelle (Graphics Device Interface, GDI)
- Farbverwaltung, Grafikgeräte Schnittstelle (Graphics Device Interface, GDI)
- Farben, Grafikgeräte Schnittstelle (GDI)
- Graphics Device Interface (GDI)
- GDI (Grafikgeräte Schnittstelle)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f411d5d91c36bf5d2f2fa82f332c9b15519d800d
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106362797"
---
# <a name="using-gdi-functions-with-wcs"></a>Verwenden von GDI-Funktionen mit WCS

Es gibt verschiedene Funktionen in der Graphics Device Interface (GDI), die Farbdaten verwenden oder verwenden. Einige sind für die Verwendung mit WCS und einigen nicht verfügbar. Die folgenden GDI-Funktionen sind für ICM relevant:

-   [Gerätekontext Funktionen mit WCS](#device-context-functions-with-wcs)
-   [Stift-und Pinsel Funktionen mit WCS](#pen-and-brush-functions-with-wcs)
-   [Text Ausgabefunktionen mit WCS](#text-output-functions-with-wcs)
-   [Bitmap-Funktionen mit WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Gerätekontext Funktionen mit WCS



|                    |                                                                                                                                                                                                                                 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Kreatecompatibledc" | Wenn der Gerätekontext (DC), der über seinen hdc-Parameter an diese Funktion übergeben wird, für ICM aktiviert ist, ist der von der Funktion erstellte Domänen Controller ebenfalls ICM-fähig. Die Quell-und Ziel Farbbereiche werden im DC angegeben. |
| -           | ICM kann aktiviert werden, indem der dmicmmethod-Member der DEVMODE-Struktur, auf die durch den pinitdata-Parameter gezeigt wird, auf den entsprechenden Wert festgelegt wird. Weitere Informationen finden Sie in der Dokumentation zum Platform SDK in der DEVMODE-Struktur.  |
| ResetDC            | Das Farbprofil des Geräte Kontexts, der durch den hdc-Parameter angegeben wird, wird basierend auf den Informationen in der DEVMODE-Struktur zurückgesetzt, die durch den lpinitdata-Parameter angegeben wird.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Stift-und Pinsel Funktionen mit WCS



|                 |                                                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Pinsel Funktionen | Bei der Pinsel Erstellung erfolgt keine Farbverwaltung. Die Farbverwaltung wird jedoch ausgeführt, wenn der Pinsel in einem ICM-fähigen DC ausgewählt wird. |
| "Kreatepen"       | Bei der Stift Erstellung erfolgt keine Farbverwaltung. Die Farbverwaltung wird jedoch ausgeführt, wenn der Pinsel in einem ICM-fähigen DC ausgewählt wird.   |
| Extkreatepen    | Bei der Stift Erstellung erfolgt keine Farbverwaltung. Die Farbverwaltung wird jedoch ausgeführt, wenn der Pinsel in einem ICM-fähigen DC ausgewählt wird.   |
| SelectObject    | Wenn es sich bei dem ausgewählten Objekt um einen Pinsel oder einen Stift handelt, wird die Farbverwaltung ausgeführt.                                                              |
| Setdcbrushcolor | Die Farbverwaltung wird ausgeführt, wenn WCS aktiviert ist.                                                                                              |
| Setdcpcolor   | Die Farbverwaltung wird ausgeführt, wenn WCS aktiviert ist.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Text Ausgabefunktionen mit WCS



|              |                                                  |
|--------------|--------------------------------------------------|
| SetBkColor   | Die Farbverwaltung wird ausgeführt, wenn WCS aktiviert ist. |
| SetTextColor | Die Farbverwaltung wird ausgeführt, wenn WCS aktiviert ist. |



 

## <a name="bitmap-functions-with-wcs"></a>Bitmap-Funktionen mit WCS



|                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitBLT            | Es wird keine Farbverwaltung ausgeführt, wenn Blits auftreten.                                                                                                                                                                                                                                                                                                                                                                                             |
| "Kreatedibitmap"    | Der fuusage-Parameter gibt an, dass der bmicolors-Member der BitmapInfo-Struktur, auf die durch den lpbmi-Parameter gezeigt wird, keine Farbinformationen enthält. Wenn dies nicht der Fall ist, wird für diese Bitmap keine Farbverwaltung ausgeführt. Die Bitmap muss Version 4 oder 5 der BitmapInfo-Struktur verwenden, damit die Farbverwaltung aktiviert wird. Der Inhalt der resultierenden Bitmap ist nach dem Erstellen der Bitmap nicht mit Farben übereinstimmen. |
| "Kreatedibsection"  | Wenn die BitmapInfo-Struktur, die über den pbmi-Parameter übergeben wird, nicht Version 4 oder Version 5 ist, erfolgt keine Farbverwaltung. Wenn es sich um Version 4 oder 5 handelt, ist die Farbverwaltung aktiviert, und der angegebene Farbraum wird der Bitmap zugeordnet.                                                                                                                                                                                                   |
| MaskBlt           | Es wird keine Farbverwaltung ausgeführt, wenn Blits auftreten.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Wenn es sich bei dem Objekt um eine mit "kreatedibsection" erstellte Bitmap handelt, wird die Farbverwaltung ausgeführt. Der Farbraum der Bitmap wird als Ziel Farbraum verwendet.                                                                                                                                                                                                                                                                                       |
| SetDIBits         | Die Farbverwaltung wird ausgeführt. Wenn die angegebene BitmapInfo-Struktur nicht Version 4 oder 5 ist, wird das Farbprofil des aktuellen Domänen Controllers als Quell Farb Raum Profil verwendet. Wenn keine vorhanden ist, wird der sRGB-Speicherplatz verwendet. Wenn die angegebene BitmapInfo-Struktur Version 4 oder 5 ist, wird das im Bitmap-Header angegebene Farb Raum Profil als Quell Farb Raum Profil verwendet.                                         |
| SetDIBitsToDevice | Die Farbverwaltung wird ausgeführt. Wenn die angegebene BitmapInfo-Struktur nicht Version 4 oder 5 ist, wird das Farbprofil des aktuellen Geräte Kontexts als Quell Farb Raum Profil verwendet. Wenn keine vorhanden ist, wird der sRGB-Farbraum verwendet. Wenn die angegebene BitmapInfo-Struktur Version 4 oder Version 5 ist, wird das der Bitmap zugeordnete Farb Raum Profil als Quell Farbraum verwendet.                                    |
| Setdibcolortable  | Es wird keine Farbverwaltung ausgeführt.                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | Es wird keine Farbverwaltung ausgeführt, wenn Blits auftreten.                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | Die Farbverwaltung wird ausgeführt. Wenn die angegebene BitmapInfo-Struktur nicht Version 4 oder 5 ist, wird das Farbprofil des aktuellen Domänen Controllers als Quell Farb Raum Profil verwendet. Wenn keine vorhanden ist, wird der sRGB-Speicherplatz verwendet. Wenn die angegebene BitmapInfo-Struktur Version 4 oder 5 ist, wird das im Bitmap-Header angegebene Farb Raum Profil als Quell Farb Raum Profil verwendet.                                         |



 

 

 




