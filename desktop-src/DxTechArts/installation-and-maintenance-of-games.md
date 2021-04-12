---
title: Installation und Wartung von spielen
description: In diesem Artikel wird eine Reihe bewährter Methoden beschrieben, mit denen die Benutzer Frustration in der Zeit, die zum Installieren eines Spiels erforderlich ist, vermieden werden kann, unnötige Support Anrufe vermieden werden und es Benutzern ermöglicht wird, das Spiel so schnell und einfach wie möglich zu spielen.
ms.assetid: c953165d-2318-ca06-a895-abedcbcb594c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de171fd76654eb3b6edb8818ec073c4ef5ba8ca4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316376"
---
# <a name="installation-and-maintenance-of-games"></a>Installation und Wartung von spielen

In diesem Artikel wird eine Reihe bewährter Methoden beschrieben, mit denen die Benutzer Frustration in der Zeit, die zum Installieren eines Spiels erforderlich ist, vermieden werden kann, unnötige Support Anrufe vermieden werden und es Benutzern ermöglicht wird, das Spiel so schnell und einfach wie möglich zu spielen.

-   [Erst Installation](#initial-installation)
    -   [Optimieren der Installations Benutzeroberfläche](#streamlining-the-installation-ui)
    -   [Verkürzen der für die Installation benötigten Zeit](#reducing-the-time-required-for-installation)
    -   [Minimale Installation](#minimal-installation)
    -   [Bedarfs gesteuert installieren](#install-on-demand)
-   [Spiele nach der Installation](#post-installation-game-play)
    -   [Auto ausführen](#autorun)
    -   [Umstellen einer Installation bei Bedarf in eine vollständige Installation](#converting-an-install-on-demand-installation-to-a-full-installation)
    -   [Wartung von Spiel Software und Inhalten](#maintenance-of-game-software-and-content)
    -   [Automatisches Suchen nach Updates](#checking-for-updates-automatically)
    -   [Patches werden automatisch heruntergeladen](#downloading-patches-automatically)
-   [Andere Ressourcen](#other-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="initial-installation"></a>Erstinstallation

Die Benutzer kaufen Spiele, weil Sie Sie spielen, nicht, weil Sie Sie nicht installieren können. Die Installation eines Spiels sollte so schnell, unkompliziert und so unkompliziert wie möglich für den Endbenutzer erfolgen. Im Idealfall sollte den Endbenutzern nicht einmal eine Installations Benutzeroberfläche angezeigt werden. Sie sollten in der Lage sein, den Spiel Datenträger einfach in der Info Leiste abzulegen und wieder zu spielen.

### <a name="streamlining-the-installation-ui"></a>Optimieren der Installations Benutzeroberfläche

Allgemeine Aspekte der vorhandenen Spielinstallation beeinträchtigen die gewünschte Endbenutzer Leistung:

-   Stellen Sie dem Benutzer unnötige Fragen.

    Viele Spiele Fragen z. b., ob der Benutzer DirectX installieren möchte. Wenn das Spiel erfordert, dass Microsoft DirectX ausgeführt wird, und die richtige Version von DirectX nicht bereits installiert ist, sollte das Spiel einfach DirectX installieren.

-   Fragen Sie den Benutzer, dass eine große Mehrheit der Benutzer auf die gleiche Weise antwortet.

    Für typische Benutzer sind die Standardeinstellungen für den Installationspfad, den Speicherort des Start Menüs usw. in Ordnung. Bieten Sie erweiterte Optionen für Benutzer, die diese Einstellungen ändern möchten.

Die Benutzeroberfläche für die Installation sollte so entworfen werden, dass der typische Benutzer so bald wie möglich mit der Wiedergabe des Spiels beginnen kann. Wenn AutoRun auf dem Computer des Benutzers aktiviert ist (Standardeinstellung), sollte das Setup Programm davon ausgehen, dass der Benutzer das Spiel so schnell wie möglich wiedergeben möchte. dabei werden unnötige Fragen umgangen. Die Installation von installationsp[on Demand](#install-on-demand)m sollte die Installation des Spiels mit dem Standard Installationspfad beginnen, vorzugsweise mithilfe eines-Setups, wie in beschrieben. Es ist sinnvoll, Benutzern zu gestatten, die Installationseinstellungen zu ändern, bevor Sie die Installation automatisch starten. Dies sollte jedoch erreicht werden, indem der Benutzer aufgefordert wird, einen Schlüssel für erweiterte Setup Optionen zu erreichen, und dann automatisch mit den Standardoptionen fortzufahren, wenn der Benutzer diesen Schlüssel nicht innerhalb von fünf bis zehn Sekunden erreicht.

Wenn AutoRun auf dem Computer des Benutzers nicht aktiviert ist, sollte das Setup Programm davon ausgehen, dass der Benutzer nicht automatisch mit der Installation des Spiels beginnen soll. Wenn das Setup Programm auf andere Weise als Autorun gestartet wird, sollte die erweiterte Setup-Benutzeroberfläche gestartet werden.

### <a name="reducing-the-time-required-for-installation"></a>Verkürzen der für die Installation benötigten Zeit

Die meisten Microsoft Windows-Spiele nehmen heute zwischen fünf Minuten und einer halben Stunde Zeit in Anspruch, um den Installationsvorgang abzuschließen. Im Gegensatz dazu beanspruchen die meisten Konsolenspiele höchstens 30 Sekunden ab dem Zeitpunkt, an dem der Benutzer die Spiele-CD einfügt. Dieser Unterschied ist darauf zurückzuführen, dass die meisten Windows-Spiele so konzipiert sind, dass Sie die meisten, wenn nicht alle Inhalte von der Festplatte des Computers ausführen. Konsolen, die keinen Platz zum permanenten Speichern großer Mengen von Inhalten haben, erfordern, dass der Inhalt vom Quell Medium aus ausgeführt wird. Beim Laden von Inhalten von der lokalen Festplatte werden schnellere Ladezeiten für das Spiel ausgeführt. der Nachteil ist jedoch, dass der gesamte Inhalt an einem bestimmten Punkt von den Quell Medien auf die Festplatte kopiert werden muss. Bei den meisten Windows-spielen wird der gesamte Inhalt im Rahmen eines Installationsvorgangs auf die Festplatte kopiert. Dies beeinträchtigt die anfängliche Benutzer Darstellung des Benutzers, indem der Benutzer für einige Minuten eine Statusanzeige anfordert, bevor er das Spiel spielen kann.

Es gibt zwei Ansätze, die verwendet werden können, um die Zeit zu minimieren, die bei der anfänglichen Installation des Spiels aufgewendet wurde: [minimale Installation](#minimal-installation) und [Bedarfs](#install-on-demand)gesteuerte Installation.

### <a name="minimal-installation"></a>Minimale Installation

Bei einem minimalen Installationsszenario installiert das Spiel nur einen minimalen minimalen Satz an Inhalten auf der Festplatte. Normalerweise besteht dies nur aus der ausführbaren Datei des Spiels und den DLLs. Der Rest des Inhalts wird direkt vom Quell Medium aus aufgerufen. Dadurch wird die für die Installation erforderliche Zeit drastisch reduziert, da die ausführbare Datei eines Spiels selten größer als 10-20 MB ist. Der Nachteil ist, dass das Spiel das Laden von Inhalten während des Spiels länger dauert, da es von dem langsameren Quell Medium geladen werden muss.

So erstellen Sie eine minimale Installations Konfiguration in einer Windows Installer basierten Einrichtung:

-   Gruppieren Sie alle zu installierenden Komponenten auf der Festplatte in einer Funktion, die für die lokale Installation markiert ist.

    Diese Funktion wird als "Bootstrap"-Funktion bezeichnet.

-   Gruppieren Sie alle Komponenten, die vom Quell Medium ausgeführt werden sollen, in eine Funktion, die als "aus Quelle ausführen" gekennzeichnet ist.
-   Wenn Sie eine Datei öffnen, die sich möglicherweise auf dem Quell Medium befindet, verwenden Sie die [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) -Funktion, um den Pfad zu der Datei zu bestimmen, anstatt den Pfad hart zu codieren.

    Dadurch wird sichergestellt, dass die Datei auch dann gefunden werden kann, wenn sich der Laufwerk Buchstabe des CD/DVD-Laufwerks des Benutzers ändert.

-   Komprimieren Sie Inhalte, die auf der CD/DVD verbleiben.

    Die Menge an CPU-Zeit, die zum Testen des Inhalts aufgewendet wird, wird normalerweise durch die langsame Übertragungsrate der Daten vom CD/DVD-Laufwerk ausgeblendet.

-   Gruppieren Sie Inhalte in großen, zusammenhängenden Dateien, und greifen Sie in sequenzieller Reihenfolge darauf zu.

    Die Suchzeiten von CD/DVD-Laufwerken sind im Vergleich zu den Festplatten geringer, und die meisten CD/DVD-Laufwerke erreichen keine Spitzen Übertragungsraten, es sei denn, Sie lesen eine große, zusammenhängende Datei.

-   Legen Sie Inhalte auf CD/DVD in der Reihenfolge fest, in der der Zugriff darauf möglich ist.

    Die Suchzeiten werden erheblich reduziert, wenn auf Dateien in der gleichen Reihenfolge wie das Layout auf dem Datenträger zugegriffen wird.

### <a name="install-on-demand"></a>Bedarfs gesteuert installieren

Bei einem on-Demand-Szenario, wie bei minimaler Installation, wird das Spiel zunächst auf der Festplatte installiert, um nur die Dateien zu installieren, die zum Starten des Spiels benötigt werden. Anstatt jedoch jedes Mal, wenn Sie benötigt wird, auf den verbleibenden Inhalt des Quell Mediums zuzugreifen, installiert das Spiel tatsächlich jeden Inhalt auf der Festplatte, da er zum ersten Mal benötigt wird, und greift dann bei jeder nachfolgenden Verwendung von der lokalen Festplatte aus darauf zu. Die für die Erstinstallation erforderliche Zeit ist für eine minimale Installation so klein wie in, aber nach dem ersten Zugriff auf jeden Inhalt werden die Ladezeiten verbessert.

So erstellen Sie eine install-on-Demand-Konfiguration in einer Windows Installer basierten Installation:

-   Gruppieren Sie alle Komponenten, die anfänglich auf der Festplatte installiert werden sollen, in eine Funktion, die für die lokale Installation markiert ist.

    Beachten Sie, dass dies mit dem Bootstrap-Feature für eine minimale Installation identisch ist.

-   Gruppieren Sie den verbleibenden Inhalt auf der Grundlage von Komponenten, die mit hoher Wahrscheinlichkeit verwendet werden, in mehrere Features.

    Gruppieren Sie z. b. in einem ebenenbasierten Spiel alle Inhalte, die auf einer bestimmten Ebene verwendet werden, zu einem Feature. Beachten Sie, dass Windows Installer die gemeinsame Verwendung einer Komponente durch mehrere Features zulässt. Wenn Sie also über Inhalte verfügen, die auf mehreren Ebenen verwendet werden, können Sie diesen Inhalt den Features für alle erforderlichen Ebenen hinzufügen, ohne den Inhalt zu replizieren. Alle diese Features sollten als "angekündigt" gekennzeichnet werden, was bedeutet, dass Sie nicht anfänglich installiert werden, sondern später nach Bedarf installiert werden können.

-   Wenn eine Datei benötigt wird, überprüfen Sie zunächst, ob die Datei bereits mit der [**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea)-Funktion installiert ist.

    Wenn Sie noch nicht installiert ist (d. h., der Status ist "InstallState" \_ angekündigt), wenden Sie die Funktion " [**msikonfigurirefeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) " an, um die Funktion lokal zu installieren. Wenn die Datei nach der Installation geöffnet wird, müssen Sie [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) aufrufen, um den Pfad zu der Datei zu bestimmen. Obwohl es für dieses Szenario nicht unbedingt erforderlich ist (da der Inhalt vor der Verwendung immer auf der Festplatte installiert wird), ist es einfacher, die minimale Installation zusätzlich zur Installation bei Bedarf zu unterstützen.

-   Wenn möglich, sollten Sie vorhersehen, welcher Inhalt bald benötigt wird, und ihn während der Leerlaufzeit im Hintergrund installieren.

    Die Hintergrund Installation ist am besten geeignet, wenn sich das Spiel an einem Punkt befindet, der nicht alle letzten Leistungsdaten des Computers benötigt. Dies ist beispielsweise der Fall, wenn ein Intro-Film, eine Ausschneide Szene, ein Menü usw. angezeigt wird.

-   Erstellen Sie eine Option im Menü Optionen des Spiels, um die Installation aller verbleibenden Inhalte zu erzwingen.

    Um dies zu implementieren, erstellen Sie ein Feature, das übergeordnet ist, und rufen Sie dann [**msikonfiguriertes**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) Feature auf, um diese Master Funktion lokal zu installieren. Dies führt dazu, dass die Teilfunktionen auch lokal installiert werden.

-   Das Inhalts Layout sollte bei einer minimalen Installation ähnlich sein, mit der Ausnahme, dass Inhalte nur mit anderen Inhalten gruppiert werden sollen, die wahrscheinlich zur gleichen Zeit benötigt werden (z. b. der gesamte Inhalt für eine Ebene sollte gleich sein).

## <a name="post-installation-game-play"></a>Game-Play nach der Installation

### <a name="autorun"></a>Auto ausführen

Um ein bereits installiertes Spiel zu spielen, sollte der Benutzer nur den Installations Datenträger in der Laufwerk Leiste ablegen. Als erstes muss die ausführbare autorun-Datei auf der Festplatte überprüft werden, um zu überprüfen, ob das Spiel bereits installiert wurde. ist dies der Fall, starten Sie das Spiel. Wenn Sie davon ausgehen, dass das Spiel mithilfe eines Windows Installer basierten Setups installiert wurde, können Sie überprüfen, ob das Spiel installiert ist, indem Sie die Funktion " [**msiqueryproductstate**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea)" abrufen.

### <a name="converting-an-install-on-demand-installation-to-a-full-installation"></a>Umstellen einer Installation bei Bedarf in eine vollständige Installation

Während eine Installation bei Bedarf den Benutzer viel schneller als eine vollständige Installation spielen kann, möchte ein Benutzer den Rest der Spielinhalte explizit auf der lokalen Festplatte installieren. Der Benutzer möchte das Spiel möglicherweise ohne das Quell Medium abspielen, oder er möchte einfach die längere Ladezeiten vermeiden, die durch die Installation von Inhalten bei Bedarf entstehen. Wenn das Setup des Spiels Windows Installer verwendet, kann das Spiel in der Benutzeroberfläche der in-Game-Optionen eine Option bereitstellen, um die Installation der restlichen Inhalte abzuschließen. Wenn der Benutzer diese Option auswählt, kann das Spiel [**msikonfigurirefeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) anrufen, um zu erzwingen, dass die restlichen Funktionen lokal installiert werden. hierfür ist es nicht erforderlich, eine separate Setup Anwendung zu erstellen.

### <a name="maintenance-of-game-software-and-content"></a>Wartung von Spiel Software und Inhalten

Einer der Vorteile, den Windows-Spiele gegenüber Konsolen spielen haben, ist die relative Leichtigkeit, mit der der Herausgeber Updates für das Spiel nach seiner ersten Veröffentlichung veröffentlichen kann. Unabhängig davon, ob diese Updates neue Inhalte einführen oder Probleme beheben, ist es wichtig, den Aktualisierungsprozess für den Endbenutzer so einfach wie möglich zu gestalten. Der Aktualisierungsprozess ist für Online Spiele noch wichtiger, da in der Regel alle Benutzer die neueste Version des Spiels ausführen müssen, um eine Verbindung herzustellen.

### <a name="checking-for-updates-automatically"></a>Automatisches Suchen nach Updates

Benutzer sollten nicht daran denken, Patches zu suchen. Wenn ein Update für das Spiel verfügbar ist, sollte der Benutzer zumindest benachrichtigt werden, und im Idealfall sollte der Patch bereits heruntergeladen werden.

Eine einfache Möglichkeit für ein Spiel, nach Updates zu suchen, ist das Herstellen einer Verbindung mit einem Webserver, der vom Verleger mithilfe einer bestimmten URL gehostet wird, und das Herunterladen einer Textdatei, die die Versionsnummer der letzten verfügbaren Version des Spiels angibt, sowie einer URL, aus der ein Paket heruntergeladen wird, das das Spiel auf die neueste Version aktualisiert.

Die Suche nach Updates jedes Mal, wenn der Benutzer das Spiel spielt, ist ausreichend, um sicherzustellen, dass der Benutzer die neueste Version ausgeführt hat. Wenn das vorhanden sein eines neuen Updates jedoch unmittelbar vor der Wiedergabe des Spiels erkannt wird, wird der Benutzer möglicherweise gezwungen, das Spiel zu verzögern, bis der Download abgeschlossen ist. Bei großen Updates oder langsamen Verbindungen kann diese Verzögerung in der Reihenfolge der Stunden liegen. Um zu vermeiden, dass der Benutzer vor dem Spielen des Spiels wartet, kann das Spiel Taskplaner verwenden, um regelmäßige Überprüfungen auf neue Updates zu planen. Wenn ein Update erkannt wird, kann das Spiel sofort mit dem Herunterladen des Updates beginnen, sodass es wahrscheinlich vollständig heruntergeladen und bereit für die Installation ist, wenn der Benutzer das Spiel das nächste Mal spielt.

### <a name="downloading-patches-automatically"></a>Patches werden automatisch heruntergeladen

Nachdem das Spiel festgestellt hat, dass ein neues Update verfügbar ist, sollte es sofort mit dem Herunterladen des Updates beginnen. Da der Task, der die Überprüfung auf Updates durchführt, in der Regel im Hintergrund ausgeführt wird, muss der Download so unaufdringlich wie möglich sein. Bei der Background Intelligent Transfer Service (Bits) handelt es sich um ein Betriebssystem Feature, mit dem Anwendungen Dateien aus dem Internet herunterladen können, auch wenn die Anwendung selbst nicht ausgeführt wird. Bits-Download Aufträge werden nur ausgeführt, wenn der Benutzer angemeldet ist, und nur, wenn der Computer bereits mit dem Netzwerk verbunden ist. Bits versucht nicht zu erzwingen, dass der Computer eigenständig eine Verbindung mit dem Netzwerk herstellt. Wenn der Benutzer die Verbindung mit dem Netzwerk trennt oder abmeldet, wird der BITS-Auftrag angehalten, und der Download wird wieder aufgenommen, wenn sich der Benutzer das nächste Mal anmeldet und eine Verbindung mit dem Netzwerk herstellt. Die Anwendung kann ihre Bits-Aufträge so konfigurieren, dass nur die Netzwerkbandbreite verwendet wird, die andernfalls nicht verwendet wird, um zu verhindern, dass der Auftrag die Leistung anderer Anwendungen beeinträchtigt, die möglicherweise das Netzwerk verwenden (z. b. ein Onlinespiel). Bits ist unter Windows XP und Windows 2000 Service Pack 3 verfügbar.

## <a name="other-resources"></a>Weitere Ressourcen

Weitere Informationen zu den Technologien, auf die in diesem Artikel verwiesen wird, finden Sie in den entsprechenden Abschnitten der MSDN Library:

-   [Windows Installer](/windows/desktop/Msi/windows-installer-portal)
-   [Aufgabenplanung](/windows/desktop/TaskSchd/task-scheduler-start-page)
-   [Background Intelligent Transfer Service](/windows/desktop/Bits/background-intelligent-transfer-service-portal) (Bits)

Weitere Informationen zur Verwendung von Windows Installer für Spiele finden Sie im Artikel "Einführung in Windows Installer für Spieleentwickler" im nächsten Monat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Msikonfigurierfeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[**Msiqueryproductstate**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea)
</dt> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea)
</dt> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 