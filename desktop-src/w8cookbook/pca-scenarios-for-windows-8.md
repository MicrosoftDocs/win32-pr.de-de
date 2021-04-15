---
title: Szenarios für den Programmkompatibilitäts-Assistenten für Windows 8
description: Szenarios für den Programmkompatibilitäts-Assistenten für Windows 8
ms.assetid: C61BF746-63EE-4F4E-81D3-52947FD4954D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebada2ca5115d24f260808a1c9ae899963184a8
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104556334"
---
# <a name="program-compatibility-assistant-scenarios-for-windows-8"></a>Szenarios für den Programmkompatibilitäts-Assistenten für Windows 8

## <a name="platforms"></a>Plattformen

**Clients** -Windows XP \| Windows Vista Windows \| 7 Windows \| 8  

## <a name="description"></a>BESCHREIBUNG

Der Programmkompatibilitäts-Assistent (PCA) ist ein Feature in Windows 8, mit dem Endbenutzer Desktop-Apps ausführen können, die für frühere Windows-Versionen entwickelt wurden. Windows 8 verfügt über eine hervorragend integrierte APP-Kompatibilität, die es ermöglicht, dass apps, die für Windows 7 oder frühere Windows-Versionen entwickelt wurden, automatisch auf Windows 8 funktionieren Allerdings gibt es eine kleine Anzahl von apps, die ohne Eingriff Probleme ausführen können.

Wenn ein Benutzer eine APP ausführt, verfolgt PCA die APP und identifiziert alle Symptome bestimmter bekannter Kompatibilitätsprobleme in Windows 8. Wenn es Probleme mit dem Problem erkennt, bietet es dem Benutzer die Möglichkeit, eine empfohlene Lösung anzuwenden, mit der die APP besser auf Windows 8 ausgeführt werden kann.

## <a name="scenarios"></a>Szenarien

PCA verfolgt Apps für eine Reihe bekannter Kompatibilitätsprobleme in Windows 8. PCA verfolgt die Probleme, identifiziert die Korrekturen und stellt dem Benutzer ein Dialogfeld mit Anweisungen zum Anwenden einer empfohlenen Lösung zur Verfügung. Der Benutzer kann entscheiden, ob er die empfohlenen Korrekturen anwendet oder nichts Unternehmen und die Empfehlung abbrechen möchte. Wenn der Benutzer abbricht, wird diese APP von PCA nicht mehr nachverfolgt.

PCA wendet in der Regel einen der drei Windows-Kompatibilitäts Modi an – Windows XP SP3, Windows Vista SP2 oder Windows 7, je nachdem, wann das Programm (oder dessen Setup) erstellt wurde. PCA verwendet die Attribute "Link \_ Date" und "Subsystem Version" des Programms und die Abschnitte "trustInfo" und "Kompatibilität" des ausführbaren Datei Manifests, um zu bestimmen, welcher der Modi relevant ist und Windows XP SP3 (einschließlich Administrator Berechtigung), Windows Vista SP2 oder Windows 7 anwendet. Ein Glossar am Ende des Dokuments Listet jeden der Kompatibilitäts Modi auf, die vom PCA und dessen Beschreibung angewendet werden.

Für alle unten aufgeführten Szenarien verfolgt PCA apps ein zweites Mal nach dem Anwenden einer Korrektur nach. Wenn die APP auch nach dem Anwenden eines Kompatibilitäts Fixes weiterhin auf dieselbe Weise ausfällt, stellt PCA die Korrektur wieder her. Der PCA beendet die Nachverfolgung der einzelnen fehlerhaften app dann dauerhaft.

Während der PCA viele potenzielle Probleme nachverfolgt, werden nicht alle Probleme tatsächlich zu app-Fehlern führen. PCA empfiehlt Korrekturen nur in Situationen, in denen eine hohe Wahrscheinlichkeit besteht, dass der APP-Fehler auf Windows-Kompatibilitäts Gründe zurückzuführen ist. In den folgenden Abschnitten werden die in Windows 8 entwickelten PCA-Szenarien erweitert. In jedem Abschnitt werden das Problem Szenario und die Empfehlungen beschrieben, die von PCA bereitstellt werden, damit die APP weiterhin ordnungsgemäß auf Windows 8 funktioniert.

Weitere Informationen zu Kompatibilitäts Änderungen in Windows 8 finden Sie in den anderen Themen im *Windows 8 Compatibility Cookbook*.

Folgende Szenarien werden von PCA nachverfolgt und empfohlen:

-   Die APP kann nicht installiert oder deinstalliert werden.
-   Die APP kann nicht mit einer Windows-Versions Überprüfung ausgeführt werden.
-   Die APP kann aufgrund von Administratorrechten nicht gestartet werden.
-   App stürzt aufgrund bestimmter Speicherprobleme ab
-   App schlägt aufgrund nicht übereinstimmender Systemdateien fehl
-   App schlägt aufgrund von nicht behandelten Fehlern auf 64-Bit-Fenstern fehl
-   App schlägt fehl, wenn geschützte nicht-Windows-Dateien gelöscht werden.
-   App schlägt fehl, wenn Windows-Dateien geändert werden
-   App schlägt aufgrund der Verwendung von 8-oder 16-Bit-Farbmodi fehl
-   App schlägt aufgrund von Grafik-und Anzeigeproblemen fehl
-   App kann keine dpi-Informationen deklarieren
-   App schlägt aufgrund von fehlenden Windows-Features fehl
-   App schlägt aufgrund von nicht signierten Treibern auf 64-Bit-Windows 8 fehl
-   Über Kompatibilitäts Einstellungen installierte apps werden überwacht.
-   App kann Installationsprogramme oder updaterer nicht starten
-   App-Installationsprogramme, die mit Administrator Berechtigungen ausgeführt werden müssen
-   Ältere Systemsteuerungs-Applets, die mit Administrator Berechtigungen ausgeführt werden müssen

