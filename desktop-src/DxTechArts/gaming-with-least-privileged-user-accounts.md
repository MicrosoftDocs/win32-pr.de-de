---
title: Gaming mit Least-Privileged Benutzerkonten
description: In diesem Artikel wird beschrieben, wie Spieleentwickler Microsoft Windows-Spiele erstellen können, die gut mit Benutzerkonten mit den geringsten Berechtigungen (auch als Konten mit eingeschränkten Benutzerkonten bezeichnet) funktionieren.
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939d22b1d8bf381e98c5b6a7222be29b565c3d9e1f0758788aff94b0915b1807
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340740"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Gaming mit Least-Privileged Benutzerkonten

In diesem Artikel wird beschrieben, wie Spieleentwickler Microsoft Windows-Spiele erstellen können, die gut mit Benutzerkonten mit den geringsten Berechtigungen (auch als Konten mit eingeschränkten Benutzerkonten bezeichnet) funktionieren.

-   [Introduction (Einführung)](#introduction)
-   [Dateizugriff für Least-Privileged Benutzerkonten](#file-access-for-least-privileged-user-accounts)
    -   [Szenario 1: Dateien, die von Benutzern nicht angezeigt oder geändert werden müssen](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Szenario 2: Dateien, die von Benutzern angezeigt oder geändert werden müssen](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Registrierungszugriff für Least-Privileged Benutzerkonten](#registry-access-for-least-privileged-user-accounts)
-   [Patchen mit Least-Privileged Benutzerkonten](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Einführung

Windows verwaltet ihre Benutzer mit Konten. Heute teilen sich mehr als 80 Prozent der Computerbenutzer zu Hause ihren Computer mit anderen Familienmitgliedern. Wenn mehrere Benutzer einen Windows Computer gemeinsam verwenden, werden mehrere Benutzerkonten erstellt, und jeder Benutzer meldet sich mit einem einzelnen Konto an, um auf den Computer zu zugreifen. Mit dem zunehmenden Sicherheitsbewusstsein betreiben immer mehr Benutzer ihre Computer mit Benutzerkonten mit den geringsten Berechtigungen, die auch als Konten mit eingeschränkten Benutzerkonten bezeichnet werden und keine vollständige Kontrolle über das System haben. Administratorkonten haben in der Regel uneingeschränkten Zugriff auf jeden Teil des Computers. Dies kann sich auf die Windows-basierten Spiele auswirken.

Es gibt zusätzliche Vorteile für Spieleentwickler, die ihre Spiele für die Arbeit mit Benutzerkonten mit den geringsten Berechtigungen schreiben. In Windows Vista und höher werden Benutzerkonten mit den geringsten Rechten erzwungen. Dies bedeutet, dass jedes Konto im System mit Ausnahme des lokalen Administrators ein Benutzerkonto mit den geringsten Rechten ist. Dies wirkt sich darauf aus, wie Spiele, die nicht der Richtlinie (Legacyanwendungen) folgen, unter Windows Vista und höher ausgeführt werden. Wenn eine Anwendung beispielsweise versucht, in einen Ordner oder einen Registrierungswert zu schreiben, für den sie nicht über die Berechtigung verfügt, wird der Datei-Schreibzugriff an einen virtuellen Dateispeicher für den Benutzer umgeleitet. Dieser virtuelle Dateispeicher befindet sich in einem Ordner, auf den der Benutzer Schreibzugriff hat. Dieses Verhalten erscheint möglicherweise nicht so schwerwiegender, als wenn der Schreibversuch nicht ganz fehlschlägt. Allerdings können Anwendungen, die virtualisierte Dateien erstellen, Benutzer verwirren, da Dateien nicht an den speicherort geschrieben werden, den Benutzer erwarten. Beispielsweise schreiben Spiele, die dateien mit hoher Bewertung in denselben Ordner wie der ausführbare Ordner schreiben, diese Dateien stattdessen in einen virtualisierten Ordner. Folglich kann ein Benutzer die von einem anderen Benutzer erzielten Hohen Bewertung nicht sehen, da jeder Benutzer über einen separaten virtualisierten Dateispeicher verfügt.

Spiele, die den Richtlinien in diesem Artikel folgen, werden mit Benutzerkonten mit den geringsten Rechten ausgeführt und behalten daher die Kompatibilität mit Windows Vista und höher bei.

## <a name="file-access-for-least-privileged-user-accounts"></a>Dateizugriff für Least-Privileged Benutzerkonten

Windows unterstützt zwei Dateisysteme: FAT32 und NTFS. FAT32 ist ein Legacydateisystem, das nur aus Gründen der Abwärtskompatibilität unterstützt wird. NTFS unterstützt leistungsfähigere und stabilere Dateiberechtigungen. Die Verwendung von NTFS wird immer weiter erweitert, da Einzelhändler neue Computer Windows auf einer NTFS-partitionierten Festplatte vorinstalliert sind. Auf einem NTFS-basierten Windows XP-System haben Benutzer mit Benutzerkonten mit den geringsten Berechtigungen nur eingeschränkten Zugriff auf mehrere Ordner. Sie hätten jedoch vollständigen Zugriff auf ein FAT32-basiertes Windows XP-System.

In der folgenden Tabelle sind der Standardspeicherort dieser Ordner und deren Berechtigungen aufgeführt.



| Pfad                                               | Ordnerinhalt              | Lesen | Schreiben | Erstellen/Löschen |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| <Drive>: \\ Windows                            | Das Windows Betriebssystem | X    |       |               |
| <Drive>: \\ Programmdateien                      | Ausführbare Anwendungsdateien | X    |       |               |
| <Drive>: \\ Dokumente und Einstellungen \\ Benutzername\* | Dateien der einzelnen Benutzer            | X    | X     | X             |
| <Drive>: \\ Dokumente und Einstellungen Alle \\ Benutzer  | Alle Benutzerdateien               | X    | X     | X             |



 

\* Benutzername ist der Anmeldename des Benutzers.

In einem Benutzerkonto mit den geringsten Berechtigungen können Sie Dateien in beiden Ordnern lesen, schreiben, erstellen und löschen: Dokumente und Einstellungen Benutzername oder Dokumente und \\ Einstellungen \\ Alle Benutzer.

Dies bedeutet, dass Sie keine Spiele speichern in Programmdateien platzieren sollten, sondern in einem Unterordner \\ in \\ Eigene Dokumente. Außerdem sollten Sie keine temporären Anwendungsdaten in Programmdateien oder Eigene Dokumente, sondern im Ordner Anwendungsdaten \\ \\ (CSIDL \_ LOCAL \_ APPDATA) platzieren.

Genauer gesagt gibt es zwei Szenarien, die jedes Spiel verarbeiten sollte:

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Szenario 1: Dateien, die von Benutzern nicht angezeigt oder geändert werden müssen

Ein typisches Beispiel wären die Konfigurationsdatei des Spiels, temporäre Dateien und Spielcachedateien. Diese Dateien werden in der Regel im Ordner Anwendungsdaten gespeichert. Um diesen Ordnerpfad zu erhalten, rufen Sie die [**SHGetFolderPath-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit CSIDL APPDATA oder CSIDL LOCAL APPDATA auf, wie im folgenden \_ \_ \_ Codebeispiel gezeigt.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

// Local Application Data
SHGetFolderPath( hWnd, CSIDL_LOCAL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
// Roaming Application Data
SHGetFolderPath( hWnd, CSIDL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

Der Unterschied zwischen lokalen und roaminggespeicherten Anwendungsdatenordnern besteht in dem Unterschied, dass roamingseitige Inhalte auf Windows 2000 und Windows XP während des Anmelde-/Abmeldevorgangs auf den serverseitigen Server kopiert werden, während der lokale Inhalt nicht. Für die meisten Spiele sind lokale Anwendungsdaten ausreichend.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Szenario 2: Dateien, die von Benutzern angezeigt oder geändert werden müssen

Ein typisches Beispiel wären die gespeicherten Spieldateien eines Benutzers. Store Dateien im Dokumentordner des Benutzers, damit sie für den Benutzer leicht sichtbar sind. Eine Anwendung ruft den Dokumentordnerpfad des Benutzers ab, indem [**sie SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit CSIDL PERSONAL aufruft, wie im \_ folgenden Codebeispiel gezeigt:

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

Manchmal muss ein Spiel möglicherweise Dateien speichern, die alle Benutzer sehen und verwenden sollen. Ein Beispiel hierfür ist der High Score-Datensatz, bei dem alle Benutzer in dieselbe Datensatzdatei schreiben, damit die Höchstergebnisse systemweit und nicht für jeden Benutzer separat hochgewertet werden. Weitere Beispiele sind heruntergeladene Karten, Missionen und Spieländerungen. Wenn diese freigegeben werden, muss nur ein Benutzer sie anstelle jedes Benutzers herunterladen. Verwenden Sie in diesem Szenario den Dokumentordner unter dem Freigegebenen Profilordner, wie im folgenden Code gezeigt.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_COMMON_DOCUMENTS, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

## <a name="registry-access-for-least-privileged-user-accounts"></a>Registrierungszugriff für Least-Privileged Benutzerkonten

Es ist üblich, dass Anwendungen die Windows zum Speichern von Informationen verwenden. Ähnlich wie beim Dateizugriff verfügen Administratorkonten und Benutzerkonten mit den geringsten Berechtigungen nicht über die gleiche Berechtigung für die Registrierung. Für Benutzerkonten mit den geringsten Berechtigungen ist der gesamte HKEY \_ LOCAL \_ MACHINE-Knoten schreibgeschützt. Beispielsweise kann ein Spiel die Standardkonfigurationsinformationen lesen, aber möglicherweise keine neuen Informationen auf diesen Knoten schreiben. Folglich müssen Spiele, die im Benutzermodus mit den geringsten Berechtigungen ausgeführt werden und in die Registrierung schreiben müssen, den Knoten HKEY CURRENT USER verwenden, um Benutzerinformationen zu speichern, wie im folgenden Code \_ \_ veranschaulicht.

``` syntax
#define APP_REGISTRY_KEY_PATH L"Software\\MyCompany\\MyApp"

LONG lRetVal;
HKEY hKey;

lRetVal = RegCreateKeyExW( HKEY_CURRENT_USER,
                           APP_REGISTRY_KEY_PATH,
                           0,
                           NULL,
                           REG_OPTION_NON_VOLATILE,
                           KEY_WRITE|KEY_READ,
                           NULL,
                           &hKey,
                           NULL );

if( ERROR_SUCCESS == lRetVal )
{
    // Store information in hKey
}
```

Es ist zu sehen, dass während der Installation Registrierungsinformationen auf HKEY LOCAL MACHINE und nicht \_ \_ auf HKEY CURRENT USER geschrieben werden \_ \_ sollten. Dies liegt daran, dass die Person, die die Installation ausgeführt, in der Regel ein Administrator ist und möglicherweise nicht die einzige Person ist, die das Programm verwendet. In diesem Fall macht das Schreiben in HKEY CURRENT USER die \_ Informationen für andere Benutzer nicht \_ verfügbar. Dies ist in der Regel kein Problem, da die während der Installation in die Registrierung geschriebenen Informationen die Konfigurations- und Standardeinstellungen sind, die für jeden Benutzer des Programms gelten.

Beim Deinstallieren des Spiels ist zusätzlicher Aufwand erforderlich, um jeden Wert zu entfernen, den das Spiel in die Registrierung geschrieben hat. Da das Deinstallationsprogramm von einer Person (in der Regel vom Administrator) ausgeführt wird, werden durch das einfache Löschen der relevanten Informationen in HKEY LOCAL MACHINE und HKEY CURRENT USER keine Werte für andere \_ \_ Benutzer \_ \_ entfernt. Eine Möglichkeit zum Entfernen der benutzerspezifischen Informationen in der Registrierung ist das Aufzählen des Registrierungsstamms HKEY \_ USERS. Jeder Unterschlüssel unter HKEY \_ USERS entspricht der HKEY CURRENT \_ \_ USER-Struktur für einen bestimmten Benutzer im System. Durch Aufzählen von HKEY-BENUTZERN und Entfernen der spielspezifischen Informationen unter jedem Unterschlüssel kann das Deinstallationsprogramm sicherstellen, dass keine Informationen \_ zurückgelassen werden.

## <a name="patching-with-least-privileged-user-accounts"></a>Patchen mit Least-Privileged Benutzerkonten

Das Patchen eines Spiels umfasst das Aktualisieren der Dateien des Spiels. Daher ist in der Regel Schreibzugriff auf den Programmordner des Spiels erforderlich. Das Patchen eines Spiels ist ein einfacher Prozess, wenn er von einem Administrator durchgeführt wird, da er uneingeschränkten Zugriff auf den Programmordner des Spiels hat. Umgekehrt war es für einen Benutzer mit den geringsten Berechtigungen aufgrund der Zugriffsbeschränkung bisher schwierig, wenn nicht gar unmöglich, Spiele zu patchen. Nun wurde [Windows Installer](/windows/desktop/Msi/windows-installer-portal) erweitert, um das Patchen von Benutzerkonten mit den geringsten Berechtigungen zu ermöglichen. Um dieses Feature nutzen zu können, sollten Spiele Windows Installer für Installation und Patchen verwenden.

Ab Windows Installer 3.0 können Anwendungspatches von Benutzern mit den geringsten Berechtigungen angewendet werden, wenn bestimmte Bedingungen erfüllt sind. Dies sind die folgenden Bedingungen:

-   Die Anwendung wurde mithilfe Windows Installer 3.0 installiert.
-   Die Anwendung wurde ursprünglich pro Computer installiert.
-   Die Anwendung wird von Wechselmedien wie CD-ROM oder dvd (Digital Video Disc) installiert.
-   Die Patches werden digital durch ein Zertifikat signiert, das vom ursprünglichen Installationspaket (.msi wird.
-   Die Patches können anhand der digitalen Signatur überprüft werden.
-   Das ursprüngliche Installationspaket hat das Patchen von Benutzerkonten mit den geringsten Berechtigungen nicht deaktiviert.
-   Der Systemadministrator hat das Patchen von Benutzerkonten mit den geringsten Berechtigungen über die Systemrichtlinie nicht deaktiviert.

Normalerweise kann ein Benutzer mit den geringsten Berechtigungen die Programmdateien eines Spiels nicht ändern. Wenn jedoch die oben genannten Bedingungen erfüllt sind und DAS LUA-Patchen aktiviert ist, kann Windows Installer die Dateien des Spiels aktualisieren, sodass der Benutzer die neueste Version erhält.

> [!Note]  
> Die in diesem Artikel enthaltenen Informationen beziehen sich auf vorab veröffentlichten Softwareprodukt, das vor der ersten kommerziellen Version erheblich geändert werden kann. Entsprechend können die Informationen das Softwareprodukt bei der ersten kommerziellen Version nicht genau beschreiben oder widerspiegeln. Dieser Artikel dient nur zu Informationszwecken, und Microsoft übernimmt keine Gewährleistungen, weder ausdrücklich noch konkludent, in Bezug auf diesen Artikel oder die darin enthaltenen Informationen.

 

 

 