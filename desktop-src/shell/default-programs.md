---
description: Verwenden Sie Standardprogramme, um die Standardbenutzerfreundlichkeit festzulegen.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Standardprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1cd54afe23291c191fdd045ca3cb42b68361aa8f7f3d8ef431042cfe9f5c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861357"
---
# <a name="default-programs"></a>Standardprogramme

Verwenden Sie **Standardprogramme,** um die Standardbenutzerfreundlichkeit festzulegen. Benutzer können über Systemsteuerung oder direkt über das **Startmenü** auf **Standardprogramme** zugreifen. [Set Program Access and Computer Defaults (SPAD)-Tool,](cpl-setprogramaccess.md) die primäre Standardfunktion für Benutzer in Windows XP, ist jetzt ein Teil von **Standardprogrammen.**

> [!IMPORTANT]
> Dieses Thema gilt nicht für Windows 10. Die Funktionsweise von Standarddateizuordnungen hat sich in Windows 10 geändert. Weitere Informationen finden Sie im Abschnitt Änderungen an der Verarbeitung von **Standard-Apps durch Windows 10** in [diesem Beitrag.](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)

 

Wenn ein Benutzer die Programmstandardeinstellungen mit **Standardprogrammen** festlegt, gilt die Standardeinstellung nur für diesen Benutzer und nicht für andere Benutzer, die möglicherweise denselben Computer verwenden. **Standardprogramme** bieten eine Reihe von APIs (veraltet in Windows 8), mit denen unabhängige Softwarehersteller (ISVs) ihre Programme oder Anwendungen in das Standardsystem einschließen können. Der API-Satz hilft ISVs auch dabei, ihren Status als Standardwerte besser zu verwalten.

Dieses Thema ist wie folgt organisiert:

