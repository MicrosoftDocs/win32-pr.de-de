---
title: Szenarien des Programmkompatibilitäts-Assistenten für Windows 8
description: Szenarien des Programmkompatibilitäts-Assistenten für Windows 8
ms.assetid: C61BF746-63EE-4F4E-81D3-52947FD4954D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63fbd912e14ac682ffe820ad140b2cad6a487dfbac833aa419c53389a9339ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852596"
---
# <a name="program-compatibility-assistant-scenarios-for-windows-8"></a>Szenarien des Programmkompatibilitäts-Assistenten für Windows 8

## <a name="platforms"></a>Plattformen

**Clients–** Windows XP \| Windows Vista \| Windows 7 \| Windows 8  

## <a name="description"></a>Beschreibung

Der Programmkompatibilitäts-Assistent (Program Compatibility Assistant, PCA) ist ein Feature in Windows 8, mit dem Endbenutzer Desktop-Apps ausführen können, die für frühere Windows-Versionen entwickelt wurden. Windows 8 verfügt über eine hervorragende integrierte App-Kompatibilität, mit der Apps, die für Windows 7 oder frühere Windows-Versionen entwickelt wurden, automatisch für Windows 8 geeignet sind. Es gibt jedoch eine kleine Anzahl von Apps, die Probleme beim Ausführen ohne Eingriff haben können.

Wenn ein Benutzer eine App ausführt, verfolgt PCA die App und identifiziert alle Symptome bestimmter bekannter Kompatibilitätsprobleme in Windows 8. Wenn problemede Symptome erkannt werden, bietet es dem Benutzer die Möglichkeit, eine empfohlene Korrektur anzuwenden, mit der die App auf Windows 8 besser ausgeführt werden kann.

## <a name="scenarios"></a>Szenarien

Pca verfolgt Apps nach einer Reihe bekannter Kompatibilitätsprobleme in Windows 8. Die PCA verfolgt die Probleme, identifiziert die Fehlerbehebungen und stellt dem Benutzer ein Dialogfeld mit Anweisungen zum Anwenden einer empfohlenen Fehlerbehebung bereit. Der Benutzer kann sich dafür entscheiden, die empfohlenen Fehlerbehebungen anzuwenden oder nichts zu unternehmen und die Empfehlung abzubrechen. Wenn der Benutzer den Vorgang abbricht, wird diese App von DER PCA nicht mehr nachverfolgt.

PCA wendet in der Regel einen von drei Windows Kompatibilitätsmodi an: Windows XP SP3, Windows Vista SP2 oder Windows 7, je nachdem, wann das Programm (oder sein Setup) erstellt wurde. PCA verwendet die Attribute LINK \_ DATE und SUBSYSTEM VERSION des Programms sowie die Abschnitte TRUSTINFO und COMPATIBILITY des ausführbaren Dateimanifests, um zu bestimmen, welcher der Modi relevant ist, und wendet Windows XP SP3 (einschließlich Administratorberechtigungen), Windows Vista SP2 bzw. Windows 7 an. Ein Glossar am Ende des Dokuments enthält die einzelnen Kompatibilitätsmodi, die pca anwendet, und die zugehörige Beschreibung.

Für alle unten aufgeführten Szenarien verfolgt pca Apps ein zweites Mal nach, nachdem eine Korrektur angewendet wurde. Wenn die App auch nach dem Anwenden eines Kompatibilitätsfixes weiterhin auf die gleiche Weise fehlschlägt, wird die Korrektur vom PCA wie folgt zurückgesetzt. Die PCA beendet dann dauerhaft die Nachverfolgung der spezifischen App, bei der ein Fehler aufgetreten ist.

PcA verfolgt zwar viele potenzielle Probleme, aber nicht alle Probleme verursachen tatsächlich App-Fehler. Die PCA empfiehlt Korrekturen nur in Situationen, in denen eine hohe Wahrscheinlichkeit besteht, dass der App-Fehler auf Windows Kompatibilitätsgründen zurückzuführen ist. In den folgenden Abschnitten werden die einzelnen PCA-Szenarien erweitert, die in Windows 8 entwickelt wurden. In jedem Abschnitt werden das Problemszenario und die Empfehlungen beschrieben, die pca bietet, damit die App weiterhin ordnungsgemäß an Windows 8 funktioniert.

Weitere Informationen zu Kompatibilitätsänderungen in Windows 8 finden Sie in den anderen Themen im *Windows 8 Compatibility Cookbook*.

In den folgenden Szenarien verfolgt der PCA Korrekturen nach und empfiehlt diese:

-   App kann nicht installiert oder deinstalliert werden
-   App kann nicht mit einer meldung zur Windows Versionsprüfung ausgeführt werden
-   App kann aufgrund von Administratorrechten nicht gestartet werden
-   App stürzt aufgrund bestimmter Arbeitsspeicherprobleme ab
-   App schlägt aufgrund von nicht übereinstimmenden Systemdateien fehl
-   App-Fehler aufgrund von Nicht behandelten Fehlern auf 64-Bit-Windows
-   App schlägt fehl, wenn versucht wird, geschützte, nicht Windows Dateien zu löschen
-   App schlägt fehl, wenn versucht wird, Windows Dateien zu ändern
-   App-Fehler aufgrund der Verwendung von 8- oder 16-Bit-Farbmodi
-   App schlägt aufgrund von Grafik- und Anzeigeproblemen fehl
-   App kann DPI-Bekanntheit nicht deklarieren
-   App-Fehler aufgrund fehlender Windows Features
-   App-Fehler aufgrund von nicht signierten Treibern auf 64-Bit-Windows 8
-   Nachverfolgen von Apps, die über Kompatibilitätseinstellungen installiert wurden
-   App kann Installationsprogramme oder Updater nicht starten
-   App-Installer, die mit Administratorrechten ausgeführt werden müssen
-   Legacy-Systemsteuerung Applets, die mit Administratorrechten ausgeführt werden müssen

