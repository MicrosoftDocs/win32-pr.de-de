---
title: Geräterkalibrierung und Charakterisierungsfunktionen
description: Die folgenden Funktionen sind nützlich für das Schreiben von Tools zur Gerätekalibrierung und -färbung, die zum Installieren und Kalibrieren von Farbanzeigegeräten wie Monitoren und Druckern erforderlich sind.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bildfarbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCS,Functions
- Windows Farbsystem (WCS), Gerätekalibrierung
- WCS (Windows Color System), Gerätekalibrierung
- Bildfarbverwaltung, Gerätekalibrierung
- Farbverwaltung, Gerätekalibrierung
- Farben, Gerätekalibrierung
- WCS-Referenz, Gerätekalibrierung
- Referenz für WCS, Gerätekalibrierung
- Windows Farbsystem (WCS),konsistent
- WCS (Windows Color System)
- Bildfarbverwaltung,beschreibung
- Farbverwaltung, Verwaltung
- farben, colors
- WCS-Referenz
- Referenz für WCS, über die
- Kalibrierung von Geräten
- Kalibrierung
- Charakterisierung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aea24f0a1e033df62c70674c44c9b5e9c6c0e0de1011b9ea95b9e5389d6004c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452026"
---
# <a name="device-calibration-and-characterization-functions"></a>Geräterkalibrierung und Charakterisierungsfunktionen

Die folgenden Funktionen sind nützlich für das Schreiben von Tools zur Gerätekalibrierung und -färbung, die zum Installieren und Kalibrieren von Farbanzeigegeräten wie Monitoren und Druckern erforderlich sind.



| Funktion | BESCHREIBUNG |
|-|-|
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Schließt ein geöffnetes Profilhandle. |
| [**CreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | Erstellt ein *GERÄTELINKprofil* (International Color Consortium, INTERNATIONAL Color Consortium) aus einer Reihe von Farbprofilen unter Verwendung der angegebenen Absichten. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Kopiert Daten aus einem angegebenen markierten Profilelement eines angegebenen Farbprofils in einen Puffer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Ruft den tag-Namen ab, der von *dwIndex* in der Tagtabelle eines angegebenen COLOR-Farbprofils (International Color Consortium) angegeben wird, wobei *dwIndex* ein 1-basierter Index in dieser Tabelle ist. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| Ruft den Inhalt des Farbprofils ab, wenn ein Handle für ein offenes Farbprofil angegeben wird.     |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Ruft die CAB-Headerstruktur aus dem COLOR-Farbprofil oder dem WCS-XML-Profil ab oder leitet diese ab. Treiber und Anwendungen sollten davon ausgehen, dass **TRUE** zurückgegeben wird, gibt nur an, dass ein ordnungsgemäß strukturierter Header zurückgegeben wird. Jedes Tag muss weiterhin unabhängig mithilfe von Legacy-ICM2-APIs oder XML-Schema-APIs überprüft werden. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Ruft die Anzahl der markierten Elemente in einem angegebenen Farbprofil ab. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Ruft das Farbrenderingwörterbuch der PostScript Ebene 2 aus dem angegebenen COLOR-Farbprofil ab. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Ruft die Absicht für PostScript [Farbrendering](r.md) auf Ebene 2 aus einem COLOR-Farbprofil ab. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Ruft das PostScript Level [2-Farbraumarray](c.md) aus einem COLOR-Farbprofil ab. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Gibt an, ob im angegebenen Farbprofil ein angegebenes INTERNATIONAL Color Consortium-Tag (INTERNATIONAL Color Consortium) vorhanden ist. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Hiermit können Sie bestimmen, ob das angegebene Profil ein gültiges INTERNATIONAL Color Consortium-Profil (INTERNATIONAL Color Consortium) oder ein gültiges WCS-Profilhandle (Windows Color System) ist, das für die Farbverwaltung verwendet werden kann. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Erstellt ein Handle für ein angegebenes Farbprofil. Das Handle kann dann in anderen Profilverwaltungsfunktionen verwendet werden. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Legt die Elementdaten für ein markiertes Profilelement in einem COLOR-Farbprofil fest. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Erstellt in einem angegebenen COLOR-Farbprofil ein neues Tag, das auf dieselben Daten wie ein vorhandenes Tag verweist. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Legt die Größe eines markierten Elements in einem COLOR-Farbprofil fest. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Legt die Headerdaten in einem angegebenen COLOR-Farbprofil fest. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Bestimmt, ob die Systemverwaltung des Kalibrierungszustands der Anzeige aktiviert ist. |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Bestimmt, ob die Systemverwaltung des Kalibrierungszustands der Anzeige aktiviert ist. |



 

 

 




