---
description: Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht. Diese flachen API-Funktionen werden von der C++-Klasse GdiplusBase umschlossen.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Arbeitsspeicherfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395825"
---
# <a name="memory-functions"></a>Arbeitsspeicherfunktionen

Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden. Die Funktionen in der flachen GDI+-API werden von einer Sammlung von etwa 40 C++-Klassen umschlossen. Es wird empfohlen, die Funktionen in der flachen API nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Microsoft Product Support Services bietet keine Unterstützung für Code, der die flache API direkt aufruft. Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flachen API-Funktionen werden von der C++-Klasse [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) umschlossen.

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Speicherfunktionen und entsprechende Wrappermethoden



| Flat-Funktion                                          | Wrappermethode                                                                                                                                      | Bemerkungen                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc(size \_ t size)<br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (operator new)(size \_ t in \_ size)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Belegt Arbeitsspeicher für ein Windows GDI+-Objekt. <br/> GdipAlloc wird in GdiplusMem.h deklariert.<br/>  |
| GpStatus WINGDIPAPI GdipFree(void \* ptr);<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void \* in \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Hebt die Speicherbeteilung für ein Windows GDI+-Objekt auf. <br/> GdipFree wird in GdiplusMem.h deklariert.<br/> |



 

 

 