Jedes dieser Szenarien wird im Folgenden erweitert:

**App kann nicht installiert oder deinstalliert werden**

Einer der häufigsten Arten von App-Fehlern tritt während der Installation der App auf. Ältere Setupprogramme schlagen am häufigsten auf zwei Arten fehl:

-   Das Setupprogramm kennt die Features der Benutzerkontensteuerung (User Account Control, UAC) in Windows 8 nicht, sodass es möglicherweise nicht mit den vollständigen Berechtigungen ausgeführt wird, die erforderlich sind, um Systemänderungen an den geschützten Bereichen von Windows 8
-   Das Setupprogramm sucht nach der Windows Version und blockiert die Ausführung, wenn die Version höher als erwartet ist.

Diese Fehlerbedingungen sind zwei der häufigsten Arten von Kompatibilitätsfehlern beim Setup. PCA erkennt setup-Programme beim Start mithilfe verschiedener anderer Windows-Komponenten wie UAC und verfolgt sie bis zum Ende der Installation nach. Wenn das Setupprogramm dateien oder einen gültigen Eintrag im Teil "Software hinzufügen" der Windows Systemsteuerung nicht hinzufügen kann, betrachtet PCA das Setup als fehlgeschlagen.

In diesem Fall empfiehlt pca einen für die App geeigneten Kompatibilitätsmodus. Der Kompatibilitätsmodus ermöglicht die Ausführung des Setupprogramms im Windows Modus, für den es entwickelt wurde, und stellt außerdem sicher, dass die App mit Administratorrechten ausgeführt wird. PCA wendet den RUNASADMIN-Kompatibilitätsmodus zusammen mit dem entsprechenden Windows XP-, Windows Vista- oder Windows 7-Kompatibilitätsmodus an. Dem Benutzer wird am Ende der fehlgeschlagenen Installation ein Dialogfeld mit der PCA-Empfehlung angezeigt:

![Das Dialogfeld "App kann nicht installiert oder deinstalliert werden"](images/pcafigure1.png)

Der Benutzer kann dann Folgendes auswählen:

-   Führen Sie das Programm mithilfe der Kompatibilitätseinstellungen (empfohlene Option) aus. Danach wendet pca die empfohlene Einstellung an (Kompatibilitätsmodus), startet das Setupprogramm neu und verfolgt es nach, bis das Setup erfolgreich abgeschlossen ist.
-   Geben Sie an, dass das Programm ordnungsgemäß installiert wurde. In diesem Fall fügt pca keine Einstellungen hinzu und beendet die Nachverfolgung des Setups.
-   Klicken Sie auf Schließen. In diesem Fall fügt PCA keine Einstellungen hinzu und beendet die Nachverfolgung dieses Setups.

Der gleiche Mechanismus wird verwendet, um die Deinstallation der App zu unterstützen, wenn ein Benutzer versucht, die App entweder über den Abschnitt "Programme hinzufügen" in Windows oder über die Deinstallationsverknüpfung der App zu deinstallieren.

**App kann nicht mit einer meldung zur Windows Versionsprüfung ausgeführt werden**

Einer der häufigsten Kompatibilitätsfehler in der App-Runtime ist auf die Windows Versionsprüfung zurückzuführen. Viele Apps überprüfen beim Start die Windows Version. Wenn sie die Version nicht erkennen, blockieren sie sich selbst, auch wenn die App ohne Probleme ausgeführt werden konnte.

Im Allgemeinen sind solche Überprüfungen zwei Bedingungen zugeordnet, die von der PCA verfolgt werden:

Die App zeigt ein Meldungsfeld an, das den Benutzer warnt. Ein Beispiel finden Sie unten:

![Die App kann nicht mit einem Meldungsdialogfeld für die Windows-Versionsprüfung ausgeführt werden.](images/pcafigure2.png)

-   Die App wird sofort beendet oder stürzt ab.

Wenn pca beide Bedingungen für eine App identifiziert, gibt sie dem Benutzer eine Empfehlung. Pca ermöglicht dem Benutzer, die App mit Kompatibilitätseinstellungen erneut auszuführen. Pca wendet den entsprechenden kompatibilitätsbasierten Windows XP-, Windows Vista- oder Windows 7-Kompatibilitätsmodus basierend auf der App an. Wie in jedem der Szenarien kann der Benutzer pca mitteilen, dass die App ordnungsgemäß ausgeführt wurde, oder die empfohlenen Einstellungen deaktivieren, indem er auf die Schaltfläche "Schließen" klickt. Ein Beispieldialogfeld wird wie folgt bereitgestellt:

![app fails to run with a windows version check message option dialog (App kann nicht mit einer Meldungsoption für die Windows-Versionsprüfung ausgeführt werden)](images/pcafigure3.png)

**App kann aufgrund von Administratorrechten nicht gestartet oder ausgeführt werden**

Einige Apps benötigen Administratorrechte zum Ausführen und Ausführen ihrer Funktionen. In Windows 8, ähnlich wie Windows 7 und Windows Vista, werden Apps aufgrund von UAC jedoch standardmäßig in niedrigeren Berechtigungsstufen ausgeführt. Neuere Apps, die für Windows Vista und höher entwickelt wurden, deklarieren im Allgemeinen die Berechtigungsstufe, die sie für die Ausführung benötigen, im Abschnitt TRUSTINFO des EXE-Manifests. Ältere Apps schlagen jedoch in der Regel auf zwei Arten fehl:

-   Die App zeigt dem Benutzer eine Meldung an, dass administratorrechte erforderlich sind, wie im folgenden Beispiel dargestellt:

![App kann aufgrund von Administratorrechten nicht gestartet oder ausgeführt werden](images/pcafigure4a.png)

-   App wird entweder sofort beendet oder stürzt ab

