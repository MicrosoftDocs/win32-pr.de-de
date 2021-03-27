---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: AdjustableArrowCap-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d377b319169a2a10c864db5aec402fe633beb3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994463"
---
# <a name="adjustablearrowcap-functions"></a>AdjustableArrowCap-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind. Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt. Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, sollten Sie dies tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird. Weitere Informationen zur Verwendung dieser Wrapper Methoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flatapi-Funktionen werden von der Klasse " [**AdjustableArrowCap**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) C++" umschließt.

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>"AdjustableArrowCap"-Funktionen und entsprechende Wrapper Methoden



| Flat-Funktion                                                                                                          | Wrapper Methode                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gpstatus wingdipapi gdipkreateadjustablearrowcap (Real Height, Real Width, bool isfill, gpadjustablearrowcap \* \* Cap) | [**AdjustableArrowCap:: AdjustableArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Erstellt eine anpassbare Pfeil Linien Abdeckung mit der angegebenen Höhe und Breite. Das Pfeil Zeilenende kann ausgefüllt oder nicht ausgefüllt werden. Die mittlere inmenge ist standardmäßig 0 (null).                                                                              |
| Gpstatus wingdipapi gdipsetadjustablearrowcapheight (gpadjustablearrowcap- \* Cap, Real Height)                           | [**AdjustableArrowCap::**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | Die Methode " [**AdjustableArrowCap:: SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) " legt die Höhe des Pfeil Endes fest. Dies ist der Abstand zwischen der Basis des Pfeils und dem Scheitelpunkt.                                 |
| Gpstatus wingdipapi gdipgetadjustablearrowcapheight (gpadjustablearrowcap- \* Cap, Real \* Height)                         | [**AdjustableArrowCap:: GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | Die Methode " [**AdjustableArrowCap:: GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) " Ruft die Höhe der Pfeil Abdeckung ab. Die Höhe entspricht der Entfernung von der Basis des Pfeils zum Scheitelpunkt.                                  |
| Gpstatus wingdipapi gdipsetadjustablearrowcapwidth (gpadjustablearrowcap- \* Cap, echte Breite)                             | [**AdjustableArrowCap::-Sitzungsart**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | Mit der Methode " [**AdjustableArrowCap:: SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) " wird die Breite der Pfeil Abdeckung festgelegt. Die Breite ist der Abstand zwischen den Endpunkten der Basis des Pfeils.                          |
| Gpstatus wingdipapi gdipgetadjustablearrowcapwidth (gpadjustablearrowcap- \* Cap, echte \* Breite)                           | [**AdjustableArrowCap:: getWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | Die Methode " [**AdjustableArrowCap:: getWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) " Ruft die Breite des Pfeil Endes ab. Die Breite ist der Abstand zwischen den Endpunkten der Basis des Pfeils.                                |
| Gpstatus wingdipapi gdipsetadjustablearrowcapmiddleinset (gpadjustablearrowcap \* Cap, Real MiddleInset)                 | [**AdjustableArrowCap:: setmiddleinset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | Mit der Methode " [**AdjustableArrowCap:: setmiddleinset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) " wird die Anzahl der Einheiten festgelegt, die der Mittelpunkt der Basis auf den Scheitelpunkt verschiebt.                                 |
| Gpstatus wingdipapi gdipgetadjustablearrowcapmiddleinset (gpadjustablearrowcap \* Cap, Real \* MiddleInset)<br/>    | [**AdjustableArrowCap:: getmiddleinset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | Die Methode " [**AdjustableArrowCap:: getmiddleinset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) " Ruft den Wert des insets ab. Die mittlere inmenge ist die Anzahl der Einheiten, die der Mittelpunkt der Basis auf den Scheitelpunkt verlagert. |
| Gpstatus wingdipapi gdipsetadjustablearrowcapfillstate (gpadjustablearrowcap \* Cap, bool fillstate)<br/>          | [**AdjustableArrowCap:: setfillstate**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | Die Methode " [**AdjustableArrowCap:: setfillstate**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) " legt den Füll Zustand der Pfeil Abdeckung fest. Wenn das Pfeil Limit nicht aufgefüllt ist, wird nur die Gliederung gezeichnet.                         |
| Gpstatus wingdipapi gdipgetadjustablearrowcapfillstate (gpadjustablearrowcap \* Cap, bool \* fillstate)<br/>        | [**AdjustableArrowCap:: isfill**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | Die Methode " [**AdjustableArrowCap:: isfill**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) " bestimmt, ob die Pfeil Abdeckung ausgefüllt ist.                                                                                               |



 

 

