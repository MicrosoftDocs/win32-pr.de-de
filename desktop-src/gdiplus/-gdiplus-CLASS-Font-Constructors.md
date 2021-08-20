---
description: In diesem Thema werden die Konstruktoren der Font-Klasse aufgeführt. Eine vollständige Auflistung der Klassen finden Sie unter Schriftartklasse.
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Font.Font-Konstruktoren
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ff876120655adcf58318a471ed66ddfa4502d625305d9fda37f01c966e19e0cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977900"
---
# <a name="fontfont-constructors"></a>Font.Font-Konstruktoren

In diesem Thema werden die Konstruktoren der [**Font-Klasse**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) aufgeführt. Eine vollständige Klassenauflistung finden Sie unter **Schriftartklasse**.

### <a name="overload-list"></a>Überladeliste



| Konstruktor                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Font(HDC,HFONT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Erstellt indirekt [**ein Font::Font-Objekt**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) aus einer logischen GDI-Schriftart, indem ein Handle für eine GDI **LOGFONT-Struktur verwendet** wird.<br/>                                                                                                                                   |
| [**Font(HDC,LOGFONTA \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Erstellt ein [**Font::Font-Objekt**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) direkt aus einer logischen GDI-Schriftart. Die logische GDI-Schriftart ist eine **LOGFONTA-Struktur,** bei der es sich um die Ein-Byte-Zeichenversion einer logischen Schriftart handelt. Dieser Konstruktor wird zur Kompatibilität mit GDI bereitgestellt.<br/> |
| [**Font(HDC,LOGFONTW \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Erstellt ein [**Font::Font-Objekt**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) direkt aus einer logischen GDI-Schriftart. Die logische GDI-Schriftart ist eine **LOGFONTW-Struktur,** bei der es sich um die Breitzeichenversion einer logischen Schriftart handelt. Dieser Konstruktor wird zur Kompatibilität mit GDI bereitgestellt.<br/>     |
| [**Font(FontFamily \* ,REAL,INT,Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Erstellt ein [**Font::Font-Objekt**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) basierend auf einem [**FontFamily-Objekt,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) einem Schriftgrad, einem Schriftschnitt und einer Maßeinheit.<br/>                                                                               |
| [**Font(WCHAR \* ,REAL,INT,Unit,FontCollection \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Erstellt ein [**Font::Font-Objekt**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) basierend auf einer Schriftfamilie, einem Schriftgrad, einem Schriftschnitt, einer Maßeinheit und einem [**FontCollection-Objekt.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection)<br/>                                     |
| [**Font(HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Erstellt ein [**Font::Font-Objekt**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) basierend auf dem GDI-Schriftartobjekt, das derzeit in einem angegebenen Gerätekontext ausgewählt ist. Dieser Konstruktor wird zur Kompatibilität mit GDI bereitgestellt. <br/>                                                                           |



 

 
