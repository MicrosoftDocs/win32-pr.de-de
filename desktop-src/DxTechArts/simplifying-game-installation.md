---
title: Vereinfachen der Spieleinstallation
description: In diesem Artikel werden einige Konzepte beschrieben, die Entwickler von Spielen für Windows implementieren können und sollten, um die Gesamterfahrung zu verbessern.
ms.assetid: 356780b7-801d-c6dd-a266-6272bcb8bd36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53062b9905e59435f1b9175eb95832294d93e51193003622d3bcc6dd16ee07df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042468"
---
# <a name="simplifying-game-installation"></a>Vereinfachen der Spieleinstallation

Ein großer Vorteil von Spielen, die in einer Konsole statt auf Windows ausgeführt werden, ist der Installationsvorgang – oder deren Fehlen. Wenn ein Spiel zum ersten Mal in einer Konsole ausgeführt wird, trifft der Spieler einige Auswahlmöglichkeiten oder Bestätigungen und kann fast sofort mit der Wiedergabe beginnen. Die Installation eines Spiels auf Windows ist im Vergleich dazu komplizierter, da erhebliche Benutzereingaben erforderlich sind und der Installationsvorgang möglicherweise lange dauert. Dieser Installationsvorgang kann jedoch verbessert werden, um Spieler von Windows-basierten Spielen besser zu erleben. In diesem Artikel werden einige Konzepte beschrieben, die Entwickler von Spielen für Windows implementieren können und sollten, um die Gesamterfahrung zu verbessern.

