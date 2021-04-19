---
title: Geräterkalibrierung und Charakterisierungsfunktionen
description: Die folgenden Funktionen sind nützlich für das Schreiben von geräterkalibrierung und-Charakterisierungs Tools, die für die Installation und das Kalibrieren von Farbanzeige Geräten wie Monitoren und Druckern erforderlich
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bild Farbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCs, Funktionen
- Windows Color System (WCS), Gerätekalibrierung
- WCS (Windows Color System), Gerätekalibrierung
- Bild Farbverwaltung, Gerätekalibrierung
- Farbverwaltung, Gerätekalibrierung
- Farben, Gerätekalibrierung
- WCS-Referenz, Gerätekalibrierung
- Referenz für WCs, Gerätekalibrierung
- Windows Color System (WCS), Charakterisierung
- WCS (Windows Color System), Charakterisierung
- Bild Farbverwaltung,-Charakterisierung
- Farbverwaltung, Charakterisierung
- Farben, Charakterisierung
- WCS-Referenz,-Charakterisierung
- Referenz für WCs, Charakterisierung
- Gerätekalibrierung
- Energie
- Charakterisierung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106361834"
---
# <a name="device-calibration-and-characterization-functions"></a>Geräterkalibrierung und Charakterisierungsfunktionen

Die folgenden Funktionen sind nützlich für das Schreiben von geräterkalibrierung und-Charakterisierungs Tools, die für die Installation und das Kalibrieren von Farbanzeige Geräten wie Monitoren und Druckern erforderlich



| Funktion | BESCHREIBUNG |
|-|-|
| [**Closecolorprofile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Schließt ein geöffnetes Profil handle. |
| [**"Kreatedevicelinkprofile"**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | Erstellt unter Verwendung der angegebenen Intents ein International Color Consortium (ICC)-Geräte Verknüpfungs *Profil* aus einem Satz von Farbprofilen. |
| [**Getcolorprofileelement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Kopiert Daten aus einem angegebenen markierten Profil Element eines angegebenen Farbprofils in einen Puffer. |
| [**Getcolorprofileelementtag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Ruft den von *dwIndex* angegebenen Tagnamen in der Tagtabelle eines bestimmten International Color Consortium (ICC)-Farbprofils ab, wobei *dwIndex* ein einbasierter Index in dieser Tabelle ist. |
| [**Getcolorprofilefromhandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| Ruft den Farbprofil Inhalt ab, wenn ein Handle für ein geöffnetes Farbprofil angegeben ist.     |
| [**Getcolorprofileheader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Ruft die ICC-Header Struktur entweder aus dem ICC-Farbprofil oder dem WCS-XML-Profil ab oder leitet Sie Treiber und Anwendungen sollten davon ausgehen, dass die Rückgabe von **true** nur bedeutet, dass ein ordnungsgemäß strukturierter Header zurückgegeben wird Jedes Tag muss mithilfe von Legacy-ICM2-APIs oder XML-Schema-APIs unabhängig überprüft werden. |
| [**Getcountrytcolorprofileelements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Ruft die Anzahl der markierten Elemente in einem angegebenen Farbprofil ab. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Ruft das textrenderingwörterbuch der PostScript-Ebene 2 aus dem angegebenen "ICC"-Farbprofil |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Ruft die [textrenderingabsicht](r.md) der PostScript-Ebene 2 aus einem ICC-Farbprofil ab. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Ruft das Bytearray der [](c.md) PostScript-Ebene 2 aus einem ICC-Farbprofil ab. |
| [**Iscolorprofiletagpresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Meldet, ob ein angegebenes International Color Consortium-Tag (ICC) im angegebenen Farbprofil vorhanden ist. |
| [**Iscolorprofilevalid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Hiermit können Sie bestimmen, ob es sich bei dem angegebenen Profil um ein gültiges International Color Consortium (ICC)-Profil oder ein gültiges Windows Color System (WCS)-Profil Handle handelt, das für die Farbverwaltung verwendet werden kann. |
| [**Opencolorprofilew**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Erstellt ein Handle für ein angegebenes Farbprofil. Das Handle kann dann in anderen Profil Verwaltungsfunktionen verwendet werden. |
| [**Setcolorprofileelement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Legt die Elementdaten für ein getaggtes Profil Element in einem Datenprofil für den IStGH fest. |
| [**Setcolorprofileelementreference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Erstellt in einem angegebenen ICC-Farbprofil ein neues Tag, das auf dieselben Daten wie ein vorhandenes Tag verweist. |
| [**Setcolorprofileelementsize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Legt die Größe eines markierten Elements in einem poolfarbprofil fest. |
| [**Setcolorprofileheader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Legt die Header Daten in einem angegebenen ICC-Farbprofil fest. |
| [**Wcsgetcalibrationmanagementstate**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Bestimmt, ob die Systemverwaltung des Anzeige-Kalibrierungs Zustands aktiviert ist. |
| [**Wcssetcalibrationmanagementstate**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Bestimmt, ob die Systemverwaltung des Anzeige-Kalibrierungs Zustands aktiviert ist. |



 

 

 