Wenn pca beide Bedingungen für eine App identifiziert, gibt sie dem Benutzer eine Empfehlung. PCA ermöglicht dem Benutzer, die App mit Administratorrechten erneut auszuführen (PCA wendet den RUNASHIGHEST-Kompatibilitätsmodus an). Der Benutzer erhält eine UAC-Eingabeaufforderung, wenn die App erneut ausgeführt wird. Wie in jedem der Szenarien kann der Benutzer die empfohlene Einstellung erneut ausführen oder die empfohlenen Einstellungen deaktivieren, indem er auf Schließen klickt. Ein Beispieldialogfeld wird wie folgt bereitgestellt:

![app fails to launch or run due to administrative privilege option dialog (App kann aufgrund von Administratorrechten nicht gestartet oder ausgeführt werden)](images/pcafigure5.png)

**App stürzt aufgrund bestimmter Arbeitsspeicherprobleme ab**

Einige Apps stürzt aufgrund eines bekannten Arbeitsspeicherproblems ab. Die App dereferenziert eine DLL aus dem Arbeitsspeicher und ruft dann eine Funktion auf, um Code in derselben DLL auszuführen. Dies führt zu einem sofortigen Absturz der App. Obwohl dieses Problem nicht auf Windows 8 Kompatibilitätsänderungen zurückzuführen ist, ist es ein relativ häufiges Problem, das in einer Vielzahl von Apps auftritt. Pca verfolgt dieses Problem, um Benutzern die Möglichkeit zu geben, ihre App zuverlässiger auszuführen.

Für diese Apps wendet PCA automatisch den PINDLL-Kompatibilitätsmodus automatisch an. Der von PCA aufgerufene Kompatibilitätsmodus verhindert, dass die App die DLL aus dem Arbeitsspeicher freisetzt. Der Funktionsaufruf der DLL durch die App funktioniert also, sodass die App nicht abstürzt und weiterhin ordnungsgemäß funktioniert.

**App schlägt aufgrund von nicht übereinstimmenden Systemdateien fehl**

Einige Apps, die für Windows XP und früher entwickelt wurden, enthalten Kopien von Windows System-DLLs zusammen mit ihren Installationsprogrammen. Wenn solche Apps installiert sind, enthält die App sowohl eine ältere Kopie der DLL in ihrem eigenen Ordner als auch die neueste Version der DLL, die sich in den Windows Systemordnern befindet.

Auf Windows Vista und höher kann diese Bedingung dazu führen, dass die App fehlschlägt, wenn sie versucht, die lokale DLL zu laden, da diese DLL nicht gut mit den übrigen aktuellen Windows System-DLLs funktioniert. Da die App die neueren Versionen dieser DLL im Allgemeinen nicht kennt, funktioniert sie nicht ordnungsgemäß.

Wenn pca erkennt, dass die DLL nicht ordnungsgemäß geladen werden konnte, wird eine Kompatibilitätseinstellung angewendet, die es Windows ermöglicht, die neueste Version der DLL aus dem Windows Systemordner zu laden, damit die App ordnungsgemäß ausgeführt werden kann.

Am Ende der ersten fehlerhaften Ausführung der App wird den Benutzern das PCA-Dialogfeld angezeigt, in dem sie wie folgt über die angewendete Einstellung benachrichtigt werden:

![App schlägt aufgrund eines nicht übereinstimmenden Dialogfelds für Systemdateien fehl](images/pcafigure6.png)

**App-Fehler aufgrund von Nicht behandelten Fehlern auf 64-Bit-Windows**

Bei der 64-Bit-Version von Windows 8 wurde eine neue Ausnahme für den Rückrufmechanismus der Nachrichtenschleife aktiviert. Obwohl diese Ausnahme erstmals in Windows 7 eingeführt wurde, war es nicht zwingend erforderlich, diesen Fehler zu behandeln. In Windows 8 müssen Apps, die Nachrichtenschleifen verwenden, diese neue Ausnahme behandeln. Wenn dies nicht dere ist, werden sie abgestürzt. Apps, die für ältere Windows Versionen entwickelt wurden, kennen diese Ausnahme möglicherweise nicht und behandeln diesen Fehler (Ausnahme) möglicherweise nicht ordnungsgemäß.

PCA erkennt Apps, die aufgrund dieses nicht behandelten Fehlers fehlschlagen, und wendet automatisch den KOMPATIBILITÄTsmodus DISABLEUSERCALLBACKEXCEPTION für die App an. Nachdem die Einstellung am Ende der Ausführung angewendet wurde, wird der Benutzer wie folgt benachrichtigt. Die App erhält den Modus bei der nächsten Ausführung und kann diesen Fehler vermeiden.

![app fails due to unhandled errors on 64-bit windows dialog (App-Fehler aufgrund nicht behandelter Fehler im 64-Bit-Fensterdialogfeld)](images/pcafigure7.png)

**App schlägt fehl, wenn versucht wird, geschützte, nicht Windows Dateien zu löschen**

Einige Apps, die für Windows XP entwickelt wurden und früher davon ausgehen, dass sie in der Regel mit vollständigen Administratorrechten ausgeführt werden. Im Rahmen des normalen App-Verhaltens versuchen sie möglicherweise, geschützte, nicht Windows Dateien zu löschen (entweder in Programmdateien oder Windows Ordnern). Wenn der Löschvorgang fehlschlägt, können viele solche Apps abstürzten.

Pca erkennt diese Apps, die geschützte Dateien nicht löschen und abstürzt, und gibt dem Benutzer eine Empfehlung. Pca ermöglicht dem Benutzer, die App mit Kompatibilitätseinstellungen erneut auszuführen. Wie in jedem der Szenarien kann der Benutzer pca mitteilen, dass die App ordnungsgemäß ausgeführt wurde, oder die empfohlenen Einstellungen deaktivieren, indem er auf die Schaltfläche "Schließen" klickt. In diesem Fall wendet PCA den VIRTUALIZEDELETE-Kompatibilitätsmodus an. Ein Beispieldialogfeld wird wie folgt bereitgestellt:

