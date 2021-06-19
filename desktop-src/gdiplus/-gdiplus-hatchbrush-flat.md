---
description: Windows GDI+ macht eine flache API verfügbar, die aus ca. 600 Funktionen besteht. Diese flachen API-Funktionen werden von der HatchBrush C++-Klasse umschlossen.
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: HatchBrush-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa455c1194ca4f3397673d1a4412dc9ed7e3473
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395265"
---
# <a name="hatchbrush-functions"></a>HatchBrush-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus ca. 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden. Die Funktionen in der flachen GDI+-API werden von einer Sammlung von ca. 40 C++-Klassen umschlossen. Es wird empfohlen, die Funktionen in der flachen API nicht direkt auf aufruft. Wenn Sie GDI+ aufrufen, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, der die flache API direkt aufruft. Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flachen API-Funktionen werden von der [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) C++-Klasse umschlossen.

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>HatchBrush-Funktionen und entsprechende Wrappermethoden



| Flat-Funktion                                                                                                               | Wrappermethode                                                                                                                                                                                   | Bemerkungen                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateHatchBrush(GpHatchStyle hatchstyle, ARGB forecol, ARGB backcol, GpHatch \* \* brush)<br/> | [**HatchBrush::HatchBrush(IN HatchStyle hatchStyle, IN const Color& foreColor, IN const Color& backColor = Color())**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | Erstellt ein [**HatchBrush-Objekt**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) basierend auf einem Schraffurstil, einer Vordergrundfarbe und einer Hintergrundfarbe. |
| GpStatus WINGDIPAPI GdipGetHatchStyle(GpHatch \* brush, GpHatchStyle \* hatchstyle)<br/>                                | [**HatchStyle HatchBrush::GetHatchStyle() const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | Ruft den Schraffurstil dieses Schraffurpinsels ab.                                                                                                  |
| GpStatus WINGDIPAPI GdipGetHatchForegroundColor(GpHatch \* brush, ARGB \* forecol)<br/>                                 | [**Status HatchBrush::GetForegroundColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | Ruft die Vordergrundfarbe dieses Schraffraffierpinsels ab.                                                                                             |
| GpStatus WINGDIPAPI GdipGetHatchBackgroundColor(GpHatch \* brush, ARGB \* backcol)<br/>                                 | [**Status HatchBrush::GetBackgroundColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | Ruft die Hintergrundfarbe dieses Schraffraffenpinsels ab.                                                                                             |



 

 

 
