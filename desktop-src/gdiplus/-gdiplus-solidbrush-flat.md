---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: SolidBrush-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977545"
---
# <a name="solidbrush-functions"></a>SolidBrush-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind. Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt. Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, empfiehlt es sich, dies zu tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird. Weitere Informationen zur Verwendung dieser Wrapper Methoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flatapi-Funktionen werden von der [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++-Klasse umschließt.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Pinsel Funktionen und entsprechende Wrapper Methoden



| Flat-Funktion                                                                               | Wrapper Methode                                                                                       | Bemerkungen                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Gpstatus wingdipapi gdipkreatesolidfill (ARGB-Farbe, gpsolidfill- \* \* Pinsel)**<br/>   | [**SolidBrush:: SolidBrush (in konstanten Farben& Farbe)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Erstellt ein [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) -Objekt auf Grundlage einer Farbe. |
| **Gpstatus wingdipapi gdipsetsolidfillcolor (gpsolidfill- \* Pinsel, ARGB-Farbe)**<br/>   | [**SolidBrush:: setColor (in konstanten Farben& Farbe)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Legt die Farbe dieses Pinsel-Pinsels fest.                                                      |
| **Gpstatus wingdipapi gdipgetsolidfillcolor (gpsolidfill- \* Pinsel, ARGB- \* Farbe)**<br/> | [**SolidBrush:: GetColor (out Color \* Color) konstant**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Ruft die Farbe dieses Pinsel-Pinsels ab.                                                      |



 

 

 
