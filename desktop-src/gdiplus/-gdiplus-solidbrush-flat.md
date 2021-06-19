---
description: Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht. Diese flachen API-Funktionen werden von der SolidBrush C++-Klasse umschlossen.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: SolidBrush-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395555"
---
# <a name="solidbrush-functions"></a>SolidBrush-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden. Die Funktionen in der flachen GDI+-API werden von einer Sammlung von etwa 40 C++-Klassen umschlossen. Es wird empfohlen, die Funktionen in der flachen API nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, wird empfohlen, dies durch Aufrufen der Methoden und Funktionen zu tun, die von den C++-Wrappern bereitgestellt werden. Microsoft Product Support Services bietet keine Unterstützung für Code, der die flache API direkt aufruft. Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flachen API-Funktionen werden von der [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++-Klasse umschlossen.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Pinselfunktionen und entsprechende Wrappermethoden



| Flat-Funktion                                                                               | Wrappermethode                                                                                       | Bemerkungen                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \* \* brush)**<br/>   | [**SolidBrush::SolidBrush(IN const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Erstellt ein [**SolidBrush-Objekt**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basierend auf einer Farbe |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \* brush, ARGB color)**<br/>   | [**SolidBrush::SetColor(IN const Color& color)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Legt die Farbe dieses Volltonpinsels fest.                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill-Pinsel, \* \* ARGB-Farbe)**<br/> | [**SolidBrush::GetColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Ruft die Farbe dieses Volltonpinsels ab.                                                      |



 

 

 
