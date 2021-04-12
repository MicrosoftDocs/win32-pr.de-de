---
title: Vereinfachen der Spiele Installation
description: In diesem Artikel werden einige Konzepte erläutert, die Entwickler von Spielen für Windows implementieren können, um die Gesamtleistung zu verbessern.
ms.assetid: 356780b7-801d-c6dd-a266-6272bcb8bd36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8728eb2c9c53a99673ee742a5c961b91e37abed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315854"
---
# <a name="simplifying-game-installation"></a>Vereinfachen der Spiele Installation

Ein wichtiger Vorteil von spielen, die auf einer Konsole anstelle von Windows ausgeführt werden, ist der Installationsvorgang – oder das Fehlen davon. Wenn ein Spiel zum ersten Mal in einer Konsole ausgeführt wird, stellt der Spieler einige Auswahlmöglichkeiten oder Bestätigungen bereit und kann fast sofort mit der Wiedergabe beginnen. Das Installieren eines Spiels unter Windows ist durch die Notwendigkeit einer beträchtlichen Benutzereingabe und des potenziell langen Installationsprozesses komplizierter. Dieser Installationsvorgang kann jedoch verbessert werden, um für Spieler von Windows-basierten spielen eine bessere Leistung zu bieten. In diesem Artikel werden einige Konzepte erläutert, die Entwickler von Spielen für Windows implementieren können, um die Gesamtleistung zu verbessern.

