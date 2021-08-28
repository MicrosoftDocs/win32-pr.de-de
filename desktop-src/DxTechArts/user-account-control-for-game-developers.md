---
title: Benutzerkontensteuerung für Spieleentwickler
description: In diesem Artikel werden die Richtlinien und bewährten Methoden für Spieleentwickler beschrieben, um effektiv mit dem in Windows Vista eingeführten Sicherheitsfeature für die Benutzerkontensteuerung (User Account Control, UAC) zu arbeiten.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb8b6ac31ef13e3ace4d439c82f4708673aeffb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886071"
---
# <a name="user-account-control-for-game-developers"></a>Benutzerkontensteuerung für Spieleentwickler

In diesem Artikel werden die Richtlinien und bewährten Methoden für Spieleentwickler beschrieben, um effektiv mit dem in Windows Vista eingeführten Sicherheitsfeature für die Benutzerkontensteuerung (User Account Control, UAC) zu arbeiten.

-   [Übersicht über die Benutzerkontensteuerung](#overview-of-user-account-control)
-   [Benutzerkonten in Windows Vista](#user-accounts-in-windows-vista)
-   [Dateizugriff als Standardbenutzer](#file-access-as-a-standard-user)
-   [Registrierungszugriff als Standardbenutzer](#registry-access-as-a-standard-user)
-   [Rechteerweiterungen](#privilege-elevation)
-   [Auswirkungen der UAC mit CreateProcess()](#uac-implications-with-createprocess)
-   [Festlegen der Ausführungsebene im Anwendungsmanifest](#setting-the-execution-level-in-the-application-manifest)
-   [Einbetten eines Manifests in Visual Studio](#embedding-a-manifest-in-visual-studio)
-   [UAC-Kompatibilität mit älteren Spielen](#uac-compatibility-with-older-games)
-   [Legacyszenarien und Manifeste](#legacy-scenarios-and-manifests)
-   [Zusammenfassung](#conclusion)
-   [Weitere Informationen](#further-reading)

## <a name="overview-of-user-account-control"></a>Übersicht über die Benutzerkontensteuerung

Die Benutzerkontensteuerung (User Account Control, UAC), die in Windows Vista eingeführt wurde, ist ein Sicherheitsfeature, das dazu dient, böswillige Angreifer daran zu hindern, Schwachstellen oder Fehler in weit verbreiteten Anwendungen zu verwenden, um das Betriebssystem oder andere installierte Programme zu ändern. Dies wird erreicht, indem die überwiegende Mehrheit der Programme und Prozesse als Standardbenutzer (auch als eingeschränkter Benutzer, eingeschränkter Benutzer oder Least-Privileged Benutzer bezeichnet) ausgeführt wird, auch wenn das Konto des aktuellen Benutzers über Administratoranmeldeinformationen verfügt. Ein Prozess mit Standardbenutzerberechtigungen weist viele inhärente Einschränkungen auf, die verhindern, dass er systemweite Änderungen vornimmt.

Die benutzerseitige Zugriffssteuerung ist auch für die Rechteerweiterung eines Prozesses verantwortlich, indem ein dialogbasiertes Authentifizierungsschema verwendet wird, das bei der Ausführung bestimmter Prozesse initiiert wird, die administratorrechte erfordern. Rechteerweiterungen ermöglichen Administratoren, den Großteil ihrer Anwendungen auf einer sicheren Berechtigungsebene auszuführen (wie jeder andere Standardbenutzer), lassen aber auch Prozesse und Vorgänge zu, die Administratorrechte erfordern. UAC unterstützt die Over-the-Shoulder-Authentifizierung, sodass ein Administrator einem Programm erhöhte Rechte erteilen kann, während ein Standardbenutzer derzeit am System angemeldet ist.

Die UAC-Funktion ist standardmäßig aktiviert. Es ist zwar möglich, dass ein Administrator die UAC systemweit deaktiviert, aber dies hat eine Reihe negativer Auswirkungen. Erstens beeinträchtigt dies die Sicherheit aller Administratorkonten, da alle Prozesse mit Administratoranmeldeinformationen ausgeführt werden, auch wenn die meisten Anwendungen diese nicht tatsächlich benötigen. Wenn UAC deaktiviert ist, kann eine Standardbenutzeranwendung, die ein ausnutzbares Sicherheitsrisiko verfügbar macht, möglicherweise verwendet werden, um private Informationen zu stehlen, Rootkits oder Spyware zu installieren, die Systemintegrität zu zerstören oder Angriffe auf andere Systeme zu hosten. Während UAC aktiviert ist, schränkt die Ausführung des Großteils der Software als Standardbenutzer den potenziellen Schaden durch einen solchen Fehler erheblich ein. Zweitens deaktiviert das Deaktivieren der benutzerkontenabhängigen Anwendungskompatibilität viele der Problemumgehungen für die Anwendungskompatibilität, die es echten Standardbenutzern ermöglichen, eine vielzahl von Anwendungen erfolgreich auszuführen. Das Deaktivieren der UAC sollte nie als Kompatibilitätsumgehung empfohlen werden.

Es ist wichtig zu beachten, dass Anwendungen versuchen sollten, nur standardbenutzerrechte zu verwenden, wenn dies überhaupt möglich ist. Administratoren können die Berechtigungen eines Prozesses leicht erhöhen, aber die Rechteerweiterung erfordert immer noch Benutzerinteraktion und Bestätigung jedes Mal, wenn eine Anwendung ausgeführt wird, die Administratoranmeldeinformationen erfordert. Diese Erhöhung muss auch zum Zeitpunkt des Programmstarts erfolgen, sodass die Anforderung von Administratoranmeldeinformationen auch für einen einzelnen Vorgang erfordert, dass das System für die gesamte Ausführungszeit der Anwendung einem größeren Risiko ausgesetzt wird. Standardbenutzer ohne Möglichkeit, ihre Berechtigungen zu erhöhen, sind auch in familien- und geschäftlichen Einstellungen üblich. "Als Administrator ausführen" ist keine gute Problemumgehung für die Kompatibilität, macht den Benutzer und das System einem größeren Sicherheitsrisiko ausgesetzt und sorgt in vielen Situationen für Frust für Benutzer.

> [!Note]  
> Das in Windows Vista eingeführte Feature "Benutzerkontensteuerung" ist auch in Windows 7 verfügbar. Die Benutzerfreundlichkeit bei der Arbeit mit den verschiedenen Systemfeatures wurde in Bezug auf die Benutzerkontensteuerung verbessert, aber die Auswirkungen auf Anwendungen sind im Grunde gleich. Alle Empfehlungen Windows Vista in diesem Artikel gelten auch für Windows 7. Ausführliche Informationen zu den UAC-Ui-Änderungen für Windows 7 finden Sie unter Benutzeroberfläche – [Dialogfeld "Benutzerkontensteuerung".](../win7appqual/user-interface---user-account-control-dialog-updates.md)

 

## <a name="user-accounts-in-windows-vista"></a>Benutzerkonten in Windows Vista

Windows Vista kategorisiert jeden Benutzer in zwei Benutzerkontotypen: Administratoren und Standardbenutzer.

Ein Standardbenutzerkonto ähnelt einem eingeschränkten Benutzerkonto in Windows XP. Wie in Windows XP kann ein Standardbenutzer nicht in den Ordner Programme schreiben, nicht in den \_ HKEY LOCAL \_ MACHINE-Teil der Registrierung schreiben und keine Aufgaben ausführen, die das System ändern, z. B. die Installation eines Kernelmodustreibers oder den Zugriff auf Prozessräume auf Systemebene.

Das Administratorkonto hat sich seit der Veröffentlichung Windows XP erheblich geändert. Zuvor wurden allen Prozessen, die von einem Mitglied der Gruppe Administratoren gestartet wurden, Administratorrechte erteilt. Wenn UAC aktiviert ist, werden alle Prozesse mit Standardbenutzerberechtigungen ausgeführt, es sei denn, sie wurden ausdrücklich von einem Administrator erhöht. Dieser Unterschied macht Konten in der Gruppe "Administratoren" sicherer, indem das Sicherheitsrisiko reduziert wird, das durch potenzielle Fehler in den meisten Programmen entstehen kann.

Es ist wichtig, dass alle Anwendungen, insbesondere Spiele, effektiv und verantwortungsbewusst ausgeführt werden, wenn sie als Standardbenutzerprozess ausgeführt werden. Alle Vorgänge, die Administratorrechte erfordern, sollten entweder zur Installationszeit oder von Hilfsprogrammen ausgeführt werden, die explizit Administratoranmeldeinformationen anfordern. Während die Rechteerweiterung für ein Mitglied der Gruppe "Administratoren" recht trivial ist, müssen Standardbenutzer auf eine Person mit Administratoranmeldeinformationen zurückstellen, um ihr Kennwort physisch einzugeben, um Berechtigungen zu erhöhen. Da konten, die durch Die Jugendschutz geschützt werden, Standardbenutzer sein müssen, ist dies eine sehr häufige Situation für Spieler, die Windows Vista verwenden.

Wenn Ihr Spiel bereits mit eingeschränkten Benutzerkonten an Windows XP arbeitet, sollte der Wechsel zur Benutzerkontensteuerung auf Windows Vista sehr einfach sein. Der Großteil dieser Anwendungen funktioniert wie beschädigend, obwohl das Hinzufügen eines Anwendungsmanifests dringend empfohlen wird. (Manifeste werden weiter unten in diesem Thema unter [Festlegen der Ausführungsebene im Anwendungsmanifest](#setting-the-execution-level-in-the-application-manifest)beschrieben.)

## <a name="file-access-as-a-standard-user"></a>Dateizugriff als Standardbenutzer

Der Aspekt Ihres Spiels, der am stärksten von Standardbenutzereinschränkungen betroffen ist, ist die Organisation des Dateisystems und die Barrierefreiheit. Sie sollten nie davon ausgehen, dass Ihr Spiel Dateien in den Ordner schreiben kann, in dem Ihr Spiel installiert ist. In Windows Vista müssen z. B. die Berechtigungen eines Benutzers vom Betriebssystem erhöht werden, bevor eine Anwendung in den Ordner Programme schreiben kann. Um dies zu vermeiden, sollten Sie die Datendateien Ihres Spiels nach Umfang und Barrierefreiheit kategorisieren und die [**SHGetFolderPath-Funktion**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) zusammen mit den CSIDL-Konstanten verwenden, die von der Windows Shell bereitgestellt werden, um die entsprechenden Dateipfade zu generieren. Die CSIDL-Konstanten entsprechen bekannten Ordnern im Dateisystem, die vom Betriebssystem verwendet und zur Partitionierung globaler und benutzerspezifischer Dateien heraufgestuft werden.

Wenn Sie versuchen, eine Datei oder ein Verzeichnis in einem Ordner zu erstellen oder zu schreiben, der dem Prozess keine Schreibberechtigung erteilt, tritt unter Windows Vista ein Fehler auf, wenn die Anwendung nicht über Administratorrechte verfügt. Wenn Ihre ausführbare 32-Bit-Spieldatei im Legacymodus ausgeführt wird, da sie keine angeforderte Ausführungsebene deklariert hat, werden die Schreibvorgänge erfolgreich ausgeführt, aber sie unterliegen der Virtualisierung, wie im Abschnitt "UAC-Kompatibilität mit älteren Spielen" weiter unten in diesem Artikel beschrieben.

**Tabelle 1. Bekannte Ordner**



| CSIDL-Name             | Typischer Pfad (Windows Vista)                                                   | Standardbenutzerrechte | Administratorrechte | Zugriffsbereich | Beschreibung                                                                                                                      | Beispiele                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CSIDL \_ PERSONAL        | C: \\ \\ Benutzerbenutzername \\ Dokumente                                                | Lesen/Schreiben           | Lesen/Schreiben           | Per-User     | Benutzerspezifische Spieldateien, die gelesen und geändert werden und außerhalb des Spielkontexts bearbeitet werden können.                          | Screenshots. Gespeicherte Spieldateien mit einer Dateierweiterungszuordnung. |
| CSIDL \_ LOCAL \_ APPDATA  | C: \\ \\ Benutzerbenutzername \\ AppData \\ Local                                           | Lesen/Schreiben           | Lesen/Schreiben           | Per-User     | Benutzerspezifische Spieldateien, die gelesen und geändert werden und nur innerhalb des Spielkontexts verwendet werden.                                 | Spielcachedateien. Playerkonfigurationen.                          |
| CSIDL \_ COMMON \_ APPDATA | C: \\ ProgramData                                                                | Lesen/Schreiben, wenn Besitzer  | Lesen/Schreiben           | Allen Benutzern    | Spieldateien, die von einem Benutzer erstellt und von allen Benutzern gelesen werden können. Schreibzugriff wird nur dem Ersteller der Datei (Besitzer) gewährt. | Benutzerprofile                                                     |
| \_CSIDL-PROGRAMMDATEIEN \_  | C: \\ Programme<br/> oder<br/> C: \\ Programme (x86) <br/> | Schreibgeschützt            | Lesen/Schreiben           | Allen Benutzern    | Statische Spieldateien, die vom Installer des Spiels geschrieben wurden und von allen Benutzern gelesen werden.                                                    | Spielressourcen, z. B. Materialien und Gitternetze.                        |



 

Ihr Spiel wird in der Regel in einem Ordner unter dem Ordner installiert, der durch die \_ CSIDL PROGRAM \_ FILES-Konstante dargestellt wird. Dies ist jedoch nicht immer der Fall. Sie sollten stattdessen einen relativen Pfad aus Ihrer ausführbaren Datei verwenden, wenn Sie Pfadzeichenfolgen zu Dateien oder Verzeichnissen im Installationsordner generieren.

Sie sollten auch von hart codierten Annahmen über die bekannten Ordnerpfade absehen. Auf Windows XP Professional 64-Bit Edition und Windows Vista x64 lautet der Pfad der Programmdateien beispielsweise C: \\ Programme (x86) für 32-Bit-Programme und C: \\ Programme für 64-Bit-Programme. Diese bekannten Pfade werden von Windows XP geändert, und Benutzer können den Speicherort vieler dieser Ordner neu konfigurieren und sie sogar auf verschiedenen Laufwerken finden. Verwenden Sie daher immer die CSIDL-Konstanten, um Verwirrung und potenzielle Probleme zu vermeiden. Windows Setup versteht diese bekannten Ordnerspeicherorte und verschiebe die Daten beim Upgrade des Betriebssystems von Windows XP. Im Gegensatz dazu kann die Verwendung von nicht standardmäßigen Speicherorten oder hart codierten Pfaden nach einem Betriebssystemupgrade fehlschlagen.

Beachten Sie die geringfügigen Benutzerfreundlichkeitsunterschiede zwischen den benutzerspezifischen Ordnern, die von CSIDL \_ PERSONAL und CSIDL LOCAL APPDATA angegeben \_ \_ werden. Es wird empfohlen, die CSIDL-Konstante auszuwählen, die zum Schreiben einer Datei verwendet werden soll, indem Sie CSIDL \_ PERSONAL verwenden, wenn der Benutzer mit der Datei interagieren soll, z. B. doppelklicken, um sie in einem Tool oder einer Anwendung zu öffnen, und CSIDL LOCAL APPDATA für andere Dateien zu \_ \_ verwenden. Beide Ordner können von Ihrer Anwendung genutzt werden, um benutzerspezifische Datendateien zu speichern und zu organisieren, da es keinen Unterschied in ihrem Zugriffsbereich oder ihrer Berechtigungsebene gibt. Achten Sie darauf, Pfadnamen zu erstellen, die eindeutig genug sind, um nicht mit anderen Anwendungen in Konflikt zu geraten, aber kurz genug sind, um die Anzahl der Zeichen im vollständigen Pfad kleiner als der Wert von MAX \_ PATH, 260, zu halten.

Der folgende Code enthält ein Beispiel für das Schreiben einer Datei in einen bekannten Ordner:

``` syntax
#include <windows.h>
#include <shlobj.h>
#include <shlwapi.h>
        ...
        ...
        ...
        TCHAR strPath[MAX_PATH];
        if( SUCCEEDED(
        SHGetFolderPath( NULL, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, strPath ) ) )
        {
        PathAppend( strPath, TEXT( "Company Name\\Title" ) );

        if( !PathFileExists( strPath ) )
        {
        if( ERROR_SUCCESS != SHCreateDirectoryEx( NULL, strPath, NULL ) )
        return E_FAIL;
        }

        PathAppend( strPath, TEXT( "gamefile.txt" ) );

        // strPath is now something like:
        // C:\Users\<current user>\Documents\Company Name\Title\gamefile.txt
        // Open the file for writing
        HANDLE hFile = CreateFile(strPath, GENERIC_WRITE, NULL, NULL, CREATE_ALWAYS, FILE_ATTRIBUTE_NORMAL, NULL);

        if( INVALID_HANDLE_VALUE != hFile )
        {
        // TODO: Write to file
        CloseHandle(hFile);
        }
        }
```

## <a name="registry-access-as-a-standard-user"></a>Registrierungszugriff als Standardbenutzer

Der Registrierungszugriff durch einen Standardbenutzer ist auf ähnliche Weise eingeschränkt wie das Dateisystem. Einem Standardbenutzer wird Lesezugriff auf alle Schlüssel in der Registrierung gewährt. Schreibzugriff wird jedoch nur der Unterstruktur HKEY \_ CURRENT \_ USER (HKCU) gewährt, die intern dem benutzerspezifischen Unterschlüssel HKEY \_ USERS Security ID \\ (SID) des aktuellen Benutzers zugeordnet ist. Eine Anwendung, die in einen anderen Registrierungsspeicherort als HKEY CURRENT USER schreiben muss, \_ \_ erfordert Administratorrechte.

Wenn die 32-Bit-Anwendung im Manifest keine angeforderte Ausführungsebene enthält, werden alle Schreibvorgänge in HKEY \_ LOCAL \_ MACHINE Software \\ virtualisiert, während Schreibvorgänge an andere Speicherorte außerhalb von HKEY \_ CURRENT USER \_ fehlschlagen.

Das Speichern persistenter Daten in der Registrierung, z. B. die Konfiguration eines Benutzers, wird nicht empfohlen. Die bevorzugte Methode zum Speichern persistenter Daten aus Ihrem Spiel besteht darin, die Daten durch Aufrufen von [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) in das Dateisystem zu schreiben und den Wert einer CSIDL-Konstante abzurufen, die im vorherigen Abschnitt beschrieben wurde.

## <a name="privilege-elevation"></a>Rechteerweiterungen

In Windows Vista muss jede Anwendung, die Administratorrechte erfordert, eine Anforderung für eine administrative Ausführungsebene in ihrem Manifest deklarieren (wie im nächsten Abschnitt [Festlegen der Ausführungsebene im Anwendungsmanifest](#setting-the-execution-level-in-the-application-manifest)beschrieben).

Die Rechteerweiterung ist bekanntlich das Verfahren, das von der UAC zum Heraufstufen eines Prozesses in einen Administrativen Prozess gesteuert wird. Die Berechtigungen eines Prozesses können nur zum Zeitpunkt der Erstellung erhöht werden. Nach der Erstellung wird ein Prozess nie auf eine höhere Berechtigungsstufe heraufgestuft. Aus diesem Grund. -Vorgänge, die Administratoranmeldeinformationen erfordern, sollten isoliert werden, um Installationsprogramme und andere Hilfsprogramme zu trennen.

Bei der Ausführung eines Programms überprüft die benutzerkontensteuerung die angeforderte Ausführungsebene im Manifest. Wenn erhöhte Rechte erforderlich sind, fordert die Benutzerkontensteuerung den aktuellen Benutzer mit einem von zwei Standarddialogfeldern auf: einem für einen Standardbenutzer und einem für einen Administrator.

Wenn der aktuelle Benutzer ein Standardbenutzer ist, fordert die Benutzerkontenverwaltung den Benutzer zur Eingabe der Anmeldeinformationen eines Administrators auf, bevor das Programm ausgeführt werden kann.

**Abbildung 1: Auffordern eines Standardbenutzers zur Eingabe von Anmeldeinformationen für ein Administratorkonto**

![Eingabeaufforderung für einen Standardbenutzer zur Eingabe von Anmeldeinformationen für ein Administratorkonto](images/uac-prompt-elevation.jpg)

Wenn der aktuelle Benutzer Administrator ist, fordert die Benutzerkontenverwaltung den Benutzer zur Eingabe der Berechtigung auf, bevor das Programm ausgeführt werden kann.

**Abbildung 2. Auffordern eines Administrators zum Autorisieren von Änderungen am Computer**

![Aufforderung zum Autorisieren von Änderungen am Computer durch einen Administrator](images/uac-prompt-authorization.jpg)

Der Anwendung werden nur Dann Administratorrechte gewährt, wenn ein Standardbenutzer die richtigen Administratoranmeldeinformationen bereitstellt oder ein Administrator eine Bestätigung bereitstellt. Andernfalls wird die Anwendung beendet.

Es ist wichtig zu beachten, dass ein Prozess mit erhöhten Rechten als Administrator ausgeführt wird, der Anmeldeinformationen in der UAC-Eingabeaufforderung eingegeben hat, anstatt als Standardbenutzer, der derzeit angemeldet ist. Dies ähnelt **RunAs** in Windows XP. Der Prozess mit erhöhten Rechten ruft beim Zugriff auf benutzerspezifische Daten den Ordner und die Registrierungsschlüssel des Administrators ab, und alle Programme, die der erweiterte Prozess startet, erben ebenfalls sowohl die Administratorrechte als auch die Speicherorte des Benutzerkontos. Für Administratoren, die zur Bestätigung aufgefordert werden **(Weiter** oder **Abbrechen),** entsprechen diese Speicherorte den Standorten des aktuellen Benutzers. Im Allgemeinen sollten Prozesse, für die erhöhte Rechte erforderlich sind, jedoch nicht auf Benutzerdaten ausgeführt werden. Beachten Sie, dass sich dies erheblich auf die Funktionsweise Ihres Installationsprogramms auswirken kann. Wenn das Installationsprogramm, das als Administrator ausgeführt wird, in HKCU oder in das Profil eines Benutzers schreibt, kann es sehr gut sein, an den falschen Speicherort zu schreiben. Erwägen Sie, diese Benutzerwerte bei der ersten Ausführung des Spiels zu erstellen.

## <a name="uac-implications-with-createprocess"></a>Auswirkungen der UAC mit CreateProcess()

Der UAC-Erhöhungsmechanismus wird nicht von einem Aufruf der Win32 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)()-Funktion aufgerufen, um eine ausführbare Datei zu starten, die so konfiguriert ist, dass sie eine höhere Ausführungsebene als der aktuelle Prozess erfordert. Daher schlägt der Aufruf von **CreateProcess**() fehl, wenn [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)() ERROR ELEVATION REQUIRED zurückgibt. \_ \_ **CreateProcess**() ist nur erfolgreich, wenn die Ausführungsebene des Aufgerufenen gleich oder kleiner als die des Aufrufers ist. Ein Prozess ohne erhöhte Rechte, der Prozesse mit erhöhten Rechten erzeugen muss, sollte dies mithilfe der [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)()-Funktion tun. Dies führt dazu, dass der UAC-Erhöhungsmechanismus über die Shell ausgelöst wird.

## <a name="setting-the-execution-level-in-the-application-manifest"></a>Festlegen der Ausführungsebene im Anwendungsmanifest

Sie deklarieren die angeforderte Ausführungsebene Ihres Spiels, indem Sie dem Manifest der Anwendung eine Erweiterung hinzufügen. Der folgende XML-Code zeigt die minimale Konfiguration, die zum Festlegen der Ausführungsebene für eine Anwendung erforderlich ist:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
        <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
                <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
        </ms_asmv2:security>
    </ms_asmv2:trustInfo>
</assembly>
```

Im vorangehenden Code wird das Betriebssystem darüber informiert, dass das Spiel nur Standardbenutzerberechtigungen mit dem folgenden Tag erfordert:

``` syntax
<ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
```

Durch explizites Festlegen von requestedExecutionLevel auf "asInvoker" bestätigt dieses Beispiel dem Betriebssystem, dass sich das Spiel ohne Administratorrechte ordnungsgemäß verhält. Daher deaktiviert UAC die Virtualisierung und führt das Spiel mit den gleichen Berechtigungen wie der Aufrufer aus, bei dem es sich in der Regel um Standardbenutzerberechtigungen handelt, da Windows Explorer als Standardbenutzer ausgeführt wird.

Das Betriebssystem kann informiert werden, wenn ein Spiel eine Erhöhung der Administratorrechte erfordert, indem "asInvoker" durch "requireAdministrator" ersetzt wird, um das folgende Tag zu erstellen:

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Bei dieser Konfiguration fordert das Betriebssystem den aktuellen Benutzer bei jeder Ausführung des Spiels mit einem der Standardmäßigen UAC-Dialogfelder zur Erhöhung der Rechte auf. Es wird dringend empfohlen, dass kein Spiel Administratorberechtigungen benötigt, da dieser Dialog nicht nur schnell ungärr wird, sondern auch das Spiel mit den Jugendschutzmechanismen inkompatibel macht. Überlegen Sie sehr sorgfältig, bevor Sie diese Anforderung einer ausführbaren Datei hinzufügen.

Ein häufiges Missverständnis besteht darin, dass das Hinzufügen eines Manifests, das requestedExecutionLevel auf "requireAdministrator" festlegt, die Notwendigkeit einer Eingabeaufforderung für erhöhte Rechte umgeht. Das ist falsch. Sie verhindert einfach, dass das Betriebssystem erraten kann, ob Ihre Setup- oder Updateanwendung Administratorrechte benötigt. Der Benutzer wird weiterhin aufgefordert, erhöhte Rechte zu autorisieren.

Windows überprüft die Signatur einer Anwendung, die für erhöhte Rechte markiert ist, bevor die UAC-Eingabeaufforderung angezeigt wird. Eine große ausführbare Datei, die für erhöhte Rechte markiert ist, dauert länger als eine kleine ausführbare Datei und länger als eine ausführbare Datei, die als "asInvoker" markiert ist. Ausführbare Setupdateien, die selbstextrahiert werden, sollten daher als "asInvoker" markiert werden, und alle Teile, die als "requireAdministrator" gekennzeichnet werden müssen, sollten in einer separaten ausführbaren Hilfsdatei platziert werden.

Das attribut uiAccess, das in den vorherigen Beispielen gezeigt wird, sollte für Spiele immer FALSE sein. Dieses Attribut gibt an, ob Benutzeroberflächenautomatisierungs-Clients Zugriff auf die benutzeroberfläche des geschützten Systems haben, und hat besondere Auswirkungen auf die Sicherheit, wenn sie auf TRUE festgelegt ist.

## <a name="embedding-a-manifest-in-visual-studio"></a>Einbetten eines Manifests in Visual Studio

Die Manifestunterstützung wurde Visual Studio ab VS2005 hinzugefügt. Standardmäßig wird für eine ausführbare Datei, die in Visual Studio 2005 (oder neuer) erstellt wurde, ein automatisch generiertes Manifest als Teil des Buildprozesses eingebettet. Der Inhalt des automatisch generierten Manifests hängt von bestimmten Projektkonfigurationen ab, die Sie im Dialogfeld "Projekteigenschaften" angeben.

Das Manifest, das von Visual Studio 2005 automatisch generiert wird, enthält keinen &lt; trustInfo-Block, &gt; da es keine Möglichkeit gibt, die UAC-Ausführungsebene in den Projekteigenschaften zu konfigurieren. Die bevorzugte Methode zum Hinzufügen dieser Informationen besteht darin, VS2005 ein benutzerdefiniertes Manifest, das den trustInfo-Block enthält, mit dem automatisch generierten Manifest zusammenführen zu &lt; &gt; lassen. Dies ist so einfach wie das Hinzufügen einer \* MANIFEST-Datei zu Ihrer Projektmappe, die den im vorherigen Abschnitt aufgeführten XML-Code enthält. Wenn Visual Studio in Ihrer Projektmappe auf eine MANIFEST-Datei trifft, wird automatisch das Manifesttool (mt.exe) aufgerufen, um die MANIFEST-Dateien mit der automatisch generierten Datei zusammenzuführen.

> [!Note]  
> Im manifest-Tool (mt.exe), das von Visual Studio 2005 bereitgestellt wird, gibt es einen Fehler, der zu einem zusammengeführten und eingebetteten Manifest führt, das Probleme verursachen kann, wenn die ausführbare Datei auf Windows XP vor SP3 ausgeführt wird. Der Fehler ist das Ergebnis der Neudefinition des Standardnamespace durch das Tool bei der Deklaration des &lt; &gt; trustInfo-Blocks. Glücklicherweise ist es einfach, das Problem vollständig zu umgehen, indem sie explizit einen anderen Namespace im trustInfo-Block deklarieren &lt; &gt; und die untergeordneten Knoten auf den neuen Namespace einteilen. Der im vorherigen Abschnitt bereitgestellte XML-Code veranschaulicht diese Korrektur.

 

Ein Nachteil bei der Verwendung des in Visual Studio 2005 enthaltenen tools mt.exe besteht darin, dass beim Verarbeiten des trustInfo-Blocks eine Warnung generiert wird, &lt; da das Tool kein &gt; aktualisiertes Schema für die Xml-Überprüfung enthält. Um diese Warnung zu beheben, wird empfohlen, alle mt.exe Dateien im Installationsverzeichnis Visual Studio 2005 (es gibt mehrere Instanzen) durch die mt.exe zu ersetzen, die im neuesten Windows SDK bereitgestellt werden.

Ab Visual Studio 2008 können Sie jetzt die Ausführungsebene einer Anwendung im Dialogfeld mit den Projekteigenschaften (Abbildung 3) oder mithilfe des /MANIFESTUAC-Linkerflags angeben. Wenn Sie diese Optionen festlegen, generiert Visual Studio 2008 automatisch ein Manifest mit dem entsprechenden trustInfo-Block und bettet es &lt; in die ausführbare Datei &gt; ein.

**Abbildung 3: Festlegen der Ausführungsebene in Visual Studio 2008**

![Festlegen der Ausführungsebene in Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

Das Einbetten eines Manifests in ältere Versionen von Visual Studio ohne Manifestunterstützung ist weiterhin möglich, erfordert jedoch mehr Arbeit vom Entwickler. Ein Beispiel hierfür finden Sie im Projekt Visual Studio 2003, das in einem beliebigen Beispiel im DirectX SDK vor der Version von März 2008 enthalten ist.

## <a name="uac-compatibility-with-older-games"></a>UAC-Kompatibilität mit älteren Spielen

Wenn Ihr Spiel scheinbar eine Datei erfolgreich im Verzeichnis Programme speichert und lädt, aber keine Beweise für die Datei iOn Windows Vista vorliegen, wird jede 32-Bit-Anwendung, die keine angeforderte Ausführungsebene im Manifest enthält, als Legacyanwendung betrachtet. Vor Windows Vista wurden die meisten Anwendungen in der Regel von Benutzern mit Administratorrechten ausgeführt. Daher konnten diese Anwendungen Systemdateien und Registrierungsschlüssel frei lesen und schreiben, und viele Entwickler haben nicht die erforderlichen Änderungen vorgenommen, um auf eingeschränkten Benutzerkonten auf Windows XP ordnungsgemäß zu funktionieren. Auf Windows Vista würden diese Anwendungen nun jedoch aufgrund unzureichender Zugriffsberechtigungen unter dem neuen Sicherheitsmodell fehlschlagen, das die Standardbenutzerausführung für Legacyanwendungen erzwingt. Um die Auswirkungen zu minimieren, wurde die Virtualisierung auch zu Windows Vista hinzugefügt. Mit der Virtualisierung funktionieren Tausende von Legacyanwendungen weiterhin gut auf Windows Vista, ohne dass diese Anwendungen jederzeit über erhöhte Berechtigungen verfügen müssen, um nur bei wenigen kleineren Vorgängen erfolgreich zu sein. s gefunden, wahrscheinlich wird Ihr Spiel im Legacymodus ausgeführt und wurde einer Virtualisierung unterzogen.

Die Virtualisierung wirkt sich auf das Dateisystem und die Registrierung aus, indem systemabhängige Schreibvorgänge (und nachfolgende Datei- oder Registrierungsvorgänge) an einen Benutzerspeicherort innerhalb des Profils des aktuellen Benutzers umgeleitet werden. Wenn eine Anwendung beispielsweise versucht, in die folgende Datei zu schreiben:

<dl> C: \\ Programme Company Name Title \\ \\ \\config.ini  
</dl>

der Schreibzugriff wird automatisch an Folgenden umgeleitet:

<dl> C: \\ \\ Benutzerbenutzername \\ AppData \\ Local \\ VirtualStore \\ Program Files Company Name \\ Titleconfig.ini \\ \\  
</dl>

Ebenso, wenn eine Anwendung versucht, einen Registrierungswert wie den folgenden zu schreiben:

<dl> HKEY \_ LOCAL \_ MACHINE \\ Software \\ Company Name \\ Title  
</dl>

Stattdessen wird sie an Dies wird umgeleitet:

<dl> HKEY \_ CURRENT \_ USER \\ Software \\ Classes \\ VirtualStore \\ MACHINE \\ Software \\ Company Name \\ Title  
</dl>

Auf Dateien und Registrierungsschlüssel, die von der Virtualisierung betroffen sind, kann nur über Datei- und Registrierungsvorgänge von virtualisierten Anwendungen zugegriffen werden, die als aktueller Benutzer ausgeführt werden.

Es gibt jedoch viele Einschränkungen bei der Virtualisierung. Eine ist, dass 64-Bit-Anwendungen nie im Legacymodus für Kompatibilitätsvorgänge ausgeführt werden, die der Virtualisierung in 32-Bit-Anwendungen unterliegen, in 64-Bit-Anwendungen nur fehlschlagen. Wenn eine legacy-Anwendung, die als Standardbenutzer ausgeführt wird, versucht, einen beliebigen Typ von ausführbarer Datei an einen Speicherort zu schreiben, der Administratoranmeldeinformationen erfordert, tritt keine Virtualisierung auf, und der Schreibfehler tritt auf.

**Abbildung 4. Virtualisierungsprozess**

![Virtualisierungsprozess](images/uac-virtualization-process.jpg)

Wenn eine Legacyanwendung versucht, einen Lesevorgang an systemspezifischen Speicherorten im Dateisystem oder in der Registrierung zu versuchen, werden zuerst die virtuellen Speicherorte durchsucht. Wenn die Datei oder der Registrierungsschlüssel nicht gefunden wird, greifen das Betriebssystem auf die Standardsystemspeicherorte zu.

Die Virtualisierung wird aus nachfolgenden Versionen von Windows daher ist es wichtig, sich nicht auf dieses Feature zu verlassen. Stattdessen sollten Sie Ihr Anwendungsmanifest explizit für Standardbenutzer- oder Administratorrechte konfigurieren, da dadurch die Virtualisierung deaktiviert wird. Die Virtualisierung ist auch für Endbenutzer nicht offensichtlich. Obwohl die Virtualisierung die Ausführung Ihrer Anwendung ermöglicht, kann sie Supportanrufe generieren und die Problemlösung für diese Kunden erschweren.

Beachten Sie, dass die Virtualisierung ebenfalls deaktiviert ist, wenn die UAC deaktiviert ist. Wenn die Virtualisierung deaktiviert ist, verhalten sich Standardbenutzerkonten genau wie eingeschränkte Benutzerkonten in Windows XP, und Ältere Anwendungen funktionieren möglicherweise nicht ordnungsgemäß für Standardbenutzer, die andernfalls aufgrund der Virtualisierung erfolgreich waren.

## <a name="legacy-scenarios-and-manifests"></a>Legacyszenarien und Manifeste

In den meisten Verwendungsszenarien ist es für eine hervorragende UAC-Kompatibilität ausreichend, einfach den .exe mit den richtigen UAC-Manifestelementen zu markieren und sicherzustellen, dass die Anwendung als Standardbenutzer ordnungsgemäß funktioniert. Die meisten Gamer werden mit Windows Vista oder Windows 7 mit aktivierter Benutzerkontensteuerung ausgeführt. Für Windows XP und Benutzer unter Windows Vista oder Windows7 mit deaktivierter Benutzerkontensteuerung werden sie in der Regel mit Administratorkonten ausgeführt. Obwohl dies ein weniger sicherer Betriebsmodus ist, kommt es in der Regel nicht zu zusätzlichen Kompatibilitätsproblemen, obwohl die Deaktivierung der UAC auch die Virtualisierung deaktiviert.

Es gibt einen Sonderfall, der zu notieren ist, wenn das Programm im UAC-Manifest als "requireAdministrator" markiert ist. Auf Windows XP und Windows Vista oder Windows 7 mit deaktivierter Benutzerkontensteuerung werden die UAC-Manifestelemente vom System ignoriert. In diesem Fall führen Benutzer mit Administratorkonten immer alle Programme mit vollständigen Administratorrechten aus, und daher funktionieren diese Programme wie erwartet. Windows Eingeschränkte XP-Benutzer und Standardbenutzer, die unter Windows Vista oder Windows 7 ausgeführt werden, führen diese Programme jedoch immer mit eingeschränkten Rechten aus, und alle Vorgänge auf Administratorebene fehlschlagen. Daher wird empfohlen, dass Programme, die als "requiretAdministrator" gekennzeichnet sind, Beim Start [**IsUserAnAdmin**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) aufrufen und eine schwerwiegende Fehlermeldung anzeigen, wenn FALSE zurückgegeben wird. Im obigen Mehrheitsszenario ist dies immer erfolgreich, bietet jedoch eine bessere Benutzererfahrung und eine klare Fehlermeldung für diese seltene Situation.

## <a name="conclusion"></a>Zusammenfassung

Als Spieleentwickler, der die Windows-Benutzerumgebung anpeilt, ist es zwingend erforderlich, dass Sie Ihr Spiel so entwerfen, dass es effektiv und verantwortungsbewusst funktioniert. Die ausführbare Hauptdatei Ihres Spiels sollte nicht von Administratorrechten abhängig sein. Dies verhindert nicht nur die Darstellung von Eingabeaufforderungen zur Erhöhung bei jeder Ausführung Ihres Spiels, was sich negativ auf die allgemeine Benutzererfahrung auswirken kann, sondern ermöglicht es Ihrem Spiel auch, andere Features zu nutzen, die die Ausführung mit Standardbenutzerberechtigungen erfordern, z. B. Die Jugendschutzkontrollen.

Anwendungen, die ordnungsgemäß so konzipiert sind, dass sie mit den Anmeldeinformationen eines Standardbenutzers (oder eines eingeschränkten Benutzers) unter früheren Versionen von Windows funktionieren, sind nicht von der UAC,die ohne Erhöhung der Rechte ausgeführt werden, nicht von der UAC-Ausführung aus. Sie sollten jedoch ein Manifest mit der angeforderten Ausführungsebene enthalten, die auf "asInvoker" festgelegt ist, um den Anwendungsstandards für Vista zu entsprechen.

## <a name="further-reading"></a>Weitere Informationen

Um Unterstützung beim Entwerfen von Anwendungen für Windows Vista zu erhalten, die mit der Benutzerkontensteuerung kompatibel sind, laden Sie das folgende Whitepaper herunter: [Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10)).

Dieses Whitepaper enthält ausführliche Schritte zum Entwurfsprozess sowie Codebeispiele, Anforderungen und bewährte Methoden. In diesem Artikel werden auch die technischen Updates und Änderungen an der Benutzeroberfläche in Windows Vista detailst.

Weitere Informationen zur Benutzerkontensteuerung finden Sie unter [Windows Vista: Benutzerkontensteuerung](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) auf [Microsoft TechNet.](https://www.microsoft.com/technet/)

Eine weitere nützliche Ressource ist der Artikel [Teach Your Apps To Play Nicely with Windows Vista User Account Control](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control)aus dem MSDN [Magazine](/archive/msdn-magazine/msdn-magazine-issues), Januar 2007. In diesem Artikel werden allgemeine Probleme bei der Anwendungskompatibilität sowie die Vorteile und Probleme bei der Verwendung von Windows Installer-Paketen unter Windows Vista erläutert.

Weitere Informationen zum Fehler und zur Behebung von mt.exe, dem tool, das von Visual Studio 2005 zum automatischen Zusammenführen und Einbetten eines Manifests in eine ausführbare Datei verwendet wird, finden Sie unter [Exploring Manifests Part 2: Default Namespaces and UAC Manifests in Windows Vista](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) (Erkunden von Manifesten Teil 2: Standardnamespaces und UAC-Manifeste in Windows Vista) im Blog von Chris Vista auf [MSDN](/archive/blogs/).

 