-   [Typische Spielinstallation](#typical-game-installation)
-   [Vereinfachte Spielinstallation](#simplified-game-installation)
    -   [Alle Fragen im Voraus stellen](#ask-all-questions-up-front)
    -   [Bereitstellen spezieller Installationsmodi](#provide-special-installation-modes)
    -   [Minimieren der Anzahl von Installationsfragen](#minimize-the-quantity-of-installation-questions)
    -   [Ändern optionaler Komponenten in erforderliche Komponenten](#change-optional-components-into-required-components)
    -   [Installieren Sie Immer DirectX, und führen Sie dies im Hintergrund aus.](#always-install-directx-and-do-so-silently)
    -   [Denken Sie an Ihre Lizenzvereinbarung.](#think-about-your-eula)
    -   [Automatisch nach der Installation starten](#automatically-launch-after-installation)
    -   [Optimieren der Installationsleistung](#optimize-your-installation-performance)
    -   [Registrieren bei Windows Firewall während der Installation](#register-with-windows-firewall-during-installation)
    -   [Installation für alle Benutzer, nicht nur für den aktuellen Benutzer](#install-for-all-users-not-just-the-current-user)
-   [Beispiel für eine vereinfachte Installation](#example-of-simplified-installation)
-   [Zusammenfassung](#summary)

## <a name="typical-game-installation"></a>Typische Spielinstallation

Beim Vergleich der Einfachheit der Installation und der Zeit, die zum Spielen eines Spiels erforderlich ist, ist die typische Xbox-Erfahrung viel besser als Windows. Das Flussdiagramm in Abbildung 1 zeigt die typischen Installationsprozesse auf Xbox und auf Windows zum Vergleich.

**Abbildung 1: Typischer Installationsprozess, Xbox im Vergleich zu Windows**

![Xbox \- im Vergleich zu \- PC](images/pcvsconsoleinstall.png)

## <a name="simplified-game-installation"></a>Vereinfachte Spielinstallation

Die höheren Anforderungen an den Benutzer, ein Spiel auf Windows zu installieren, müssen jedoch nicht sein. Durch die Implementierung der folgenden Konzepte verringern Sie die Anzahl der Schritte, die ein Benutzer ausführen muss, was die für die Installation benötigte Zeit verkürzen kann.

### <a name="ask-all-questions-up-front"></a>Alle Fragen im Voraus stellen

Alle Auswahlmöglichkeiten, die der Spieler während der Installation auswählt, die möglicherweise dazu führen, dass die Installation abgebrochen wird, sollten vor den Optionen angeboten werden, die die Installation nicht beenden. Im schlimmsten Fall wird dem Spieler eine Auswahl angeboten, die dazu führen kann, dass die Installation abgebrochen wird, nachdem das Spiel vollständig von den Installationsmedien kopiert wurde. Dies kann besonders frustrierend sein, wenn für die Installation der Austausch mehrerer Datenträger erforderlich ist. Sie sollten Ihren Installer so entwerfen, dass zu Beginn des Prozesses alle wichtigen Fragen gestellt werden (z. B. die Zustimmung zur Lizenzvereinbarung), damit für die Installation kein Rollback ausgeführt werden muss.

Sie können den Benutzer auch auffordern, die Lizenzbedingungen zu akzeptieren und den Product Key einzugeben, wenn das Spiel zum ersten Mal gestartet wird, anstatt diese im Rahmen der Installation anzufordern. In diesem Szenario wird die Installation nicht zurückgesetzt, wenn sie die Lizenzvereinbarung akzeptieren oder während der Eingabe des Product Key abbrechen, da diese Eingabeaufforderungen Teil des Spiels selbst sind. Dies kann nützlich sein, wenn Sie vorinstallierte oder OEM-Szenarien verwendet haben. Achten Sie jedoch darauf, den Benutzer nicht aufzufordern, beim ersten Start Entscheidungen zu treffen, die Administratoranmeldeinformationen erfordern.

### <a name="provide-special-installation-modes"></a>Bereitstellen spezieller Installationsmodi

Im Idealfall sollten Windows Spielinstallationsprogramme nur vollständig automatische und benutzerdefinierte Installationsmodi und nichts dazwischen bieten.

Der automatische Modus sollte keine weiteren Fragen stellen, als unbedingt erforderlich sind, um eine funktionsfähige Installation zu erstellen, und einfach Standardeinstellungen verwenden, ohne zur Eingabe anderer Optionen aufzufordern. Viele Spieler interessieren sich nicht für die Position des Spiels auf der Festplatte oder die anfänglichen Spieleinstellungen– sie möchten das Spiel so schnell wie möglich spielen.

Der benutzerdefinierte Modus sollte nur für Hauptbenutzer gelten, die den Installationspfad oder andere Installationsoptionen benötigen oder ändern möchten, und er sollte nicht der Standardmodus sein.

Der benutzerdefinierte Modus kann die Wahl zwischen einer vollständigen Installation oder einer Mindestinstallation bieten, die nur die Dateien installiert, die zum Spielen des Spiels erforderlich sind. Wenn der Spieler die Mindestinstallation ausschließt, kann das Spiel Install-on-Demand- oder Streamingtechniken verwenden, um die verbleibenden Installationsdaten zu lesen, wodurch der Spieler schnell mit dem Spielen beginnen kann, ohne auf den Abschluss einer vollständigen Installation warten zu müssen. Das Installieren von Daten auf diese Weise wirkt sich jedoch auf das Design der Spiel-Engine aus. Weitere Informationen zum Installieren von Inhalten bei Bedarf finden Sie unter [Install-on-Demand for Games](/windows/desktop/DxTechArts/install-on-demand-for-games).

### <a name="minimize-the-quantity-of-installation-questions"></a>Minimieren der Anzahl von Installationsfragen

In beiden Installationsmodi sollten Sie versuchen, die Anzahl der Aufforderungen des Spielers während der Installation zu begrenzen. Dadurch wird der Leseaufwand reduziert, der erforderlich ist, um das Spiel zu installieren und auszuführen. Bei Bedarf sollte nach Abschluss der Installation nur eine Folgeaufforderung angezeigt werden. Wie Sie sehen können, enthält das in Abbildung 1 gezeigte Beispiel zu viele Eingabeaufforderungen nach der Installation.

### <a name="change-optional-components-into-required-components"></a>Ändern optionaler Komponenten in erforderliche Komponenten

Machen Sie die Installation aller Komponenten erforderlich, anstatt sie optional zu machen, es sei denn, es gibt einen guten Grund, dies andernfalls zu tun. Wenn Sie einfach alle Komponenten installieren, wird das Spiel ohne weitere Verzögerung und ohne weitere Verzögerung gestartet.

### <a name="always-install-directx-and-do-so-silently"></a>Installieren Sie Immer DirectX, und führen Sie dies im Hintergrund aus.

Es wird dringend empfohlen, das DirectX Redistributable, für das das Spiel erstellt wurde, im Hintergrund zu installieren. Der DirectX-Installationsprozess ist so konzipiert, dass überprüft wird, ob etwas aktualisiert werden muss, und es wird schnell zurückgegeben, wenn dies nicht der Dereinst ist. Daher müssen Benutzer nicht gefragt werden, ob DirectX installiert werden soll. Eine automatische Installation von DirectX kann ausgeführt werden, indem Sie den folgenden Befehl aus Ihrem Installationspaket ausführen: **dxsetup.exe /silent**

Die Frage eines Benutzers, ob er DirectX installieren möchte, kann viele Probleme verursachen. Wenn der Benutzer beispielsweise annimmt, dass die neueste verteilbare Version installiert ist und die Installation von DirectX übersprungen werden soll, Die Installation des Spiels könnte trotzdem erfolgreich fortgesetzt werden. Wenn das Spiel jedoch eine bestimmte Version von D3DX oder eine andere aktualisierte Funktionalität erfordert, die übersprungen wurde, funktioniert das Spiel nicht, und der Benutzer ist sehr frustriert.

Wenn Sie den Benutzer aus irgendeinem Grund fragen müssen, ob er DirectX installieren möchte, sollte Ihr Installationsprogramm – zumindest – den gesamten Installationsvorgang abbrechen und ein Rollback durchführen, wenn der Benutzer sich gegen die Installation von DirectX entscheidet. Ein Rollback der Installation vermeidet Fehler, die dadurch verursacht werden, dass auf dem System nicht die neueste Version von DirectX installiert ist, wenn das Spiel gestartet wird.

Beachten Sie, dass es wichtig ist, das Weiterverteilbare zu versenden, für das Ihr Spiel erstellt wurde, anstatt einfach das redistributable aus dem neuesten DirectX SDK zu versenden. Die neueste redistributable-Version enthält möglicherweise nicht alle Komponenten, die in einer früheren Version gefunden wurden.

Es ist auch wichtig, dass das Installationsprogramm überprüft wird, um festzustellen, was bereits installiert ist, und zu bestimmen, ob ein Neustart des Systems erforderlich ist. Wenn DirectX auf dem neuesten Stand ist, sollte das Kopieren einer DLL keinen Neustart erfordern.

### <a name="think-about-your-eula"></a>Denken Sie an Ihre Lizenzvereinbarung.

Die Lizenzbedingungen für DirectX können und sollten an die Lizenzbedingungen des Spieleentwicklers angefügt werden. Es hat keinen Sinn, dem Benutzer zu erlauben, der Lizenzbedingungen des Entwicklers und nicht der Lizenzbedingungen für DirectX zuzustimmen. Entweder muss der Benutzer beiden EULAs zustimmen oder das Spiel nicht installieren. Wenn ein Entwickler der Meinung ist, dass er dem Benutzer die Auswahl anbieten muss, sollte die gesamte Installation fehlschlagen, wenn der Benutzer dem DirectX-Lizenzvertrag nicht zustimmen möchte.

Wenden Sie sich nach Möglichkeit an Ihre Rechtsabteilung, um zu prüfen, ob Sie EULAs vollständig vermeiden können, und verwenden Sie eine verkleinerte Lizenzbedingungen wie Konsolenspielnutzung. Dadurch müssen Benutzer nicht gefragt werden, ob sie die Lizenzvereinbarung akzeptieren möchten. Die Lizenzvereinbarung für DirectX muss an die verkleinerte Lizenzvereinbarung angefügt werden. Andernfalls muss die Lizenzbedingungen für DirectX angezeigt und akzeptiert werden, was den Zweck der Verwendung einer lizenzbedingungen mit Verkleinerung verwindet.

Eine Ausnahme von einer verkleinerten EULA ist für einen Inhalts-Editor. Jeder Editor muss während der Installation des Editors oder beim ersten Starten des Editors eine Lizenzvereinbarung anzeigen. Viele Gamer sind nur an der Wiedergabe und nicht am Erstellen von Inhalten interessiert, sodass die Installation eines Editors ein separater Prozess sein sollte.

### <a name="automatically-launch-after-installation"></a>Automatisch nach der Installation starten

Fast alle Spieler möchten ein Spiel spielen, sobald sie es erhalten. Standardmäßig sollte das Installationsprogramm das Spiel nach Abschluss der Installation starten, obwohl es in einer benutzerdefinierten Installation eine bewährte Methode ist, dies in einem Kontrollkästchen anzugeben, das der Benutzer überschreiben kann.

### <a name="optimize-your-installation-performance"></a>Optimieren der Installationsleistung

Entwickler sollten ihre Installationen testen, um zu ermitteln, wie viel Zeit für die Installation benötigt wird. Entwickler können die Installationszeit verkürzen, indem sie die neueste Version ihrer Installationstools verwenden und das Datenlayout auf den Installationsmedien optimieren. Die meisten DVD-Erstellungstools verfügen über Optionen für die Layoutoptimierung, die die Installationszeiten verbessern können, ohne die Entwicklungsworkload zu erhöhen.

### <a name="register-with-windows-firewall-during-installation"></a>Registrieren bei Windows Firewall während der Installation

Wenn Ihr Spiel als Server ausgeführt werden kann oder das Netzwerkmodell des Spiels Peer-zu-Peer ist, registrieren Sie Ihr Spiel zur Installationszeit bei Windows Firewall. Dadurch wird verhindert, dass das Firewalldialogfeld während des Spiels angezeigt wird, wenn der Benutzer versucht, auf das Netzwerk zuzugreifen. Wenn es sich bei dem Spiel um einen reinen Client handelt, sollte das Installationsprogramm das Spiel nicht der Ausnahmenliste der Firewall hinzufügen.

Weitere Informationen finden Sie unter Windows Firewall für Spieleentwickler.

### <a name="install-for-all-users-not-just-the-current-user"></a>Installation für alle Benutzer, nicht nur für den aktuellen Benutzer

Standardmäßig wird das Spiel für alle Benutzer installiert. Dadurch kann jeder neue Benutzer auf dem System das Spiel spielen, ohne es für ihn installieren zu müssen. Wenn die Installation für alle Benutzer in einem Least-Privileged Benutzerkonto versucht wird, schlägt das Installationsprogramm entweder fehl oder fordert den Benutzer zur Eingabe eines Administratorkennworts auf. Versuchen Sie also zu ermitteln, ob das Konto über die richtigen Berechtigungen verfügt, bevor Sie die Option zur Installation für alle Benutzer anbieten. Wenn der Benutzer das Spiel nur für den aktuellen Benutzer installiert, achten Sie darauf, den Installationspfad in einen Speicherort im Profil des Benutzers zu ändern. Im Idealfall ändern Sie den Pfad an einen Ort in nicht roamingbasierten Anwendungsdaten (z. B. ein Unterverzeichnis von CSIDL \_ LOCAL \_ APPDATA).

## <a name="example-of-simplified-installation"></a>Beispiel für eine vereinfachte Installation

Abbildung 2 ist ein Beispiel für einen verbesserten Prozess zum Installieren eines Spiels in Windows mit vereinfachten Installationsdialogfeldern.

**Abbildung 2. Vereinfachter Installationsprozess**

![Installieren](images/simplifiedgameinstall.png)

Im Folgenden sind wichtige Punkte zu beachten:

-   Das Installationsprogramm wird beim Einfügen des Installationsdatenträgers automatisch gestartet (automatische Ausführung).
-   Der Begrüßungsbildschirm mit Optionen zum Installieren, Entfernen, Anzeigen der Website oder Beenden wird nicht angezeigt, wenn das Spiel noch nicht auf dem Computer installiert ist.
-   Das **Dialogfeld Installation** ist das erste Dialogfeld, das vom Installationsprogramm angezeigt wird.
-   Die Schaltfläche **Installieren** ist die Implementierung des automatischen Installationsmodus.
-   Die Schaltfläche **Optionen** ist die Implementierung des benutzerdefinierten Installationsmodus.
-   Mit der Schaltfläche **Abbrechen** wird das Installationsprogramm sofort beendet. Da das Starten des Installationsprogramms eine triviale Aktion für den Benutzer ist, fordern Sie nicht zur Bestätigung auf.
-   Sobald der Benutzer die Lizenzbedingungen akzeptiert und einen gültigen Product Key eingibt, wird die Installation gestartet.
-   Wenn der Installationsvorgang abgeschlossen ist, wird das Spiel entweder automatisch gestartet oder ein Dialogfeld angezeigt, in dem der Benutzer darüber informiert wird, dass die Installation abgeschlossen ist, und weitere Optionen angeboten werden, je nachdem, ob **Spiel nach der Installation ausführen** ausgewählt wurde.
-   Das **Kontrollkästchen Spiel ausführen** bietet der Einfachheit halber eine weitere Möglichkeit, das Spiel zu starten. Diese Option ist standardmäßig immer deaktiviert, da das Dialogfeld **Installation abgeschlossen** nur angezeigt werden kann, wenn Das Spiel nach der **Installation ausführen** im Dialogfeld **Installationsoptionen** deaktiviert wurde.
-   Mit der Schaltfläche **OK** wird das Dialogfeld verworfen, und optional werden Aktionen für die Kontrollkästchen **Ausführen** und Anzeigen **der Readme** ausgeführt.

## <a name="summary"></a>Zusammenfassung

Spieler möchten so bald wie möglich ein Spiel spielen. Das letzte, was ein Spieler tun möchte, ist das Waden durch Dialoge und das Treffen von Entscheidungen, die mit denen für alle anderen Spiele identisch sind, die er installiert hat. Die Implementierung dieser Ideen kann die Zeit verkürzen, die ein Spieler für die Installation eines Spiels auf Windows aufwendet, und die Gesamtqualität der Windows Spielerfahrung verbessern.

 

 