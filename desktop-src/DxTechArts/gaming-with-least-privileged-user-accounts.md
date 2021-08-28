---
title: Gaming mit Least-Privileged Benutzerkonten
description: In diesem Artikel wird beschrieben, wie Spieleentwickler Microsoft Windows Spiele erstellen können, die gut mit Benutzerkonten mit den geringsten Berechtigungen (auch als Eingeschränkte Benutzerkonten bezeichnet) funktionieren.
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db15302eb856aaeb05c68fae4746110dd42cb4a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887384"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Gaming mit Least-Privileged Benutzerkonten

In diesem Artikel wird beschrieben, wie Spieleentwickler Microsoft Windows Spiele erstellen können, die gut mit Benutzerkonten mit den geringsten Berechtigungen (auch als Eingeschränkte Benutzerkonten bezeichnet) funktionieren.

-   [Introduction (Einführung)](#introduction)
-   [Dateizugriff für Least-Privileged Benutzerkonten](#file-access-for-least-privileged-user-accounts)
    -   [Szenario 1: Dateien, die von Benutzern nicht angezeigt oder geändert werden müssen](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Szenario 2: Dateien, die von Benutzern angezeigt oder geändert werden müssen](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Registrierungszugriff für Least-Privileged Benutzerkonten](#registry-access-for-least-privileged-user-accounts)
-   [Patchen mit Least-Privileged Benutzerkonten](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Einführung

Windows verwaltet seine Benutzer mit Konten. Heute teilen mehr als 80 Prozent der Computerbenutzer zu Hause ihren Computer mit anderen Familienmitgliedern. Wenn mehrere Benutzer einen Windows Computer freigeben, werden mehrere Benutzerkonten erstellt, und jeder Benutzer meldet sich mit einem einzelnen Konto an, um auf den Computer zuzugreifen. Mit dem zunehmenden Sicherheitsbewusstsein betreiben mehr Personen ihre Computer mit Benutzerkonten mit den geringsten Berechtigungen, die auch als Konten mit eingeschränkten Berechtigungen bezeichnet werden und keine vollständige Kontrolle über das System haben. Administratorkonten haben in der Regel uneingeschränkten Zugriff auf jeden Teil des Computers. Dies kann sich auf die Funktionsweise Windows-basierten Spiele auswirken.

Es gibt zusätzliche Vorteile für Spieleentwickler, die ihre Spiele schreiben, um mit Benutzerkonten mit den geringsten Berechtigungen zu arbeiten. In Windows Vista und höher werden Benutzerkonten mit den geringsten Berechtigungen erzwungen. Dies bedeutet, dass jedes Konto auf dem System mit Ausnahme des lokalen Administrators ein Benutzerkonto mit den geringsten Berechtigungen ist. Dies wirkt sich darauf aus, wie Spiele, die nicht der Richtlinie entsprechen (Legacyanwendungen), auf Windows Vista und höher ausgeführt werden. Wenn eine Anwendung beispielsweise versucht, in einen Ordner oder einen Registrierungswert zu schreiben, für den sie keine Berechtigung besitzt, wird der Dateischreibvorgang an einen virtuellen Dateispeicher für den Benutzer umgeleitet. Dieser virtuelle Dateispeicher befindet sich in einem Ordner, auf den der Benutzer Schreibzugriff hat. Dieses Verhalten scheint möglicherweise nicht so schwerwiegender zu sein wie ein Fehler beim Schreibversuch. Anwendungen, die virtualisierte Dateien erstellen, können Benutzer jedoch verwirren, da Dateien nicht an den Speicherort geschrieben werden, den Benutzer erwarten. Beispielsweise schreiben Spiele, die Dateien mit hoher Bewertung in denselben Ordner schreiben wie der ausführbare Ordner, stattdessen diese Dateien in einen virtualisierten Ordner. Folglich kann ein Benutzer die von einem anderen Benutzer erzielten hohen Ergebnisse nicht sehen, da jeder Benutzer über einen separaten virtualisierten Dateispeicher verfügt.

Spiele, die den Richtlinien in diesem Artikel entsprechen, werden mit Benutzerkonten mit den geringsten Berechtigungen ausgeführt und behalten daher die Kompatibilität mit Windows Vista und höher bei.

## <a name="file-access-for-least-privileged-user-accounts"></a>Dateizugriff für Least-Privileged Benutzerkonten

Windows unterstützt zwei Dateisysteme: FAT32 und NTFS. FAT32 ist ein älteres Dateisystem, das nur aus Gründen der Abwärtskompatibilität unterstützt wird. NTFS unterstützt leistungsfähigere und stabilere Dateiberechtigungen. Die Verwendung von NTFS wird erweitert, da Einzelhändler neue Computer mit Windows vorinstalliert auf einer NTFS-partitionierten Festplatte versenden. Auf einem NTFS-basierten Windows XP-System haben Benutzer mit Benutzerkonten mit den geringsten Berechtigungen nur eingeschränkten Zugriff auf mehrere Ordner. Sie hätten jedoch vollständigen Zugriff auf ein FAT32-basiertes Windows XP-System.

In der folgenden Tabelle sind der Standardspeicherort dieser Ordner und deren Berechtigungen aufgeführt.



| Pfad                                               | Ordnerinhalt              | Lesen | Schreiben | Erstellen/Löschen |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| &lt;Laufwerk: &gt; \\ Windows                            | Das Windows Betriebssystem | X    |       |               |
| &lt;Laufwerk: &gt; \\ Programmdateien                      | Ausführbare Anwendungsdateien | X    |       |               |
| &lt;Laufwerk: &gt; \\ Dokumente und Einstellungen \\ Benutzername\* | Dateien jedes Benutzers            | X    | X     | X             |
| &lt;Laufwerk: &gt; Dokumente und Einstellungen Alle \\ \\ Benutzer  | Alle Benutzerdateien               | X    | X     | X             |



 

\* Benutzername ist der Anmeldename des Benutzers.

In einem Benutzerkonto mit den geringsten Berechtigungen können Sie Dateien in beiden Ordnern lesen, schreiben, erstellen und löschen: Dokumente und Einstellungen \\ Benutzername oder Dokumente und Einstellungen Alle \\ Benutzer.

Dies bedeutet, dass Sie keine Spiele in Programmdateien speichern \\ sollten, sondern in einem Unterordner in \\ Eigene Dokumente. Außerdem sollten Sie keine temporären Anwendungsdaten in \\ Programmdateien oder \\ Eigene Dokumente platzieren, sondern im Ordner Anwendungsdaten (CSIDL \_ LOCAL \_ APPDATA).

Genauer gesagt gibt es zwei Szenarien, die jedes Spiel behandeln sollte:

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Szenario 1: Dateien, die von Benutzern nicht angezeigt oder geändert werden müssen

Ein typisches Beispiel wären die Konfigurationsdatei des Spiels, temporäre Dateien und Spielcachedateien. Diese Dateien werden in der Regel im Ordner Anwendungsdaten gespeichert. Um diesen Ordnerpfad abzurufen, rufen Sie die [**SHGetFolderPath-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit CSIDL \_ APPDATA oder CSIDL LOCAL APPDATA auf, \_ wie im folgenden \_ Codebeispiel gezeigt.

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

Der Unterschied zwischen lokalen und roaminggespeicherten Anwendungsdatenordnern besteht darin, dass bei Windows 2000 und Windows XP Roaminginhalte während des Anmelde-/Abmeldungsprozesses auf den server kopiert werden, während lokale Inhalte nicht auf den Server kopiert werden. Für die meisten Spiele sind lokale Anwendungsdaten ausreichend.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Szenario 2: Dateien, die von Benutzern angezeigt oder geändert werden müssen

Ein typisches Beispiel wären die gespeicherten Spieldateien eines Benutzers. Store die Dateien im Dokumentordner des Benutzers, damit sie für den Benutzer leicht sichtbar sind. Eine Anwendung ruft den Dokumentordnerpfad des Benutzers ab, indem [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit CSIDL PERSONAL aufgerufen \_ wird, wie im folgenden Codebeispiel gezeigt:

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

Manchmal muss ein Spiel möglicherweise Dateien speichern, die alle Benutzer sehen und verwenden sollen. Ein Beispiel ist der Datensatz mit hoher Bewertung, bei dem alle Benutzer in die gleiche Datensatzdatei schreiben, sodass hohe Bewertungen systemweit anstatt einer separaten hohen Bewertung für jeden Benutzer beibehalten werden. Weitere Beispiele sind heruntergeladene Karten, Missionen und Spieländerungen. Wenn diese freigegeben werden, muss nur ein Benutzer diese anstelle jedes Benutzers herunterladen. Verwenden Sie in diesem Szenario den Dokumentordner unter dem freigegebenen Profilordner, wie im folgenden Code gezeigt.

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

Es ist üblich, dass Anwendungen die Windows Registrierung verwenden, um Informationen zu speichern. Ähnlich wie beim Dateizugriff verfügen Administratorkonten und Benutzerkonten mit den geringsten Berechtigungen nicht über die gleiche Berechtigung für die Registrierung. Bei Benutzerkonten mit den geringsten Berechtigungen ist der gesamte \_ HKEY LOCAL \_ MACHINE-Knoten schreibgeschützt. Beispielsweise kann ein Spiel die Standardkonfigurationsinformationen lesen, aber möglicherweise keine neuen Informationen auf diesen Knoten schreiben. Daher müssen Spiele, die im Benutzermodus mit den geringsten Berechtigungen ausgeführt werden und in die Registrierung schreiben müssen, den Knoten HKEY \_ CURRENT \_ USER verwenden, um Benutzerinformationen zu speichern, wie im folgenden Code veranschaulicht.

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

Beachten Sie, dass während der Installation Registrierungsinformationen in HKEY LOCAL MACHINE und nicht in HKEY CURRENT USER geschrieben werden \_ \_ \_ \_ sollten. Dies liegt daran, dass die Person, die die Installation ausführt, in der Regel ein Administrator ist und möglicherweise nicht die einzige Person ist, die das Programm verwendet. Wenn Sie in diesem Fall HKEY CURRENT USER schreiben, \_ sind die Informationen für andere Benutzer nicht \_ verfügbar. Dies ist in der Regel kein Problem, da die während der Installation in die Registrierung geschriebenen Informationen die Konfiguration und die Standardeinstellungen sind, die für jeden Benutzer des Programms gelten.

Beim Deinstallieren des Spiels ist zusätzlicher Aufwand erforderlich, um jeden Wert zu entfernen, den das Spiel in die Registrierung geschrieben hat. Da das Deinstallationsprogramm von einer Person (in der Regel vom Administrator) ausgeführt wird, werden beim einfachen Löschen der relevanten Informationen in HKEY \_ LOCAL \_ MACHINE und HKEY CURRENT USER \_ keine Werte für andere Benutzer \_ entfernt. Eine Möglichkeit, die Benutzerinformationen in der Registrierung zu entfernen, besteht darin, den Stamm der HKEY \_ USERS-Registrierungsstruktur aufzuzählen. Jeder Unterschlüssel unter HKEY \_ USERS entspricht der HKEY \_ CURRENT \_ USER-Struktur für einen bestimmten Benutzer im System. Durch aufzählen von HKEY \_ USERS und Entfernen der spielspezifischen Informationen unter jedem Unterschlüssel kann das Deinstallationsprogramm sicherstellen, dass keine Informationen zurückbleiben.

## <a name="patching-with-least-privileged-user-accounts"></a>Patchen mit Least-Privileged Benutzerkonten

Das Patchen eines Spiels umfasst das Aktualisieren der Dateien des Spiels. Daher ist in der Regel Schreibzugriff auf den Programmordner des Spiels erforderlich. Das Patchen eines Spiels ist ein einfacher Prozess, wenn es von einem Administrator durchgeführt wird, da er uneingeschränkten Zugriff auf den Programmordner des Spiels hat. Umgekehrt war es für einen Benutzer mit den geringsten Berechtigungen aufgrund der Zugriffseinschränkung traditionell schwierig, wenn nicht unmöglich, Spiele zu patchen. Nun wurde [Windows Installer](/windows/desktop/Msi/windows-installer-portal) verbessert, um das Patchen von Benutzerkonten mit den geringsten Berechtigungen zu ermöglichen. Um dieses Feature nutzen zu können, sollten Spiele Windows Installer für installation und patchen verwenden.

Ab Windows Installer 3.0 können Anwendungspatches von Benutzern mit den geringsten Berechtigungen angewendet werden, wenn bestimmte Bedingungen erfüllt sind. Folgende Bedingungen sind zu erfüllen:

-   Die Anwendung wurde mit Windows Installer 3.0 installiert.
-   Die Anwendung wurde ursprünglich pro Computer installiert.
-   Die Anwendung wird über Wechselmedien wie CD-ROM oder digitale Videodatenträger (DVD) installiert.
-   Die Patches werden digital von einem Zertifikat signiert, das durch das ursprüngliche Installationspaket (.msi-Datei) identifiziert wird.
-   Die Patches können anhand der digitalen Signatur überprüft werden.
-   Das ursprüngliche Installationspaket hat das Patchen von Benutzerkonten mit den geringsten Berechtigungen nicht deaktiviert.
-   Der Systemadministrator hat das Patchen von Benutzerkonten mit den geringsten Berechtigungen nicht über die Systemrichtlinie deaktiviert.

Normalerweise kann ein Benutzer mit den geringsten Berechtigungen die Programmdateien eines Spiels nicht ändern. Wenn die oben genannten Bedingungen erfüllt sind und DAS LUA-Patchen aktiviert ist, kann Windows Installer die Dateien des Spiels aktualisieren, sodass der Benutzer die neueste Version erhält.

> [!Note]  
> Die in diesem Artikel enthaltenen Informationen beziehen sich auf vorab veröffentlichte Softwareprodukte, die vor der ersten kommerziellen Version erheblich geändert werden können. Entsprechend können die Informationen das Softwareprodukt bei der ersten kommerziellen Veröffentlichung nicht genau beschreiben oder widerspiegeln. Dieser Artikel dient nur zu Informationszwecken, und Microsoft übernimmt keine ausdrücklichen oder konkludenten Gewährleistungen in Bezug auf diesen Artikel oder die darin enthaltenen Informationen.

 

 

 
