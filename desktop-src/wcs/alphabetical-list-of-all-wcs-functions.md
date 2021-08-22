---
title: Alphabetische Liste aller WCS-Funktionen
description: Es folgt eine vollständige alphabetische Liste der WCS 1.0-API-Funktionen, die von Windows \ 160;98 und höher und Windows \ 160;2000 und höher bereitgestellt werden.
ms.assetid: aba45dbd-6fc2-4788-87f0-043579fa53f9
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bildfarbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCS,Functions
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e2c9250cc9fb1e9e418079ed3b9524b3add2535dd780eed65ae998bda80ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706660"
---
# <a name="alphabetical-list-of-all-wcs-functions"></a>Alphabetische Liste aller WCS-Funktionen

Es folgt eine vollständige alphabetische Liste der WCS 1.0-API-Funktionen, die von Windows 98 und höher und Windows 2000 und höher bereitgestellt werden.



| Funktion oder Struktur                                                                 | Beschreibung                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (oder **ApplyCallbackFunction**) ist eine Rückruffunktion, die Sie implementieren, die die WCS-Konfigurationsdaten aktualisiert, während das von der [**SetupColorMatchingW-Funktion**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) angezeigte Dialogfeld ausgeführt wird. |
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Ordnet einem angegebenen Gerät ein angegebenes Farbprofil zu.                                                                                                            |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Überprüft, ob die Pixel in einer angegebenen Bitmap innerhalb der Ausgabe [gamut](g.md) einer angegebenen Transformation liegen. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Bestimmt, ob die Farben in einem Array innerhalb des [Ausgabeumfangs](g.md) einer angegebenen Transformation liegen. |
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                                       | Überprüft, ob sich die angegebenen Farben im Gamut eines Geräts befinden.                                                                                                      |
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Schließt ein geöffnetes Profilhandle. |
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Bestimmt, ob die angegebenen Farben innerhalb der Ausgabe [gamut](./g.md) einer angegebenen Transformation liegen. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Bestimmt, ob die angegebenen RGB-Dreier in der Ausgabe [gamut](./g.md) einer angegebenen Transformation liegen. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                                     | Überprüft Bitmapfarben anhand eines Ausgabe-Gamuts.                                                                                                        |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Konvertiert Farbnamen in einem benannten Farbraum in Indexnummern in einem Farbprofil. |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Erstellt ein [Gerätelinkprofil](./d.md) in dem Format, das vom International Color Consortium in seiner FORMATSPEZIFIKATION FÜR DAS PROFIL ANGEGEBEN wird. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Akzeptiert ein Array von Profilen oder ein einzelnes [Gerätelinkprofil](./d.md) und erstellt eine Farbtransformation. Bei dieser Transformation handelt es sich um eine Zuordnung vom Farbraum, der vom ersten Profil angegeben wird, zu dem des zweiten Profils usw. zum letzten Profil. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Erstellt ein Anzeigefarbprofil aus einer [**LOGCOLORSPACEA-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Erstellt ein Anzeigefarbprofil aus einer [**LOGCOLORSPACEW-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | Veraltet. Es gibt keine Ersatz-API, da diese nicht mehr verwendet wurde. Entwickler alternativer CMM-Module müssen sie nicht implementieren. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Erstellt eine Farbtransformation, die aus einer [**LOGCOLORSPACEA-Eingabe**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) einem optionalen Zielbereich und dann einem Ausgabegerät zugeordnet wird. Dabei wird ein Satz von Flags verwendet, die definieren, wie die Transformation erstellt werden soll. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Erstellt eine Farbtransformation, die aus einer [**LOGCOLORSPACEW-Eingabe**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) einem optionalen Zielbereich und dann einem Ausgabegerät zugeordnet wird, indem ein Satz von Flags verwendet wird, die definieren, wie die Transformation erstellt werden soll. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | Veraltet. Es gibt keine Ersatz-API, da diese nicht mehr verwendet wurde. Entwickler alternativer CMM-Module müssen sie nicht implementieren. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Löscht eine angegebene Farbtransformation und gibt den zugeordneten Arbeitsspeicher frei. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Ruft verschiedene Informationen zum Farbverwaltungsmodul (Color Management Module, CMM) ab. |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Ruft Informationen zum angegebenen benannten Farbprofil ab. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/)           | Ruft ein PostScript Farbrenderingwörterbuch ab.                                                                                                        |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Ruft die [PostScript Farbrenderingabsicht](rendering-intents.md) der Ebene 2 aus einem Profil ab. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                             | Ruft ein PostScript Farbraumarray ab.                                                                                                                 |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Gibt an, ob es sich bei dem angegebenen Profil um ein gültiges PROFIL handelt, das für die Farbverwaltung verwendet werden kann. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Übersetzt ein Array von Farben aus einem [Quellfarbraum](color-spaces.md) mithilfe einer Farbtransformation in einen Zielfarbraum. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Übersetzt ein von der Anwendung bereitgestelltes RGBQuad in den [Farbraum](color-spaces.md)des Geräts. |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Übersetzt eine Bitmap mithilfe einer Farbtransformation aus einem [Farbraum](color-spaces.md) in einen anderen. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Übersetzt eine Bitmap aus einem definierten Format in ein anderes definiertes Format und ruft in regelmäßigen Abständen eine Rückruffunktion auf, wenn eine angegeben ist, um den Fortschritt zu melden und der aufrufenden Anwendung zu erlauben, die Übersetzung zu beenden. |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                                     | Korrigiert die Einträge in einer Palette für einen Gerätekontext.                                                                                              |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                                       | Führt farbliche Zuordnungen für Vorschauzwecke durch.                                                                                                         |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Konvertiert Farbnamen in einem benannten Farbraum in Indexnummern in einem COLOR-Farbprofil (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                                           | Erstellt einen Farbraum.                                                                                                                               |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransforma) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Akzeptiert ein Array von Profilen oder ein einzelnes [Gerätelinkprofil](d.md) und erstellt eine Farbtransformation, die Anwendungen zum Durchführen der Farbzuordnung verwenden können. |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Konvertiert einen logischen [Farbraum](c.md) in ein [Geräteprofil.](d.md) |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                                           | Löscht einen Farbraum.                                                                                                                               |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Löscht eine angegebene Farbtransformation. |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Trennt die Zuordnung eines angegebenen Farbprofils zu einem angegebenen Gerät auf einem angegebenen Computer. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Listet alle Profile auf, die die angegebenen Enumerationskriterien erfüllen. |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                                             | Listet Ausgabefarbprofile auf, die für einen bestimmten Gerätekontext verfügbar sind.                                                                               |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/)                     | Anwendungsdefinierte Rückruffunktion für [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).                                                                |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Ruft verschiedene Informationen zum Farbverwaltungsmodul (Color Management Module, CMM) ab, das die angegebene Farbtransformation erstellt hat. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Ruft den Pfad des Windows COLOR-Verzeichnisses auf einem angegebenen Computer ab. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Kopiert Daten aus einem angegebenen markierten Profilelement eines angegebenen Farbprofils in einen Puffer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Ruft den tag-Namen ab, der von *dwIndex* in der Tagtabelle eines angegebenen COLOR-Farbprofils (International Color Consortium) angegeben wird, wobei *dwIndex* ein 1-basierter Index in dieser Tabelle ist. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/getcolorprofilefromhandle)                         | Ruft den Inhalt des Farbprofils ab, wenn ein Handle für ein offenes Farbprofil angegeben wird.                                                                        |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Ruft die CAB-Headerstruktur aus dem COLOR-Farbprofil oder dem WCS-XML-Profil ab oder leitet diese ab. Treiber und Anwendungen sollten davon ausgehen, dass **TRUE** zurückgegeben wird, gibt nur an, dass ein ordnungsgemäß strukturierter Header zurückgegeben wird. Jedes Tag muss weiterhin unabhängig mithilfe von Legacy-ICM2-APIs oder XML-Schema-APIs überprüft werden. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Ruft den aktuellen Eingabefarbraum in einem Gerätekontext ab. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Ruft die Anzahl der markierten Elemente in einem angegebenen Farbprofil ab. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Ruft die Gamma-Rampe aus direkten Farbanzeigeboards ab.                                                                                                |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                                                 | Ruft das aktuelle Ausgabefarbprofil eines Gerätekontexts ab.                                                                                           |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                                           | Ruft die [**LOGCOLORSPACE-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) eines Gerätekontexts ab.                                                                       |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Ruft Informationen zum benannten Farbprofil des International Color Consortium (INTERNATIONAL) ab, das im ersten Parameter angegeben ist. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Ruft das Farbrenderingwörterbuch der PostScript Ebene 2 aus dem angegebenen COLOR-Farbprofil ab. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Ruft die [Farbrenderingabsicht](r.md) PostScript Ebene 2 aus einem COLOR-Farbprofil ab. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Ruft das PostScript Level [2-Farbraumarray](c.md) aus einem COLOR-Farbprofil ab. |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Ruft das Farbprofil ab, das für den angegebenen [Standardfarbraum](c.md)registriert ist. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)                             | Von der Anwendung bereitgestellter Rückruf zum Melden des Fortschritts.                                                                                                    |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installiert ein bestimmtes Profil zur Verwendung auf einem angegebenen Computer. Das Profil wird auch in das Verzeichnis COLOR kopiert. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Gibt an, ob im angegebenen Farbprofil ein angegebenes INTERNATIONAL Color Consortium-Tag (INTERNATIONAL Color Consortium) vorhanden ist. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Hiermit können Sie bestimmen, ob das angegebene Profil ein gültiges INTERNATIONAL Color Consortium-Profil (INTERNATIONAL Color Consortium) oder ein gültiges WCS-Profilhandle (Windows Color System) ist, das für die Farbverwaltung verwendet werden kann. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Erstellt ein Handle für ein angegebenes Farbprofil. Das Handle kann dann in anderen Profilverwaltungsfunktionen verwendet werden. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Ordnet der angegebenen Dynamic Link Library (CMM DLL) des angegebenen Farbverwaltungsmoduls einen angegebenen Identifikationswert zu. Wenn diese ID in einem Farbprofil angezeigt wird, können Windows das entsprechende CMM suchen, um eine Transformation zu erstellen. |
| [**Wählen SieCMM aus.**](/windows/win32/api/icm/nf-icm-selectcmm) | Ermöglicht ihnen die Auswahl des bevorzugten Farbverwaltungsmoduls (CMM), das verwendet werden soll. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Legt die Elementdaten für ein markiertes Profilelement in einem COLOR-Farbprofil fest. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Erstellt in einem angegebenen COLOR-Farbprofil ein neues Tag, das auf dieselben Daten wie ein vorhandenes Tag verweist. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Legt die Größe eines markierten Elements in einem COLOR-Farbprofil fest. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Legt die Headerdaten in einem angegebenen COLOR-Farbprofil fest. |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                                                 | Legt den Eingabefarbraum eines Gerätekontexts fest.                                                                                                           |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Legt die Gamma-Rampe auf direkten Farbanzeigeboards fest.                                                                                                  |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                                       | Aktiviert oder deaktiviert die Farbverwaltung in einem Gerätekontext.                                                                                                |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                                                 | Legt das Ausgabefarbprofil für einen bestimmten Gerätekontext fest.                                                                                            |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registriert ein angegebenes Profil für einen angegebenen [Standardfarbraum.](c.md) Das Profil kann mit [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew)abgefragt werden. |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                                       | Stellt die Benutzersteuerung über die Farbverwaltung über ein Dialogfeld bereit.                                                                                  |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                                     | Konvertiert Bitmapfarben mithilfe einer Farbtransformation.                                                                                                      |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Übersetzt ein Array von Farben aus dem [Quellfarbraum](c.md) in den Zielfarbraum, wie durch eine Farbtransformation definiert. |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Entfernt ein angegebenes Farbprofil von einem angegebenen Computer. Zugeordnete Dateien werden optional aus dem System gelöscht. |
| [**Aufheben der Registrierung vonCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Hebt die Trennung eines angegebenen ID-Werts von einer angegebenen Dynamic Link Library (CMM-DLL) des Farbverwaltungsmoduls auf. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Ordnet einem angegebenen Gerät ein angegebenes WCS-Farbprofil zu.                                                                                    |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                                               | Bestimmt, ob die Farben in einem Array innerhalb der Ausgabe gamut einer angegebenen WCS-Farbtransformation liegen.                                            |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Konvertiert ein WCS-Profil in einWKS-Profil.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Trennt die Zuordnung eines angegebenen WCS-Farbprofils zu einem angegebenen Gerät auf einem angegebenen Computer.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Listet alle Farbprofile auf, die die Enumerationskriterien im angegebenen Profilverwaltungsbereich erfüllen.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) | Gibt die Größe des Puffers in Bytes zurück, der von der [**WcsEnumColorProfiles-Funktion**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) zum Aufzählen von Farbprofilen benötigt wird. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Bestimmt, ob die Systemverwaltung des Kalibrierungszustands der Anzeige aktiviert ist.                                                                    |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) | Ruft das Standardfarbprofil für ein Gerät oder den geräteunabhängigen Standard ab, wenn das Gerät nicht angegeben ist.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Gibt die Größe des Standardfarbprofilnamens für ein  Gerät in Bytes zurück, einschließlich des NULL-Abschlusszeichens.                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Gibt die benutzer- oder systemweite Renderingabsicht zurück.                                                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Bestimmt, ob der Benutzer eine Benutzerprofil-Zuordnungsliste für das angegebene Gerät verwendet hat.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Erstellt ein Handle für ein angegebenes Farbprofil.                                                                                                       |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Aktiviert oder deaktiviert die Systemverwaltung des Kalibrierungszustands der Anzeige.                                                                              |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Legt den Standardfarbprofilnamen des angegebenen Profiltyps im angegebenen Profilverwaltungsbereich fest.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Legt die benutzer- oder systemweite Renderingabsicht fest.                                                                                                       |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Ermöglicht dem Benutzer anzugeben, ob eine Benutzerprofil-Zuordnungsliste für das angegebene Gerät verwendet werden soll.                                       |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Übersetzt ein Array von Farben aus dem Quellfarbraum in den Zielfarbraum, wie durch eine Farbtransformation definiert.                            |



 

 

 