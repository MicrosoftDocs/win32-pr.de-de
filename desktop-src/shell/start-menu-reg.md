---
description: Das Startmenü in Windows XP und Windows Vista enthält reservierte Slots für die Standard Clients für Internet (Browser) und e-Mail (Mail), die häufig als Startmenü-Internetanwendungen bezeichnet werden.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219050"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a>Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü

> [!Note]  
> Dieses Thema gilt für Windows XP, Windows Vista und Windows 7.

 

Das Startmenü in Windows XP und Windows Vista enthält reservierte Slots für die Standard Clients für **Internet** (Browser) und **e-Mail** (Mail), die häufig als *Startmenü-Internetanwendungen* bezeichnet werden. Anwendungen, die als Startmenü-Internet Anwendungen registriert sind, über das gesamte System (pro Computer). In Windows Vista kann der Benutzer das **Standardprogramm "Programme** " verwenden, um eine Standardeinstellung für Benutzer festzulegen.

Wenn Anwendungen als Startmenü-Internet Anwendungen registriert werden, erstellen Windows XP und Windows Vista **Internet** -und **e-Mail-** Symbole im Startmenü. Wenn Sie auf diese Symbole klicken, wird das Startmenü zum Überprüfen der Registrierungs Teilstruktur pro Benutzer (**HKEY \_ Current \_ User**) verwendet. Wenn keine benutzerspezifische Standardeinstellung gefunden wird, sucht das Startmenü in der Unterstruktur des **lokalen HKEY-Computers nach \_ \_** dem Standard Unterschlüssel pro Computer.

> [!Note]  
> Die Standardinstallation von Windows registriert nicht ein standardmäßiges Internet oder e-Mail-Programm pro Benutzer, sondern nur eine systemweite Standardeinstellung. Dies bietet einen reibungslosen Upgradepfad von früheren Versionen des Betriebssystems, in dem nur die HKEY- \_ \_ Unterstruktur lokaler Computer für Client Registrierungen unterstützt wird.

 

In diesem Thema werden die folgenden Elemente erläutert:

-   [Registrieren für den Startmenü-Internet Link](#registering-for-the-start-menu-internet-link)
    -   [Registrieren als standardmäßiger Internet Client](#how-to-register-as-the-default-internet-client)
-   [Registrieren für den Link "Startmenü-e-Mail"](#registering-for-the-start-menu-email-link)
    -   [Anzeigen des Standard-e-Mail-Clients im Startmenü](#how-the-start-menu-displays-the-default-email-client)
    -   [Registrieren als Standard-e-Mail-Client](#how-to-register-as-the-default-email-client)
-   [Anpassen des Kontextmenüs](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a>Registrieren für den Startmenü-Internet Link

> [!Note]  
> Diese Registrierung ist ab Windows 7 veraltet, wodurch kein Startmenü-Internet Link mehr zur Verfügung steht. Vorhandene Registrierungen werden in Windows 7 und höher ignoriert. Die Registrierung als standardmäßige Startmenü-Internet Anwendung ist nicht identisch mit der Registrierung als Standard Webbrowser. Der Standard Webbrowser wird verwendet, um beliebige URLs von einer beliebigen Stelle im System aus zu starten. Das Startmenü "Internetanwendung" steuert nur das Programm, das gestartet wird, wenn der Benutzer im Startmenü auf das Internet-Symbol klickt.

 

Alle Webbrowser Anwendungen können sich registrieren, damit Sie im Startmenü als Internet Client angezeigt werden. Diese Sichtbarkeit, gekoppelt mit der ordnungsgemäßen Registrierung für die [Datei](fa-intro.md) -und [Protokoll](/previous-versions//aa767743(v=vs.85)) Typen einer Anwendung, gibt dem Standardbrowser Status der Anwendung.

Registrierungen, die in der **HKEY \_ Current \_ User** -Teilstruktur vorgenommen wurden, haben Vorrang vor den entsprechenden Registrierungen, die auf dem **lokalen HKEY- \_ \_ Computer** durchgeführt wurden. Für neue Benutzer im System werden die auf dem **lokalen HKEY- \_ \_ Computer** gespeicherten Einstellungen verwendet. Ab Windows XP werden die Internet Einstellungen für das Startmenü in den Standardeinträgen für zwei Registrierungs Speicherorte gespeichert:

-   **HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Clients** \\ **StartMenuInternet**
-   **HKEY \_ Software Clients für lokale \_ Computer** \\  \\  \\ **StartMenuInternet**

Der Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Clients** \\ **StartMenuInternet** beschreibt den Internetbrowser, der gestartet wird, wenn der Benutzer im Startmenü auf das **Internet** -Symbol klickt. Wenn der Unterschlüssel leer ist oder nicht vorhanden ist, wird das **Internet** -Symbol im Startmenü auf den Standardwert des Systems festgelegt, das am zweiten Speicherort auf **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **StartMenuInternet** gespeichert ist, in dem alle auf dem System installierten Internet Browser Anwendungen beschrieben werden.

Wenn ein neuer Benutzer sich beim System anmeldet, verwendet das Startmenü den Standardwert im Unterschlüssel auf **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **StartMenuInternet** , um den standardmäßigen Internet Client anzuzeigen und die registrierte Anwendung zu starten, wenn auf das Symbol geklickt wird.

### <a name="how-to-register-as-the-default-internet-client"></a>Registrieren als standardmäßiger Internet Client

Unterhalb des unter Schlüssels **HKEY \_ lokale \_ Computer** \\ **Software** \\ **Clients** \\ **StartMenuInternet** können NULL oder mehr Unterschlüssel vorhanden sein, eine für jede registrierte Internet Browser Anwendung. Ein hypothetisches System könnte z. b. folgende Anordnung aufweisen:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

Wir veranschaulichen Registrierungseinträge mit einem hypothetischen Browser namens "Lit View" aus einem fiktiven Unternehmen namens Litware Inc. angenommen, der Name der ausführbaren Datei ist Litview.exe. Die Registrierung der beleuchteten Ansicht erfolgt wie hier gezeigt:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Die LocalizedString-Daten sind vom Typ reg \_ SZ, oder reg \_ Expand SZ, \_ Wenn Pfad Variablen wie `%programfiles%` verwendet werden. LocalizedString stellt den Pfad zu einer ausführbaren Datei (. exe) oder einer Bibliotheksdatei (DLL-Datei) bereit. Beachten Sie, dass die Pfad Zeichenfolge mit einem "at"-Zeichen (@) beginnt und dass für den Pfad keine Anführungszeichen erforderlich sind, unabhängig davon, ob darin Leerzeichen enthalten sind. Die ganzzahlige Ganzzahl ist die ID einer Zeichen folgen Ressource, die in der angegebenen dll enthalten ist, deren Wert dem Benutzer angezeigt werden soll. Dadurch kann dieselbe Registrierung für mehrere Sprachen verwendet werden. Jede Sprache stellt eine andere ResourceDLL.dll bereit. Dadurch kann das System die richtige Zeichenfolge auf der Grundlage der aktuell ausgewählten Sprache anzeigen.

Mit dem folgenden reg \_ SZ-oder reg \_ Expand-Wert wird \_ das Startmenü des Standard Symbols angezeigt, das angezeigt wird, wenn der Benutzer die Beleuchtung als Startmenü im Internet Browser auswählt.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

Der folgende Registrierungs Unterschlüssel gibt eine Befehlszeile an, die ausgeführt werden soll, wenn der Benutzer im Startmenü auf den Menübefehl Internet klickt Der Befehl könnte z. b. den Browser mit der Startseite des Benutzers öffnen, oder der Befehl könnte eine einführende Benutzeroberfläche starten, die der unabhängige Softwarehersteller (ISV) geeignet ist. Die Daten sind vom Typ reg \_ SZ oder reg \_ Expand \_ SZ. Beachten Sie jedoch, dass der Pfad der ausführbaren Datei in Anführungszeichen eingeschlossen ist, weil der Befehlszeilen Pfad leer ist.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

Wenn der Benutzer über [Set Program Access and Computer defaults (SPAD)](cpl-setprogramaccess.md) angibt, dass die beleuchtete Ansicht als Standard Webbrowser auf Computer Ebene verwendet werden soll, sollte die Anwendung den folgenden reg \_ SZ-Eintrag festlegen. Beachten Sie, dass der Zugriff auf diesen Unterschlüssel zulässig ist, da SPAD mit Administrator Rechten ausgeführt wird.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> In Windows Vista sollte der Standard Webbrowser auf Benutzerebene mit dem Tool " **Standardprogramme** " und nicht mit " [SPAD](cpl-setprogramaccess.md)" festgelegt werden.
> 
> **Die folgenden Informationen gelten nur für Windows XP.**
> 
> Wenn die Registrierung des Standard Webbrowser auf Computer Ebene unter HKEY \_ local \_ Machine, wie oben gezeigt, erfolgreich ist, sollte die Anwendung den Standardeintrag unter dem folgenden Unterschlüssel löschen:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> Wenn die Registrierung des Standard Webbrowser auf Computer Ebene unter HKEY \_ local \_ Machine fehlschlägt, sollte die Anwendung die REG SZ- \_ Daten wie im folgenden Beispiel für die Anwendung lit View festlegen:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

Nach dem Aktualisieren der entsprechenden Unterschlüssel überträgt die Anwendung die [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht, wobei der *wParam* -Parameter auf 0 festgelegt ist und der zugehörige *LPARAM* -Parameter auf die auf NULL endenden Zeichenfolge verweist `"Software\Clients\StartMenuInternet"` . Dadurch wird das Betriebssystem benachrichtigt, dass sich der Standard Client geändert hat.

Das Festlegen dieser Unterschlüssel für das standardmäßige Startmenü Internet Browser ist erforderlich, um die Abwärtskompatibilität mit alten Webbrowsern beizubehalten, die keine benutzerspezifischen Registrierungen unterstützen.

## <a name="registering-for-the-start-menu-email-link"></a>Registrieren für den Link "Startmenü-e-Mail"

> [!Note]  
> Der Link für den Startmenü-e-Mail-Link wurde ab Windows 7 entfernt. Diese in diesem Abschnitt erörterte Registrierung sollte jedoch weiterhin durchgeführt werden, um den standardmäßigen MAPI-Client zuzuweisen.

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a>Anzeigen des Standard-e-Mail-Clients im Startmenü

Eine beliebige e-Mail-Anwendung kann als e-Mail-Client im Startmenü angezeigt werden. Diese Sichtbarkeit, gekoppelt mit der ordnungsgemäßen Registrierung für die [Datei](fa-intro.md) -und [Protokoll](/previous-versions//aa767743(v=vs.85)) Typen einer Anwendung, gibt dem Standard-e-Mail-Status der Anwendung.

Registrierungen, die in der **HKEY \_ Current \_ User** -Teilstruktur vorgenommen wurden, haben Vorrang vor den entsprechenden Registrierungen, die auf dem **lokalen HKEY- \_ \_ Computer** durchgeführt wurden. Für neue Benutzer im System werden die auf dem **lokalen HKEY- \_ \_ Computer** gespeicherten Einstellungen verwendet. Ab Windows XP werden die e-Mail-Einstellungen für das Startmenü in den Standardeinträgen für zwei Registrierungs Speicherorte gespeichert:

-   **HKEY \_ \_** \\ **Software** \\ **Clients** \\  aktueller Benutzer
-   **HKEY \_ E \_**- \\  \\  \\ **Mail** -Clients für lokale Computer

Der Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Clients** \\ **Mail** beschreibt den e-Mail-Client, der gestartet wird, wenn der Benutzer im Startmenü auf das **e-Mail-** Symbol klickt.

Der Unterschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** beschreibt die e-Mail-Anwendungen, die auf dem System installiert sind, sowie die Standard-e-Mail-Anwendung.

Wenn die e-Mail-Clients des **aktuellen HKEY- \_ \_ Benutzers** \\  \\  \\  leer sind oder nicht vorhanden sind, wird der Standardwert, der in **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** definiert ist, verwendet, um die im Startmenü angezeigte e-Mail-Anwendung auszuwählen

Wenn ein neuer Benutzer sich beim System anmeldet, verwendet das Startmenü den Standardwert im Unterschlüssel unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** , um den Standard-e-Mail-Client anzuzeigen, und startet die registrierte Anwendung, wenn auf das Symbol geklickt wird.

### <a name="how-to-register-as-the-default-email-client"></a>Registrieren als Standard-e-Mail-Client

**HKEY \_ E \_** \\  \\  \\ -**Mail** -Clients für lokale Computer können keine oder mehrere Unterschlüssel enthalten, eine für jede registrierte e-Mail-Anwendung. Ein hypothetisches System könnte z. b. die folgenden Unterschlüssel definieren:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

Wir veranschaulichen Registrierungseinträge mit einem hypothetischen e-Mail-Client namens "Lit Mail" aus dem fiktiven Unternehmen namens Litware Inc. Litware Inc. beschließt, diesen e-Mail-Client unter dem internen Namen "LitMail" zu registrieren. Wie bei einem Browser ist der interne Name eine eindeutige Zeichenfolge, die als Unterschlüssel Name verwendet wird, der aber nie dem Benutzer angezeigt wird.

Um den e-Mail-Client für die Beleuchtung als Standard zu installieren, verwenden Sie den folgenden Unterschlüssel und die zugehörigen Einträge:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

Die LocalizedString-Daten sind vom Typ reg \_ SZ, oder reg \_ Expand SZ, \_ Wenn Pfad Variablen wie `%programfiles%` verwendet werden. LocalizedString stellt den Pfad zu einer ausführbaren Datei (. exe) oder einer Bibliotheksdatei (DLL-Datei) bereit. Beachten Sie, dass die Pfad Zeichenfolge mit einem "at"-Zeichen (@) beginnt und dass für den Pfad keine Anführungszeichen erforderlich sind, unabhängig davon, ob darin Leerzeichen enthalten sind. Die ganzzahlige Ganzzahl ist die ID einer Zeichen folgen Ressource, die in der angegebenen dll enthalten ist, deren Wert dem Benutzer angezeigt werden soll. Dadurch kann dieselbe Registrierung für mehrere Sprachen verwendet werden. Jede Sprache stellt eine andere ResourceDLL.dll bereit. Dadurch kann das System die richtige Zeichenfolge auf der Grundlage der aktuell ausgewählten Sprache anzeigen.

Nach dem Aktualisieren der entsprechenden Unterschlüssel überträgt die Anwendung die [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht, wobei der *wParam* -Parameter auf 0 festgelegt ist und der zugehörige *LPARAM* -Parameter auf die auf NULL endenden Zeichenfolge verweist `"Software\Clients\Mail"` . Dadurch wird das Betriebssystem benachrichtigt, dass sich der Standard Client geändert hat.

Aus Gründen der Abwärtskompatibilität mit Anwendungen, die keine lokalisierten Zeichen folgen unterstützen, sollte der Name der Anwendung in der installierten Sprache auch als Standardwert für den Unterschlüssel festgelegt werden.

Mit dem folgenden **reg \_ SZ** -oder reg-Erweiterungs Wert wird das Startmenü des Standard Symbols angezeigt, das angezeigt wird, wenn der Benutzer "Lit Mail" als Start Menü-e-Mail-Programm auswählt: **\_ \_**

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

Der folgende Eintrag gibt eine Befehlszeile an, die ausgeführt werden soll, wenn der Benutzer im Startmenü auf das Menü Element **e-Mail** klickt, vorausgesetzt, dass Lit Mail das ausgewählte e-Mail-Programm für das Startmenü ist Diese Befehlszeile wird auch ausgeführt, wenn der Benutzer im Menü Extras von Windows **Internet Explorer die** Option **e-Mail lesen auswählt** . Die Daten sind vom Typ **reg \_ SZ** oder **reg \_ Expand \_ SZ**. Beachten Sie jedoch, dass der Pfad der ausführbaren Datei in Anführungszeichen eingeschlossen ist, weil der Befehlszeilen Pfad leer ist.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

Wenn (und nur wenn) *der Benutzer die* Beleuchtung als standardmäßige Startmenü-e-Mail-Anwendung angibt, kann die Anwendung "Lit Mail" den internen Namen in den folgenden **reg- \_ SZ** -Wert schreiben:

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

Wenn (und nur wenn) *der Benutzer die* Beleuchtung als systemweite Standard-e-Mail-Anwendung angibt, kann die Anwendung "Lit Mail" den internen Namen in den unten angegebenen **reg \_ SZ** -Wert schreiben. Beachten Sie, dass der Zugriff auf diesen Unterschlüssel möglicherweise eingeschränkt ist. Anwendungen sollten nicht davon ausgehen, dass alle Benutzer über die Berechtigung zum Ändern der systemweiten Standard-e-Mail-Anwendung verfügen.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

Die Registrierung als standardmäßige Startmenü-e-Mail-Anwendung entspricht nicht der Registrierung als Standard-e-Mail-Client des Systems oder dem registrierten *mailto* -Handler.

-   Der Standard-e-Mail-Client des Systems wird gestartet, wenn der Benutzer im **Internet Explorer** -Menü Extras auf **e-Mail lesen** klickt.
-   Der registrierte *mailto* -Handler wird gestartet, wenn der Benutzer auf eine URL des Formulars klickt `mailto:someone@example.com` .
-   Die Start Menü-e-Mail-Anwendung wird gestartet, wenn der Benutzer im Startmenü auf das **e-Mail-** Symbol klickt.

Wenn keine standardmäßige Start Menü-e-Mail-Anwendung angegeben ist, wird das e-Mail-Symbol im Startmenü den standardmäßigen e-Mail-Client

In diesem Thema wird die Registrierung der Anwendung nicht als Standard- *mailto* -Protokollhandler behandelt. Anwendungen, die sich auf diese Weise registrieren möchten, sollten weiterhin den vorhandenen Spezifikationen für diesen Betreff entsprechen.

## <a name="customizing-the-context-menu"></a>Anpassen des Kontextmenüs

Eine Anwendung kann die Eigenschaften Seiten anpassen, die angezeigt werden, wenn der Benutzer im Kontextmenü des **e-Mail-** Symbols (oder des **Internet** Symbols) **Eigenschaften** auswählt. Die Litware-e-Mail-Anwendung fügt z. b. die folgenden **reg \_ SZ** -oder **reg \_ Expand \_** -Daten hinzu, um ein benutzerdefiniertes Eigenschaften Blatt für das **e-Mail-** Symbol anstelle seines Standardeigenschaften Blatts anzuzeigen

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

Das MUIVerb-Datenelement wird beginnend mit einem "at"-Zeichen (@), gefolgt vom vollständigen Pfad zur Ressourcen-DLL, einem Komma, einem Minuszeichen (-) und dann dem anzuzeigenden Dezimalzeichen folgen Ressourcen Bezeichner erstellt. Beachten Sie, dass der Pfad zum LitMail.exe Programm Leerzeichen enthält, sodass die Pfad Zeichenfolge in Anführungszeichen gesetzt wird.

Eine Anwendung kann dem Kontextmenü auch weitere Befehle hinzufügen. Beispielsweise fügt die Litware-e-Mail-Anwendung einen **Find** -Befehl mit den folgenden **reg \_ SZ** -Daten hinzu:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

Der Unterschlüssel Name unterhalb der **Shell** (in diesem Fall "Find") ist ein beliebiger, nicht lokalisierter Name. Erneut enthalten die MUIVerb-Daten ein "at"-Zeichen (@) als erstes Element, gefolgt vom Pfad zu einer Ressourcen-DLL, einem Komma Trennzeichen und einem Minuszeichen, das dem Dezimalzeichen folgen Ressourcen Bezeichner vorangestellt ist. Beispielsweise könnte diese Zeichen folgen Ressource "Open Address Book" lauten. Beachten Sie schließlich, dass die Befehlszeilen Zeichenfolge Leerzeichen enthält, sodass Sie in Anführungszeichen eingeschlossen ist.

 

 