![app fails while attempting to delete protected non-windows files dialog (App schlägt fehl, wenn versucht wird, geschützte Nicht-Windows-Dateien zu löschen)](images/pcafigure8.png)

**App schlägt fehl, wenn versucht wird, Windows Dateien oder Registrierungsschlüssel zu ändern**

Einige Apps, die für Windows XP entwickelt wurden und früher davon ausgehen, dass sie in der Regel mit vollständigen Administratorrechten ausgeführt werden. Im Rahmen des normalen App-Verhaltens können sie versuchen, Windows geschützten Dateien (entweder in Programmdateien oder Windows Ordnern) oder Registrierungsschlüssel im Besitz von Windows zu ändern, zu löschen oder zu schreiben. Wenn ein Schreib-, Lösch- oder Änderungsvorgang für eine Datei oder einen Registrierungsschlüssel fehlschlägt, können viele solche Apps abstürzt oder fehlerhaft sein.

Pca erkennt diese Apps, die nicht in geschützte Windows Dateien oder Registrierungsschlüssel schreiben können, und gibt dem Benutzer eine Empfehlung, wenn die App beendet wird. Pca ermöglicht dem Benutzer, die App mit Kompatibilitätseinstellungen erneut auszuführen. Wie in jedem der Szenarien kann der Benutzer pca mitteilen, dass die App ordnungsgemäß ausgeführt wurde, oder die empfohlenen Einstellungen deaktivieren, indem er auf die Schaltfläche Schließen klickt. In diesem Fall wendet PCA den WRPMITIGATION-Kompatibilitätsmodus an. Ein Beispieldialogfeld wird wie folgt bereitgestellt:

![app fails while attempting to modify windows files or registry keys dialog (App schlägt beim Ändern von Windows-Dateien oder Registrierungsschlüsseln fehl)](images/pcafigure9.png)

**App-Fehler aufgrund der Verwendung von 8- oder 16-Bit-Farbmodi**

Im Rahmen der Neuinsagierung Windows 8 für Windows Store-Apps ist eine der wichtigsten Änderungen, dass die Desktopfenster-Manager (DWM) jetzt nur 32-Bit-Farben in Windows 8 unterstützt. Niedrigere Farbmodi werden jetzt simuliert.

Viele ältere Apps und Spiele, die für Windows XP oder vor entwickelt wurden, verwenden 8-Bit- oder 16-Bit-Farbmodi. Ohne Risikominderung können diese Apps auf Windows 8 nicht ausgeführt werden. Wenn diese Apps jedoch einen der 8-Bit- oder 16-Bit-Farbmodi für die Anzeige auflisten oder zu verwenden versuchen, identifiziert PCA sofort das Problem und stellt mithilfe von DWM sicher, dass die App ordnungsgemäß mit dem simulierten Farbmodus funktioniert.

Beachten Sie, dass dies geschieht, sobald die App die Modi mit niedriger Farbe anfordert und für den Benutzer transparent ist. Der Benutzer muss die App nicht neu starten, um diese Lösung zu erhalten, da diese Korrektur immer erforderlich ist, um sicherzustellen, dass die App ordnungsgemäß funktioniert.

**Anwendung schlägt aufgrund von Grafik- und Anzeigeproblemen fehl**

Da Desktopfenster-Manager (DWM) in Windows 8 immer aktiviert ist, können einige ältere Apps aus Windows XP-Zeit fehlschlagen, wenn die App Grafik-APIs im gemischten Modus verwendet, wie bei der Verwendung von GDI- und DirectX-APIs zum Zeichnen auf dem Bildschirm (meist ältere Spiele) und versucht, den Vollbildmodus zu verwenden:

-   DWM verhindert das direkte Zeichnen auf dem Desktop, und das Spiel oder die App schlägt entweder fehl, oder es wird ein schwarzer Bildschirm auf dem Desktop gezeichnet, und keine der Grafiken ist sichtbar.
-   Wenn die App beendet wird, erkennt Windows in solchen Fällen, dass die App oder das Spiel ein Problem mit dem Vollbildmodus hat, und wendet den DXMAXIMIZEDWINDOWEDMODE-Kompatibilitätsmodus an, der die Ausführung der App oder des Spiels in einem maximierten Fenstermodus anstelle eines Vollbildmodus ermöglicht.
-   Nachdem die Einstellung am Ende der Ausführung angewendet wurde, wird der Benutzer wie unten gezeigt per PCA benachrichtigt. Die App erhält bei der nächsten Ausführung den Kompatibilitätsmodus und kann ordnungsgemäß ausgeführt werden.

![Anwendung schlägt aufgrund von Grafik- und Anzeigeproblemen fehl](images/pcafigure10.png)

**App kann DPI-Bekanntheit nicht deklarieren**

