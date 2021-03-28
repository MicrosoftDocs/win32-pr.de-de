---
description: In diesem Thema werden die Konstruktoren der Font-Klasse aufgelistet. Eine komplette Klassen Auflistung finden Sie unter Font-Klasse.
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Font. Font-Konstruktoren
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: bdf533e292734956c02d3f8a424ca619cb722c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218245"
---
# <a name="fontfont-constructors"></a>Font. Font-Konstruktoren

In diesem Thema werden die Konstruktoren der [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) -Klasse aufgelistet. Eine komplette Klassen Auflistung finden Sie unter **Font-Klasse**.

### <a name="overload-list"></a>Überladeliste



| Konstruktor                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schriftart (hdc, hFont)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Erstellt ein [**Schriftart:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) -Objekt indirekt aus einer logischen GDI-Schriftart mithilfe eines Handles für eine GDI- **LOGFONT** -Struktur.<br/>                                                                                                                                   |
| [**Schriftart (hdc, logfonta \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Erstellt ein [**Schriftart:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) -Objekt direkt aus einer logischen GDI-Schriftart. Die logische GDI-Schriftart ist eine **logfonta** -Struktur, bei der es sich um die 1-Byte-Zeichen Version einer logischen Schriftart handelt. Dieser Konstruktor wird für die Kompatibilität mit GDI bereitgestellt.<br/> |
| [**Schriftart (hdc, logfontw \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Erstellt ein [**Schriftart:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) -Objekt direkt aus einer logischen GDI-Schriftart. Die logische GDI-Schriftart ist eine **logfontw** -Struktur, die die breit Zeichen Version einer logischen Schriftart ist. Dieser Konstruktor wird für die Kompatibilität mit GDI bereitgestellt.<br/>     |
| [**Font (FontFamily \* , Real, int, Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Erstellt ein [**Schriftart:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) -Objekt auf Grundlage eines [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekts, einer Größe, eines Schrift Stils und einer Maßeinheit.<br/>                                                                               |
| [**Schriftart (WChar \* , Real, int, Unit, FontCollection \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Erstellt ein [**Schriftart:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) -Objekt auf Grundlage einer Schriftfamilie, einer Größe, eines Schrift Stils, einer Maßeinheit und eines [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) -Objekts.<br/>                                     |
| [**Schriftart (HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Erstellt ein [**Schriftart:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) -Objekt, das auf dem GDI-Schriftart Objekt basiert, das momentan in einem angegebenen Gerätekontext ausgewählt ist. Dieser Konstruktor wird für die Kompatibilität mit GDI bereitgestellt. <br/>                                                                           |



 

 