Jedes dieser Szenarien wird unten erweitert:

**Die APP kann nicht installiert oder deinstalliert werden.**

Einer der gängigsten Arten von App-Fehlern tritt während der Installation der APP auf. Ältere Setup Programme schlagen in der Regel auf zweierlei Weise fehl:

-   Das Setup Programm kennt die Features der Benutzerkontensteuerung (User Account Control, UAC) in Windows 8 nicht, sodass es möglicherweise nicht mit den vollständigen Berechtigungen ausgeführt wird, die erforderlich sind, um Systemänderungen an den geschützten Bereichen von Windows 8 vorzunehmen.
-   Das Setup Programm überprüft, ob die Windows-Version ausgeführt wird, und blockiert die Ausführung, wenn die Version höher als erwartet ist.

Diese Fehlerbedingungen sind zwei der gängigsten Typen von Kompatibilitäts Fehlern beim Setup. Durch die Unterstützung verschiedener anderer Windows-Komponenten, wie z. b. UAC, werden Setup Programme beim Start erkannt und am Ende der Installation nachverfolgt. Wenn beim Setup Programm entweder keine Dateien hinzugefügt werden oder ein gültiger Eintrag in der Windows-Systemsteuerung in der Windows-Systemsteuerung hinzugefügt werden kann, betrachtet PCA das Setup als fehlgeschlagen.

In diesem Fall empfiehlt PCA einen geeigneten Kompatibilitätsmodus für die app. Im Kompatibilitätsmodus kann das Setup Programm im Windows-Modus ausgeführt werden, für den es entworfen wurde, und es wird außerdem sichergestellt, dass die APP mit Administratorrechten ausgeführt wird. PCA wendet den RunAsAdmin-Kompatibilitätsmodus zusammen mit dem entsprechenden Kompatibilitätsmodus von Windows XP, Windows Vista oder Windows 7 an. Der Benutzer kann am Ende der fehlgeschlagenen Installation ein Dialogfeld mit der PCA-Empfehlung sehen:

![Dialogfeld "Fehler beim Installieren oder deinstallieren" der APP](images/pcafigure1.png)

Der Benutzer kann dann Folgendes auswählen:

-   Führen Sie das Programm mit den Kompatibilitäts Einstellungen (empfohlene Option) aus, nach der PCA die empfohlene Einstellung anwendet (Kompatibilitätsmodus), das Setup Programm neu starten und nachverfolgen, bis das Setup erfolgreich abgeschlossen wurde.
-   Geben Sie an, dass das Programm ordnungsgemäß installiert ist. in diesem Fall fügt der PCA keine Einstellungen hinzu und beendet die Nachverfolgung des Setups.
-   Klicken Sie auf schließen. in diesem Fall fügt der PCA keine Einstellungen hinzu und beendet die Nachverfolgung dieses Setups.

Derselbe Mechanismus wird verwendet, um die Deinstallation der APP zu unterstützen, wenn ein Benutzer versucht, die APP entweder über den Abschnitt "Software entfernen" in Windows oder über die Verknüpfung der APP-Deinstallation zu deinstallieren.

**Die APP kann nicht mit einer Windows-Versions Überprüfung ausgeführt werden.**

Einer der gängigeren Kompatibilitäts Fehler in der APP-Laufzeit ist die Überprüfung der Windows-Version. Viele apps überprüfen beim Start die Windows-Version. Wenn Sie die Version nicht erkennen, blockieren Sie sich selbst dann, wenn die APP ohne Probleme ausgeführt werden kann.

Im Allgemeinen sind solche Überprüfungen zwei Bedingungen zugeordnet, die der PCA verfolgt:

Die APP zeigt ein Meldungs Feld an, das den Benutzer warnt. Unten ist ein Beispiel angegeben:

![Fehler beim Ausführen der APP mit dem Dialogfeld "Windows-Versions Überprüfung"](images/pcafigure2.png)

-   Die APP wird sofort beendet oder stürzt ab

Wenn der PCA beide Bedingungen für eine APP identifiziert, wird dem Benutzer eine Empfehlung bereitgestellt. PCA ermöglicht dem Benutzer, die APP mit Kompatibilitäts Einstellungen erneut auszuführen. Der PCA wendet den entsprechenden Windows XP-, Windows Vista-oder Windows 7-Kompatibilitätsmodus basierend auf der APP an. Wie in jedem Szenario kann der Benutzer PCA mitteilen, dass die APP ordnungsgemäß ausgeführt wurde, oder die empfohlenen Einstellungen durch Klicken auf die Schaltfläche Schließen ablehnen. Ein Beispiel Dialogfeld wird wie folgt bereitgestellt:

![Fehler beim Ausführen der APP mit einer Option zur Option "Windows-Versions Überprüfung"](images/pcafigure3.png)

**Die APP kann aufgrund von Administrator Berechtigungen nicht gestartet oder ausgeführt werden.**

Einige apps benötigen Administratorrechte, um ihre Funktionalität auszuführen und auszuführen. In Windows 8, ähnlich wie Windows 7 und Windows Vista, werden apps jedoch standardmäßig aufgrund von UAC auf niedrigeren Berechtigungsstufen ausgeführt. Neuere apps, die für Windows Vista und höher entwickelt wurden, deklarieren im Allgemeinen die Berechtigungsstufe, die Sie für die Verwendung im Trust Info-Abschnitt des exe-Manifests benötigen. Ältere apps schlagen jedoch im Allgemeinen auf zweierlei Weise fehl:

-   Die APP zeigt dem Benutzer eine Meldung an, dass Administrator Berechtigungen erforderlich sind, wie im folgenden Beispiel gezeigt:

![die APP kann aufgrund des Dialog Felds für administrative Berechtigungen nicht gestartet oder ausgeführt werden.](images/pcafigure4a.png)

