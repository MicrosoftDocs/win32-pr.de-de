---
description: Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht. Diese flachen API-Funktionen werden von der Brush C++-Klasse umschlossen.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Pinselfunktionen (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395085"
---
# <a name="brush-functions-gdi"></a>Pinselfunktionen (GDI+)

Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden. Die Funktionen in der flachen GDI+-API werden von einer Sammlung von etwa 40 C++-Klassen umschlossen. Es wird empfohlen, die Funktionen in der flachen API nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Microsoft Product Support Services bietet keine Unterstützung für Code, der die flache API direkt aufruft. Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flachen API-Funktionen werden von der [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++-Klasse umschlossen.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Pinselfunktionen und entsprechende Wrappermethoden



| Flat-Funktion                                                                        | Wrappermethode                                          | Beschreibung                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush(GpBrush-Pinsel, \* GpBrush \* \* cloneBrush)          | [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | Die [**Brush::Clone-Methode**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) erstellt ein neues [**Brush-Objekt,**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) das auf diesem Pinsel basiert. |
| GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush-Pinsel) \*                                 | virtual ~Brush()                                        | Bereinigt die von einem [**Brush-Objekt**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) verwendeten Ressourcen.                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType(GpBrush-Pinsel, \* \* GpBrushType-Typ)<br/> | [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | Die [**Brush::GetType-Methode**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) ruft den Typ dieses Pinsels ab.                                                      |



 

 

 




