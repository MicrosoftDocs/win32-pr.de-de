---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: HatchBrush-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d444fea500ce1e56e4c59420b913d5ff6cee965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994222"
---
# <a name="hatchbrush-functions"></a>HatchBrush-Funktionen

Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind. Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt. Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, sollten Sie dies tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird. Weitere Informationen zur Verwendung dieser Wrapper Methoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Die folgenden flatapi-Funktionen werden von der [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) C++-Klasse umschließt.

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>HatchBrush-Funktionen und entsprechende Wrapper Methoden



| Flat-Funktion                                                                                                               | Wrapper Methode                                                                                                                                                                                   | Bemerkungen                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Gpstatus wingdipapi gdipkreatehatchbrush (gphatchstyle HatchStyle, ARGB forecol, ARGB backcol, gphatch \* \* Brush)<br/> | [**HatchBrush:: HatchBrush (in HatchStyle HatchStyle, in Konstante Farbe& ForeColor, in Konstante Farbe& BackColor = Color ())**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | Erstellt ein [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) -Objekt auf Grundlage einer Schraffurart, einer Vordergrundfarbe und einer Hintergrundfarbe. |
| Gpstatus wingdipapi gdipgethatchstyle (gphatch- \* Pinsel, gphatchstyle \* HatchStyle)<br/>                                | [**HatchStyle HatchBrush:: gethatchstyle () Konstanten**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | Ruft die Schraffurart dieses schraffurpinsels ab.                                                                                                  |
| Gpstatus wingdipapi gdipgethatchforegroundcolor (gphatch- \* Pinsel, ARGB \* forecol)<br/>                                 | [**Status HatchBrush:: getforegroundcolor (Farbe der out-Farbe \* )**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | Ruft die Vordergrundfarbe dieses schraffurpinsels ab.                                                                                             |
| Gpstatus wingdipapi gdipgethatchbackgroundcolor (gphatch \* Pinsel, ARGB \* backcol)<br/>                                 | [**Status HatchBrush:: getbackgroundcolor (Farbe der out-Farbe \* )**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | Ruft die Hintergrundfarbe dieses schraffurpinsels ab.                                                                                             |



 

 

 