-   [Einführung in Standardprogramme und den zugehörigen API-Satz](#introduction-to-default-programs-and-its-related-api-set)
-   [Registrieren einer Anwendung für die Verwendung mit Standardprogrammen](#registering-an-application-for-use-with-default-programs)
    -   [ProgIDs](#progids)
    -   [Registrierungsunterschlüssel und Wertbeschreibungen](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [Beispiel für vollständige Registrierung](#full-registration-example)
-   [Wird zum Standardbrowser](#becoming-the-default-browser)
-   [Benutzeroberfläche für Standardprogramme](#default-programs-ui)
-   [Bewährte Methoden für die Verwendung von Standardprogrammen](#best-practices-for-using-default-programs)
    -   [Während der Installation](#during-installation)
    -   [Nach der Installation](#after-installation)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>Einführung in Standardprogramme und den zugehörigen API-Satz

**Standardprogramme** sind in erster Linie für Anwendungen konzipiert, die Standarddateitypen wie .mp3 oder .jpg Dateien oder Standardprotokolle wie HTTP oder mailto verwenden. Anwendungen, die ihre eigenen proprietären Protokolle und Dateizuordnungen verwenden, verwenden in der Regel nicht die **Standardprogrammfunktion.**

Nachdem Sie eine Anwendung für die **Standardprogrammfunktionalität** registriert haben, sind die folgenden Optionen und Funktionen mithilfe des API-Satzes verfügbar:

-   Stellen Sie alle registrierten Standardwerte für eine Anwendung wieder her. Für Windows 8 veraltet.
-   Stellen Sie einen einzelnen registrierten Standardwert für eine Anwendung wieder her. Für Windows 8 veraltet.
-   Fragen Sie den Besitzer eines bestimmten Standardwerts in einem einzelnen Aufruf ab, anstatt die Registrierung zu durchsuchen. Sie können den Standardwert einer Dateizuordnung, eines Protokolls oder eines kanonischen Verbs im **Startmenü** abfragen.
-   Starten Sie eine Benutzeroberfläche für eine bestimmte Anwendung, auf der ein Benutzer einzelne Standardwerte festlegen kann.
-   Entfernen Sie alle Benutzerzuordnungen.

**Standardprogramme** bietet auch eine Benutzeroberfläche, mit der Sie eine Anwendung registrieren können, um dem Benutzer zusätzliche Informationen bereitzustellen. Beispielsweise kann eine digital signierte Anwendung eine URL zur Startseite des Herstellers enthalten.

Die Verwendung des zugeordneten API-Satzes kann dazu beitragen, dass eine Anwendung ordnungsgemäß unter dem in Windows Vista eingeführten Feature zur Benutzerkontensteuerung (User Account Control, UAC) funktioniert. Unter UAC wird ein Administrator dem System als Standardbenutzer angezeigt, sodass dieser Administrator in der Regel nicht in die **HKEY \_ LOCAL \_ MACHINE-Unterstruktur** schreiben kann. Diese Einschränkung ist ein Sicherheitsfeature, das verhindert, dass ein Prozess ohne das Wissen des Administrators als Administrator fungiert.

Die Installation eines Programms durch einen Benutzer erfolgt in der Regel als Prozess mit erhöhten Rechten. Versuche einer Anwendung, das Standardzuordnungsverhalten nach der Installation auf Computerebene zu ändern, sind jedoch nicht erfolgreich. Stattdessen müssen Standardwerte auf Benutzerebene registriert werden, wodurch verhindert wird, dass mehrere Benutzer die Standardwerte gegenseitig überschreiben.

Die hierarchische Registrierungsstruktur für Datei- und Protokollzuordnungen hat Vorrang vor Den Standardwerten pro Benutzer und den Standardwerten auf Computerebene. Einige Anwendungen enthalten Punkte in ihrem Code, die ihre Rechte vorübergehend erhöhen, wenn sie die in **HKEY \_ LOCAL \_ MACHINE** registrierten Standardwerte beanspruchen. Bei diesen Anwendungen treten möglicherweise unerwartete Ergebnisse auf, wenn eine andere Anwendung bereits als Standard pro Benutzer registriert ist. Die Verwendung von **Standardprogrammen** verhindert diese Mehrdeutigkeit und garantiert erwartete Ergebnisse auf Benutzerebene.

## <a name="registering-an-application-for-use-with-default-programs"></a>Registrieren einer Anwendung für die Verwendung mit Standardprogrammen

In diesem Abschnitt werden die Registrierungsunterschlüssel und -werte angezeigt, die zum Registrieren einer Anwendung bei **Standardprogrammen** erforderlich sind. Es enthält ein vollständiges Beispiel.

Dieser Abschnitt enthält die folgenden Themen:

-   [ProgIDs](#progids)
-   [Registrierungsunterschlüssel und Wertbeschreibungen](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [Beispiel für vollständige Registrierung](#full-registration-example)

**Standardprogramme** erfordern, dass jede Anwendung explizit die Dateizuordnungen, MIME-Zuordnungen und Protokolle registriert, für die die Anwendung als möglicher Standard aufgeführt werden soll. Sie registrieren die Zuordnungen mithilfe der folgenden Registrierungselemente, die weiter unten in diesem Thema unter [Registrierungsunterschlüssel und Wertbeschreibungen](#registration-subkey-and-value-descriptions)ausführlich erläutert werden:

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

Das folgende Beispiel zeigt die Registrierungseinträge für einen fiktiven Contoso-Browser namens WebBrowser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a>ProgIDs

Eine Anwendung muss eine bestimmte [ProgID](fa-progids.md)bereitstellen. Stellen Sie sicher, dass Sie alle Informationen einschließen, die normalerweise in den generischen Standardunterschlüssel für die Erweiterung geschrieben werden. Der fiktive Litware Media Player stellt beispielsweise die anwendungsspezifischen **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Classes** \\ **LitwarePlayer11.AssocFile.MP3** Unterschlüssel bereit. Dieser Unterschlüssel enthält alle Informationen im generischen Standardunterschlüssel **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Classes** \\ **.mp3** sowie alle zusätzlichen Informationen, die die Anwendung registrieren soll. Dadurch wird sichergestellt, dass die Informationen des Litware-Players intakt sind und nicht von einer anderen Anwendung überschrieben wurden, wenn der Benutzer die .mp3 Zuordnung zum Litware-Player wiederherstellt. (Das Überschreiben kann auftreten, wenn der Standardunterschlüssel die einzige Quelle dieser Informationen ist.)

Wenn Sie eine ProgID einer Dateinamenerweiterung oder einem Dateierweiterung oder Protokoll zuordnen, kann eine Anwendung 1:1 oder 1:n zuordnen. Im Contoso-Beispiel verweist ContosoHTML auf eine einzelne ProgID, die shellexecute-Informationen für die Erweiterungen .htm, .html, .shtml, .xht und .xhtml bereitstellt. Da für jedes Protokoll eine andere ProgID vorhanden ist, aktivieren Sie bei Verwendung von Protokollen, dass jedes Protokoll über eine eigene Ausführungszeichenfolge verfügt.

Wenn Ihr MIME-Typ inline in einem Browser angezeigt werden kann, muss die ProgID für den MIME-Typ den **CLSID-Unterschlüssel** enthalten, der den Klassenbezeichner (CLSID) der entsprechenden Anwendung verwendet. Diese CLSID wird in einer Suche nach der CLSID in der MIME-Datenbank verwendet, die in **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** Classes MIME Database Content Type gespeichert \\  \\  \\  \\ ist. Wenn Ihr MIME-Typ nicht inline in einem Browser angezeigt werden soll, kann dieser Schritt ausgelassen werden.

### <a name="registration-subkey-and-value-descriptions"></a>Registrierungsunterschlüssel und Wertbeschreibungen

In diesem Abschnitt werden die einzelnen Registrierungsunterschlüssel und -werte beschrieben, die beim Registrieren einer Anwendung bei **Standardprogrammen** verwendet werden, wie zuvor veranschaulicht.

### <a name="capabilities"></a>Funktionen

Der Unterschlüssel **Funktionen** enthält alle **Informationen zu Standardprogrammen** für eine bestimmte Anwendung. Der Platzhalter %ApplicationCapabilityPath% bezieht sich auf den Registrierungspfad von **HKEY \_ CURRENT \_ USER** oder **HKEY \_ LOCAL \_ MACHINE** zum Unterschlüssel **Capabilities** der Anwendung. Dieser Unterschlüssel enthält die signifikanten Werte, die in der folgenden Tabelle dargestellt sind.



| Wert                  | type                       | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | REG \_ SZ oder REG EXPAND \_ \_ SZ | **Erforderlich**. Damit ein Benutzer eine informierte Standardzuweisungsauswahl treffen kann, muss eine Anwendung eine Zeichenfolge bereitstellen, die die Funktionen der Anwendung beschreibt. Obwohl im vorherigen Contoso-Beispiel die Beschreibung direkt dem ApplicationDescription-Wert zugewiesen wird, stellen Anwendungen die Beschreibung in der Regel als Ressource bereit, die in eine .dll-Datei eingebettet ist, um die Lokalisierung zu vereinfachen. Wenn ApplicationDescription nicht bereitgestellt wird, wird die Anwendung nicht in benutzeroberflächenlisten potenzieller Standardprogramme angezeigt.                                                            |
| ApplicationName        | REG \_ SZ oder REG EXPAND \_ \_ SZ | **Optional.** Der Name, mit dem das Programm auf der Benutzeroberfläche der Standardprogramme angezeigt wird. Wenn diese Daten nicht von der Anwendung bereitgestellt werden, wird der Name des ausführbaren Programms, das der ersten registrierten ProgID für die Anwendung zugeordnet ist, in der Benutzeroberfläche verwendet. ApplicationName muss immer mit dem Namen übereinstimmen, der unter [RegisteredApplications](#registeredapplications)registriert ist. Sie können ApplicationName verwenden, wenn Sie verschiedene Anwendungstypen wie einen Browser und einen E-Mail-Client verwenden möchten, um auf dieselbe ausführbare Datei zu verweisen, während sie als unterschiedliche Namen angezeigt werden.<br/> |
| Ausgeblendet                 | REG \_ DWORD                 | **Optional.** Legen Sie diesen Wert auf 1 fest, um die Anwendung aus der Liste der Programme im Dialogfeld **Standardprogramme festlegen** zu unterdrücken. Wenn dieser Wert 0 ist oder nicht vorhanden ist, wird die Anwendung normal in der Liste angezeigt.                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>FileAssociations

Der **Unterschlüssel FileAssociations** enthält bestimmte Dateizuordnungen, die von der Anwendung beansprucht werden. Diese Ansprüche werden als Werte mit einem Wert für jede Erweiterung gespeichert. Zuordnungen verweisen auf eine anwendungsspezifische ProgID anstelle einer generischen ProgID. Es ist jedoch nicht erforderlich, dass alle Zuordnungen auf dieselbe ProgID verweisen.

### <a name="mimeassociations"></a>MIMEAssociations

Der **MIMEAssociations-Unterschlüssel** enthält bestimmte MIME-Typen, die von der Anwendung beansprucht werden. Diese Ansprüche werden als Werte mit einem Wert für jeden MIME-Typ gespeichert. Der Wertname für jeden MIME-Typ muss genau mit dem MIME-Namen übereinstimmen, der in der MIME-Datenbank gespeichert ist. Dem Wert muss außerdem eine anwendungsspezifische ProgID zugewiesen werden, die die entsprechende CLSID der Anwendung enthält.

### <a name="startmenu"></a>Startmenü

Der **Unterschlüssel Startmenu** ist den vom Benutzer zuweisbaren **Internet-** und **E-Mail-Einträgen** im **Startmenü** zugeordnet. Eine Anwendung muss sich separat als Konkurrent für diese Einträge registrieren. Weitere Informationen finden Sie unter [Registrieren von Programmen mit Clienttypen.](reg-middleware-apps.md)

> [!Note]  
> Ab Windows 7 sind im **Startmenü** keine **Internet-** und **E-Mail-Einträge** mehr vorhanden. Die dem **E-Mail-Eintrag** zugeordneten Registrierungsdaten werden weiterhin für den MAPI-Standardclient verwendet, aber die dem **Interneteintrag** zugeordneten Registrierungsdaten werden von Windows überhaupt nicht verwendet.

 

Indem die **Startmenüregistrierung** einer Anwendung ihrer **Standardprogrammregistrierung** zugeordnet wird, wird die Anwendung in der Benutzeroberfläche **Zuordnungen festlegen** als potenzieller Standardwert angezeigt. Wenn der Benutzer die Anwendung als Standard ausgewählt hat und dann alle Anwendungsstandardeinstellungen später wiederherstellt, wird die Anwendung an der **Startmenüposition** für diesen Benutzer wiederhergestellt. Weitere Informationen und eine Abbildung finden Sie weiter unten in diesem Thema im Abschnitt [Benutzeroberfläche für Standardprogramme.](#default-programs-ui)

Der **Unterschlüssel Startmenu** verfügt über zwei Einträge: StartMenuInternet und Mail, die den kanonischen **Internet-** und **E-Mail-Positionen** im **Startmenü** entsprechen. Eine Anwendung weist entweder StartMenuInternet oder Mail einen Wert zu, der dem Namen des registrierten Unterschlüssels der Anwendung unter **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **StartMenuInternet** oder **HKEY LOCAL \_ \_ MACHINE** SOFTWARE Clients Mail entspricht \\  \\  \\  (wie unter Registrieren von Programmen [mit Clienttypen](reg-middleware-apps.md)beschrieben).

Im Fall der kanonischen **E-Mail-Position** im **Startmenü** stellt sie den STANDARDMÄßIGEN MAPI-Client dar und wird daher angenommen, dass er MAPI-Aufrufe übergeben kann. Während unter Windows 7 keine kanonische **E-Mail-Position** mehr im **Startmenü** vorhanden ist, wird dieser Unterschlüssel weiterhin für den MAPI-Standardclient verwendet. Eine Anwendung, die den E-Mail-Standardwert anfordert, sollte sich als MAPI-Handler unter dem folgenden Unterschlüssel registrieren:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

Wenn ein Mailclient MAPI nicht unterstützen kann, aber trotzdem um die kanonische Position des **Startmenüs** **"E-Mail"** ringen möchte, kann er eine Befehlszeile unter dem folgenden Unterschlüssel registrieren:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

Fügen Sie außerdem unter **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **Mail** \\ *CanonicalName* einen Standardwert mit dem Anwendungsnamen hinzu.

Mit diesen Einträgen kann die Anwendung über die **E-Mail-Position** des **Startmenüs** gestartet werden. Beachten Sie, dass MAPI-Aufrufe weiterhin an die Anwendung erfolgen und entweder durch den vorherigen MAPI-Handler fallen oder fehlschlagen, wenn kein MAPI-Handler festgelegt wurde. Weitere Informationen finden Sie unter [Registrieren von Programmen mit Clienttypen.](reg-middleware-apps.md)

### <a name="urlassociations"></a>UrlAssociations

Der **Unterschlüssel UrlAssociations** enthält die spezifischen URL-Protokolle, die von der Anwendung beansprucht werden. Diese Ansprüche werden als Werte mit einem Wert für jedes Protokoll gespeichert. Jedes Protokoll muss auf eine anwendungsspezifische ProgID anstatt auf eine generische ProgID verweisen. Wie im Contoso-Beispiel erwähnt, können Sie für jedes Protokoll eine andere ProgID verwenden, damit jedes eine eigene Ausführungszeichenfolge hat.

### <a name="registeredapplications"></a>RegisteredApplications

Der vollständige Unterschlüssel für **RegisteredApplications** lautet:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **RegisteredApplications**

Dieser Unterschlüssel stellt dem Betriebssystem den Registrierungsspeicherort der **Standardprogramminformationen** für die Anwendung bereit. Der Speicherort wird als Wert gespeichert, dessen Name mit dem Namen der Anwendung übereinstimmen muss.

### <a name="full-registration-example"></a>Beispiel für vollständige Registrierung

Dieses Beispiel zeigt die Unterschlüssel und Werte, die beim Registrieren des fiktiven Litware-Medienplayers verwendet werden. Das Beispiel enthält die ProgID-Einträge, um zu zeigen, wie alles zusammenpasst.

Der folgende Unterschlüssel zeigt die anwendungsspezifische ProgID für den .mp3 MIME-Typ:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

Als Nächstes folgt die anwendungsspezifische ProgID, mit der das Litware-Programm der .mp3 Dateinamenerweiterung zugeordnet wird.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

Die nächsten Einträge zeigen die kombinierte ProgID für den .mpeg MIME-Typ und die Dateinamenerweiterung an.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

Mit den nächsten Einträgen wird das Litware-Programm unter **Standardprogramme** registriert und die zuvor registrierten ProgIDs verwendet.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

In diesem Beispiel wird schließlich der Speicherort der **Litware-Standardprogrammregistrierung** registriert.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>Wird zum Standardbrowser

Die Browserregistrierung muss den in diesem Thema beschriebenen bewährten Methoden entsprechen. Wenn der Browser installiert ist, können Windows dem Benutzer eine Systembenachrichtigung anzeigen, über die der Benutzer den Browser als Systemstandard auswählen kann. Diese Benachrichtigung wird angezeigt, wenn diese Bedingungen erfüllt sind:

-   Das Installationsprogramm des Browsers ruft [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) mit dem **SHCNE \_ ASSOCCHANGED-Flag** auf, um Windows mitzuteilen, dass neue Protokollhandler registriert wurden.
-   Windows erkennt, dass eine oder mehrere neue Anwendungen registriert wurden, um sowohl http://- als auch https:// Protokolle zu verarbeiten, und der Benutzer wurde noch nicht benachrichtigt. Anders ausgedrückt: Dem Benutzer wurde keine der folgenden Informationen angezeigt: eine Systembenachrichtigung, die die Anwendung ankkündigungt, ein OpenWith-Flyout, das die Anwendung enthält, oder die Seite Set User Defaults (CSV) Systemsteuerung für die Anwendung.

Das folgende Beispiel zeigt den empfohlenen Registrierungscode, den das Installationsprogramm des Browsers ausführen soll, nachdem die Registrierungsschlüssel geschrieben wurden.

[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) benachrichtigt das System zunächst darüber, dass neue Zuordnungsoptionen verfügbar sind. Der **SHChangeNotify-Aufruf** ist erforderlich, um sicherzustellen, dass die Systemstandardeinstellungen ordnungsgemäß funktionieren.

Eine [**Sleep-Anweisung**](/windows/win32/api/synchapi/nf-synchapi-sleep) lässt dann Zeit für Systemprozesse zu, um die Benachrichtigung zu verarbeiten.


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



Wenn der Benutzer die resultierende Benachrichtigung oder das Flyout verwarf oder ignoriert, ohne eine neue Standardbrowserauswahl vorzunehmen, bleibt der Standardbrowser unverändert. Beachten Sie, dass der Benutzer den Standardbrowser auch jederzeit über andere Mechanismen ändern kann, einschließlich Festlegen von Benutzerstandardeinstellungen im Systemsteuerung.

## <a name="default-programs-ui"></a>Benutzeroberfläche für Standardprogramme

Die Abbildungen in diesem Abschnitt zeigen die Benutzeroberfläche für **Standardprogramme,** die vom Benutzer angezeigt wird.

Die folgende Abbildung zeigt das Hauptfenster **Standardprogramme** in Systemsteuerung.

![Screenshot der Einstiegsseite für Standardprogramme](images/defaultprogramsmain.png)

Wenn ein Benutzer die Option **Standardprogramme festlegen** ausgibt, wird das folgende Fenster angezeigt. Benutzer können diese Seite verwenden, um ein Standardprogramm für alle Dateitypen und Protokolle zuzuweisen, für die das Programm eine mögliche Standardeinstellung ist. Wie in der folgenden Abbildung dargestellt, werden alle [registrierten](#registering-an-application-for-use-with-default-programs) Programme und das Programmsymbol im Feld **Programme** auf der linken Seite angezeigt.

![Screenshot der Seite "Standardprogramme festlegen"](images/setyourdefaultprograms.png)

Wenn der Benutzer ein Programm aus der Liste auswählt, werden das Programmsymbol und der Anbieter angezeigt. Wenn die URL in das digital signierte Zertifikat des Programms eingebettet ist, kann das Programm auch eine URL anzeigen. Programme, die nicht digital signiert sind, können keine URL anzeigen.

Beschreibender Text, der während der Registrierung vom Programm bereitgestellt wird, wird ebenfalls angezeigt. Dieser Text ist erforderlich. Unterhalb des Beschreibungsfelds befindet sich ein Hinweis darauf, wie viele Standardwerte dem Programm derzeit aus der vollständigen Anzahl zugewiesen sind, die es verarbeiten soll.

Um ein Programm als Standard für alle Dateien und Protokolle, für die es registriert ist, zuzuweisen oder wiederherzustellen, klickt der Benutzer auf die Option **Dieses Programm als Standard festlegen.**

Um einem Programm einzelne Dateitypen und Protokolle zuzuweisen, klickt der Benutzer auf die Option **Standardwerte für dieses Programm auswählen,** die eine **Zuordnung für ein Programmfenster** festlegen wie in der folgenden Abbildung anzeigt.

> [!Note]  
> Es wird empfohlen, die **Einstellung Zuordnungen für ein Programm** mithilfe von [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui)aufzurufen.

 

![Screenshot der Satzzuordnungen für eine Programmseite](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>Bewährte Methoden für die Verwendung von Standardprogrammen

Dieser Abschnitt enthält Richtlinien für bewährte Methoden für die Verwendung von **Standardprogrammen** beim Registrieren von Anwendungen. Es bietet auch Entwurfsvorschläge zum Erstellen einer Anwendung, die Benutzern optimale **Standardprogrammfunktionen** bietet.

### <a name="during-installation"></a>Während der Installation

Zusätzlich zu den Installationsverfahren, die normalerweise unter Windows XP geübt werden, muss sich eine Windows Vista- oder höher-basierte Anwendung bei der **Funktion Standardprogramme** registrieren, um ihre Funktionalität nutzen zu können.

Führen Sie während der Installation die folgenden Schritte aus. Die Schritte 1 bis 3 entsprechen den Schritten, die in Windows XP verwendet wurden. Schritt 4 war neu in Windows Vista.

1.  Installieren Sie die erforderlichen Binärdateien.
2.  Schreiben Sie ProgIDs auf HKEY \_ LOCAL \_ MACHINE. Beachten Sie, dass Anwendungen anwendungsspezifische ProgIDs für ihre Zuordnungen erstellen müssen.
3.  Registrieren Sie die Anwendung bei **Standardprogrammen,** wie zuvor unter [Registrieren einer Anwendung für die Verwendung mit Standardprogrammen](#registering-an-application-for-use-with-default-programs)erläutert.

### <a name="after-installation"></a>Nach der Installation

In diesem Abschnitt wird erläutert, wie die Eingabeaufforderung der Anwendung jedem Benutzer zunächst die Standardoptionen präsentieren soll. Außerdem wird erläutert, wie eine Anwendung ihren Status als Standard für mögliche Zuordnungen und Protokolle überwachen kann.

### <a name="first-run-experiences"></a>Erste Ausführungserfahrungen

Wenn die Anwendung zum ersten Mal von einem Benutzer ausgeführt wird, wird empfohlen, dass die Benutzeroberfläche der Anwendung dem Benutzer angezeigt wird, die in der Regel diese beiden Optionen enthält:

-   Übernehmen Sie die Standardanwendungseinstellungen. Diese Option ist standardmäßig ausgewählt.
-   Passen Sie die Standardanwendungseinstellungen an.

Wenn der Benutzer vor Windows 8 die Standardeinstellungen akzeptiert, ruft Ihre Anwendung [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall)auf, wodurch alle Zuordnungen auf Computerebene, die während der Installation deklariert werden, in benutzerspezifische Einstellungen für diesen Benutzer konvertiert werden.

Wenn der Benutzer die Einstellungen anpassen möchte, ruft Ihre Anwendung [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) auf, um die Benutzeroberfläche für die Dateizuordnung anzuzeigen. Die folgende Abbildung zeigt dieses Fenster für den fiktiven Litware-Medienplayer.

![Screenshot der festgelegten Zuordnungen für eine Programmseite für Litware](images/setassociationsforaprogramforlitware.png)

Im Dateizuordnungsfenster werden die Von der Anwendung registrierten Standardwerte sowie die aktuelle Standardeinstellung für andere Erweiterungen und Protokolle angezeigt. Nachdem der Benutzer die Anpassung seiner Standardwerte abgeschlossen hat, klickt er auf die Schaltfläche **Speichern,** um die Änderungen zu übernehmen. Wenn der Benutzer auf **Abbrechen** klickt, wird das Fenster geschlossen, ohne Änderungen zu speichern.

Sie sollten diese Benutzeroberfläche für Ihre Anwendungen verwenden, anstatt eine eigene zu erstellen. Auf diese Weise speichern Sie die Ressourcen, die zuvor zum Entwickeln der Benutzeroberfläche für die Dateizuordnung erforderlich waren. Sie garantieren auch, dass Zuordnungen ordnungsgemäß gespeichert werden.

### <a name="set-an-application-to-check-whether-it-is-the-default"></a>Festlegen einer Anwendung, um zu überprüfen, ob sie die Standardeinstellung ist

> [!Note]  
> Dies wird ab Windows 8 nicht mehr unterstützt.

 

Anwendungen überprüfen in der Regel, ob sie beim Ausführen als Standard festgelegt sind. Legen Sie Ihre Anwendungen für diese Überprüfung fest, indem [**Sie IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) oder [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall)aufrufen.

Wenn die Anwendung feststellt, dass es sich nicht um die Standardeinstellung handelt, kann sie die Benutzeroberfläche darstellen, die den Benutzer auffordert, die aktuelle Situation zu akzeptieren oder die Anwendung zur Standardeinstellung zu machen. Schließen Sie immer ein Kontrollkästchen in diese Benutzeroberfläche ein, das standardmäßig ausgewählt ist und die Option darstellt, nicht erneut gefragt zu werden.

> [!Note]  
> Die Standardeinstellung sollte benutzergesteuert sein. Eine Anwendung sollte niemals einen Standardwert zurückfordern, ohne den Benutzer zu fragen.

 

Die folgende Abbildung zeigt ein Beispieldialogfeld.

![Screenshot eines Beispieldialogfelds](images/notthedefaultui.png)

## <a name="additional-resources"></a>Weitere Ressourcen

-   [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Dateizuordnungen](fa-best-practices.md)
</dt> <dt>

[Dateizuordnungsbeispielszenario](fa-sample-scenarios.md)
</dt> <dt>

[Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher](vista-managing-defaults.md)
</dt> <dt>

[Festlegen von Programmzugriff und Computerstandard (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
