---
title: Erst malig
description: Bei der optimalen erstmaligen Benutzer Installation installieren Sie das Programm und verwenden es sofort, ohne eine Reihe von Fragen zu beantworten oder eine Reihe von Dingen kennenzulernen.
ms.assetid: d925f71c-fc5a-4ff2-8f5d-9434c162b4b4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c965ae77507b0041d17cabb34c4f53dc8216c134
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218948"
---
# <a name="first-experience"></a>Erst malig

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Bei der optimalen erstmaligen Benutzer Installation installieren Sie das Programm und verwenden es sofort, ohne eine Reihe von Fragen zu beantworten oder eine Reihe von Dingen kennenzulernen.

Eine Benutzeroberfläche für die erstmaligen Benutzeroberfläche unterstützt Benutzer beim Übergang von ihrer ersten Übertragung zu einem neuen Programm oder Feature zur alltäglichen Verwendung.

Bei Windows-Programmen tritt das erste Mal auf, wenn Benutzer das Setup Programm ausführen. Setup Programme sind in der Regel:

-   Erfordert, dass der Benutzer einen Endbenutzer-Lizenzvertrag (EULA) akzeptiert.
-   Fragen Sie nach einem Product Key.
-   Stellen Sie die erforderlichen Konfigurations bezogenen Optionen einschließlich der Installation optionaler Software zur Verfügung.
-   Kopieren Sie die Software auf die Festplatte des Benutzers.
-   Stellen Sie Programmoptionen dar, die für alle Benutzer gelten.

![Screenshot des Dialog Felds "geben Sie das Product Key" ein ](images/exper-first-exper-image1.png)

Teil eines typischen Windows-Setups.

Die erste Möglichkeit besteht dann in der ersten Verwendung des Programms oder Features. Diese erste Verwendung bietet folgende Möglichkeiten:

-   Stellen Sie Programmoptionen dar, die nur für den aktuellen Benutzer gelten.
-   Angebots Lernprogramme für Produkte oder Features.

![Screenshot des Willkommens Centers (Dialogfeld) ](images/exper-first-exper-image2.png)

Der erste Verwendungs Vorgang.

**Hinweis:** Richtlinien, die sich auf [Programmoptionen](win-property-win.md) beziehen, werden in einem separaten Artikel vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Beachten Sie die folgenden Fragen, um zu entscheiden.

### <a name="setup-experience"></a>Einrichtung

Gelten die folgenden Bedingungen?

-   Die richtigen Einstellungen sind erforderlich, um das Programm zu verwenden, und gelten für alle Benutzer.
-   Mit den Einstellungen wird eine zentrale Benutzerumgebung oder eine Lösung angepasst, die für die persönliche Identifizierung des Benutzers mit dem Programm entscheidend ist.
-   Es gibt keinen sicheren Standardwert, der Benutzer kann wahrscheinlich Einstellungen auswählen, die nicht die Standardeinstellung sind, oder die Standardeinstellungen erfordern eine Zustimmung des Benutzers.
-   Der Benutzer ist unwahrscheinlich, dass die Einstellungen nach der Installation geändert werden.
-   Das Ändern der Einstellungen erfordert eine Erhöhung der Rechte.

Wenn dies der Fall ist, sollten Sie die Einstellungen während der Einrichtung in Erwägung gezogen.

### <a name="first-use-experience"></a>Erste Verwendung

Gelten die folgenden Bedingungen?

-   Die richtigen Einstellungen oder Aufgaben sind erforderlich, um das Programm oder Feature zu verwenden, und gelten für einzelne Benutzer.
-   Mit den Einstellungen wird eine zentrale Benutzerumgebung oder eine Lösung angepasst, die für die persönliche Identifizierung des Benutzers mit dem Programm entscheidend ist.
-   Es gibt keinen sicheren Standardwert, der Benutzer kann wahrscheinlich Einstellungen auswählen, die nicht die Standardeinstellung sind, oder die Standardeinstellungen erfordern eine Zustimmung des Benutzers.
-   Benutzer treffen wahrscheinlich bessere Entscheidungen innerhalb des Programm Kontexts als innerhalb des Setups.
-   Der Benutzer ist unwahrscheinlich, dass Einstellungen mithilfe von Optionen geändert werden.

Wenn dies der Fall ist, sollten Sie die Aufgaben und Einstellungen während der ersten Verwendung des Programms oder Features vorstellen.

