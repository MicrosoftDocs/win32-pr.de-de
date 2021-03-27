---
description: In diesem Thema wird das Feature "Programm Zugriff und Computer Standardwerte (SPAD)" in der Systemsteuerung erläutert.
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f35d9ed70d382e2db6714082ade2d2d76e6ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214434"
---
# <a name="set-program-access-and-computer-defaults-spad"></a>Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD)

In diesem Thema wird das Feature " **Programm Zugriff und Computer Standardwerte (SPAD)** " in der Systemsteuerung erläutert. SPAD befindet sich unter dem System Steuerungselement [Standardprogramme](default-programs.md) in Windows Vista und höheren Versionen von Windows. In Windows XP befindet er sich **im Element "Software" unter "** Software" und hat den Titel " **Programm Zugriff und Standardwerte festlegen**".

> [!IMPORTANT]
> Dieses Thema gilt nicht für Windows 10. Die Art und Weise, wie standardmäßige Dateizuordnungen in Windows 10 geändert werden. Weitere Informationen finden Sie im Abschnitt zu den **Änderungen in Windows 10** für die Behandlung von Standard-apps in [diesem Beitrag](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

-   [Verwenden des Tools "Programm Zugriff und Computer Standards festlegen"](#using-the-set-program-access-and-computer-defaults-tool)
    -   [Eine Übersicht über das Festlegen des Programm Zugriffs und der Standardeinstellungen für Computer](#an-overview-of-set-program-access-and-computer-defaults)
    -   [Der Registrierungs Wert "lastuserinitiateddefaultchange"](#the-lastuserinitiateddefaultchange-registry-value)
-   [Filtern der Liste "Software"](#filtering-the-add-or-remove-programs-list)
-   [Weitere Ressourcen](#filtering-the-add-or-remove-programs-list)
-   [Zugehörige Themen](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>Verwenden des Tools "Programm Zugriff und Computer Standards festlegen"

> [!Note]  
> Ab Windows 8 konfiguriert SPAD standardmäßig die Standardeinstellungen für den aktuellen Benutzer. Vor Windows 8 wurden die Standardeinstellungen für die SPAD-Gruppe festgelegt. Wenn ein Benutzer standardmäßig noch nicht vom Benutzer konfiguriert wurde, werden Sie vom System aufgefordert, eine benutzerspezifische Standardeinstellung festzulegen, anstatt einen computerbasierten Standardwert zurückzusetzen. Es ist möglich, dass die Standardeinstellungen für Computer in Windows Vista und Windows 7 nie von Benutzern erkannt werden, wenn Sie zuvor benutzerspezifische Standardeinstellungen festgelegt haben, da benutzerspezifische Standardeinstellungen in diesen Betriebssystemen standardmäßig überschreiben.

 

In Windows XP **ist das** **Festlegen des Programm Zugriffs und der Standardeinstellungen** ein Tool, das in der Systemsteuerung in der Systemsteuerung als Option festgestellt wird. In Windows Vista und höher befindet sich diese unter dem System Steuerungselement " [Standardprogramme](default-programs.md) ". Für [registrierte](reg-middleware-apps.md) Programme führt Sie die folgenden Funktionen aus:

-   Aktiviert die Auswahl von Standardprogrammen für jeden Clienttyp (nur bis zu Windows 7).
-   Ermöglicht das Steuern der Anzeige der Symbole, Verknüpfungen und Menüeinträge des Programms.
-   Stellt einen Satz vordefinierter Standardprogramm Optionen bereit. (Nur Windows XP Service Pack 1 (SP1))

Dieses Tool wird für die folgenden fünf Client Typen verwendet.

-   Browser
-   Email
-   Programm für sofortige Messung
-   Media Player
-   Virtueller Computer für Java

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>Eine Übersicht über das Festlegen des Programm Zugriffs und der Standardeinstellungen für Computer

Die Seite " **Programm Zugriff und Computer Standards festlegen** " von Windows 8 wird im folgenden Screenshot gezeigt.

![Screenshot der Eintrags Ansicht "Programm Zugriff und Computer Standards festlegen"](images/spad-initial.png)

Dem Benutzer werden drei mögliche Konfigurationsoptionen angezeigt, mit der Option, dass OEMs eine vierte Option mit dem Namen "Computer Hersteller" präsentieren können.

-   [Microsoft Windows](#microsoft-windows)
-   [Nicht von Microsoft](#non-microsoft)
-   [Benutzerdefiniert](#custom)
-   [Computerhersteller](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

Die **Microsoft Windows** -Konfiguration besteht aus einer Reihe von Standardprogrammen, die mit Windows bereitgestellt werden, wie im folgenden Screenshot gezeigt.

![Screenshot der Optionen zum Festlegen des Programm Zugriffs und der Standardeinstellungen von Microsoft](images/mspage.png)

Wenn Sie die **Microsoft Windows** -Konfiguration auswählen, können Sie auch die Symbole, Verknüpfungen oder Menüeinträge für jedes Programm anzeigen, das für einen der fünf Client Typen registriert ist. Diese Symbole, Verknüpfungen und Menüeinträge sind für den Benutzer im **Startmenü** oder auf dem Startbildschirm, auf dem Desktop und an allen anderen Speicherorten verfügbar, denen Sie hinzugefügt wurden.

### <a name="non-microsoft"></a>Nicht von Microsoft

Die **nicht-Microsoft-** Konfiguration, die im folgenden Screenshot gezeigt wird, wird für registrierte Anwendungen auf dem System des Benutzers verwendet, die nicht von Microsoft erstellt wurden. Diese Anwendungen können im System des Benutzers vorinstalliert werden, oder es kann sich um nicht von Microsoft erstellte Anwendungen handeln, die der Benutzer installiert hat.

> [!Note]  
> Anwendungen müssen sich registrieren, damit Sie auf dieser Seite angezeigt werden. Anweisungen zum Registrieren einer Anwendung finden Sie unter [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md).

 

![Screenshot der Optionen Set Program Access und defaults Non-Microsoft](images/nonmspage.png)

Wenn Sie die Option **nicht von Microsoft** auswählen, wird auch der Zugriff auf die Symbole, Verknüpfungen und Menüeinträge der Microsoft-Programme, die in der [Microsoft Windows](#microsoft-windows) -Konfiguration für alle Client Typen aufgeführt sind, aufgehoben. Diese Symbole, Verknüpfungen und Menüeinträge von Microsoft werden aus dem **Startmenü** , dem Desktop und anderen Speicherorten entfernt, denen Sie hinzugefügt wurden.

### <a name="custom"></a>Benutzerdefiniert

Die **benutzerdefinierte** Konfiguration, die im folgenden Screenshot gezeigt wird, ermöglicht es Benutzern, ihre Systeme mit einer beliebigen Kombination aus Microsoft-und nicht-Microsoft-Programmen anzupassen, die als Standard Möglichkeiten für die fünf Client Typen registriert sind. Dies ist die einzige der vier verfügbaren Optionen in Windows 2000 Service Pack 3 (SP3).

![Screenshot der benutzerdefinierten Optionen zum Festlegen des Programm Zugriffs und der Standardeinstellungen](images/custompage.png)

Alle Optionen, die in den [Microsoft Windows](#microsoft-windows) [-und nicht-Microsoft-](#non-microsoft) Konfigurationen angezeigt werden, sind für den Benutzer im Abschnitt **Benutzer** definiert sowie alle zusätzlich installierten Microsoft-Anwendungen, die nicht Teil von Windows sind, verfügbar. Das Optionsfeld **meinen aktuellen Webbrowser verwenden** ist vorab ausgewählt, wie im vorherigen Screenshot dargestellt. Es gibt keine Möglichkeit, den aktuellen Standardbrowser auf der Benutzeroberfläche zu ermitteln. Das Aufrufen von Weblinks oder Dateien in Windows ist die einzige Möglichkeit, den aktuellen Standardbrowser zu ermitteln.

Wenn ein Benutzer das Kontrollkästchen **Zugriff auf dieses Programm aktivieren** für ein Programm aktiviert, werden die Symbole, Verknüpfungen und Menüeinträge des Programms im Startmenü oder auf dem Startbildschirm, auf dem Desktop oder an einem anderen Speicherort angezeigt, an dem Sie installiert wurden. Wenn Sie diese Option deaktivieren, sollten Sie die Symbole, Verknüpfungen und Menüeinträge entfernen, aber die Art und Weise, wie sich diese Optionen Verhalten, ist für den Anwendungshersteller vollständig. Windows steuert nicht, wie der Zugriff auf der gesamten Benutzeroberfläche aktiviert oder entfernt wird. Es ist auch wichtig zu verstehen, dass Anwendungen nicht für das Festlegen des **Programm Zugriffs und der Standardeinstellungen des Computers** registriert werden müssen.

### <a name="computer-manufacturer"></a>Computerhersteller

Eine vierte Kategorie mit dem Namen "Computer Hersteller" kann auf einigen Systemen im SPAD-Fenster angezeigt werden. Computerhersteller können auswählen, ob Ihre Computer mit einem benutzerdefinierten Satz von Standardeinstellungen vorkonfiguriert werden sollen. dabei wählen Sie aus der Auswahl, die in der [benutzerdefinierten](#custom) Konfiguration verfügbar ist (Zu Veranschaulichung wird ein fiktiver Satz von Anwendungen namens Litware für die Verwendung mit allen Client Typen registriert.) Benutzer können jederzeit zur Standardkonfiguration des Computerherstellers zurückkehren, indem Sie die Option **Computerhersteller** auswählen, wie im folgenden Windows XP-Screenshot dargestellt.

> [!Note]  
> Diese Konfiguration wird nicht auf allen Systemen angezeigt. Weitere Informationen finden Sie in der OEM Preinstallation Kit (OPK).

 

![Screenshot der Optionen zum Festlegen des Programm Zugriffs und der Standardeinstellungen für Computerhersteller](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>Der Registrierungs Wert "lastuserinitiateddefaultchange"

Der Wert lastuserinitiateddefaultchange wurde der Registrierung hinzugefügt, um Anwendungen bei der Erkennung und Einhaltung der Standardoptionen des Benutzers zu unterstützen. Der-Wert enthält \_ binäre reg-Daten in Form einer [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, die das Datum und die Uhrzeit (in koordinierter Weltzeit (koordinierte Weltzeit)) der letzten Änderung der Standardauswahl über das Tool **Programm Zugriff und Computer Standards festlegen** enthält. Dieser Wert befindet sich unter dem folgenden Unterschlüssel.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

Im folgenden Szenario wird dieser Wert für eine Anwendung verwendet, die Dateizuordnungen überwacht.

1.  Eine Anwendung zeichnet die Zeit, zu der Sie zuletzt als Standardprogramm für Ihren Clienttyp festgelegt wurde (entweder bei der Installation oder zu einem späteren Zeitpunkt), auf.
2.  Die Anwendung erkennt, dass das Standardprogramm für den Clienttyp zu einem anderen Programm als sich selbst oder der Anwendung, die es darstellt (im Fall von background Helper-Programmen), geändert wurde. Wird nicht in Windows 8 unterstützt.
3.  Die Anwendung liest den Wert von lastuserinitiateddefaultchange (der Zeitstempel der letzten vom Benutzer initiierten Standardänderung) und vergleicht sie mit dem Zeitstempelwert, den Sie als Standardwert für die eigene Auswahl gespeichert hat.
4.  Wenn "lastuserinitiateddefaultchange" nach dem gespeicherten Wert der Anwendung liegt, sollte von dieser Anwendung keine Aktion ausgeführt werden, da die Änderung explizit vom Benutzer über das Tool " **Programm Zugriff und Standardeinstellungen festlegen** " angefordert wurde.
5.  Die Anwendung überwacht diese Datei Zuordnung nicht mehr, bis Sie erneut als Standard ausgewählt wird. Wird nicht in Windows 8 unterstützt.

Durch einhalten eines solchen Schemas werden die Wünsche des Benutzers respektiert, und der endgültige Besitz seiner Systeme bleibt erhalten.

## <a name="filtering-the-add-or-remove-programs-list"></a>Filtern der Liste "Software"

> [!Note]  
> Dieser Abschnitt gilt für Windows XP Service Pack 2 (SP2) und höher sowie Windows Server 2003 und höher.

 

In Windows XP und Windows Server **2003 kann die** Liste der Anwendungen, die auf der Registerkarte **Programme ändern oder entfernen** unter Software angezeigt werden, vom Benutzer gefiltert werden, um Einträge für Anwendungs Updates auszuschließen. In diesen Versionen von Windows wird dies mithilfe des Kontrollkästchens **Updates anzeigen** am oberen Rand des Fensters erreicht. Die Option **Updates anzeigen** ist standardmäßig nicht aktiviert, sodass Updates *nicht* angezeigt werden, es sei denn, der Benutzer wählt diese anzeigen aus. Änderungen am Kontrollkästchen Zustand bleiben erhalten, **Wenn "** Software" geschlossen wird. Wenn ein Benutzer die Aktualisierung anzeigt, wird er weiterhin angezeigt, bis der Benutzer das Kontrollkästchen deaktiviert.

> [!Note]  
> Das Windows XP SP2-Update selbst ist eine Ausnahme bei der Filterung. Sie wird immer unabhängig vom Kontrollkästchen angezeigt.

 

In Windows Vista und höher werden Anwendungs Updates auf einer separaten Seite in der Systemsteuerung angezeigt, die nur für Updates vorgesehen ist. Diese Seite wird angezeigt, wenn der Benutzer auf den Link **installierte Updates anzeigen** klickt. Es ist keine Benutzer auswählbare Option verfügbar, um Updates auf derselben Seite wie installierte Programme anzuzeigen. Trotz der Änderung der Benutzeroberfläche bleibt der Mechanismus für die Registrierung als Update für ein installiertes Programm mit dem in früheren Versionen von Windows identisch.

Microsoft-und nicht-Microsoft-Anwendungen, die die Windows Installer verwenden, müssen nichts weiter tun, damit Ihre Updates als Updates erkannt werden. Nicht-Microsoft-Anwendungen, die Windows Installer nicht verwenden, müssen bestimmte Werte in der Registrierung als Teil Ihrer Installation deklarieren, damit Sie als Update für ein vorhandenes Programm erkannt werden.

Im folgenden Beispiel wird veranschaulicht, welche Registrierungs Werte deklariert werden müssen, damit eine Installation als Update für ein vorhandenes Programm erkannt wird.

1.  Die übergeordnete Anwendung muss die Deinstallations Informationen in einem Unterschlüssel unter dem Unterschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall** hinzufügen. Weitere Informationen zur Verwendung des **Deinstallations** unter Schlüssels finden Sie im Thema zur [Installation](/previous-versions/ms997548(v=msdn.10)) .
2.  Bei jedem Update dieser übergeordneten Anwendung müssen auch die zugehörigen Informationen als Unterschlüssel des **Deinstallations** unter Schlüssels hinzugefügt werden. Dabei sollte eine bestimmte Benennungs Konvention Ihrer Wahl verwendet werden, und es wird versucht, potenzielle Konflikte mit anderen Programmen zu vermeiden. Die folgenden Konventionen sind als Unterschlüssel Namen von Microsoft für die Verwendung mit Windows-Updates reserviert.
    -   Ieupdate
    -   Oeupdate
    -   "KB", gefolgt von sechs Ziffern, z. b. "KB123456"
    -   "Q", gefolgt von sechs Ziffern, z. b. "Q123456"
    -   Sechs Ziffern, z. b. "123456"
3.  Zusätzlich zu den Standard Deinstallations Informationen, die für die übergeordnete Anwendung hinzugefügt wurden, müssen die Unterschlüssel für jedes Update zusätzlich zwei der folgenden drei Einträge enthalten. Ihre Werte sind vom Typ reg \_ SZ.
    -   Element **keyName**. Dieser Wert ist erforderlich. Dies ist der Name des unter Schlüssels, der in Schritt 1 deklariert wurde. Dadurch wird das Update mit dem Programm verknüpft.
    -   "Element **Display Name**". Dieser Wert ist erforderlich. Wenn kein unter **Schlüssel mit dem** Namen in "Element keyName" übereinstimmt, wird dieser Wert als Platzhalter-übergeordnetes Programm verwendet, das in "Software" angezeigt wird.
    -   **InstallDate**. Dieser Wert ist optional. Das Formular sollte zum `yyyymmdd` angeben des Datums verwendet werden. Dieses Datum wird für die **auf installierten** Informationen verwendet, die neben dem Eintrag des Updates in der Benutzeroberfläche angezeigt werden. Wenn kein **InstallDate** -Eintrag vorhanden ist, oder wenn dieser vorhanden ist, aber kein Wert zugewiesen ist, geschieht Folgendes:
        -   Andere Betriebssystemversionen als Windows Vista und Windows 7: Es werden keine **installierten** Informationen angezeigt.
        -   Windows Vista und höher: Es wird ein Standard Datum verwendet. Dies ist das Datum der letzten Änderung für alle Einträge unter dem Unterschlüssel dieses Updates. Dies ist normalerweise der Tag, an dem das Update der Registrierung hinzugefügt wurde. Da es sich jedoch um das Datum der letzten Änderung handelt, bewirkt jede nachfolgende Änderung an den Einträgen des unter Schlüssels, dass der Wert von "InstallDate" auf das Datum der Änderung geändert wird.

Das folgende Beispiel zeigt die entsprechenden Registrierungseinträge für ein Update für die Litware Deluxe-Anwendung.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Uninstall
                  LitWare
                     DisplayName = LitWare Deluxe
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\litware.exe" /uninstall
                  LitWare_Update123456
                     DisplayName = LitWare Deluxe Update 123456. Fixes printing problems.
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\Updates\123456.exe" /uninstall
                     ParentKeyName = LitWare
                     ParentDisplayName = LitWare Deluxe
                     InstallDate = 20050513
```

Nicht-Microsoft-Anwendungen, die nicht die entsprechenden Registrierungsinformationen bereitstellen, wie z. b. Updates, die vor der Verfügbarkeit dieser Option erstellt wurden, werden weiterhin normal in der Liste der installierten Programme angezeigt und nicht herausgefiltert.

Das Filtern von Updates in anderen Betriebssystemversionen als Windows Vista und Windows 7 ist normalerweise eine benutzergesteuerte Einstellung und sollte wie von Anwendungen beachtet werden. In einer Unternehmensumgebung können Administratoren jedoch steuern, ob Benutzer die Option zum Filtern von Updates über den DontGroupPatches-Registrierungs Wert erhalten, wie im folgenden Beispiel gezeigt.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               policies
                  Uninstall
                     DontGroupPatches = 0 or 1
```

Dieser Wert ist vom Typ "reg \_ DWORD" und wird wie folgt interpretiert.



| DontGroupPatches-Wert             | Bedeutung                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                  | Das Kontrollkästchen **Updates anzeigen** wird dem Benutzer angezeigt. Das Filtern hängt davon ab, ob der Benutzer dieses Kontrollkästchen aktiviert hat.                                                                                         |
| 1                                  | Das Kontrollkästchen **Updates anzeigen** wird aus der Benutzeroberfläche entfernt. Updates werden nicht in der Liste gefiltert. Dieser Wert wird im Grunde auf das Windows XP SP1-Verhalten zurückgesetzt, bevor die Funktion " **Updates anzeigen** " eingeführt wurde. |
| Der Eintrag "DontGroupPatches" ist nicht vorhanden. | Dies entspricht dem Festlegen des Werts auf 0 (null).                                                                                                                                                                       |



 

DontGroupPatches hat in Windows Vista und Windows 7 keine Auswirkung, wenn die Benutzeroberfläche kein Kontrollkästchen enthält und registrierte Updates immer gefiltert werden.

> [!Note]  
> Richtlinien werden nur von Administratoren festgelegt. Anwendungen sollten diesen Wert nicht ändern. Weitere Informationen zum Festlegen eines Registrierungs basierten Gruppenrichtlinie finden Sie unter [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page) oder [Windows Server Gruppenrichtlinie](/windows/deployment/deploy-whats-new).

 

## <a name="additional-resources"></a>Weitere Ressourcen

-   [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md)
-   [Installation](/previous-versions/ms997548(v=msdn.10))
-   [Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Dateizuordnungen](fa-best-practices.md)
</dt> <dt>

[Beispielszenario für Datei Zuordnung](fa-sample-scenarios.md)
</dt> <dt>

[Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher](vista-managing-defaults.md)
</dt> <dt>

[Standardprogramme](default-programs.md)
</dt> </dl>

 

 
