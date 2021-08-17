---
title: Bewährte Methoden für die Installation von Massively Multiplayer Online Games
description: In diesem Artikel wird das Erstellen einer Vertrauenskette für die MMOG-Clientinstallation (Massively Multiplayer Online Games) und benutzerdefinierte Spielupdatesysteme beschrieben, die gut mit Windows und dem Sicherheitsmodell von Windows Vista und Windows 7 funktionieren.
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b574bdf2ae98b28fabed97340d6aa38b1a864c24519bb6532d0aa4069882efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815435"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a>Bewährte Methoden für die Installation von Massively Multiplayer Online Games

In diesem Artikel wird das Erstellen einer Vertrauenskette für die MMOG-Clientinstallation (Massively Multiplayer Online Games) und benutzerdefinierte Spielupdatesysteme beschrieben, die gut mit Windows und dem Sicherheitsmodell von Windows Vista und Windows 7 funktionieren. Der Ansatz ist darauf ausgelegt, das Patchen von MMOG-Titeln zu ermöglichen und gleichzeitig Standardbenutzerkonten zu unterstützen, die eingeschränkten Zugriff auf die Festplatte und die Systemregistrierung haben.

-   [Warum MMOG-Clients unterschiedliche Anforderungen haben als herkömmliche, im Einzelhandel erworbene Spiele](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [Übersicht über einen Vertrauenskette-Ansatz](#overview-of-a-chain-of-trust-approach)
-   [Alles wird auf dem Server überprüft. Warum sollte ich mich Gedanken machen, wenn mein Client gehackt wird?](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [Erstellen der Trust-Worthy Loader-Anwendung](#construction-of-the-trust-worthy-loader-application)
    -   [Hintergrundleseinformationen](#background-reading)
    -   [Installation des vertrauenswürdigen Lade- und Patchers](#installation-of-the-trusted-loader-and-patcher)
    -   [Installation der ausführbaren Spieldateien, DLLs und Daten](#installation-of-the-game-executables-dlls-and-data)
    -   [Access Control Listenänderungscode](#access-control-list-modification-code)
    -   [Installationen für fortgeschrittene Benutzer](#installations-for-advanced-users)
    -   [Überprüfung der Vertrauenswürdigkeit des Ladeers](#the-loaders-verification-of-trust)
    -   [Datenüberprüfung](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a>Warum MMOG-Clients unterschiedliche Anforderungen haben als herkömmliche, im Einzelhandel erworbene Spiele

Die ständig verbundene und sich ständig weiterentwickelnde Natur von MMOGs macht es zu einer grundlegenden Anforderung, regelmäßige Updates von Clientcode und Inhalten zur Behebung von Sicherheitsrisiken und zur Erweiterung der Spielerfahrung zu bieten. Mit dem Potenzial für fast tägliche Updates erfordert das MMOG-Szenario eine sorgfältige Verwaltung, um eine benutzerfreundliche Benutzeroberfläche sicherzustellen. Dies unterscheidet sich vom herkömmlichen Einzelhandelskaufmodell, bei dem eine kleine Anzahl von Patches in der Nähe des Versanddatums des Produkts bereitgestellt werden kann. Die Windows Installer limited user patching technology provided with the operating system is designed to handle small numbers of application patches, and not the large quantity and high frequency needed by MMOGs. Daher ist es häufig erforderlich, dass benutzerdefinierte Patchsysteme entwickelt werden, um die Anforderungen von MMOGs zu erfüllen, einschließlich aller speziellen Anforderungen, die speziell für die zu entwickelnde MMOG gelten.

Da so viele Computer mit dem Internet verbunden sind, verfügen Windows Vista und Windows 7 über strengere Sicherheitseinschränkungen und Sicherheitsmaßnahmen für Benutzer, die den Zugriff von Anwendungen auf verschiedene Bereiche der Festplatte einschränken. Im Gegensatz Windows XP sind diese Einschränkungen für den Standardmodus für Benutzerkonten aktiviert. Diese Einschränkungen müssen beim Entwerfen des Layouts eines Spiels, einer ausführbaren Datei und von Daten und des zugehörigen Patchsystems berücksichtigt werden. Weitere Informationen zu den Sicherheitsmaßnahmen, die vom Betriebssystem bereitgestellt werden, finden Sie unter [Benutzerkontensteuerung für Spieleentwickler.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

## <a name="overview-of-a-chain-of-trust-approach"></a>Übersicht über einen Vertrauenskette-Ansatz

Der in diesem Whitepaper vorgestellte benutzerdefinierte Updateansatz basiert auf einer vertrauenswürdigen Ladeprogrammanwendung, die im geschützten Ordner "Programme" installiert ist, während die ausführbaren Dateien und Daten der Spiele in einem freigegebenen, für den Benutzer zugänglichen Bereich gespeichert werden. Eine Vertrauenskette beginnt mit dem Lader, der gültigkeitsprüfungen für die Binärdateien und Daten des Spiels vor dem Start ausführt.

![Vertrauenskette beginnt mit einem vertrauenswürdigen Lader](images/mmo-installation-best-practices-01.gif)

Das vertrauenswürdige Ladeprogramm muss über genügend Logik verfügen, um vor dem Starten des Spiels überprüfen zu können, ob die ausführbare Datei des Spiels und andere Binärdateien nicht manipuliert wurden. Das Lader kann spieldaten auch so oft wie nötig überprüfen, aber die Größe der Spieldaten ist in der Regel zu groß, um sie jedes Mal in einem einzelnen Durchgang überprüfen zu können. Ein alternativer Ansatz ist die Verwendung eines Stichprobenmusters, das sicherstellt, dass die Überprüfung des gesamten DataSets über einen längeren Zeitraum erfolgt. Die Laderanwendung kann eine Game Patching-Engine enthalten, die eine vertrauenswürdige Methode von bietet, um Updates in das installierte Spiel zu integrieren.

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a>Alles wird auf dem Server überprüft. Warum sollte ich mich Gedanken machen, wenn mein Client gehackt wird?

Es ist unmöglich zu vertrauen, dass der Client nicht kompromittiert wurde. Daher ist es üblich, dass MMOG-Server alle vom Client empfangenen Daten überprüfen. Während diese Verarbeitung kompromittierte oder spickende Spielclients innerhalb des Spiel-Universes identifizieren kann, kann der Server nicht einfach alle Probleme identifizieren, für die der Spielclient verfügbar gemacht werden kann. Es ist wichtig, den Schutz vor Hackern zu stärken, die Ihren Client als Plattform für Angriffe auf Ihren Dienst, andere Benutzer oder sogar einfach als Vektor für Angriffe auf die Clientcomputer selbst verwenden möchten. Die Anwendung von Techniken zur Codesignierung und Datenüberprüfung kann dazu beitragen, kompromittierte Clients zu erkennen, bevor sie ausgeführt werden. Da der Patchmechanismus das Verfügbar machen von ausführbaren und DLL-Binärdateien erfordert, die nicht durch die schreibgeschützten Standardberechtigungen für Programmdateien geschützt sind, ist es wichtig, diese Dateien vor dem Start zu überprüfen, um die allgemeine Systemsicherheit zu gewährleisten.

Dieses Modell versucht nicht, sich mit dem Szenario eines böswilligen Administratorbenutzers zu befassen, bei dem das Ladeprogramm selbst kompromittiert werden könnte, sondern konzentriert sich auf den Schutz von Standardbenutzern vor versehentlichem Ausführen von manipuliertem Code. Herkömmliche Server-Client-Validierungstechniken sind tatsächlich die einzige mögliche Lösung für böswillige Clientsystemadministratoren.

## <a name="construction-of-the-trust-worthy-loader-application"></a>Erstellen der Trust-Worthy Loader-Anwendung

### <a name="background-reading"></a>Hintergrundleseinformationen

Leser sollten sich mit der folgenden Dokumentation vertraut machen, die Details zur Grundlegenden Technologie zur Sicherstellung der bewährten Methode für softwarebasiertes Vertrauen enthält.

<dl> <dt>

<span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>Signieren von Code
</dt> <dd>

[Authenticode Signing for Game Developers](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>Signtool
</dt> <dd>

[SignTool](/windows/desktop/SecCrypto/signtool) auf MSDN

</dd> </dl>

Im folgenden Abschnitt werden die APIs beschrieben, die zum Erstellen der Ladeanwendung verwendet werden sollen, die das Datenträgerlayout für die Installation und Überprüfung der Vertrauensüberprüfung unterstützen.

### <a name="installation-of-the-trusted-loader-and-patcher"></a>Installation des vertrauenswürdigen Lade- und Patchers

Das vertrauenswürdige Ladeprogramm und die Basisversion des Patcher-Hilfsprogramms sollten wie bei herkömmlichen Installationen im geschützten Ordner "Programme" auf dem HDD installiert werden. Das Installieren und Patchen der Laderanwendung erfordert Administratorrechte. Daher ist es wichtig, die Updatehäufigkeit für das Lader zu minimieren, um sicherzustellen, dass Endbenutzer nicht häufig erhöhte Rechte benötigen, obwohl Windows Installer limited user patching verwendet werden kann, um Erhöhungen für Laderpatches zu vermeiden.

Weitere Informationen finden Sie im Artikel Patching Game Software in Windows XP, Windows Vista und Windows 7.

### <a name="installation-of-the-game-executables-dlls-and-data"></a>Installation der ausführbaren Spieldateien, DLLs und Daten

Um Standardbenutzerupdates des Spiels ohne Administratorrechte zu ermöglichen, müssen die ausführbaren Dateien, DLLs und Daten des Spiels in einem Bereich der Festplatte installiert werden, auf den alle Benutzer zugriff können. Das Betriebssystem stellt einen Bereich "Alle Benutzeranwendungsdaten" zur Verfügung, der als Standardspeicherort für die Installation verwendet werden kann. [**SHGetFolderPath sollte**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit dem CSIDL COMMON APPDATA-Schlüssel verwendet werden, \_ um den \_ Dateipfad für diesen Bereich zu bestimmen. Es ist wichtig, dass keine Annahmen über den Pfad getroffen werden, zu dem dieser Schlüssel zurückkehrt, da er vom Benutzer konfigurierbar sein kann.

Die Installation muss die Ordnerberechtigungen ändern oder verwalten, um den Zugriff auf alle Benutzer mit freigegebenen Schreibzugriffen zu erreichen, die zum Aktualisieren des Titels erforderlich sind. Mit den richtigen Berechtigungen kann die Spielupdatefunktion des Ladeprogramms das Spiel problemlos patchen, ohne dass besondere Berechtigungen von einem Benutzerkonto erforderlich sind, einschließlich der Zeiten, in denen es von Standardbenutzern gestartet wird.

### <a name="access-control-list-modification-code"></a>Access Control Listenänderungscode

Für Windows XP müssen Sie Code ausführen, um die Zugriffssteuerungsliste (Access Control List, ACL) manuell zu ändern. Dies ist eine Beispielfunktion, die dies veranschaulicht:

``` syntax
HRESULT ChangeACLtoAllowUserRW( WCHAR* strDir )
{
    EXPLICIT_ACCESS explicitaccess;
    PACL NewAcl = NULL;
    DWORD dwError;

    BuildExplicitAccessWithName( &explicitaccess, L"BUILTIN\\Users",
                                 GENERIC_ALL, GRANT_ACCESS,
                                 SUB_CONTAINERS_AND_OBJECTS_INHERIT );
                                 
    dwError = SetEntriesInAcl( 1, &explicitaccess, NULL, &NewAcl );
    if( dwError == ERROR_SUCCESS) 
    {
        dwError = SetNamedSecurityInfo( strDir, SE_FILE_OBJECT,
                                        DACL_SECURITY_INFORMATION,
                                        NULL, NULL, NewAcl, NULL );
        if( dwError == ERROR_SUCCESS)
        {
            if( NewAcl != NULL ) AccFree( NewAcl );
            return S_OK;
        }
    }

    if( NewAcl != NULL ) AccFree( NewAcl );
    return E_FAIL;
}
```

Dieses Codebeispiel funktioniert auch für Windows Vista und Windows 7; Sie stellen jedoch auch das Befehlszeilen-Hilfsprogramm icacls zum Bearbeiten von Datei-ACLS zur Verfügung, die Sie stattdessen verwenden können.

Das Tool bietet eine detaillierte Hilfe, wenn es ausgeführt wird. Ein Beispiel für die Verwendung des Tools ist:

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

Durch diese Verwendung wird dem Benutzer die DAC-Berechtigungen Rex Löschen und Schreiben für den Spielordner gewährt, der in den Bereichen Alle Benutzer der Festplatte gespeichert ist.

### <a name="installations-for-advanced-users"></a>Installationen für fortgeschrittene Benutzer

Bei erweiterten Benutzerinstallationsszenarien kann ein Benutzer den Installationspfad für Spiele manuell angeben. Die Verzeichnisauswahl sollte auf eine Datei außerhalb der Programmdateien beschränkt werden, um sicherzustellen, dass sich der Ordner in einem wirklich beretzbaren Bereich der Festplatte befindet. Der vom Benutzer ausgewählte Pfad sollte nur für die Exe-Dateien und Daten der Spiele verwendet werden, da das Game Loader und die Patcher-EXE-Dateien aus Sicherheitsgründen immer im sicheren Ordner Programme installiert werden sollten.

### <a name="the-loaders-verification-of-trust"></a>Überprüfung der Vertrauenswürdigkeit des Ladeers

Windows stellt die [**WinVerifyTrust-Funktion**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) zum Überprüfen der Gültigkeit von signiertem Code zur Verfügung und basiert auf den kryptografischen Diensten im Betriebssystem. Die Funktion ist vollständig auf MSDN dokumentiert: **WinVerifyTrust-Funktion.**

Das folgende Beispielprogramm auf MSDN zeigt die Verwendung der -Funktion, um zu bestimmen, ob eine ausführbare Programmdatei mit einem gültigen Zertifikat signiert [ist: Beispiel C-Programm: Überprüfen](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)der Signatur einer PE-Datei .

Um zu überprüfen, ob die ausführbare Datei des signierten Spiels vertrauenswürdig ist, um innerhalb des Ladeprogramm ausgeführt zu werden, reicht die Generische Überprüfungsaktion aus:

<dl> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

WINTRUST \_ ACTION \_ GENERIC \_ VERIFY \_ V2

</dd> <dt>

<span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>Bedeutung
</dt> <dd>

Überprüfen Sie eine Datei oder ein Objekt mithilfe des Authenticode-Richtlinienanbieters.

</dd> </dl>

Die Funktion verwendet ein Eingabestrukturargument, das Informationen enthält, die der Vertrauensanbieter benötigt, um die angegebene Aktion zu verarbeiten. In der Regel enthält die -Struktur wie im vorherigen Beispielfall Informationen, die das Objekt identifizieren, das der Vertrauensanbieter auswerten muss.

Das Format der -Struktur ist spezifisch für den Aktionsbezeichner. Im folgenden Thema auf MSDN wird die Beispielstruktur für den WinTrust-Anbieter beschrieben: [**WINTRUST \_ DATA**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) Structure.

Wenn der Vertrauensanbieter überprüft, ob der Subjekt für die angegebene Aktion vertrauenswürdig ist, ist der Rückgabewert 0 (null). Kein anderer Wert außer 0 (null) sollte als erfolgreiche Rückgabe betrachtet werden.

### <a name="data-validation"></a>Datenüberprüfung

Der Codesignierungsmechanismus unterstützt nur das Signieren bestimmter Dateitypen, einschließlich ausführbarer Dateien, DLLs, Windows Installer-Pakete (.msi-Dateien) und cabinet-Dateien (.cab). Die [**WinVerifyTrust-API**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) sollte nicht verwendet werden, um zu überprüfen, ob große Datendateien (z.B. .cab-Dateien) nicht manipuliert wurden, da es bei der Überprüfung sehr großer Dateien einige Probleme mit der Leistung und Stabilität gibt. Ausführbare Programmdateien sind in der Regel klein genug, damit eine vollständige Vertrauenswürdigkeitsprüfung mithilfe des WinTrust-Anbieters erfolgt, aber Datendateien für Spiele liegen häufig im Bereich von vielen Gigabytes. Der Vom Lader zur Überprüfung von Spieldaten verfolgte Ansatz sollte ein Ansatz sein, bei dem eine kleine Stichprobe des Datasets während der Laufzeit des Spiels getestet wird. Dieser Ansatz verteilt die Kosten für Überprüfungstests über die Lebensdauer der Spielerfahrung und kann eine nahtlose Benutzererfahrung ohne lange Wartezeiten bieten. Um dies zu erreichen, ist möglicherweise eine sorgfältige Organisation der Daten erforderlich. Einige MMOGs verwenden einen Datenbankansatz, um die Verwaltung, Verwaltung und Überprüfung der Richtigkeit von Spielressourcen im Laufe der Zeit zu unterstützen.

Aus Sicherheitsgründen sollte der Clientcode so entworfen werden, dass datendateien nicht vertraut werden, auch wenn eine art grundlegende Datenüberprüfung mit dem vertrauenswürdigen Lader verwendet wird. Headerüberprüfungen, Hashes und andere herkömmliche Integritätsprüfungen sollten verwendet werden. Die Arbeit zum Härten des E/A-Codes des Clients sollte auch mitHilfe von Techniken wie Fuzztests erfolgen und automatische statische Codeanalysetools wie den **Schalter /analyze** in Visual Studio 2005 und Visual Studio 2008 nutzen (verfügbar in Visual Studio Team System und dem kostenlosen Compiler, der mit dem Windows SDK bereitgestellt wird).

Weitere Informationen zur Softwaresicherheit finden Sie unter [Best Security Practices in Game Development](/windows/desktop/DxTechArts/best-security-practices-in-game-development).

 

 