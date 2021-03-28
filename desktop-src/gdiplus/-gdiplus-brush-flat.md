---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Pinsel Funktionen (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345108"
---
# <a name="brush-functions-gdi"></a>Pinsel Funktionen (GDI+)

Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind. Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt. Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, sollten Sie dies tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird. Weitere Informationen zur Verwendung dieser Wrapper Methoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flatapi-Funktionen werden von der [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++-Klasse umschließt.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Pinsel Funktionen und entsprechende Wrapper Methoden



| Flat-Funktion                                                                        | Wrapper Methode                                          | BESCHREIBUNG                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gpstatus wingdipapi gdipclonebrush (gpbrush-Pinsel \* , gpbrush \* \* cloneBrush)          | [**Pinsel:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | Die [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) -Methode erstellt ein neues [**Pinsel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekt auf Grundlage dieses Pinsels. |
| Gpstatus wingdipapi gdipdeletebrush (gpbrush-Pinsel \* )                                 | virtuelles ~ Brush ()                                        | Bereinigt die von einem [**Pinsel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekt verwendeten Ressourcen.                                                                    |
| Gpstatus wingdipapi gdipgetbrushtype (gpbrush-Pinsel \* , gpbrushtype- \* Typ)<br/> | [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | Mit der [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) -Methode wird der Typ dieses Pinsels abgerufen.                                                      |



 

 

 




