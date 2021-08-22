---
title: Profilverwaltungsfunktionen
description: Profilverwaltungsfunktionen
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Farbsystem (WCS), Funktionen
- WCS (Windows Color System), Functions
- Bildfarbverwaltung,Funktionen
- Farbverwaltung,Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCS, Functions
- Windows Farbsystem (WCS), Profile
- WCS (Windows Color System), Profiles
- Bildfarbverwaltung,Profile
- Farbverwaltung,Profile
- Farben,Profile
- WCS-Referenz,Profile
- Referenz für WCS, Profile
- Profilverwaltung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f047c2dee199800fad976dd7b959fbbb54d585fd252fb8b5390c3223415db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587770"
---
# <a name="profile-management-functions"></a>Profilverwaltungsfunktionen

## <a name="profile-management-functions"></a>Profilverwaltungsfunktionen

Die folgenden API-Funktionen sind bei der Profilverwaltung nützlich.



| Funktion                                                                               | Beschreibung                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Ordnet einem angegebenen Gerät ein angegebenes Farbprofil zu.                                                              |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Konvertiert einen logischen [Farbraum in](c.md) ein [Geräteprofil.](d.md) |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Die Zuordnung eines angegebenen Farbprofils zu einem angegebenen Gerät auf einem angegebenen Computer wird eingestellt. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumeriert alle Profile, die die angegebenen Enumerationskriterien erfüllen. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Ruft den Pfad des Verzeichnisses Windows COLOR auf einem angegebenen Computer ab. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Ruft die Gamma-Rampe aus direkten Farbanzeigeboards ab.                                                                                                |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Ruft das für den angegebenen Standardfarbraum registrierte [Farbprofil ab.](c.md) |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installiert ein bestimmtes Profil für die Verwendung auf einem angegebenen Computer. Das Profil wird auch in das Verzeichnis COLOR kopiert. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Ordnet der angegebenen CmM-DLL (Dynamic Link Library) des Farbverwaltungsmoduls einen angegebenen Identifikationswert zu. Wenn diese ID in einem Farbprofil angezeigt wird, Windows dann das entsprechende CMM suchen, um eine Transformation zu erstellen. |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Legt die Gamma-Rampe auf direkten Farbanzeigeboards fest.                                                                                                  |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registriert ein angegebenes Profil für einen angegebenen [Standardfarbraum.](c.md) Das Profil kann mit [GetStandardColorSpaceProfileW abgefragt werden.](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Entfernt ein angegebenes Farbprofil von einem angegebenen Computer. Zugeordnete Dateien werden optional aus dem System gelöscht. |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Entfernt einen angegebenen ID-Wert von einer angegebenen Dynamic Link Library (CMM-DLL) eines Farbverwaltungsmoduls. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Ordnet einem angegebenen Gerät ein angegebenes WCS-Farbprofil zu.                                                                                    |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Konvertiert ein WCS-Profil in einCS-Profil.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Die Zuordnung eines angegebenen WCS-Farbprofils zu einem angegebenen Gerät auf einem angegebenen Computer wird eingestellt.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumeriert alle Farbprofile, die die Enumerationskriterien im angegebenen Profilverwaltungsbereich erfüllen.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | Gibt die Größe des Puffers in Bytes zurück, der von der [**WcsEnumColorProfiles-Funktion**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) zum Aufzählen von Farbprofilen benötigt wird. |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | Ruft das Standardfarbprofil für ein Gerät oder den geräteunabhängigen Standard ab, wenn das Gerät nicht angegeben ist.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Gibt die Größe des Standardfarbprofilnamens für ein  Gerät in Bytes zurück, einschließlich des NULL-Abschlusszeichens.                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Ruft die Standardrenderingabsicht im angegebenen Profilverwaltungsbereich ab.                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Bestimmt, ob der Benutzer eine Benutzerprofil-Zuordnungsliste für das angegebene Gerät verwendet hat.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Erstellt ein Handle für ein angegebenes Farbprofil.                                                                                                       |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Legt den Standardfarbprofilnamen des angegebenen Profiltyps im angegebenen Profilverwaltungsbereich fest.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Legt die Standardrenderingabsicht im angegebenen Profilverwaltungsbereich fest.                                                                         |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Ermöglicht dem Benutzer anzugeben, ob eine Benutzerprofil-Zuordnungsliste für das angegebene Gerät verwendet werden soll.                                              |



 

## <a name="profile-consumption-functions"></a>Profilverbrauchsfunktionen

Die Profilverbrauchs-APIs sind die APIs in ICM2, die COD- oder WCS-XML-Profile, Profilhandles oder Renderingabsichten als Parameter und eine Reihe neuer APIs für wcs-Profilunterstützung für Anwendungsfarbverwaltungscode verwenden.

 

## <a name="profiles-and-profile-management-functions"></a>Profile und Profilverwaltungsfunktionen

Der Workflow für die Profilverwaltung basiert auf vorhandenen ICM2-APIs, die erweitert wurden, um zusätzliche Funktionen für die Überarbeitung von Anwendungscode zu bieten.

Profile enthalten Informationen, die von Farbverarbeitungsalgorithmen verwendet werden, um Farben zwischen verschiedenen Farbräumen zu übersetzen. Die Profilverwaltung bietet eine Möglichkeit zum Abfragen und Angeben der Profile, die vom Farbverarbeitungsmodell in verschiedenen Phasen verwendet werden, um die Farbausgabe verschiedener Peripheriegeräte mit unterschiedlichen Farbmerkmalen zu verwalten.

Die Profilverwaltung bietet die folgenden Funktionen:

 

1. Installieren von Farbprofilen für die Verwendung im System.

 

2. Zuordnen eines oder mehrere installierter Farbprofile zu einem bestimmten Gerät.

 

3. Auswählen eines Standardfarbprofils eines bestimmten Typs unter den Profilen, die für die Verwendung in einer bestimmten Phase der Farbverarbeitung verfügbar sind. Dies kann für ein Gerät unter den zugeordneten Profilen oder unter den im System installierten Profilen und nicht gerätespezifisch sein.

 

4. Aufzählen von Farbprofilen, die bestimmte Kriterien unter den im System installierten Profilen erfüllen.

Die Dateierweiterungen des WCS-Profils sind ".cdmp" für DMPs, ".sollen" für NAPPs und ".gmmp" für GMMPs sein.

 

**Profilverwaltung pro Benutzer und Aktivieren der Ausführung im LUA-Kontext**

Das Ziel des im aktuellen Dokument beschriebenen Entwurfs lautet wie folgt:

 

1. Die ICM2-Legacyimplementierung bietet keine Unterstützung für die Profilverwaltung pro Benutzer. Verschiedene Benutzer können keine eigenen Profileinstellungen haben. In Vista können Benutzer mit der WCS-Profilverwaltungsinfrastruktur individuelle Profileinstellungen für die meisten Funktionen konfigurieren.

 

2. Alle älteren ICM2-Profilverwaltungs-APIs ändern Einstellungen systemweit und erfordern Administratorrechte. In Windows Vista werden in den meisten Jahren alle Benutzer in den LUA-Einstellungen (Least-Privileged User Account) ausgeführt, und Administratoren können die Berechtigungen selektiv erhöhen, um Anwendungen ausführen zu können, die systemweite Einstellungen ändern. In der WCS-Profilverwaltung können alle Benutzerprofileinstellungen im LUA-Kontext konfiguriert werden. Profilverwaltungsanwendungen können als LUA-Einstellungen ausgeführt werden, um ihren Umfang zu erhöhen und sicherzustellen, dass die Sicherheit des Systems nicht beeinträchtigt wird.

Die Profilverwaltung in Vista bietet die folgenden Verbesserungen gegenüber der älteren ICM2-Infrastruktur:

 

1. Sie ermöglicht die Profilzuordnung mit Geräten, Standardprofileinstellungen und die Enumeration von Profilen im benutzer- und systemweiten Bereich.

 

2. Die Installation eines Profils bleibt systemweit und erfordert Administratorrechte. Dies entspricht der Profilinstallation während der Geräteinstallation, da die Geräteinstallation systemweit erfolgt und Administratorrechte erfordert.

 

Ob Geräte aus dem LUA-Kontext installiert werden können, hängt davon ab, was für diese Geräteklasse unterstützt wird. In Vista ist es beispielsweise möglich, eine Druckerinstallation aus dem LUA-Kontext durchzuführen, wenn dem Benutzer berechtigungen zum Kopieren von Dateien in den Treiberspeicher von einem Domänenadministrator mithilfe von Treiberspeicherrichtlinien gewährt wurden. Die Infrastruktur für die Farbprofilverwaltung muss in dieser Hinsicht nichts Besonderes tun, da die Installation im Spoolerkontext erfolgt.

 

3. Das Ändern von Profileinstellungen im Benutzerbereich kann im LUA-Kontext erfolgen. Systemweite Änderungen erforderten Administratorrechte. Profilverwaltungsvorgänge, die das Lesen von Konfigurationsinformationen erfordern, können sowohl für benutzer- als auch systemweite Einstellungen im LUA-Kontext ausgeführt werden.

Der Profilverwaltungsbereich gibt den Umfang der ausgeführten Vorgänge an. entweder pro Benutzer oder systemweit.

Für jeden Vorgang wird angegeben, ob dies über den LUA-Kontext erfolgen kann. Wenn ein Vorgang im LUA-Kontext nicht ausgeführt werden kann, gibt die entsprechende Profilverwaltungs-API einen Fehler zurück, bei dem der Zugriff verweigert wurde. Anwendungen, die die API verwenden, z. B. Color Management Systemsteuerung, können es dem Benutzer ermöglichen, einen Erhöhten Aufschluss über den Administratorkontext zu geben (über OTS oder Consent UI), und dann die API aus dem Kontext mit erhöhten Rechten aufrufen, damit der Vorgang erfolgreich ist.



Vorgang

Profilverwaltungsbereich

Vorbedingung

Nachbedingung

Ausführbare Datei im LUA-Kontext

${ROWSPAN2}$Install Profil${REMOVE}$  

Systemweit

Profil kopiert, in das System installiert und zur Verwendung verfügbar. Das Profil ist im systemweiten und aktuellen Benutzerbereich für alle Benutzer aufzählbar.

Während der Installation des Gerätetreibers, gesteuert durch Treiberinstallationsrichtlinien. Andernfalls nein.

Aktueller Benutzer

Nicht unterstützt

${ROWSPAN2}$Uninstall Profil${REMOVE}$  

Systemweit

Das Profil wird im System installiert.

Das Profil wurde vom System deinstalliert und optional aus dem Profilspeicher gelöscht. Das Profil ist nicht mehr für die Verwendung verfügbar und in keinem Bereich aufzählbar.

Nein

Aktueller Benutzer

Nicht unterstützt

${ROWSPAN2}$Associate Profil mit Gerät${REMOVE}$  

Systemweit

Das Profil ist installiert und hat den Typ "STAMP" oder "CDMP".

Das Profil ist für die Verwendung mit dem Gerät durch alle Benutzer verfügbar. Es ist aufzählbar, im systemweiten Bereich und auch im aktuellen Benutzerbereich für alle Benutzer, wie dem Gerät zugeordnet.

Nein

Aktueller Benutzer

Das Profil ist installiert. Es spielt keine Rolle, ob das Profil dem Gerät bereits im systemweiten Bereich zugeordnet ist und vom Typ CAB oder CDMP ist.

Das Profil ist für die Verwendung mit dem Gerät durch den aktuellen Benutzer verfügbar. Sie ist nur im Aktuelle-Benutzer-Bereich aufzählbar (es sei denn, es gibt auch eine systemweite Zuordnung), die dem Gerät zugeordnet ist.

Ja

${ROWSPAN2}$Disassociate Profil von Gerät${REMOVE}$  

Systemweit

Das Profil ist dem Gerät im systemweiten Bereich zugeordnet und hat den Typ "STAMP" oder "CDMP".

Das Profil ist nicht mehr für die Verwendung verfügbar (mit Ausnahme von Benutzern, die diese Zuordnung auch in ihrem aktuellen Benutzerbereich haben). Sie ist im systemweiten Bereich nicht aufzählbar. Dies kann jedoch im Aktuelle-Benutzer-Bereich für einen Benutzer aufzählbar sein, der über diese Zuordnung in seinem Bereich verfügt.

Nein

Aktueller Benutzer

Das Profil ist dem Gerät im Aktuelle-Benutzer-Bereich zugeordnet (unabhängig davon, ob es dem systemweiten Bereich zugeordnet ist) und ist vom Typ CSV oder CDMP.

Das Profil ist für den aktuellen Benutzer nicht mehr für die Verwendung oder aufzählbar, wie es dem Gerät zugeordnet ist (es sei denn, es ist auch im systemweiten Bereich des Geräts zugeordnet).

Ja

${ROWSPAN2}$Set Profil für einen Typ (DMP oder STAMP) als Standard für ein Gerät${REMOVE}$  

Systemweit

Profil vom Typ "STAMP" oder "CDMP"

Das Profil wird standardmäßig für den jeweiligen Typ mit dem Gerät für alle Benutzer verwendet, mit Ausnahme von Benutzern, die diese Einstellung in ihrem aktuellen Benutzerbereich überschrieben haben. (Das Profil wird installiert und dem Gerätesystem zugeordnet, sofern dies nicht bereits der Fall ist.)

Nein

Aktueller Benutzer

Profil vom Typ "STAMP" oder "CDMP"

Das Profil wird standardmäßig für den jeweiligen Typ mit dem Gerät im Fall des aktuellen Benutzers verwendet, unabhängig von der systemweiten Standardeinstellung für diesen. (Das Profil wird installiert und dem Gerät für den aktuellen Benutzer zugeordnet, wenn dies nicht bereits der Fall ist.)

Ja, wenn das Profil bereits installiert ist

${ROWSPAN2}$Set Profil für einen Typ (KOMBIN, DMP, MIX, GMMP) und eine Untertypkombination als globaler Standardwert${REMOVE}$  

Systemweit

Geräte können nur MIT DEM- und CDMP-Profilen verknüpft werden.

Das Profil wird standardmäßig für den jeweiligen Typ verwendet. Benutzer können diese Einstellung im Aktuelle-Benutzer-Bereich überschreiben. (Das Profil wird installiert, wenn dies noch nicht der Fall ist.)

Nein

Aktueller Benutzer

Geräte können nur MIT DEM- und CDMP-Profilen verknüpft werden.

Das Profil wird standardmäßig für den jeweiligen Typ des aktuellen Benutzers verwendet. (Das Profil wird installiert, wenn dies noch nicht der Fall ist.)

Ja, wenn das Profil bereits installiert ist.

${ROWSPAN2}$Erase die Aktuelle-Benutzer-Außerkraftsetzung für eine bestimmte Standardprofileinstellung, sodass die Standardeinstellung des Systems immer verwendet wird (als Fallback) auch für den Aktuelle-Benutzer-Bereich.${REMOVE}$  

Systemweit

Nicht verfügbar

Aktueller Benutzer

Selbst für Abfragen von aktuellen Benutzern für Standardprofileinstellungen werden systemweite Einstellungen zur Verwendung zurückgegeben.

Ja

${ROWSPAN2}$Enumerate installierte Profile, die bestimmte Kriterien erfüllen (z. B. Geräteklasse, Profilklasse usw.). ${REMOVE}$  

Systemweit

Für Geräte können nur DIE PROFILE UND CDMP zugeordnet und aufzählt werden.

Profile, die installiert sind und die angegebenen Kriterien im systemweiten Bereich erfüllen, werden aufzählt.

Ja

Aktueller Benutzer

Geräte können nur MIT UNDM-Profilen verknüpft und daher für Geräte aufzählt werden.

Profile, die installiert sind und die angegebenen Kriterien im systemweiten Bereich erfüllen, werden aufzählt.

Ja

${ROWSPAN2}$Enumerate Profile, die einem bestimmten Gerät zugeordnet sind, das bestimmte Kriterien erfüllt, z. B. Geräteklasse und Profilklasse${REMOVE}$  

Systemweit

Für Geräte können nur DIE PROFILE UND CDMP zugeordnet und aufzählt werden.

Profile, die dem Gerät im systemweiten Bereich zugeordnet sind und die angegebenen Kriterien im systemweiten Bereich erfüllen, werden aufzählt.

Ja

Aktueller Benutzer

Für Geräte können nur DIE PROFILE UND CDMP zugeordnet und aufzählt werden.

Profile, die als dem Gerät zugeordnet im Aktuelle-Benutzer-Bereich verfügbar sind, die die systemweiten Zuordnungen enthalten und die angegebenen Kriterien im Aktuelle-Benutzer-Bereich erfüllen, werden aufzählt.

Ja



 

Die gültigen Farbprofiltypen werden von der COLORPROFILETYPE-Enumeration bereitgestellt.

Die gültigen Farbprofiluntertypen werden von der COLORPROFILESUBTYPE-Enumeration bereitgestellt.

Die gültigen Kombinationen aus Profiltyp und Untertyp sind in der folgenden Tabelle dargestellt.



COLORPROFILETYPE 

Gültige COLORPROFILESUBTYPE-DATEI

Hinweise

Gerätestandard

Globaler Standardwert

Beabsichtigte Verwendung

Beabsichtigte Verwendung

\_CPT- UND CPT-CPT-

CPST \_ NONE

Abrufen/Festlegen des einem Gerät zugeordneten DEFAULT-PROFILs

CPST \_ RGBWorkingSpace oder CPST \_ CustomWorkingSpace

Dient zum Abrufen/Festlegen des RGB-Profils als globales RGB- oder benutzerdefiniertes Arbeitsbereichsprofil. Siehe Hinweis.

Die COLORPROFILETYPE \_ CPT- und \_ CPT-DMP-Dateien schließen sich gegenseitig aus. Das Standardfarbprofil, das Sie für einen bestimmten Arbeitsbereich (RGB oder Benutzerdefiniert) festlegen, kann entweder ein RGB-Profil oder ein DMP-Profil sein, aber nicht beides.

CPT \_ DMP

CPST \_ NONE

Abrufen/Festlegen des einem Gerät zugeordneten DMP-Standardprofils

CPST \_ RGBWorkingSpace oder CPST \_ CustomWorkingSpace

Abrufen/Festlegen des DMP-Profils als globales RGB- oder benutzerdefiniertes Arbeitsbereichsprofil. Siehe Hinweis.

Die COLORPROFILETYPE \_ CPT- und \_ CPT-DMP-Dateien schließen sich gegenseitig aus. Das Standardfarbprofil, das Sie für einen bestimmten Arbeitsbereich (RGB oder Benutzerdefiniert) festlegen, kann entweder ein RGB-Profil oder ein DMP-Profil sein, aber nicht beides.



 

> [!Note]  
> Wenn WcsSetDefaultColorProfile aufgerufen wird, um ein DMP-Profil als Standardprofil für den RGB-Arbeitsbereich oder einen benutzerdefinierten Arbeitsbereich festzulegen, ist nur ein DMP-Profil vom Typ RGBVirtualDevice, RGB oder CRT gültig.
>
>  
>
> Wenn WcsSetDefaultColorProfile aufgerufen wird, um ein RGB-Profil als Standardprofil für den RGB-Arbeitsbereich oder einen benutzerdefinierten Arbeitsbereich festzulegen, ist nur einWK-Profil gültig, dessen Klasse "spac" oder "disp" ist und dessen Farbraum "RGB" ist.

 

Die Architektur wurde gemäß den Anforderungen der Vorgänge entworfen, die in den obigen Enumerationen und Tabellen erwähnt werden.

### <a name="profile-management-public-api-layer"></a>Öffentliche API-Ebene für die Profilverwaltung

Da der Profilverwaltungsbereich von älteren ICM2-APIs nicht unterstützt wird, ist ein neuer Satz von WCS-Profilverwaltungs-APIs erforderlich, der den Profilverwaltungsbereich als systemweiten oder aktuellen Benutzer definiert. ? Legacy-ICM2-APIs werden aus Gründen der Abwärtskompatibilität weiterhin unterstützt und arbeiten mit dem Profilverwaltungsbereich, der für den Aufruf implizit ist. o ICM2-APIs, die im Aktuelle-Benutzer-Bereich funktionieren? Dies gilt für Vorgänge, die sowohl für den systemweiten als auch für den aktuellen Benutzerbereich in der WCS-Profilverwaltung unterstützt werden. Legacy-ICM2-APIs rufen neue WCS-APIs mit Profilverwaltungsbereich als aktueller Benutzer auf. Dies ist aus Benutzersicht sinnvoll, da dies benutzerspezifische Einstellungen von Legacyanwendungen ermöglicht und auch die meisten Vorgänge im LUA-Kontext ausführt. o ICM2-APIs, die im systemweiten Bereich funktionieren? Dies gilt für Vorgänge (Installieren von Profilen und Deinstallieren von Profilen), die nur den systemweiten Bereich unterstützen. Es werden keine neuen WCS-Profilverwaltungs-APIs erstellt, und vorhandene APIs können geändert werden.

Die zugrunde liegenden Implementierungen der Profilverwaltungsvorgänge arbeiten mit den folgenden Konfigurationsdatenentitäten, um den Kontext für Farbverarbeitungsalgorithmen zu erstellen, um Farbverwaltungsfunktionen bereitzustellen. Dabei handelt es sich entweder um gerätespezifische oder globale (geräteunabhängige) Einstellungen. o Gerätespezifische Konfigurationsdaten: ? Liste der Profile, die einem bestimmten Gerät zugeordnet sind. ? Standardprofil für verschiedene Profiltypen, die einem Gerät zugeordnet sind. ? Abgleichsmodus von Profilen, die für die Enumeration verwendet werden. o Globale Konfigurationsdaten: ? Liste der im System installierten Profile. ? Globales Standardprofil für verschiedene Profiltypen. ? Die zugrunde liegenden Implementierungen des Konfigurationsdatenspeichers übernehmen den Speicherbereich für Konfigurationsdaten (geräteunabhängig oder gerätespezifisch), die entweder systemweit oder aktuell sein können. Dies unterscheidet sich vom Bereich der Profilverwaltung. Ein Vorgang mit dem Verwaltungsbereich des aktuellen Benutzerprofils kann dazu führen, dass ein Lesevorgang aus einem systemweiten Speicherbereich durchgeführt wird, wenn die aktuelle Benutzereinstellung für diesen Vorgang nicht vorhanden ist. ? Die ICM2/WCS-API-Schicht ruft in dieser Speicherebene zum Abrufen und Festlegen von Daten mit entsprechendem Speicherbereich auf. Die Speicherebene ist für den Profilverwaltungsbereich transparent. Die Logik zum Kombinieren von Daten aus aktuellen und systemweiten Speicherbereichen, um eine Konfiguration entsprechend dem vom API-Aufrufer angegebenen Profilverwaltungsbereich zu erstellen oder zu aktualisieren. Diese Logik ist in der ICM2/WCS-API-Ebene vorhanden.

### <a name="device-specific-storage-layer"></a>Gerätespezifische Speicherebene

Der Speicher für verschiedene Geräteklassen wie Drucken, Erfassen oder Anzeigen kann sich voneinander unterscheiden. Konfigurationsdaten für ein Druckgerät müssen beispielsweise mithilfe von Standarddruck-APIs wie SetPrinterDataEx und GetPrinterDataEx gespeichert werden, damit die Profile kopiert und Einstellungen während der Point-and-Print-Verbindung auf einen Clientcomputer übertragen werden können. ? Diese Ebene exportiert Funktionen zum Öffnen des Speichers, Abrufen von Daten, Festlegen von Daten und Schließen des Speichers mithilfe allgemeiner vordefinierter Schnittstellen, sodass die Speicherebene der Profilverwaltungskonfiguration sie aufrufen kann, während sie transparent für die Art und Weise sind, wie die Daten für dieses Gerät gespeichert werden.

Diese Architektur wird anhand des folgenden Diagramms veranschaulicht.



Öffentliche API-Ebene für die Profilverwaltung

${ROWSPAN2}$Legacy ICM2-APIs für Vorgänge, die nur den systemweiten Profilverwaltungsbereich in Vista unterstützen (Installieren, Deinstallieren und Abrufen des Farbverzeichnisses). Sie rufen die Konfigurationsspeicherebene mit dem entsprechenden Speicherbereich auf.${REMOVE}$  

Legacy-ICM2-API für Vorgänge, die sowohl den systemweiten als auch den aktuellen Benutzerprofilverwaltungsbereich in Vista unterstützen (alle Vorgänge außer installation, uninstall und get color directory). Sie funktionieren implizit für den Aktuelle-Benutzer-Bereich und rufen eine neue WCS-API mit Profilverwaltungsbereich als aktueller Benutzer auf.

Neue WCS-API mit systemweiter und Unterstützung der Profilverwaltung für aktuelle Benutzer. Sie rufen die Konfigurationsspeicherebene mit entsprechendem Speicherbereich auf.



 



Profilverwaltungskonfiguration Storage Ebene

Geräteunabhängige globale Konfigurationsroutinen

Gerätespezifische Konfigurationsroutinen

${ROWSPAN3}$Profile Installation und geräteunabhängige Verwaltung von Standardprofileinstellungen, unterstützt im systemweiten und aktuellen Benutzerspeicherbereich.${REMOVE}$  

Gerätezuordnung und gerätespezifische Verwaltung von Standardprofileinstellungen, die im systemweiten und aktuellen Benutzerspeicherbereich unterstützt werden.

Device-Specific Storage Ebene

Drucken eines bestimmten Speichers

Anzeigen eines bestimmten Speichers

Erfassen eines bestimmten Speichers



 

Legacy-ICM2-APIs für Vorgänge, die nur den systemweiten Profilverwaltungsbereich in Vista unterstützen, haben keine Verhaltensänderungen. Installations- und Deinstallationsvorgänge fallen in diese Kategorie.

Ältere ICM2-APIs für Vorgänge, die sowohl den systemweiten als auch den Verwaltungsbereich für aktuelle Benutzerprofile unterstützen, haben ihr Verhalten geändert, um Einstellungen für aktuelle Benutzer abzufragen und zu konfigurieren. Alle Vorgänge außer der Installation und Deinstallation fallen in diese Kategorie.

 

 