-   Die APP wird entweder sofort beendet oder stürzt ab.

Wenn der PCA beide Bedingungen für eine APP identifiziert, wird dem Benutzer eine Empfehlung bereitgestellt. PCA ermöglicht dem Benutzer die erneute Ausführung der APP mit Administratorrechten (PCA wendet den RunAsHighest-Kompatibilitätsmodus an). Der Benutzer erhält eine UAC-Eingabeaufforderung, wenn die APP erneut ausgeführt wird. Wie in jedem Szenario kann der Benutzer mit der empfohlenen Einstellung erneut ausführen oder die empfohlenen Einstellungen durch Klicken auf Schließen ablehnen. Ein Beispiel Dialogfeld wird wie folgt bereitgestellt:

![Fehler beim Starten oder Ausführen der APP aufgrund der Option für administrative Berechtigungen.](images/pcafigure5.png)

**App stürzt aufgrund bestimmter Speicherprobleme ab**

Einige Apps Abstürzen aufgrund eines bekannten Speicher Problems. Die APP verweist auf eine DLL aus dem Arbeitsspeicher und ruft dann eine Funktion auf, um Code in derselben DLL auszuführen. Dies führt zu einem sofortigen Absturz der app. Obwohl dieses Problem nicht auf Windows 8-Kompatibilitäts Änderungen zurückzuführen ist, ist es ein relativ häufiges Problem, das in einer Vielzahl von apps auftritt. PCA verfolgt dieses Problem nach, um Benutzern die Möglichkeit zu geben, Ihre APP zuverlässiger auszuführen.

Für diese apps wendet PCA den pindll-Kompatibilitätsmodus automatisch automatisch an. Der von PCA aufgerufene Kompatibilitätsmodus verhindert, dass die APP die dll aus dem Arbeitsspeicher freigibt. Daher funktioniert der Funktionsaufrufe der DLL von der APP, sodass die APP abstürzen kann, sodass Sie weiterhin ordnungsgemäß funktioniert.

**App schlägt aufgrund nicht übereinstimmender Systemdateien fehl**

Einige apps, die für Windows XP und früher entwickelt wurden, umfassen Kopien von Windows-System-DLLs zusammen mit ihren Installationsprogrammen. Wenn solche apps installiert sind, verfügt die APP sowohl über eine ältere Kopie der dll als auch über die aktuelle Version der dll in den Windows-Systemordnern.

Unter Windows Vista und höher kann diese Bedingung bewirken, dass die APP fehlschlägt, wenn versucht wird, die lokale dll zu laden, da diese DLL nicht gut mit den restlichen Windows-System-DLLs funktioniert. Da die app in der Regel nicht die neueren Versionen dieser DLL kennt, funktioniert Sie nicht ordnungsgemäß.

Wenn der PCA erkennt, dass die dll nicht ordnungsgemäß geladen werden konnte, wendet er eine Kompatibilitäts Einstellung an, die Windows das Laden der neuesten Version der dll aus dem Windows-Systemordner ermöglicht, damit die APP ordnungsgemäß ausgeführt werden kann.

Am Ende der ersten fehlgeschlagenen APP wird das Dialogfeld "PCA" angezeigt, in dem Sie über die angewendete Einstellung benachrichtigt werden, wie unten gezeigt:

![App schlägt aufgrund von nicht übereinstimmenden Systemdateien fehl](images/pcafigure6.png)

**App schlägt aufgrund von nicht behandelten Fehlern auf 64-Bit-Fenstern fehl**

Bei der 64-Bit-Version von Windows 8 wurde eine neue Ausnahme für den Rückrufmechanismus der Nachrichten Schleife aktiviert. Diese Ausnahme wurde in Windows 7 eingeführt, es ist jedoch nicht zwingend erforderlich, diesen Fehler zu behandeln. In Windows 8 müssen apps, die Nachrichten Schleifen verwenden, diese neue Ausnahme behandeln. Wenn dies nicht der Fall ist, stürzt dies ab. Apps, die für ältere Windows-Versionen entwickelt wurden, kennen diese Ausnahme möglicherweise nicht. Daher wird dieser Fehler (Ausnahme) möglicherweise nicht ordnungsgemäß behandelt.

Der PCA erkennt apps, die aufgrund dieses unbehandelten Fehlers fehlschlagen, und wendet automatisch den Kompatibilitätsmodus "disableusercallbackexception" für die APP an. Nachdem die Einstellung am Ende der Ausführung angewendet wurde, wird der Benutzer wie unten beschrieben benachrichtigt. Die APP erhält den Modus bei der nächsten Testlauf und kann diesen Fehler vermeiden.

![App schlägt aufgrund von nicht behandelten Fehlern im Windows-Dialogfeld 64-Bit-Windows fehl](images/pcafigure7.png)

**App schlägt fehl, wenn geschützte nicht-Windows-Dateien gelöscht werden.**

Für einige apps, die für Windows XP und früher entwickelt wurden, wird davon ausgegangen, dass Sie normalerweise mit vollen Administratorrechten Im Rahmen des normalen App-Verhaltens können Sie versuchen, geschützte nicht-Windows-Dateien (entweder in Programmdateien oder in Windows-Ordnern) zu löschen. Wenn der Löschvorgang fehlschlägt, können viele derartige Apps Abstürzen.

Der PCA erkennt diese apps, die geschützte Dateien und Abstürze nicht löschen können, und bietet dem Benutzer eine Empfehlung. PCA ermöglicht dem Benutzer, die APP mit Kompatibilitäts Einstellungen erneut auszuführen. Wie in jedem Szenario kann der Benutzer PCA mitteilen, dass die APP ordnungsgemäß ausgeführt wurde, oder die empfohlenen Einstellungen durch Klicken auf die Schaltfläche Schließen ablehnen. In diesem Fall wendet PCA den virtualizedelete-Kompatibilitätsmodus an. Ein Beispiel Dialogfeld wird wie folgt bereitgestellt:

