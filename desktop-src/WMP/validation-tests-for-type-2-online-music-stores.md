---
title: Validierungs Tests für den onboardingtyp 2 Online Stores
description: In diesem Thema werden Tests beschrieben, die von Microsoft zum Überprüfen des Online Store vom Typ 2 durchgeführt werden. Microsoft erfordert, dass Sie diese Tests ausführen, bevor Sie eine Release Candidate senden. Ihr Online Shop muss die zu veröffentlichenden Tests erfolgreich durchlaufen.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388360"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a>Validierungs Tests für den onboardingtyp 2 Online Stores

In diesem Thema werden Tests beschrieben, die von Microsoft zum Überprüfen des Online Store vom Typ 2 durchgeführt werden. Microsoft erfordert, dass Sie diese Tests ausführen, bevor Sie eine Release Candidate senden. Ihr Online Shop muss die zu veröffentlichenden Tests erfolgreich durchlaufen.

> [!Note]  
> Wenn Ihr Speicher vom Typ 1 und nicht vom Typ 2 ist, können Sie dieses Thema als Richtlinie verwenden, um den Umfang der für den Speicher vom Typ 1 behandelten Zertifizierungstests zu verstehen. Wenden Sie sich an [Microsoft-Support](https://support.microsoft.com/ph/7763#tab0), um einen umfassenden Satz von Tests für Speicher vom Typ 1 zu erhalten.

 

Dieses Thema enthält folgende Abschnitte:

-   [Test Checkliste](#test-checklist)
    -   [Test Durchlauf Vorbereitung](#test-pass-preparation)
-   [Test Umgebung](#test-environment)
-   [Konfiguration und Einrichtung](#configuration-and-setup)
    -   [Einrichten eines Test Computers](#setting-up-a-test-machine)
    -   [Einrichten eines Stores](#setting-up-a-store)
    -   [Erstellen eines Kontos](#creating-an-account)
    -   [Einrichten der Zwischenspeicherung von Anmelde Informationen](#setting-up-credential-caching)
-   [Inhalts Erfassung](#content-acquisition)
    -   [Streaming von Inhalten](#streaming-content)
    -   [Abrufen von Inhalten](#obtaining-content)
    -   [Brennen von Inhalten](#burning-content)
    -   [Inhalt wird übertragen](#transferring-content)
-   [Store-Features](#store-features)
    -   [Verwalten eines Kontos](#managing-an-account)
    -   [Verwalten des Info Centers](#managing-the-info-center)
-   [Speichern der Interaktion](#store-interaction)
    -   [Ergebnis des aktiven Stores](#yielding-to-the-active-store)
    -   [Verhindern, dass der getestete Speicher den aktiven Speicher übernimmt](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [Zugreifen auf einen Speicher im High-Contrast Modus](#accessing-a-store-in-high-contrast-mode)
    -   [Sichern eines Stores](#securing-a-store)

## <a name="test-checklist"></a>Test Checkliste

Verwenden Sie die Prüfliste in der folgenden Tabelle, um den Typ 2-Online Shop zu validieren, den Sie in die Platine bringen möchten.



Test

Windows XP

Windows Vista

Windows 7

Ergebnis (erfolgreich/Fehler/nicht zutreffend)

32

64

32

64

32

64

1. Überprüfen Sie die Installation von Software.

2. Überprüfen Sie, ob Software deinstalliert wird.

3. Vergewissern Sie sich, dass die Software nicht in der Taskleiste ausgeführt wird.

4. Überprüfen Sie, ob die Registerkarte Store funktioniert.

5. Vergewissern Sie sich, dass der Speicher über eine Option zum Erstellen eines neuen Kontos verfügt.

6. Vergewissern Sie sich, dass sich das erstellte Konto anmelden kann.

7. Vergewissern Sie sich, dass der Speicher über eine Option zum Speichern von Benutzerinformationen verfügt.

8. Überprüfen Sie, ob das Zwischenspeichern von Anmelde Informationen vorhanden ist und funktioniert

9. Vergewissern Sie sich, dass der Benutzer zur Eingabe von Anmelde Informationen aufgefordert wird

10. Überprüfen Sie, ob alle verfügbaren Typen von Inhaltsstream vorhanden

11. Überprüfen Sie, ob die Inhalte in Microsoft Windows Media Player abgespielt werden.

12. Überprüfen Sie, ob ein berechneter Preis richtig ist.

13. Überprüfen Sie, ob erworbene Inhalte in die Bibliothek heruntergeladen wurden.

14. Vergewissern Sie sich, dass die Metadaten für den Einkauf heruntergeladen werden.

15. Überprüfen Sie, ob die Medien Nutzungsrechte für den Kauf korrekt sind.

16. Überprüfen Sie, ob die erworbenen Inhalte wiedergegeben werden können

17. Vergewissern Sie sich, dass durch Klicken auf **die Schaltfläche** **kaufen oder kaufen** zum Store gewechselt wird.

18. Überprüfen Sie, ob erworbene Inhalte heruntergeladen wurden

19. Überprüfen Sie, ob erworbene Inhalte gebrannt werden können.

20. Vergewissern Sie sich, dass die Anzahl der Verbrennungen verringert wird.

21. Überprüfen Sie, ob Inhalt auf einen anderen Computer übertragen werden kann.

22. Überprüfen Sie, ob Inhalt an ein Gerät übertragen wird

23. Vergewissern Sie sich, dass die Synchronisierungs Anzahl dekrementiert wird.

24. Vergewissern Sie sich, dass der Kaufverlauf vorherige Käufe nachverfolgt.

25. Überprüfen Sie, ob ein vorheriger Kauf wieder hergestellt werden kann.

26. Überprüfen Sie die Funktionalität eines Stores, um mehrere Computer zu verwalten.

27. Vergewissern Sie sich, dass das Info Center standardmäßig deaktiviert ist.

28. Überprüfen Sie, ob das Info Center über Medieninformationen im Bereich der nun Wiedergabe verfügt.

29. Überprüfen Sie, ob die Links zum Speicher navigieren.

30. Vergewissern Sie sich, dass der getestete Speicher den aktiven Speicher liefert.

31. Vergewissern Sie sich, dass der getestete Speicher den aktuellen Speicher nicht übernehmen kann.

32. Vergewissern Sie sich, dass der Speicher im Modus mit hohem Kontrast verfügbar ist.

33. Vergewissern Sie sich, dass der Speicher sicher ist.



 

### <a name="test-pass-preparation"></a>Test Durchlauf Vorbereitung

Bevor Sie einen Test Durchlauf ausführen, sollten Sie sicherstellen, dass die Speicher-und Testkonten zum Testen bereit sind. Sie sollten die folgenden Informationen bestimmen, bevor der Pass gestartet wird. Wenn Sie die Informationen einige Tage vor dem Test Durchlauf ermitteln können, wird der Durchlauf effizienter ausgeführt.

-   Bestimmen Sie die folgenden Informationen zu Testkonten, die vom Speicher bereitgestellt werden:
    -   Konten und Kenn Wörter funktionieren, damit sich ein Benutzer anmelden kann
    -   Konten werden für jeden Typ von Geschäfts Modus, den der Store anbietet, ordnungsgemäß und angemessen finanziert.
    -   Konten sind für alle zu testenden Gebiets Schemas gültig, oder für jedes Gebiets Schema sind Konten vorhanden, wenn Konten keine Gebiets Schema übergreifende
-   Bestimmen Sie, welche Gebiets Schemata getestet werden sollen.
-   Bestimmen Sie, welche Sprachen getestet werden sollen.
-   Bestimmen Sie die folgenden Informationen zur Testumgebung:

    -   Live Stores, die mit Windows XP, Windows Vista und Windows 7 zusammenarbeiten
    -   Der zu testende nicht-Live Store
    -   Vergewissern Sie sich, dass der zu testende Non-Live Store in allen Versionen des Betriebssystems und allen Versionen der Windows Media Player-Plattform sichtbar ist.

-   Bestimmen Sie die folgenden Informationen zum zu testenden Speicher:

    -   Name des Datenspeichers
    -   Erwartete Logo Grafiken und Bezeichnung für Store-Registerkarten
    -   Ist der Speicher für alle Betriebssystemversionen Live?
    -   Handelt es sich hierbei um eine neue Version des zu testenden Stores?
    -   Wird der zu testende Speicher vom Typ 1 oder vom Typ 2 gespeichert?
    -   Hat sich der Store-Typ geändert?

-   Bestimmen Sie, auf welchen Betriebssystemversionen und Plattformen Sie den Speicher testen möchten.
-   Stellen Sie fest, dass das Installationsprogramm und das Plug-in auf allen zu testenden Betriebssystemversionen und-Plattformen funktionieren.
-   Stellen Sie fest, ob ein Navigations Dokument erforderlich ist.
-   Bestimmen Sie die folgenden Informationen zu den Medien, die im Store angeboten werden:

    -   Formate
    -   Ist eine proprietäre Software erforderlich?
    -   Müssen Sie alle Medientypen oder nur eine Teilmenge der Medientypen testen?

-   Bestimmen Sie die folgenden Informationen zu den Medien Nutzungsrechten:

    -   Verfügen die Store-Medien über Inhalts Schutz?
    -   Wenn dies der Fall ist, bestimmen Sie den Typ des Inhalts Schutzes, den die Medien besitzen.
    -   Wenn dies der Fall ist, bestimmen Sie das erwartete geschützte Verhalten.
    -   Beinhalten die Nutzungsrechte für die Medien die Computer-zu-Computer-Freigabe?
    -   Die Synchronisierungs Rechte
    -   Die Verbrauchs Rechte
    -   Die Wiedergabe Rechte
    -   Die Ablaufdatums Angaben (sofern vorhanden).

-   Stellen Sie fest, ob Sie über ausreichend Medien (einen ausreichend großen Katalog) verfügen, um ein aussagekräftiges Beispiel zu erhalten.
-   Bestimmen Sie, was der Phasen Durchlauf ist: RC 0, Compliance usw.
-   Bestimmen Sie, ob es sich bei dem Test Durchlauf um einen bestimmten Typ handelt: Regression, Rauch usw.

## <a name="test-environment"></a>Testumgebung

Sie müssen Tests für die folgenden Konfigurationen durchführen:

-   Microsoft Windows Media Player 11 unter Windows XP mit Service Pack 3 (SP3) 32-Bit-und 64-Bit-Betriebssystemen
-   Windows Media Player 11 unter Windows Vista 32-Bit-und 64-Bit-Betriebssysteme (32-Bit Windows Media Player)
-   Betriebssysteme Microsoft Windows Media Player 12 auf Windows 7 32-Bit und 64-Bit (32-Bit Windows Media Player)

Obwohl Sie Tests für alle aufgeführten Betriebssystemversionen und Plattformen durchführen müssen, sind die 32-Bit-Versionen von Windows Vista und Windows 7 die Prioritäts orientierten Betriebssystemversionen. Sie müssen die Installation von Software auf allen Plattformen testen.

In den Screenshots in diesem Thema wird die Verwendung der Benutzeroberfläche mithilfe eines fiktiven Stores (Proseware) veranschaulicht.

## <a name="configuration-and-setup"></a>Konfiguration und Setup

In den folgenden Abschnitten wird beschrieben, wie Sie Validierungstests für den Online Shop eines Typs 2 konfigurieren und einrichten.

### <a name="setting-up-a-test-machine"></a>Einrichten eines Test Computers

Führen Sie die folgenden Schritte aus, um einen Testcomputer einzurichten:

1.  Zeigen Sie den Testcomputer auf Inhalts Testserver, indem Sie einen Speicher spezifischen Registrierungsschlüssel hinzufügen.
2.  Legen Sie die Werte im Dialogfeld Regions **-und Sprachoptionen** auf die richtigen sprach-und Gebiets Schema Einstellungen fest. Um die Sprache festzulegen, wählen Sie die Registerkarte **Formate** aus, und wählen Sie dann die Sprache aus dem Kombinations Feld **Aktuelles Format** aus. Um den Bereich festzulegen, wählen Sie die Registerkarte **Speicherort** aus, und wählen Sie dann die Region im Kombinations Feld **Aktueller Speicherort** aus. Außerdem müssen Sie für Speicher, die eine Installation eines Plug-ins oder einer Speicher spezifischen, benutzerdefinierten Software erfordern, möglicherweise das System Gebiets Schema in die Sprache des Gebiets Schemas des Speichers ändern, um die Installation zu vereinfachen. Das Software Installationsprogramm muss sowohl Einzel-als auch Doppelbyte-Zeichen unterstützen und muss in jedem Gebiets Schema ausgeführt werden. Sie müssen im systemeigenen Gebiets Schema testen. Um das Native Gebiets Schema festzulegen, öffnen Sie das Dialogfeld **Region und Sprache** , wählen Sie die Registerkarte **Verwaltung** aus, und klicken Sie dann auf die Schaltfläche System Gebiets Schema **ändern** , wie im folgenden Screenshot gezeigt. Durch Klicken auf diese Schaltfläche wird das Dialogfeld **Regions-und Spracheinstellungen** angezeigt. Das **aktuelle System** Gebiets Schema-Kombinations Feld in diesem Dialogfeld ändert das System Gebiets Schema.

    Die folgenden Screenshots zeigen die Registerkarten, auf denen Sie Region und Sprache festlegen können:

    ![Screenshot des Dialog Felds "Regions-und Sprachoptionen"](images/reg-lang-opt.png)

    ![Screenshot, der zeigt, wie das aktuelle System Gebiets Schema geändert wird](images/reg-lang-settings.png)

3.  Deaktivieren Sie die Ansicht des Informations Centers eines Informations Centers, indem Sie Windows Media Player festlegen, um eine Visualisierung wiederzugeben. Der Hauptunterschied zwischen den Plattformen besteht darin, dass Sie in Windows Media Player 11 zunächst auf " **abspielen**" klicken, während Sie in Windows Media Player 12 zunächst mit der rechten Maustaste auf das Hauptfenster klicken.

    Der folgende Screenshot zeigt die Reihenfolge der Menü Optionen, die eine Visualisierung in Windows Media Player 11 wieder gibt:

    ![Screenshot, der zeigt, wie Sie eine Visualisierung in Windows Media Player 11 abspielen](images/wmp11-visual.png)

    Der folgende Screenshot zeigt die Reihenfolge der Menü Optionen, die eine Visualisierung in Windows Media Player 12 wieder gibt:

    ![Screenshot, der zeigt, wie Sie eine Visualisierung in Windows Media Player 12 abspielen](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a>Einrichten eines Stores

Führen Sie zuerst die folgenden Schritte aus, um einen Speicher einzurichten, und führen Sie dann die Schritte aus, die die ersten Schritte zum Überprüfen der Speicher Einrichtung ausführen:

1.  Starten Sie Windows Media Player, und warten Sie einige Sekunden, bis die aktuelle AllServices.xml Datei abgerufen wurde.
2.  Wenn Sie für Windows XP und Windows Vista einen Online Shop auswählen möchten, klicken Sie zuerst auf die Registerkarte, die zwischen der Medien Leit Faden Ansicht und der Ansicht der Online Filialen aufgeteilt wird. Klicken Sie dann im Menü auf **alle Online Stores durchsuchen**, und wählen Sie den Store aus, indem Sie in der Liste der Filialen auf das entsprechende Symbol klicken. Klicken Sie für Windows 7 im Navigationsbereich der Bibliothek auf die Schaltfläche, die zwischen der Schaltfläche **Medienhandbuch** und der Schaltfläche **Online Stores** aufgeteilt wird. Klicken Sie dann im Menü auf **alle Online Stores durchsuchen**, und wählen Sie den Store aus, indem Sie in der Liste der Filialen auf das entsprechende Symbol klicken.

    Der folgende Screenshot zeigt, wie ein Online Store in Windows Media Player 11 ausgewählt wird:

    ![Screenshot, der zeigt, wie Sie einen Online Shop in Windows Media Player 11 auswählen](images/wmp11-set-store.png)

    Der folgende Screenshot zeigt, wie Sie einen Online Shop in Windows Media Player 12 auswählen:

    ![Screenshot, der zeigt, wie Sie einen Online Shop in Windows Media Player 12 auswählen](images/wmp12-set-store.png)

3.  Befolgen Sie die Anweisungen aus dem Store, um zusätzliche Software zu installieren, die für die Verwendung des Stores benötigt wird.

**So überprüfen Sie die Speicher Einrichtung**

1.  Überprüfen Sie, ob die Software installiert ist.

    Vergewissern Sie sich, dass das OCX-Plug-in oder eine beliebige andere Software aus dem Store ohne Fehler heruntergeladen und installiert wird.

2.  Überprüfen Sie, ob die Software deinstalliert wird.

    Überprüfen Sie, ob in der Systemsteuerung unter **Programme und Funktionen** die Software, die der Speicher installiert, in der Liste **Programm deinstallieren oder ändern** angezeigt wird, und vergewissern Sie sich, dass Sie Sie ohne Fehler aus dieser Liste deinstallieren können.

3.  Vergewissern Sie sich, dass die Software nicht in der Taskleiste ausgeführt wird.

    Stellen Sie sicher, dass keine der Software aus dem Store Symbole zum Programm Benachrichtigungsbereich hinzufügt (auf der Taskleiste auf der linken Seite der Uhr), bevor die Kunden Zustimmung zum Herunterladen von Store-Software hat.

    Für den grundlegenden Speicherbedarf sollte die Installation zusätzlicher Software nicht erforderlich sein. Es sollte eine grundlegende Mediendarstellung (z. b. Streaming-Medien) verfügbar sein. Einige Geschäfte installieren zusätzliche Software, z. b. Download-Manager für die Premier-Medien. Diese Speicher können Symbole in der Taskleiste aufweisen, wenn die Symbole Anwendungen darstellen, die von Windows Media Player getrennt sind.

4.  Überprüfen Sie, ob die Registerkarte Store funktioniert.

    Überprüfen Sie, ob sich die Registerkarte "Store" ändert, um den ausgewählten Speicher

    Stellen Sie für Windows XP und Windows Vista mit Windows Media Player 11 sicher, dass der Name und das Symbol des Stores für den dunklen Fenster Media Player 11-Hintergrund sichtbar sind.

    Vergewissern Sie sich bei Windows 7 mit Windows Media Player 12, dass der Name und das Symbol des Geschäfts im Navigationsbereich der Bibliothek im Kontextmenü für die Dienst Auswahl angezeigt werden.

    Vergewissern Sie sich, dass der Speicher im Menü am oberen Rand der Liste der Store-Selektoren aufgeführt ist.

    > [!Note]  
    > Es wird keine Menüoption " **aktuellen Dienst hinzufügen** " angezeigt, wenn der Typ 2-Speicher der für die Region vorgestellte (Standard-) Speicher ist.

     

    Der folgende Screenshot zeigt das Menü, das angezeigt wird, wenn Sie auf die Registerkarte in der oberen rechten Ecke von Windows Media Player 11 klicken:

    ![Screenshot mit der Registerkarte "Store" in Windows Media Player 11](images/wmp11-verify-store.png)

    Der folgende Screenshot zeigt das Menü, das angezeigt wird, wenn Sie in der unteren linken Ecke von Windows Media Player 12 auf die unterteilte Schaltfläche klicken:

    ![Screenshot mit der Registerkarte "Store" in Windows Media Player 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a>Erstellen eines Kontos

**So überprüfen Sie die Konto Einrichtung**

1.  Vergewissern Sie sich, dass der Speicher über eine Option zum Erstellen eines neuen Kontos verfügt, und befolgen Sie dann die Anweisungen im Store, um ein neues Konto zu erstellen.

    Der folgende Screenshot zeigt die Schaltfläche **Neues Konto erstellen** , wie Sie in Windows Media Player 11 angezeigt werden kann:

    ![Screenshot, der zeigt, wie Sie die Konto Einrichtung für Windows Media Player 11 überprüfen](images/wmp11-verify-account.png)

    Der folgende Screenshot zeigt die Schaltfläche **Neues Konto erstellen** , wie Sie in Windows Media Player 12 angezeigt werden kann:

    ![Screenshot, der zeigt, wie Sie die Konto Einrichtung für Windows Media Player 12 überprüfen](images/wmp12-verify-account.png)

2.  Vergewissern Sie sich, dass Sie sich bei dem Konto anmelden können, das Sie erstellt haben.

### <a name="setting-up-credential-caching"></a>Einrichten der Zwischenspeicherung von Anmelde Informationen

Führen Sie zuerst die folgenden Schritte aus, um das Zwischenspeichern von Anmelde Informationen einzurichten, und führen Sie dann die Schritte aus, die den ersten Schritten folgen, um die Einrichtung der Anmelde Informationen zu überprüfen:

1.  Geben Sie auf der Anmeldeseite die Anmelde Informationen ein, und wählen Sie die Option zum Speichern von Benutzerinformationen aus.
2.  Vergewissern Sie sich, dass auf der Anmeldeseite ein Kontrollkästchen für den Benutzer zum Zwischenspeichern von Anmelde Informationen zulässig ist.
3.  Die optionale Zwischenspeicherung von Anmelde Informationen ist ein wichtiger Sicherheitsaspekt. Das automatische Zwischenspeichern von Anmelde Informationen kann personenbezogene Informationen von Benutzern verfügbar machen, die sich bei einem freigegebenen oder öffentlichen Computer anmelden. Sie sollten Kundeninformationen schützen, indem Sie ein Kontrollkästchen anbieten, das das Caching optional rendert.

**Überprüfen der Zwischenspeicherung von Anmelde Informationen**

1.  Vergewissern Sie sich, dass der Speicher über ein Kontrollkästchen für die Option **meine Benutzerinformationen speichern** verfügt.

    1.  Schließen Sie Windows-Media Player.
    2.  Öffnen Sie Windows Media Player erneut, und versuchen Sie, Inhalte herunterzuladen.

2.  Überprüfen Sie, ob das Zwischenspeichern von Anmelde Informationen vorhanden ist und funktioniert

    1.  Melden Sie sich beim Store ab.
    2.  Schließen Sie Windows-Media Player.
    3.  Öffnen Sie Windows Media Player erneut, und versuchen Sie, Inhalte herunterzuladen.

3.  Vergewissern Sie sich, dass der Benutzer zur Eingabe von Anmelde Informationen aufgefordert wird

    Nach der Abmeldung und dem anschließenden Versuch, den Speicher zu verwenden, sollte der Kunde zur Eingabe von Anmelde Informationen aufgefordert werden.

## <a name="content-acquisition"></a>Inhalts Erfassung

In diesem Abschnitt werden die verschiedenen Möglichkeiten zum Abrufen von Inhalten beschrieben und erläutert, wie Sie überprüfen können, ob dieser Inhalt abgerufen wurde.

### <a name="streaming-content"></a>Streaming von Inhalten

Streamen Sie alle verfügbaren Inhaltstypen aus dem Speicher. Beispiel: Streamen von Radio-, Video-, Audio-und Vorschau Inhalt.

**So überprüfen Sie Streaminginhalte**

1.  Überprüfen Sie, ob alle verfügbaren Typen von Inhaltsstream vorhanden

2.  Überprüfen Sie, ob der Inhalt in Windows Media Player und nicht in einem anderen Player oder Steuerelement abgespielt wird.

### <a name="obtaining-content"></a>Abrufen von Inhalten

Führen Sie zuerst die folgenden Schritte aus, um den Inhalt zu erwerben, und führen Sie dann die Schritte aus, die die ersten Schritte ausführen, um den Kauf zu überprüfen

1.  Starten Sie Windows Media Player.
2.  Melden Sie sich beim Testkonto an.
3.  Navigieren Sie zu dem zu Erwerb-Inhalt.
4.  Befolgen Sie das Speicher spezifische Verfahren, um Inhalte zu erwerben.

**So überprüfen Sie den erworbenen und heruntergeladenen Inhalt**

1.  Vergewissern Sie sich, dass der berechnete Preis richtig ist.

    Überprüfen Sie, ob der Preis korrekt ist, insbesondere, wenn Sie mehrere Inhaltselemente gleichzeitig erwerben, und überprüfen Sie, ob die Informationen zum Konto Saldo nach dem Kauf ordnungsgemäß aktualisiert wurden. Einige Inhalte können als einzelne Spuren und nur als Alben erworben werden. Vergewissern Sie sich, dass der albumpreis nicht größer als die Summe der einzelnen Spuren ist.

2.  Überprüfen Sie, ob die erworbenen Inhalte in die Bibliothek heruntergeladen wurden.

    Wenn der Download abgeschlossen ist, navigieren Sie zu dem heruntergeladenen Inhalt in der Windows Media Player-Bibliothek. Der heruntergeladene Inhalt befindet sich in der Bibliothek des aktuellen Benutzers.

    -   Für Windows XP und Windows Vista mit Windows Media Player 11 wird heruntergeladener Inhalt im Navigationsbereich Bibliothek unter **Bibliothek** Pivot und dann unter **Lieder** angezeigt.
    -   Für Windows 7 mit Windows Media Player 12 wird der Inhalt, der in die Windows Media Player Bibliothek heruntergeladen wird, im Navigationsbereich Windows Media Player unter " **Musik**" angezeigt.

3.  Überprüfen Sie, ob für den Kauf Metadaten heruntergeladen wurden

    Stellen Sie sicher, dass die folgenden Spalten in der Windows Media Player-Bibliothek angezeigt werden (fügen Sie Sie andernfalls hinzu):

    -   Album-Künstlerin
    -   Titel
    -   Titel des Albums
    -   Inhaltsanbieter
    -   Genre

    Die vorangehenden Spalten müssen ausgefüllt werden. Der Inhalt sollte über eine Albumgrafik verfügen. Es ist jedoch nicht erforderlich, dass Albumkunst Validierungstests bestanden hat.

4.  Überprüfen Sie, ob die Medien Nutzungsrechte für den Kauf korrekt sind.

    Klicken Sie für jede heruntergeladene Spur mit der rechten Maustaste auf den Titel, und wählen Sie **Eigenschaften**, und wählen Sie dann die Registerkarte **Medien Verwendungs Rechte** aus.

    Der Speicher kann seinen Inhalt mit Medien Nutzungsrechten schützen oder den Inhalt nicht schützen. Auf der Registerkarte **Medien Verwendungs Rechte** wird der Status entweder durch Auflisten der Einschränkungen oder durch Angabe, dass der Inhalt nicht geschützt ist, angezeigt. Der Speicher muss seinen aktuellen Plan für die Medien Nutzungsrechte kommunizieren. Sie müssen tatsächliche Ergebnisse anhand dieses erwarteten Verhaltens überprüfen.

    Die Lizenzen für Medienrechte müssen vorab zugestellt werden. Der Kunde darf den Inhalt nicht wiedergeben oder einen anderen Prozess zum erhalten der Lizenz durchlaufen. Sie müssen die jeweiligen Medien Nutzungsrechte mit den Anforderungen vergleichen, die der Speicher dem Kunden nach Bedarf mitgeteilt hat. Rechte müssen auf mindestens zwei andere Computer übertragbar sein. Kunden müssen in der Lage sein, Ihre Medien zu brennen und zu synchronisieren.

    Der folgende Screenshot zeigt die Medien Nutzungsrechte einer geschützten Datei:

    ![Screenshot mit den Medien Verwendungs rechten für eine geschützte Datei](images/media-rights-protected.png)

    Wenn der Inhalt nicht geschützt ist, wird auf der Registerkarte " **Medien Nutzungsrechte** " Dieser Fakt angezeigt.

    Der folgende Screenshot zeigt die Medien Nutzungsrechte einer ungeschützten Datei:

    ![Screenshot mit den Medien Verwendungs rechten für eine ungeschützte Datei](images/media-rights-not-protected.png)

5.  Überprüfen Sie, ob die erworbenen Inhalte abgespielt werden.

    Überprüfen Sie, ob heruntergeladene Inhalte in Windows Media Player abgespielt werden.

    Wiedergeben jeglichen Inhalts, der aus dem Store gekauft wurde und der sich in der lokalen Bibliothek befindet, oder Streamen einer Vorschau.

    Führen Sie die folgenden Schritte aus, um Inhalte in Windows XP und Windows Vista mit Windows Media Player 11 zu erwerben:

    1.  Klicken Sie auf die Registerkarte **jetzt Wiedergabe** .
    2.  Positionieren Sie den Mauszeiger im Listen Bereich mit dem Mauszeiger auf Album Art, um den Link zum **kaufen** anzuzeigen.
    3.  Klicken Sie auf **kaufen**.

    Der folgende Screenshot zeigt den Speicherort des **Kaufs** Links in Windows Media Player 11:

    ![Screenshot, der zeigt, wie Sie Inhalte in Windows Media Player 11 kaufen](images/wmp11-verify-buy-play.png)

    Führen Sie die folgenden Schritte aus, um Inhalte in Windows 7 mit Windows Media Player 12 zu erwerben:

    1.  Klicken Sie im Bibliotheks Modus auf die Registerkarte wieder **Gabe** .
    2.  Klicken Sie in der Wiedergabeliste unter der Albumgrafik auf **Shop** .

    Der folgende Screenshot zeigt, wie Sie Inhalte in Windows Media Player 12 kaufen:

    ![Screenshot, der zeigt, wie Sie Inhalte in Windows Media Player 12 kaufen](images/wmp12-verify-buy-play.png)

6.  Vergewissern Sie sich, dass Sie auf **kaufen** **oder auf** den Store wechseln.

    Der Windows-Media Player sollte zum Store in der Bibliotheks Ansicht wechseln und die Einkaufsmöglichkeiten des Stores laden.

    Sie müssen dann den Titel weiter kaufen.

7.  Vergewissern Sie sich, dass nach dem Klicken auf **kaufen** oder **Einkaufen** die Inhalte heruntergeladen werden.

    Überprüfen Sie, ob die Medien Nutzungsrechte für den erworbenen Inhalt und seine Metadaten geeignet sind, und überprüfen Sie, ob die Nachverfolgung abgespielt wird. Im Allgemeinen sollte diese Kaufmethode dieselben Ergebnisse aufweisen wie andere Methoden.

### <a name="burning-content"></a>Brennen von Inhalten

Führen Sie zuerst die folgenden Schritte aus, um erworbene Inhalte zu brennen (Kopieren Sie erworbene Inhalte auf eine beschreibbare CD oder DVD), und führen Sie dann die Schritte aus, die den ersten Schritten folgen, um zu überprüfen, ob der Inhalt brennt:

> [!Note]  
> Beachten Sie vor dem Brennen eines erworbenen Titels seine Verbrauchs Anzahl, damit Sie später überprüfen können, ob die Anzahl nach dem Brennen des Titels Dekremente.

 

1.  Klicken Sie auf die Registerkarte **Brennen**
2.  Ziehen Sie erworbene Spuren in die **Liste der Verbrennungen**.
3.  Klicken Sie auf die Schaltfläche **Start brennen** .

Der folgende Screenshot zeigt die **Burn-Liste** auf der rechten Seite des Bildschirms und die Schaltfläche " **Brennen starten** " unterhalb der **Verbrennungs Liste** in Windows Media Player 11:

![Screenshot, der zeigt, wie Sie Inhalte in Windows Media Player 11 brennen](images/wmp11-verify-burn.png)

Der folgende Screenshot zeigt, wie die Verbrauchs Liste in Windows Media Player 12 angezeigt wird, nachdem Sie eine Spur in die Liste mit den Ausbrennen gezogen haben und die Schaltfläche **Start brennen** am oberen Rand der Registerkarte **Brennen** anzeigt:

![Screenshot, der zeigt, wie Sie Inhalte in Windows Media Player 12 brennen](images/wmp12-verify-burn.png)

**So überprüfen Sie, ob erworbene Inhalte gebrannt werden können**

1.  Überprüfen Sie, ob der erworbene Inhalt durch Abspielen der CD oder DVD nach Abschluss des Vorgangs gebrannt wird.

2.  Vergewissern Sie sich, dass die Anzahl der Verbrennungen verringert wird.

    Navigieren Sie zu der Bibliothek, und öffnen Sie die Medien Nutzungsrechte für einen erworbenen Titel, der gebrannt wurde.

    Wenn die Anzahl der verbrannten Vorkommen eines Titels begrenzt ist, überprüfen Sie, ob diese Zahl nach dem Brennen des Titels abnimmt.

### <a name="transferring-content"></a>Inhalt wird übertragen

Übertragen von Inhalt auf einen anderen Computer.

**So überprüfen Sie, ob erworbene Inhalte auf einen anderen Computer übertragen werden können**

-   Wenn der Speicher die Übertragung von Inhalt an einen anderen Computer zulässt, übertragen Sie den Inhalt auf mindestens zwei Computer.

Führen Sie zuerst die folgenden Schritte aus, um eine Synchronisierung mit einem Gerät durchzuführen und erworbene Inhalte an dieses Gerät zu übertragen. führen Sie dann die Schritte aus, die den ersten Schritten folgen, um zu überprüfen, ob der

> [!Note]  
> Beachten Sie vor der Übertragung eines erworbenen Titels seine Synchronisierungs Anzahl, damit Sie später überprüfen können, ob die Anzahl nach der Übertragung des Titels Dekremente.

 

1.  Verbinden Sie ein Gerät mit einer sicheren Uhr. Beispiele hierfür sind Geräte, die Windows Media DRM für tragbare Geräte verwenden, z. b. ein portables Medien Center wie z. b. iRiver H10, Creative Zen usw.
2.  Klicken Sie unter Windows Media Player auf die Registerkarte **Synchronisieren** .
3.  Ziehen Sie Inhalt aus der Bibliothek auf der Registerkarte **Synchronisieren** in den Bereich **Synchronisierungs Liste** .
4.  Klicken Sie auf die Schaltfläche **Synchronisierung starten** .

Der folgende Screenshot zeigt Track 1 im Bereich **Synchronisierungs Liste** und zeigt die Schaltfläche **Synchronisierung starten** in Windows Media Player 11 an:

![Screenshot, der zeigt, wie Inhalt in Windows Media Player 11 übertragen wird](images/wmp11-verify-transfer.png)

Der folgende Screenshot zeigt Track 1 im Bereich **Synchronisierungs Liste** und zeigt die Schaltfläche **Synchronisierung starten** in Windows Media Player 12 an:

![Screenshot, der zeigt, wie Inhalt in Windows Media Player 12 übertragen wird](images/wmp12-verify-transfer.png)

**So überprüfen Sie, ob erworbene Inhalte auf ein anderes Gerät übertragen werden können**

1.  Überprüfen Sie, ob der erworbene Inhalt auf das Gerät übertragen wird, indem Sie den Inhalt auf dem Gerät abspielen. Der übertragene Inhalt muss auch über die entsprechenden Metadaten verfügen.

2.  Vergewissern Sie sich, dass die Synchronisierungs Anzahl dekrementiert wird.

    Navigieren Sie zu der Bibliothek, und öffnen Sie die Medien Nutzungsrechte für eine übertragene Spur.

    Wenn die Anzahl der Synchronisierungs Versuche für eine Nachverfolgung begrenzt ist, überprüfen Sie, ob diese Zahl bei der Übertragung des Titels abnimmt.

## <a name="store-features"></a>Store-Features

In den folgenden Abschnitten wird beschrieben, wie Sie verschiedene Features eines integrierten Online Stores testen.

### <a name="managing-an-account"></a>Verwalten eines Kontos

Melden Sie sich mit einem Konto an, das einige Einkäufe getätigt hat, und öffnen Sie den Kauf Verlauf.

**So überprüfen Sie den Kauf Verlauf**

-   Vergewissern Sie sich, dass der Kaufverlauf vorherige Käufe nachverfolgt.

Wenn der Speicher-oder Kontotyp dieses Feature unterstützt, versuchen Sie, einen gelöschten Kauf wiederherzustellen.

**So überprüfen Sie, ob vorherige Käufe erneut erworben werden können**

-   Überprüfen Sie, ob ein vorheriger Kauf wieder hergestellt werden kann.

Wenn der Speicher die Verwendung mehrerer Computer mit dem Konto unterstützt, überprüfen Sie alle Funktionen, die diese Funktion bereitstellt.

**So überprüfen Sie die Verwaltung mehrerer Computer mit einem einzelnen Konto**

-   Überprüfen Sie die Funktionalität des Stores, um mehrere Computer zu verwalten.

### <a name="managing-a-store-specific-account"></a>Verwalten eines Store-Specific Kontos

Der Speicher hat möglicherweise keine typischen Konto Typen, Einschränkungen oder Inhalte. Ein Speicher, der Streaming-Videos mietet, benötigt z. b. eine Benutzeroberfläche, um aktive Vermietungen anzuzeigen, und die Benutzeroberfläche muss getestet werden.

> [!Note]  
> Obwohl Microsoft keine Speicher spezifischen Kontofunktionen zertifizieren kann, sollten Sie diese Funktionalität testen, um eine gute Kundenfreundlichkeit zu gewährleisten.

 

### <a name="managing-the-info-center"></a>Verwalten des Info Centers

Führen Sie zuerst die folgenden Schritte aus, um das Testen des Standardstatus vorzubereiten, und führen Sie dann den nächsten Schritt aus, der den ersten Schritten folgt, um zu überprüfen, ob das Info Center standardmäßig deaktiviert ist:

1.  Wiedergabe von Inhalten aus dem Store.
2.  Wechseln Sie zum jetzt Wiedergabe-Modus. Klicken Sie unter Windows XP oder Windows Vista mit Windows Media Player 11 auf die Registerkarte **jetzt Wiedergabe** . Klicken Sie in Windows 7 mit Windows Media Player 12 in der unteren rechten Ecke auf die Schaltfläche **zum jetzt abspielen wechseln** .

**So überprüfen Sie, ob das Info Center standardmäßig deaktiviert ist**

-   Vergewissern Sie sich, dass das Info Center standardmäßig deaktiviert ist.

Wenn das Geschäft eine Info Center-Ansicht bietet, geben Sie Inhalte aus dem Store wieder, während der Inhalt wiedergegeben wird, wechseln Sie in den Modus jetzt wiedergeben, und schalten Sie Info Center ein.

Unter Windows XP oder Windows Vista mit Windows Media Player 11 Klicken Sie mit der rechten Maustaste auf das Fenster jetzt Wiedergabe und wählen dann im Kontextmenü **Info Center-Ansicht** aus.

Der folgende Screenshot zeigt das Kontextmenü in Windows Media Player 11:

![Screenshot, der zeigt, wie Sie auf das InfoCenter eines Stores in Windows Media Player 11 zugreifen](images/wmp11-info-center.png)

Klicken Sie unter Windows 7 mit Windows Media Player 12 mit der rechten Maustaste auf das Fenster jetzt Wiedergabe, wählen Sie im Kontextmenü die Option **Visualisierungen** aus, und klicken Sie dann auf **Info Center-Ansicht**.

Der folgende Screenshot zeigt das Kontextmenü in Windows Media Player 12:

![Screenshot, der zeigt, wie Sie auf das InfoCenter eines Stores in Windows Media Player 12 zugreifen](images/wmp12-info-center.png)

**So überprüfen Sie, ob das Info Center funktionsfähig ist**

-   Vergewissern Sie sich, dass im Bereich jetzt Wiedergabe im Info Center Medieninformationen angezeigt werden. Der folgende Screenshot zeigt ein Beispiel für Medieninformationen:

    ![Screenshot mit der Funktionalität eines Informations Centers für das Geschäft](images/media-information.png)

Wenn auf der Seite ein Kauf Verknüpfungen oder andere Links angezeigt werden, klicken Sie auf die Links.

**So überprüfen Sie die Links in der Info Center-Ansicht**

-   Überprüfen Sie, ob die Links den Speicher anzeigen.

    Der Windows-Media Player sollte in seiner Bibliothek zum Speicher wechseln.

## <a name="store-interaction"></a>Speichern der Interaktion

In den folgenden Abschnitten wird beschrieben, wie Sie die Interaktion zwischen den anderen Stores und dem zu testenden Speicher testen.

### <a name="yielding-to-the-active-store"></a>Ergebnis des aktiven Stores

Wechseln Sie zu einem anderen Speicher als dem zu testenden Speicher.

**So überprüfen Sie das Ergebnis im aktiven Speicher**

-   Vergewissern Sie sich, dass der getestete Speicher den aktiven Speicher liefert.

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a>Verhindern, dass der getestete Speicher den aktiven Speicher übernimmt

-   Wenn ein anderer Speicher ausgewählt ist, schließen Sie Windows Media Player und starten Sie den Computer neu.
-   Starten Sie Windows Media Player.

**So überprüfen Sie, ob der getestete Speicher**

-   Vergewissern Sie sich, dass der zuletzt aktive Speicher angezeigt wird und dass der getestete Speicher nicht angezeigt wird.

### <a name="accessing-a-store-in-high-contrast-mode"></a>Zugreifen auf einen Speicher im High-Contrast Modus

Aktivieren Sie zuerst den Modus für hohe Kontraste durch Drücken von Left Shift + Left Alt + Print, und führen Sie dann die folgenden Schritte aus, um die Barrierefreiheit mit hohem Kontrast zu überprüfen:

**So überprüfen Sie, ob der Speicher im Modus mit hohem Kontrast verfügbar ist**

1.  Überprüfen Sie, ob die Anmelde Benutzeroberfläche intakt und funktionsfähig ist.
2.  Vergewissern Sie sich, dass alle Fenster und Dialogfelder ordnungsgemäß angezeigt werden.
3.  Medien erwerben. Überprüfen Sie, ob die Schaltflächen "kaufen" und "herunterladen", "Downloads", "Preisinformationen" usw.
4.  Überprüfen Sie, ob Sie streamen, brennen und synchronisieren können.
5.  Suchen Sie nach ausgeschnittenen Text-und Benutzeroberflächen Elementen, Text, der nicht lesbar ist, und anderen sichtbaren Fehlern.

### <a name="securing-a-store"></a>Sichern eines Stores

Führen Sie folgende Schritte aus, um die Kontosicherheit zu überprüfen:

**So überprüfen Sie die Kontosicherheit**

1.  Geben Sie falsch formatierte Kontoinformationen in die Anmeldeseite und das Dialogfeld ein, und überprüfen Sie, ob Sie vom Speicher abgelehnt werden.
2.  Melden Sie sich an, zeigen Sie die Kontoseite an, und melden Sie sich ab.
3.  Klicken Sie in Windows Media Player auf die Schaltfläche zurück, und vergewissern Sie sich, dass die vorherigen Benutzerkontoinformationen nicht angezeigt werden.

 

 




