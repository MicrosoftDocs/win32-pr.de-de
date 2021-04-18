---
title: Alphabetische Liste aller WCS-Funktionen
description: Im folgenden finden Sie eine komplette alphabetische Liste der WCS 1,0-API-Funktionen, die von Windows \ 160; 98 und höher und Windows \ 160; 2000 und höher bereitgestellt werden.
ms.assetid: aba45dbd-6fc2-4788-87f0-043579fa53f9
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bild Farbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCs, Funktionen
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b70208c1f1f7d87b4f5cd6f4a14f3f22e0bc2f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351859"
---
# <a name="alphabetical-list-of-all-wcs-functions"></a>Alphabetische Liste aller WCS-Funktionen

Im folgenden finden Sie eine komplette alphabetische Liste der WCS 1,0-API-Funktionen, die von Windows 98 und höher und Windows 2000 und höher bereitgestellt werden.



| Funktion oder Struktur                                                                 | BESCHREIBUNG                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (oder **applycallbackfunction**) ist eine Rückruffunktion, die Sie implementieren, um die WCS-Konfigurationsdaten zu aktualisieren, während das Dialogfeld, das von der [**setupcolormatchingw**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) -Funktion angezeigt wird, ausgeführt wird. |
| [**Associatecolorprofilewithdevicew**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Ordnet ein angegebenes Farbprofil einem angegebenen Gerät zu.                                                                                                            |
| [**Checkbitmapbits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Überprüft, ob die Pixel in einer angegebenen Bitmap innerhalb des Ausgabe [gamches](g.md) einer angegebenen Transformation liegen. |
| [**Prüf Farben**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Bestimmt, ob die Farben in einem Array [im Ausgabe Spiel einer angegebenen](g.md) Transformation liegen. |
| [**Checkcolorsingamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                                       | Überprüft, ob die angegebenen Farben sich im Gamut eines Geräts befinden.                                                                                                      |
| [**Closecolorprofile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Schließt ein geöffnetes Profil handle. |
| [**Cmcheckcolors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Bestimmt, ob angegebene Farben [im Ausgabe Spiel einer angegebenen](./g.md) Transformation liegen. |
| [**Cmcheckcolorsingamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Bestimmt, ob die angegebenen RGB-drei [im Ausgabe Spiel einer angegebenen](./g.md) Transformation liegen. |
| [**Cmcheckrgsb**](/windows/desktop/api/Wingdi/)                                                     | Überprüft Bitmap-Farben anhand eines Ausgabe gamches.                                                                                                        |
| [**Cmconvertcolornametoindex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Konvertiert Farbnamen in einem benannten Farbraum in Indexnummern in einem Farbprofil |
| [**Cmconvertindexycolorname**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**Cmkreatedevicelinkprofile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Erstellt ein [Geräte](./d.md) Verknüpfungs Profil in dem Format, das vom International Color Consortium in seiner Spezifikation für das ICC-Profil Format angegeben wird. |
| [**Cmkreatemultiprofiletransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Akzeptiert ein Array von Profilen oder ein einzelnes [Geräte](./d.md) Verknüpfungs Profil und erstellt eine Farb Transformation. Diese Transformation ist eine Zuordnung von dem Farbraum, der durch das erste Profil angegeben wird, zu dem des zweiten Profils usw. |
| [**Cmkreateprofile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Erstellt ein Anzeige Farbprofil aus einer [**logcolorspacea**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) -Struktur. |
| [**Cmkreateprofilew**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Erstellt ein Anzeige Farbprofil aus einer [**logcolorspacew**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) -Struktur. |
| [**Cmkreatetransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | Veraltet. Es gibt keine Ersatz-API, da diese nicht mehr verwendet wird. Entwickler alternativer CMM-Module müssen diese nicht implementieren. |
| [**Cmkreatetransformext**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Erstellt eine Farb Transformation, die von einer Eingabe [**logcolorspacea**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) zu einem optionalen Ziel Raum und dann zu einem Ausgabegerät zugeordnet wird. dabei wird ein Satz von Flags verwendet, die definieren, wie die Transformation erstellt werden soll. |
| [**Cmkreatetransformextw**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Erstellt eine Farb Transformation, die von einer Eingabe [**logcolorspacew**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) zu einem optionalen Ziel Raum und dann zu einem Ausgabegerät zugeordnet wird. dabei wird ein Satz von Flags verwendet, die definieren, wie die Transformation erstellt werden soll. |
| [**Cmkreatetransformw**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | Veraltet. Es gibt keine Ersatz-API, da diese nicht mehr verwendet wird. Entwickler alternativer CMM-Module müssen diese nicht implementieren. |
| [**Cmdeletetransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Löscht eine angegebene Farb Transformation und gibt den zugeordneten Arbeitsspeicher frei. |
| [**Cmgetinfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Ruft verschiedene Informationen über das Farb Verwaltungsmodul (Color Management Module, CMM) ab. |
| [**Cmgetnamedprofileingefo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Ruft Informationen über das angegebene benannte Farbprofil ab. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/)           | Ruft ein PostScript-Farb Rendering-Wörterbuch ab.                                                                                                        |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Ruft das [textrenderingziel](rendering-intents.md) der PostScript-Ebene 2 aus einem Profil ab. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                             | Ruft ein Zeichen für ein PostScript-Farbraum ab.                                                                                                                 |
| [**Cmispromelevalid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Meldet, ob das angegebene Profil ein gültiges ICC-Profil ist, das für die Farbverwaltung verwendet werden kann. |
| [**Cmtranslatecolors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Übersetzt ein Array von Farben aus einem Quell [Farbraum](color-spaces.md) mithilfe einer Farb Transformation in einen Ziel Farbraum. |
| [**Cmtranslatergb**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Übersetzt ein von der Anwendung bereitgestelltes rgbquad in den Geräte [Farbraum](color-spaces.md). |
| [**Cmtranslatergsb**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Übersetzt eine Bitmap mithilfe einer Farb Transformation von einem [Farb Raum](color-spaces.md) in einen anderen. |
| [**Cmtranslatergbsegxt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Übersetzt eine Bitmap aus einem definierten Format in ein anderes definiertes Format und ruft in regelmäßigen Abständen eine Rückruffunktion auf, wenn eine angegeben wird, um den Fortschritt zu melden und zuzulassen, dass die aufrufenden Anwendung die Übersetzung beendet. |
| [**Colorcorrectpalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                                     | Korrigiert die Einträge in einer Palette für einen Gerätekontext.                                                                                              |
| [**Colormatchdetarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                                       | Führt eine Farbzuordnung für Vorschau Zwecke aus.                                                                                                         |
| [**Convertcolornametoindex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Konvertiert Farbnamen in einem benannten Farbraum in Indexnummern in einem International Color Consortium (ICC)-Farbprofil. |
| [**Convertindexycolorname**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**"Kreatecolorspace"**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                                           | Erstellt einen Farbraum.                                                                                                                               |
| [**"Kreatecolortransformw"**](/windows/win32/api/icm/nf-icm-createcolortransforma) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**"Kreatecolortransformw"**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**"Kreatemultiprofiletransform"**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Akzeptiert ein Array von Profilen oder ein einzelnes [Geräte](d.md) Verknüpfungs Profil und erstellt eine Farb Transformation, mit der Anwendungen eine Farbzuordnung durchführen können. |
| [**Erkreateprofilefromlogcolorspacew**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Konvertiert einen logischen [Farbraum](c.md) in ein [Geräte Profil](d.md). |
| [**Deletecolorspace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                                           | Löscht einen Farbraum.                                                                                                                               |
| [**Deletecolortransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Löscht eine angegebene Farb Transformation. |
| [**Disassociatecolorprofilefromdevicew**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Trennt ein angegebenes Farbprofil einem angegebenen Gerät auf einem angegebenen Computer. |
| [**Enumcolorprofilesw**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Listet alle Profile auf, die die angegebenen enumerationskriterien erfüllen. |
| [**"Umumicmprofiles"**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                                             | Listet Ausgabe Farbprofile auf, die für einen bestimmten Gerätekontext verfügbar sind.                                                                               |
| [**"Umumicmprofilesproccallback"**](/windows/desktop/api/Wingdi/)                     | Anwendungs definierte Rückruffunktion für [**enumicmprofiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).                                                                |
| [**Getcmminfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Ruft verschiedene Informationen über das Farb Verwaltungsmodul (Color Management Module, CMM) ab, das die angegebene Farb Transformation erstellt hat. |
| [**Getcolordirector**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Ruft den Pfad des Windows-Farb Verzeichnisses auf einem angegebenen Computer ab. |
| [**Getcolorprofileelement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Kopiert Daten aus einem angegebenen markierten Profil Element eines angegebenen Farbprofils in einen Puffer. |
| [**Getcolorprofileelementtag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Ruft den von *dwIndex* angegebenen Tagnamen in der Tagtabelle eines bestimmten International Color Consortium (ICC)-Farbprofils ab, wobei *dwIndex* ein einbasierter Index in dieser Tabelle ist. |
| [**Getcolorprofilefromhandle**](/windows/win32/api/icm/getcolorprofilefromhandle)                         | Ruft den Farbprofil Inhalt ab, wenn ein Handle für ein geöffnetes Farbprofil angegeben ist.                                                                        |
| [**Getcolorprofileheader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Ruft die ICC-Header Struktur entweder aus dem ICC-Farbprofil oder dem WCS-XML-Profil ab oder leitet Sie Treiber und Anwendungen sollten davon ausgehen, dass die Rückgabe von **true** nur bedeutet, dass ein ordnungsgemäß strukturierter Header zurückgegeben wird Jedes Tag muss mithilfe von Legacy-ICM2-APIs oder XML-Schema-APIs unabhängig überprüft werden. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Ruft den aktuellen Eingabe Farbraum in einem Gerätekontext ab. |
| [**Getcountrytcolorprofileelements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Ruft die Anzahl der markierten Elemente in einem angegebenen Farbprofil ab. |
| [**Getde vicegammaramp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Ruft die Gamma-Rampe von der direkten Farbanzeige Boards ab.                                                                                                |
| [**Geticmprofile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                                                 | Ruft das aktuelle Ausgabe Farbprofil eines Geräte Kontexts ab.                                                                                           |
| [**Getlogcolorspace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                                           | Ruft die [**logcolorspace**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) -Struktur eines Geräte Kontexts ab.                                                                       |
| [**Getnamedprofilinfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Ruft Informationen über das im ersten Parameter angegebene benannte Farbprofil des International Color Consortium (ICC) ab. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Ruft das textrenderingwörterbuch der PostScript-Ebene 2 aus dem angegebenen "ICC"-Farbprofil |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Ruft die [textrenderingabsicht](r.md) der PostScript-Ebene 2 aus einem ICC-Farbprofil ab. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Ruft das Bytearray der [](c.md) PostScript-Ebene 2 aus einem ICC-Farbprofil ab. |
| [**Getstandardcolorspaceprofilew**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Ruft das Farbprofil ab, das für den angegebenen Standard [Farbraum](c.md)registriert ist. |
| [**Icmprogressproccallback**](icmprogressproccallback.md)                             | Von der Anwendung bereitgestellter Rückruf zum Melden des Status.                                                                                                    |
| [**Installcolorprofilew**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installiert ein bestimmtes Profil für die Verwendung auf einem angegebenen Computer. Das Profil wird auch in das Farb Verzeichnis kopiert. |
| [**Iscolorprofiletagpresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Meldet, ob ein angegebenes International Color Consortium-Tag (ICC) im angegebenen Farbprofil vorhanden ist. |
| [**Iscolorprofilevalid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Hiermit können Sie bestimmen, ob es sich bei dem angegebenen Profil um ein gültiges International Color Consortium (ICC)-Profil oder ein gültiges Windows Color System (WCS)-Profil Handle handelt, das für die Farbverwaltung verwendet werden kann. |
| [**Opencolorprofilew**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Erstellt ein Handle für ein angegebenes Farbprofil. Das Handle kann dann in anderen Profil Verwaltungsfunktionen verwendet werden. |
| [**Registercmmw**](/windows/win32/api/icm/nf-icm-registercmmw) | Ordnet einen angegebenen Identifikations Wert der angegebenen CMM-dll (Dynamic Link Library) des Farb Verwaltungs Moduls zu. Wenn diese ID in einem Farbprofil angezeigt wird, kann Windows den entsprechenden CMM-Code suchen, um eine Transformation zu erstellen. |
| [**Selectcmm**](/windows/win32/api/icm/nf-icm-selectcmm) | Ermöglicht es Ihnen, das zu verwendende bevorzugte Farb Verwaltungsmodul (CMM) auszuwählen. |
| [**Setcolorprofileelement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Legt die Elementdaten für ein getaggtes Profil Element in einem Datenprofil für den IStGH fest. |
| [**Setcolorprofileelementreference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Erstellt in einem angegebenen ICC-Farbprofil ein neues Tag, das auf dieselben Daten wie ein vorhandenes Tag verweist. |
| [**Setcolorprofileelementsize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Legt die Größe eines markierten Elements in einem poolfarbprofil fest. |
| [**Setcolorprofileheader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Legt die Header Daten in einem angegebenen ICC-Farbprofil fest. |
| [**Setcolorspace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                                                 | Legt den Eingabe Farbraum eines Geräte Kontexts fest.                                                                                                           |
| [**Setde vicegammaramp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Legt die Gamma-Rampe für die Anzeige Boards der direkten Farbe fest.                                                                                                  |
| [**-Modus**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                                       | Schaltet die Farbverwaltung in einem Gerätekontext ein bzw. aus.                                                                                                |
| [**"Abbild profile"**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                                                 | Legt das Ausgabe Farbprofil für einen angegebenen Gerätekontext fest.                                                                                            |
| [**Setstandardcolorspaceprofilew**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registriert ein angegebenes Profil für einen angegebenen Standard [Farbraum](c.md). Das Profil kann mithilfe von [getstandardcolorspaceprofilew](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew)abgefragt werden. |
| [**Setupcolormatchingw**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                                       | Ermöglicht die Benutzersteuerung der Farbverwaltung über ein Dialogfeld.                                                                                  |
| [**Translatebitmapbits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                                     | Konvertiert Bitmapfarben mithilfe einer Farb Transformation.                                                                                                      |
| [**Translatecolors**](/windows/win32/api/icm/nf-icm-translatecolors) | Übersetzt ein Array von Farben aus dem [Quellfarbraum](c.md) in den Ziel Farbraum, wie durch eine Farb Transformation definiert. |
| [**Uninstallcolorprofilew**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Entfernt ein angegebenes Farbprofil von einem angegebenen Computer. Zugehörige Dateien werden optional aus dem System gelöscht. |
| [**Unregistercmmw**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Trennt einen angegebenen ID-Wert aus einer angegebenen Dynamic Link Library (CMM-dll) des Farb Verwaltungs Moduls. |
| [**Wcsassociatecolorprofilewithdevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Ordnet ein angegebenes WCS-Farbprofil einem angegebenen Gerät zu.                                                                                    |
| [**Wcscheckcolors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                                               | Bestimmt, ob die Farben in einem Array innerhalb des Ausgabe Farbskala einer angegebenen WCS-Farb Transformation liegen.                                            |
| [**Wcscreateiccprofile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Konvertiert ein WCS-Profil in ein-ICC-Profil.                                                                                                          |
| [**Wcsdisassociatecolorprofilefromdevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Trennt ein angegebenes WCS-Farbprofil einem angegebenen Gerät auf einem angegebenen Computer.                                                         |
| [**Wcsenaufcolorprofiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Listet alle Farbprofile auf, die die enumerationskriterien im angegebenen Profil Verwaltungsbereich erfüllen.                                       |
| [**Wcsenaufcolorprofilessize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) | Gibt die Größe (in Bytes) des Puffers zurück, der von der Funktion [**wcsenumcolorprofiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) zum Auflisten von Farbprofilen benötigt wird. |
| [**Wcsgetcalibrationmanagementstate**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Bestimmt, ob die Systemverwaltung des Anzeige-Kalibrierungs Zustands aktiviert ist.                                                                    |
| [**Wcsgetdefaultcolorprofile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) | Ruft das Standard Farbprofil für ein Gerät oder den geräteunabhängigen Standardwert ab, wenn das Gerät nicht angegeben ist.                                  |
| [**Wcsgetdefaultcolorprofilesize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Gibt die Größe (in Bytes) des standardmäßigen Farbprofil namens für ein Gerät zurück, einschließlich des **null** -Terminator.                                       |
| [**Wcsgetdefaultrenderingintent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Gibt die Benutzer-oder systemweite renderabsicht zurück.                                                                                                    |
| [**Wcsgetuseperuserprofiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Bestimmt, ob der Benutzer eine benutzerspezifische Profil Zuordnungs Liste für das angegebene Gerät verwendet hat.                                          |
| [**Wcsopeincolorprofilew**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Erstellt ein Handle für ein angegebenes Farbprofil.                                                                                                       |
| [**Wcssetcalibrationmanagementstate**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Aktiviert oder deaktiviert die Systemverwaltung des Status der Anzeige Kalibrierung.                                                                              |
| [**Wcssetdefaultcolorprofile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Legt den Standardnamen des Farbprofils für den angegebenen Profiltyp im angegebenen Profil Verwaltungsbereich fest.                                         |
| [**Wcssetdefaultrenderingintent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Legt die Benutzer-oder systemweite renderabsicht fest.                                                                                                       |
| [**Wcssetuseperuserprofiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Ermöglicht es dem Benutzer anzugeben, ob für das angegebene Gerät eine Profil Zuordnungs Liste pro Benutzer verwendet werden soll.                                       |
| [**Wcstranslatecolors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Übersetzt ein Array von Farben aus dem Quellfarbraum in den Ziel Farbraum, wie durch eine Farb Transformation definiert.                            |



 

 

 