![App schlägt fehl, während versucht wird, geschützte nicht-Windows-Dateien zu löschen.](images/pcafigure8.png)

**App schlägt fehl, wenn versucht wird, Windows-Dateien oder Registrierungsschlüssel zu ändern**

Für einige apps, die für Windows XP und früher entwickelt wurden, wird davon ausgegangen, dass Sie normalerweise mit vollen Administratorrechten Im Rahmen des normalen App-Verhaltens können Sie versuchen, Windows-geschützte Dateien (entweder in Programmdateien oder Windows-Ordnern) oder Registrierungs Schlüsseln im Besitz von Windows zu ändern, zu löschen oder zu schreiben. Wenn ein Schreib-, Lösch-oder Änderungs Vorgang für eine Datei oder einen Registrierungsschlüssel fehlschlägt, können viele derartige Apps Abstürzen oder fehlschlagen.

PCA erkennt diese apps, die nicht in geschützte Windows-Dateien oder Registrierungsschlüssel schreiben können, und bietet dem Benutzer eine Empfehlung, wenn die APP beendet wird. PCA ermöglicht dem Benutzer, die APP mit Kompatibilitäts Einstellungen erneut auszuführen. Wie in jedem Szenario kann der Benutzer PCA mitteilen, dass die APP ordnungsgemäß ausgeführt wurde, oder die empfohlenen Einstellungen durch Klicken auf die Schaltfläche Schließen ablehnen. In diesem Fall wendet PCA den Kompatibilitätsmodus "wrpentschärfung" an. Ein Beispiel Dialogfeld wird wie folgt bereitgestellt:

![App schlägt fehl, wenn versucht wird, Windows-Dateien oder Registrierungsschlüssel zu ändern.](images/pcafigure9.png)

**App schlägt aufgrund der Verwendung von 8-oder 16-Bit-Farbmodi fehl**

Als Teil der reimaginierung von Windows 8 für Windows Store-Apps ist einer der wichtigsten Änderungen, dass die Desktopfenster-Manager (DWM) jetzt nur 32-Bit-Farben in Windows 8 unterstützt. Niedrigere Farbmodi werden nun simuliert.

Viele ältere apps und Spiele, die für Windows XP oder vor der Verwendung von 8-Bit-oder 16-Bit-Farbmodi entwickelt wurden. Ohne Entschärfung können diese apps unter Windows 8 nicht ausgeführt werden. Wenn diese apps jedoch einen der 8-Bit-oder 16-Bit-Farbmodi zur Anzeige verwenden, identifiziert PCA das Problem sofort und stellt mit der Hilfe von DWM sicher, dass die APP ordnungsgemäß mit dem simulierten Farb Modus funktioniert.

Beachten Sie, dass dies geschieht, sobald die APP den unteren Farbmodus anfordert und für den Benutzer transparent ist. Der Benutzer muss die APP nicht neu starten, um diese Entschärfung zu erhalten, da diese Korrektur immer erforderlich ist, um sicherzustellen, dass die APP ordnungsgemäß funktioniert.

**Anwendung schlägt aufgrund von Grafik-und Anzeigeproblemen fehl**

Da Desktopfenster-Manager (DWM) in Windows 8 immer aktiviert ist, kann es bei einigen älteren Windows XP-ERA-apps zu Fehlern kommen, wenn die APP Grafik-APIs im gemischten Modus verwendet, wie bei der Verwendung von GDI-und DirectX-APIs zum Zeichnen auf den Bildschirm (meistens ältere Spiele) und versucht, den Vollbildmodus zu verwenden

-   DWM verhindert, dass das Zeichnen direkt auf dem Desktop erfolgt, und das Spiel oder die APP schlägt fehl, oder es wird ein schwarzer Bildschirm auf den Desktop gezeichnet, und keines der Grafiken ist sichtbar.
-   In solchen Fällen erkennt Windows, wenn die APP beendet wird,, dass die APP oder das Spiel ein Problem mit dem Vollbildmodus hat, und wendet den Kompatibilitätsmodus dxmaximizedwindowedmode an, mit dem die APP oder das Spiel in einem maximierten Fenstermodus statt im Vollbildmodus ausgeführt werden kann.
-   Nachdem die Einstellung am Ende der Ausführung angewendet wurde, wird der Benutzer vom PCA benachrichtigt, wie unten gezeigt. die APP erhält beim nächsten Testlauf den Kompatibilitätsmodus und kann ordnungsgemäß ausgeführt werden.

![Anwendung schlägt aufgrund von Grafik-und Anzeigeproblemen fehl](images/pcafigure10.png)

**App kann keine dpi-Informationen deklarieren**

