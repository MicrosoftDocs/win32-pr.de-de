---
description: Windows GDI+ macht eine flache API verfügbar, die aus ca. 600 Funktionen besteht. Diese flachen API-Funktionen werden von der SolidBrush C++-Klasse umschlossen.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: SolidBrush-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0a45d36a174e765990f284d99d18a18d420745967b36cdd40d4a0ee7d1c0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014700"
---
# <a name="solidbrush-functions"></a>SolidBrush-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus ca. 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden. Die Funktionen in der GDI+-API werden von einer Sammlung von ca. 40 C++-Klassen umschlossen. Es wird empfohlen, die Funktionen in der flachen API nicht direkt auf aufruft. Wenn Sie Aufrufe von GDI+, wird empfohlen, dies durch Aufrufen der Methoden und Funktionen zu tun, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, der die flache API direkt aufruft. Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter GDI+ [Flat-API](-gdiplus-flatapi-flat.md).

Die folgenden flachen API-Funktionen werden von der [**SolidBrush C++-Klasse**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) umschlossen.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Pinselfunktionen und entsprechende Wrappermethoden



| Flat-Funktion                                                                               | Wrappermethode                                                                                       | Hinweise                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB-Farbe, GpSolidFill-Pinsel) \* \***<br/>   | [**SolidBrush::SolidBrush(IN const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Erstellt ein [**SolidBrush-Objekt**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basierend auf einer Farbe |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \* brush, ARGB color)**<br/>   | [**SolidBrush::SetColor(IN const Color& Color)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Legt die Farbe dieses Volltonpinsels fest.                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \* brush, ARGB \* color)**<br/> | [**SolidBrush::GetColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Ruft die Farbe dieses Volltonpinsels ab.                                                      |



 

 

 