-   [Typische Spiele Installation](#typical-game-installation)
-   [Vereinfachte Spiele Installation](#simplified-game-installation)
    -   [Alle Fragen im Vordergrund stellen](#ask-all-questions-up-front)
    -   [Bereitstellen spezieller Installations Modi](#provide-special-installation-modes)
    -   [Minimieren Sie die Anzahl der Installations Fragen.](#minimize-the-quantity-of-installation-questions)
    -   [Optionale Komponenten in erforderliche Komponenten ändern](#change-optional-components-into-required-components)
    -   [Installieren Sie immer DirectX, und gehen Sie so vor.](#always-install-directx-and-do-so-silently)
    -   [Berücksichtigen Sie Ihre EULA](#think-about-your-eula)
    -   [Nach der Installation automatisch starten](#automatically-launch-after-installation)
    -   [Optimieren der Installations Leistung](#optimize-your-installation-performance)
    -   [Bei der Installation bei der Windows-Firewall registrieren](#register-with-windows-firewall-during-installation)
    -   [Installation für alle Benutzer, nicht nur für den aktuellen Benutzer](#install-for-all-users-not-just-the-current-user)
-   [Beispiel für eine vereinfachte Installation](#example-of-simplified-installation)
-   [Zusammenfassung](#summary)

## <a name="typical-game-installation"></a>Typische Spiele Installation

Wenn Sie die einfache Installation und die erforderliche Zeit für das Spielen eines Spiels vergleichen, ist die typische Xbox-Darstellung wesentlich besser als Windows. Das Flussdiagramm in Abbildung 1 zeigt die typischen Installationsprozesse auf Xbox und unter Windows für den Vergleich.

**Abbildung 1. Typischer Installationsvorgang, Xbox und Windows**

![Xbox \- vs- \- PC](images/pcvsconsoleinstall.png)

## <a name="simplified-game-installation"></a>Vereinfachte Spiele Installation

Die größeren Anforderungen des Benutzers zum Installieren eines Spiels unter Windows müssen jedoch nicht erfüllt werden. Durch die Implementierung der folgenden Konzepte verringern Sie die Anzahl der Schritte, die ein Benutzer ausführen muss, wodurch die erforderliche Zeit für die Installation verkürzt werden kann.

### <a name="ask-all-questions-up-front"></a>Alle Fragen im Vordergrund stellen

Alle Optionen, die der Spieler während der Installation auswählt, die zu einer Abbruchs-Installation führen können, sollten vor denjenigen angeboten werden, die die Installation nicht beenden. der ungünstigste Fall besteht darin, dass für den Spieler eine Auswahl geboten wird, die dazu führen kann, dass die Installation abgebrochen wird, nachdem das Spiel vollständig vom Installationsmedium kopiert wurde. Dies kann besonders frustrierend sein, wenn die Installation das Austauschen mehrerer Datenträger erfordert. Sie sollten den Installer so entwerfen, dass alle wichtigen Fragen (z. b. die Annahme der Lizenzbedingungen) zu Beginn des Prozesses gestellt werden, damit für die Installation nicht ein Rollback zum Abschluss des Vorgangs ausgeführt werden muss.

Sie können den Benutzer auch auffordern, die Lizenzbedingungen zu akzeptieren und die Product Key einzugeben, wenn das Spiel zum ersten Mal gestartet wird, anstatt diese im Rahmen der Installation zu Fragen. In diesem Szenario wird die Installation nicht rückgängig machen, wenn Sie die Zustimmung zu den Lizenzbedingungen ablehnen oder während des Eintrags des Product Key abbrechen, da diese Eingabe Aufforderungen Teil des Spiels selbst sind. Dies kann nützlich sein, wenn Sie über vorinstallierte oder OEM-Szenarien verfügen. Achten Sie jedoch darauf, dass Sie den Benutzer nicht auffordern, während des ersten Starts, der administrative Anmelde Informationen erfordert, Entscheidungen zu treffen.

### <a name="provide-special-installation-modes"></a>Bereitstellen spezieller Installations Modi

Im Idealfall sollten Windows-Spiel Installationsprogramme nur vollständig automatische und benutzerdefinierte Installations Modi und nichts dazwischen anbieten.

Der automatische Modus sollte keine Fragen stellen, die nicht unbedingt erforderlich sind, um eine funktionierende Installation zu erstellen, und einfach die Standardeinstellungen verwenden, ohne nach anderen Optionen aufzufordern. Viele Spieler interessieren sich nicht für die Position des Spiels auf der Festplatte oder die anfänglichen Spieleinstellungen – Sie möchten das Spiel nur so bald wie möglich wiedergeben.

Der benutzerdefinierte Modus sollte nur für Hauptbenutzer bestimmt sein, die den Installationspfad oder andere Installationsoptionen ändern möchten, und er sollte nicht der Standardmodus sein.

Der benutzerdefinierte Modus kann entweder eine vollständige Installation oder eine minimale Installation bieten, bei der nur die Dateien installiert werden, die für die Wiedergabe des Spiels benötigt werden. Wenn der Spieler die minimale Installation auswählt, kann das Spiel Installations-on-Demand-oder Streamingtechniken verwenden, um die verbleibenden Installationsdaten zu lesen, sodass der Spieler schnell mit der Wiedergabe des Spiels beginnen muss, ohne auf den Abschluss einer vollständigen Installation warten zu müssen. Das Installieren von Daten auf diese Weise wirkt sich jedoch auf das Design der Spiel-Engine aus. Weitere Informationen zum bedarfsgesteuerten Installieren von Inhalten finden Sie unter [install-on-Demand for Games](/windows/desktop/DxTechArts/install-on-demand-for-games).

### <a name="minimize-the-quantity-of-installation-questions"></a>Minimieren Sie die Anzahl der Installations Fragen.

In beiden Installations Modi sollten Sie versuchen, die Anzahl der während der Installation aufzurufenden Versuche einzuschränken. Dadurch wird die Anzahl der Lesevorgänge reduziert, die erforderlich sind, um das Spiel zu installieren und zu starten. Bei Bedarf sollte nach Abschluss der Installation nur noch eine Eingabeaufforderung vorhanden sein. Wie Sie sehen können, enthält das in Abbildung 1 gezeigte Beispiel zu viele Eingabe Aufforderungen nach der Installation.

### <a name="change-optional-components-into-required-components"></a>Optionale Komponenten in erforderliche Komponenten ändern

Machen Sie die Installation aller Komponenten erforderlich, anstatt Sie als optional zu gestalten, es sei denn, es gibt einen guten Grund dafür. Durch die einfache Installation aller Komponenten wird das Spiel ohne weitere Verzögerung und Hektik gestartet.

### <a name="always-install-directx-and-do-so-silently"></a>Installieren Sie immer DirectX, und gehen Sie so vor.

Es wird dringend empfohlen, dass das Spiel eine unbeaufsichtigte Installation von DirectX Redistributable durchläuft, für das das Spiel erstellt wurde. Der DirectX-Installationsvorgang ist so konzipiert, dass überprüft wird, ob etwas aktualisiert werden muss, und gibt es schnell zurück, wenn dies nicht der Fall ist. Es ist also nicht erforderlich, Benutzer zu Fragen, ob DirectX installiert werden soll. Sie können eine unbeaufsichtigte Installation von DirectX ausführen, indem Sie den folgenden Befehl aus dem Installationspaket ausführen: **dxsetup.exe/Silent**

Wenn ein Benutzer gefragt wird, ob er DirectX installieren möchte, kann dies zu vielen Problemen führen. Angenommen, der Benutzer geht davon aus, dass er über die neueste verteilbare Komponente verfügt und die Installation von DirectX überspringen soll. die Installation des Spiels könnte trotzdem erfolgreich fortgesetzt werden. Wenn das Spiel jedoch eine bestimmte Version von D3DX oder eine andere aktualisierte Funktionalität erfordert, die übersprungen wurde, funktioniert das Spiel nicht, und der Benutzer wird sehr frustriert sein.

Wenn Sie den Benutzer aus irgendeinem Grund bitten müssen, DirectX zu installieren, sollte das Installationsprogramm mindestens – abbrechen und einen Rollback für den gesamten Installationsvorgang ausführen, wenn der Benutzer nicht DirectX installieren möchte. Durch das Rollback der Installation werden Fehler vermieden, die dadurch verursacht werden, dass das System beim Start des Spiels nicht die neueste Version von DirectX installiert hat.

Beachten Sie, dass es wichtig ist, die verteilbare Komponente, für die das Spiel erstellt wurde, zu versenden, anstatt einfach die verteilbare Komponente aus dem aktuellen DirectX SDK zu versenden. Die neueste verteilbare Tabelle enthält möglicherweise nicht alle Komponenten, die in einer früheren Version gefunden wurden.

Außerdem ist es wichtig, dass das Installationsprogramm überprüft, ob es bereits installiert ist, und feststellen, ob ein Neustart des Systems erforderlich ist. Wenn DirectX auf dem neuesten Stand ist, muss das Kopieren einer DLL nicht neu gestartet werden.

### <a name="think-about-your-eula"></a>Berücksichtigen Sie Ihre EULA

Die DirectX-EULA können und an den EULA des Spielentwicklers angehängt werden. Es ist nicht möglich, den Benutzern die Zustimmung zu den EULA des Entwicklers und nicht an DirectX-EULA zu gewähren. Der Benutzer muss entweder EULAs zustimmen oder das Spiel nicht installieren. Wenn ein Entwickler der Meinung ist, dass er dem Benutzer die Wahl bieten muss, sollte die gesamte Installation fehlschlagen, wenn der Benutzer nicht den DirectX-EULA zustimmt.

Wenn möglich, wenden Sie sich an Ihre Rechtsabteilung, um zu erfahren, ob Sie EULAs vollständig vermeiden können, und verwenden Sie einen Verkleinerungs umschließenden EULA wie die Verwendung von Konsolen spielen Dadurch müssen die Benutzer nicht gefragt werden, ob Sie die Lizenzbedingungen akzeptieren möchten. Die DirectX-EULA muss an die EULA mit den Verkleinerungs umschließenden EULA angehängt werden. Andernfalls müssen die DirectX-EULA angezeigt und akzeptiert werden, wodurch der Zweck der Verwendung von EULA mit Verkleinerungs Umbrüchen abgelehnt wird.

Eine Ausnahme von einem Verkleinerungs umschließenen EULA ist für einen Inhalts-Editor. Ein Editor muss bei der Installation des Editors einen EULA anzeigen, oder wenn der Editor zum ersten Mal gestartet wird. Viele Spieler sind nur daran interessiert, Inhalte zu spielen, sodass die Installation eines Editors ein separater Prozess sein sollte.

### <a name="automatically-launch-after-installation"></a>Nach der Installation automatisch starten

Fast alle Spieler möchten ein Spiel abspielen, sobald Sie es erhalten. Standardmäßig sollte das-Installationsprogramm nach Abschluss der Installation das Spiel starten, obwohl es in einer benutzerdefinierten Installation üblich ist, dies in einem Kontrollkästchen anzugeben, das der Benutzer außer Kraft setzen kann.

### <a name="optimize-your-installation-performance"></a>Optimieren der Installations Leistung

Entwickler sollten ihre Installationen testen, um zu bestimmen, wie viel Zeit für die Installation erforderlich ist. Entwickler können die Installationszeit verringern, indem Sie die neueste Version Ihrer Installations Tools verwenden und das Datenlayout auf den Installationsmedien optimieren. Die meisten DVD-Erstellungs Tools verfügen über Optionen für die Layoutoptimierung, die die Installationszeiten verbessern können, ohne die Entwicklung

### <a name="register-with-windows-firewall-during-installation"></a>Bei der Installation bei der Windows-Firewall registrieren

Wenn Ihr Spiel als Server ausgeführt werden kann oder das Spiel Netzwerkmodell ein Peer-to-Peer-Modell ist, registrieren Sie das Spiel beim Installations Zeitpunkt bei der Windows-Firewall. Dadurch wird verhindert, dass das firewalldialogfeld in der Mitte des Spiels in das Pop wechselt, wenn der Benutzer versucht, auf das Netzwerk zuzugreifen. Wenn das Spiel ein reiner Client ist, sollte das Installationsprogramm das Spiel nicht zur Ausnahmeliste der Firewall hinzufügen.

Weitere Informationen finden Sie unter Windows-Firewall für Spieleentwickler.

### <a name="install-for-all-users-not-just-the-current-user"></a>Installation für alle Benutzer, nicht nur für den aktuellen Benutzer

Standardmäßig wird das Spiel für alle Benutzer installiert. Dadurch kann jeder neue Benutzer im System das Spiel abspielen, ohne es für Sie installieren zu müssen. Wenn eine Installation für alle Benutzer auf einem Least-Privileged Benutzerkonto durchgeführt wird, schlägt das Installationsprogramm fehl oder fordert den Benutzer zur Eingabe eines Administrator Kennworts auf. Versuchen Sie also zu erkennen, ob das Konto über die erforderlichen Berechtigungen verfügt, bevor Sie die Option zur Installation für alle Benutzer anbieten. Wenn der Benutzer das Spiel nur für den aktuellen Benutzer installiert, müssen Sie sicherstellen, dass der Installationspfad zu einem Speicherort im Profil des Benutzers geändert wird. Im Idealfall ändern Sie den Pfad in nicht roaminganwendungsdaten (z. b. ein Unterverzeichnis von "Lokales CSIDL \_ \_ AppData").

## <a name="example-of-simplified-installation"></a>Beispiel für eine vereinfachte Installation

In Abbildung 2 finden Sie ein Beispiel für einen verbesserten Prozess für die Installation eines Spiels in Windows mit vereinfachten Installations Dialogfeldern.

**Abbildung 2. Vereinfachter Installationsvorgang**

![Installieren](images/simplifiedgameinstall.png)

Beachten Sie die folgenden wichtigen Punkte:

-   Das Installationsprogramm wird automatisch gestartet, wenn der Installations Datenträger (automatische Testlauf) eingefügt wird.
-   Der Begrüßungsbildschirm – mit Optionen zum Installieren, entfernen, Anzeigen der Website oder zum Beenden von – wird nicht angezeigt, wenn das Spiel noch nicht auf dem Computer installiert ist.
-   Das **Installations** Dialogfeld ist das erste Dialogfeld, das vom Installationsprogramm angezeigt wird.
-   Die Schaltfläche **Installieren** ist die Implementierung des automatischen Installationsmodus.
-   Die **options** Schaltfläche ist die Implementierung des benutzerdefinierten Installationsmodus.
-   Mit der Schaltfläche **Abbrechen** wird das Installationsprogramm sofort beendet. Da das Starten des Installers eine triviale Aktion für den Benutzer ist, werden Sie nicht zur Bestätigung aufgefordert.
-   Sobald der Benutzer die Lizenzbedingungen akzeptiert und einen gültigen Product Key eingibt, wird die Installation gestartet.
-   Wenn der Installationsvorgang beendet ist, wird das Spiel entweder automatisch gestartet, oder es wird ein Dialogfeld angezeigt, in dem der Benutzer benachrichtigt wird, dass die Installation beendet ist, und es werden zusätzliche Optionen angeboten, je nachdem, ob **nach der Installation ein Spiel ausgeführt** wird.
-   Das Kontrollkästchen " **Spiel ausführen** " bietet eine weitere Möglichkeit zum Starten des Spiels. Diese Option ist standardmäßig deaktiviert, da das Dialogfeld zum **Abschluss der Installation** nur angezeigt werden kann, wenn im Dialogfeld **Installationsoptionen** die Option **Spiel ausführen nach der Installation** deaktiviert wurde.
-   Mit der Schaltfläche " **OK** " wird das Dialogfeld geschlossen, und optional wird eine Aktion für die Schaltfläche " **Ausführen" ausgeführt** und **die** Info Kästchen

## <a name="summary"></a>Zusammenfassung

Spieler möchten so bald wie möglich ein Spiel spielen. Das letzte, was ein Spieler tun möchte, ist das Durchsuchen von Dialogfeldern und das Treffen von Optionen, die für alle anderen Spiele, die er installiert hat, identisch sind. Das Implementieren dieser Ideen kann die Zeit verkürzen, die ein Spieler bei der Installation eines Spiels unter Windows verbringt, und die Gesamtqualität des Windows-Spielerlebnisses verbessern.

 

 