Ein weiteres typisches Anzeigeproblem bei vielen älteren Apps tritt auf, wenn Windows und die App im Modus mit hohem DPI-Wert ausgeführt wird, die App jedoch nicht über ihr EXE-Manifest ihr Bewusstsein für hohe DPI deklariert. Zu den häufigen Problemen, die aufgrund dieses Konflikts in den Einstellungen auftreten können, gehören beschnittene Benutzeroberflächenelemente oder Text und ein falscher Schriftgrad. Weitere Informationen zu den Problemen finden Sie unter diesem [Link.](/previous-versions//dd464660(v=vs.85))

In solchen Fällen erkennt Windows, dass die App einen hohen DPI-Wert erkennt, und wendet den HIGHDPIAWARE-Kompatibilitätsmodus am Ende der ersten Ausführung auf die App an. Die PCA informiert den Benutzer dann wie unten gezeigt darüber:

![app fails to declare dpi awareness dialog (Dialogfeld zur DPI-Erkennung nicht deklarieren)](images/pcafigure11.png)

**Fehler bei der Anwendung aufgrund fehlender Windows Features**

Einige Apps sind von Windows Features abhängig, die seit Windows Vista entfernt wurden. Wenn diese Apps versuchen, die fehlenden DLLs oder COM-Komponenten zu laden, funktionieren sie nicht.

Die PCA erkennt Apps, wenn sie versuchen, die fehlenden Windows Features zu laden, und bietet eine Empfehlung, diese Komponenten herunterzuladen und zu installieren, nachdem die App beendet wurde. Der Benutzer kann auf "Hilfe online abrufen" klicken, um entweder eine Alternative zu finden oder das Feature herunterzuladen und zu installieren. Bei Bedarf kann der Benutzer nichts tun, indem er auf Schließen klickt.

![Anwendung schlägt aufgrund fehlender Windows-Features fehl](images/pcafigure12.png)

**App-Fehler aufgrund von nicht signierten Treibern auf 64-Bit-Windows 8**

64-Bit-Windows verfügt seit Windows Vista über erforderliche digital signierte Treiber (SYS-Dateien). Ältere Apps, die vor der Veröffentlichung von Windows Vista entwickelt wurden, lieferten jedoch Treiber, die nicht digital signiert wurden. Wenn ein solcher Treiber ohne Vorzeichen installiert ist, werden sie von Windows nicht geladen. In seltenen Fällen ist es möglich, dass Windows nicht gestartet wird, wenn diese Treiber als Startzeittreiber markiert sind.

Einige ältere Apps installieren Treiber, die nicht auf 64-Bit-Windows signiert sind. Alle Geräte oder Apps, die versuchen, diesen Treiber zu verwenden, können fehlschlagen oder zu einem Systemabsturz führen. Um ein solches Szenario zu verhindern, erkennt PCA Apps, wenn sie nicht signierte Treiber installieren, und deaktiviert den Treiber, der als Startzeittreiber markiert ist.

Außerdem wird der Benutzer angewiesen, einen digital signierten Treiber zu erwerben, damit die App ordnungsgemäß funktioniert. Die Meldung wird als Ergebnis der Installation des Treibers und als Ergebnis der Installation der App angezeigt. Wenn eine andere App denselben Treiber installiert, erhält diese App auch die gleiche Meldung.

![app fails due to unsigned drivers on 64-bit windows 8 dialog (App schlägt aufgrund von nicht signierten Treibern im 64-Bit-Dialogfeld von Windows 8 fehl)](images/pcafigure13.png)

**Nachverfolgen von Apps, die über Kompatibilitätseinstellungen installiert wurden**

Wenn ein Installationsprogramm ausfällt, unterstützt PCA das Installationsprogramm je nach Art des Fehlers mit verschiedenen Kompatibilitätsmodi. Sobald das Installationsprogramm mit kompatibilitätseinstellungen erfolgreich ausgeführt wurde, verfolgt pca die Verknüpfungen nach, die das Installationsprogramm hinzugefügt hat. Dadurch wird nachverfolgt, ob die installierten Apps möglicherweise auch die Kompatibilitätseinstellungen benötigen, die auf das Installationsprogramm angewendet werden.

Wenn ein Benutzer eine solche App startet, fordert PCA den Benutzer auf, zu fragen, ob die App ordnungsgemäß funktioniert hat. Wenn der Benutzer die Antwort "Ja" gibt, beendet die PCA die Nachverfolgung der App. Wenn der Benutzer "Nein" beantwortet, wendet er den gleichen Kompatibilitätsmodus an, der auf das Installationsprogramm der App angewendet wurde, und führt die App mit dem angewendeten Kompatibilitätsmodus erneut aus.

**App kann Installationsprogramme oder Updater nicht starten**

Apps starten manchmal untergeordnete Programme, die als Administratoren ausgeführt werden müssen. Dies ist in der Regel der Fall, wenn eine App versucht, ihre Updatersoftware zu starten, um neue Updates für die App zu überprüfen und zu installieren. Wenn Apps solche untergeordneten Programme direkt ausführen, kann das untergeordnete Programm nicht gestartet werden, weil die App selbst nicht über Administratorrechte verfügte oder weil das untergeordnete Programm nicht ordnungsgemäß für erhöhte Rechte mit dem UAC-Manifest markiert wurde.

PCA verfolgt diese Fehler nach, und wenn die primäre App geschlossen wird, wird automatisch der ELEVATECREATEPROCESS-Kompatibilitätsmodus angewendet, der die ordnungsgemäße Ausführung der untergeordneten Programme unterstützt. Wenn die App die untergeordnete App bei nachfolgenden Ausführungen startet, wird dem Benutzer ein UAC-Dialogfeld für das untergeordnete Programm angezeigt.

Ein Beispiel für das PCA-Dialogfeld ist unten dargestellt:

![App kann das Dialogfeld "Installationsprogramme oder Updater" nicht starten](images/pcafigure14.png)

**App-Installer, die mit Administratorrechten ausgeführt werden müssen**

Installationsprogramme von Windows Desktop-Apps erfordern Administratorrechte, da sie Dateien, Ordner und Registrierungseinträge in geschützte Systembereiche schreiben. Windows (UAC) verfügt über Erkennungslogik, um zu ermitteln, wann ein Installationsprogramm ausgeführt wird, und fordert den Benutzer sofort auf, Administratorrechte über das UAC-Dialogfeld bereitzustellen. In einigen Fällen kann diese Logik jedoch nicht feststellen, dass eine App tatsächlich ein Installationsprogramm war, und erhält möglicherweise keine Administratorrechte. Dies sind im Allgemeinen benutzerdefinierte Installationsprogramme, die keine bekannten Installationstechnologien wie Windows Installer oder Install Shield verwenden.

In solchen Fällen erkennt pca, dass das Installationsprogramm seine Dateien nicht schreiben konnte. Wenn bei der Installation ein Fehler aufgetreten ist, wird vom PCA eine Empfehlung zum Anwenden von Kompatibilitätseinstellungen angezeigt. Wenn der Benutzer auf "Programm ausführen" klickt, wendet PCA den RUNASADMIN-Kompatibilitätsmodus an und führt das Installationsprogramm erneut aus. Wenn sich der Benutzer für das Schließen entscheidet, wird keine Einstellung angewendet. Im Folgenden finden Sie ein PcA-Beispieldialogfeld:

![Screenshot: Beispiel für ein Dialogfeld für ein App-Installationsprogramm, das mit Administratorrechten ausgeführt werden muss](images/pcafigure15.png)

Legacy-Systemsteuerung Applets, die mit Administratorrechten ausgeführt werden müssen, ändern in der Regel Systemeinstellungen und benötigen die Möglichkeit, Ad-Administrator auszuführen. Diejenigen, die vor Windows Vista geschrieben wurden, verfügen jedoch entweder nicht über ein EXE-Manifest oder nicht über den TRUSTINFO-Abschnitt, der die erforderliche Berechtigungsstufe deklariert. Wenn solche Applets ausgeführt werden, erkennt pca sie und gibt am Ende der ersten Ausführung eine Empfehlung zur Ausführung mit Administratoreinstellungen an. Wenn der Benutzer auf "Programm ausführen" klickt, wendet PCA den RUNASADMIN-Kompatibilitätsmodus an und führt das Installationsprogramm erneut aus. Wenn sich der Benutzer für das Schließen entscheidet, werden keine Einstellungen angewendet. Im Folgenden finden Sie ein PcA-Beispieldialogfeld:

![App-Installer, die mit Administratorrechten ausgeführt werden müssen](images/pcafigure16.png)

**Überprüfen der empfohlenen Einstellungen durch Benutzerfeedback**

Am Ende jedes Szenarios (nachdem die App mit empfohlenen Kompatibilitätseinstellungen ausgeführt wurde) stellt PCA dem Benutzer eine einfache Frage:

![Überprüfen der empfohlenen Einstellungen über das Dialogfeld "Benutzerfeedback"](images/pcafigure17.png)

Der Benutzer kann Feedback geben, wenn die App mit der Kompatibilitätseinstellung funktioniert hat oder fehlgeschlagen ist. Diese Daten werden anonym an Microsoft gesendet. Dadurch wird sichergestellt, dass solche Fehlerbehebungen über Windows Updateprozess in Windows 8 integriert werden können, sodass zukünftige Benutzer von Windows 8 nicht mehr auf den App-Fehler stoßen und die PCA die App nicht mehr auf den Fehler nachverfolgen muss.

**Nachverfolgen von Problemen ohne Empfehlungen**

Apps können aus Kompatibilitätsgründen auf viele verschiedene Arten ausfallen. PCA verfolgt viel mehr Kompatibilitätsprobleme als in den obigen Szenarien aufgeführt. In diesen Fällen hängt das Problem häufig von der App ab. Dies bedeutet, dass einige Apps solche Probleme ordnungsgemäß behandeln und daraus wiederherstellen, während andere dies möglicherweise nicht tun. Bei solchen Problemen bietet pca zwar weiterhin die App, aber keine direkte Empfehlung für eine Behebung.

Zu den Problemen, die pca verfolgt, die keine empfohlene Einstellung oder kein Dialogfeld aufweisen, gehören Apps, die:

-   Sehr kurze Laufzeit: Apps werden nicht länger als drei Sekunden ausgeführt.
-   Erstellen von globalen Speicherobjekten ohne Administratorrechte
-   Fehler (Win32-Ausnahme) beim Start
-   Überprüfen auf Administratorrechte (aber möglicherweise nicht fehlgeschlagen)
-   Verwenden von Indeo-Codecs (veraltet ab Windows Vista)
-   Versuchen Sie, Schlüssel aus geschützten Registrierungsspeicherorten wie HKLM zu schreiben oder zu löschen.
-   Absturz beim Start

**Anwenden von Fehlerbehebungen über die Registerkarte "Kompatibilität" und "Kompatibilitätsproblembehandlung"**

Wie bereits erwähnt, können Apps aus verschiedenen Kompatibilitätsgründen fehlschlagen. Nicht alle haben eine klare PCA-Empfehlung, da die Einstellungen von der App abhängig sind. Benutzer können jedoch zur Kompatibilitätsproblembehandlung oder zur Registerkarte Kompatibilität wechseln, um bestimmte allgemeine Fehlerbehebungen anzuwenden, um zu versuchen, ihre fehlerhafte App ordnungsgemäß auf Windows 8 zu bearbeiten. In solchen Fällen verfolgt die PCA die App weiterhin auf Kompatibilitätsprobleme nach, bevor und nachdem die Korrektur angewendet wurde. Nachdem die App mit angewendeter Korrektur ausgeführt wurde, fragt pca den Benutzer, ob die Korrektur funktioniert hat. Nachdem der Benutzer die Frage beantwortet hat, werden die Daten anonym über Telemetriedaten an Microsoft gesendet. Diese Daten werden von vielen Benutzern gesammelt und analysiert, und die qualifizierenden Fehlerbehebungen werden dann über Windows Update auf alle Windows 8 Benutzer verteilt.

**Verwenden der Kompatibilitätsproblembehandlung**

Die Kompatibilitätsproblembehandlung ist ein Mechanismus in Windows, mit dem Sie Probleme mit Apps diagnostizieren und empfohlene Fehlerbehebungen anwenden können, damit sie ordnungsgemäß funktionieren. Dies ist nur erforderlich, wenn pca keine Empfehlung für die App bereitstellen soll.

Mit der Problembehandlung können Benutzer eine Reihe von Fragen durchlaufen und beantworten. Basierend auf den Antworten wenden sie eine Reihe von Fehlerbehebungen an und ermöglichen es den Benutzern, ihre Apps zu testen und die Fehlerbehebungen zu überprüfen. Nach der Überprüfung werden die Fehlerbehebungen dauerhaft auf die Apps angewendet, damit sie bei Windows 8 besser funktionieren.

Die Problembehandlungsbenutzeroberfläche wird unten als Referenz angezeigt:

![Verwenden des Dialogfelds "Kompatibilitätsproblembehandlung"](images/pcafigure18.png)

Sie können die Kompatibilitätsproblembehandlung auf zwei Arten starten:

**Auf dem Startbildschirm:**

1.  Typ: Kompatibilitätsproblembehandlung
2.  Klicken Sie im Abschnitt "Einstellungen" auf die Kachel "Programme für vorherige Version von Windows ausführen".

  
**Über die App-Kachel:**

1.  Klicken Sie im Startbildschirm mit der rechten Maustaste auf die App-Kachel.
2.  Klicken Sie auf "Dateispeicherort öffnen" (nur Desktop-Apps).
3.  Klicken Sie im Menüband Explorer auf die Registerkarte "App".
4.  Wählen Sie "Problembehandlung bei der Kompatibilität" aus.

  


**Verwenden der Registerkarte "Kompatibilität"**

Beachten Sie, dass dies nur für Benutzer empfohlen wird, die Experten sind, die verschiedene Kompatibilitätseinstellungen ausprobieren. Diese Methode bietet keine Empfehlung für den Typ der Fehlerbehebung, die auf Apps angewendet werden soll. Hier muss der Benutzer wissen, welche Korrekturen angewendet werden können, damit die App funktioniert. Wenn Sie sich über die Fehlerbehebungen nicht sicher sind, verwenden Sie die Kompatibilitätsproblembehandlung, um eine Lösung für die App zu finden.

So greifen Sie auf die Registerkarte Kompatibilität zu:

 **Auf dem Startbildschirm:**

1.  Klicken Sie mit der rechten Maustaste auf die App-Kachel.
2.  Dateispeicherort öffnen (nur Desktop-Apps)

  
**Über das Menüband Explorer:**

1.  Klicken Sie auf Eigenschaften.
2.  Navigieren Sie zur Registerkarte Kompatibilität.
3.  Auswählen der Kompatibilitätskorrekturen
4.  Erneutes Ausführen der App
    > [!Note]  
    > Sie können wieder an den gleichen Ort zurückkehren, um die Fehlerbehebungen ebenfalls zu ändern oder zu entfernen. Sie können die Fehlerbehebungen auch auf alle Benutzer auf dem Computer anwenden, indem Sie die Schaltfläche auf der Registerkarte verwenden.

     

  


![mithilfe der Registerkarte "Kompatibilität"](images/pcafigure19.png)

**Apps mit bekannten Kompatibilitätsproblemen**

Neben den oben aufgeführten Szenarien zur Erkennung von Laufzeitproblemen informiert pca Benutzer beim Start der App auch, wenn die App bekannte Kompatibilitätsprobleme auflistet. Die Liste wird in der Kompatibilitätsdatenbank der System-App gespeichert. Es gibt zwei Arten von Nachrichten:

-   **Hartblockmeldungen:** Wenn bekannt ist, dass die App inkompatibel ist und die Ausführung der App zu schwerwiegenden Auswirkungen auf das System führt (z. B. ein Windows Absturz oder der Start nach der Installation nicht möglich ist), wird eine Blockierungsmeldung wie unten dargestellt angezeigt.

![Apps mit bekannten Kompatibilitätsproblemen – Dialogfeld "Meldungen mit harter Blockierung"](images/pcafigure20.png)

-   **Soft Block Messages**: Wenn die App über ein bekanntes Kompatibilitätsproblem verfügt und möglicherweise nicht ordnungsgemäß funktioniert, wird die folgende Meldung angezeigt:

![Apps mit bekannten Kompatibilitätsproblemen – Dialogfeld "Softblocknachrichten"](images/pcafigure21.png)

In beiden Fällen sendet die Option "Hilfe online abrufen" einen Windows Fehlerbericht, um eine Onlineantwort von Microsoft zu erhalten und dem Benutzer anzuzeigen. In der Regel verweisen die Antworten den Benutzer auf einen von drei Arten von Ressourcen:

-   Ein Update des App-Anbieters
-   Website eines App-Anbieters für weitere Informationen
-   Weitere Informationen finden Sie in einem Microsoft Knowledge Base-Artikel.

**Telemetrie für PCA**

Nachdem pca alle App-Probleme auf einem Windows 8 Computer behoben und das gesamte Benutzerfeedback erhalten hat, sammelt sie anonyme Daten über die App, das Installationsprogramm, die erkannten Probleme und die auf die App angewendeten Kompatibilitätseinstellungen und sendet sie zurück an Microsoft. Diese Daten werden von jedem Benutzer gesammelt, der bereit ist, solche anonymen Daten bereitzustellen (über die Programm zur Verbesserung der Benutzerfreundlichkeit – CEIP). Sobald diese Daten gesammelt wurden, werden die Fehler und Fehlerbehebungen der App analysiert, und die Fehlerbehebungen werden dann über den Windows Updatemechanismus an das gesamte Windows Ökosystem verteilt, sodass alle Benutzer der App in Zukunft automatisch von der Korrektur profitieren.

**Administrative Steuerungen und Verwalten von PCA-Einstellungen**

IT-Administratoren können das PCA-Verhalten auf zwei Arten steuern:

-   **PCA deaktivieren:** Mit dieser Einstellung können IT-Administratoren die Dialoge deaktivieren, die der PCA den Benutzern anzeigt. PCA verfolgt weiterhin Probleme und erkennt sie und sendet Telemetriedaten zurück.
-   **App-Telemetrie deaktivieren:** Diese Einstellung deaktiviert jegliche Erfassung und das Senden von Telemetriedaten per PCA.
    > [!Note]  
    > Wenn CEIP deaktiviert ist, hat diese Einstellung keine Auswirkungen.

     

**Entwerfen von Apps für die Arbeit mit PCA**

Entwickler müssen sicherstellen, dass ihre Apps in allen oben beschriebenen Kompatibilitätsszenarien gut funktionieren. Entwickler müssen ihre Apps für jedes der oben genannten Szenarien testen und überprüfen und sicherstellen, dass keine Kompatibilitätsprobleme vorliegen. Wenn Kompatibilitätsprobleme erkannt werden, sollten Entwickler die erforderlichen Korrekturen an ihren Apps vornehmen, um sicherzustellen, dass das Kompatibilitätsproblem behoben wird. Zu den häufigen Fehlerbehebungen, die Entwickler vornehmen sollten, gehören:

-   Entfernen Windows Überprüfungen der Betriebssystemversion bei der Installation und Laufzeit
-   Entfernen der Berechtigungsprüfung (Überprüfung auf Administratorzugriff) Verwenden des EXE-Manifests zum Deklarieren der erforderlichen Berechtigungsebene
-   Stellen Sie sicher, dass Windows Binärdateien nicht im App-Installer enthalten sind.
-   Vermeiden des Schreibens in geschützte Bereiche (Registrierung, Ordner) oder Schreiben über geschützte Dateien
-   Digitales Signieren aller Binärdateien (EXE, DLL, SYS-Dateien)
-   Stellen Sie für Installationsprogramme sicher, dass der richtige Eintrag "Programme hinzufügen/entfernen" hinzugefügt wird. Dieser App-Metadateneintrag sollte mindestens den App-Namen, den Herausgeber, die Versionszeichenfolge und die unterstützte Sprache enthalten. Dies gibt der PCA an, dass das Installationsprogramm erfolgreich abgeschlossen wurde, und bietet Benutzern auch eine bequeme Möglichkeit, die App zu deinstallieren.

Stellen Sie sicher, dass der Abschnitt TRUSTINFO und COMPATIBILITY des App-Manifests (ausführbare Datei) wie im Windows 8 Compatibility Cookbook aufgeführt aktualisiert wird, informiert pca den PCA darüber, dass die App für Windows 8 entwickelt wurde, und stellt außerdem sicher, dass die App immer nativ ausgeführt wird, ohne dass kompatibilitätsmodi angewendet werden.

So stellen Sie sicher, dass die PCA die App als für Windows 8 konzipiert betrachtet:

-   Alle EXEs (Installationsprogramm oder Runtime) müssen für die Abschnitte TRUSTINFO und COMPATIBILITY für Windows 8
-   Das Installationsprogramm sollte einen Eintrag "Programme hinzufügen/entfernen" hinzufügen.

**Glossar**

Die von DER PCA verwendeten Kompatibilitätsmodi sind unten mit einer kurzen Beschreibung aufgeführt, was der Modus ermöglicht.



| Mode                         | BESCHREIBUNG                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows7RTM                  | Dieser Modus emuliert das allgemeine Verhalten Windows 7, einschließlich der Betriebssystemversionsnummer 6.1.                                                                   |
| WindowsVistaSP2              | Dieser Modus emuliert das allgemeine Verhalten Windows 7, einschließlich der Betriebssystemversionsnummer 6.1.                                                                   |
| WindowsXPSp3                 | Dieser Modus emuliert allgemeines Windows XP SP3-Verhalten, einschließlich der Betriebssystemversionsnummer 5.1. Dies schließt auch den RUNASHIGHEST-Modus ein.                    |
| RUNASHIGHEST                 | In diesem Modus wird der Benutzer aufgefordert, die App mit den höchsten verfügbaren Berechtigungen auszuführen. Benutzern mit Administratorrechten wird eine UAC-Eingabeaufforderung für erhöhte Rechte für die App angezeigt. |
| Runasadmin                   | In diesem Modus wird der Benutzer immer aufgefordert, die App mit Administratorrechten auszuführen. -Apps mit diesem Modus erhalten immer die Eingabeaufforderung für erhöhte Rechte durch die UAC.                    |
| ELEVATECREATEPROCESS         | In diesem Modus werden untergeordnete Prozesse der Haupt-App mit Administratorrechten ausgeführt. Die untergeordneten Prozesse erhalten ein UAC-Dialogfeld für erhöhte Rechte.                          |
| PINDLL                       | Dieser Modus erzwingt, dass sich eine DLL im Arbeitsspeicher für eine App befindet, auch wenn die App die DLL entlädt.                                                                                |
| DISABLEUSERCALLBACKEXCEPTION | Dieser Modus fängt Benutzerrückrufausnahmen ab und ermöglicht es der App, fortzufahren, ohne die Ausnahme behandeln zu müssen.                                          |
| VIRTUALIZEDELETE             | Dieser Modus fängt Löschvorgänge für geschützte Dateien ab und verhindert, dass Apps aufgrund nicht behandelter Ausnahmen aus dem Löschvorgang fehlschlagen.                   |
| WRPMITIGATION                | Dieser Modus gibt erfolglos zurück, wenn eine App versucht, Windows geschützten Dateien oder Registrierungseinträgen zu schreiben, zu ändern oder zu löschen (ohne den Vorgang tatsächlich abzuschließen).  |
| DXMAXIMIZEDWINDOWEDMODE      | Dieser Modus identifiziert Apps, die in den Vollbildmodus wechseln, und leitet sie in einen maximierten Fenstermodus um.                                                          |
| HIGHDPIAWARE                 | In diesem Modus werden die restlichen Windows darüber informiert, dass die App über hohe DPI-Fähige Daten (High DPI Aware, DPI) informiert ist und das ordnungsgemäße Rendern von Benutzeroberflächenelementen, Text, Schriftart usw. unterstützt.                              |



 

 

 