---
description: 'In diesem Thema wird erläutert, wie Sie ein Programm in der Windows-Registrierung als einen der folgenden Clienttypen registrieren: Browser, E-Mail, Medienwiedergabe, Instant Messaging oder virtueller Computer für Java.'
title: Registrieren von Programmen mit Clienttypen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9c2d9a4589b684580250c487a6f83c3c9e79dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470418"
---
# <a name="registering-programs-with-client-types"></a>Registrieren von Programmen mit Clienttypen

In diesem Thema wird erläutert, wie Sie ein Programm in der Windows-Registrierung als einen der folgenden Clienttypen registrieren: Browser, E-Mail, Medienwiedergabe, Instant Messaging oder virtueller Computer für Java.

> [!Note]  
> Diese Informationen gelten für die folgenden Betriebssysteme:
> 
> -   Windows 2000 Service Pack 3 (SP3)
> -   Windows 2000 Service Pack 4 (SP4)
> -   Windows XP Service Pack 1 (SP1)
> -   Windows XP Service Pack 2 (SP2)
> -   Windows XP Service Pack 3 (SP3)
> -   Windows Server 2003
> -   Windows Vista
> -   Windows Vista Service Pack 1 (SP1)
> -   Windows 8

 

Das Thema enthält folgende Abschnitte:

-   [Allgemeine Registrierungselemente für alle Clienttypen](#common-registration-elements-for-all-client-types)
    -   [Auswählen eines kanonischen Namens](#selecting-a-canonical-name)
    -   [Registrieren des Anzeigenamens eines Programms](#registering-a-programs-display-name)
    -   [Registrieren des Symbols eines Programms](#registering-a-programs-icon)
    -   [Registrieren eines offenen Verbs](#registering-an-open-verb)
    -   [Registrieren von Installationsinformationen](#registering-installation-information)
-   [Registrierungselemente für bestimmte Clienttypen](#registration-elements-for-specific-client-types)
    -   [Registrierung im Startmenü](#start-menu-registration)
    -   [Registrierung des E-Mail-Clients](#mail-client-registration)
-   [Vollständige Beispielregistrierungen](#complete-sample-registrations)
    -   [Beispielbrowser](#a-sample-browser)
    -   [Ein Beispiel-E-Mail-Browser](#a-sample-mail-browser)
    -   [Beispiel Media Player](#a-sample-media-player)
    -   [Ein Beispiel für ein Instant Messenger-Programm](#a-sample-instant-messenger-program)
    -   [Ein virtueller Beispielcomputer für Java](#a-sample-virtual-machine-for-java)
-   [Zugehörige Themen](#related-topics)

In diesem Thema wird die vorhandene Dokumentation zum Registrieren eines Programms als bestimmter Clienttyp erweitert. Links zu dieser Dokumentation finden Sie im Abschnitt Verwandte Themen.

## <a name="common-registration-elements-for-all-client-types"></a>Allgemeine Registrierungselemente für alle Clienttypen

Wenn Sie ein Programm als Clienttyp registrieren, sind die meisten Registrierungseinträge unabhängig vom Clienttyp identisch. Einige Registrierungseinträge sind jedoch spezifisch für den Clienttyp, und diese sind im Abschnitt [Registrierungselemente für bestimmte Clienttypen](#registration-elements-for-specific-client-types) angegeben.

In diesem Abschnitt werden die folgenden Themen erläutert:

-   [Auswählen eines kanonischen Namens](#selecting-a-canonical-name)
-   [Registrieren des Anzeigenamens eines Programms](#registering-a-programs-display-name)
-   [Registrieren des Symbols eines Programms](#registering-a-programs-icon)
-   [Registrieren eines offenen Verbs](#registering-an-open-verb)
-   [Registrieren von Installationsinformationen](#registering-installation-information)

> [!Note]  
> Unterschlüsselnamen, die in diesem Thema in italisch angegeben werden, sind Platzhalter für benutzerdefinierte Unterschlüsselnamen oder eine Reihe möglicher Werte. Vollständige Beispiele mit Beispielnamen finden Sie im Abschnitt [Vollständige Beispielregistrierungen.](#complete-sample-registrations)

 

Alle Registrierungsinformationen des Clienttyps werden unter dem folgenden Unterschlüssel gespeichert:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

*ClientTypeName* ist einer der folgenden Unterschlüsselnamen:

-   StartMenuInternet (für Browser)
-   E-Mail (für E-Mail)
-   Medien (für die Medienwiedergabe)
-   IM (für Instant Messaging)
-   JavaVM (für virtuelle Computer für Java)

In diesem Thema werden Sie Verweise auf ein fiktives Computerprogramm namens "Lit View" von Litware Inc. mit einer ausführbaren Datei namens Litview.exe. Dieses hypothetische Programm wird austauschbar als Instant Messenger, als Browser oder als andere Art von Clientprogramm verwendet, wenn dies zu Veranschaulichungszwecken erforderlich ist.

### <a name="selecting-a-canonical-name"></a>Auswählen eines kanonischen Namens

Der Hersteller muss einen *kanonischen Namen für* das Programm auswählen. Der kanonische Name wird dem Benutzer nie angezeigt, sodass er nicht lokalisiert werden muss. Der einzige Zweck besteht in der Bereitstellung einer eindeutigen Zeichenfolge, die zum Identifizieren des Programms verwendet werden kann. Es ist in der Regel identisch mit dem englischen Namen des Programms, aber dies ist lediglich eine Konvention.

Für andere Clienttypen als Browser kann der kanonische Name eine beliebige Zeichenfolge sein. Wählen Sie einen eindeutigen Namen aus, der wahrscheinlich nicht von einem anderen Anbieter verwendet wird.

Bei Browserclients muss der kanonische Name der Name der zugeordneten ausführbaren Datei sein , einschließlich der Erweiterung. Beispiel: "Litview.exe".

Hier sind einige Beispiele für kanonische Namen.

-   Iexplore.exe (Browser)
-   Windows E-Mail (E-Mail)
-   Windows Media Player (Medien)
-   Windows Messenger (Instant Messaging)

Registrieren Sie den kanonischen Namen, indem Sie wie hier gezeigt einen Unterschlüssel erstellen. Der Name des Unterschlüssels ist der kanonische Name. Alle Informationen im Zusammenhang mit der Registrierung dieses Programms sind unter diesem Unterschlüssel vorhanden.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a>Registrieren des Anzeigenamens eines Programms

Der nächste Schritt bei der Registrierung besteht im Angeben des Anzeigenamens des Programms. Sie wird wie hier gezeigt als Wert unter dem kanonischen Namensschlüssel angegeben. Beachten Sie *erneut, dass CanonicalName* und *ClientTypeName* nicht die tatsächlichen Namen der Schlüssel sind, sondern nur Platzhalter für die tatsächlichen Namen, z. B. *Lit View*.

> [!Note]  
> Ab Windows 8 sollte der Name, der zum Registrieren für Set Program Access [](default-programs.md) [and Computer Defaults (SPAD)](cpl-setprogramaccess.md) und für Standardprogramme verwendet wird, übereinstimmen, damit SPAD-Änderungen Standardprogrammregistrierungen auslösen.

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

Der **LocalizedString-Wert** ist eine REG SZ-Zeichenfolge und besteht aus einem "at"-Zeichen (@), dem vollständigen Pfad zu einer .dll- oder .exe-Datei, einem Komma, einem Minuszeichen und einer dezimalen ganzen \_ Zahl. Die ganze Dezimalzahl ist die ID einer Zeichenfolgenressource, die in der .dll- oder .exe-Datei enthalten ist, deren Wert dem Benutzer als Name dieses Clients angezeigt werden soll. Beachten Sie, dass der Dateipfad keine Anführungszeichen erfordert, auch wenn er Leerzeichen enthält.

Wenn Sie die Anzeigenamenzeichenfolge auf diese Weise registrieren, kann dieselbe Registrierung für mehrere Sprachen verwendet werden. Jede Sprachinstallation bietet eine andere Ressourcendatei mit dem Anzeigenamen, der unter der gleichen Ressourcen-ID gespeichert ist.

Das folgende Beispiel zeigt die Registrierung für ein fiktives Lit View-Instant Messaging-Programm. Da es sich um ein Instant Messaging-Programm handelt, wird der *Unterschlüssel CanonicalName* (in diesem Fall *Lit View)* unter dem **Im-Unterschlüssel** gespeichert.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Beachten Sie die Verwendung des Eintrags (Standard) als sekundäre Deklaration des Anzeigenamens des Clients. Wenn **LocalizedString nicht** vorhanden ist, wird stattdessen der (Standard)-Wert verwendet. Dies funktioniert mit allen Clienttypen (Internetbrowser, E-Mail-Browser, Instant Messenger und Media Player). Aus Gründen der Abwärtskompatibilität mit dem [Internet Explorer-Clientregistrierungslayout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))sollten E-Mail-Programme den (Standard)-Wert des *Unterschlüssels CanonicalName* auf den Anzeigenamen des Clients in der aktuell installierten Sprache festlegen.

### <a name="registering-a-programs-icon"></a>Registrieren des Symbols eines Programms

> [!Note]  
> Dieser Abschnitt gilt nicht für Windows 2000.

 

Standardmäßig enthält der obere Abschnitt Windows XP- und Windows **Vista-Startmenü** **Internet-** und **E-Mail-Symbole.** Diese Symbole sind in Windows 7 und höher nicht vorhanden. Wenn für Browser- und E-Mail-Clients ein Programm als Standard für seinen Clienttyp zugewiesen wird, wird das registrierte Symbol dieses Programms für diese **Startmenüeinträge** angezeigt.

Das Registrieren des Symbols eines Programms ist für Browser- und E-Mail-Clients obligatorisch. Das Registrieren eines Symbols für die Medienwiedergabe, das Instant Messaging oder den virtuellen Computer für Java-Clienttypen ist optional, und registrierte Symbole für diese Clienttypen werden derzeit nicht von Windows verwendet und nicht im oberen Abschnitt des Windows XP- oder Windows **Vista-Startmenüs** angezeigt.

Um ein Symbol für ein Clientprogramm zu registrieren, fügen Sie einen **DefaultIcon-Unterschlüssel** mit einem Standardwert hinzu, wie hier gezeigt.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

Der **FilePath-Wert** ist der vollständige Pfad zu der Datei, die das Symbol enthält. Dieser Pfad erfordert keine Anführungszeichen, auch wenn er Leerzeichen enthält.

Der **IconIndex-Wert** wird wie folgt interpretiert:

-   Wenn **IconIndex** eine positive Zahl ist, wird die Zahl als Index des *nullbasierten* Arrays von Symbolen verwendet, die in der Datei gespeichert sind. Wenn **IconIndex** beispielsweise 1 ist, wird das zweite Symbol aus der Datei geladen.
-   Wenn **IconIndex eine** negative Zahl ist, wird der absolute Wert von **IconIndex** als Ressourcenbezeichner (anstelle des Indexes) für das Symbol verwendet. Wenn **IconIndex** beispielsweise -3 ist, wird das Symbol, dessen Ressourcenbezeichner 3 ist, aus der Datei geladen.

Das folgende Beispiel zeigt die Registrierung eines hypothetischen Lit View-Browsers. Das zweite Symbol, das in der Litview.exe gespeichert ist, wird als Standard verwendet.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a>Registrieren eines offenen Verbs

> [!Note]  
> Dieser Abschnitt gilt nicht für Windows 2000. Der folgende Schritt ist nur für Browser- und E-Mail-Clients erforderlich.

 

Angenommen, ein Benutzer hat Ihr Programm als Standard-Internet- oder E-Mail-Programm ausgewählt. Dieser Benutzer klickt auf das **Internet-** oder **E-Mail-Symbol** im Windows XP oder Windows **Vista-Startmenü,** um das Programm zu öffnen. An diesem Punkt wird die hier registrierte Befehlszeile ausgeführt.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

Die Befehlszeile muss einen vollqualifizierten absoluten Pfad zur Datei gefolgt von optionalen Befehlszeilenoptionen angeben. Wenn der Eintragstyp REG EXPAND SZ ist, können \_ \_ Umgebungsvariablen im Pfad verwendet werden. Verwenden Sie anführungszeichen entsprechend, um sicherzustellen, dass Leerzeichen in der Befehlszeile nicht falsch interpretiert werden. Die Befehlszeile sollte das Programm mit den entsprechenden Standardwerten ausführen. Browser verwenden in der Regel standardmäßig die Startseite des Benutzers. E-Mail-Programme öffnen in der Regel den **Posteingang des Benutzers.**

Das folgende Beispiel zeigt die Registrierung eines `open` Verbs für einen hypothetischen Lit View-Browser. Sie gibt keine Befehlszeilenoptionen an.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

Beachten Sie, dass in diesem Wert Anführungszeichen um den Pfad platziert werden, da er eingebettete Leerzeichen enthält. Das Weglassen dieser Anführungszeichen kann dazu führen, dass die Befehlszeile falsch interpretiert wird.

### <a name="registering-installation-information"></a>Registrieren von Installationsinformationen

> [!Note]  
> Dieser Abschnitt gilt nicht für Windows Server 2003.

 

-   [Befehl "Neu installieren"](#the-reinstall-command)
-   [Befehl "Symbole ausblenden"](#the-hide-icons-command)
-   [Befehl "Symbole anzeigen"](#the-show-icons-command)
-   [Konfiguration des Gruppenprogramms](#group-program-configuration)
-   [Beispiel für die Browserregistrierung](#browser-registration-example)

Das Feature, mit dem der Benutzer computerspezifische Standardprogramme auswählt, wird benannt, und es wird darauf zugegriffen, wie in der folgenden Tabelle gezeigt. (Windows Vista das neue Feature Set **your default programs**(Standardprogramme festlegen) eingeführt, mit dem benutzerspezifische Standardwerte festgelegt werden können.)




| Betriebssystem | Titel | Zugriffsort | 
|------------------|-------|-----------------|
| Windows 7 | Festlegen der Standardeinstellungen für Programmzugriff und Computer | <ul><li>Option <strong>"Standardprogramme" im Startmenü</strong> <strong></strong></li><li><strong>Standardprogramme</strong> Systemsteuerung Element</li></ul> | 
| Windows Vista | Festlegen der Standardeinstellungen für Programmzugriff und Computer | <ul><li>Option <strong>"Standardprogramme" im Startmenü</strong> <strong></strong></li><li><strong>Standardprogramme</strong> Systemsteuerung Element</li></ul> | 
| Windows XP SP2 | Festlegen von Programmzugriff und Standardwerten | <ul><li><strong>Startmenü</strong></li><li><strong>Hinzufügen oder Entfernen von Programmen</strong> Systemsteuerung Element</li></ul> | 
| Windows XP SP1 | Konfigurieren von Programmen | <ul><li><strong>Hinzufügen oder Entfernen von Programmen</strong> Systemsteuerung Element</li></ul> | 




 

Der Einfachheit halber wird in diesem Thema der titel Windows 7 des Features verwendet. Alle Versionen des Features werden häufig als SPAD bezeichnet.

> [!Note]  
> Wenn Sie Windows 2000 oder Windows XP ausführen, muss mindestens Windows 2000 SP3 oder Windows XP SP1 installiert  sein, um die Seite Programmzugriff und Standardwerte festlegen anzuzeigen. In Windows Vista und höher sind für den Zugriff auf die Seite Programmzugriff und **Computereinstellungen** festlegen Administratorrechte erforderlich. Aus diesem Grund wird Entwicklern empfohlen, sich für das Element Set [your default programs](default-programs.md) Systemsteuerung (Standardprogramme festlegen) zu registrieren, damit jeder Benutzer die Standardeinstellungen der Anwendung verwalten kann.

 

Die folgende Registrierungsstruktur zeigt die Vielzahl von Informationen, die im **InstallInfo-Schlüssel** des Programms registriert werden müssen, damit das Programm auf der Seite Programmzugriff und **Computereinstellungen** festlegen als Option für seinen Clienttyp angezeigt wird. Jeder dieser Werte wird in den folgenden Abschnitten ausführlich erläutert.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

Die Befehlszeile muss einen vollqualifizierten absoluten Pfad zur Datei gefolgt von optionalen Befehlszeilenoptionen angeben. Verwenden Sie anführungszeichen entsprechend, um sicherzustellen, dass Leerzeichen in der Befehlszeile nicht falsch interpretiert werden.

### <a name="the-reinstall-command"></a>Befehl "Neu installieren"

Die im Wert ReinstallCommand deklarierte **Neuinstallationsbefehlszeile** wird ausgeführt, wenn der Benutzer auf der Seite Programmzugriff und Computereinstellungen festlegen ihr Programm als Standard für seinen Clienttyp auswählt. In Windows Vista und höher erfordert der Zugriff auf diese Seite eine Administratorberechtigungsstufe. Wenn Sie in Windows 8 Ihre Anwendung mit demselben Namen sowohl für Programmzugriff festlegen als auch für **Computereinstellungen** und Standardprogramme registriert haben, werden die **in** Standardprogramme für diese Anwendung angegebenen Standardwerte für den aktuellen Benutzer angewendet und der **Neuinstallationsbefehl** ausgeführt.

Das von der Neuinstallationsbefehlszeile gestartete Programm [](fa-intro.md) muss [](/previous-versions//aa767743(v=vs.85)) die Anwendung dem vollständigen Satz von Datei- und Protokolltypen zuordnen, die die Anwendung verarbeiten kann. Alle Anwendungen müssen die Handlerfunktion im Neuinstallationsbefehl einrichten. Anwendungen können den Befehl "neu installieren" verwenden, um funktionen zu registrieren und optional den Standardstatus zu erstellen. Wenn sich eine Anwendung dafür entscheidet, sowohl den Funktions- als auch den Standardhandlerstatus im Neuinstallationsbefehl zu implementieren, sollte sie auch alle gewünschten sichtbaren Links oder Tastenkombinationen bzw. Verknüpfungen erneut ausführen. Die sichtbaren Einstiegspunkte, die von den meisten Anwendungen verwendet werden, sind im [Befehl Symbole ausblenden aufgeführt.](#the-hide-icons-command)

> [!Note]  
> Es wird dringend empfohlen, dass Anwendungen die Behandlungsfunktion im Neuinstallationsbefehl implementieren.

 

Sobald der Neuinstallationsvorgang abgeschlossen ist, sollte das von der Neuinstallationsbefehlszeile gestartete Programm beendet werden. Das entsprechende Programm sollte nicht gestartet werden. Es sollten lediglich Standardwerte registriert werden. Beispielsweise sollte der Neuinstallationsbefehl für einen Browser die Startseite des Benutzers nicht öffnen.

> [!Note]  
> Für Browser- und E-Mail-Clients in Windows XP und Windows Vista sollten Sich Anwendungen, die sowohl die Behandlungsfunktion als auch den Standardstatus im Neuinstallationsbefehl festlegen, für das entsprechende Symbol am oberen Startmenü. Weitere [Informationen finden Sie unter Startmenüregistrierung.](#start-menu-registration)

 

### <a name="the-hide-icons-command"></a>Befehl "Symbole ausblenden"

Die im HideIconsCommand-Wert deklarierte Befehlszeile wird ausgeführt,  wenn der Benutzer das Feld Zugriff auf dieses Programm aktivieren auf der Seite Programmzugriff und **Computereinstellungen festlegen deaktiviert.** Diese Befehlszeile muss alle Zugriffspunkte Ihres Programms ausblenden, die auf der Benutzeroberfläche sichtbar sind. Die spezifischen Richtlinien sind das Entfernen von Verknüpfungen und Symbolen aus den folgenden Speicherorten:

-   Desktopsymbole
-   Startmenü, einschließlich der **Startgruppe**
-   Schnellstart von Balkenlinks
-   Benachrichtigungsbereich
-   Kontextmenüs
-   Ordner-Taskband

Diese Befehlszeile muss auch automatische Aufrufe des Programms verhindern, z. B. die im Registrierungsschlüssel **Ausführen** angegebenen Aufrufe. Anbietern wird empfohlen, diese Richtlinien im Rückruf Zugriff ausblenden der Anwendung zu implementieren.

Sie müssen die Registrierung (Anwendungsfunktion) von Dateitypen nicht abgeben, wenn Symbole ausgeblendet sind. Sie müssen auch nicht den Standardstatus der Anwendung für Datei- und Protokolltypen abgeben. Dies kann zu einer schlechten Benutzererfahrung führen, wenn diese Typen auf der Benutzeroberfläche auftreten.

Nach dem erfolgreichen Ausblenden von Symbolen müssen Sie den Registrierungswert IconsVisible wie gezeigt auf 0 (0) aktualisieren:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

Der Eintrag IconsVisible ist vom Typ **REG \_ DWORD.**

### <a name="an-alternate-hide-icons-method-in-spad"></a>Eine alternative Methode zum Ausblenden von Symbolen in SPAD

Bei einigen Legacyanwendungen ist eine vollständige Implementierung von Zugriff ausblenden möglicherweise nicht praktikabel. Eine alternative Methode, die den gleichen Effekt erzielt, ist die Deinstallation der Anwendung. Der folgende Abschnitt zeigt Beispielverhalten und Beispielcode zum Implementieren dieser Alternative. Im Allgemeinen sollten unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) diese Alternative vermeiden, da sie:

-   Deinstallieren Sie die Anwendung vollständig aus dem System.
-   Entfernt zuvor ausgewählte Standardwerte.
-   Lassen Sie keine Benutzeroberflächenoption, um die Anwendung neu zu installieren.
-   Stellen Sie das Feature "Zugriff aktivieren" nicht mehr zur Verfügung, da eine Deinstallation die Anwendung vollständig aus SPAD entfernt.

Die empfohlene Benutzeroberfläche lautet wie folgt:

-   Wenn der Benutzer das Kontrollkästchen Zugriff **auf** dieses Programm aktivieren in SPAD deaktiviert, wird die folgende Benutzeroberfläche angezeigt.

    ![Dialogfeld zum Ausblenden des Zugriffs auf das Programm](images/hideaccessvista.png)

-   Wenn der Benutzer OK **auswählt,** **wird** das Systemsteuerung gestartet, damit der Benutzer die Anwendung deinstallieren kann.
-   Windows Xp-Benutzern sollte dieses Dialogfeld angezeigt werden.

    ![Entsprechendes Windows XP-Dialogfeld](images/hideaccessxp.png)

-   Wenn der Windows XP-Benutzer **OK** auswählt, wird das Element **Software** Systemsteuerung gestartet, damit der Benutzer die Anwendung deinstallieren kann.

Der folgende Code stellt eine wiederverwendbare Implementierung für das Feature Zugriff ausblenden bereit, wie oben beschrieben. Sie kann auf Windows XP, Windows Vista und Windows 7 verwendet werden.


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a>Befehl "Symbole anzeigen"

Die im Eintrag ShowIconsCommand deklarierte Befehlszeile wird ausgeführt, wenn der Benutzer auf der Seite **Programmzugriff und Computerstandardeinstellungen festlegen** das Feld **Zugriff auf dieses Programm aktivieren** überprüft. Über diese Befehlszeile können die Zugriffspunkte Ihres Programms wiederhergestellt werden, einschließlich derer im **Startmenü,** auf dem Desktop und in der **Startgruppe** sowie normale automatische Aufrufe, z. B. die im Registrierungsschlüssel **Ausführen** angegebenen. Die sichtbaren Zugriffspunkte, die für die meisten Anwendungen von Interesse sind, sind im [Befehl Symbole ausblenden](#the-hide-icons-command)aufgeführt. Die Standardeinstellungen pro Benutzer sollten von der Anwendung nicht geändert werden. Diese Änderung sollte vom Benutzer über **Standardprogramme** vorgenommen werden.

Nachdem Sie Ihre Symbole erfolgreich angezeigt haben, müssen Sie den Registrierungswert IconsVisible wie gezeigt auf 1 aktualisieren:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

Beachten Sie Folgendes: Wenn Sie den Eintrag HideIconsCommand verwendet haben, um eine Deinstallation der Anwendung anzufordern, wird der Eintrag ShowIconsCommand nicht verwendet. Sie sollte während der Deinstallation mit den restlichen Informationen der Anwendung aus der Registrierung entfernt werden.

### <a name="group-program-configuration"></a>Konfiguration des Gruppenprogramms

> [!Note]  
> Dieser Abschnitt gilt nicht für Windows 2000.

 

Im Rahmen der Systemvorbereitung kann ein OEM eine Konfiguration einrichten, die Zugriffspunkte für den Microsoft-Browser, E-Mail, Medienwiedergabe, Instant Messaging oder den virtuellen Computer für Java-Clientprogramme ausblendet und eigene Standardprogramme angibt. OEMs können es Benutzern ermöglichen, ihre Computer jederzeit auf diese Standardkonfiguration zurückzusetzen, indem sie die folgenden Registrierungswerte festlegen.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

Wenn diese Schlüssel festgelegt sind, können Benutzer die OEM-Konfiguration wiederherstellen, indem sie auf der Seite **Programmzugriff und Computerstandardeinstellungen festlegen** die Option **Computerhersteller** auswählen. Wenn diese Schlüssel nicht festgelegt sind, wird die Option **Computerhersteller** nicht angezeigt.

Der Eintrag **OEMShowIcons** legt ggf. das Symbol zum Anzeigen des Zustands für den angegebenen Client fest, der angewendet wird, wenn der Benutzer **Computerhersteller** auswählt. Der Wert 1 bewirkt, dass Symbole angezeigt werden, und der Wert 0 bewirkt, dass Symbole nicht angezeigt werden. Wenn **OEMShowIcons** nicht vorhanden ist, wirkt sich die Auswahl von **Computerhersteller** nicht auf die Einstellung symbol show aus. **OEMShowIcons** ist vom Typ **REG \_ DWORD.**

Wenn der **OEMDefault-Eintrag** vorhanden und auf 1 festgelegt ist, wird die OEM-Einstellung für den Standardclient des angegebenen Typs festgelegt. Nur ein Client eines bestimmten Typs kann als OEM-Standard markiert werden. Wenn mehr als die Registrierung eines Clients den **OEMDefault-Eintrag** enthält, werden alle ignoriert, und der aktuelle Client wird weiterhin als Standardclient verwendet. Wenn der **OEMDefault-Eintrag** nicht vorhanden oder vorhanden ist und auf 0 festgelegt ist, wird dieser bestimmte Client nicht als Standardclient verwendet, wenn der Benutzer **Computerhersteller** auswählt. **OEMDefault** ist vom Typ **REG \_ DWORD.**

Zusätzlich zur Option, ihre Computer auf die vom OEM festgelegte Standardkonfiguration zurückzusetzen, haben Benutzer drei weitere Konfigurationsoptionen:

-   Legen Sie ihren Computer auf eine Microsoft Windows-Konfiguration fest. In diesem Fall ermöglicht die Seite **Programmzugriff und Computerstandardeinstellungen festlegen** den Zugriff auf alle Microsoft- und Nicht-Microsoft-Software auf dem Computer, der in den relevanten Produktkategorien registriert ist. Microsoft Windows-Programme werden als Standardoption für jede Kategorie ausgewählt.
-   Legen Sie ihren Computer auf eine Nicht-Microsoft-Konfiguration fest. Diese Konfiguration blendet Zugriffspunkte (z. B. das **Startmenü)** für Windows Internet Explorer, Windows Media Player, Windows Messenger und Microsoft Outlook Express aus. Sie ermöglicht den Zugriff auf die Nicht-Microsoft-Software auf dem Computer in diesen Kategorien. Wenn außerdem ein Nicht-Microsoft-Programm in einer Kategorie verfügbar ist, wird es als Standard für diese Kategorie festgelegt. Wenn mehrere Nicht-Microsoft-Programme in einer Kategorie verfügbar sind, wird der Benutzer aufgefordert, auszuwählen, welches Nicht-Microsoft-Programm als Standard verwendet werden soll.
-   Richten Sie eine benutzerdefinierte Konfiguration ein. Benutzer treffen ihre eigene Auswahl zum Aktivieren oder Entfernen des Zugriffs, indem sie Microsoft- und Nicht-Microsoft-Programme nach Bedarf kombinieren. Benutzer richten Standardoptionen kategorieweise ein.

Benutzer können diese Optionen jederzeit ändern.

### <a name="browser-registration-example"></a>Beispiel für die Browserregistrierung

Das folgende Beispiel zeigt die vollständige **InstallInfo-Registrierung** für einen fiktiven Lit View-Browser. In diesem Fall ermöglichen die Befehlszeilenschalter dem Litview.exe Datei, alle aktionen auszuführen, die für jeden Wert erforderlich sind.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

Beachten Sie, dass anführungszeichen um die Pfade platziert werden, da sie eingebettete Leerzeichen enthalten.

## <a name="registration-elements-for-specific-client-types"></a>Registrierungselemente für bestimmte Clienttypen

Die folgenden Informationen finden Sie auch in den Ressourcen, die am Ende dieses Themas im Abschnitt Verwandte Themen aufgeführt sind.

-   [Registrierung im Startmenü](#start-menu-registration)
-   [E-Mail-Clientregistrierung](#mail-client-registration)

### <a name="start-menu-registration"></a>Registrierung im Startmenü

Unter Windows XP registrierten Anwendungen in der Regel Standardwerte auf einem computerweiten Bereich **(HKEY \_ LOCAL \_ MACHINE)** anstelle eines Benutzerbereichs **(HKEY \_ CURRENT \_ USER).** Mit dem Windows Vista-Einführung der Benutzerkontensteuerung (User Account Control, UAC) müssen Anwendungen, die die **Internet-** und **E-Mail-Slots** im **Startmenü** beanspruchen, den Neuinstallationsbefehl im richtigen Ausführungskontext implementieren.

> [!Note]  
> Der Startmenü **E-Mail-Link** wurde ab Windows 7 entfernt. Die in diesem Abschnitt beschriebene Registrierung sollte jedoch weiterhin ausgeführt werden, da der MAPI-Standardclient zugewiesen wird.

 

Ein eingeschränkter Benutzer auf Windows XP, Windows Vista oder Windows 7 kann nicht auf SPAD zugreifen. Aus diesem Grund wird Entwicklern empfohlen, sich für das Element Set your default programs Systemsteuerung **(Standardprogramme** Systemsteuerung festlegen) zu registrieren, damit benutzerspezifische Anwendungsstandardeinstellungen von jedem Benutzer verwaltet werden können.

Die in SPAD getroffene Auswahl sollte sich nur auf die Einstellungen pro Computer auswirken.

Legen Sie den Registrierungswert wie folgt fest.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> **Die folgenden Informationen gelten nur für Windows XP.**
> 
> Wenn die Registrierung des Standardwerts auf Computerebene unter HKEY \_ LOCAL MACHINE wie oben gezeigt erfolgreich \_ ist, sollte die Anwendung den Wert löschen, der dem Standardeintrag unter dem folgenden Unterschlüssel zugewiesen ist:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> Wenn bei der Registrierung der Standardeinstellung auf Computerebene unter HKEY \_ LOCAL MACHINE wie oben gezeigt ein Fehler \_ auftritt, in der Regel, weil der Benutzer keine Schreibberechtigung für den Unterschlüssel hat, sollte die Anwendung den folgenden Wert festlegen:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> Dadurch wird der kanonische Name nur für den aktuellen Benutzer registriert, nicht für alle Benutzer.

 

Nach dem Aktualisieren der Registrierungsschlüssel sollte das Programm die [**WM \_ SETTINGCHANGE-Nachricht**](../winmsg/wm-settingchange.md) mit **wParam** = 0 und **lParam** übertragen, die auf die auf NULL endende Zeichenfolge "SoftwareClientTypeName" \\ \\ zeigt, um das Betriebssystem zu benachrichtigen, dass der Standardclient geändert wurde.

### <a name="mail-client-registration"></a>E-Mail-Clientregistrierung

Für einen E-Mail-Client muss das Programm über registrierte Einstellungen unter dem **\_ \_ HKEY CLASSES ROOT** \\ **mailto-Schlüssel** verfügen, um URLs zu bedienen, die das `mailto` Protokoll verwenden. Legen Sie Werte und Schlüssel fest, die diese Einstellungen unter dem folgenden Schlüssel spiegeln.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

Diese Registrierungshierarchie ersetzt die vorhandene `mailto` Registrierungshierarchie unter **HKEY \_ CLASSES \_ ROOT** \\ **mailto**. Die Hierarchie bleibt unverändert, nur der Speicherort wurde geändert. Das Format dieser Hierarchie ist auf MSDN unter [Asynchronous Pluggable Protocol Overviews and Tutorials (Übersichten zu asynchronen austauschbaren Protokollen und Tutorials)](/previous-versions//aa767913(v=vs.85))dokumentiert. In der Regel wird das `mailto` Protokoll bei einem Programm und nicht bei einem asynchronen Protokoll registriert. In diesem Fall gilt die Dokumentation zum Registrieren einer Anwendung bei einem [URI-Schema.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

Das folgende Beispiel zeigt den `mailto` Abschnitt der Registrierung für einen Handler, der bei einem Programm registriert `mailto` ist.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

Der Registrierungswert EditFlags ist in [Dateitypen](fa-file-types.md) im Abschnitt "Definieren von Dateitypattributen" dokumentiert.

## <a name="complete-sample-registrations"></a>Abschließen von Beispielregistrierungen

Die folgenden Beispiele zeigen die vollständigen Registrierungsanforderungen für die verschiedenen Clienttypen.

-   [Beispielbrowser](#a-sample-browser)
-   [Beispiel für einen E-Mail-Browser](#a-sample-mail-browser)
-   [Beispiel Media Player](#a-sample-media-player)
-   [Ein Instant Messenger-Beispielprogramm](#a-sample-instant-messenger-program)
-   [Ein virtueller Beispielcomputer für Java](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a>Ein Beispielbrowser

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a>Beispiel für einen E-Mail-Browser

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a>Beispiel Media Player

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a>Ein Instant Messenger-Beispielprogramm

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a>Beispiel für einen virtuellen Computer für Java

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

*Die hier dargestellten Beispielunternehmen, Organisationen, Produkte, Domänennamen, E-Mail-Adressen, Logos, Personen, Orte und Ereignisse sind fiktive Namen. Es ist keine Zuordnung zu einem echten Unternehmen, einer Organisation, einem Produkt, einem Domänennamen, einer E-Mail-Adresse, einem Logo, einer Person, einem Ort oder einem Ereignis beabsichtigt oder sollte abgeleitet werden.*

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Standardprogramme](default-programs.md)
</dt> <dt>

[Registrieren eines Internetbrowsers oder E-Mail-Clients mit dem Windows Startmenü](start-menu-reg.md)
</dt> <dt>

[Internet Explorer Layout der Clientregistrierung (siehe Abschnitt "Clientregistrierungsschlüsseldefinitionen")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))
</dt> <dt>

[Übersichten und Tutorials zu asynchronen austauschbaren Protokollen](/previous-versions//aa767913(v=vs.85))
</dt> <dt>

[Registrieren einer Anwendung bei einem URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))
</dt> </dl>

 

 
