---
description: Verwenden Sie Standardprogramme, um die Standardbenutzer Funktion festzulegen.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Standardprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2021
ms.locfileid: "103869292"
---
# <a name="default-programs"></a>Standardprogramme

Verwenden Sie **Standardprogramme** , um die Standardbenutzer Funktion festzulegen. Benutzer können über die Systemsteuerung oder direkt über das **Startmenü** auf **Standardprogramme** zugreifen. Legen Sie das Tool [Programm Zugriffs-und Computer Standardwerte (SPAD) fest](cpl-setprogramaccess.md) , das primäre Standardbenutzer Oberflächen für Benutzer in Windows XP.

> [!IMPORTANT]
> Dieses Thema gilt nicht für Windows 10. Die Art und Weise, wie standardmäßige Dateizuordnungen in Windows 10 geändert werden. Weitere Informationen finden Sie im Abschnitt zu den **Änderungen in Windows 10** für die Behandlung von Standard-apps in [diesem Beitrag](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Wenn ein Benutzerprogramm Standardwerte mithilfe von **Standardprogrammen** festlegt, gilt die Standardeinstellung nur für diesen Benutzer und nicht für andere Benutzer, die den gleichen Computer verwenden können. **Standardprogramme** bieten eine Reihe von APIs (in Windows 8 veraltet), mit denen unabhängige Softwarehersteller (ISVs) ihre Programme oder Anwendungen in das Standardsystem einbeziehen können. Der API-Satz hilft ISVs bei der besseren Verwaltung Ihres Status als Standardwerte.

Dieses Thema ist wie folgt organisiert:

-   [Einführung in Standardprogramme und den zugehörigen API-Satz](#introduction-to-default-programs-and-its-related-api-set)
-   [Registrieren einer Anwendung für die Verwendung mit Standardprogrammen](#registering-an-application-for-use-with-default-programs)
    -   [ProgIDs](#progids)
    -   [Registrierungs Unterschlüssel und Wert Beschreibungen](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [Beispiel für vollständige Registrierung](#full-registration-example)
-   [Wird zum Standard Browser](#becoming-the-default-browser)
-   [Benutzeroberfläche von Standardprogrammen](#default-programs-ui)
-   [Bewährte Methoden für die Verwendung von Standardprogrammen](#best-practices-for-using-default-programs)
    -   [Während der Installation](#during-installation)
    -   [Nach der Installation](#after-installation)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>Einführung in Standardprogramme und den zugehörigen API-Satz

**Standardprogramme** sind hauptsächlich für Anwendungen konzipiert, die Standard Dateitypen wie z. b. MP3-oder JPG-Dateien oder Standardprotokolle, wie z. b. http oder mailto, verwenden. Anwendungen, die ihre eigenen proprietären Protokolle und Dateizuordnungen verwenden, verwenden in der Regel nicht die **Standard-Programm** Funktionalität.

Nachdem Sie eine Anwendung für die **Standardprogramm** Funktionalität registriert haben, sind die folgenden Optionen und Funktionen verfügbar, indem Sie den API-Satz verwenden:

-   Stellen Sie alle registrierten Standardwerte für eine Anwendung wieder her. Veraltet für Windows 8.
-   Stellen Sie einen einzelnen registrierten Standardwert für eine Anwendung wieder her. Veraltet für Windows 8.
-   Fragen Sie den Besitzer eines bestimmten standardmäßig in einem einzelnen-Befehl ab, anstatt die Registrierung zu durchsuchen. Sie können den Standardwert einer Datei Zuordnung, eines Protokolls oder eines kanonischen Verbs im **Startmenü** Abfragen.
-   Hiermit wird eine Benutzeroberfläche für eine bestimmte Anwendung gestartet, in der ein Benutzer individuelle Standardeinstellungen festlegen kann.
-   Entfernen Sie alle Benutzer bezogenen Zuordnungen.

**Standardprogramme** bieten außerdem eine Benutzeroberfläche, die Ihnen ermöglicht, eine Anwendung zu registrieren, um dem Benutzer zusätzliche Informationen bereitzustellen. Eine Digital signierte Anwendung kann z. b. eine URL zur Startseite des Herstellers enthalten.

Die Verwendung des zugeordneten API-Satzes kann dazu beitragen, dass eine Anwendung unter der in Windows Vista eingeführten Benutzerkontensteuerung (User Account Control, UAC) ordnungsgemäß funktioniert. Unter UAC wird dem System ein Administrator als Standardbenutzer angezeigt, sodass der Administrator in der Regel nicht in die Unterstruktur des **\_ lokalen \_ HKEY** -Computers schreiben kann. Diese Einschränkung ist ein Sicherheits Feature, das verhindert, dass ein Prozess als Administrator ohne das Wissen des Administrators fungiert.

Die Installation eines Programms durch einen Benutzer wird in der Regel als erhöhter Prozess ausgeführt. Versuche einer Anwendung, das Standard Zuordnungs Verhalten auf Computer Ebene nach der Installation zu ändern, sind jedoch nicht erfolgreich. Stattdessen müssen die Standardeinstellungen auf Benutzerebene registriert werden, wodurch verhindert wird, dass mehrere Benutzer die Standardwerte der anderen überschreiben.

Die hierarchische Registrierungs Struktur für Datei-und Protokoll Zuordnungen hat Vorrang vor Standardeinstellungen auf Computer Ebene. Einige Anwendungen enthalten Punkte in Ihrem Code, die ihre Rechte vorübergehend erhöhen, wenn Sie die Standardwerte für den **lokalen HKEY- \_ \_ Computer** beanspruchen. Diese Anwendungen können unerwartete Ergebnisse erleben, wenn eine andere Anwendung bereits als Standardbenutzer registriert ist. Die Verwendung von **Standardprogrammen** verhindert diese Mehrdeutigkeit und garantiert die erwarteten Ergebnisse auf der Ebene pro Benutzer.

## <a name="registering-an-application-for-use-with-default-programs"></a>Registrieren einer Anwendung für die Verwendung mit Standardprogrammen

In diesem Abschnitt werden die Registrierungs Unterschlüssel und-Werte angezeigt, die zum Registrieren einer Anwendung mit **Standardprogrammen** benötigt werden. Es enthält ein vollständiges Beispiel.

Dieser Abschnitt enthält die folgenden Themen:

-   [ProgIDs](#progids)
-   [Registrierungs Unterschlüssel und Wert Beschreibungen](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [Beispiel für vollständige Registrierung](#full-registration-example)

**Standardprogramme** erfordert, dass jede Anwendung explizit die Dateizuordnungen, MIME-Zuordnungen und Protokolle registriert, für die die Anwendung als möglicher Standard aufgeführt werden soll. Sie registrieren die Zuordnungen mithilfe der folgenden Registrierungs Elemente, die später in diesem Thema unter [Registrierungs Unterschlüssel und Wert Beschreibungen](#registration-subkey-and-value-descriptions)ausführlich erläutert werden:

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

Im folgenden Beispiel werden die Registrierungseinträge für einen fiktiven Ordner mit dem Namen Webbrowser angezeigt:

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

Eine Anwendung muss eine bestimmte [ProgID](fa-progids.md)bereitstellen. Stellen Sie sicher, dass Sie alle Informationen einschließen, die in der Regel in den generischen Standard Unterschlüssel für die Erweiterung geschrieben werden. Der fiktive Litware Media Player stellt z. b. die anwendungsspezifischen HKEY-Software Klassen für **\_ lokale \_ Computer** \\  \\  \\ **LitwarePlayer11.AssocFile.MP3** Unterschlüssel bereit. Dieser Unterschlüssel enthält alle Informationen im generischen Standard-Unterschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Classes** \\ **. MP3** sowie alle zusätzlichen Informationen, die von der Anwendung registriert werden sollen. Dadurch wird sichergestellt, dass die Informationen des Litware-Players, wenn der Benutzer die. MP3-Zuordnung wiederherstellt, intakt sind und nicht von einer anderen Anwendung überschrieben wurden. (Überschreiben kann auftreten, wenn der Standard Unterschlüssel die einzige Quelle dieser Informationen ist.)

Wenn Sie eine ProgID einer Dateinamenerweiterung oder eines Protokolls zuordnen, kann eine Anwendung eins zu eins oder 1: n zuordnen. In CONSO Example zeigt condesohtml auf eine einzelne ProgID, die ShellExecute-Informationen für die Erweiterungen. htm,. html,. shtml,. xht und. XHTML bereitstellt. Da für jedes Protokoll eine andere ProgID vorhanden ist, aktivieren Sie bei Verwendung von Protokollen für jedes Protokoll eine eigene Ausführungs Zeichenfolge.

Wenn Ihr MIME-Typ Inline in einem Browser angezeigt werden kann, muss die ProgID für den MIME-Typ den **CLSID** -Unterschlüssel enthalten, der den Klassen Bezeichner (CLSID) der entsprechenden Anwendung verwendet. Diese CLSID wird in einer Suche nach der CLSID in der MIME-Datenbank verwendet, die in **HKEY- \_ \_** \\ **Software** \\ **Klassen** der \\ **MIME**- \\ **Datenbank**- \\ **Inhaltstyp** gespeichert ist. Wenn Ihr MIME-Typ nicht als Inline in einem Browser angezeigt werden soll, kann dieser Schritt ausgelassen werden.

### <a name="registration-subkey-and-value-descriptions"></a>Registrierungs Unterschlüssel und Wert Beschreibungen

In diesem Abschnitt werden die einzelnen Registrierungs Unterschlüssel und Werte beschrieben, die zum Registrieren einer Anwendung mit **Standardprogrammen** verwendet werden, wie zuvor veranschaulicht.

### <a name="capabilities"></a>Funktionen

Der Unterschlüssel **Funktionen** enthält alle **Standardprogramm** Informationen für eine bestimmte Anwendung. Der Platzhalter "% applicationcapabilitypath%" bezieht sich auf den Registrierungs Pfad von **HKEY \_ Current \_ User** oder **HKEY \_ local \_ Machine** zum Unterschlüssel der Anwendungs **Funktionen** . Dieser Unterschlüssel enthält die signifikanten Werte, die in der folgenden Tabelle aufgeführt sind.



| Wert                  | type                       | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | Reg \_ SZ oder reg \_ Expand \_ SZ | **Erforderlich**. Damit ein Benutzer eine fundierte Standard Zuweisungs Auswahl treffen kann, muss eine Anwendung eine Zeichenfolge bereitstellen, die die Funktionen der Anwendung beschreibt. Obwohl das vorherige Beispiel von "cationdescription" die Beschreibung direkt dem Wert "applicationdescription" zuweist, stellen Anwendungen die Beschreibung in der Regel als eine Ressource bereit, die in eine DLL-Datei eingebettet ist, um die Lokalisierung zu vereinfachen. Wenn "applicationdescription" nicht angegeben wird, wird die Anwendung nicht in der Benutzeroberflächen Liste möglicher Standardprogramme angezeigt.                                                            |
| ApplicationName        | Reg \_ SZ oder reg \_ Expand \_ SZ | **Optional.** Der Name, mit dem das Programm in der Benutzeroberfläche der Standardprogramme angezeigt wird. Wenn diese Daten nicht von der Anwendung bereitgestellt werden, wird der Name des ausführbaren Programms, das mit der ersten registrierten ProgID für die Anwendung verknüpft ist, in der Benutzeroberfläche verwendet. ApplicationName muss immer mit dem Namen identisch sein, der unter [RegisteredApplications](#registeredapplications)registriert ist. Sie können ApplicationName verwenden, wenn Sie möchten, dass verschiedene Anwendungs Typen, z. b. ein Browser und ein e-Mail-Client, auf dieselbe ausführbare Datei verweisen, während Sie als unterschiedliche Namen angezeigt werden.<br/> |
| Ausgeblendet                 | REG \_ DWORD                 | **Optional.** Legen Sie diesen Wert auf 1 fest, um die Anwendung aus der Liste der Programme im Dialogfeld " **Standardprogramme festlegen** " zu unterdrücken. Wenn dieser Wert 0 oder nicht vorhanden ist, wird die Anwendung normal in der Liste angezeigt.                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>Dateizuordnungen

Der Unterschlüssel **fileassociations** enthält bestimmte Dateizuordnungen, die von der Anwendung beansprucht werden. Diese Ansprüche werden als Werte mit einem Wert für jede Erweiterung gespeichert. Zuordnungen zeigen auf eine anwendungsspezifische ProgID anstelle einer generischen ProgID. Allerdings sind nicht alle Zuordnungen erforderlich, um auf dieselbe ProgID zu verweisen.

### <a name="mimeassociations"></a>Fehlstellungen

Der Unterschlüssel **MIMEAssociations** enthält bestimmte MIME-Typen, die von der Anwendung beansprucht werden. Diese Ansprüche werden als Werte mit einem Wert für jeden MIME-Typ gespeichert. Der Wertname für jeden MIME-Typ muss exakt mit dem MIME-Namen übereinstimmen, der in der MIME-Datenbank gespeichert ist. Dem Wert muss außerdem eine anwendungsspezifische ProgID zugewiesen werden, die die entsprechende CLSID der Anwendung enthält.

### <a name="startmenu"></a>Startmenü

Der Unterschlüssel **Startmenu** ist den vom Benutzer zustellbaren **Internet** -und **e-Mail** -Einträgen im **Startmenü** zugeordnet. Eine Anwendung muss separat als Kandidat für diese Einträge registriert werden. Weitere Informationen finden Sie unter [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md).

> [!Note]  
> Ab Windows 7 sind im **Startmenü** keine **Internet** -und **e-Mail-** Einträge mehr vorhanden. Die dem **e-Mail-** Eintrag zugeordneten Registrierungsdaten werden weiterhin für den Standard-MAPI-Client verwendet, aber die mit dem **Internet** Eintrag verknüpften Registrierungsdaten werden von Windows überhaupt nicht verwendet.

 

Indem die Registrierung einer Anwendung im **Startmenü** mit der Registrierung der **Standardprogramme** verknüpft wird, wird die Anwendung als potenzieller Standardwert in der Benutzeroberfläche der **Set-Zuordnungen** angezeigt. Wenn der Benutzer die Anwendung als Standard ausgewählt hat und anschließend alle Anwendungs Standardwerte später wiederherstellen möchten, wird die Anwendung für diesen Benutzer an der **Start** Menü Position wieder hergestellt. Weitere Informationen und eine Abbildung finden Sie im Abschnitt [default Programme UI](#default-programs-ui) weiter unten in diesem Thema.

Der Unterschlüssel **Startmenu** hat zwei Einträge: StartMenuInternet und Mail, die den kanonischen **Internet** -und **e-Mail-** Positionen im **Startmenü** entsprechen. Eine Anwendung weist entweder StartMenuInternet oder Mail einen Wert zu, der dem Namen des registrierten unter Schlüssels der Anwendung unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **StartMenuInternet** oder **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** entspricht (wie unter [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md)beschrieben).

Wenn die kanonische **e-Mail-** Position im **Startmenü** angezeigt wird, stellt Sie den Standard-MAPI-Client dar und wird daher als fähig angenommen, MAPI-Aufrufe zu übergeben. Wenn im **Startmenü** unter Windows 7 keine kanonische **e-Mail-** Position mehr vorhanden ist, wird dieser Unterschlüssel weiterhin für den standardmäßigen MAPI-Client verwendet. Eine Anwendung, die den Standardwert für die e-Mail beansprucht, sollte sich als MAPI-Handler unter dem folgenden Unterschlüssel registrieren:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

Wenn ein e-Mail-Client MAPI nicht unterstützen kann, aber immer noch für die kanonische Position des **Startmenü** **-e-Mail-** Supports kämpfen möchte, kann er eine Befehlszeile unter folgendem Unterschlüssel registrieren

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

Fügen Sie außerdem unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** \\ *CanonicalName* einen Standardwert mit dem Anwendungsnamen hinzu.

Diese Einträge ermöglichen das Starten der Anwendung über die **e-Mail-** Position des **Start** Menüs. Beachten Sie, dass MAPI-Aufrufe weiterhin an der Anwendung vorgenommen werden und entweder auf den vorherigen MAPI-Handler zugreifen oder einen Fehler erzeugen, wenn kein MAPI-Handler festgelegt wurde. Weitere Informationen finden Sie unter [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md).

### <a name="urlassociations"></a>Urlzuordnungen

Der **UrlAssociations** -Unterschlüssel enthält die spezifischen URL-Protokolle, die von der Anwendung beansprucht werden. Diese Ansprüche werden als Werte mit einem Wert für jedes Protokoll gespeichert. Jedes Protokoll muss auf eine anwendungsspezifische ProgID anstelle einer generischen ProgID zeigen. Wie im Beispiel "" von "" in "" von "", können Sie für jedes Protokoll eine andere ProgID verwenden, damit jede eine eigene Ausführungs Zeichenfolge hat.

### <a name="registeredapplications"></a>RegisteredApplications

Der vollständige Unterschlüssel für **RegisteredApplications** lautet:

**HKEY \_ \_** \\ **Software**- \\ **RegisteredApplications** für lokale Computer

Dieser Unterschlüssel stellt dem Betriebssystem den Registrierungs Speicherort der **Standardprogramm** Informationen für die Anwendung bereit. Der Speicherort wird als Wert gespeichert, dessen Name dem Namen der Anwendung entsprechen muss.

### <a name="full-registration-example"></a>Beispiel für vollständige Registrierung

Dieses Beispiel zeigt die Unterschlüssel und Werte, die beim Registrieren des fiktiven Litware Media Player verwendet werden. Das Beispiel enthält die ProgID-Einträge, um zu zeigen, wie alles zueinander passt.

Der folgende Unterschlüssel zeigt die anwendungsspezifische ProgID für den. MP3-MIME-Typ:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

Als nächstes ist die anwendungsspezifische ProgID, die das Litware-Programm der Dateinamenerweiterung ". MP3" zuordnet.

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

In den nächsten Einträgen wird die kombinierte ProgID sowohl für den MIME-Typ (. MPEG) als auch für die Dateinamenerweiterung angezeigt.

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

Mit den nächsten Einträgen wird das Litware-Programm in **Standardprogrammen** registriert und die zuvor registrierten ProgIDs verwendet.

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

Schließlich wird in diesem Beispiel der Speicherort der Litware- **Standardprogramm** Registrierung registriert.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>Wird zum Standard Browser

Die Browser Registrierung muss den in diesem Thema beschriebenen bewährten Methoden entsprechen. Wenn der Browser installiert ist, kann Windows dem Benutzer eine System Benachrichtigung präsentieren, über die der Benutzer den Browser als System Standard auswählen kann. Diese Benachrichtigung wird angezeigt, wenn die folgenden Bedingungen erfüllt sind:

-   Der Installer des Browsers ruft [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) mit dem Flag **shcne \_ assocchanged** auf, um Windows mitzuteilen, dass neue Protokollhandler registriert wurden.
-   Windows erkennt, dass eine oder mehrere neue Anwendungen registriert wurden, um sowohl die http://-als auch die https://-Protokolle zu verarbeiten, und der Benutzer wurde noch nicht benachrichtigt. Das heißt, dass dem Benutzer keine der folgenden Elemente angezeigt wird: eine System Benachrichtigung, die die Anwendung sendet, ein openWith Flyout, das die Anwendung enthält, oder die System Steuerungs Seite "Benutzer Standards festlegen (Sud)" für die Anwendung.

Das folgende Beispiel zeigt den empfohlenen Registrierungscode, den der Installer des Browsers ausführen muss, nachdem er seine Registrierungsschlüssel geschrieben hat.

" [**Shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) " benachrichtigt das System zunächst, dass neue Zuordnungs Optionen verfügbar sind. Der **shchangenotify** -Befehl ist erforderlich, um die ordnungsgemäße Funktionsweise von System Standardwerten sicherzustellen.

Eine [**Standby**](/windows/win32/api/synchapi/nf-synchapi-sleep) -Anweisung ermöglicht dann Zeit für System Prozesse, die Benachrichtigung zu verarbeiten.


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



Wenn der Benutzer die sich ergebende Benachrichtigung oder das resultierende Flyout ignoriert oder ignoriert, ohne eine neue Standardbrowser Auswahl vorzunehmen, bleibt der Standardbrowser unverändert. Beachten Sie, dass der Benutzer den Standardbrowser jederzeit über andere Mechanismen ändern kann, einschließlich der Einstellung Benutzer Standardwerte in der Systemsteuerung.

## <a name="default-programs-ui"></a>Benutzeroberfläche von Standardprogrammen

Die Abbildungen in diesem Abschnitt zeigen die Benutzeroberfläche für **Standardprogramme** , wie Sie der Benutzer sehen.

Die folgende Abbildung zeigt das Hauptfenster " **Programme** " in der Systemsteuerung.

![Screenshot der Seite "Standardprogramme-Eintrag"](images/defaultprogramsmain.png)

Wenn ein Benutzer die Option **Standardprogramme festlegen** auswählt, wird das folgende Fenster angezeigt. Benutzer können diese Seite verwenden, um ein Standardprogramm für alle Dateitypen und Protokolle zuzuweisen, für die das Programm eine mögliche Standardeinstellung ist. Wie in der folgenden Abbildung gezeigt, werden alle [registrierten](#registering-an-application-for-use-with-default-programs) Programme und das Programmsymbol auf der linken Seite im Feld **Programme** angezeigt.

![Screenshot der Seite "Festlegen der Standardprogramme"](images/setyourdefaultprograms.png)

Wenn der Benutzer ein Programm aus der Liste auswählt, werden das Programmsymbol und der Anbieter angezeigt. Wenn die URL in das Digital signierte Zertifikat des Programms eingebettet ist, kann das Programm auch eine URL anzeigen. Programme, die nicht digital signiert sind, können keine URL anzeigen.

Ein beschreibender Text, der vom Programm während der Registrierung bereitgestellt wird, wird ebenfalls angezeigt. Dieser Text ist erforderlich. Unter dem Feld Beschreibung finden Sie einen Hinweis darauf, wie viele Standardwerte dem Programm derzeit von der vollständigen Nummer zugewiesen werden, die für die Verarbeitung registriert ist.

Wenn Sie ein Programm als Standard für alle Dateien und Protokolle zuweisen oder wiederherstellen möchten, für die es registriert ist, klickt der Benutzer auf die Option **dieses Programm als Standard festlegen** .

Um einzelne Dateitypen und Protokolle einem Programm zuzuweisen, klickt der Benutzer auf die Option **Standardwerte für dieses Programm auswählen** , die eine **Gruppe von Zuordnungen für ein Programm** Fenster anzeigt, wie in der folgenden Abbildung dargestellt.

> [!Note]  
> Es wird empfohlen, dass Sie die **Set-Zuordnungen für ein Programm** mithilfe von [**iapplicationassociationregistrationui:: launchadvancedassociationui**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui)aufrufen.

 

![Screenshot der Seite "Sätze für ein Programm festlegen"](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>Bewährte Methoden für die Verwendung von Standardprogrammen

Dieser Abschnitt enthält bewährte Methoden für die Verwendung von **Standardprogrammen** beim Registrieren von Anwendungen. Außerdem bietet es Entwurfsvorschläge zum Erstellen einer Anwendung, die den Benutzern optimale **Standardprogramm** Funktionen bietet.

### <a name="during-installation"></a>Während der Installation

Zusätzlich zu den Installations Prozeduren, die normalerweise unter Windows XP ausgeführt werden, muss eine auf Windows Vista oder höher basierende Anwendung mit der **Standardprogramm** Funktion registriert werden, um von den Funktionen zu profitieren.

Führen Sie die folgenden Schritte während der Installation aus. Die Schritte 1-3 entsprechen den Schritten, die in Windows XP verwendet wurden. Schritt 4 war neu in Windows Vista.

1.  Installieren Sie die erforderlichen Binärdateien.
2.  Schreiben Sie ProgIDs auf den lokalen HKEY- \_ \_ Computer. Beachten Sie, dass Anwendungen anwendungsspezifische ProgIDs für Ihre Zuordnungen erstellen müssen.
3.  Registrieren Sie die Anwendung mit **Standardprogrammen** , wie zuvor in [Registrieren einer Anwendung für die Verwendung mit Standardprogrammen](#registering-an-application-for-use-with-default-programs)erläutert.

### <a name="after-installation"></a>Nach der Installation

In diesem Abschnitt wird erläutert, wie die Anwendungs Aufforderung den einzelnen Benutzern zuerst die Standardoptionen präsentieren sollte. Außerdem wird erläutert, wie eine Anwendung ihren Status als Standardwert für die möglichen Zuordnungen und Protokolle überwachen kann.

### <a name="first-run-experiences"></a>Erfahrung beim ersten Ausführen

Wenn die Anwendung zum ersten Mal von einem Benutzer ausgeführt wird, wird empfohlen, dass die Anwendung die Benutzeroberfläche für den Benutzer anzeigt, der normalerweise diese beiden Optionen umfasst:

-   Akzeptieren Sie die Standard Anwendungseinstellungen. Diese Option ist standardmäßig ausgewählt.
-   Passen Sie die Standard Anwendungseinstellungen an.

Wenn der Benutzer vor Windows 8 die Standardeinstellungen annimmt, ruft die Anwendung [**iapplicationassociationregistration:: setappasdefaultall**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall)auf, bei der alle während der Installation deklarierten Zuordnungen auf Computer Ebene für diesen Benutzer in benutzerspezifische Einstellungen konvertiert werden.

Wenn sich der Benutzer entscheidet, die Einstellungen anzupassen, ruft die Anwendung [**iapplicationassociationregistrationui:: launchadvancedassociationui**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) auf, um die Benutzeroberfläche der Datei Zuordnung anzuzeigen. Die folgende Abbildung zeigt dieses Fenster für den fiktiven Litware Media Player.

![Screenshot der Seite "Zuordnungen für ein Programm festlegen" für Litware](images/setassociationsforaprogramforlitware.png)

Das Fenster Datei Zuordnung zeigt die Standardwerte an, die die Anwendung registriert hat, und zeigt außerdem den aktuellen Standardwert für andere Erweiterungen und Protokolle an. Nachdem der Benutzer seine Standardeinstellungen angepasst hat, klicken Sie auf die Schaltfläche **Speichern** , um die Änderungen zu übertragen. Wenn der Benutzer auf **Abbrechen** klickt, wird das Fenster geschlossen, ohne die Änderungen zu speichern.

Sie sollten diese Benutzeroberfläche für Ihre Anwendungen verwenden, anstatt ihre eigenen zu erstellen. Auf diese Weise können Sie die Ressourcen speichern, die zuvor zum Entwickeln der Benutzeroberfläche für die Datei Zuordnung benötigt wurden. Außerdem gewährleisten Sie, dass Zuordnungen ordnungsgemäß gespeichert werden.

### <a name="set-an-application-to-check-whether-it-is-the-default"></a>Festlegen einer Anwendung, um zu überprüfen, ob Sie die Standardeinstellung ist

> [!Note]  
> Dies wird ab Windows 8 nicht mehr unterstützt.

 

Anwendungen überprüfen in der Regel, ob Sie als Standard festgelegt werden, wenn Sie ausgeführt werden. Legen Sie Ihre Anwendungen so fest, dass diese Überprüfung durch Aufrufen von " [**iapplicationassociationregistration:: queryappisdefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) " oder " [**iapplicationassociationregistration:: queryappisdefaultall**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall)" durchführen wird.

Wenn die Anwendung feststellt, dass es sich nicht um die Standardeinstellung handelt, kann Sie die Benutzeroberfläche zur Verfügung stellen, die den Benutzer auffordert, ob Sie die aktuelle Situation akzeptieren oder die Anwendung als Standard festlegen möchten. Fügen Sie in dieser Benutzeroberfläche immer ein Kontrollkästchen ein, das standardmäßig ausgewählt ist und die Option anzeigt, dass die Option nicht erneut angefordert werden soll.

> [!Note]  
> Der Standardwert sollte vom Benutzer gesteuert werden. Eine Anwendung sollte niemals einen Standardwert freigeben, ohne den Benutzer zu Fragen.

 

Die folgende Abbildung zeigt ein Beispiel Dialogfeld.

![Screenshot eines Beispiel Dialogfelds](images/notthedefaultui.png)

## <a name="additional-resources"></a>Weitere Ressourcen

-   [**Iapplicationassociationregistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [**Iapplicationassociationregistrationui**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Dateizuordnungen](fa-best-practices.md)
</dt> <dt>

[Beispielszenario für Datei Zuordnung](fa-sample-scenarios.md)
</dt> <dt>

[Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher](vista-managing-defaults.md)
</dt> <dt>

[Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
