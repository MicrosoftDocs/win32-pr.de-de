---
title: Validierungstests für On-Onboarding-Onlineshops vom Typ 2
description: In diesem Thema werden Tests beschrieben, die Microsoft zum Überprüfen Ihres Onlineshops vom Typ 2 durchführt. Microsoft erfordert, dass Sie diese Tests ausführen, bevor Sie einen Release Candidate übermitteln. Ihr Onlineshop muss diese Tests erfolgreich bestehen, um veröffentlicht zu werden.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2cb1b4d44b1bd3c6289311c6b276de7c75ed1bcd955431796a36d272811942
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901305"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a>Validierungstests für On-Onboarding-Onlineshops vom Typ 2

In diesem Thema werden Tests beschrieben, die Microsoft zum Überprüfen Ihres Onlineshops vom Typ 2 durchführt. Microsoft erfordert, dass Sie diese Tests ausführen, bevor Sie einen Release Candidate übermitteln. Ihr Onlineshop muss diese Tests erfolgreich bestehen, um veröffentlicht zu werden.

> [!Note]  
> Wenn Ihr Speicher Typ 1 anstelle von Typ 2 ist, können Sie dieses Thema als Richtlinie verwenden, um den Umfang der Zertifizierungstests zu verstehen, die für Filialen vom Typ 1 abgedeckt sind. Wenden Sie sich an Microsoft-Support , um den vollständigen Testsatz für Speicher vom Typ 1 [zu](https://support.microsoft.com/ph/7763#tab0)testen.

 

Dieses Thema enthält folgende Abschnitte:

-   [Prüfliste für Tests](#test-checklist)
    -   [Vorbereitung des Testdurchlaufs](#test-pass-preparation)
-   [Testumgebung](#test-environment)
-   [Konfiguration und Einrichtung](#configuration-and-setup)
    -   [Einrichten eines Testcomputers](#setting-up-a-test-machine)
    -   [Einrichten eines Store](#setting-up-a-store)
    -   [Erstellen eines Kontos](#creating-an-account)
    -   [Einrichten der Zwischenspeicherung von Anmeldeinformationen](#setting-up-credential-caching)
-   [Inhaltserfassung](#content-acquisition)
    -   [Streaminginhalt](#streaming-content)
    -   [Abrufen von Inhalten](#obtaining-content)
    -   [Inhaltsinhalt](#burning-content)
    -   [Übertragen von Inhalten](#transferring-content)
-   [Store Funktionen](#store-features)
    -   [Verwalten eines Kontos](#managing-an-account)
    -   [Verwalten des Infocenters](#managing-the-info-center)
-   [Store Interaktion](#store-interaction)
    -   [An die aktive Store](#yielding-to-the-active-store)
    -   [Verhindern der Übernahme des aktiven Store durch den getesteten Store](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [Zugreifen auf eine Store im High-Contrast-Modus](#accessing-a-store-in-high-contrast-mode)
    -   [Sichern eines Store](#securing-a-store)

## <a name="test-checklist"></a>Prüfliste für Tests

Verwenden Sie die Prüfliste in der folgenden Tabelle, um Ihren Onlineshop vom Typ 2 zu überprüfen, den Sie ins Boot holen möchten.



Test

Windows XP

Windows Vista

Windows 7

Ergebnis (pass/fail/not applicable)

32

64

32

64

32

64

1. Überprüfen Sie, ob die Software installiert wird.

2. Überprüfen Sie, ob die Software deinstalliert wird.

3. Vergewissern Sie sich, dass die Software nicht in der Taskleiste ausgeführt wird.

4. Überprüfen Sie, ob die Registerkarte "Store" funktioniert.

5. Stellen Sie sicher, dass der Speicher über eine Option zum Erstellen eines neuen Kontos verfügt.

6. Vergewissern Sie sich, dass sich das erstellte Konto anmelden kann.

7. Stellen Sie sicher, dass der Speicher über eine Option zum Speichern von Benutzerinformationen verfügt.

8. Vergewissern Sie sich, dass die Zwischenspeicherung von Anmeldeinformationen vorhanden ist und funktioniert.

9. Vergewissern Sie sich, dass der Benutzer zur Eingabe von Anmeldeinformationen aufgefordert wird, wenn er nicht zwischengespeichert wird.

10. Überprüfen Sie, ob alle verfügbaren Inhaltsstreamtypen verfügbar sind.

11. Vergewissern Sie sich, dass Inhalte in Microsoft Windows Media Player wiedergegeben werden.

12. Überprüfen Sie, ob ein berechneter Preis richtig ist.

13. Vergewissern Sie sich, dass erworbene Inhalte in die Bibliothek heruntergeladen werden.

14. Vergewissern Sie sich, dass metadaten für den Kauf heruntergeladen werden.

15. Vergewissern Sie sich, dass die Mediennutzungsrechte für den Kauf korrekt sind.

16. Vergewissern Sie sich, dass die erworbenen Inhalte wiedergegeben werden können.

17. Vergewissern Sie sich, dass durch Klicken auf die Schaltfläche **Kaufen** oder **Kaufen** zum Store gewechselt wird.

18. Überprüfen Sie, ob der erworbene Inhalt heruntergeladen wurde.

19. Vergewissern Sie sich, dass erworbene Inhalte zusammengestellt werden können.

20. Vergewissern Sie sich, dass die Anzahl der Burns dekrementiert ist.

21. Stellen Sie sicher, dass Inhalte auf einen anderen Computer übertragen werden können.

22. Überprüfen Sie, ob Inhalte an ein Gerät übertragen werden.

23. Überprüfen Sie, ob die Synchronisierungsanzahl dekrementiert ist.

24. Überprüfen Sie, ob der Kaufverlauf vorherige Käufe nachzeichnet.

25. Vergewissern Sie sich, dass ein vorheriger Kauf wiederhergestellt werden kann.

26. Überprüfen Sie die Funktionalität eines Speichers, um mehrere Computer zu verwalten.

27. Vergewissern Sie sich, dass das Infocenter standardmäßig deaktiviert ist.

28. Vergewissern Sie sich, dass das Infocenter über Medieninformationen im Jetzt wiedergegebenen Bereich verfügt.

29. Vergewissern Sie sich, dass links zum Store navigieren.

30. Überprüfen Sie, ob der getestete Speicher dem aktiven Speicher ergibt.

31. Vergewissern Sie sich, dass der getestete Speicher den aktuellen Speicher nicht übernimmt.

32. Vergewissern Sie sich, dass auf den Speicher im Modus mit hohem Kontrast zugegriffen werden kann.

33. Überprüfen Sie, ob der Speicher sicher ist.



 

### <a name="test-pass-preparation"></a>Vorbereitung des Testdurchlaufs

Bevor Sie einen Testdurchlauf ausführen, sollten Sie sicherstellen, dass der Speicher und die Testkonten für Tests bereit sind. Sie sollten die folgenden Informationen bestimmen, bevor der Durchlauf beginnt. Wenn Sie die Informationen einige Tage vor dem Testdurchlauf ermitteln können, wird der Durchlauf effizienter ausgeführt.

-   Bestimmen Sie die folgenden Informationen zu Testkonten, die vom Speicher bereitgestellt werden:
    -   Konten und Kennwörter ermöglichen einem Benutzer die Anmeldung.
    -   Konten werden für jede Art von Geschäftsmodus, die der Store anbietet, ordnungsgemäß und angemessen bezahlt.
    -   Konten sind für alle Gebietsschemas gültig, die getestet werden sollen, oder Konten sind für jedes Gebietsschema vorhanden, wenn Konten nicht gebietsschemaübergreifend sein können.
-   Bestimmen Sie, welche Gebietsschemas getestet werden sollen.
-   Bestimmen Sie, welche Sprachen getestet werden sollen.
-   Bestimmen Sie die folgenden Informationen zur Testumgebung:

    -   Livespeicher, die mit Windows XP, Windows Vista und Windows 7 funktionieren
    -   Der zu testende Nicht-Livespeicher
    -   Vergewissern Sie sich, dass der zu testende Nicht-Livespeicher in allen Versionen des Betriebssystems und allen Versionen der Windows Media Player-Plattform sichtbar ist.

-   Bestimmen Sie die folgenden Informationen zum zu testden Speicher:

    -   Name des Datenspeichers
    -   Erwartete Logografiken und Bezeichnungen der Registerkarte "Store"
    -   Ist der Speicher für alle Betriebssystemversionen live?
    -   Handelt es sich hierbei um eine neue Version des zu test befindlichen Speichers?
    -   Handelt es sich bei dem zu test befindlichen Speicher um einen Speicher vom Typ 1 oder Typ 2?
    -   Hat sich der Speichertyp geändert?

-   Bestimmen Sie, auf welchen Betriebssystemversionen und Plattformen Sie den Speicher testen möchten.
-   Bestimmen Sie, ob das Installationsprogramm und das Plug-In auf allen betriebssystembasierten Versionen und Plattformen funktionieren, die getestet werden sollen.
-   Bestimmen Sie, ob ein Navigationsdokument erforderlich ist.
-   Bestimmen Sie die folgenden Informationen zu den Medien, die der Store anbietet:

    -   Formate
    -   Ist proprietäre Software erforderlich?
    -   Müssen Sie alle Medientypen oder nur eine Teilmenge von Medientypen testen?

-   Bestimmen Sie die folgenden Informationen zu Mediennutzungsrechten:

    -   Verfügt das Speichermedium über Inhaltsschutz?
    -   Wenn ja, bestimmen Sie den Typ des Inhaltsschutzes, über den die Medien verfügen.
    -   Wenn dies der Fall ist, bestimmen Sie das erwartete geschützte Verhalten.
    -   Umfassen die Mediennutzungsrechte die Computer-zu-Computer-Freigabe?
    -   Die Synchronisierungsrechte
    -   Die Nutzungsrechte
    -   Die Wiedergaberechte
    -   Die Ablaufdaten( falls vorhanden)

-   Ermitteln Sie, ob Sie über ausreichende Medien (einen ausreichend großen Katalog) verfügen, um ein aussagekräftiges Beispiel bereitzustellen.
-   Bestimmen Sie, was der Phasendurchlauf ist: RC 0, Konformität usw.
-   Bestimmen Sie, ob es sich bei dem Testdurchlauf um einen bestimmten Typ handelt: Regression, Feuer usw.

## <a name="test-environment"></a>Testumgebung

Sie müssen Tests für die folgenden Konfigurationen durchführen:

-   Microsoft Windows Media Player 11 unter Windows XP mit 32-Bit- und 64-Bit-Betriebssystemen für Service Pack 3 (SP3)
-   Windows Media Player 11 unter Windows 32-Bit- und 64-Bit-Betriebssystemen (32-Bit-Windows Media Player) von Vista
-   Microsoft Windows Media Player 12 unter Windows 7 32-Bit- und 64-Bit-Betriebssystemen (32-Bit-Windows Media Player)

Obwohl Sie Tests auf allen aufgeführten Betriebssystemversionen und Plattformen durchführen müssen, sind 32-Bit-Versionen von Windows Vista und Windows 7 die Zielbetriebssystemversionen. Sie müssen die Installation von Software auf allen Plattformen testen.

Screenshots in diesem Thema verwenden den fiktiven Store Proseware, um die Verwendung der Benutzeroberfläche zu veranschaulichen.

## <a name="configuration-and-setup"></a>Konfiguration und Setup

In den folgenden Abschnitten wird beschrieben, wie Sie Validierungstests konfigurieren und einrichten, um in einen Onlineshop vom Typ 2 einzuladen.

### <a name="setting-up-a-test-machine"></a>Einrichten eines Testcomputers

Führen Sie die folgenden Schritte aus, um einen Testcomputer einzurichten:

1.  Verweisen Sie den Testcomputer auf Inhaltstestserver, indem Sie einen speicherspezifischen Registrierungsschlüssel hinzufügen.
2.  Legen Sie werte im Dialogfeld **Regions- und Sprachoptionen** auf die richtigen Sprach- und Gebietsschemaeinstellungen fest. Wählen Sie zum Festlegen der Sprache die Registerkarte **Formate** und dann im Kombinationsfeld **Aktuelles Format** die Sprache aus. Wählen Sie zum Festlegen der Region die Registerkarte **Standort** aus, und wählen Sie dann im Kombinationsfeld **Aktueller Standort** die Region aus. Darüber hinaus müssen Sie für Speicher, die die Installation eines Plug-Ins oder einer speicherspezifischen benutzerdefinierten Software erfordern, möglicherweise das Gebietsschema des Systems in die Sprache des Gebietsschemas des Speichers ändern, um die Installation zu vereinfachen. Das Softwareinstallationsprogramm muss sowohl Einzel- als auch Doppel-Bytezeichen unterstützen und in jedem Gebietsschema ausgeführt werden. Sie müssen im nativen Gebietsschema testen. Öffnen Sie zum Festlegen des nativen Gebietsschemas das Dialogfeld **Region und Sprache,** wählen Sie die Registerkarte **Verwaltung** aus, und klicken Sie dann auf die Schaltfläche **Systemgebietsschema ändern,** wie im folgenden Screenshot gezeigt. Wenn Sie auf diese Schaltfläche klicken, wird das Dialogfeld **Region und Sprache Einstellungen** angezeigt. Das Kombinationsfeld **Aktuelles Systemschema** in diesem Dialogfeld ändert das Systemschema.

    Die folgenden Screenshots zeigen die Registerkarten, auf denen Sie Region und Sprache festlegen können:

    ![Screenshot des Dialogfelds "Regionale Optionen" und "Sprachoptionen"](images/reg-lang-opt.png)

    ![Screenshot: Ändern des aktuellen Systemschemas](images/reg-lang-settings.png)

3.  Deaktivieren Sie die Ansicht des Infocenters eines Geschäfts, indem Sie Windows Media Player festlegen, um eine Visualisierung wiederzuspielen. Der Hauptunterschied zwischen den Plattformen besteht darin, dass Sie in Windows Media Player 11 zunächst auf **Jetzt wiedergeben** klicken, während Sie in Windows Media Player 12 mit der rechten Maustaste auf das Hauptfenster klicken.

    Der folgende Screenshot zeigt die Abfolge der Menüoptionen, die eine Visualisierung in Windows Media Player 11 wiedergegeben:

    ![Screenshot: Wiedergeben einer Visualisierung in Windows Media Player 11](images/wmp11-visual.png)

    Der folgende Screenshot zeigt die Abfolge der Menüoptionen, die eine Visualisierung in Windows Media Player 12 wiedergegeben:

    ![Screenshot: Wiedergeben einer Visualisierung in Windows Media Player 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a>Einrichten eines Store

Führen Sie zunächst die folgenden Schritte aus, um einen Speicher einzurichten, und führen Sie dann die Schritte aus, die den ersten Schritten zum Überprüfen der Einrichtung des Geschäfts folgen:

1.  Starten Sie Windows Media Player, und warten Sie einige Sekunden, um die neueste AllServices.xml-Datei zu erhalten.
2.  Klicken Sie zum Auswählen eines Onlineshops für Windows XP und Windows Vista zunächst auf die Registerkarte, die zwischen der Ansicht Medienleitfaden und der Ansicht Onlineshops aufgeteilt ist. Klicken Sie dann im Menü auf **Alle Onlineshops durchsuchen,** und wählen Sie den Store aus, indem Sie in der Liste der Filialen auf das zugehörige Symbol klicken. Klicken Sie für Windows 7 auf die Schaltfläche im Bibliotheksnavigationsbereich, die sich zwischen der Schaltfläche **Medienleitfaden** und der Schaltfläche **Onlineshops** befindet. Klicken Sie dann im Menü auf **Alle Onlineshops durchsuchen,** und wählen Sie den Store aus, indem Sie in der Liste der Filialen auf das zugehörige Symbol klicken.

    Der folgende Screenshot zeigt, wie Sie einen Onlineshop in Windows Media Player 11 auswählen:

    ![Screenshot: Auswählen eines Onlineshops in Windows Media Player 11](images/wmp11-set-store.png)

    Der folgende Screenshot zeigt, wie Sie eine Online-Store in Windows Media Player 12 auswählen:

    ![Screenshot: Auswählen eines Onlineshops in Windows Media Player 12](images/wmp12-set-store.png)

3.  Befolgen Sie die Anweisungen aus dem Store, um zusätzliche Software zu installieren, die für die Verwendung des Speichers erforderlich ist.

**So überprüfen Sie die Speichereinrichtung**

1.  Überprüfen Sie, ob die Software installiert ist.

    Stellen Sie sicher, dass das OCX-Plug-In oder eine andere Software aus dem Store ohne Fehler heruntergeladen und installiert wird.

2.  Überprüfen Sie, ob die Software deinstalliert wird.

    Vergewissern Sie sich, dass in Systemsteuerung im Element **Programme und Features** die software, die der Speicher installiert, in der Liste Programm deinstallieren oder **ändern** angezeigt wird, und vergewissern Sie sich, dass Sie sie ohne Fehler aus dieser Liste deinstallieren können.

3.  Vergewissern Sie sich, dass die Software nicht in der Taskleiste ausgeführt wird.

    Vergewissern Sie sich, dass keine software aus dem Store Symbole zum Programmbenachrichtigungsbereich (auf der Taskleiste links neben der Uhr) hinzufügt, bevor der Kunde seine Zustimmung zum Herunterladen von Storesoftware erteilt.

    Die grundlegende Speichererfahrung sollte keine Installation zusätzlicher Software erfordern. Eine grundlegende Medienerfahrung, z. B. Streamingmedien, sollte verfügbar sein. Einige Stores installieren zusätzliche Software, z. B. Download-Manager für eine erstklassige Medienerfahrung. Diese Speicher können symbole in der Taskleiste enthalten, wenn die Symbole Anwendungen darstellen, die von Windows Media Player getrennt sind.

4.  Überprüfen Sie, ob die Registerkarte "Store" funktioniert.

    Vergewissern Sie sich, dass sich die Registerkarte "Store" ändert, um den ausgewählten Speicher anzugeben.

    Vergewissern Sie sich bei Windows XP und Windows Vista mit Windows Media Player 11, dass der Geschäftsname und das Symbol im dunklen Windows Media Player 11-Hintergrund sichtbar sind.

    Überprüfen Sie für Windows 7 mit Windows Media Player 12, ob der Speichername und das Symbol im Bibliotheksnavigationsbereich im Kontextmenü der Dienstauswahl angezeigt werden.

    Vergewissern Sie sich, dass der Store oben in der Liste der Storeselektoren im Menü aufgeführt ist.

    > [!Note]  
    > Es gibt keine **Menüoption Aktuellen Dienst zu Menü hinzufügen,** wenn der Speicher Typ 2 der ausgewählte (Standard-)Speicher für die Region ist.

     

    Der folgende Screenshot zeigt das Menü, das angezeigt wird, wenn Sie auf die Registerkarte in der oberen rechten Ecke von Windows Media Player 11 klicken:

    ![Screenshot: Registerkarte "Store" in Windows Media Player 11](images/wmp11-verify-store.png)

    Der folgende Screenshot zeigt das Menü, das angezeigt wird, wenn Sie in der unteren linken Ecke von Windows Media Player 12 auf die Schaltfläche "Teilen" klicken:

    ![Screenshot der Registerkarte "Store" in Windows Media Player 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a>Erstellen eines Kontos

**So überprüfen Sie die Kontoeinrichtung**

1.  Vergewissern Sie sich, dass der Store über eine Option zum Erstellen eines neuen Kontos verfügt, und befolgen Sie dann die Anweisungen zum Erstellen eines neuen Kontos.

    Im folgenden Screenshot wird die Schaltfläche **Neues Konto erstellen** hervorgehoben, wie sie möglicherweise in Windows Media Player 11 angezeigt wird:

    ![Screenshot: Überprüfen der Kontoeinrichtung für Windows Media Player 11](images/wmp11-verify-account.png)

    Im folgenden Screenshot wird die Schaltfläche **Neues Konto erstellen** hervorgehoben, da sie möglicherweise in Windows Media Player 12 angezeigt wird:

    ![Screenshot: Überprüfen der Kontoeinrichtung für Windows Media Player 12](images/wmp12-verify-account.png)

2.  Vergewissern Sie sich, dass Sie sich bei dem konto anmelden können, das Sie erstellt haben.

### <a name="setting-up-credential-caching"></a>Einrichten der Zwischenspeicherung von Anmeldeinformationen

Führen Sie zunächst die folgenden Schritte aus, um das Zwischenspeichern von Anmeldeinformationen einzurichten, und führen Sie dann die Schritte aus, die den ersten Schritten folgen, um das Setup für die Zwischenspeicherung von Anmeldeinformationen zu überprüfen:

1.  Geben Sie auf der Anmeldeseite Anmeldeinformationen ein, und wählen Sie die Option zum Speichern von Benutzerinformationen aus.
2.  Stellen Sie sicher, dass die Anmeldeseite über ein Kontrollkästchen verfügt, mit dem der Benutzer Anmeldeinformationen zwischenspeichern kann.
3.  Das zwischenspeichern von optionalen Anmeldeinformationen ist ein wichtiger Sicherheitspunkt. Die automatische Zwischenspeicherung von Anmeldeinformationen kann personenbezogene Informationen von Benutzern verfügbar machen, die sich bei einem freigegebenen oder öffentlichen Computer anmelden. Sie sollten Kundeninformationen schützen, indem Sie ein Kontrollkästchen aktivieren, das die Zwischenspeicherung optional rendert.

**So überprüfen Sie die Zwischenspeicherung von Anmeldeinformationen**

1.  Vergewissern Sie sich, dass der Speicher über ein Kontrollkästchen für die Option **Benutzerinformationen speichern** verfügt.

    1.  Schließen Sie Windows Media Player.
    2.  Öffnen Sie Windows Media Player erneut, und versuchen Sie, Inhalte herunterzuladen.

2.  Vergewissern Sie sich, dass die Zwischenspeicherung von Anmeldeinformationen vorhanden ist und funktioniert.

    1.  Melden Sie sich vom Store ab.
    2.  Schließen Sie Windows Media Player.
    3.  Öffnen Sie Windows Media Player erneut, und versuchen Sie, Inhalte herunterzuladen.

3.  Vergewissern Sie sich, dass der Benutzer zur Eingabe von Anmeldeinformationen aufgefordert wird, wenn er nicht zwischengespeichert wird.

    Nach der Abmeldung und dem Versuch, den Store zu verwenden, sollte der Kunde zur Eingabe von Anmeldeinformationen aufgefordert werden.

## <a name="content-acquisition"></a>Inhaltserfassung

In diesem Abschnitt werden die verschiedenen Möglichkeiten zum Abrufen von Inhalten und die Überprüfung beschrieben, ob der Inhalt erworben wurde.

### <a name="streaming-content"></a>Streaminginhalt

Streamen Sie alle verfügbaren Inhaltstypen aus dem Speicher. Beispiel: Streamen von Radio, Video, Audio und Vorschau von Inhalten.

**So überprüfen Sie Streaminginhalte**

1.  Überprüfen Sie, ob alle verfügbaren Inhaltsstreamtypen verfügbar sind.

2.  Stellen Sie sicher, dass Der Inhalt in Windows Media Player und nicht in einem anderen Player oder Steuerelement wiedergegeben wird.

### <a name="obtaining-content"></a>Abrufen von Inhalten

Führen Sie zunächst die folgenden Schritte aus, um Inhalte zu erwerben, und führen Sie dann die Schritte aus, die den ersten Schritten folgen, um den Kauf zu überprüfen und zu überprüfen, ob der Inhalt heruntergeladen wurde:

1.  Starten Sie Windows Media Player.
2.  Melden Sie sich beim Testkonto an.
3.  Navigieren Sie zu dem zu erwerbende Inhalt.
4.  Befolgen Sie das storespezifische Verfahren zum Erwerben von Inhalten.

**So überprüfen Sie erworbene und heruntergeladene Inhalte**

1.  Überprüfen Sie, ob der berechnete Preis richtig ist.

    Überprüfen Sie, ob der Preis korrekt ist, insbesondere wenn Sie mehrere Inhaltsteile gleichzeitig erwerben, und überprüfen Sie, ob alle Kontostandsinformationen nach dem Kauf ordnungsgemäß aktualisiert werden. Einige Inhalte können als einzelne Titel und andere nur als Alben erworben werden. Stellen Sie sicher, dass der Albumpreis nicht größer als die Summe der einzelnen Spuren ist.

2.  Überprüfen Sie, ob die erworbenen Inhalte in die Bibliothek heruntergeladen werden.

    Navigieren Sie nach Abschluss des Downloads zu dem heruntergeladenen Inhalt in der Windows Media Player Bibliothek. Der heruntergeladene Inhalt befindet sich in der Bibliothek des aktuellen Benutzers.

    -   Für Windows XP und Windows Vista mit Windows Media Player 11 wird heruntergeladener Inhalt im Bibliotheksnavigationsbereich unter Bibliothekspivot und dann unter **Hits** angezeigt. 
    -   Für Windows 7 mit Windows Media Player 12 wird Inhalt, der in die Windows Media Player-Bibliothek heruntergeladen wird, im navigationsbereich Windows Media Player unter **Musik** angezeigt.

3.  Überprüfen Sie, ob Metadaten für den Kauf heruntergeladen werden.

    Stellen Sie sicher, dass die folgenden Spalten in der bibliothek Windows Media Player angezeigt werden (fügen Sie sie hinzu, falls nicht):

    -   Albumartist
    -   Titel
    -   Albumtitel
    -   Inhaltsanbieter
    -   Genre

    Die vorangehenden Spalten müssen aufgefüllt werden. Inhalte sollten über Albumart verfügen. Die Albumart ist jedoch nicht erforderlich, um Validierungstests zu bestehen.

4.  Vergewissern Sie sich, dass die Mediennutzungsrechte für den Kauf korrekt sind.

    Klicken Sie für jede heruntergeladene Spur mit der rechten Maustaste auf die Spur, und wählen Sie **Eigenschaften** und dann die Registerkarte **Mediennutzungsrechte** aus.

    Der Speicher kann seine Inhalte mit Mediennutzungsrechten schützen oder den Inhalt nicht schützen. Die Registerkarte **Mediennutzungsrechte** gibt diesen Status entweder durch Auflisten der Einschränkungen oder durch Angabe an, dass der Inhalt nicht geschützt ist. Der Speicher muss seinen aktuellen Plan für Mediennutzungsrechte kommunizieren. Sie müssen die tatsächlichen Ergebnisse anhand dieses erwarteten Verhaltens überprüfen.

    Lizenzen für Medienrechte müssen vorab übermittelt werden. Der Kunde muss den Inhalt nicht wiedergeben oder einen anderen Prozess durchlaufen, um die Lizenz zu erhalten. Sie müssen die spezifischen Mediennutzungsrechte mit dem vergleichen, was der Store dem Kunden entsprechend mitgeteilt hat. Rechte müssen auf mindestens zwei andere Computer übertragen werden können. Kunden müssen in der Lage sein, ihre Medien zu verbrauchen und zu synchronisieren.

    Der folgende Screenshot zeigt die Mediennutzungsrechte einer geschützten Datei:

    ![Screenshot der Mediennutzungsrechte für eine geschützte Datei](images/media-rights-protected.png)

    Wenn der Inhalt nicht geschützt ist, wird dies auf der Registerkarte **Mediennutzungsrechte** angezeigt.

    Der folgende Screenshot zeigt die Mediennutzungsrechte einer nicht geschützten Datei:

    ![Screenshot mit den Mediennutzungsrechten für eine nicht geschützte Datei](images/media-rights-not-protected.png)

5.  Vergewissern Sie sich, dass der erworbene Inhalt wiedergegeben wird.

    Vergewissern Sie sich, dass heruntergeladene Inhalte in Windows Media Player wiedergegeben werden.

    Wiedergeben von Inhalten, die aus dem Store erworben wurden und sich in der lokalen Bibliothek befinden, oder Streamen einer Vorschau.

    Führen Sie die folgenden Schritte aus, um Inhalte in Windows XP und Windows Vista mit Windows Media Player 11 zu erwerben:

    1.  Klicken Sie auf die Registerkarte **Jetzt wiedergeben.**
    2.  Positionieren Sie im Listenbereich den Mauszeiger, um mit dem Mauszeiger auf die Albumart zu zeigen, um den Link **Kaufen** anzuzeigen.
    3.  Klicken Sie auf **Kaufen.**

    Der folgende Screenshot zeigt den Speicherort des Links **Kaufen** in Windows Media Player 11:

    ![Screenshot: Kaufen von Inhalten in Windows Media Player 11](images/wmp11-verify-buy-play.png)

    Führen Sie die folgenden Schritte aus, um Inhalte in Windows 7 mit Windows Media Player 12 zu erwerben:

    1.  Klicken Sie im Bibliotheksmodus auf die Registerkarte **Wiedergeben.**
    2.  Klicken Sie in der Wiedergabeliste unter der Albumart auf **Shop**

    Der folgende Screenshot zeigt, wie Sie Inhalte in Windows Media Player 12 kaufen:

    ![Screenshot: Kaufen von Inhalten in Windows Media Player 12](images/wmp12-verify-buy-play.png)

6.  Vergewissern Sie sich, dass durch Klicken auf **Kaufen** oder **Geschäft** zum Store gewechselt wird.

    Die Windows Media Player sollte zum Store in der Bibliotheksansicht wechseln und die Kauferfahrung des Geschäfts laden.

    Anschließend müssen Sie mit dem Erwerb der Spur fortfahren.

7.  Stellen Sie sicher, dass der Inhalt heruntergeladen wird, nachdem Sie auf **Kaufen** oder **Kaufen** geklickt haben.

    Vergewissern Sie sich, dass die Mediennutzungsrechte für den erworbenen Inhalt und die zugehörigen Metadaten geeignet sind, und überprüfen Sie, ob die Spur wiedergegeben wird. Im Allgemeinen sollte diese Kaufmethode die gleichen Ergebnisse wie andere Methoden haben.

### <a name="burning-content"></a>Inhaltsinhalt

Führen Sie zunächst die folgenden Schritte aus, um erworbene Inhalte zu kopieren (kopieren Sie erworbene Inhalte auf eine beschreibbare CD oder DVD), und führen Sie dann die Schritte aus, die den ersten Schritten folgen, um zu überprüfen, ob der Inhalt verbraucht wird:

> [!Note]  
> Bevor Sie eine erworbene Spur verwerten, notieren Sie sich deren Anzahl, damit Sie später überprüfen können, ob die Anzahl nach dem Verbrauch der Spur dekrementiert wird.

 

1.  Klicken Sie auf die Registerkarte **"Burn".**
2.  Ziehen Sie erworbene Spuren in die **Burn List**.
3.  Klicken Sie auf die Schaltfläche **Burn starten.**

Der folgende Screenshot zeigt die **Brandliste** auf der rechten Seite des Bildschirms und die Schaltfläche **"Burn starten"** unterhalb der **Brandliste** in Windows Media Player 11:

![Screenshot, der zeigt, wie Inhalte in Windows Media Player 11 verbraucht werden](images/wmp11-verify-burn.png)

Der folgende Screenshot zeigt, wie die Brandliste in Windows Media Player 12 angezeigt wird, nachdem Sie eine Spur in die Brandliste gezogen haben, und es wird die Schaltfläche **"Burn starten"** oben auf der Registerkarte **"Burn"** angezeigt:

![Screenshot, der zeigt, wie Inhalte in Windows Media Player 12 verbraucht werden](images/wmp12-verify-burn.png)

**So überprüfen Sie, ob erworbene Inhalte verbraucht werden können**

1.  Vergewissern Sie sich, dass der erworbene Inhalt abgespielt wird, indem Sie die CD oder DVD nach Abschluss des Vorgangs wiedergeben.

2.  Vergewissern Sie sich, dass die Anzahl der Burns dekrementiert ist.

    Navigieren Sie zur Bibliothek, und öffnen Sie die Mediennutzungsrechte für eine erworbene Spur, die in Brand geraten ist.

    Wenn die Anzahl der Verätzungen einer Spur begrenzt ist, stellen Sie sicher, dass diese Anzahl nach dem Brand der Spur abnimmt.

### <a name="transferring-content"></a>Übertragen von Inhalten

Übertragen von Inhalten auf einen anderen Computer.

**So überprüfen Sie, ob erworbene Inhalte auf einen anderen Computer übertragen werden können**

-   Wenn der Speicher das Übertragen von Inhalten auf einen anderen Computer zulässt, übertragen Sie den Inhalt auf mindestens zwei Computer.

Führen Sie zunächst die folgenden Schritte aus, um eine Synchronisierung mit einem Gerät durchzuführen und erworbene Inhalte auf dieses Gerät zu übertragen, und führen Sie dann die Schritte aus, die den ersten Schritten folgen, um zu überprüfen, ob der Inhalt übertragen wird:

> [!Note]  
> Bevor Sie eine erworbene Spur übertragen, notieren Sie sich die Synchronisierungsanzahl, damit Sie später überprüfen können, ob die Anzahl nach der Übertragung der Spur dekrementiert wird.

 

1.  Verbinden ein Gerät mit einer sicheren Uhr. Beispiele hierfür sind Geräte, die Windows Medien-DRM für portable Geräte verwenden, z. B. ein portables Mediencenter wie iRiver H10, Creative Zen usw.
2.  Klicken Sie in Windows Media Player auf die Registerkarte **Synchronisieren.**
3.  Ziehen Sie Inhalt aus der Bibliothek in den **Listenbereich Synchronisierung** auf der Registerkarte **Synchronisierung.**
4.  Klicken Sie auf die Schaltfläche **Synchronisierung starten.**

Der folgende Screenshot zeigt Track 1 im **Listenbereich Synchronisierung** und die Schaltfläche **Synchronisierung starten** in Windows Media Player 11:

![Screenshot: Übertragen von Inhalten in Windows Media Player 11](images/wmp11-verify-transfer.png)

Der folgende Screenshot zeigt Track 1 im **Listenbereich Synchronisierung** und die Schaltfläche **Synchronisierung starten** in Windows Media Player 12:

![Screenshot: Übertragen von Inhalten in Windows Media Player 12](images/wmp12-verify-transfer.png)

**So überprüfen Sie, ob erworbene Inhalte auf ein anderes Gerät übertragen werden können**

1.  Überprüfen Sie, ob der erworbene Inhalt auf das Gerät übertragen wird, indem Sie den Inhalt auf dem Gerät wiedergeben. Der übertragene Inhalt muss auch über entsprechende Metadaten verfügen.

2.  Überprüfen Sie, ob die Synchronisierungsanzahl dekrementiert ist.

    Navigieren Sie zur Bibliothek, und öffnen Sie die Mediennutzungsrechte für eine übertragene Spur.

    Wenn die Anzahl der Synchronisierungen einer Spur begrenzt ist, überprüfen Sie, ob diese Anzahl abnimmt, wenn die Spur übertragen wird.

## <a name="store-features"></a>Store Funktionen

In den folgenden Abschnitten wird beschrieben, wie Verschiedene Features eines online geschalteten Onlineshops getestet werden.

### <a name="managing-an-account"></a>Verwalten eines Kontos

Melden Sie sich mit einem Konto an, das einige Käufe getätigt hat, und öffnen Sie den Kaufverlauf.

**So überprüfen Sie den Kaufverlauf**

-   Überprüfen Sie, ob der Kaufverlauf vorherige Käufe nachzeichnet.

Wenn der Store- oder Kontotyp dieses Feature unterstützt, versuchen Sie, einen gelöschten Kauf wiederherzustellen.

**So überprüfen Sie, ob vorherige Käufe erneut erworben werden können**

-   Vergewissern Sie sich, dass ein vorheriger Kauf wiederhergestellt werden kann.

Wenn der Speicher die Verwendung mehrerer Computer mit dem Konto unterstützt, überprüfen Sie alle Funktionen, die dieses Feature bereitstellt.

**So überprüfen Sie die Verwaltung mehrerer Computer mit einem einzigen Konto**

-   Überprüfen Sie die Funktionalität des Speichers, um mehrere Computer zu verwalten.

### <a name="managing-a-store-specific-account"></a>Verwalten eines Store-Specific-Kontos

Der Speicher weist möglicherweise keine typischen Kontotypen, Einschränkungen oder Inhalte auf. Ein Laden, in dem Streamingvideos geliehen werden, benötigt beispielsweise eine Benutzeroberfläche, um aktive Verleihe anzuzeigen, und diese Benutzeroberfläche müsste getestet werden.

> [!Note]  
> Obwohl Microsoft storespezifische Kontofunktionen nicht zertifizieren kann, sollten Sie diese Funktionalität testen, um eine gute Kundenerfahrung sicherzustellen.

 

### <a name="managing-the-info-center"></a>Verwalten des Infocenters

Führen Sie zunächst die folgenden Schritte aus, um sich auf das Testen des Standardzustands vorzubereiten, und führen Sie dann den nächsten Schritt aus, der auf die ersten Schritte folgt, um zu überprüfen, ob das Infocenter standardmäßig deaktiviert ist:

1.  Wiedergeben von Inhalten aus dem Store.
2.  Wechseln Sie zum Modus Jetzt wiedergeben. Klicken Sie in Windows XP oder Windows Vista mit Windows Media Player 11 auf die Registerkarte **Jetzt wiedergeben.** Klicken Sie in Windows 7 mit Windows Media Player 12 in der unteren rechten Ecke auf die Schaltfläche **Jetzt wiedergeben.**

**So überprüfen Sie, ob das Infocenter standardmäßig deaktiviert ist**

-   Vergewissern Sie sich, dass das Infocenter standardmäßig deaktiviert ist.

Wenn der Store eine InfoCenter-Ansicht bietet, können Sie Inhalte aus dem Store wiedergeben, und während der Inhalt wiedergegeben wird, wechseln Sie zum Modus Jetzt wiedergeben, und aktivieren Sie das Infocenter.

Klicken Sie in Windows XP oder Windows Vista mit Windows Media Player 11 mit der rechten Maustaste auf das jetzt wiedergegebene Fenster, und wählen Sie dann im Kontextmenü **infocenteransicht** aus.

Der folgende Screenshot zeigt das Kontextmenü in Windows Media Player 11:

![Screenshot: Zugreifen auf das Infocenter eines Geschäfts in Windows Media Player 11](images/wmp11-info-center.png)

Klicken Sie in Windows 7 mit Windows Media Player 12 mit der rechten Maustaste auf das jetzt wiedergegebene Fenster, wählen Sie im Kontextmenü **Visualisierungen** aus, und klicken Sie dann auf **Infocenteransicht.**

Der folgende Screenshot zeigt das Kontextmenü in Windows Media Player 12:

![Screenshot: Zugreifen auf das Infocenter eines Geschäfts in Windows Media Player 12](images/wmp12-info-center.png)

**So überprüfen Sie, ob das Infocenter funktionsfähig ist**

-   Vergewissern Sie sich, dass im Infocenter Medieninformationen im bereich "Jetzt wiedergegeben" angezeigt werden. Der folgende Screenshot zeigt ein Beispiel für solche Medieninformationen:

    ![Screenshot der Funktionalität des Infocenters eines Geschäfts](images/media-information.png)

Wenn Kauflinks oder andere Links auf der Seite angezeigt werden, klicken Sie auf die Links.

**So überprüfen Sie Links in der Info Center-Ansicht**

-   Überprüfen Sie, ob der Speicher unter den Links angezeigt wird.

    Der Windows Media Player sollte zum Speicher in seiner Bibliothek wechseln.

## <a name="store-interaction"></a>Store Interaktion

In den folgenden Abschnitten wird beschrieben, wie Sie die Interaktion zwischen den anderen Stores und dem zu testden Store testen.

### <a name="yielding-to-the-active-store"></a>An die aktive Store

Wechseln Sie zu einem anderen Speicher als dem zu testbaren Store.

**So überprüfen Sie, ob das Ergebnis an den aktiven Speicher geht**

-   Überprüfen Sie, ob der getestete Speicher dem aktiven Speicher ergibt.

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a>Verhindern der Übernahme des aktiven Store durch den getesteten Store

-   Wenn ein anderer Speicher ausgewählt ist, schließen Sie Windows Media Player, und starten Sie den Computer neu.
-   Starten Sie Windows Media Player.

**So überprüfen Sie, ob der getestete Speicher nicht übernimmt**

-   Vergewissern Sie sich, dass der zuletzt aktive Speicher angezeigt wird und dass der getestete Speicher nicht angezeigt wird.

### <a name="accessing-a-store-in-high-contrast-mode"></a>Zugreifen auf eine Store im High-Contrast-Modus

Aktivieren Sie zunächst den Modus für hohen Kontrast, indem Sie LEFT SHIFT+LEFT ALT+PRINT SCREEN drücken, und führen Sie dann die folgenden Schritte aus, um die Barrierefreiheit mit hohem Kontrast zu überprüfen:

**So überprüfen Sie, ob auf den Speicher im Modus mit hohem Kontrast zugegriffen werden kann**

1.  Vergewissern Sie sich, dass die Anmeldebenutzeroberfläche intakt und funktionsfähig ist.
2.  Vergewissern Sie sich, dass alle Fenster und Dialogfelder ordnungsgemäß angezeigt werden.
3.  Kaufmedien. Vergewissern Sie sich, dass Schaltflächen für Kauf und Download, Download-Manager, Preisinformationen usw. angezeigt werden.
4.  Vergewissern Sie sich, dass Sie streamen, verbrauchen und synchronisieren können.
5.  Suchen Sie nach abgeschnittenen Text- und Benutzeroberflächenelementen, nicht lesbaren Text und anderen sichtbaren Fehlern.

### <a name="securing-a-store"></a>Sichern eines Store

Führen Sie die folgenden Schritte aus, um die Kontosicherheit zu überprüfen:

**So überprüfen Sie die Kontosicherheit**

1.  Geben Sie auf der Anmeldeseite und im Dialogfeld falsch formatierte Kontoinformationen ein, und vergewissern Sie sich, dass sie vom Speicher abgelehnt werden.
2.  Melden Sie sich an, zeigen Sie die Kontoseite an, und melden Sie sich ab.
3.  Klicken Sie in Windows Media Player auf die Schaltfläche Zurück, und vergewissern Sie sich, dass die vorherigen Benutzerkontoinformationen nicht angezeigt werden.

 

 