## <a name="design-concepts"></a>Entwurfskonzepte

Bei der optimalen erstmaligen Benutzer Installation installieren Sie das Programm (oder starten es auch einfach, wenn es keine Installation erfordert) und verwenden es sofort, ohne eine Reihe von Fragen zu beantworten oder eine Reihe von Dingen kennenzulernen.

Diese ideale Funktion ist für die meisten Programme nicht erreichbar. Daher sollten Sie sich bei Bedarf an dieser idealen Art bemühen. Dieses Ziel ist jedoch oft nicht für Programme zugänglich, die eine beträchtliche Systemintegration erfordern, viele optionale Features haben oder Auswirkungen auf den Datenschutz haben. Wenn Ihr Programm z. b. über Features verfügt, die möglicherweise persönliche Informationen für nicht vertrauenswürdige Parteien offenlegen, erfordern die Mandanten des [vertrauenswürdigen Computing](https://www.microsoft.com/mscorp/twc/default.mspx) , dass Sie die Zustimmung des Benutzers erhalten, bevor Sie diese Features aktivieren.

### <a name="questions-arent-choices"></a>Fragen sind keine Auswahlmöglichkeiten

Fragen erfordern Antworten, die beantwortet werden müssen, damit Benutzer den Vorgang fortsetzen können. Fragen während der ersten Darstellung sind Hürden, die Benutzer überspringen müssen, bevor Sie Ihr Programm produktiv verwenden können. Im Gegensatz dazu sind Optionen optional. Benutzer müssen nicht darauf antworten, oder Sie können Sie nur anzeigen, wenn Sie möchten.

Daher sind die im Haupt Ablauf eines Setup-Assistenten dargestellten Einstellungen Fragen, wohingegen Einstellungen außerhalb des Haupt-Setup-oder Dialog Felds "Programmoptionen" ausgewählt werden. Unnötige Fragen machen die erste Benutzer Arbeit Ihres Programms umständlich und lange, wodurch die positive Erwartung und die Aufregung, die Benutzer über die ersten Schritte mit Ihrem Programm haben, vermieden werden.

### <a name="use-the-first-experience-when-you-must"></a>Verwenden Sie die erste Möglichkeit, wenn Sie

Stellen Sie den Benutzern während der ersten Benutzeroberfläche Einstellungen und Aufgaben zur Verfügung, aber in der Regel gibt es bessere Alternativen:



|                                             |                                                                                                                                                    |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Erst malig**<br/>             | **Alternativen**<br/>                                                                                                                        |
| Fragen zum Setup<br/>                  | Wählen Sie geeignete Standardwerte aus.<br/> Benutzern das Ändern von Programmoptionen gestatten<br/> Stellen Sie typische und benutzerdefinierte Setup Pfade bereit. <br/> |
| Fragen zur ersten Verwendung<br/>              | Wählen Sie geeignete Standardwerte aus, und lassen Sie den Benutzern das Ändern von Programmoptionen zu.<br/>                                                            |
| Erste Verwendungs Aufgaben<br/>                  | Stattdessen in der Kontext Darstellung vorhanden.<br/>                                                                                                           |
| Verwenden Sie erst Funktions Ankündigungen.<br/> | Machen Sie die gängigsten und wichtigsten Aufgaben sichtbar und kontextbezogen.<br/>                                                                   |
| Erste Verwendungs Lernprogramme<br/>              | Machen Sie Programmfunktionen selbsterklärend.<br/>                                                                                                 |
| Produktregistrierung<br/>             | Geben Sie im Hilfemenü und im Feld Info einen Befehl an<br/>                                                                                             |



 

**Wenn Sie nur eine Aktion ausführen...**

Sorgen Sie dafür, dass Ihr erstes Verfahren so einfach wie möglich ist. Bringen Sie Ihr Programm sofort in Betrieb. Wählen Sie sichere, sichere und bequeme Standardwerte aus, und stellen Sie während des Setups Fragen.

Sie haben nur eine Chance, einen guten ersten Eindruck zu machen, und der erste Eindruck ist dauerhaft.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Beschränken Sie die erstmaligen Oberflächen auf Aufgaben und Einstellungen, die für die Verwendung eines Programms oder einer Funktion erforderlich sind, und schließen Sie diese nur ein, wenn keine bessere Alternative** Weitere Informationen finden Sie in der vorherigen Tabelle.
    -   **Ausnahme:** Fügen Sie der ersten Umgebung Personalisierungs-oder Programm Anpassungs Einstellungen hinzu, wenn ihre Anpassung Teil der Kern Umgebung ist oder für die persönliche Identifizierung des Benutzers mit dem Programm entscheidend ist.

![Screenshot des Dialog Felds "geben Sie einen Computernamen ein" ](images/exper-first-exper-image3.png)

Windows fragt Benutzer nach dem Computernamen und der Auswahl des Hintergrunds während des Setups ab, da diese Einstellungen eine emotionale Verbindung mit dem Produkt bilden.

-   **Verwenden Sie die Setup** Umgebung für Tasks und Einstellungen, wenn Sie für alle Benutzer gelten oder wenn Sie die Einstellungen ändern müssen.
-   **Verwenden Sie die erste Verwendungs** Umgebung für Tasks und Einstellungen, wenn Sie für einzelne Benutzer gelten.

### <a name="presentation"></a>Präsentation

-   **Bevorzugen Sie optionale Aufgaben und Einstellungen für erforderliche Tasks und Einstellungen.** Vermeiden Sie, dass Benutzer Ihr Programm konfigurieren.

    ![Screenshot des Dialog Felds "neue Hardware gefunden" ](images/exper-first-exper-image4.png)

    Im Dialogfeld neue Hardware finden ist es optional, Treibersoftware zu installieren, anstatt Sie als erforderliche Aufgabe zu verwenden.

-   **Nehmen Sie bei Bedarf optionale Aufgaben und Einstellungen aus dem Hauptaufgaben Fluss vor.** Viele Setup Programme stellen z. b. einen benutzerdefinierten Installationspfad bereit, um nicht häufig geänderte Einstellungen aus dem Hauptaufgaben Fluss zu entfernen.

    ![Screenshot der vollständigen und benutzerdefinierten Options Felder ](images/exper-first-exper-image5.png)

    Eine Setup-Benutzerfunktion, die den Hauptaufgaben Fluss erleichtert, wenn der Benutzer die Installation nicht anpassen möchte.

-   **Benutzer mit Aufgaben und Einstellungen nicht überfordern:**
    -   **Fangen Sie einfach an.** Beginnen Sie mit einfachen Personalisierungs Einstellungen und Fortschritt in Bezug auf komplexere, technische Aufgaben und Einstellungen. Beispielsweise beginnt Windows Setup mit persönlichen Informationen und endet mit der Netzwerkkonfiguration.
    -   Verwenden Sie für Aufgaben und Einstellungen **eine kontextabhängige erste** Umgebung, wenn Sie nur auf Funktionen angewendet werden, die für das Hauptprogramm nicht von Bedeutung sind.

        ![Screenshot des Dialog Felds "Einrichten von Audiodateien und Videos" ](images/exper-first-exper-image6.png)

        Windows Live Messenger hat eine kontextabhängige Einrichtung für Audiodaten und Videos, da Sie von sekundären Features verwendet werden.

-   **Präsentieren Sie alles nicht gleichzeitig.** Konsolidieren Sie, um eine einzelne Benutzeroberfläche anstelle mehrerer Benutzeroberflächen Oberflächen zu verwenden, oder zeigen Sie Aufgaben zu unterschiedlichen Zeiten anstelle von gleichzeitig an.

    **Falsch:**

    ![Screenshot der fünf überlappenden Dialogfelder ](images/exper-first-exper-image7.png)

    In diesem Beispiel ist die erste Verwendung überwältigend.

-   **Stellen Sie Fragen und Optionen in Bezug auf die Ziele und Aufgaben der Benutzer dar, nicht in Bezug auf die Technologie.** Geben Sie Optionen an, die Benutzer verstehen und eindeutig unterscheiden. Stellen Sie sicher, dass Sie genügend Informationen für Benutzer bereitstellen, um fundierte Entscheidungen zu treffen.
-   **Wenn die Notwendigkeit persönlicher Informationen nicht offensichtlich ist, erklären Sie, warum Ihr Programm die Informationen benötigt und wie diese verwendet werden.**

    ![Screenshot des Texts zum Angeben der e-Mail-Adress Verwendung ](images/exper-first-exper-image8.png)

    In diesem Beispiel wird in einer e-Commerce-Anwendung erläutert, wie persönliche Informationen verwendet werden.

-   **Präsentieren Sie zuerst den Vollbildmodus, wenn Benutzer nicht produktiv andere Aufgaben ausführen können.** Beispielsweise wird Windows Setup voll Bildschirm angezeigt, um Benutzer daran abzuraten, andere Aufgaben auszuführen, während Windows installiert wird. Die meisten ersten Erfahrungen sollten nicht voll Bildschirm sein.

### <a name="settings"></a>Einstellungen

-   **Wählen Sie für alle Einstellungen das sicherste (um den Verlust von Daten oder den System Zugriff zu verhindern), den sichersten und den privaten Wert standardmäßig aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den wahrscheinlichsten oder einfachsten Wert aus. Die Auswahl guter Standardwerte ist eine effektive Möglichkeit, das erste Verhalten zu vereinfachen.
-   **Benutzer müssen sich für Folgendes entscheiden:**

    -   Einstellungen mit rechtlichen Implikationen, wie z. b. Endbenutzer Lizenzverträge (EULAs). Diese Einstellungen können nicht über eine Standardauswahl verfügen.
    -   Features, die automatische Systemkonfigurations Änderungen ausführen, wie z. b. automatische Windows-Updates.
    -   Funktionen, die personenbezogene Informationen (PII) oder Systeminformationen offenlegen.
    -   Änderungen am Desktop des Benutzers über das Hinzufügen von Einträgen zum Startmenü, z. b. das Hinzufügen von Symbolen zum Desktop oder die Schnellstartleiste.
    -   Optionale Software, z. b. Produktverbesserungen, Abonnements und Produkte von Drittanbietern.

    ![Screenshot der gewünschten Features auswählen (Dialogfeld) ](images/exper-first-exper-image9.png)

    In diesem Beispiel abonnieren Benutzerprodukt Erweiterungen, Abonnements und Produkte von Drittanbietern.

-   **Wenn eine Einstellung stark empfohlen wird, fügen Sie "(empfohlen)" der Bezeichnung hinzu.** Stellen Sie für options Felder und Kontrollkästchen sicher, dass Sie der Steuerelement Bezeichnung und nicht den ergänzenden Notizen hinzufügen.
-   **Wenn eine Einstellung nur für fortgeschrittene Benutzer vorgesehen ist, fügen Sie der Bezeichnung "(erweitert)" hinzu.** Stellen Sie für options Felder und Kontrollkästchen sicher, dass Sie der Steuerelement Bezeichnung und nicht den ergänzenden Notizen hinzufügen.

### <a name="tasks"></a>Aufgaben

-   **Helfen Sie Benutzern, die Wartezeit produktiv zu übergeben.**
    -   Wenn die Wartezeit in der Regel zwischen 1 und zwei Minuten liegt, sollten Sie hilfreiche Informationen bereitstellen, während die Benutzer warten, z. b. eine Präsentation der Neuerungen während des Setups.
    -   Wenn die Wartezeit in der Regel länger als zwei Minuten ist, können Sie den Benutzern das Ausführen anderer Aufgaben erleichtern. Anzeigen der geschätzten Wartezeit, empfohlen, dass Benutzer in der Zwischenzeit etwas anderes ausführen und die Aufgaben Vervollständigung offenlegen, indem der Bildschirm erheblich geändert wird.
-   **Überdenken Sie bei der ersten Durchführung von Tutorials.** Die meisten Benutzer möchten das Programm sofort verwenden und sind zu einem späteren Zeitpunkt an Tutorials interessiert.
-   **Verwenden Sie bei der ersten Verwendung keine Benachrichtigungen zu featureankündigungen.** Anstatt eine Benachrichtigung über eine [featureankündigung](mess-notif.md)zu verwenden, sollten Sie die Funktion so entwerfen, dass Sie in den Kontexten, in denen Sie benötigt wird, einfacher zu erkennen ist
-   **Verwenden Sie während der anfänglichen Windows-Darstellung keine Benachrichtigungen.** Um die erste Umgebung zu verbessern, unterdrückt Windows 7 alle Benachrichtigungen, die während der ersten Stunden der Nutzung angezeigt werden. Entwerfen Sie Ihr Programm, vorausgesetzt, Benutzer werden keine Benachrichtigungen erhalten.

 