Ein weiteres typisches Anzeige Problem bei vielen älteren apps tritt auf, wenn Windows und die APP im Modus mit hohem dpi-Modus ausgeführt werden, die APP jedoch nicht das Bewusstsein für hohe dpi-Vorgänge über das exe-Manifest deklariert. Zu den häufigen Problemen, die aufgrund dieser nicht Übereinstimmung in den Einstellungen auftreten können, zählen Elemente der Benutzeroberfläche oder Text und falscher Schrift Grad. Weitere Informationen zu den Problemen finden Sie [hier](/previous-versions//dd464660(v=vs.85)).

In solchen Fällen erkennt Windows, dass die APP hoch dpi-fähig ist, und wendet den highdpiaware-Kompatibilitätsmodus auf die APP am Ende der ersten Testlauf an. Die PCA informiert den Benutzer dann über diese Informationen wie unten gezeigt:

![Fehler beim Deklarieren des dpi-Dialog Felds für die APP](images/pcafigure11.png)

**Anwendung schlägt aufgrund von fehlenden Windows-Features fehl**

Einige apps sind von Windows-Features abhängig, die seit Windows Vista entfernt wurden. Wenn diese apps versuchen, die fehlenden DLLs oder COM-Komponenten zu laden, funktionieren Sie nicht mehr.

PCA erkennt apps, wenn Sie versuchen, die fehlenden Windows-Features zu laden, und gibt eine Empfehlung zum Herunterladen dieser Komponenten und deren Installation nach dem Beenden der APP an. Der Benutzer kann auf "Get Help Online" klicken, um eine Alternative zu finden oder das Feature herunterzuladen und zu installieren. Wenn dies erforderlich ist, kann der Benutzer durch Klicken auf schließen auswählen, dass nichts unternommen werden soll.

![Anwendungsfehler aufgrund eines fehlenden Dialog Felds "Windows-Features"](images/pcafigure12.png)

**App schlägt aufgrund von nicht signierten Treibern auf 64-Bit-Windows 8 fehl**

64-Bit-Windows hat seit Windows Vista Digital signierte Treiber (sys-Dateien) benötigt. Ältere apps wurden jedoch vor der Veröffentlichung von Windows Vista-ausgeliefert-Treibern entworfen, die nicht digital signiert waren. Wenn ein solcher nicht signierter Treiber installiert ist, lädt Windows ihn nicht. In seltenen Fällen kann es vorkommen, dass Windows nicht gestartet wird, wenn solche Treiber als Treiber für die Start Zeit gekennzeichnet sind.

Einige ältere apps installieren Treiber, die nicht auf 64-Bit-Windows signiert sind. Jedes Gerät oder jede APP, das versucht, diesen Treiber zu verwenden, kann fehlschlagen oder zu einem Systemabsturz führen. Um ein solches Szenario zu verhindern, erkennt der PCA apps, wenn er nicht signierte Treiber installiert, und deaktiviert den Treiber, der als Treiber für die Start Zeit markiert ist.

Außerdem weist Sie den Benutzer an, einen digital signierten Treiber zu erhalten, damit die APP ordnungsgemäß funktioniert. Die Meldung wird als Ergebnis der Installation des Treibers und als Ergebnis der Installation der App angezeigt. Wenn der gleiche Treiber von einer anderen APP installiert wird, erhält diese APP ebenfalls dieselbe Nachricht.

![App schlägt aufgrund von nicht signierten Treibern auf dem 64-Bit-Dialogfeld für Windows 8 fehl](images/pcafigure13.png)

**Über Kompatibilitäts Einstellungen installierte apps werden überwacht.**

Wenn ein Installer ausfällt, unterstützt PCA das Installationsprogramm je nach Fehlerart verschiedene Kompatibilitäts Modi. Nachdem das Installationsprogramm mit Kompatibilitäts Einstellungen erfolgreich abgeschlossen wurde, verfolgt PCA die Verknüpfungen, die das Installationsprogramm hinzugefügt hat Dadurch wird nachverfolgt, ob die installierten Apps möglicherweise auch die Kompatibilitäts Einstellungen für das Installationsprogramm benötigen.

Wenn ein Benutzer eine solche APP aufruft, fordert PCA den Benutzer dazu auf, zu Fragen, ob die APP ordnungsgemäß funktioniert hat. Wenn der Benutzer antwortet, "yes", hält der PCA die Nachverfolgung der APP an. Wenn der Benutzer "Nein" antwortet, wendet er denselben Kompatibilitätsmodus an, der auf das Installationsprogramm der APP angewendet wurde, und führt die APP erneut mit dem angewendeten Kompatibilitätsmodus aus.

**App kann Installationsprogramme oder updaterer nicht starten**

Apps starten manchmal untergeordnete Programme, die als Administratoren ausgeführt werden müssen. Dies ist in der Regel der Fall, wenn eine APP versucht, die Updater-Software zu starten, um neue Updates für die APP zu überprüfen und zu installieren. Wenn apps solche untergeordneten Programme direkt ausführen, kann das untergeordnete Programm nicht gestartet werden, da die APP selbst nicht über Administratorrechte verfügte oder weil das untergeordnete Programm nicht ordnungsgemäß für die Rechte Erweiterung mit dem UAC-Manifest gekennzeichnet wurde.

PCA verfolgt diese Fehler nach, und wenn die primäre app geschlossen wird, wendet sie automatisch den ElevateCreateProcess-Kompatibilitätsmodus an, der dabei hilft, dass untergeordnete Programme ordnungsgemäß ausgeführt werden. Wenn die APP die untergeordnete App bei nachfolgenden Ausführungen startet, wird dem Benutzer ein UAC-Dialogfeld für das untergeordnete Programm angezeigt.

Im folgenden wird ein Beispiel für das PCA-Dialogfeld angezeigt:

![Fehler beim Starten des Dialog Felds "Installer oder updaterer" der APP](images/pcafigure14.png)

**App-Installationsprogramme, die mit Administrator Berechtigungen ausgeführt werden müssen**

Installer von Windows-Desktop-Apps erfordern Administratorrechte, da Sie Dateien, Ordner und Registrierungseinträge in geschützte Systembereiche schreiben. Windows (UAC) verfügt über Erkennungs Logik, um zu ermitteln, wann ein Installer ausgeführt wird, und fordert den Benutzer sofort auf, Administratorrechte über das UAC-Dialogfeld anzugeben. In einigen Fällen kann diese Logik jedoch nicht ermitteln, ob es sich bei einer APP tatsächlich um ein Installationsprogramm handelt, und es werden möglicherweise keine Administratorrechte erhalten. Dabei handelt es sich im Allgemeinen um benutzerdefinierte Installationsprogramme, die keine bekannten Installationstechnologien wie Windows Installer oder Install Shield verwenden.

In solchen Fällen erkennt der PCA, dass der Installer seine Dateien nicht schreiben konnte. Wenn die fehlgeschlagene Installation fehlschlägt, gibt PCA eine Empfehlung zum Anwenden von Kompatibilitäts Einstellungen an. Wenn der Benutzer auf "Programm ausführen" klickt, wendet PCA den RunAsAdmin-Kompatibilitätsmodus an und führt den Installer erneut aus. Wenn sich der Benutzer für das Schließen entscheidet, wird keine Einstellung angewendet. Ein Beispiel für ein PCA-Dialogfeld ist unten dargestellt:

![Screenshot, der ein Beispiel für ein Dialogfeld für ein App-Installationsprogramm anzeigt, das mit Administratorrechten ausgeführt werden muss.](images/pcafigure15.png)

Ältere Systemsteuerungs-Applets, die mit Administratorrechten System Steuerungs Applets ausgeführt werden müssen, ändern in der Regel die Systemeinstellungen und benötigen die Möglichkeit, AD-Administrator auszuführen. Die, die vor Windows Vista geschrieben wurden, verfügen jedoch nicht über ein exe-Manifest, oder Sie verfügen nicht über den Trust Info-Abschnitt, der die gewünschte Berechtigungsstufe deklariert. Wenn solche Applets ausgeführt werden, erkennt der PCA Sie, und gibt am Ende der ersten Testlauf eine Empfehlung zur Durchführung der administrativen Einstellungen an. Wenn der Benutzer auf "Programm ausführen" klickt, wendet PCA den RunAsAdmin-Kompatibilitätsmodus an und führt den Installer erneut aus. Wenn sich der Benutzer für das Schließen entscheidet, werden keine Einstellungen angewendet. Ein Beispiel für ein PCA-Dialogfeld ist unten dargestellt:

![App-Installationsprogramme, die mit Administrator Berechtigungen ausgeführt werden müssen](images/pcafigure16.png)

**Überprüfen der empfohlenen Einstellungen durch Benutzer Feedback**

Am Ende jedes Szenarios (nachdem die APP mit den empfohlenen Kompatibilitäts Einstellungen ausgeführt wurde) fragt PCA den Benutzer nach einer einfachen Frage:

![Überprüfen der empfohlenen Einstellungen im Dialogfeld "Benutzer Feedback"](images/pcafigure17.png)

Der Benutzer kann Feedback geben, wenn die APP mit der Kompatibilitäts Einstellung funktioniert hat oder fehlgeschlagen ist. Diese Daten werden anonym an Microsoft gesendet. Dadurch wird sichergestellt, dass solche Korrekturen in Windows 8 über den Windows Update-Prozess integriert werden können, sodass zukünftige Benutzer von Windows 8 den App-Fehler nicht mehr erreichen, und PCA die APP nicht mehr nach dem Fehler nachverfolgen muss.

**Nachverfolgen von Problemen ohne Empfehlungen**

Apps können aus Kompatibilitätsgründen auf viele verschiedene Arten fehlschlagen. PCA verfolgt viele weitere Kompatibilitätsprobleme, als in den obigen Szenarien aufgeführt sind. In diesen Fällen hängt die Problem Manifestation oft von der App ab. Dies bedeutet, dass einige apps solche Probleme ordnungsgemäß behandeln und daraus wiederherstellen können, während andere dies nicht tun. Daher bietet der PCA, bei dem der PCA die APP weiterhin verfolgt, keine direkte Empfehlung für eine Korrektur.

Zu den Problemen, die von PCA nachverfolgt werden, ohne dass eine empfohlene Einstellung oder ein Dialogfeld angezeigt wird, gehören folgende apps:

-   Sehr kurze Laufzeit – apps werden nicht mehr als drei Sekunden ausgeführt.
-   Erstellen globaler Speicher Objekte ohne Administratorrechte
-   Fehler (Win32-Ausnahme) beim Start
-   Überprüfen auf Administratorrechte (schlägt jedoch möglicherweise fehl)
-   Verwenden von Indeo-Codecs (veraltet von Windows Vista)
-   Versuchen Sie, Schlüssel von geschützten Registrierungs Speicherorten wie HKLM zu schreiben oder zu löschen.
-   Absturz beim Start

**Anwenden von Korrekturen auf der Registerkarte "Kompatibilität" und Kompatibilitätsproblemen**

Wie bereits erwähnt, können Apps aus einer Vielzahl von Kompatibilitätsgründen fehlschlagen. Nicht alle diese haben eine Clear PCA-Empfehlung, da die Einstellungen App-abhängig sind. Benutzer können jedoch zur Kompatibilitätsproblem Behandlung oder zur Registerkarte Kompatibilität wechseln, um bestimmte gängige Korrekturen anzuwenden, um zu versuchen, ihre fehlerhafte App auf Windows 8 ordnungsgemäß zu verwenden. In solchen Fällen verfolgt PCA die APP weiterhin auf Kompatibilitätsprobleme, bevor und nachdem die Lösung angewendet wird. Nachdem die APP mit der Anwendung ausgeführt wurde, wird der Benutzer vom PCA gefragt, ob der Fehler behoben wurde. Nachdem der Benutzer die Frage beantwortet hat, werden die Daten anonym über Telemetriedaten an Microsoft gesendet. Diese Daten werden von vielen Benutzern gesammelt und analysiert, und die qualifizierenden Korrekturen werden dann über Windows Update umfassend an alle Windows 8-Benutzer verteilt.

**Verwenden der Kompatibilitätsproblem Behandlung**

Die Kompatibilitätsproblem Behandlung ist ein Mechanismus in Windows, mit dem Sie Probleme mit apps diagnostizieren und empfohlene Korrekturen anwenden können, damit Sie ordnungsgemäß funktionieren. Dies ist nur erforderlich, wenn der PCA keine Empfehlung für die APP bereitstellt.

Mit der Problembehandlung können Benutzer eine Reihe von Fragen durchlaufen und beantworten. basierend auf den Antworten wird ein Satz von Korrekturen angewendet, und die Benutzer können ihre Apps testen und die Korrekturen überprüfen. Nach der Überprüfung werden die Korrekturen dauerhaft auf die apps angewendet, damit Sie unter Windows 8 besser funktionieren.

Im folgenden finden Sie eine Referenz zur Problembehandlung:

![Verwenden des Dialog Felds zur Kompatibilität von Kompatibilitätsproblemen](images/pcafigure18.png)

Die Kompatibilitätsproblem Behandlung kann auf zwei Arten gestartet werden:

**Über den Startbildschirm:**

1.  Typ: Kompatibilitätsproblem Behandlung
2.  Klicken Sie im Abschnitt Einstellungen auf die Kachel "Programme, die für vorherige Version von Windows ausgeführt wurden".

  
**Über die APP-Kachel:**

1.  Klicken Sie im Start Bildschirm mit der rechten Maustaste auf die APP-Kachel.
2.  Klicken Sie auf "Datei Speicherort öffnen" (nur Desktop-Apps).
3.  Klicken Sie im Explorer-Menüband auf die Registerkarte "App".
4.  "Behandlung von Kompatibilitätsproblemen" auswählen

  


**Verwenden der Registerkarte "Kompatibilität"**

Beachten Sie, dass dies nur für Benutzer empfohlen wird, die verschiedene Kompatibilitäts Einstellungen ausprobieren möchten. Diese Methode bietet keine Empfehlung zur Art der Behebung, die auf apps angewendet werden soll. Hier wird erwartet, dass der Benutzer weiß, welche Korrekturen angewendet werden können, damit die APP funktioniert. Wenn Sie sich nicht sicher sind, welche Korrekturen vorliegen, verwenden Sie die Kompatibilitätsproblem Behandlung, um eine Lösung für die APP zu finden.

So greifen Sie auf die Registerkarte Kompatibilität zu:

 **Über den Startbildschirm:**

1.  Rechtsklick auf die APP-Kachel
2.  Datei Speicherort öffnen (nur Desktop-Apps)

  
**Im Explorer-Menüband:**

1.  Klicken Sie auf Eigenschaften
2.  Navigieren Sie zur Registerkarte Kompatibilität.
3.  Kompatibilitäts Korrekturen auswählen
4.  Erneutes Ausführen der APP
    > [!Note]  
    > Sie können erneut an derselben Stelle zurückkehren, um die Korrekturen zu ändern oder zu entfernen. Sie können die Korrekturen auch auf alle Benutzer auf dem Computer anwenden, indem Sie die Schaltfläche auf der Registerkarte verwenden.

     

  


![Verwenden der Registerkarte "Kompatibilität"](images/pcafigure19.png)

**Apps mit bekannten Kompatibilitätsproblemen**

Abgesehen von den oben aufgeführten Erkennungs Szenarien zur Laufzeit werden die Benutzer von PCA auch beim Starten der APP informiert, wenn die APP bekannte Kompatibilitätsprobleme aufweist. Die Liste wird in der Kompatibilitätsdatenbank der System-App gespeichert. Es gibt zwei Arten von Nachrichten:

-   **Hard-Block-Nachrichten**– wenn die APP bekanntermaßen nicht kompatibel ist und das Zulassen der Ausführung der APP zu schwerwiegenden Auswirkungen auf das System führt (z. b. ein Windows-Absturz oder nach der Installation nicht starten kann), wird eine blockierende Meldung angezeigt, wie unten gezeigt.

![Apps mit bekannten Kompatibilitätsproblemen: Dialogfeld "Hard Block Messages"](images/pcafigure20.png)

-   **Soft-Block-Nachrichten**– wenn die APP ein bekanntes Kompatibilitätsproblem aufweist und möglicherweise nicht ordnungsgemäß funktioniert, wird diese Meldung angezeigt:

![Apps mit bekannten Kompatibilitätsproblemen-Dialogfeld "Soft Block Messages"](images/pcafigure21.png)

In beiden Fällen sendet die Option "Get Help Online" einen Windows-Fehlerbericht, um eine Online Antwort von Microsoft zu erhalten, und zeigt Sie dem Benutzer an. In der Regel weisen die Antworten den Benutzer auf einen von drei Arten von Ressourcen hin:

-   Ein Update vom APP-Hersteller
-   Die Website eines App-Anbieters für weitere Informationen
-   Microsoft Knowledge Base-Artikel weitere Informationen

**Telemetrie für PCA**

Nachdem der PCA alle App-Probleme auf einem Windows 8-Computer behoben hat und alle Benutzer Feedback erhält, sammelt er anonyme Daten über die APP, das Installationsprogramm, die erkannten Probleme und die Kompatibilitäts Einstellungen, die auf die APP angewendet werden, und sendet Sie an Microsoft zurück. Diese Daten werden von jedem Benutzer gesammelt, der bereit ist, solche anonymen Daten (über das Programm zur Verbesserung der Benutzerfreundlichkeit CEIP) bereitzustellen. Nachdem diese Daten erfasst wurden, werden die Fehler und Fehlerbehebungen der APP analysiert, und die Korrekturen werden dann über den Windows Update Mechanismus an das gesamte Windows-Ökosystem verteilt, sodass jeder Benutzer der app in Zukunft automatisch von der Behebung profitiert.

**Administrative Steuerelemente und Verwalten der PCA-Einstellungen**

IT-Administratoren können das PCA-Verhalten auf zwei Arten steuern:

-   **PCA** deaktivieren – diese Einstellung ermöglicht es IT-Administratoren, die Dialogfelder, die PCA anzeigt, für die Benutzer zu deaktivieren. PCA verfolgt und erkennt weiterhin Probleme und sendet Telemetriedaten.
-   **App-Telemetrie deaktivieren** – durch diese Einstellung wird das Sammeln und Senden von Telemetriedaten durch PCA deaktiviert.
    > [!Note]  
    > Wenn CEIP deaktiviert ist, hat diese Einstellung keine Auswirkungen.

     

**Entwerfen von Apps für die Zusammenarbeit mit PCA**

Entwickler müssen sicherstellen, dass Ihre apps in allen oben beschriebenen Kompatibilitäts Szenarien gut funktionieren. Entwickler müssen ihre Apps für die einzelnen Szenarien testen und validieren und sicherstellen, dass es keine Kompatibilitätsprobleme gibt. Wenn Kompatibilitätsprobleme erkannt werden, sollten Entwickler die erforderlichen Korrekturen an Ihren Apps vornehmen, um sicherzustellen, dass das Kompatibilitätsproblem behoben ist. Zu den häufigsten Fehlerbehebungen, die Entwickler erstellen sollten, zählen:

-   Windows-Betriebssystem-Versions Prüfungen bei Installation und Laufzeit eliminieren
-   Berechtigungsprüfung entfernen (Überprüfung des Administrator Zugriffs); Verwenden Sie das exe-Manifest, um die richtige Berechtigungsebene zu deklarieren.
-   Stellen Sie sicher, dass Windows-Binärdateien nicht innerhalb des App-Installers ausgeliefert werden.
-   Vermeiden Sie das Schreiben in geschützte Bereiche (Registrierung, Ordner) oder das Schreiben von geschützten Dateien.
-   Alle Binärdateien digital signieren (exe, dll, sys-Dateien)
-   Stellen Sie für Installationsprogramme sicher, dass der richtige Eintrag zum Hinzufügen/Entfernen der Software hinzugefügt wird. dieser APP-Metadateneintrag sollte mindestens den APP-Namen, den Herausgeber, die Versions Zeichenfolge und die unterstützte Sprache enthalten. Dadurch wird dem PCA mitgeteilt, dass das Installationsprogramm erfolgreich abgeschlossen wurde, und es wird eine bequeme Möglichkeit für Benutzer bereitgestellt, die APP zu deinstallieren.

Um sicherzustellen, dass der Trust Info-Abschnitt und der Kompatibilitäts Abschnitt des App-Manifests (ausführbare Datei) gemäß den Angaben im Windows 8 Compatibility Cookbook aktualisiert wird, weiß der PCA, dass die APP für Windows 8 entwickelt wurde, und stellt außerdem sicher, dass die APP immer nativ ausgeführt wird, ohne dass alle Kompatibilitäts Modi darauf angewendet

Um sicherzustellen, dass PCA die APP für Windows 8 entwickelt:

-   Alle exe-Dateien (Installer oder Runtime) müssen für die trustInfo-und Kompatibilitäts Abschnitte für Windows 8 angezeigt werden.
-   Der Installer muss den Eintrag "Software hinzufügen/entfernen" hinzufügen.

**Glossar**

Die vom PCA verwendeten Kompatibilitäts Modi sind unten aufgeführt, und es wird eine kurze Beschreibung der Funktionsweise des Modus angezeigt.



| Mode                         | BESCHREIBUNG                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows7RTM                  | Dieser Modus emuliert das allgemeine Verhalten von Windows 7, einschließlich der Betriebssystem-Versionsnummer 6,1.                                                                   |
| WindowsVistaSP2              | Dieser Modus emuliert das allgemeine Verhalten von Windows 7, einschließlich der Betriebssystem-Versionsnummer 6,1.                                                                   |
| WindowsXPSp3                 | Dieser Modus emuliert das allgemeine Verhalten von Windows XP SP3, einschließlich der Betriebssystem-Versionsnummer 5,1. Dies schließt auch den RunAsHighest-Modus ein.                    |
| Runashöchste                 | Dieser Modus fordert den Benutzer auf, die APP mit der höchsten verfügbaren Berechtigung auszuführen. Benutzern mit Administratorrechten wird eine UAC-Eingabeaufforderung für erhöhte Rechte für die App angezeigt. |
| RUNASADMIN                   | In diesem Modus wird der Benutzer immer aufgefordert, die APP mit Administratorrechten auszuführen. bei apps mit diesem Modus wird immer die UAC-Eingabeaufforderung für erhöhte Rechte angezeigt.                    |
| ELEVATECREATEPROCESS         | Dieser Modus bewirkt, dass untergeordnete Prozesse der Haupt-App mit Administratorrechten ausgeführt werden. die untergeordneten Prozesse erhalten ein UAC-Erweiterungs Dialogfeld.                          |
| Pindll                       | Dieser Modus erzwingt, dass eine DLL für eine APP im Arbeitsspeicher vorhanden ist, auch wenn die APP die dll entlädt.                                                                                |
| Disableusercallbackexception | In diesem Modus werden Benutzer Rückruf Ausnahmen abgefangen, und die APP kann fortgesetzt werden, ohne dass die Ausnahme behandelt werden muss.                                          |
| Virtualizedelete             | Dieser Modus fängt Löschvorgänge für geschützte Dateien ab und verhindert, dass apps aufgrund von nicht behandelten Ausnahmen vom Löschvorgang fehlschlagen.                   |
| Wrpentschärfung                | Dieser Modus gibt Erfolg zurück, wenn eine APP versucht, Windows-geschützte Dateien oder Registrierungseinträge zu schreiben, zu ändern oder zu löschen (ohne den Vorgang tatsächlich abzuschließen).  |
| Dxmaximizedwindowedmode      | Dieser Modus identifiziert apps, die in den Vollbildmodus wechseln, und leitet Sie in einen maximierten Fenstermodus um.                                                          |
| Highdpiaware                 | Mit diesem Modus weiß der Rest von Windows, dass die APP hohe dpi-Werte hat, und hilft bei der ordnungsgemäßen Darstellung von Benutzeroberflächen Elementen, Text, Schriftart usw.                              |



 

 

 