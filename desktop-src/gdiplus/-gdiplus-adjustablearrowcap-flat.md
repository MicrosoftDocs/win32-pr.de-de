---
description: Windows GDI+ macht eine flache API verfügbar, die aus ca. 600 Funktionen besteht. Diese flachen API-Funktionen werden von der C++-Klasse "AdjustableArrowCap" umschlossen.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: AnpassbareArrowCap-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9ee90ea50c4b487ceb90e1b30f1329151533
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395075"
---
# <a name="adjustablearrowcap-functions"></a>AnpassbareArrowCap-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus ca. 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden. Die Funktionen in der flachen GDI+-API werden von einer Sammlung von ca. 40 C++-Klassen umschlossen. Es wird empfohlen, die Funktionen in der flachen API nicht direkt auf aufruft. Wenn Sie GDI+ aufrufen, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, der die flache API direkt aufruft. Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flachen API-Funktionen werden von der C++-Klasse [**"AdjustableArrowCap"**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) umschlossen.

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>AnpassbareArrowCap-Funktionen und entsprechende Wrappermethoden



| Flat-Funktion                                                                                                          | Wrappermethode                                                                                                                | Beschreibung                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateAdjustableArrowCap(REAL height, REAL width, BOOL isFilled, GpAdjustableArrowCap \* \* cap) | [**AnpassbareArrowCap::AnpassbareArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Erstellt eine anpassbare Pfeillinienobergrenze mit der angegebenen Höhe und Breite. Das Pfeillinien-Ende kann ausgefüllt oder nicht ausgefüllt werden. Die mittlere Inset-Standardeinstellung ist 0 (null).                                                                              |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapHeight(GpAdjustableArrowCap \* cap, REAL height)                           | [**AnpassbareArrowCap::SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | Die [**AnpassbareArrowCap::SetHeight-Methode**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) legt die Höhe der Pfeilobergrenze fest. Dies ist der Abstand zwischen der Basis des Pfeils und seinem Scheitelpunkt.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapHeight(GpAdjustableArrowCap \* cap, REAL \* height)                         | [**AnpassbareArrowCap::GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | Die [**AnpassbareArrowCap::GetHeight-Methode**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) ruft die Höhe der Pfeilobergrenze ab. Die Höhe ist der Abstand zwischen der Basis des Pfeils und seinem Scheitelpunkt.                                  |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapWidth(GpAdjustableArrowCap \* cap, REAL width)                             | [**AnpassbareArrowCap::SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | Die [**AnpassbareArrowCap::SetWidth-Methode**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) legt die Breite der Pfeilobergrenze fest. Die Breite ist der Abstand zwischen den Endpunkten der Basis des Pfeils.                          |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapWidth(GpAdjustableArrowCap \* cap, REAL \* width)                           | [**AnpassbareArrowCap::GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | Die [**AnpassbareArrowCap::GetWidth-Methode**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) ruft die Breite der Pfeilobergrenze ab. Die Breite ist der Abstand zwischen den Endpunkten der Basis des Pfeils.                                |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapMiddleInset(GpAdjustableArrowCap \* cap, REAL middleInset)                 | [**AnpassbareArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | Die [**AnpassbareArrowCap::SetMiddleInset-Methode**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) legt die Anzahl der Einheiten fest, die der Mittelpunkt der Basis zum Scheitelpunkt verschiebt.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapMiddleInset(GpAdjustableArrowCap \* cap, REAL \* middleInset)<br/>    | [**AnpassbareArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | Die [**AnpassbareArrowCap::GetMiddleInset-Methode**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) ruft den Wert des Einbruchs ab. Der mittlere Einsatz ist die Anzahl der Einheiten, die der Mittelpunkt der Basis zum Scheitelpunkt verschiebt. |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapFillState(GpAdjustableArrowCap \* cap, BOOL fillState)<br/>          | [**AnpassbareArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | Die [**AnpassbareArrowCap::SetFillState-Methode**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) legt den Füllzustand der Pfeilobergrenze fest. Wenn die Pfeilobergrenze nicht ausgefüllt ist, wird nur die Kontur gezeichnet.                         |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapFillState(GpAdjustableArrowCap \* cap, BOOL \* fillState)<br/>        | [**AnpassbareArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | Die [**AnpassbareArrowCap::IsFilled-Methode**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) bestimmt, ob die Pfeilobergrenze ausgefüllt ist.                                                                                               |



 

 

