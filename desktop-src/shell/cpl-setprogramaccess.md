---
description: In diesem Thema wird das Feature Programmzugriff festlegen und Computerstandardeinstellungen (SpaD) in Systemsteuerung erläutert.
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: Festlegen von Programmzugriff und Computerstandard (SPAD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978749171366e3091738ac22c78e04cd92123a75d2288f7c83200ee8532d232c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861463"
---
# <a name="set-program-access-and-computer-defaults-spad"></a>Festlegen von Programmzugriff und Computerstandard (SPAD)

In diesem Thema wird das Feature **Programmzugriff und Computerstandardeinstellungen festlegen (SPAD)** in Systemsteuerung erläutert. SPAD befindet sich unter dem Element [Standardprogramme](default-programs.md) Systemsteuerung in Windows Vista und neueren Versionen von Windows. In Windows XP befindet es sich im Element **Software** und trägt den Titel **Programmzugriff festlegen und Standardwerte.**

> [!IMPORTANT]
> Dieses Thema gilt nicht für Windows 10. Die Funktionsweise von Standarddateizuordnungen hat sich in Windows 10 geändert. Weitere Informationen finden Sie im Abschnitt Änderungen an der Verarbeitung von **Standard-Apps durch Windows 10** in [diesem Beitrag.](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)

 

-   [Verwenden des Tools "Programmzugriff und Computerstandardeinstellungen festlegen"](#using-the-set-program-access-and-computer-defaults-tool)
    -   [Übersicht über festlegen des Programmzugriffs und der Computerstandardeinstellungen](#an-overview-of-set-program-access-and-computer-defaults)
    -   [Der Registrierungswert LastUserInitiatedDefaultChange](#the-lastuserinitiateddefaultchange-registry-value)
-   [Filtern der Liste "Programme hinzufügen oder entfernen"](#filtering-the-add-or-remove-programs-list)
-   [Weitere Ressourcen](#filtering-the-add-or-remove-programs-list)
-   [Zugehörige Themen](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>Verwenden des Tools "Programmzugriff und Computerstandardeinstellungen festlegen"

> [!Note]  
> Ab Windows 8 konfiguriert SPAD die Standardwerte pro Benutzer für den aktuellen Benutzer. Vor Windows 8 wird für SPAD die Standardwerte pro Computer festgelegt. Wenn vom Benutzer noch keine Standardeinstellung pro Benutzer konfiguriert wurde, fordert das System sie auf, einen Standardwert pro Benutzer festzulegen, anstatt auf einen Standardwert pro Computer zurückzusetzen. Es ist möglich, dass benutzerspezifische Standardwerte in Windows Vista und Windows 7 nie angezeigt wurden, wenn sie zuvor Standardwerte pro Benutzer festgelegt hatten, da die Standardwerte pro Benutzer in diesen Betriebssystemen die Standardwerte pro Computer überschreiben.

 

In Windows XP ist **Programmzugriff und Standardwerte festlegen** ein Tool, das als Option im Element **Software** Systemsteuerung gefunden wird. In Windows Vista und höher befindet es sich unter dem Element [Standardprogramme](default-programs.md) Systemsteuerung. Für [registrierte](reg-middleware-apps.md) Programme werden die folgenden Funktionen ausgeführt:

-   Ermöglicht die Auswahl von Standardprogrammen für jeden Clienttyp (nur bis zu Windows 7).
-   Ermöglicht die Steuerung der Anzeige der Symbole, Verknüpfungen und Menüeinträge des Programms.
-   Stellt eine Reihe vordefinierter Standardprogrammoptionen bereit. (nur Windows XP Service Pack 1 (SP1)

Dieses Tool wird für die folgenden fünf Clienttypen verwendet.

-   Browser
-   E-Mail
-   Programm zum sofortigen Messen
-   Media Player
-   Virtueller Computer für Java

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>Übersicht über festlegen des Programmzugriffs und der Computerstandardeinstellungen

Die Seite **Programmzugriff und Computerstandardeinstellungen festlegen** Windows 8 wird im folgenden Screenshot gezeigt.

![Screenshot der Einstellung des Programmzugriffs und der Standardeintragsansicht des Computers](images/spad-initial.png)

Dem Benutzer werden drei mögliche Konfigurationsoptionen angezeigt, mit der Option, dass OEMs eine vierte Option mit dem Titel "Computerhersteller" präsentieren können.

-   [Microsoft Windows](#microsoft-windows)
-   [Nicht-Microsoft](#non-microsoft)
-   [Benutzerdefiniert](#custom)
-   [Computerhersteller](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

Die **Microsoft Windows-Konfiguration** besteht aus einer Reihe von Standardprogrammen, die mit Windows bereitgestellt werden, wie im folgenden Screenshot gezeigt.

![Screenshot: Festlegen des Programmzugriffs und Standardmäßige Microsoft-Optionen](images/mspage.png)

Wenn Sie die **Microsoft Windows-Konfiguration** auswählen, wird auch die Anzeige der Symbole, Verknüpfungen oder Menüeinträge für jedes Programm aktiviert, das für einen der fünf Clienttypen registriert ist. Diese Symbole, Tastenkombinationen und Menüeinträge stehen dem Benutzer im **Startmenü** oder im Startbildschirm, auf dem Desktop und an allen anderen Speicherorten zur Verfügung, denen sie hinzugefügt wurden.

### <a name="non-microsoft"></a>Nicht-Microsoft

Die **Nicht-Microsoft-Konfiguration,** die im folgenden Screenshot gezeigt wird, wird für registrierte Anwendungen auf dem System des Benutzers verwendet, die nicht von Microsoft erstellt werden. Diese Anwendungen können auf dem System des Benutzers vorinstalliert werden, oder es kann sich um Nicht-Microsoft-Anwendungen handelt, die der Benutzer installiert hat.

> [!Note]  
> Anwendungen müssen registriert werden, damit sie auf dieser Seite angezeigt werden. Anweisungen zum Registrieren einer Anwendung finden Sie unter [Registrieren von Programmen bei Clienttypen.](reg-middleware-apps.md)

 

![Screenshot des festgelegten Programmzugriffs und Standardwerte für Nicht-Microsoft-Optionen](images/nonmspage.png)

Wenn Sie die Option **Nicht-Microsoft** auswählen, wird auch der Zugriff auf die Symbole, Verknüpfungen und Menüeinträge der Microsoft-Programme entfernt, die in der [Microsoft Windows-Konfiguration](#microsoft-windows) für alle Clienttypen mit diesen aufgeführt sind. Diese Microsoft-Symbole, Verknüpfungen und Menüeinträge werden aus dem **Startmenü,** dem Desktop und anderen Speicherorten entfernt, denen sie hinzugefügt wurden.

### <a name="custom"></a>Benutzerdefiniert

Mit der **benutzerdefinierten** Konfiguration, die im folgenden Screenshot gezeigt wird, können Benutzer ihre Systeme mit einer beliebigen Kombination von Microsoft- und Nicht-Microsoft-Programmen anpassen, die als Standardmöglichkeiten für die fünf Clienttypen registriert sind. Dies ist die einzige der vier Optionen, die in Windows 2000 Service Pack 3 (SP3) verfügbar sind.

![Screenshot: Festlegen des Programmzugriffs und Standardmäßige benutzerdefinierte Optionen](images/custompage.png)

Alle Optionen, die in den Microsoft [Windows-](#microsoft-windows) und [Nicht-Microsoft-Konfigurationen](#non-microsoft) angezeigt werden, stehen dem Benutzer im Abschnitt **Benutzerdefiniert** sowie alle zusätzlich installierten Microsoft-Anwendungen zur Verfügung, die nicht Teil Windows sind. Das Optionsfeld **Use my current web browser (Aktuellen Webbrowser** verwenden) ist vorab ausgewählt, wie im vorherigen Screenshot gezeigt. Es gibt keine Möglichkeit, den aktuellen Standardbrowser über die Benutzeroberfläche zu bestimmen. Das Aufrufen von Weblinks oder Dateien in Windows ist die einzige Möglichkeit, den aktuellen Standardbrowser zu ermitteln.

Wenn ein Benutzer das Kontrollkästchen **Zugriff auf dieses Programm aktivieren** für ein Programm aktiviert, werden die Symbole, Verknüpfungen und Menüeinträge dieses Programms im Startmenü oder Startbildschirm, auf dem Desktop oder an einem anderen Speicherort angezeigt, an dem sie installiert wurden. Wenn Sie diese Option deaktivieren, sollten diese Symbole, Verknüpfungen und Menüeinträge entfernt werden. Das Verhalten dieser Optionen liegt jedoch vollständig beim Anwendungsanbieter. Windows steuert nicht, wie der Zugriff auf der gesamten Benutzeroberfläche aktiviert oder entfernt wird. Es ist auch wichtig zu verstehen, dass Anwendungen nicht für **Programmzugriff festlegen und Computerstandardeinstellungen** registriert werden müssen.

### <a name="computer-manufacturer"></a>Computerhersteller

Eine vierte Kategorie mit dem Titel "Computerhersteller" kann auf einigen Systemen im SPAD-Fenster angezeigt werden. Computerhersteller können ihre Computer mit einem benutzerdefinierten Satz von Standardwerten vorkonfigurieren und dabei aus der gleichen Auswahl wählen, die in der [benutzerdefinierten](#custom) Konfiguration verfügbar ist. (Zur Veranschaulichung wird ein fiktiver Satz von Anwendungen namens LitWare für die Verwendung mit allen Clienttypen registriert.) Ein Benutzer kann jederzeit zur Standardkonfiguration des Computerherstellers zurückkehren, indem er die Option **Computerhersteller** auswählt, wie im folgenden Screenshot Windows XP gezeigt.

> [!Note]  
> Diese Konfiguration wird nicht auf allen Systemen angezeigt. Ausführliche Informationen finden Sie im OEM Preinstallation Kit (OPK).

 

![Screenshot: Festlegen des Programmzugriffs und Standardmäßige Computerherstelleroptionen](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>Der Registrierungswert LastUserInitiatedDefaultChange

Der Wert LastUserInitiatedDefaultChange wurde der Registrierung hinzugefügt, um Anwendungen bei der Erkennung und Einhaltung der Standardoptionen des Benutzers zu unterstützen. Der Wert enthält REG \_ BINARY-Daten in Form einer [**FILETIME-Struktur,**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) die das Datum und die Uhrzeit (in koordinierte Weltzeit (UTC)) des Zeitpunkts enthält, zu dem der Benutzer eine Standardauswahl über das Tool **Programmzugriff und Computerstandardwerte festlegen** geändert hat. Dieser Wert befindet sich unter dem folgenden Unterschlüssel.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

Im folgenden Szenario wird dieser Wert für eine Anwendung verwendet, die Dateizuordnungen überwacht.

1.  Eine Anwendung zeichnet intern den Zeitpunkt auf, zu dem sie zuletzt als Standardprogramm für ihren Clienttyp festgelegt wurde (entweder bei der Installation oder zu einem späteren Zeitpunkt).
2.  Die Anwendung erkennt, dass das Standardprogramm für ihren Clienttyp in ein anderes Programm als sich selbst oder die Anwendung geändert wurde, die es darstellt (im Fall von Hintergrundhilfsprogrammen). Wird nicht in Windows 8 unterstützt.
3.  Die Anwendung liest den Wert von LastUserInitiatedDefaultChange (den Zeitstempel der letzten vom Benutzer initiierten Standardänderung) und vergleicht ihn mit dem Zeitstempelwert, den sie für die eigene Auswahl als Standard gespeichert hat.
4.  Wenn LastUserInitiatedDefaultChange nach dem gespeicherten Wert der Anwendung liegt, sollte von dieser Anwendung keine Aktion ausgeführt werden, da die Änderung explizit vom Benutzer über das Tool **Programmzugriff und Standardwerte festlegen** angefordert wurde.
5.  Die Anwendung überwacht diese Dateizuordnung nicht mehr, bis sie wieder als Standard ausgewählt wird. Wird nicht in Windows 8 unterstützt.

Durch die Einhaltung eines solchen Schemas werden die Bedürfnisse des Benutzers berücksichtigt, und sein endgültiger Besitz an seinen Systemen wird beibehalten.

## <a name="filtering-the-add-or-remove-programs-list"></a>Filtern der Liste "Programme hinzufügen oder entfernen"

> [!Note]  
> Dieser Abschnitt gilt für Windows XP Service Pack 2 (SP2) und höher und Windows Server 2003 und höher.

 

In Windows XP und Windows Server 2003 kann die Liste der Anwendungen, die auf der Registerkarte **Programme ändern oder entfernen** unter **Software** angezeigt werden, vom Benutzer gefiltert werden, um Einträge für Anwendungsupdates auszuschließen. In diesen Versionen von Windows wird dies über das Kontrollkästchen **Updates anzeigen** am oberen Rand des Fensters erreicht. Die Option **Updates anzeigen** ist standardmäßig nicht aktiviert, sodass Updates *nur* angezeigt werden, wenn der Benutzer sie anzeigen möchte. Änderungen am Kontrollkästchenzustand bleiben erhalten, wenn **Software** geschlossen wird. Wenn ein Benutzer die Updates anzeigen möchte, wird er weiterhin angezeigt, bis der Benutzer das Kontrollkästchen löscht.

> [!Note]  
> Das Windows XP SP2-Update selbst ist eine Ausnahme bei der Filterung. Sie wird immer unabhängig vom Kontrollkästchenzustand angezeigt.

 

In Windows Vista und höher werden Anwendungsupdates auf einer separaten Seite in Systemsteuerung nur für Updates reserviert angezeigt. Diese Seite wird angezeigt, wenn der Benutzer auf den Task **Installierte Updates anzeigen klickt.** Es gibt keine vom Benutzer auswählbare Option zum Anzeigen von Updates auf der gleichen Seite wie installierte Programme. Trotz der Änderung der Benutzeroberfläche bleibt der Mechanismus für die Registrierung als Update für ein installiertes Programm unverändert wie in früheren Versionen von Windows.

Microsoft- und Nicht-Microsoft-Anwendungen, die den Windows Installer verwenden, müssen nichts weiter tun, damit ihre Updates als Updates erkannt werden. Nicht-Microsoft-Anwendungen, die nicht Windows Installer verwenden, müssen bestimmte Werte in der Registrierung als Teil ihrer Installation deklarieren, um als Update für ein vorhandenes Programm erkannt zu werden.

Das folgende Beispiel veranschaulicht, welche Registrierungswerte deklariert werden müssen, damit eine Installation als Update für ein vorhandenes Programm erkannt wird.

1.  Die übergeordnete Anwendung muss ihre Deinstallationsinformationen in einem Unterschlüssel unter dem **Unterschlüssel HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall** hinzufügen. Weitere Informationen [zur Verwendung](/previous-versions/ms997548(v=msdn.10)) des Unterschlüssels **Deinstallieren** finden Sie im Thema Installation.
2.  Jedes Update dieser übergeordneten Anwendung muss auch seine Informationen als Unterschlüssel des Unterschlüssels **Deinstallieren** hinzufügen. Es sollte eine bestimmte Benennungskonvention seiner Wahl verwenden, um potenzielle Konflikte mit anderen Programmen zu vermeiden. Die folgenden Konventionen sind von Microsoft als Unterschlüsselnamen für die Verwendung mit Windows reserviert.
    -   IEUpdate
    -   OEUpdate
    -   "KB" gefolgt von sechs Ziffern, z.B. "KB123456"
    -   "Q" gefolgt von sechs Ziffern, z.B. "Q123456"
    -   Sechs Ziffern, z. B. "123456"
3.  Zusätzlich zu den standardmäßigen Deinstallationsinformationen, die für die übergeordnete Anwendung hinzugefügt wurden, müssen die Unterschlüssel für jedes Update zusätzlich zwei der folgenden drei Einträge enthalten. Ihre Werte sind vom Typ REG \_ SZ.
    -   **ParentKeyName**. Dieser Wert ist erforderlich. Dies ist der Name des Unterschlüssels des übergeordneten Elements, der in Schritt 1 deklariert wurde. Dies ordnet das Update dem Programm zu.
    -   **ParentDisplayName**. Dieser Wert ist erforderlich. Wenn kein Unterschlüssel mit dem in ParentKeyName benannten entspricht, wird dieser Wert als übergeordnetes Platzhalterprogramm verwendet, das in Programme hinzufügen oder **entfernen angezeigt werden soll.**
    -   **InstallDate**. Dieser Wert ist optional. Sie sollte das Formular verwenden, `yyyymmdd` um das Datum anzugeben. Dieses Datum wird für die **Informationen installiert bei** verwendet, die neben dem Updateeintrag auf der Benutzeroberfläche angezeigt werden. Wenn kein **InstallDate-Eintrag** vorhanden ist oder wenn er vorhanden ist, ihm aber kein Wert zugewiesen ist, geschieht Folgendes:
        -   Andere Betriebssystemversionen als Windows Vista und Windows 7: **Es** werden keine Informationen unter Installiert angezeigt.
        -   Windows Vista und höher: Es wird ein Standarddatum verwendet. Dies ist das Datum der letzten Änderung für alle Einträge unter dem Unterschlüssel dieses Updates. Dies ist normalerweise der Tag, an dem das Update zur Registrierung hinzugefügt wurde. Da es sich jedoch um ein Datum der letzten Änderung handelt, bewirkt jede nachfolgende Änderung an den Einträgen des Unterschlüssels, dass der InstallDate-Wert in das Datum dieser Änderung geändert wird.

Das folgende Beispiel zeigt die relevanten Registrierungseinträge für ein Update der LitWare-Anwendung".

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

Nicht-Microsoft-Anwendungen, die nicht die entsprechenden Registrierungsinformationen liefern, z. B. Updates, die vor der Bereitstellung dieser Option erstellt wurden, werden weiterhin normal in der Liste der installierten Programme angezeigt und werden nicht herausgefiltert.

Die Updatefilterung in anderen Betriebssystemversionen als Windows Vista und Windows 7 ist normalerweise eine benutzergesteuerte Einstellung und sollte von Anwendungen als solche beachtet werden. In einer Unternehmensumgebung können Administratoren jedoch steuern, ob Benutzer die Option erhalten, Updates über den Registrierungswert DontGroupPatches zu filtern, wie im folgenden Beispiel gezeigt.

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

Dieser Wert ist vom Typ REG \_ DWORD und wird wie folgt interpretiert.



| DontGroupPatches-Wert             | Bedeutung                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                  | Das **Kontrollkästchen Updates** anzeigen wird dem Benutzer angezeigt. Die Filterung hängt davon ab, ob der Benutzer dieses Kontrollkästchen kontrollkästchent oder nicht.                                                                                         |
| 1                                  | Das **Kontrollkästchen Updates** anzeigen wird von der Benutzeroberfläche entfernt. Updates werden nicht aus der Liste gefiltert. Dieser Wert wird im Wesentlichen auf das xp Windows SP1-Verhalten zurückverwendet, bevor die Funktion **Updates** anzeigen eingeführt wurde. |
| Eintrag "DontGroupPatches" nicht vorhanden | Dies entspricht dem Festlegen des Werts auf 0.                                                                                                                                                                       |



 

DontGroupPatches hat in Windows Vista und Windows 7 keine Auswirkungen, wenn die Benutzeroberfläche kein Kontrollkästchen enthält und registrierte Updates immer gefiltert werden.

> [!Note]  
> Richtlinien werden nur von Administratoren festgelegt. Anwendungen sollten diesen Wert nicht ändern. Weitere Informationen zum Festlegen einer registrierungsbasierten Gruppenrichtlinie finden Sie [unter](/previous-versions/windows/desktop/Policy/group-policy-start-page) Gruppenrichtlinie oder Windows [Server Gruppenrichtlinie](/windows/deployment/deploy-whats-new).

 

## <a name="additional-resources"></a>Weitere Ressourcen

-   [Registrieren von Programmen mit Clienttypen](reg-middleware-apps.md)
-   [Installation](/previous-versions/ms997548(v=msdn.10))
-   [Konfigurieren von Programmen zum Hinzufügen/Entfernen mit Windows Installer](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Dateizuordnungen](fa-best-practices.md)
</dt> <dt>

[Beispielszenario für dateiassoz](fa-sample-scenarios.md)
</dt> <dt>

[Richtlinien zum Verwalten von Standardanwendungen in Windows Vista und höher](vista-managing-defaults.md)
</dt> <dt>

[Standardprogramme](default-programs.md)
</dt> </dl>

 

 
