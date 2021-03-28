---
description: 'In diesem Thema wird erläutert, wie Sie ein Programm in der Windows-Registrierung als einen der folgenden Client Typen registrieren: Browser, e-Mail, Medienwiedergabe, Instant Messaging oder virtueller Computer für Java.'
title: Registrieren von Programmen mit Client Typen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869627"
---
# <a name="registering-programs-with-client-types"></a>Registrieren von Programmen mit Client Typen

In diesem Thema wird erläutert, wie Sie ein Programm in der Windows-Registrierung als einen der folgenden Client Typen registrieren: Browser, e-Mail, Medienwiedergabe, Instant Messaging oder virtueller Computer für Java.

> [!Note]  
> Diese Informationen gelten für die folgenden Betriebssysteme:
> 
> -   Windows 2000 Service Pack 3 (SP3)
> -   Windows 2000 Service Pack 4 (SP4)
> -   Windows XP Service Pack 1 (SP1)
> -   Windows XP Service Pack 2 (SP2)
> -   Windows XP Service Pack 3 (SP3)
> -   Windows Server 2003
> -   Windows Vista
> -   Windows Vista Service Pack 1 (SP1)
> -   Windows 8

 

Das Thema enthält folgende Abschnitte:

-   [Allgemeine Registrierungs Elemente für alle Client Typen](#common-registration-elements-for-all-client-types)
    -   [Auswählen eines kanonischen Namens](#selecting-a-canonical-name)
    -   [Registrieren des anzeigen Amens eines Programms](#registering-a-programs-display-name)
    -   [Registrieren eines Programm Symbols](#registering-a-programs-icon)
    -   [Registrieren eines geöffneten Verbs](#registering-an-open-verb)
    -   [Installationsinformationen werden registriert](#registering-installation-information)
-   [Registrierungs Elemente für bestimmte Client Typen](#registration-elements-for-specific-client-types)
    -   [Start Menü Registrierung](#start-menu-registration)
    -   [Mail Client Registrierung](#mail-client-registration)
-   [Vervollständigen von Beispiel Registrierungen](#complete-sample-registrations)
    -   [Ein Beispiel Browser](#a-sample-browser)
    -   [Beispiel-e-Mail-Browser](#a-sample-mail-browser)
    -   [Ein Beispiel Media Player](#a-sample-media-player)
    -   [Ein Instant Messenger-Beispielprogramm](#a-sample-instant-messenger-program)
    -   [Ein Beispiel für einen virtuellen Computer für Java](#a-sample-virtual-machine-for-java)
-   [Zugehörige Themen](#related-topics)

Dieses Thema erweitert die vorhandene Dokumentation zum Registrieren eines Programms als bestimmten Clienttyp. Links zu dieser Dokumentation finden Sie im Abschnitt Verwandte Themen.

## <a name="common-registration-elements-for-all-client-types"></a>Allgemeine Registrierungs Elemente für alle Client Typen

Wenn Sie ein Programm als Clienttyp registrieren, sind die meisten Registrierungseinträge unabhängig vom Clienttyp identisch. Einige Registrierungseinträge sind jedoch spezifisch für den Clienttyp, und Sie sind im Abschnitt [Registrierungs Elemente für bestimmte Client Typen](#registration-elements-for-specific-client-types) vermerkt.

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Auswählen eines kanonischen Namens](#selecting-a-canonical-name)
-   [Registrieren des anzeigen Amens eines Programms](#registering-a-programs-display-name)
-   [Registrieren eines Programm Symbols](#registering-a-programs-icon)
-   [Registrieren eines geöffneten Verbs](#registering-an-open-verb)
-   [Installationsinformationen werden registriert](#registering-installation-information)

> [!Note]  
> Unterschlüssel Namen, die in diesem Thema kursiv angegeben sind, sind Platzhalter für benutzerdefinierte Unterschlüssel Namen oder einen Satz möglicher Werte. Vollständige Beispiele mit Beispiel Namen finden Sie im Abschnitt [vollständige Beispiel Registrierungen](#complete-sample-registrations) .

 

Alle Clienttyp-Registrierungsinformationen werden unter dem folgenden Unterschlüssel gespeichert:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

*Clienttypname* ist einer der folgenden Unterschlüssel Namen:

-   Startmenü Internet (für Browser)
-   E-Mail (für e-Mail)
-   Medien (für Medienwiedergabe)
-   IM (für Instant Messaging)
-   JavaVM (für virtuellen Computer für Java)

In diesem Thema finden Sie Verweise auf ein fiktives Computerprogramm mit dem Namen "Lit View" von Litware Inc. mit einer ausführbaren Datei namens Litview.exe. Dieses hypothetische Programm wird als Instant Messenger, Browser oder ein anderer Typ von Client Programm verwendet, der für die Veranschaulichung benötigt wird.

### <a name="selecting-a-canonical-name"></a>Auswählen eines kanonischen Namens

Der Anbieter muss einen *kanonischen Namen* für das Programm auswählen. Der kanonische Name wird dem Benutzer nie angezeigt und muss daher nicht lokalisiert werden. Der einzige Zweck besteht darin, eine eindeutige Zeichenfolge bereitzustellen, die zum Identifizieren des Programms verwendet werden kann. Er ist in der Regel mit dem englischen Namen des Programms identisch, aber dies ist lediglich eine Konvention.

Für andere Client Typen als Browser kann der kanonische Name eine beliebige Zeichenfolge sein. Wählen Sie einen eindeutigen Namen aus, der nicht wahrscheinlich von einem anderen Anbieter verwendet werden soll.

Bei Browser Clients muss der kanonische Name der Name – einschließlich der Erweiterung – der zugeordneten ausführbaren Datei sein. Beispiel: "Litview.exe".

Im folgenden finden Sie einige Beispiele für kanonische Namen.

-   Iexplore.exe (Browser)
-   Windows Mail (e-Mail)
-   Windows-Media Player (Medien)
-   Windows Messenger (Instant Messaging)

Registrieren Sie den kanonischen Namen, indem Sie wie hier gezeigt einen Unterschlüssel erstellen. Der Name des unter Schlüssels ist der kanonische Name. Alle Informationen im Zusammenhang mit der Registrierung dieses Programms sind unter diesem Unterschlüssel vorhanden.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a>Registrieren des anzeigen Amens eines Programms

Der nächste Schritt bei der Registrierung besteht darin, den anzeigen amen des Programms anzugeben. Sie wird als Wert unter dem kanonischen Namens Schlüssel angegeben, wie hier gezeigt. Beachten Sie, dass *CanonicalName* und *clienttykame* nicht die tatsächlichen Namen der Schlüssel sind, sondern nur Platzhalter für die tatsächlichen Namen, wie z. b. die *Beleuchtung*.

> [!Note]  
> Ab Windows 8 sollte der Name, der für die Registrierung für [Set Program Access und Computer Standards (SPAD)](cpl-setprogramaccess.md) und für [Standardprogramme](default-programs.md) verwendet wird, identisch sein, damit SPAD-Änderungen Standardprogramm Registrierungen auslöst.

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

Der **LocalizedString** -Wert ist eine reg \_ SZ-Zeichenfolge und besteht aus einem "at"-Zeichen (@), dem vollständigen Pfad zu einer DLL-oder exe-Datei, einem Komma, einem Minuszeichen und einer ganzen Dezimalzahl. Die ganzzahlige Ganzzahl ist die ID einer Zeichen folgen Ressource –, die in der DLL-oder exe-Datei enthalten ist –, deren Wert dem Benutzer als Name dieses Clients angezeigt werden soll. Beachten Sie, dass der Dateipfad keine Anführungszeichen erfordert, auch wenn er Leerzeichen enthält.

Wenn Sie die Zeichenfolge für den anzeigen Amen auf diese Weise registrieren, kann dieselbe Registrierung für mehrere Sprachen verwendet werden. Jede sprach Installation bietet eine andere Ressourcen Datei mit dem anzeigen Amen, der in derselben Ressourcen-ID gespeichert ist.

Im folgenden Beispiel wird die Registrierung für ein fiktives beleuchtetes Ansichts-Instant Messaging-Programm gezeigt. Da es sich um ein Instant Messaging-Programm handelt, wird der Unterschlüssel " *CanonicalName* " (in diesem Fall " *lit View*") unter dem **im** -Unterschlüssel gespeichert.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Beachten Sie die Verwendung des (Standard-) Eintrags als sekundäre Deklaration des Client anzeigen Amens. Wenn die **LocalizedString** nicht vorhanden ist, wird stattdessen der (standardmäßige) Wert verwendet. Dies funktioniert bei allen Client Typen (Internet Browser, e-Mail-Browser, Instant Messenger und Media Players). Aus Gründen der Abwärtskompatibilität mit dem [Internet Explorer-Client Registrierungs Layout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))sollte der (Standardwert)-Wert des unter Schlüssels " *CanonicalName* " von e-Mail-Programmen in der aktuell installierten Sprache auf den anzeigen amen des Clients festgelegt werden.

### <a name="registering-a-programs-icon"></a>Registrieren eines Programm Symbols

> [!Note]  
> Dieser Abschnitt gilt nicht für Windows 2000.

 

Standardmäßig enthält der obere Abschnitt des **Start** Menüs von Windows XP und Windows Vista **Internet** -und **e-Mail-** Symbole. Diese Symbole sind in Windows 7 und höher nicht vorhanden. Wenn für Browser-und e-Mail-Clients ein Programm als Standardwert für den Clienttyp zugewiesen ist, wird das registrierte Symbol dieses Programms für diese Einträge im **Startmenü** angezeigt.

Das Registrieren eines Programm Symbols ist für Browser-und e-Mail-Clients obligatorisch. Das Registrieren eines Symbols für die Medienwiedergabe, das Instant Messaging oder den virtuellen Computer für Java-Client Typen ist optional, und registrierte Symbole für diese Client Typen werden zurzeit nicht von Windows verwendet und nicht im oberen Abschnitt der **Start** Menüs von Windows XP oder Windows Vista angezeigt.

Zum Registrieren eines Symbols für ein Client Programm fügen Sie einen **DefaultIcon** -Unterschlüssel mit einem Standardwert hinzu, wie hier gezeigt.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

Der Wert **FilePath** ist der vollständige Pfad zu der Datei, die das Symbol enthält. Für diesen Pfad sind keine Anführungszeichen erforderlich, auch wenn er Leerzeichen enthält.

Der **IconIndex** -Wert wird wie folgt interpretiert:

-   Wenn **IconIndex** eine positive Zahl ist, wird die Zahl als Index des *NULL basierten* Arrays von Symbolen verwendet, das in der Datei gespeichert ist. Wenn **IconIndex** z. b. 1 ist, wird das zweite Symbol aus der Datei geladen.
-   Wenn **IconIndex** eine negative Zahl ist, wird der absolute Wert von **IconIndex** als Ressourcen Bezeichner (anstelle des Indexes) für das Symbol verwendet. Wenn **IconIndex** beispielsweise den Wert-3 hat, wird das Symbol, dessen Ressourcen Bezeichner den Wert 3 hat, aus der Datei geladen.

Das folgende Beispiel zeigt die Registrierung eines hypothetischen beleuchteten Ansichts Browsers. Das zweite Symbol, das in der Litview.exe-Datei gespeichert wird, wird als Standard verwendet.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a>Registrieren eines geöffneten Verbs

> [!Note]  
> Dieser Abschnitt gilt nicht für Windows 2000. Der folgende Schritt ist nur für Browser-und e-Mail-Clients erforderlich.

 

Angenommen, ein Benutzer hat Ihr Programm als standardmäßiges Internet oder e-Mail-Programm ausgewählt. Dieser Benutzer klickt im **Startmenü** von Windows XP oder Windows Vista auf das **Internet** oder das **e-Mail-** Symbol, um das Programm zu öffnen. An diesem Punkt wird die Befehlszeile, die wie hier gezeigt registriert ist, ausgeführt.

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

Die Befehlszeile muss einen voll qualifizierten absoluten Pfad zur Datei angeben, gefolgt von optionalen Befehlszeilenoptionen. Wenn der Eintragstyp reg \_ Expand- \_ SZ ist, können Umgebungsvariablen im Pfad verwendet werden. Verwenden Sie Anführungszeichen entsprechend, um sicherzustellen, dass Leerzeichen in der Befehlszeile nicht falsch interpretiert werden. Die Befehlszeile sollte das Programm mit den entsprechenden Standardeinstellungen ausführen. Browser werden im Allgemeinen standardmäßig auf die Startseite des Benutzers eingestellt. E-Mail-Programme öffnen den **Posteingangs** des Benutzers.

Das folgende Beispiel zeigt die Registrierung eines `open` Verbs für einen hypothetischen beleuchteten Ansichts Browser. Es gibt keine Befehlszeilenoptionen an.

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

Beachten Sie, dass in diesem Wert Anführungszeichen um den Pfad platziert werden, da Sie eingebettete Leerzeichen enthält. Wenn Sie diese Anführungszeichen weglassen, kann dies dazu führen, dass die Befehlszeile falsch interpretiert wird.

### <a name="registering-installation-information"></a>Installationsinformationen werden registriert

> [!Note]  
> Dieser Abschnitt gilt nicht für Windows Server 2003.

 

-   [Der Befehl "neu installieren"](#the-reinstall-command)
-   [Befehl zum Ausblenden von Symbolen](#the-hide-icons-command)
-   [Der Befehl "Symbole anzeigen"](#the-show-icons-command)
-   [Gruppenprogramm Konfiguration](#group-program-configuration)
-   [Beispiel für eine Browser Registrierung](#browser-registration-example)

Die Funktion, mit der der Benutzer Computer spezifische Standardprogramme auswählt, wird benannt und darauf zugegriffen, wie in der folgenden Tabelle dargestellt. (In Windows Vista wurde ein neues Feature eingeführt, das **Standardprogramm wird festgelegt**, mit dem ein Benutzer benutzerspezifische Standardeinstellungen festlegen kann.)



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Betriebssystem</th>
<th>Titel</th>
<th>Zugriffs Speicherort</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows 7</td>
<td>Festlegen des Programm Zugriffs und der Standardeinstellungen des Computers</td>
<td><ul>
<li><strong>Start</strong> Menü ( <strong>Standardprogramme</strong> -Option)</li>
<li><strong>Standardprogramme</strong> System Steuerungselement</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista</td>
<td>Festlegen des Programm Zugriffs und der Standardeinstellungen des Computers</td>
<td><ul>
<li><strong>Start</strong> Menü ( <strong>Standardprogramme</strong> -Option)</li>
<li><strong>Standardprogramme</strong> System Steuerungselement</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows XP SP2</td>
<td>Festlegen des Programm Zugriffs und der Standardeinstellungen</td>
<td><ul>
<li><strong>Startmenü</strong></li>
<li>Software <strong>Hinzufügen oder entfernen</strong> System Steuerungselement</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows XP SP1</td>
<td>Konfigurieren von Programmen</td>
<td><ul>
<li>Software <strong>Hinzufügen oder entfernen</strong> System Steuerungselement</li>
</ul></td>
</tr>
</tbody>
</table>



 

Der Einfachheit halber wird in diesem Thema der Windows 7-Titel des Features verwendet. Alle Versionen der Funktion werden als SPAD bezeichnet.

> [!Note]  
> Wenn Sie Windows 2000 oder Windows XP ausführen, muss mindestens Windows 2000 SP3 oder Windows XP SP1 installiert sein, damit die Seite " **Programm Zugriff und Standardeinstellungen festlegen** " angezeigt wird. In Windows Vista und höher sind für den Zugriff auf die Seite " **Programm Zugriff und Computer Standards festlegen** " Administrator Rechte erforderlich. Aus diesem Grund wird Entwicklern empfohlen, sich für das System Steuerungselement " [Standardprogramme festlegen](default-programs.md) " zu registrieren, damit jeder Benutzer Anwendungs Standardwerte verwalten kann.

 

Die folgende Registrierungs Struktur zeigt die Vielzahl der Informationen, die im **installinfo** -Schlüssel des Programms registriert werden müssen, damit das Programm auf der Seite **Programm Zugriff und Computer Standards festlegen** als Option für den Clienttyp angezeigt wird. Diese Werte werden in den folgenden Abschnitten ausführlich erläutert.

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

Die Befehlszeile muss einen voll qualifizierten absoluten Pfad zur Datei angeben, gefolgt von optionalen Befehlszeilenoptionen. Verwenden Sie Anführungszeichen entsprechend, um sicherzustellen, dass Leerzeichen in der Befehlszeile nicht falsch interpretiert werden.

### <a name="the-reinstall-command"></a>Der Befehl "neu installieren"

Die im reinstallcommand-Wert deklarierte Befehlszeile für die erneute Installation wird ausgeführt, wenn der Benutzer die Seite " **Programm Zugriff und Computer Standards festlegen** " verwendet, um das Programm als Standardwert für den Clienttyp auszuwählen. In Windows Vista und höher ist für den Zugriff auf diese Seite eine Administrator Berechtigungsstufe erforderlich. Wenn Sie in Windows 8 Ihre Anwendung mit dem gleichen Namen sowohl für den **Programm Zugriffs Satz als** auch für **Standardprogramme** registriert haben, werden die in **Standardprogrammen** für diese Anwendung angegebenen Standardwerte auf den aktuellen Benutzer angewendet, und der Befehl "neu installieren" wird ausgeführt.

Das Programm, das von der neu [Installationsbefehlszeile](fa-intro.md) gestartet wird, muss die Anwendung mit dem kompletten Satz von Datei-und [Protokoll](/previous-versions//aa767743(v=vs.85)) Typen verknüpfen, die die Anwendung verarbeiten kann. Alle Anwendungen müssen die Handlerfunktion im Befehl Neuinstallation einrichten. Anwendungen können den Befehl "neu installieren" verwenden, um die Funktion zu registrieren und optional den Standardstatus festzulegen. Wenn eine Anwendung sowohl den Funktions-als auch den standardhandlerstatus im installieren Sie-Befehl implementiert, sollte Sie auch alle gewünschten sichtbaren Verknüpfungen oder Verknüpfungen wiederherstellen. Die sichtbaren Einstiegspunkte, die von den meisten Anwendungen ausgewählt werden, werden im [Befehl Symbole ausblenden](#the-hide-icons-command)aufgeführt.

> [!Note]  
> Es wird dringend empfohlen, dass Anwendungen die Verarbeitungs Funktion im Befehl "neu installieren" implementieren.

 

Nach Abschluss des Neuinstallations Vorgangs sollte das von der Befehlszeile für die erneute Installation gestartete Programm beendet werden. Das entsprechende Programm sollte nicht gestartet werden. Es sollten nur Standardwerte registriert werden. Beispielsweise sollte der Befehl "neu installieren" für einen Browser nicht die Startseite des Benutzers öffnen.

> [!Note]  
> Bei Browser-und e-Mail-Clients unter Windows XP und Windows Vista sollte sich eine Registrierung für das entsprechende Symbol am oberen Rand des Start Menüs durchführen. Weitere Informationen finden Sie unter [Start Menü Registrierung](#start-menu-registration) .

 

### <a name="the-hide-icons-command"></a>Befehl zum Ausblenden von Symbolen

Die Befehlszeile, die im hideidescommand-Wert deklariert wird, wird ausgeführt, wenn der Benutzer das **Kontrollkästchen Zugriff auf dieses Programm aktivieren** auf der Seite **Programm Zugriff und Computer Standards festlegen** deaktiviert. Diese Befehlszeile muss alle Zugriffspunkte Ihres Programms ausblenden, die auf der Benutzeroberfläche sichtbar sind. Die spezifischen Richtlinien sind das Entfernen von Verknüpfungen und Symbolen aus den folgenden Speicherorten:

-   Desktop Symbole
-   Startmenü Links, einschließlich der **Start** Gruppe
-   Links für die Schnellstartleiste
-   Benachrichtigungsbereich
-   Kontextmenüs
-   Ordnertaskband

Diese Befehlszeile muss auch automatische Aufrufe des Programms verhindern, z. b. die im Registrierungsschlüssel **Ausführen** angegebenen. Es wird empfohlen, diese Richtlinien in der Anwendung zum Ausblenden des Zugriffs Rückrufs zu implementieren.

Wenn Symbole ausgeblendet werden, müssen Sie die Registrierung (Anwendungsfunktion) von Dateitypen nicht aufgeben. Außerdem müssen Sie den Standardstatus der Anwendung für Datei-und Protokolltypen nicht aufgeben. Dies kann zu einer ungültigen Benutzeroberfläche führen, wenn diese Typen in der Benutzeroberfläche gefunden werden.

Nach dem erfolgreichen Ausblenden von Symbolen müssen Sie den iconsvisible-Registrierungs Wert wie folgt auf 0 aktualisieren:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

Der iconsvisible-Eintrag ist vom Typ " **reg \_ DWORD**".

### <a name="an-alternate-hide-icons-method-in-spad"></a>Eine alternative Methode zum Ausblenden von Symbolen in SPAD

Bei einigen Legacy Anwendungen ist eine vollständige Implementierung des Ausblenden des Zugriffs möglicherweise nicht praktikabel. Eine alternative Methode, die denselben Effekt erzielt, ist die Deinstallation der Anwendung. Der nachfolgende Abschnitt zeigt Beispiel Verhalten und Beispielcode zum Implementieren dieser Alternativen. Im Allgemeinen sollten unabhängige Softwarehersteller (ISVs) diese Alternative vermeiden, da Sie Folgendes bietet:

-   Deinstallieren Sie die Anwendung vollständig aus dem System.
-   Entfernt zuvor ausgewählte Standardwerte.
-   Lassen Sie die Option keine Benutzeroberfläche zur erneuten Installation der Anwendung.
-   Aktivieren Sie das Feature "Zugriff aktivieren" nicht mehr, da die Anwendung durch eine Deinstallation vollständig aus SPAD entfernt wird.

Die empfohlene Benutzer Darstellung lautet wie folgt:

-   Wenn der Benutzer das Kontrollkästchen **Zugriff auf dieses Programm aktivieren** in SPAD deaktivieren, wird die folgende Benutzeroberfläche angezeigt.

    ![Dialogfeld zum Ausblenden des Programm Zugriffs](images/hideaccessvista.png)

-   Wenn der Benutzer **OK** auswählt, wird das System Steuerungselement **Programme und Funktionen** gestartet, um dem Benutzer die Deinstallation der Anwendung zu ermöglichen.
-   In diesem Dialogfeld sollten Windows XP-Benutzer angezeigt werden.

    ![entsprechendes Windows XP-Dialogfeld](images/hideaccessxp.png)

-   Wenn der Windows XP-Benutzer **OK** auswählt, wird **das System Steuerungs** Element Software gestartet, um dem Benutzer die Deinstallation der Anwendung zu ermöglichen.

Der folgende Code stellt eine wiederverwendbare Implementierung für die Funktion "Zugriff ausblenden" bereit, wie oben beschrieben. Sie kann unter Windows XP, Windows Vista und Windows 7 verwendet werden.


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



### <a name="the-show-icons-command"></a>Der Befehl "Symbole anzeigen"

Die Befehlszeile, die im Eintrag showiconfiguration Command deklariert ist, wird ausgeführt, wenn der Benutzer das Kontrollkästchen **Zugriff auf dieses Programm aktivieren** auf der Seite **Programm Zugriff und Computer Standards festlegen** prüft. Mit dieser Befehlszeile können Sie die Zugriffspunkte Ihres Programms, einschließlich der im **Startmenü** , auf dem Desktop und in der **Start** Gruppe, sowie der normalen automatischen Aufrufe, wie z. b. der im Registrierungsschlüssel **Ausführen** angegeben, wiederherstellen. Die sichtbaren Zugriffspunkte, die für die meisten Anwendungen von Interesse sind, werden im [Befehl Symbole ausblenden](#the-hide-icons-command)aufgeführt. Die Anwendung sollte keine benutzerspezifischen Standardeinstellungen ändern. Diese Änderung sollte vom Benutzer über **Standardprogramme** durchgeführt werden.

Nachdem Sie Ihre Symbole erfolgreich angezeigt haben, müssen Sie den iconsvisible-Registrierungs Wert auf 1 aktualisieren, wie im folgenden gezeigt:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

Beachten Sie Folgendes: Wenn Sie den Eintrag hideiencommand verwendet haben, um eine Deinstallation der Anwendung einzugeben, wird der Eintrag showiencommand nicht verwendet. Er sollte bei der Deinstallation aus der Registrierung mit den restlichen Informationen der Anwendung entfernt werden.

### <a name="group-program-configuration"></a>Gruppenprogramm Konfiguration

> [!Note]  
> Dieser Abschnitt gilt nicht für Windows 2000.

 

Im Rahmen der System Vorbereitung kann ein OEM eine Konfiguration einrichten, die Zugriffspunkte für den Microsoft-Browser, die e-Mail, die Medienwiedergabe, das Instant Messaging oder den virtuellen Computer für Java-Client Programme verbirgt und seine eigenen Standardprogramme angibt. OEMs können es Benutzern ermöglichen, ihre Computer zu einem beliebigen Zeitpunkt auf diese Standardkonfiguration zurückzusetzen, indem Sie die folgenden Registrierungs Werte festlegen.

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

Wenn diese Schlüssel festgelegt sind, können Benutzer die OEM-Konfiguration wiederherstellen, indem Sie die Option **Computer Hersteller** auf der Seite **Programm Zugriff und Computer Standards festlegen** auswählen. Wenn diese Schlüssel nicht festgelegt sind, wird die Option **Computer Hersteller** nicht angezeigt.

Der **oemshowicons** -Eintrag, falls vorhanden, legt den Symbol Anzeige Status für den angegebenen Client fest, der angewendet wird, wenn der Benutzer den **Computer Hersteller** auswählt. Der Wert 1 bewirkt, dass Symbole angezeigt werden, und der Wert 0 bewirkt, dass Symbole nicht angezeigt werden. Wenn **oemshowicons** nicht vorhanden ist, hat die Auswahl von **Computer Hersteller** keine Auswirkung auf die Symbol Anzeige Einstellung. **Oemshowicons** ist vom Typ " **reg \_ DWORD**".

Der **oemdefault** -Eintrag, falls vorhanden und auf 1 festgelegt, legt die OEM-Voreinstellung für den Standard Client des festgelegten Typs fest. Nur ein Client eines bestimmten Typs kann als OEM-Standard gekennzeichnet werden. Wenn mehr als die Registrierung eines Clients den **oemdefault** -Eintrag enthält, werden alle ignoriert, und der aktuelle Client wird weiterhin als Standard Client verwendet. Wenn der **oemdefault** -Eintrag nicht vorhanden oder vorhanden und auf 0 festgelegt ist, wird der jeweilige Client nicht als Standard Client verwendet, wenn der Benutzer den **Computer Hersteller** auswählt. **Oemdefault** ist vom Typ " **reg \_ DWORD**".

Zusätzlich zur Option, ihre Computer auf die vom OEM festgelegte Standardkonfiguration zurückzusetzen, haben die Benutzer drei weitere Konfigurationsoptionen:

-   Legen Sie Ihren Computer auf eine Microsoft Windows-Konfiguration fest. In diesem Fall wird auf der Seite **Programm Zugriff und Computer Standards festlegen** der Zugriff auf alle Microsoft-und nicht-Microsoft-Software auf dem Computer ermöglicht, der in den relevanten Produktkategorien registriert ist. Microsoft Windows-Programme werden als Standardoption für jede Kategorie ausgewählt.
-   Legen Sie Ihren Computer auf eine nicht-Microsoft-Konfiguration fest. Diese Konfiguration verbirgt Zugriffspunkte (z. b. das **Startmenü** ) für Windows Internet Explorer, Windows Media Player, Windows Messenger und Microsoft Outlook Express. Er ermöglicht den Zugriff auf die Software, die nicht von Microsoft ist, auf dem Computer in diesen Kategorien. Wenn außerdem ein nicht-Microsoft-Programm in einer Kategorie verfügbar ist, wird es als Standardwert für diese Kategorie festgelegt. Wenn in einer Kategorie mehr als ein nicht-Microsoft-Programm verfügbar ist, wird der Benutzer aufgefordert zu entscheiden, welches nicht-Microsoft-Programm als Standard verwendet werden soll.
-   Richten Sie eine benutzerdefinierte Konfiguration ein. Benutzer nehmen Ihre eigene Auswahl vor, um den Zugriff zu aktivieren oder zu entfernen, und kombinieren Microsoft-und nicht-Microsoft-Programme, wenn Sie passen. Benutzer legen Standardoptionen auf kategoriebasis fest.

Benutzer können jede dieser Optionen jederzeit ändern.

### <a name="browser-registration-example"></a>Beispiel für eine Browser Registrierung

Das folgende Beispiel zeigt die vollständige **installinfo** -Registrierung für einen fiktiven beleuchteten Ansichts Browser. In diesem Fall ermöglichen die Befehls Zeilenschalter, dass die Litview.exe Datei alle Aktionen ausführt, die für jeden Wert erforderlich sind.

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

Beachten Sie, dass die Pfade in Anführungszeichen eingefügt werden, da Sie eingebettete Leerzeichen enthalten.

## <a name="registration-elements-for-specific-client-types"></a>Registrierungs Elemente für bestimmte Client Typen

Die folgenden Informationen finden Sie auch in den Ressourcen, die im Abschnitt Verwandte Themen am Ende dieses Themas aufgelistet sind.

-   [Start Menü Registrierung](#start-menu-registration)
-   [Mail Client Registrierung](#mail-client-registration)

### <a name="start-menu-registration"></a>Start Menü Registrierung

Unter Windows XP haben Anwendungen normalerweise standardmäßig standardmäßig auf einem Computer weiten (**HKEY \_ local \_ Machine**) und nicht in einem Benutzerbereich (**Aktueller HKEY- \_ \_ Benutzer**) registriert. Mit der Einführung der Benutzerkontensteuerung (User Account Control, UAC) in Windows Vista müssen Anwendungen, die die **Internet** **-und e-Mail-** Slots im **Startmenü** beanspruchen, den Befehl "neu installieren" im richtigen Ausführungs Kontext implementieren.

> [!Note]  
> Der Link für den Startmenü **-e-Mail-** Link wurde ab Windows 7 entfernt. Die in diesem Abschnitt erörterte Registrierung sollte jedoch weiterhin ausgeführt werden, da Sie den standardmäßigen MAPI-Client zuweist.

 

Ein eingeschränkter Benutzer unter Windows XP, Windows Vista oder Windows 7 kann nicht auf SPAD zugreifen. Aus diesem Grund wird Entwicklern empfohlen, sich für das System Steuerungselement " **Standardprogramme festlegen** " zu registrieren, sodass jeder Benutzer Standard Anwendungs Standardwerte verwalten kann.

Die in SPAD vorgenommene Auswahl wirkt sich nur auf die computerspezifischen Einstellungen aus.

Legen Sie den Registrierungs Wert wie folgt fest.

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
> Wenn die Registrierung des Standardwerts auf Computer Ebene unter HKEY \_ local \_ Machine, wie oben gezeigt, erfolgreich ist, sollte die Anwendung den Wert löschen, der dem Standardeintrag unter dem folgenden Unterschlüssel zugewiesen ist:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> Wenn die Registrierung des Standardwerts auf Computer Ebene unter HKEY \_ local \_ Machine, wie oben gezeigt, fehlschlägt, in der Regel, weil der Benutzer nicht über Schreibberechtigungen für den Unterschlüssel verfügt, sollte die Anwendung den folgenden Wert festlegen:
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

 

Nach dem Aktualisieren der Registrierungsschlüssel sollte das Programm die [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht mit **wParam** = 0 und **LPARAM** übertragen, um das \\ \\ Betriebssystem zu benachrichtigen, dass sich der Standard Client geändert hat.

### <a name="mail-client-registration"></a>Mail Client Registrierung

Bei einem e-Mail-Client muss das Programm unter dem Stamm-mailto-Schlüssel der **HKEY- \_ Klassen \_** über registrierte Einstellungen verfügen, um \\  URLs zu verwenden, die das `mailto` Protokoll verwenden. Legen Sie Werte und Schlüssel fest, die diese Einstellungen unter dem folgenden Schlüssel widerspiegeln.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

Diese Registrierungs Hierarchie ersetzt die vorhandene `mailto` Registrierungs Hierarchie, die unter **HKEY \_ Classes \_ root** \\ **mailto** gefunden wurde. Die Hierarchie bleibt unverändert, nur der Speicherort wurde geändert. Das Format dieser Hierarchie ist auf MSDN unter [asynchroner austauschbarer Protokoll Übersichten und Tutorials](/previous-versions//aa767913(v=vs.85))dokumentiert. In der Regel `mailto` wird das Protokoll für ein Programm und nicht für ein asynchrones Protokoll registriert. in diesem Fall gilt die Dokumentation zum [Registrieren einer Anwendung in einem URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) .

Das folgende Beispiel zeigt den `mailto` Abschnitt der Registrierung für einen `mailto` Handler, der für ein Programm registriert ist.

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

Der EditFlags-Registrierungs Wert ist in den [Dateitypen](fa-file-types.md) im Abschnitt "Definieren von Dateityp Attributen" dokumentiert.

## <a name="complete-sample-registrations"></a>Vervollständigen von Beispiel Registrierungen

In den folgenden Beispielen werden die kompletten Registrierungsanforderungen für die verschiedenen Client Typen veranschaulicht.

-   [Ein Beispiel Browser](#a-sample-browser)
-   [Beispiel-e-Mail-Browser](#a-sample-mail-browser)
-   [Ein Beispiel Media Player](#a-sample-media-player)
-   [Ein Instant Messenger-Beispielprogramm](#a-sample-instant-messenger-program)
-   [Ein Beispiel für einen virtuellen Computer für Java](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a>Ein Beispiel Browser

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

### <a name="a-sample-mail-browser"></a>Beispiel-e-Mail-Browser

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

### <a name="a-sample-media-player"></a>Ein Beispiel Media Player

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

### <a name="a-sample-virtual-machine-for-java"></a>Ein Beispiel für einen virtuellen Computer für Java

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

*Die hier dargestellten Beispiel Unternehmen, Organisationen, Produkte, Domänen Namen, e-Mail-Adressen, Logos, Personen, Orte und Ereignisse sind frei erfunden. Keine Zuordnung zu echten Unternehmen, Organisationen, Produkten, Domänen Namen, e-Mail-Adressen, Logos, Personen, stellen oder Ereignissen ist beabsichtigt oder sollte abgeleitet werden.*

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Standardprogramme](default-programs.md)
</dt> <dt>

[Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü](start-menu-reg.md)
</dt> <dt>

[Internet Explorer-Client Registrierungs Layout (siehe Abschnitt "Definitionen von Client Registrierungs Schlüsseln")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))
</dt> <dt>

[Asynchrone austauschbare Protokoll Übersichten und Tutorials](/previous-versions//aa767913(v=vs.85))
</dt> <dt>

[Registrieren einer Anwendung in einem URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))
</dt> </dl>

 

 
