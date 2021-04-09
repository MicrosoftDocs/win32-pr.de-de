---
title: Bewährte Methoden für die Installation von Massively Multiplayer Online Games
description: In diesem Artikel wird beschrieben, wie Sie eine Kette von Vertrauens Entwürfen für die MMOG-Client Installation (Massively Multiplayer Online Games) und benutzerdefinierte Spiel Update Systeme erstellen, die gut mit Windows und dem Sicherheitsmodell von Windows Vista und Windows 7 funktionieren.
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81003a434b830f046c29d606355104fe618d1f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039224"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a>Bewährte Methoden für die Installation von Massively Multiplayer Online Games

In diesem Artikel wird beschrieben, wie Sie eine Kette von Vertrauens Entwürfen für die MMOG-Client Installation (Massively Multiplayer Online Games) und benutzerdefinierte Spiel Update Systeme erstellen, die gut mit Windows und dem Sicherheitsmodell von Windows Vista und Windows 7 funktionieren. Der Ansatz ist darauf ausgelegt, das Patchen von MMOG-Titeln zu ermöglichen, während Standardbenutzer Konten unterstützt werden, die eingeschränkten Zugriff auf die Festplatte und die Systemregistrierung haben.

-   [Warum MMOG-Clients andere Anforderungen an herkömmliche Einzelhandels Spiele haben](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [Übersicht über eine Kette von Vertrauens Stellungen](#overview-of-a-chain-of-trust-approach)
-   [Alles wird auf dem Server überprüft. Warum sollte ich mich Gedanken machen, wenn mein Client gehackt wird?](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [Erstellung der Trust-Worthy Lade Anwendung](#construction-of-the-trust-worthy-loader-application)
    -   [Hintergrund Lesevorgänge](#background-reading)
    -   [Installation des vertrauenswürdigen Lade Moduls und Patcher](#installation-of-the-trusted-loader-and-patcher)
    -   [Installation der ausführbaren Spieldateien, DLLs und Daten](#installation-of-the-game-executables-dlls-and-data)
    -   [Code zur Access Control Listen Änderung](#access-control-list-modification-code)
    -   [Installationen für fortgeschrittene Benutzer](#installations-for-advanced-users)
    -   [Überprüfung der Vertrauensstellung durch das Lade Modul](#the-loaders-verification-of-trust)
    -   [Datenüberprüfung](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a>Warum MMOG-Clients andere Anforderungen an herkömmliche Einzelhandels Spiele haben

Dank der ständig verbundenen und sich weiterentwickelnden Natur von mmugs ist es eine grundlegende Anforderung, regelmäßige Updates von Client Code und Inhalt bereitzustellen, um Sicherheitsrisiken zu beheben und das Spielverhalten zu erweitern. Dank des möglichen fast Daily Updates ist für das MMOG-Szenario eine sorgfältige Verwaltung erforderlich, um eine benutzerfreundliche Benutzerfreundlichkeit zu gewährleisten. Dies unterscheidet sich vom herkömmlichen Einzelhandels kaufmodell, bei dem eine kleine Anzahl von Patches in der Nähe des Einzelhandels Datums des Produkts bereitgestellt werden kann. Die Windows Installer eingeschränkte benutzerpatching-Technologie, die mit dem Betriebssystem bereitgestellt wird, ist so konzipiert, dass Sie eine kleine Anzahl von Anwendungspatches und nicht die große Menge und hohe Häufigkeit von mmugs verarbeitet. Daher ist es häufig erforderlich, dass benutzerdefinierte patchsysteme entwickelt werden, um die Anforderungen von mmmugs zu erfüllen, einschließlich aller speziellen Anforderungen, die speziell für die jeweilige entwickelte MMOG gelten.

Da so viele Computer mit dem Internet verbunden sind, weisen Windows Vista und Windows 7 strengere Sicherheitseinschränkungen und Sicherheitsvorkehrungen für Benutzer auf, die den Zugriff von Anwendungen auf verschiedene Bereiche der Festplatte beschränken. Anders als bei Windows XP sind diese Einschränkungen für den Standardmodus für Benutzerkonten aktiviert. Diese Einschränkungen müssen berücksichtigt werden, wenn das Layout eines Spiels, der ausführbaren Datei und der Daten und des zugehörigen patchsystems entworfen wird. Weitere Informationen zu den vom Betriebssystem bereitgestellten Sicherheitsmaßnahmen finden Sie unter [Benutzerkontensteuerung für Spieleentwickler](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

## <a name="overview-of-a-chain-of-trust-approach"></a>Übersicht über eine Kette von Vertrauens Stellungen

Der in diesem Whitepaper vorgestellte benutzerdefinierte Aktualisierungs Verfahren basiert darauf, dass eine vertrauenswürdige Lade Programm Anwendung im Ordner "geschützte Programme" installiert ist. dabei werden die ausführbaren Dateien und Daten der ausführbaren Dateien in einem freigegebenen Bereich, auf den alle Benutzer zugreifen Eine Vertrauenskette beginnt mit dem Lade Tool, das vor dem Start Gültigkeits Prüfungen der Spiel Binärdateien und-Daten ausführt.

![Vertrauenskette beginnt mit einem vertrauenswürdigen Lade Tool](images/mmo-installation-best-practices-01.gif)

Das vertrauenswürdige Lade Programm muss über ausreichend Logik verfügen, um sicherzustellen, dass die ausführbare Datei des Spiels und andere Binärdateien vor dem Start des Spiels nicht manipuliert wurden. Das Lade Tool kann auch die Spieldaten so oft wie nötig überprüfen. die Größe der Spieldaten ist jedoch in der Regel zu groß, um zuzulassen, dass Sie jedes Mal in einem einzigen Durchlauf überprüft werden. Ein alternativer Ansatz ist die Verwendung eines Stichproben Musters, mit dem sichergestellt wird, dass das gesamte Dataset über einen längeren Zeitraum überprüft wird. Die Lade Anwendung enthält möglicherweise ein Spiel-Patchen-Engine, das eine vertrauenswürdige Methode von bereitstellt, um Updates in das installierte Spiel zu integrieren.

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a>Alles wird auf dem Server überprüft. Warum sollte ich mich Gedanken machen, wenn mein Client gehackt wird?

Es ist unmöglich zu vertrauen, dass der Client nicht kompromittiert wurde. Daher ist es üblich, dass MMOG-Server alle vom Client empfangenen Daten überprüfen. Diese Verarbeitung kann zwar kompromittierte oder betrügerische Spiel Clients innerhalb des Game universe erkennen, aber der Server kann nicht leicht alle Probleme identifizieren, denen der Spielclient ausgesetzt sein kann. Es ist wichtig, den Schutz vor Hackern zu verstärken, die Ihren Client als Plattform für Angriffe auf Ihren Dienst, andere Benutzer oder sogar einfach als Vektor für den Angriff auf die Client Computer verwenden möchten. Die Anwendung von Verfahren zum Signieren von Code und zur Datenüberprüfung kann helfen, kompromittierte Clients zu erkennen, bevor Sie ausgeführt werden. Da der patchingmechanismus das verfügbar machen von ausführbaren Dateien und dll-Binärdateien erfordert, die nicht durch die standardmäßigen schreibgeschützten Berechtigungen für Programmdateien geschützt sind, ist die Überprüfung dieser Dateien vor dem Starten für die allgemeine Systemsicherheit wichtig.

Dieses Modell versucht nicht, mit dem Benutzer Szenario für böswillige Administratoren umzugehen, bei dem das Lade Programm selbst kompromittiert werden kann, sondern konzentriert sich auf den Schutz von Standard Benutzern vor versehentlichem Ausführen von Manipulations Code. Herkömmliche Server-Client Validierungsverfahren sind die einzige mögliche Entschärfung für böswillige Client Systemadministratoren.

## <a name="construction-of-the-trust-worthy-loader-application"></a>Erstellung der Trust-Worthy Lade Anwendung

### <a name="background-reading"></a>Hintergrund Lesevorgänge

Die Leser sollten sich mit der folgenden Dokumentation vertraut machen, in der Details der Grundlagen der Grundlagen zur Sicherstellung der softwarebasierten Vertrauensstellung erläutert werden.

<dl> <dt>

<span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>Code Signatur
</dt> <dd>

[Authenticode-Signierung für Spieleentwickler](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>SignTool
</dt> <dd>

[SignTool](/windows/desktop/SecCrypto/signtool) auf MSDN

</dd> </dl>

Im folgenden Abschnitt werden die APIs erläutert, die zum Erstellen der Lade Programme verwendet werden sollen, die das Festplattenlayout für die Installation und Überprüfung der Vertrauens Überprüfung unterstützen.

### <a name="installation-of-the-trusted-loader-and-patcher"></a>Installation des vertrauenswürdigen Lade Moduls und Patcher

Das vertrauenswürdige Lade Programm und die Basisversion des Dienstprogramms "Patcher" sollten auf der HDD genauso wie bei herkömmlichen Installationen unter dem Ordner "geschützte Programmdateien" installiert werden. Für die Installation und das Patchen der Lade Anwendung sind Administratorrechte erforderlich. Daher ist es wichtig, die Aktualisierungshäufigkeit für das Lade Modul zu minimieren, um sicherzustellen, dass Endbenutzer nicht häufig erhöhte Rechte benötigen, obwohl Windows Installer eingeschränkte benutzerpatching verwendet werden kann, um die Erhöhung der Lade lastenpatches zu vermeiden

Weitere Informationen finden Sie im Artikel Patching Game Software in Windows XP, Windows Vista und Windows 7.

### <a name="installation-of-the-game-executables-dlls-and-data"></a>Installation der ausführbaren Spieldateien, DLLs und Daten

Um Standard Benutzer Updates des Spiels ohne Administratorrechte zu ermöglichen, müssen die ausführbaren Dateien, DLLs und Daten in einem Bereich der Festplatte installiert werden, auf den alle Benutzer zugreifen können. Das Betriebssystem stellt den Bereich "alle Benutzer Anwendungsdaten" bereit, der als Standard Speicherort für die Installation verwendet werden kann. " [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) " sollte mit dem allgemeinen CSIDL- \_ AppData-Schlüssel verwendet werden \_ , um den Dateipfad für diesen Bereich zu ermitteln. Es ist wichtig, dass keine Annahmen über den Pfad erfolgen, mit dem dieser Schlüssel zurückkehrt, da er vom Benutzer konfigurierbar sein kann.

Die Installation muss die Ordner Berechtigungen ändern oder verwalten, um den vollständig Benutzer freigegebenen Schreibzugriff zu erreichen, der zum Aktualisieren des Titels benötigt wird. Mit den richtigen Berechtigungen kann die Game Updater-Funktionalität des Lade Programms das Spiel problemlos Patchen, ohne dass für Benutzerkonten besondere Berechtigungen erforderlich sind, einschließlich Zeiten, wenn Sie von Standard Benutzern gestartet werden.

### <a name="access-control-list-modification-code"></a>Code zur Access Control Listen Änderung

Für Windows XP müssen Sie Code ausführen, um die Zugriffs Steuerungs Liste (ACL) manuell zu ändern. im folgenden finden Sie eine Beispiel Funktion, die die Vorgehensweise veranschaulicht:

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

Dieses Codebeispiel funktioniert auch für Windows Vista und Windows 7. Sie bieten jedoch auch das Befehlszeilen-Hilfsprogramm icacls zum Bearbeiten von Datei-ACLs, die Sie stattdessen verwenden können.

Das Tool bietet eine ausführliche Hilfe, wenn Sie jedoch eine Beispiel Verwendung für das Tool ausführen:

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

Durch diese Verwendung erhält der Benutzer Rex die Berechtigung zum Löschen und Schreiben von DAC für den Spiel Ordner, der in den Bereichen alle Benutzer der Festplatte gespeichert ist.

### <a name="installations-for-advanced-users"></a>Installationen für fortgeschrittene Benutzer

Für erweiterte Benutzer Installationsszenarien kann ein Benutzer den Installationspfad des Games manuell angeben. Die Verzeichnis Auswahl sollte auf eine externe Seite der Programmdateien beschränkt werden, um sicherzustellen, dass sich der Ordner in einem wirklich shardbaren Bereich der Festplatte befindet. Der vom Benutzer ausgewählte Pfad sollte nur für die Spiele und Daten verwendet werden, da das Spiel Lade Programm und die Patcher-exe-Dateien immer im Ordner sichere Programmdateien installiert werden müssen, um die Sicherheit zu erhöhen.

### <a name="the-loaders-verification-of-trust"></a>Überprüfung der Vertrauensstellung durch das Lade Modul

Windows stellt die [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) -Funktion zum Überprüfen der Gültigkeit von signiertem Code bereit und basiert auf den Kryptografiediensten im Betriebssystem. Die-Funktion ist auf MSDN: **WinVerifyTrust** -Funktion vollständig dokumentiert.

Im folgenden Beispielprogramm auf MSDN wird erläutert, wie die-Funktion verwendet wird, um zu bestimmen, ob eine ausführbare Programmdatei mit einem gültigen Zertifikat signiert ist: [example C program: Überprüfen der Signatur einer PE-Datei](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file).

Um zu überprüfen, ob die ausführbare Datei für das signierte Spiel vertrauenswürdig für die Ausführung innerhalb des Lade Programm ist, genügt die generische Verify-Aktion:

<dl> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Wintrust- \_ Aktion, \_ generische \_ Überprüfung \_ v2

</dd> <dt>

<span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>D.h.
</dt> <dd>

Überprüfen Sie eine Datei oder ein Objekt mit dem Authenticode-Richtlinien Anbieter.

</dd> </dl>

Die-Funktion nimmt ein Eingabe Struktur Argument an, das Informationen enthält, die der Vertrauensstellungs Anbieter benötigt, um die angegebene Aktion zu verarbeiten. In der Regel enthält die-Struktur, wie im vorherigen Beispiel Fall, Informationen, die das Objekt identifizieren, das der Vertrauensstellungs Anbieter auswerten muss.

Das Format der-Struktur ist spezifisch für den Aktions Bezeichner. Im folgenden Thema auf MSDN finden Sie eine Beispiel Struktur für den wintrust-Anbieter: [**wintrust- \_ Daten**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) Struktur.

Wenn der Vertrauensstellungs-Provider überprüft, ob der Betreff für die angegebene Aktion vertrauenswürdig ist, ist der Rückgabewert 0 (null). Kein anderer Wert neben NULL sollte als erfolgreiche Rückgabe angesehen werden.

### <a name="data-validation"></a>Datenüberprüfung

Der koentwurfs Mechanismus unterstützt nur das Signieren einiger bestimmter Dateitypen, einschließlich ausführbarer Dateien, DLLs, Windows Installer Paketen (MSI-Dateien) und CAB-Dateien (CAB-Dateien). Die [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) -API sollte nicht verwendet werden, um zu überprüfen, ob große Datendateien (z. b. CAB-Dateien) manipuliert wurden, da bei der Überprüfung sehr großer Dateien einige Probleme mit der Leistung und der Stabilität auftreten. Programm ausführbare Dateien sind tendenziell klein genug, damit eine voll vertrauenswürdige Überprüfung mithilfe des wintrust-Anbieters erfolgen muss, aber Datendateien für Spiele liegen häufig im Bereich von vielen Gigabyte. Der Ansatz, den das Lade Modul für die Überprüfung von Spieldaten übernimmt, sollte eine kleine Stichprobe des Datasets über die Laufzeit des Spiels getestet werden. Bei diesem Ansatz werden die Kosten der Überprüfungs Tests für die Lebensdauer der Spiel Wiedergabe verbreitet, und die Benutzer können ohne lange Wartezeit nahtlos bereitgestellt werden. Um dies zu erreichen, ist möglicherweise eine sorgfältige Organisation der Daten erforderlich. Einige mmugs verwenden einen Daten Bank Ansatz, der die Verwaltung, Wartung und Überprüfung der Richtigkeit von Spielobjekten im Zeitverlauf unterstützt.

Aus Sicht der Sicherheit sollte der Client Code so entworfen werden, dass Datendateien nicht als vertrauenswürdig eingestuft werden, auch wenn eine grundlegende Datenüberprüfung mit dem vertrauenswürdigen Lade Modul verwendet wird. Header Überprüfungen, Hashwerte und andere herkömmliche Integritätsprüfungen sollten eingesetzt werden. Die Arbeit zum Festschreiben des e/a-Codes des Clients sollte auch mithilfe von Techniken wie dem Testen von Tests erfolgen, und Sie profitieren von automatischen Tools für die statische Code Analyse, wie z. b. den **/analyze** -Switch in Visual Studio 2005 und Visual Studio 2008 (verfügbar in Visual Studio Team System und dem kostenlosen Compiler, der in der Windows SDK enthalten ist).

Weitere Informationen zur Software Sicherheit finden Sie unter [Bewährte Sicherheitsmethoden bei der Spieleentwicklung](/windows/desktop/DxTechArts/best-security-practices-in-game-development).

 

 