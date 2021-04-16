---
title: Benutzerkontensteuerung für Spieleentwickler
description: In diesem Artikel werden die Richtlinien und bewährten Methoden für Spieleentwickler beschrieben, die mit dem in Windows Vista eingeführten Sicherheits Feature der Benutzerkontensteuerung (User Account Control, UAC) effektiv arbeiten.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d5533a3fbdd349cc25dfde501a234bbd7b05b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390625"
---
# <a name="user-account-control-for-game-developers"></a>Benutzerkontensteuerung für Spieleentwickler

In diesem Artikel werden die Richtlinien und bewährten Methoden für Spieleentwickler beschrieben, die mit dem in Windows Vista eingeführten Sicherheits Feature der Benutzerkontensteuerung (User Account Control, UAC) effektiv arbeiten.

-   [Übersicht über die Benutzerkontensteuerung](#overview-of-user-account-control)
-   [Benutzerkonten in Windows Vista](#user-accounts-in-windows-vista)
-   [Dateizugriff als Standard Benutzer](#file-access-as-a-standard-user)
-   [Registrierungs Zugriff als Standard Benutzer](#registry-access-as-a-standard-user)
-   [Rechteerweiterungen](#privilege-elevation)
-   [UAC-Implikationen mit "kreateprocess ()"](#uac-implications-with-createprocess)
-   [Festlegen der Ausführungs Ebene im Anwendungs Manifest](#setting-the-execution-level-in-the-application-manifest)
-   [Einbetten eines Manifests in Visual Studio](#embedding-a-manifest-in-visual-studio)
-   [UAC-Kompatibilität mit älteren spielen](#uac-compatibility-with-older-games)
-   [Legacy Szenarios und Manifeste](#legacy-scenarios-and-manifests)
-   [Zusammenfassung](#conclusion)
-   [Weitere Informationen](#further-reading)

## <a name="overview-of-user-account-control"></a>Übersicht über die Benutzerkontensteuerung

Die in Windows Vista eingeführte Benutzerkontensteuerung (User Account Control, UAC) ist ein Sicherheits Feature, das dazu dient, böswillige Angreifer daran zu hindern, Schwachstellen oder Fehler in häufig verwendeten Anwendungen zu verwenden, um das Betriebssystem oder andere installierte Programme zu ändern. Dies wird erreicht, indem die meisten Programme und Prozesse als Standard Benutzer (auch als eingeschränkter Benutzer, eingeschränkter Benutzer oder Least-Privileged Benutzer bezeichnet) ausgeführt werden, auch wenn das Konto des aktuellen Benutzers über Administrator Anmelde Informationen verfügt. Ein Prozess mit Standardbenutzer Berechtigungen weist viele inhärente Einschränkungen auf, die eine systemweite Änderung verhindern.

UAC ist auch für die Berechtigungs Erweiterung eines Prozesses mithilfe eines dialogbasierten Authentifizierungs Schemas verantwortlich, das bei der Ausführung bestimmter Prozesse initiiert wurde, die als erforderliches Administrator Recht festgelegt sind. Die Rechte Erweiterung ermöglicht es Administratoren, die Mehrzahl Ihrer Anwendungen auf einer sicheren Berechtigungsebene (identisch mit allen anderen Standard Benutzern) auszuführen, aber auch Prozesse und Vorgänge zuzulassen, für die Administratorrechte erforderlich sind. UAC unterstützt die Authentifizierung über die Schulter, sodass ein Administrator einem Programm erweiterte Berechtigungen erteilen kann, während ein Standardbenutzer zurzeit beim System angemeldet ist.

Die UAC-Funktion ist standardmäßig aktiviert. Es ist zwar möglich, dass ein Administrator die systemweite UAC-systemweite deaktiviert, aber dies hat eine Reihe negativer Auswirkungen. Erstens wird die Sicherheit aller Administrator Konten dadurch geschwächt, dass alle Prozesse mit Administrator Anmelde Informationen ausgeführt werden, selbst wenn Sie von den meisten Anwendungen nicht tatsächlich benötigt werden. Wenn UAC deaktiviert ist, kann eine Standardbenutzer Anwendung, die eine ausnutzbare Sicherheitslücke in der Sicherheit verfügbar macht, zum stehlen privater Informationen, zum Installieren von Rootkits oder Spyware, zum zerstören der Systemintegrität oder zum Hosten von Zombie Angriffen auf anderen Systemen verwendet werden. Während bei aktivierter Benutzerkontensteuerung die Mehrzahl der Software als Standardbenutzer ausgeführt wird, werden die potenziellen Schäden durch einen solchen Fehler erheblich eingeschränkt. Zweitens werden bei der Deaktivierung der Benutzerkontensteuerung viele der Problem Umgehungen für die Anwendungs Kompatibilität deaktiviert, mit denen echte Standardbenutzer eine große Bandbreite von Anwendungen erfolgreich ausführen können. Das Deaktivieren von UAC sollte nie als Kompatibilitätsproblem Umgehung empfohlen werden.

Es ist wichtig zu beachten, dass Anwendungen nur dann die Standardbenutzer Rechte verwenden sollten, wenn dies möglich ist. Administratoren können die Berechtigungen eines Prozesses zwar problemlos erhöhen, die Erhöhung erfordert jedoch immer noch Benutzerinteraktion und-Bestätigung, wenn eine Anwendung ausgeführt wird, für die administrative Anmelde Informationen erforderlich sind. Diese Erhöhung muss auch zu dem Zeitpunkt erfolgen, zu dem das Programm gestartet wird. Wenn Sie also administrative Anmelde Informationen auch für einen einzelnen Vorgang benötigen, ist es erforderlich, dass das System für die gesamte laufende Laufzeit der Anwendung stärker gefährdet wird. Standard Benutzer, die keine Rechte haben, ihre Berechtigungen zu erhöhen, sind auch in den Einstellungen für Familie und Geschäftsumgebungen üblich. "Als Administrator ausführen" ist keine gute Lösung für die Kompatibilität, macht dem Benutzer und dem System ein höheres Sicherheitsrisiko und führt in vielen Fällen zu einer Frustration für Benutzer.

> [!Note]  
> Das in Windows Vista eingeführte Feature "Benutzerkontensteuerung" ist auch in Windows 7 enthalten. Obwohl die Benutzererfahrung bei der Arbeit mit den verschiedenen Systemfunktionen in Bezug auf die Benutzerkontensteuerung verbessert wurde, sind die Auswirkungen auf Anwendungen im Grunde genommen identisch. Alle Windows Vista-Empfehlungen in diesem Artikel gelten auch für Windows 7. Ausführliche Informationen zu den Änderungen der UAC-Benutzeroberfläche für Windows 7 finden Sie unter [Benutzeroberfläche-Dialog Informationen zur Benutzerkontensteuerung](../win7appqual/user-interface---user-account-control-dialog-updates.md).

 

## <a name="user-accounts-in-windows-vista"></a>Benutzerkonten in Windows Vista

In Windows Vista werden alle Benutzer in zwei Benutzerkonto Typen kategorisiert: Administratoren und Standardbenutzer.

Ein Standardbenutzer Konto ähnelt einem eingeschränkten Benutzerkonto in Windows XP. Wie in Windows XP kann ein Standardbenutzer nicht in den Ordner "Programme" schreiben, kann nicht in den lokalen HKEY \_ \_ -Computerbereich der Registrierung schreiben und kann keine Aufgaben ausführen, die das System ändern, wie z. b. das Installieren eines Kernelmodustreibers oder das Zugreifen auf Systemebene-Prozess Räume.

Das Administrator Konto wurde seit der Veröffentlichung von Windows XP erheblich geändert. Bisher erhielten alle Prozesse, die von einem Mitglied der Gruppe "Administratoren" gestartet wurden, Administratorrechte. Wenn UAC aktiviert ist, werden alle Prozesse mit Standardbenutzer Berechtigungen ausgeführt, sofern diese nicht ausdrücklich von einem Administrator herauf gestuft werden. Dieser Unterschied bewirkt, dass Konten in der Administratoren Gruppe sicherer werden, indem das Sicherheitsrisiko reduziert wird, das durch potenzielle Fehler in den meisten Programmen verursacht wird.

Es ist wichtig, dass alle Anwendungen, insbesondere Spiele, effektiv und verantwortungsvoll arbeiten, wenn Sie als Standardbenutzer Prozess ausgeführt werden. Alle Vorgänge, für die Administratorrechte erforderlich sind, sollten entweder zur Installationszeit oder durch Hilfsprogramme erfolgen, die explizit administrative Anmelde Informationen anfordern. Obwohl die Rechte Erweiterung für ein Mitglied der Gruppe "Administratoren" Recht einfach ist, müssen Standardbenutzer eine Person mit Administrator Anmelde Informationen zur physischen Eingabe Ihres Kennworts zur Erhöhung der Berechtigungen zurückstellen. Da Konten, die von Eltern Kontrollen geschützt sind, Standardbenutzer sein müssen, ist dies eine gängige Situation für Spieler, die Windows Vista verwenden.

Wenn Ihr Spiel bereits unter Windows XP mit eingeschränkten Benutzerkonten funktioniert, sollte der Umstieg auf die Benutzerkontensteuerung unter Windows Vista sehr einfach sein. Der Großteil dieser Anwendungen funktioniert unverändert, obwohl das Hinzufügen eines Anwendungs Manifests dringend empfohlen wird. (Manifeste werden weiter unten in diesem Thema unter [Festlegen der Ausführungs Ebene im Anwendungs Manifest](#setting-the-execution-level-in-the-application-manifest)beschrieben.)

## <a name="file-access-as-a-standard-user"></a>Dateizugriff als Standard Benutzer

Der Aspekt Ihres Spiels, der am meisten von Standardbenutzer Einschränkungen betroffen ist, ist die Dateisystem Organisation und Barrierefreiheit. Sie sollten niemals davon ausgehen, dass Ihr Spieldateien in den Ordner schreiben kann, in dem das Spiel installiert ist. In Windows Vista muss beispielsweise eine Benutzer Berechtigung vom Betriebssystem erhöht werden, damit eine Anwendung in den Ordner "Programme" schreiben kann. Um dies zu vermeiden, sollten Sie die Datendateien Ihres Spiels nach Bereich und Barrierefreiheit kategorisieren und die [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) -Funktion zusammen mit den CSIDL-Konstanten, die von der Windows-Shell bereitgestellt werden, verwenden, um die entsprechenden Dateipfade zu generieren. Die CSIDL-Konstanten entsprechen bekannten Ordnern im Dateisystem, die vom Betriebssystem verwendet und für die Partitionierung globaler und Benutzer spezifischer Dateien herauf gestuft werden.

Der Versuch, eine Datei oder ein Verzeichnis in einem Ordner zu erstellen oder zu schreiben, der keine Schreib Berechtigung für den Prozess gewährt, schlägt unter Windows Vista fehl, wenn die Anwendung nicht über Administratorrechte verfügt. Wenn die ausführbare 32-Bit-Spiel Datei im Legacy Modus ausgeführt wird, weil Sie keine angeforderte Ausführungs Ebene deklariert hat, sind Ihre Schreibvorgänge erfolgreich, aber Sie werden der Virtualisierung unterzogen, wie im Abschnitt "UAC-Kompatibilität mit älteren spielen" weiter unten in diesem Artikel beschrieben.

**Tabelle 1. Bekannte Ordner**



| CSIDL-Name             | Typischer Pfad (Windows Vista)                                                   | Standard Benutzerrechte | Administratorrechte | Zugriffsbereich | BESCHREIBUNG                                                                                                                      | Beispiele                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CSIDL \_ Personal        | C: \\ Benutzer \\ Benutzername \\ Dokumente                                                | Lesen/Schreiben           | Lesen/Schreiben           | Per-User     | Benutzerspezifische Spieldateien, die gelesen und geändert werden und außerhalb des Spiel Kontexts bearbeitet werden können.                          | Bildschirmaufnahmen. Die Spieldateien wurden mit einer Datei Erweiterungs Zuordnung gespeichert. |
| lokale CSIDL- \_ \_ AppData  | C: \\ Benutzer \\ Benutzername \\ AppData \\ local                                           | Lesen/Schreiben           | Lesen/Schreiben           | Per-User     | Benutzerspezifische Spieldateien, die gelesen und geändert werden und nur innerhalb des Spiel Kontexts verwendet werden.                                 | Spiele Cache Dateien. Player Konfigurationen.                          |
| Allgemeine CSIDL- \_ \_ AppData | C: \\ programmdata                                                                | Lese-/Schreibzugriff bei Besitzer  | Lesen/Schreiben           | Allen Benutzern    | Spieldateien, die von einem Benutzer erstellt und von allen Benutzern gelesen werden können. Schreibzugriff wird nur dem Ersteller der Datei (Besitzer) gewährt. | Benutzerprofile                                                     |
| CSIDL- \_ Programm \_ Dateien  | C: \\ Programmdateien<br/> oder<br/> C: \\ Programmdateien (x86) <br/> | Nur Lesezugriff            | Lesen/Schreiben           | Allen Benutzern    | Statische Spieldateien, die vom Spiel-Installer geschrieben wurden und von allen Benutzern gelesen werden.                                                    | Spiel Ressourcen, z. b. Material und Meshes.                        |



 

Das Spiel wird in der Regel in einem Ordner unter dem Ordner installiert, der durch die CSIDL- \_ Programmdateien-Konstante dargestellt wird \_ . Dies ist jedoch nicht immer der Fall. Sie sollten stattdessen einen relativen Pfad aus der ausführbaren Datei verwenden, wenn Sie Pfad Zeichenfolgen zu Dateien oder Verzeichnissen erstellen, die sich unter dem Installationsordner befinden.

Sie sollten auch von hart codierten Annahmen über die bekannten Ordner Pfade verzichten. In Windows XP Professional 64-Bit Edition und Windows Vista x64 lautet der Pfad der Programmdateien z. b. c: \\ Program Files (x86) für 32-Bit-Programme und c: \\ Program Files für 64-Bit-Programme. Diese bekannten Pfade werden von Windows XP geändert, und Benutzer können den Speicherort für viele dieser Ordner neu konfigurieren und sogar auf verschiedenen Laufwerken suchen. Verwenden Sie daher immer die CSIDL-Konstanten, um Verwirrung und potenzielle Probleme zu vermeiden. Windows Setup diese bekannten Ordner Speicherorte versteht und die Daten bei der Aktualisierung des Betriebssystems von Windows XP verschieben. im Gegensatz dazu kann die Verwendung von nicht standardmäßigen Speicherorten oder hart codierten Pfaden nach einem Betriebssystem Upgrade fehlschlagen.

Die geringfügigen Nutzbarkeits Unterschiede zwischen den benutzerspezifischen Ordnern, die durch CSIDL \_ Personal und CSIDL \_ local \_ AppData angegeben werden, sollten berücksichtigt werden. Die empfohlene Vorgehensweise zum Auswählen der zum Schreiben einer Datei zu verwendenden CSIDL-Konstante besteht darin, CSIDL persönlich zu verwenden \_ , wenn der Benutzer mit der Datei interagieren soll, z. b. durch Doppelklicken darauf, um ihn in einem Tool oder einer Anwendung zu öffnen, und für die Verwendung von lokalen APPDATA (CSIDL) \_ \_ für andere Dateien. Beide Ordner können von Ihrer Anwendung genutzt werden, um benutzerspezifische Datendateien zu speichern und zu organisieren, da es keinen Unterschied in Bezug auf den Zugriffs Bereich oder die Berechtigungsebene gibt. Es sollte darauf geachtet werden, Pfadnamen zu erstellen, die eindeutig genug sind, um nicht mit anderen Anwendungen zu kollidieren, aber kurz genug, um die Anzahl der Zeichen im vollständigen Pfad kleiner als der Wert von "Max \_ path, 260" beizubehalten.

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

## <a name="registry-access-as-a-standard-user"></a>Registrierungs Zugriff als Standard Benutzer

Der Registrierungs Zugriff durch einen Standardbenutzer ist auf ähnliche Weise wie das Dateisystem eingeschränkt. Einem Standardbenutzer ist Lesezugriff auf alle Schlüssel in der Registrierung gestattet. der Schreibzugriff wird jedoch nur der \_ \_ HKCU-Unterstruktur (HKEY Current User) gewährt, die der benutzerspezifischen \_ \\ Sicherheits-ID (SID) des aktuellen Benutzers intern zugeordnet wird. Eine Anwendung, die in einen anderen Registrierungs Speicherort als HKEY Current User schreiben muss, \_ \_ benötigt Administratorrechte.

Wenn die 32-Bit-Anwendung im Manifest keine angeforderte Ausführungs Ebene enthält, werden alle Schreibvorgänge in HKEY ( \_ lokale \_ Computer Software) \\ virtualisiert, während Schreibvorgänge an anderen Speicherorten außerhalb des aktuellen HKEY- \_ \_ Benutzers fehlschlagen.

Das Speichern persistenter Daten in der Registrierung, wie z. b. die Konfiguration eines Benutzers, wird nicht empfohlen. Die bevorzugte Methode zum Speichern persistenter Daten aus dem Spiel besteht darin, die Daten in das Dateisystem zu schreiben, indem Sie [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) aufrufen und den Wert einer CSIDL-Konstante abrufen, die im vorherigen Abschnitt beschrieben wurde.

## <a name="privilege-elevation"></a>Rechteerweiterungen

In Windows Vista muss jede Anwendung, für die Administratorrechte erforderlich sind, eine Anforderung für eine administrative Ausführungs Ebene im Manifest deklarieren (im nächsten Abschnitt [Festlegen der Ausführungs Ebene im Anwendungs Manifest](#setting-the-execution-level-in-the-application-manifest)).

Erhöhte Rechte sind das Verfahren, das von der Benutzerkontensteuerung zum herauf Stufen eines Prozesses zu einem administrativen Prozess gesteuert wird. Die Berechtigungen eines Prozesses können nur zur Erstellungszeit erhöht werden. Nach der Erstellung wird ein Prozess nie auf eine höhere Berechtigungsstufe herauf gestuft. Aus diesem Grund. Vorgänge, für die administrative Anmelde Informationen erforderlich sind, sollten in separaten Installationsprogrammen und anderen Hilfsprogrammen isoliert werden.

Bei der Ausführung eines Programms prüft UAC die angeforderte Ausführungs Ebene im Manifest. wenn erhöhte Rechte erforderlich sind, wird der aktuelle Benutzer von einem von zwei Standard Dialogfeldern aufgefordert: eine für einen Standardbenutzer und eine für einen Administrator.

Wenn der aktuelle Benutzer ein Standardbenutzer ist, fordert UAC den Benutzer zur Eingabe der Anmelde Informationen eines Administrators auf, bevor die Ausführung des Programms zugelassen wird.

**Abbildung 1. Eingabeaufforderung für einen Standard Benutzer zur Eingabe von Anmelde Informationen für ein Administrator Konto**

![Eingabeaufforderung für einen Standardbenutzer zur Eingabe von Anmelde Informationen für ein Administrator Konto](images/uac-prompt-elevation.jpg)

Wenn der aktuelle Benutzer ein Administrator ist, fordert UAC den Benutzer zur Eingabe der Berechtigung auf, bevor das Programm ausgeführt werden kann.

**Abbildung 2. Auffordern des Administrators, Änderungen am Computer zu autorisieren**

![auffordern des Administrators, Änderungen am Computer zu autorisieren](images/uac-prompt-authorization.jpg)

Der Anwendung werden nur Administratorrechte erteilt, wenn ein Standardbenutzer die richtigen Administratorrechte bereitstellt oder ein Administrator die Bestätigung erteilt. alles andere bewirkt, dass die Anwendung beendet wird.

Es ist wichtig zu beachten, dass ein Prozess mit erhöhten Rechten als Administrator ausgeführt wird, der Anmelde Informationen in die UAC-Eingabeaufforderung eingegeben hat, anstatt als Standardbenutzer, der aktuell angemeldet ist. Dies ähnelt **runas** in Windows XP beim erweiterten Prozess werden die Ordner-und Registrierungsschlüssel des Administrators beim Zugriff auf benutzerspezifische Daten abgerufen, und alle Programme, die vom erweiterten Prozess gestartet werden, erben sowohl die Administratorrechte als auch die Benutzerkonten. Für Administratoren, die zur Bestätigung aufgefordert werden (**fortfahren** oder **Abbrechen**), entsprechen diese Standorte den Speicherorten des aktuellen Benutzers. Im Allgemeinen sollten Prozesse, die erhöhte Rechte erfordern, jedoch nicht auf benutzerspezifische Daten angewendet werden. Beachten Sie, dass sich dies erheblich auf die Funktionsweise Ihres Installers auswirken kann! Wenn das Installationsprogramm, das als Administrator ausgeführt wird, in HKCU oder das Profil eines Benutzers schreibt, ist es möglicherweise sehr gut, an den falschen Speicherort zu schreiben. Sie sollten diese pro-Benutzer-Werte bei der ersten Durchführung des Spiels erstellen.

## <a name="uac-implications-with-createprocess"></a>UAC-Implikationen mit "kreateprocess ()"

Der UAC-Erweiterungsmechanismus wird nicht durch einen Aufruf der Win32-Funktion " [**deateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)()" aufgerufen, um eine ausführbare Datei zu starten, die so konfiguriert ist, dass Sie eine höhere Ausführungs Ebene als der aktuelle Prozess erfordert. Dies führt dazu, dass der Aufrufen von " **anateprocess**()" fehlschlägt, wenn " [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)()" die erforderliche Erhöhung des Fehlers zurückgibt \_ \_ . " **Deateprocess**()" ist nur erfolgreich, wenn die Ausführungs Ebene des aufgerufenen gleich oder kleiner ist als die des Aufrufers. Ein Prozess ohne erhöhte Rechte, der erweiterte Prozesse erzeugen muss, sollte dies mithilfe der [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)()-Funktion bewirken, was bewirkt, dass der UAC-Erweiterungsmechanismus mithilfe der Shell ausgelöst wird.

## <a name="setting-the-execution-level-in-the-application-manifest"></a>Festlegen der Ausführungs Ebene im Anwendungs Manifest

Sie deklarieren die angeforderte Ausführungs Ebene des Spiels, indem Sie dem Anwendungs Manifest eine Erweiterung hinzufügen. Der folgende XML-Code zeigt die minimale Konfiguration, die erforderlich ist, um die Ausführungs Ebene für eine Anwendung festzulegen:

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

Im vorangehenden Code wird das Betriebssystem darüber informiert, dass das Spiel nur Standardbenutzer Berechtigungen mit dem folgenden Tag erfordert:

``` syntax
<ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
```

Durch explizites Festlegen von requestedExecutionLevel auf "asInvoker" wird in diesem Beispiel dem Betriebssystem bestätigt, dass sich das Spiel ohne Administratorrechte ordnungsgemäß verhält. Folglich deaktiviert UAC die Virtualisierung und führt das Spiel mit denselben Berechtigungen wie der aufrufende Instanz aus, bei dem es sich in der Regel um Standardbenutzer Berechtigungen handelt, da Windows Explorer als Standardbenutzer ausgeführt wird.

Das Betriebssystem kann darüber informiert werden, dass ein Spiel eine Erhöhung der Administratorrechte erfordert, indem "asInvoker" durch "requiumministrator" ersetzt wird, um das folgende Tag zu erstellen:

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Bei dieser Konfiguration fordert das Betriebssystem den aktuellen Benutzer bei jedem Ausführen des Spiels zu einer der standardmäßigen UAC-Erweiterungs Dialogfelder auf. Es wird dringend empfohlen, dass kein Spiel Administratorrechte für die Durchführung erfordert, da dieses Dialogfeld nicht nur schnell lästig wird, sondern auch das Spiel mit den Eltern Steuerelementen nicht kompatibel ist. Stellen Sie sich vor dem Hinzufügen dieser Anforderung zu einer ausführbaren Datei vor.

Ein gängiges Missverständnis besteht darin, dass durch Hinzufügen eines Manifests, das requestedExecutionLevel auf "requisionministrator" festlegt, der Bedarf an einer Eingabeaufforderung mit erhöhten Rechten umgangen wird. Das ist falsch. Sie hindert das Betriebssystem einfach daran zu erraten, ob Ihre Setup-oder Update Anwendung Administratorrechte benötigt. Der Benutzer wird weiterhin aufgefordert, Rechte Erweiterungen zu autorisieren.

Die Signatur einer Anwendung, die für die Rechte Erweiterung markiert ist, wird von Windows überprüft, bevor die UAC-Eingabeaufforderung angezeigt wird. Eine große ausführbare Datei, die für die Rechte Erweiterung markiert ist, dauert länger als eine kleine ausführbare Datei und länger als eine ausführbare Datei, die als "asInvoker" gekennzeichnet ist. Ausführbare Setup Dateien, die selbst extrahiert werden, sollten daher als "asInvoker" gekennzeichnet werden, und jeder Teil, der als "requiumministrator" markiert werden muss, sollte in einer separaten Hilfsdatei für das Hilfsprogramm abgelegt werden.

Das UIAccess-Attribut, das in den vorangehenden Beispielen gezeigt wird, sollte für Spiele immer false sein. Dieses Attribut gibt an, ob Benutzeroberflächenautomatisierungs-Clients Zugriff auf die Benutzeroberfläche des geschützten Systems haben. Dies hat besondere Auswirkungen auf die Sicherheit, wenn auf true festgelegt

## <a name="embedding-a-manifest-in-visual-studio"></a>Einbetten eines Manifests in Visual Studio

Die Manifest-Unterstützung wurde zunächst zu Visual Studio hinzugefügt, beginnend bei VS2005. Standardmäßig wird für eine ausführbare Datei, die in Visual Studio 2005 (oder höher) erstellt wurde, im Rahmen des Buildprozesses ein automatisch generiertes Manifest eingebettet. Der Inhalt des automatisch generierten Manifests ist von bestimmten Projekt Konfigurationen abhängig, die Sie im Dialogfeld Projekteigenschaften angeben.

Das Manifest, das von Visual Studio 2005 automatisch generiert wird, enthält keinen <trustInfo> Block, da es keine Möglichkeit gibt, die UAC-Ausführungs Ebene in den Projekteigenschaften zu konfigurieren. Die bevorzugte Methode zum Hinzufügen dieser Informationen besteht darin, VS2005 ein benutzerdefiniertes Manifest mit dem <trustInfo> Block mit dem automatisch generierten Manifest zusammenzuführen. Dies ist so einfach wie das Hinzufügen einer \* Manifest-Datei zu ihrer Projekt Mappe, die die im vorherigen Abschnitt aufgeführten XML-Daten enthält. Wenn Visual Studio auf eine Manifest-Datei in der Projekt Mappe trifft, wird automatisch das Manifest-Tool (mt.exe) aufgerufen, um die Manifest-Dateien mit der automatisch generierten Datei zusammenzuführen.

> [!Note]  
> Im Manifest-Tool (mt.exe), das von Visual Studio 2005 bereitgestellt wird, ist ein Fehler aufgetreten, der zu einem zusammengeführten und eingebetteten Manifest führt, das Probleme verursachen kann, wenn die ausführbare Datei unter Windows XP vor SP3 ausgeführt wird. Der Fehler ist darauf zurückzuführen, wie das Tool den Standard Namespace bei der Deklaration des <trustInfo> Blocks neu definiert. Glücklicherweise ist es einfach, das Problem vollständig zu umgehen, indem Sie explizit einen anderen Namespace im <trustInfo> Block deklarieren und die untergeordneten Knoten auf den neuen Namespace umleiten. Der im vorherigen Abschnitt bereitgestellte XML-Code veranschaulicht diese Korrektur.

 

Ein Nachteil bei der Verwendung des mt.exe Tools, das in Visual Studio 2005 enthalten ist, besteht darin, dass bei der Verarbeitung des Blocks eine Warnung generiert wird, <trustInfo> da das Tool kein aktualisiertes Schema zum Validieren des XML-Codes enthält. Um diese Warnung zu beheben, empfiehlt es sich, alle mt.exe Dateien im Installationsverzeichnis von Visual Studio 2005 (es sind mehrere Instanzen vorhanden) mit den mt.exe zu ersetzen, die im letzten Windows SDK bereitgestellt werden.

Ab Visual Studio 2008 können Sie nun die Ausführungs Ebene einer Anwendung aus dem Dialogfeld "Projekteigenschaften" (Abbildung 3) oder mit dem/MANIFESTUAC Linker-Flag angeben. Das Festlegen dieser Optionen bewirkt, dass Visual Studio 2008 ein Manifest mit dem entsprechenden Block automatisch generiert und <trustInfo> in die ausführbare Datei einbettet.

**Abbildung 3. Festlegen der Ausführungs Ebene in Visual Studio 2008**

![Festlegen der Ausführungs Ebene in Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

Das Einbetten eines Manifests in älteren Versionen von Visual Studio ohne Unterstützung von Manifests ist weiterhin möglich, erfordert aber mehr Arbeit vom Entwickler. Ein Beispiel hierfür finden Sie im Visual Studio 2003-Projekt, das in einem beliebigen Beispiel im DirectX SDK vor der Release vom März 2008 enthalten ist.

## <a name="uac-compatibility-with-older-games"></a>UAC-Kompatibilität mit älteren spielen

Wenn das Spiel scheint, eine Datei erfolgreich in das Verzeichnis "Programme" zu speichern und zu laden, aber kein Beweis für die Datei "Windows Vista" ist, wird jede 32-Bit-Anwendung, die keine angeforderte Ausführungs Ebene im Manifest enthält, als ältere Anwendung betrachtet. Vor Windows Vista wurden die meisten Anwendungen normalerweise von Benutzern mit Administratorrechten ausgeführt. Daher konnten diese Anwendungen Systemdateien und Registrierungsschlüssel kostenlos lesen und schreiben, und viele Entwickler haben die Änderungen, die für die ordnungsgemäße Ausführung von eingeschränkten Benutzerkonten unter Windows XP erforderlich waren, nicht vorgenommen. Bei Windows Vista würden diese Anwendungen jedoch aufgrund unzureichender Zugriffsrechte unter dem neuen Sicherheitsmodell, das die Standardbenutzer Ausführung für ältere Anwendungen erzwingt, fehlschlagen. Um die Auswirkungen dieses Beispiels zu mindern, wurde die Virtualisierung auch Windows Vista hinzugefügt. Durch die Virtualisierung werden Tausende von Legacy Anwendungen in Windows Vista gut funktionieren, ohne dass diese Anwendungen jederzeit über erweiterte Berechtigungen verfügen müssen. s gefunden. die Wahrscheinlichkeit ist, dass Ihr Spiel im Legacy Modus ausgeführt wird und Virtualisierung unterliegt.

Die Virtualisierung wirkt sich auf das Dateisystem und die Registrierung aus, indem systemabhängige Schreibvorgänge (und nachfolgende Datei-oder Registrierungs Vorgänge) an einen benutzerspezifischen Speicherort innerhalb des Profils des aktuellen Benutzers umgeleitet werden. Wenn z. b. eine Anwendung versucht, in die folgende Datei zu schreiben:

<dl> C: \\ \\ Unternehmens-namens Titel des Unternehmens \\ \\config.ini  
</dl>

der Schreibvorgang wird automatisch an Folgendes umgeleitet:

<dl> C: \\ Benutzer \\ Benutzername \\ AppData \\ local \\ virtualstore- \\ Programmdateien \\ Firmenname \\ Titel \\config.ini  
</dl>

Ebenso, wenn eine Anwendung versucht, einen Registrierungs Wert wie den folgenden zu schreiben:

<dl> Name des \_ Unternehmens für lokale HKEY- \_ Computer \\ Software \\ \\  
</dl>

Sie wird stattdessen umgeleitet an:

<dl> HKEY \_ Current \_ User \\ Software \\ Classes \\ virtualstore \\ Computer \\ Software \\ Unternehmens Name \\ Titel  
</dl>

Der Zugriff auf Dateien und Registrierungsschlüssel, die von der Virtualisierung betroffen sind, erfolgt nur durch Datei-und Registrierungs Vorgänge von virtualisierten Anwendungen, die als aktueller Benutzer ausgeführt werden.

Es gibt jedoch viele Einschränkungen bei der Virtualisierung. Eine davon besteht darin, dass 64-Bit-Anwendungen niemals im Legacy Modus für Kompatibilitäts Vorgänge ausgeführt werden, die in 32-Bit-64 Anwendungen für die Virtualisierung unterliegen. Wenn eine ältere Anwendung, die als Standardbenutzer ausgeführt wird, versucht, eine beliebige ausführbare Datei an einen Speicherort zu schreiben, für den Administrator Anmelde Informationen erforderlich sind, wird die Virtualisierung nicht ausgeführt, und der Schreibvorgang schlägt fehl.

**Abbildung 4. Virtualisierungsprozess**

![Virtualisierungsprozess](images/uac-virtualization-process.jpg)

Wenn eine Legacy Anwendung einen Lesevorgang für System sensible Speicherorte im Dateisystem oder in der Registrierung versucht, werden zuerst die virtuellen Speicherorte durchsucht. Wenn die Datei oder der Registrierungsschlüssel nicht gefunden wird, greift das Betriebssystem auf die standardmäßigen Systemspeicher Orte zu.

Die Virtualisierung wird aus den nachfolgenden Versionen von Windows entfernt, sodass es wichtig ist, dieses Feature nicht zu verlassen. Stattdessen sollten Sie das Anwendungs manifest explizit entweder für Standardbenutzer-oder Administratorrechte konfigurieren, da hierdurch die Virtualisierung deaktiviert wird. Die Virtualisierung ist für Endbenutzer auch nicht offensichtlich. Obwohl die Virtualisierung die Anwendung möglicherweise zulässt, kann Sie Support Anrufe generieren und es schwierig machen, Probleme für diese Kunden zu lösen.

Beachten Sie Folgendes: Wenn die UAC deaktiviert ist, wird die Virtualisierung ebenfalls deaktiviert. Wenn die Virtualisierung deaktiviert ist, Verhalten sich Standardbenutzer Konten genau wie eingeschränkte Benutzerkonten in Windows XP, und ältere Anwendungen funktionieren möglicherweise nicht ordnungsgemäß für Standardbenutzer, die andernfalls aufgrund der Virtualisierung erfolgreich gewesen wären.

## <a name="legacy-scenarios-and-manifests"></a>Legacy Szenarios und Manifeste

Bei den meisten Verwendungs Szenarien ist es einfach, die exe-Datei mit den korrekten UAC-Manifest-Elementen zu markieren und sicherzustellen, dass die Anwendung ordnungsgemäß funktioniert, da ein Standard Benutzer für eine ausgezeichnete UAC-Kompatibilität ausreicht. Die meisten Spieler führen Windows Vista oder Windows 7 mit aktivierter Benutzerkontensteuerung aus. Für Windows XP und Benutzer unter Windows Vista oder Windows7 mit deaktivierter Funktion "Benutzerkontensteuerung" werden Sie normalerweise mithilfe von Administrator Konten ausgeführt. Obwohl es sich hierbei um einen weniger sicheren Betriebsmodus handelt, treten in der Regel keine zusätzlichen Kompatibilitätsprobleme auf, obwohl die Deaktivierung der Benutzerkontensteuerung auch die Virtualisierung deaktiviert.

Es ist ein Sonderfall zu beachten, wenn das Programm im UAC-Manifest als "requisionministrator" gekennzeichnet ist. Unter Windows XP und Windows Vista oder Windows 7 mit deaktivierter Benutzerkontensteuerung werden die UAC-Manifest-Elemente vom System ignoriert. In dieser Situation werden Benutzer mit Administrator Konten immer alle Programme mit vollständigen Administratorrechten ausführen, sodass diese Programme erwartungsgemäß funktionieren. Eingeschränkte Windows XP-Benutzer und Standard Benutzer, die unter Windows Vista oder Windows 7 ausgeführt werden, führen diese Programme jedoch immer mit eingeschränkten Rechten aus, und alle Vorgänge auf Administratorebene können nicht ausgeführt werden. Daher wird empfohlen, dass Programme, die als "Requirements-Administrator" gekennzeichnet sind, [**isuseranadmin**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) beim Start aufrufen und eine schwerwiegende Fehlermeldung anzeigen, wenn Sie false zurückgibt. Für das obige Mehrheits Szenario ist dies immer erfolgreich, bietet aber eine bessere Benutzer Darstellung und eine eindeutige Fehlermeldung in dieser seltenen Situation.

## <a name="conclusion"></a>Zusammenfassung

Als Spielentwickler für die mehr Benutzerumgebung von Windows ist es zwingend erforderlich, dass Sie Ihr Spiel so entwerfen, dass es effektiv und verantwortungsvoll funktioniert. Die ausführbare Hauptdatei des Spiels sollte nicht von Administratorrechten abhängig sein. Dies verhindert nicht nur, dass bei jeder Ausführung des Spiels Eingabe Aufforderungen angefordert werden, was sich negativ auf die Gesamt Benutzer Leistung auswirken kann, sondern auch die Nutzung anderer Features, die eine Ausführung mit Standardbenutzer Berechtigungen erfordern, wie z. b. Jugendschutz.

Anwendungen, die unter früheren Versionen von Windows ordnungsgemäß für den Betrieb mit den Anmelde Informationen eines Standard Benutzers (oder eines eingeschränkten Benutzers) entworfen wurden, werden von der Benutzerkontensteuerung nicht beeinträchtigt, weil Sie ohne erhöhte Rechte ausgeführt werden. Sie sollten jedoch ein Manifest mit der angeforderten Ausführungs Ebene enthalten, das auf "asInvoker" festgelegt ist, um Anwendungsstandards für Vista zu entsprechen.

## <a name="further-reading"></a>Weitere Informationen

Wenn Sie Unterstützung beim Entwerfen von Anwendungen für Windows Vista haben, die mit der Benutzerkontensteuerung kompatibel sind, laden Sie das folgende Whitepaper herunter: [Windows Vista Anwendungs Entwicklungsanforderungen für die Kompatibilität mit der Benutzerkontensteuerung](/previous-versions/dotnet/articles/bb530410(v=msdn.10)).

Dieses Whitepaper enthält ausführliche Schritte zum Entwurfsprozess sowie Codebeispiele, Anforderungen und bewährte Methoden. Außerdem werden in diesem Artikel die technischen Updates und Änderungen an der Benutzer Darstellung in Windows Vista ausführlich erläutert.

Weitere Informationen zur Benutzerkontensteuerung finden Sie unter [Windows Vista: Benutzerkontensteuerung](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) auf [Microsoft TechNet](https://www.microsoft.com/technet/).

Eine weitere nützliche Ressource ist der Artikel [zum Erlernen Ihrer Apps, um mit der Windows Vista-Benutzerkontensteuerung zu](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control)experimentieren, vom [MSDN Magazine](/archive/msdn-magazine/msdn-magazine-issues), Januar 2007. In diesem Artikel werden allgemeine Probleme mit der Anwendungs Kompatibilität sowie die Vorteile und Probleme bei der Verwendung von Windows Installer-Paketen unter Windows Vista erläutert.

Weitere Informationen zum Fehler und zum Beheben von mt.exe finden Sie im Tool, das von Visual Studio 2005 zum automatischen Zusammenführen und Einbetten eines Manifests in eine ausführbare Datei verwendet wird. Weitere Informationen finden Sie unter unter [Suchen von Manifesten Teil 2: Standardnamespaces und UAC-Manifeste in Windows Vista](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) auf der [MSDN](/archive/blogs/)-Website.

 

