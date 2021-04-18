---
title: Profilverwaltungsfunktionen
description: Profilverwaltungsfunktionen
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bild Farbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCs, Funktionen
- Windows Color System (WCS), profile
- WCS (Windows Color System), profile
- Bildfarben Verwaltung, profile
- Farbverwaltung, profile
- Farben, profile
- WCS-Referenz, profile
- Referenz für WCs, profile
- Profilverwaltung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106371802"
---
# <a name="profile-management-functions"></a>Profilverwaltungsfunktionen

## <a name="profile-management-functions"></a>Profilverwaltungsfunktionen

Die folgenden API-Funktionen sind für die Profilverwaltung nützlich.



| Funktion                                                                               | BESCHREIBUNG                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Associatecolorprofilewithdevicew**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Ordnet ein angegebenes Farbprofil einem angegebenen Gerät zu.                                                              |
| [**Erkreateprofilefromlogcolorspacew**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Konvertiert einen logischen [Farbraum](c.md) in ein [Geräte Profil](d.md). |
| [**Disassociatecolorprofilefromdevicew**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Trennt ein angegebenes Farbprofil einem angegebenen Gerät auf einem angegebenen Computer. |
| [**Enumcolorprofilesw**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Listet alle Profile auf, die die angegebenen enumerationskriterien erfüllen. |
| [**Getcolordirector**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Ruft den Pfad des Windows-Farb Verzeichnisses auf einem angegebenen Computer ab. |
| [**Getde vicegammaramp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Ruft die Gamma-Rampe von der direkten Farbanzeige Boards ab.                                                                                                |
| [**Getstandardcolorspaceprofilew**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Ruft das Farbprofil ab, das für den angegebenen Standard [Farbraum](c.md)registriert ist. |
| [**Installcolorprofilew**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installiert ein bestimmtes Profil für die Verwendung auf einem angegebenen Computer. Das Profil wird auch in das Farb Verzeichnis kopiert. |
| [**Registercmmw**](/windows/win32/api/icm/nf-icm-registercmmw) | Ordnet einen angegebenen Identifikations Wert der angegebenen CMM-dll (Dynamic Link Library) des Farb Verwaltungs Moduls zu. Wenn diese ID in einem Farbprofil angezeigt wird, kann Windows den entsprechenden CMM-Code suchen, um eine Transformation zu erstellen. |
| [**Setde vicegammaramp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Legt die Gamma-Rampe für die Anzeige Boards der direkten Farbe fest.                                                                                                  |
| [**Setstandardcolorspaceprofilew**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registriert ein angegebenes Profil für einen angegebenen Standard [Farbraum](c.md). Das Profil kann mithilfe von [getstandardcolorspaceprofilew](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew)abgefragt werden. |
| [**Uninstallcolorprofilew**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Entfernt ein angegebenes Farbprofil von einem angegebenen Computer. Zugehörige Dateien werden optional aus dem System gelöscht. |
| [**Unregistercmmw**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Trennt einen angegebenen ID-Wert aus einer angegebenen Dynamic Link Library (CMM-dll) des Farb Verwaltungs Moduls. |
| [**Wcsassociatecolorprofilewithdevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Ordnet ein angegebenes WCS-Farbprofil einem angegebenen Gerät zu.                                                                                    |
| [**Wcscreateiccprofile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Konvertiert ein WCS-Profil in ein-ICC-Profil.                                                                                                          |
| [**Wcsdisassociatecolorprofilefromdevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Trennt ein angegebenes WCS-Farbprofil einem angegebenen Gerät auf einem angegebenen Computer.                                                         |
| [**Wcsenaufcolorprofiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Listet alle Farbprofile auf, die die enumerationskriterien im angegebenen Profil Verwaltungsbereich erfüllen.                                       |
| [**Wcsenaufcolorprofilessize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | Gibt die Größe (in Bytes) des Puffers zurück, der von der Funktion [**wcsenumcolorprofiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) zum Auflisten von Farbprofilen benötigt wird. |
| [**Wcsgetdefaultcolorprofile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | Ruft das Standard Farbprofil für ein Gerät oder den geräteunabhängigen Standardwert ab, wenn das Gerät nicht angegeben ist.                                  |
| [**Wcsgetdefaultcolorprofilesize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Gibt die Größe (in Bytes) des standardmäßigen Farbprofil namens für ein Gerät zurück, einschließlich des **null** -Terminator.                                       |
| [**Wcsgetdefaultrenderingintent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Ruft die standardmäßige renderabsicht im angegebenen Profil Verwaltungsbereich ab.                                                                    |
| [**Wcsgetuseperuserprofiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Bestimmt, ob der Benutzer eine benutzerspezifische Profil Zuordnungs Liste für das angegebene Gerät verwendet hat.                                          |
| [**Wcsopeincolorprofilew**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Erstellt ein Handle für ein angegebenes Farbprofil.                                                                                                       |
| [**Wcssetdefaultcolorprofile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Legt den Standardnamen des Farbprofils für den angegebenen Profiltyp im angegebenen Profil Verwaltungsbereich fest.                                         |
| [**Wcssetdefaultrenderingintent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Legt die Standard-renderabsicht im angegebenen Profil Verwaltungsbereich fest.                                                                         |
| [**Wcssetuseperuserprofiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Ermöglicht es dem Benutzer anzugeben, ob eine Profil Zuordnungs Liste pro Benutzer für das angegebene Gerät verwendet werden soll.                                              |



 

## <a name="profile-consumption-functions"></a>Profil Nutzungs Funktionen

Bei den APIs für die Profil Nutzung handelt es sich um APIs in ICM2, die die XML-Profile, Profil Handles oder renderingintents von ICC oder WCS als Parameter und eine Reihe neuer APIs für die WCS-Profil Unterstützung für den Anwendungs Farb Verwaltungs Code verwenden.

 

## <a name="profiles-and-profile-management-functions"></a>Profile und Profil Verwaltungsfunktionen

Der Profil Verwaltungs Workflow basiert auf vorhandenen ICM2-APIs, die erweitert werden, um zusätzliche Funktionen zum Überarbeiten von Anwendungscode bereitzustellen.

Profile enthalten Informationen, die von Farb Verarbeitungsalgorithmen verwendet werden, um die Farbe zwischen verschiedenen Farbräumen zu übersetzen. Mit der Profilverwaltung können Sie Abfragen und angeben, welche Profile in verschiedenen Phasen vom Farb Verarbeitungsmodell verwendet werden, um die Farbausgabe verschiedener Peripheriegeräte mit unterschiedlichen Farb Merkmalen zu verwalten.

Die Profilverwaltung bietet die folgenden Funktionen:

 

1. Installieren von Farbprofilen für die Verwendung im System.

 

2. Zuordnen eines oder mehrerer installierter Farbprofile zu einem bestimmten Gerät.

 

3. Auswählen eines Standard Farbprofils eines bestimmten Typs in den Profilen, die in einer bestimmten Phase der Farbverarbeitung zur Verwendung verfügbar sind. Dies kann für ein Gerät in den zugeordneten Profilen oder zwischen den Profilen, die im System installiert sind, und nicht für gerätespezifisch sein.

 

4. Auflisten von Farbprofilen, die bestimmte Kriterien zwischen den im System installierten Profilen erfüllen.

Die Dateinamen Erweiterungen für WCS-Profile sind ". CDMP" für DMPs, ". Camp" für CAMPs und ". GMMP" für gmmps.

 

**Profilverwaltung pro Benutzer und Aktivierung der Ausführung im Lua-Kontext**

Das Ziel des im aktuellen Dokument beschriebenen Entwurfs ist Folgendes:

 

1. Die Legacy-ICM2-Implementierung bietet keine Unterstützung für die Profilverwaltung pro Benutzer. Verschiedene Benutzer können nicht über eigene Profileinstellungen verfügen. In Vista ermöglicht die WCS-Profil Verwaltungsinfrastruktur Benutzern, individuelle Profileinstellungen für die meisten Funktionen zu konfigurieren.

 

2. Alle veralteten ICM2-Profilverwaltungs-APIs ändern systemweite Einstellungen und erfordern Administratorrechte. In Windows Vista führen alle Benutzer in den meisten Fällen die Einstellungen mit den geringsten Berechtigungen für Benutzerkonten (LUA) aus, und Administratoren können die Berechtigung selektiv erhöhen, um Anwendungen auszuführen, die systemweite Einstellungen ändern. In der WCS-Profilverwaltung können alle Profileinstellungen pro Benutzer im Lua-Kontext konfiguriert werden. Profil Verwaltungs Anwendungen können als Lua-Einstellungen ausgeführt werden, wodurch der Verwendungs Umfang erhöht und sichergestellt wird, dass die Sicherheit des Systems nicht beeinträchtigt wird.

Die Profilverwaltung in Vista bietet die folgenden Verbesserungen gegenüber der Legacy-ICM2-Infrastruktur:

 

1. Sie ermöglicht die Zuordnung von Profilen zu Geräten, Standardprofil Einstellungen und die Enumeration von Profilen sowohl im Benutzer-als auch im systemweiten Bereich.

 

2. Die Installation eines Profils bleibt systemweit und erfordert Administratorrechte. Dies ist mit der Profil Installation während der Geräteinstallation konsistent, da die Geräteinstallation systemweit ist und Administratorrechte erfordert.

 

Ob Geräte aus dem Lua-Kontext installiert werden können, ist besonders für die unterstützte Geräteklasse von Bedeutung. In Vista ist es beispielsweise möglich, die Drucker Installation aus dem Lua-Kontext durchzuführen, wenn dem Benutzer die Berechtigung erteilt wurde, Dateien von einem Domänen Administrator mithilfe von Treiber Speicher Richtlinien in den Treiber Speicher zu kopieren. Die Infrastruktur für die Farbprofilverwaltung muss in diesem Zusammenhang nichts Besonderes tun, da die Installation im spoolerkontext erfolgt.

 

3. Das Ändern von Profileinstellungen im Benutzer bezogenen Bereich kann im Lua-Kontext erfolgen. systemweite Änderungen erforderten Administratorrechte. Profil Verwaltungsvorgänge, die das Lesen von Konfigurationsinformationen erfordern, können im Lua-Kontext sowohl für benutzerspezifische als auch für systemweite Einstellungen durchgeführt werden.

Profil Verwaltungsbereich gibt den Umfang der durchgeführten Vorgänge an. entweder pro Benutzer oder systemweit.

Für jeden Vorgang wird angegeben, ob Sie über den Lua-Kontext ausgeführt werden kann. Wenn ein Vorgang im Lua-Kontext nicht ausgeführt werden kann, gibt die entsprechende Profilverwaltungs-API einen Fehler mit dem Zugriff verweigert zurück. Anwendungen, die die API verwenden, z. b. die System Steuerungs Option "Farbverwaltung", können es Benutzern ermöglichen, die Rechte auf den administrativen Kontext zu erhöhen (mithilfe von OTS oder der Zustimmungs Benutzeroberfläche), und dann die API aus dem erweiterten Kontext aufzurufen, damit der Vorgang erfolgreich



Vorgang

Profil Verwaltungsbereich

Voraussetzung

Nach Bedingung

Ausführbare Datei im Lua-Kontext

$ {ROWSPAN2} $install Profil $ {Remove} $  

System weit

Das Profil wurde kopiert, im System installiert und ist zur Verwendung verfügbar. Das Profil kann im systemweiten und aktuellen Benutzerbereich für alle Benutzer aufgelistet werden.

Bei der Installation des Gerätetreibers unterliegen Richtlinien für die Treiberinstallation. Andernfalls nein.

Aktueller Benutzer

Nicht unterstützt

$ {ROWSPAN2} $Uninstall Profil $ {Remove} $  

System weit

Das Profil ist im System installiert.

Das Profil wurde vom System deinstalliert und optional aus dem Profil Speicher gelöscht. Das Profil ist nicht mehr zur Verwendung verfügbar und kann in keinem Bereich aufgelistet werden.

Nein

Aktueller Benutzer

Nicht unterstützt

$ {ROWSPAN2} $Associate Profil mit Gerät $ {Remove} $  

System weit

Profil ist installiert und hat den Typ "ICC" oder "CDMP".

Das Profil ist für die Verwendung mit dem Gerät durch alle Benutzer verfügbar. Sie ist für alle Benutzer, die dem Gerät zugeordnet sind, im systemweiten Bereich und auch im Gültigkeitsbereich des aktuellen Benutzers Aufzähl Bar.

Nein

Aktueller Benutzer

Das Profil ist installiert. Es spielt keine Rolle, ob das Profil bereits dem Gerät im systemweiten Gültigkeitsbereich zugeordnet ist und den Typ "ICC" oder "CDMP" hat.

Das Profil ist für die Verwendung mit dem Gerät durch den aktuellen Benutzer verfügbar. Es ist nur im Gültigkeitsbereich des aktuellen Benutzers Aufzähl Bar (es sei denn, es gibt auch eine systemweite Zuordnung), die dem Gerät zugeordnet ist.

Ja

$ {ROWSPAN2} $Disassociate Profil von Gerät $ {Remove} $  

System weit

Das Profil ist dem Gerät im systemweiten Gültigkeitsbereich zugeordnet und hat den Typ "ICC" oder "CDMP".

Das Profil ist nicht mehr zur Verwendung verfügbar (mit Ausnahme von Benutzern, die diese Zuordnung in Ihrem aktuellen Benutzerbereich aufweisen). Sie kann nicht im systemweiten Gültigkeitsbereich aufgelistet werden. Sie kann jedoch im Gültigkeitsbereich des aktuellen Benutzers aufgeführt werden, für einen Benutzer, der diese Zuordnung im Gültigkeitsbereich hat.

Nein

Aktueller Benutzer

Das Profil ist dem Gerät im Gültigkeitsbereich des aktuellen Benutzers zugeordnet (unabhängig davon, ob es im systemweiten Gültigkeitsbereich zugeordnet ist) und hat den Typ "ICC" oder "CDMP".

Das Profil kann nicht mehr verwendet werden, oder es kann vom aktuellen Benutzer als dem Gerät zugeordnetes Element nicht mehr verwendet werden (es sei denn, es ist auch im systemweiten Gültigkeitsbereich des Geräts zugeordnet).

Ja

$ {ROWSPAN2} $Set Profil für einen Typ (DMP oder ICC) als Standardwert für ein Gerät $ {Remove} $  

System weit

Profil ist vom Typ "ICC" oder "CDMP"

Das Profil wird standardmäßig für den jeweiligen Typ mit dem Gerät für alle Benutzer verwendet, mit Ausnahme derjenigen, die diese Einstellung im aktuellen Benutzerbereich überschrieben haben. (Das Profil wird installiert und dem Gerätesystem breit zugeordnet, wenn dies nicht bereits der Fall ist.)

Nein

Aktueller Benutzer

Profil ist vom Typ "ICC" oder "CDMP"

Das Profil wird standardmäßig für den jeweiligen Typ mit dem Gerät im Falle des aktuellen Benutzers verwendet, und zwar unabhängig vom systemweiten Standardwert für diesen. (Das Profil wird installiert und dem Gerät für den aktuellen Benutzer zugeordnet, wenn dies nicht bereits der Fall ist.)

Ja, wenn das Profil bereits installiert ist

$ {ROWSPAN2} $Set Profil für einen Typ ("ICC", "DMP", "Camp", "GMMP") und eine Untertyp Kombination als globaler Standardwert $ {Remove} $  

System weit

Geräte können nur die "ICC"-und "CDMP"-Profile zugeordnet werden.

Das Profil wird standardmäßig für den jeweiligen Typ verwendet. Benutzer können diese Einstellung im Gültigkeitsbereich des aktuellen Benutzers außer Kraft setzen. (Das Profil ist installiert, wenn dies nicht bereits der Fall ist.)

Nein

Aktueller Benutzer

Geräte können nur die "ICC"-und "CDMP"-Profile zugeordnet werden.

Das Profil wird standardmäßig für den jeweiligen Typ des aktuellen Benutzers verwendet. (Das Profil ist installiert, wenn dies nicht bereits der Fall ist.)

Ja, wenn das Profil bereits installiert ist.

$ {ROWSPAN2} $Erase die Überschreibung des aktuellen Benutzers für eine bestimmte Standardprofil Einstellung, sodass der System Standard immer als Fallback für den aktuellen Benutzerbereich verwendet wird. $ {Remove} $  

System weit

Nicht verfügbar

Aktueller Benutzer

Auch für aktuelle Benutzer Abfragen von Standardprofil Einstellungen werden systemweite Einstellungen zur Verwendung zurückgegeben.

Ja

$ {ROWSPAN2} $Enumerate installierte Profile, die bestimmte Kriterien erfüllen (z. b. Geräteklasse, Profilklasse usw.) $ {Remove} $  

System weit

Nur die "ICC"-und "CDMP"-Profile können für Geräte zugeordnet und aufgelistet werden.

Profile, die installiert sind und die angegebenen Kriterien im systemweiten Gültigkeitsbereich erfüllen, werden aufgezählt.

Ja

Aktueller Benutzer

Den Geräten können nur die-und-CDMP-Profile zugeordnet und somit für Geräte aufgelistet werden.

Profile, die installiert sind und die angegebenen Kriterien im systemweiten Gültigkeitsbereich erfüllen, werden aufgezählt.

Ja

$ {ROWSPAN2} $Enumerate Profile, die einem bestimmten Gerät zugeordnet sind, das bestimmte Kriterien erfüllt, z. b. Geräteklasse und Profilklasse $ {Remove} $  

System weit

Nur die "ICC"-und "CDMP"-Profile können für Geräte zugeordnet und aufgelistet werden.

Profile, die dem Gerät im systemweiten Gültigkeitsbereich zugeordnet sind und die angegebenen Kriterien im systemweiten Gültigkeitsbereich erfüllen, werden aufgezählt.

Ja

Aktueller Benutzer

Nur die "ICC"-und "CDMP"-Profile können für Geräte zugeordnet und aufgelistet werden.

Profile, die dem Gerät im Gültigkeitsbereich des aktuellen Benutzers zugeordnet sind, einschließlich der systemweiten Zuordnungen, die die angegebenen Kriterien im aktuellen Benutzerbereich erfüllen, werden aufgezählt.

Ja



 

Die gültigen Farbprofil Typen werden von der colorprofiletype-Enumeration bereitgestellt.

Die gültigen Farbprofil-Untertypen werden von der colorprofilesubtype-Enumeration bereitgestellt.

In der folgenden Tabelle sind die gültigen Profiltyp-/Untertyp Kombinationen aufgeführt.



COLORPROFILETYPE 

Gültiger colorprofilesubtype

Notizen

Gerätestandard

Globaler Standardwert

Beabsichtigte Verwendung

Beabsichtigte Verwendung

CPT- \_ ICC

CPST \_ None

Mit einem Gerät verknüpften Standard-ICC-Profil erhalten/festlegen

CPST \_ rgbworkingspace oder CPST \_ customworkingspace

Sie sollten das ICC-Profil als globales RGB-oder benutzerdefiniertes Arbeitsplatz Profil festlegen. Siehe Hinweis.

Der colorprofiletype CPT \_ -ICC und der CPT- \_ DMP schließen sich gegenseitig aus. Das Standard Farbprofil, das Sie für einen bestimmten Arbeitsbereich festlegen (RGB oder Custom), kann entweder ein ICC-Profil oder ein DMP-Profil sein, aber nicht beides.

CPT- \_ DMP

CPST \_ None

Standard-DMP-Profil, das einem Gerät zugeordnet ist, erhalten/festlegen

CPST \_ rgbworkingspace oder CPST \_ customworkingspace

Legen Sie das DMP-Profil als globales RGB-oder benutzerdefiniertes Arbeitsplatz Profil fest. Siehe Hinweis.

Der colorprofiletype CPT \_ -ICC und der CPT- \_ DMP schließen sich gegenseitig aus. Das Standard Farbprofil, das Sie für einen bestimmten Arbeitsbereich festlegen (RGB oder Custom), kann entweder ein ICC-Profil oder ein DMP-Profil sein, aber nicht beides.



 

> [!Note]  
> Wenn wcssetdefaultcolorprofile aufgerufen wird, um ein DMP-Profil als Standardprofil für den RGB-Arbeitsbereich oder einen benutzerdefinierten Arbeitsbereich festzulegen, ist nur ein DMP-Profil vom Typ rgbvirtualdevice, LCD oder CRT gültig.
>
>  
>
> Wenn wcssetdefaultcolorprofile aufgerufen wird, um ein ICC-Profil als Standardprofil für den RGB-Arbeitsbereich oder einen benutzerdefinierten Arbeitsbereich festzulegen, ist nur ein ICC-Profil, dessen Klasse "SPAC" oder "DISP" ist und dessen Farbraum "RGB" ist, gültig.

 

Die Architektur basiert auf den Anforderungen der Vorgänge, die in den obigen Enumerationen und Tabellen erwähnt wurden.

### <a name="profile-management-public-api-layer"></a>Ebene der öffentlichen API der Profilverwaltung

Da der Profil Verwaltungsbereich von Legacy-ICM2-APIs nicht unterstützt wird, ist ein neuer Satz von WCS-Profilverwaltungs-APIs erforderlich, der den Profil Verwaltungsbereich als systemweit oder aktueller Benutzer definiert. ? Ältere ICM2-APIs werden weiterhin aus Gründen der Abwärtskompatibilität unterstützt und arbeiten im Profil Verwaltungsbereich, der für den-Befehl implizit ist. o ICM2-APIs, die im Gültigkeitsbereich des aktuellen Benutzers funktionieren? Dies gilt für Vorgänge, die für den systemweiten und aktuellen Benutzerbereich in der WCS-Profilverwaltung unterstützt werden. Ältere ICM2-APIs werden für neue WCS-APIs mit Profil Verwaltungsbereich als aktueller Benutzer aufgerufen. Dies ergibt sich aus der Sicht des Benutzers, da dies benutzerspezifische Einstellungen von Legacy Anwendungen und die meisten Vorgänge im Lua-Kontext ermöglicht. o ICM2-APIs, die im systemweiten Bereich funktionieren? Dies gilt für Vorgänge (Installations Profile und Deinstallations Profile), die nur den systemweiten Bereich unterstützen. Es werden keine neuen APIs für die WCS-Profilverwaltung erstellt, und vorhandene APIs können nicht geändert werden.

Die zugrunde liegenden Implementierungen der Profil Verwaltungsvorgänge funktionieren in den folgenden Konfigurationsdaten Entitäten, um den Kontext für farbverarbeitungs Algorithmen zum Bereitstellen von Farb Verwaltungsfunktionen zu erstellen. Sie sind entweder gerätespezifische oder globale (geräteunabhängige) Einstellungen. gerätespezifische Konfigurationsdaten:? Liste der Profile, die einem bestimmten Gerät zugeordnet sind. ? Standardprofil für verschiedene Profiltypen, die einem Gerät zugeordnet sind. ? Abgleichsmodus für die Enumeration. Globale Konfigurationsdaten:? Liste der im System installierten Profile. ? Globales Standardprofil für verschiedene Profiltypen. ? Die zugrunde liegenden Implementierungen der Konfigurationsdaten Speicherung übernehmen den Speicherbereich für Konfigurationsdaten (entweder Geräte unabhängig oder gerätespezifisch), bei denen es sich entweder um systemweite oder den aktuellen Benutzer handeln kann. Dies unterscheidet sich vom Profil Verwaltungsbereich. Ein Vorgang mit dem Profil Verwaltungsbereich aktueller Benutzer kann einen Lesevorgang aus einem systemweiten Speicherbereich bewirken, wenn die aktuelle Benutzereinstellung für diesen Vorgang nicht vorhanden ist. ? Die ICM2/WCS-API-Schicht ruft in dieser Speicher Ebene auf, um Daten mit dem entsprechenden Speicherbereich zu erhalten und festzulegen. Die Speicher Ebene ist für den Profil Verwaltungsbereich transparent. Die Logik für das Kombinieren von Daten aus aktuellen Benutzer-und systemweiten Speicherbereichen zum Erstellen oder Aktualisieren einer Konfiguration gemäß dem Profil Verwaltungsbereich, der vom API-Aufrufer festgelegt wird. Diese Logik ist in der ICM2/WCS-API-Ebene vorhanden.

### <a name="device-specific-storage-layer"></a>Gerätespezifische Speicher Ebene

Der Speicher für verschiedene Klassen von Geräten, wie z. b. Print, Capture oder Display, kann sich voneinander unterscheiden. Beispielsweise müssen Konfigurationsdaten für ein Druck Gerät mithilfe von standardmäßigen Druck-APIs, wie z. b. setprinterdataex und getprinterdataex, gespeichert werden, damit die Profile kopiert werden können und Einstellungen während der Point-and-Print-Verbindung an einen Client Computer übertragen werden. ? Diese Schicht exportiert Funktionen zum Öffnen von speichern, Abrufen von Daten, Festlegen von Daten und Schließen des Speichers mithilfe allgemeiner vordefinierter Schnittstellen, sodass die Speicher Ebene der Profil Verwaltungs Konfiguration aufgerufen werden kann, während Sie transparent ist, wie die Daten für das Gerät gespeichert werden.

Diese Architektur wird anhand des folgenden Diagramms veranschaulicht.



Ebene der öffentlichen API der Profilverwaltung

$ {ROWSPAN2} $Legacy ICM2-APIs für Vorgänge, die nur den systemweiten Profil Verwaltungsbereich in Vista unterstützen (installieren, deinstallieren und das Farb Verzeichnis erhalten). Die Konfigurations Speicher Ebene wird mit dem entsprechenden Speicherbereich aufgerufen. $ {Remove} $  

Ältere ICM2-API für Vorgänge, die sowohl den systemweiten als auch den aktuellen Profil Verwaltungsbereich in Vista unterstützen (alle Vorgänge außer "Install", "Uninstall" und "Get Color Directory"). Sie arbeiten implizit mit dem aktuellen Benutzerbereich und wenden eine neue WCS-API mit Profil Verwaltungsbereich als aktueller Benutzer an.

Neue WCS-API mit Unterstützung für systemweite und aktuelle Profil Verwaltungsbereiche. Sie bezeichnen die Konfigurations Speicher Ebene mit dem entsprechenden Speicherbereich.



 



Speicher Ebene für die Profil Verwaltungs Konfiguration

Geräteunabhängige globale Konfigurations Routinen

Gerätespezifische Konfigurations Routinen

$ {ROWSPAN3} $profile Installation und geräteunabhängige Standardprofil Einstellungen-Verwaltung, unterstützt im systemweiten und aktuellen Benutzerspeicher Bereich. $ {Remove} $  

Geräte Zuordnung und gerätespezifische Standardprofil Einstellungen-Verwaltung, unterstützt im systemweiten und aktuellen Benutzerspeicher Bereich.

Device-Specific-Speicher Ebene

Drucken eines bestimmten Speichers

Anzeigen eines bestimmten Speichers

Erfassen eines bestimmten Speichers



 

Ältere ICM2-APIs für Vorgänge, die nur den systemweiten Profil Verwaltungsbereich in Vista unterstützen, weisen keine Verhaltensänderungen auf. Installations-und Deinstallations Vorgänge fallen in diese Kategorie.

Ältere ICM2-APIs für Vorgänge, die sowohl den systemweiten als auch den aktuellen Profil Verwaltungsbereich unterstützen, haben das Verhalten geändert, um die aktuellen Benutzereinstellungen abzufragen und zu konfigurieren. Alle Vorgänge außer Installation und Deinstallation fallen in diese Kategorie.

 

 




