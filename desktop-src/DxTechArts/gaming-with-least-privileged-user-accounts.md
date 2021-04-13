---
title: Gaming mit Least-Privileged Benutzerkonten
description: In diesem Artikel wird beschrieben, wie Spieleentwickler Microsoft Windows-Spiele verfassen können, die für Benutzerkonten mit den geringsten Rechten geeignet sind (auch als eingeschränkte Benutzerkonten bezeichnet).
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c44d94345462fc02ec649c5674ed88c38c12ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473669"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Gaming mit Least-Privileged Benutzerkonten

In diesem Artikel wird beschrieben, wie Spieleentwickler Microsoft Windows-Spiele verfassen können, die für Benutzerkonten mit den geringsten Rechten geeignet sind (auch als eingeschränkte Benutzerkonten bezeichnet).

-   [Introduction (Einführung)](#introduction)
-   [Dateizugriff für Least-Privileged Benutzerkonten](#file-access-for-least-privileged-user-accounts)
    -   [Szenario 1: Dateien, die nicht von Benutzern angezeigt oder geändert werden müssen](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Szenario 2: Dateien, die von Benutzern angezeigt oder geändert werden müssen](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Registrierungs Zugriff für Least-Privileged Benutzerkonten](#registry-access-for-least-privileged-user-accounts)
-   [Patchen mit Least-Privileged Benutzerkonten](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Einführung

Windows verwaltet seine Benutzer mit Konten. Heute geben mehr als 80 Prozent der Computerbenutzer zu Hause Ihren Computer für andere Familienmitglieder frei. Wenn mehrere Benutzer einen Windows-Computer gemeinsam verwenden, werden mehrere Benutzerkonten erstellt, und jeder Benutzer meldet sich mit einem einzelnen Konto an, um auf den Computer zuzugreifen. Durch die zunehmende Sicherheit der Sicherheit betreiben mehr Benutzer ihre Computer mit den Benutzerkonten mit den geringsten Rechten, die auch als eingeschränkte Benutzerkonten bezeichnet werden, die nicht über die komplette Kontrolle über das System verfügen. Administrator Konten verfügen in der Regel über uneingeschränkten Zugriff auf jeden Teil des Computers. Dies kann sich darauf auswirken, wie Windows-basierte Spiele funktionieren.

Es gibt weitere Vorteile für Spieleentwickler, die ihre Spiele schreiben, um mit den Benutzerkonten mit den geringsten Rechten zu arbeiten. In Windows Vista und höheren Versionen werden die Benutzerkonten mit den geringsten Berechtigungen erzwungen. das bedeutet, dass jedes Konto im System, mit Ausnahme des lokalen Administrators, ein Benutzerkonto mit den geringsten Berechtigungen ist. Dies wirkt sich darauf aus, wie Spiele, die nicht der Richtlinie folgen (Legacy Anwendungen), unter Windows Vista und höher ausgeführt werden. Wenn beispielsweise eine Anwendung versucht, in einen Ordner oder einen Registrierungs Wert zu schreiben, in dem Sie nicht über die erforderliche Berechtigung verfügt, wird der Datei Schreibvorgang an einen virtuellen Dateispeicher für den Benutzer umgeleitet. Dieser virtuelle Dateispeicher befindet sich in einem Ordner, für den der Benutzer Schreibzugriff hat. Dieses Verhalten erscheint möglicherweise nicht als schwerwiegend, da der Schreib Versuch nicht ganz leicht auftritt. Anwendungen, die virtualisierte Dateien erstellen, verwirren jedoch möglicherweise Benutzer, da Dateien nicht in den von Benutzern erwarteten Speicherort geschrieben werden. Beispielsweise werden bei spielen, die hoch Bewertungs Dateien in denselben Ordner wie den ausführbaren Ordner schreiben, diese Dateien stattdessen in einen virtualisierten Ordner geschrieben. Folglich kann ein Benutzer nicht die von einem anderen Benutzer erzielte hohe Bewertung sehen, da jeder Benutzer über einen separaten virtualisierten Dateispeicher verfügt.

Spiele, die die Richtlinien in diesem Artikel befolgen, werden mit den Benutzerkonten mit den geringsten Rechten ausgeführt und können daher die Kompatibilität mit Windows Vista und höher gewährleisten.

## <a name="file-access-for-least-privileged-user-accounts"></a>Dateizugriff für Least-Privileged Benutzerkonten

Windows unterstützt zwei Dateisysteme: FAT32 und NTFS. FAT32 ist ein Legacy Dateisystem, das nur aus Gründen der Abwärtskompatibilität unterstützt wird. NTFS unterstützt leistungsfähigere und robuste Dateiberechtigungen. Die Verwendung von NTFS wird erweitert, wenn Einzelhändler neue Computer mit vorinstalliertem Windows auf einer mit NTFS partitionierten Festplatte versenden. Bei einem NTFS-basierten Windows XP-System haben Benutzer mit den Benutzerkonten mit den geringsten Berechtigungen nur begrenzten Zugriff auf mehrere Ordner. Allerdings haben Sie vollen Zugriff auf ein FAT32-basiertes Windows XP-System.

In der folgenden Tabelle sind der Standard Speicherort dieser Ordner und ihre Berechtigungen aufgeführt.



| Pfad                                               | Ordnerinhalt              | Lesen | Schreiben | Erstellen/Löschen |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| <Drive>: \\ Windows                            | Das Windows-Betriebssystem | X    |       |               |
| <Drive>: \\ Programmdateien                      | Ausführbare Anwendungs Dateien | X    |       |               |
| <Drive>: \\ Benutzername für Dokumente und Einstellungen \\\* | Die Dateien jedes Benutzers            | X    | X     | X             |
| <Drive>: \\ Dokumente und Einstellungen \\ alle Benutzer  | Alle Benutzer Dateien               | X    | X     | X             |



 

\* Username ist der Anmelde Name des Benutzers.

In einem Benutzerkonto mit den geringsten Berechtigungen können Sie Dateien in jedem Ordner lesen, schreiben, erstellen und löschen: Dokumente und Einstellungen \\ Benutzername oder Dokumente und Einstellungen \\ alle Benutzer.

Dies bedeutet, dass Sie Speichern von spielen nicht in \\ Programmdateien platzieren sollten, sondern in einem Unterordner in " \\ Eigene Dokumente". Außerdem sollten Sie temporäre Anwendungsdaten nicht in \\ Programmdateien oder \\ eigenen Dokumenten platzieren, sondern sollten Sie im Ordner "Anwendungsdaten" ( \_ lokale APPDATA-Daten von CSIDL \_ ) platzieren.

Genauer gesagt, gibt es zwei Szenarien, die jedes Spiel behandeln sollte:

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Szenario 1: Dateien, die nicht von Benutzern angezeigt oder geändert werden müssen

Ein typisches Beispiel wäre die Konfigurationsdatei des Spiels, temporäre Dateien und Spiel Cache Dateien. Diese Dateien werden in der Regel im Ordner "Anwendungsdaten" gespeichert. Rufen Sie zum Abrufen dieses Ordner Pfads die Funktion " [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) " mit CSIDL \_ AppData oder "local appdata" von CSIDL auf, \_ \_ wie im folgenden Codebeispiel gezeigt.

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

Der Unterschied zwischen lokalen und roaminganwendungsdatenordnern besteht darin, dass auf Windows 2000 und Windows XP roaminginhalte während des Anmelde-/Abmelde Vorgangs auf den Server kopiert werden, während der lokale Inhalt nicht ist. Bei den meisten spielen sind lokale Anwendungsdaten ausreichend.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Szenario 2: Dateien, die von Benutzern angezeigt oder geändert werden müssen

Ein typisches Beispiel wären die gespeicherten Spieldateien eines Benutzers. Speichern Sie die Dateien im Dokument Ordner des Benutzers, damit Sie für den Benutzer leicht sichtbar sind. Eine Anwendung ruft den Dokument Ordner Pfad des Benutzers durch Aufrufen von [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit CSIDL \_ Personal ab, wie im folgenden Codebeispiel gezeigt wird:

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

Manchmal muss ein Spieldateien speichern, die von allen Benutzern angezeigt und verwendet werden sollen. Ein Beispiel hierfür ist der Datensatz mit hoher Bewertung, bei dem alle Benutzer in dieselbe Daten Satz Datei schreiben, damit hohe Bewertungen für jeden Benutzersystem weit verwaltet werden, anstelle einer separaten hohen Bewertung. Weitere Beispiele hierfür sind heruntergeladene Karten, Missionen und spieländerungen. Wenn diese freigegeben werden, muss nur ein Benutzer Sie anstelle von jedem Benutzer herunterladen. Verwenden Sie in diesem Szenario den Dokument Ordner unter dem freigegebenen Profilordner, wie im folgenden Code gezeigt.

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

## <a name="registry-access-for-least-privileged-user-accounts"></a>Registrierungs Zugriff für Least-Privileged Benutzerkonten

Es ist üblich, dass Anwendungen die Windows-Registrierung verwenden, um Informationen zu speichern. Ähnlich wie beim Dateizugriff verfügen Administratoren und Benutzerkonten mit den geringsten Berechtigungen nicht über die gleichen Berechtigungen für die Registrierung. Für Benutzerkonten mit den geringsten Rechten ist der gesamte HKEY-Knoten für den \_ lokalen Computer schreibgeschützt \_ . Beispielsweise kann ein Spiel die Standard Konfigurationsinformationen lesen, aber möglicherweise keine neuen Informationen in diesen Knoten schreiben. Folglich müssen Spiele, die im Benutzermodus mit den geringsten Rechten ausgeführt werden und in die Registrierung schreiben müssen, den HKEY \_ Current \_ User-Knoten verwenden, um benutzerspezifische Informationen zu speichern, wie im folgenden Code veranschaulicht.

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

Beachten Sie, dass die Registrierungsinformationen während der Installation auf den lokalen HKEY-Computer geschrieben werden sollten \_ \_ , nicht auf den aktuellen HKEY- \_ \_ Benutzer. Dies liegt daran, dass die Person, die die Installation ausgeführt hat, normalerweise ein Administrator ist und nicht die einzige Person ist, die das Programm verwenden soll. In dieser Situation stellt das Schreiben in HKEY \_ Current \_ User die Informationen für andere Benutzer nicht zur Verfügung. Dies ist in der Regel kein Problem, da die Informationen, die während der Installation in die Registrierung geschrieben werden, die Konfigurations-und Standardeinstellungen sind, die für jeden Benutzer des Programms gelten.

Beim Deinstallieren des Spiels ist zusätzlicher Aufwand erforderlich, um jeden Wert zu entfernen, den das Spiel in die Registrierung geschrieben hat. Da das Deinstallationsprogramm von einer Person ausgeführt wird, in der Regel der Administrator, werden die relevanten Informationen auf dem \_ lokalen HKEY \_ -Computer und HKEY ( \_ aktueller \_ Benutzer) nicht für andere Benutzer entfernt. Eine Möglichkeit, die benutzerspezifischen Informationen in der Registrierung zu entfernen, besteht darin, den Registrierungs Struktur Stamm der HKEY-Benutzer aufzuzählen \_ . Jeder Unterschlüssel unter HKEY- \_ Benutzer entspricht der HKEY \_ Current \_ User Hive für einen bestimmten Benutzer im System. Durch das Auflisten von HKEY \_ -Benutzern und das Entfernen der spielspezifischen Informationen unter den einzelnen unter Schlüsseln kann das Deinstallationsprogramm sicherstellen, dass keine Informationen zurückgelassen werden.

## <a name="patching-with-least-privileged-user-accounts"></a>Patchen mit Least-Privileged Benutzerkonten

Das Patchen eines Spiels umfasst das Aktualisieren der Spieldateien. Daher ist in der Regel ein Schreibzugriff auf den Programmordner des Spiels erforderlich. Das Patchen eines Spiels ist ein einfacher Prozess, wenn er von einem Administrator durchgeführt wird, da Sie uneingeschränkten Zugriff auf den Programmordner des Spiels haben. Umgekehrt war es bisher schwierig, wenn es nicht unmöglich war, dass ein Benutzer mit geringsten Rechten Spiele aufgrund der Zugriffs Einschränkung Patchen konnte. Nun wurde [Windows Installer](/windows/desktop/Msi/windows-installer-portal) verbessert, um das Patchen von Benutzerkonten zu ermöglichen. Um dieses Feature nutzen zu können, werden Spiele empfohlen, Windows Installer für die Installation und das Patchen zu verwenden.

Ab Windows Installer 3,0 können Anwendungspatches von den geringsten privilegierten Benutzern angewendet werden, wenn bestimmte Bedingungen erfüllt sind. Dies sind die folgenden Bedingungen:

-   Die Anwendung wurde mit Windows Installer 3,0 installiert.
-   Die Anwendung wurde ursprünglich pro Computer installiert.
-   Die Anwendung wird von einem Wechselmedium, z. b. CD-ROM oder Digital Video Disc (DVD), installiert.
-   Die Patches werden Digital von einem Zertifikat signiert, das vom ursprünglichen Installer-Paket (MSI-Datei) identifiziert wird.
-   Die Patches können anhand der digitalen Signatur überprüft werden.
-   Das ursprüngliche Installer-Paket hat das Patchen von Benutzerkonten mit geringsten Rechten nicht deaktiviert.
-   Der Systemadministrator hat das Patchen von Benutzerkonten mit den geringsten Berechtigungen nicht über die System Richtlinie deaktiviert.

Normalerweise kann ein Benutzer mit dem geringsten Privileg die Programmdateien eines Spiels nicht ändern. Wenn jedoch die oben genannten Bedingungen erfüllt sind und das Lua-Patchen aktiviert ist, können Windows Installer die Spieldateien aktualisieren, sodass der Benutzer die neueste Version erhält.

> [!Note]  
> Die in diesem Artikel enthaltenen Informationen beziehen sich auf das Produkt der Vorabversion der Software, das vor seiner ersten kommerziellen Version erheblich geändert werden kann. Entsprechend können die Informationen das Softwareprodukt bei der ersten kommerziellen Freigabe nicht exakt beschreiben oder widerspiegeln. Dieser Artikel dient nur zu Informationszwecken, und Microsoft übernimmt keinerlei ausdrückliche oder konkludente Gewährleistungen in Bezug auf diesen Artikel oder die darin enthaltenen Informationen.

 

 

 