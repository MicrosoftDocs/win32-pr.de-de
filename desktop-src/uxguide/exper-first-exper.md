---
title: Erste Erfahrung
description: In der idealen ersten Umgebung installieren Benutzer Ihr Programm und verwenden es sofort produktiv, ohne eine Reihe von Fragen zu beantworten oder eine Reihe von Dingen zu lernen.
ms.assetid: d925f71c-fc5a-4ff2-8f5d-9434c162b4b4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 04610b75e8ca4ea7602d00b840bbbd9002397d9e
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524454"
---
# <a name="first-experience"></a>Erste Erfahrung

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

In der idealen ersten Umgebung installieren Benutzer Ihr Programm und verwenden es sofort produktiv, ohne eine Reihe von Fragen zu beantworten oder eine Reihe von Dingen zu lernen.

Eine erste Benutzeroberfläche hilft Benutzern beim Übergang von ihrer ersten Belichtung zu einem neuen Programm oder Feature zur täglichen Verwendung.

Bei Windows-Programmen tritt die erste Erfahrung auf, wenn Benutzer das Setupprogramm ausführen. Setupprogramme in der Regel:

-   Fordern Sie den Benutzer auf, einem Endbenutzer-Lizenzvertrag (EULA) zuzustimmen.
-   Fragen Sie nach einem Product Key.
-   Zeigen Sie die erforderlichen konfigurationsbezogenen Optionen an, einschließlich der Installation optionaler Software.
-   Kopieren Sie die Software auf die Festplatte des Benutzers.
-   Zeigen Sie Programmoptionen an, die für alle Benutzer gelten.

![Screenshot des Dialogfelds "Product Key eingeben" ](images/exper-first-exper-image1.png)

Teil einer typischen Windows-Setup-Benutzeroberfläche.

Die erste Benutzeroberfläche setzt dann die erste Verwendung des Programms oder Features fort. Diese erste Verwendungserfahrung kann:

-   Zeigen Sie Programmoptionen an, die nur für den aktuellen Benutzer gelten.
-   Anbieten von Produkt- oder Featuretutorials.

![Screenshot des Dialogfelds "Willkommenscenter" ](images/exper-first-exper-image2.png)

Die erste Verwendungserfahrung.

**Hinweis:** Richtlinien im Zusammenhang mit [Programmoptionen](win-property-win.md) werden in einem separaten Artikel vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Berücksichtigen Sie die folgenden Fragen, um die Entscheidung zu treffen.

### <a name="setup-experience"></a>Einrichtungserfahrung

Gelten die folgenden Bedingungen?

-   Die richtigen Einstellungen sind für die Verwendung des Programms erforderlich und gelten für alle Benutzer.
-   Die Einstellungen passen eine Kernerfahrung an oder eine, die für die persönliche Identifikation des Benutzers mit dem Programm entscheidend ist.
-   Es gibt keinen sicheren Standardwert, der Benutzer wählt wahrscheinlich Einstellungen aus, die nicht die Standardeinstellungen sind, oder die Standardeinstellungen erfordern die Zustimmung des Benutzers.
-   Es ist unwahrscheinlich, dass der Benutzer die Einstellungen nach dem Setup ändert.
-   Zum Ändern der Einstellungen ist eine Erhöhung erforderlich.

Falls ja, sollten Sie die Einstellungen während der Einrichtungserfahrung darstellen.

### <a name="first-use-experience"></a>Erste Verwendungserfahrung

Gelten die folgenden Bedingungen?

-   Die richtigen Einstellungen oder Aufgaben sind für die Verwendung des Programms oder Features erforderlich und gelten für einzelne Benutzer.
-   Die Einstellungen passen eine Kernerfahrung an oder eine, die für die persönliche Identifikation des Benutzers mit dem Programm entscheidend ist.
-   Es gibt keinen sicheren Standardwert, der Benutzer wählt wahrscheinlich Einstellungen aus, die nicht die Standardeinstellungen sind, oder die Standardeinstellungen erfordern die Zustimmung des Benutzers.
-   Benutzer treffen wahrscheinlich bessere Entscheidungen im Kontext des Programms als im Setup.
-   Es ist unwahrscheinlich, dass der Benutzer einstellungen mithilfe von Optionen ändert.

Falls ja, sollten Sie die Aufgaben und Einstellungen während der ersten Verwendung des Programms oder Features darstellen.

## <a name="design-concepts"></a>Entwurfskonzepte

In der idealen ersten Umgebung installieren Benutzer Ihr Programm (oder starten es einfach, wenn es keine Installation erfordert) und verwenden es sofort produktiv, ohne eine Reihe von Fragen zu beantworten oder eine Reihe von Dingen zu lernen.

Dieses Ideal ist für die meisten Programme erhältlich, daher sollten Sie nach möglichkeit nach dieser idealen Erfahrung suchen. Dieses Ziel ist jedoch häufig nicht für Programme zu erhalten, die eine erhebliche Systemintegration erfordern, viele optionale Features aufweisen oder Auswirkungen auf den Datenschutz haben. Wenn Ihr Programm z. B. Über Features verfügt, die möglicherweise personenbezogene Informationen für nicht vertrauenswürdige Parteien preisgeben, erfordern die Grundsätze des [vertrauenswürdigen Computings,](https://www.microsoft.com/mscorp/twc/default.mspx) dass Sie die Zustimmung des Benutzers einholen, bevor Sie diese Features aktivieren.

### <a name="questions-arent-choices"></a>Fragen sind keine Auswahlmöglichkeiten

Fragen erfordern Antworten, die beantwortet werden müssen, bevor Benutzer fortfahren können. Fragen während der ersten Erfahrung sind Hindernisse, über die Benutzer springen müssen, bevor sie Ihr Programm produktiv nutzen können. Im Gegensatz dazu sind Optionen optional. Benutzer müssen nicht darauf reagieren oder können sie nur anzeigen, wenn sie möchten.

Daher sind einstellungen, die im Hauptablauf eines Setup-Assistenten angezeigt werden, Fragen, während Einstellungen außerhalb des Haupteinrichtungsflows oder in einem Programmoptionendialogfeld Auswahlmöglichkeiten sind. Unnötige Fragen machen die erste Erfahrung Ihres Programms umständlich und lang, sodass die positive Erwartung und Freundlichkeit der Benutzer beim Einstieg in Ihr Programm effektiv beseitigt wird.

### <a name="use-the-first-experience-when-you-must"></a>Verwenden Sie die erste Benutzeroberfläche, wenn Sie

Stellen Sie Benutzern einstellungen und Aufgaben während der ersten Erfahrung vor, wenn Sie dies tun müssen, aber in der Regel gibt es bessere Alternativen:



| Erste Erfahrung  | Alternativen       |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Setupfragen<br/>                  | Wählen Sie die entsprechenden Standardwerte aus.<br/> Benutzern das Ändern von Programmoptionen gestatten.<br/> Stellen Sie typische und benutzerdefinierte Setuppfade bereit. <br/> |
| Fragen zur ersten Verwendung<br/>              | Wählen Sie die entsprechenden Standardwerte aus, und erlauben Sie Benutzern, von Programmoptionen zu wechseln.<br/>                                                            |
| Erste Verwendungsaufgaben<br/>                  | Präsentieren Sie stattdessen kontextabhängig.<br/>                                                                                                           |
| Erste Verwendung von Featureanzeigen<br/> | Machen Sie die gängigsten und wichtigsten Aufgaben erkennbar und kontextabhängig.<br/>                                                                   |
| Tutorials zur ersten Verwendung<br/>              | Machen Sie Programmfeatures selbsterklärend.<br/>                                                                                                 |
| Produktregistrierung<br/>             | Geben Sie den Befehl im Menü Hilfe und im Feld Informationen an.<br/>                                                                                             |



 

**Wenn Sie nur eine Sache tun...**

Halten Sie Ihre erste Erfahrung so einfach wie möglich. Lassen Sie Ihr Programm sofort funktionieren. Wählen Sie sichere, bequeme Standardwerte aus, und stellen Sie während des Setups Fragen, und verwenden Sie sie nur dann, wenn Sie dies benötigen.

Sie haben nur eine Möglichkeit, einen guten ersten Eindruck zu machen, und dieser erste Eindruck ist dauerhaft.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Beschränken Sie die erste Benutzererfahrung auf Aufgaben und Einstellungen, die für die Verwendung eines Programms oder Features erforderlich sind, und schließen Sie diese nur ein, wenn es keine bessere Alternative gibt.** Alternativen finden Sie in der vorherigen Tabelle.
    -   **Ausnahme:** Fügen Sie der ersten Benutzeroberfläche Personalisierungs- oder Programmanpassungseinstellungen hinzu, wenn ihre Anpassung Teil der Kernerfahrung oder entscheidend für die persönliche Identifikation des Benutzers mit dem Programm ist.

![Screenshot des Dialogfelds "Computernamen eingeben" ](images/exper-first-exper-image3.png)

Windows fragt Benutzer während des Setups nach dem Computernamen und der Wahl des Hintergrunds, da diese Einstellungen dabei helfen, eine emotionale Verbindung mit dem Produkt herzustellen.

-   **Verwenden Sie die Setup-Benutzeroberfläche** für Aufgaben und Einstellungen, wenn sie für alle Benutzer gelten oder das Ändern von Einstellungen erhöhte Rechte erfordert.
-   **Verwenden Sie die erste Benutzeroberfläche** für Aufgaben und Einstellungen, wenn sie für einzelne Benutzer gelten.

### <a name="presentation"></a>Präsentation

-   **Optionale Aufgaben und Einstellungen werden den erforderlichen Aufgaben und Einstellungen vorgezogen.** Vermeiden Sie es, Benutzer zu zwingen, Ihr Programm zu konfigurieren.

    ![Screenshot des Dialogfelds "Neue Hardware gefunden" ](images/exper-first-exper-image4.png)

    Im Dialogfeld Neue Hardware gefunden ist es optional, Treibersoftware zu installieren, anstatt sie zu einer erforderlichen Aufgabe zu machen.

-   **Nehmen Sie nach Möglichkeit optionale Aufgaben und Einstellungen aus dem Haupttaskflow heraus.** Viele Setupprogramme stellen beispielsweise einen benutzerdefinierten Installationspfad bereit, um selten geänderte Einstellungen aus dem Haupttaskflow zu entfernen.

    ![Screenshot der vollständigen und benutzerdefinierten Optionsfelder ](images/exper-first-exper-image5.png)

    Eine Einrichtungserfahrung, die den Haupttaskflow erleichtert, wenn der Benutzer die Installation nicht anpassen möchte.

-   **Überlasten Sie Benutzer nicht mit Aufgaben und Einstellungen:**
    -   **Fangen Sie einfach an.** Beginnen Sie mit einfachen Personalisierungseinstellungen und dem Fortschritt hin zu komplexeren, technischen Aufgaben und Einstellungen. Das Windows-Setup beginnt beispielsweise mit persönlichen Informationen und endet mit der Netzwerkkonfiguration.
    -   **Verwenden Sie eine kontextbezogene erste Benutzeroberfläche** für Aufgaben und Einstellungen, wenn sie nur für Features gelten, die für das Hauptprogramm nicht von grundlegender Bedeutung sind.

        ![Screenshot des Dialogfelds "Audio- und Videoeinrichtung" ](images/exper-first-exper-image6.png)

        Windows Live Messenger verfügt über ein kontextbezogenes Setup für Audio und Video, da sie von sekundären Features verwendet werden.

-   **Stellen Sie nicht alles auf einmal vor.** Konsolidieren Sie, um eine einzelne Benutzeroberfläche anstelle mehrerer Benutzeroberflächenoberflächen zu verwenden, oder zeigen Sie Aufgaben zu unterschiedlichen Zeitpunkten anstelle von allen gleichzeitig an.

    **Falsch:**

    ![Screenshot von fünf überlappenden Dialogfeldern ](images/exper-first-exper-image7.png)

    In diesem Beispiel ist die erste Verwendungserfahrung überfordernd.

-   **Stellen Sie Fragen und Optionen in Bezug auf die Ziele und Aufgaben der Benutzer, nicht in Bezug auf die Technologie.** Stellen Sie Optionen zur Verfügung, die Benutzer verstehen und eindeutig unterscheiden können. Stellen Sie sicher, dass Sie genügend Informationen bereitstellen, damit Benutzer fundierte Entscheidungen treffen können.
-   **Wenn die Notwendigkeit persönlicher Informationen nicht offensichtlich ist, erläutern Sie, warum Ihr Programm die Informationen benötigt und wie sie verwendet werden.**

    ![Screenshot des Texts, in dem die Verwendung der E-Mail-Adresse angezeigt wird ](images/exper-first-exper-image8.png)

    In diesem Beispiel wird in einer E-Commerce-Anwendung erläutert, wie personenbezogene Informationen verwendet werden.

-   **Stellen Sie die ersten Funktionen nur dann im Vollbildmodus zur Verfügung, wenn Benutzer andere Aufgaben nicht produktiv ausführen können.** Beispielsweise wird das Windows-Setup im Vollbildmodus angezeigt, um Benutzer davon abzuraten, andere Aufgaben auszuführen, während Windows installiert wird. Die meisten ersten Erfahrungen sollten nicht im Vollbildmodus angezeigt werden.

### <a name="settings"></a>Einstellungen

-   **Wählen Sie für alle Einstellungen den sichersten Wert (um Datenverlust oder Systemzugriff zu verhindern), standardmäßig den sichersten und privaten Wert aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den wahrscheinlichsten oder bequemsten Wert aus. Die Auswahl guter Standardwerte ist eine effektive Möglichkeit, die erste Erfahrung zu vereinfachen.
-   **Benutzer müssen sich für Dies ist erforderlich:**

    -   Einstellungen mit rechtlichen Auswirkungen, z. B. Endbenutzerlizenzverträge (EULAs). Solche Einstellungen können keine Standardauswahl haben.
    -   Features, die automatische Systemkonfigurationsänderungen ausführen, z. B. automatische Windows-Updates.
    -   Features, die personenbezogene Informationen (Personally Identifiable Information, PII) oder Systeminformationen anzeigen.
    -   Änderungen am Desktop des Benutzers über das Hinzufügen von Einträgen zum Startmenü, z. B. das Hinzufügen von Symbolen zum Desktop oder der Schnellstartleiste.
    -   Optionale Software, z. B. Produktverbesserungen, Abonnements und Produkte von Drittanbietern.

    ![Screenshot des Dialogfelds "Features auswählen" ](images/exper-first-exper-image9.png)

    In diesem Beispiel entscheiden sich Benutzer für Produktverbesserungen, Abonnements und Produkte von Drittanbietern.

-   **Wenn eine Einstellung dringend empfohlen wird, fügen Sie der Bezeichnung "(recommended)" hinzu.** Achten Sie bei Optionsfeldern und Kontrollkästchen darauf, der Steuerelementbezeichnung und nicht den zusätzlichen Hinweisen hinzuzufügen.
-   **Wenn eine Einstellung nur für fortgeschrittene Benutzer vorgesehen ist, fügen Sie der Bezeichnung "(advanced)" hinzu.** Achten Sie bei Optionsfeldern und Kontrollkästchen darauf, der Steuerelementbezeichnung und nicht den zusätzlichen Hinweisen hinzuzufügen.

### <a name="tasks"></a>Aufgaben

-   **Helfen Sie Benutzern, Wartezeiten produktiv zu übergeben.**
    -   Wenn die Wartezeit in der Regel zwischen ein und zwei Minuten liegt, sollten Sie hilfreiche Informationen bereitstellen, während Benutzer warten, z. B. eine Präsentation der Neuen während des Setups.
    -   Wenn die Wartezeit in der Regel länger als zwei Minuten ist, können Benutzer problemlos andere Aufgaben ausführen. Zeigen Sie die geschätzte Wartezeit an, empfehlen Sie Benutzern, in der Zwischenzeit etwas anderes zu tun, und machen Sie den Abschluss der Aufgabe offensichtlich, indem Sie den Bildschirm erheblich ändern.
-   **In der ersten Übung werden Tutorials präsentiert.** Wahrscheinlich möchten Benutzer Ihr Programm sofort verwenden und sind an Tutorials zu einem späteren Zeitpunkt interessiert.
-   **Verwenden Sie in der ersten Erfahrung keine Featurebenachrichtigungsbenachrichtigungen.** Anstatt eine Featurebenachrichtigung zu [verwenden,](mess-notif.md)entwerfen Sie das Feature so, dass es in Kontexten einfacher zu finden ist, in denen es benötigt wird, oder machen Sie keine besonderen Maßnahmen, und lassen Sie Benutzer das Feature selbst entdecken.
-   **Verwenden Sie während der ersten Windows-Beerfahrung keine Benachrichtigungen.** Um die erste Erfahrung zu verbessern, unterdrückt Windows 7 alle Benachrichtigungen, die während der ersten Nutzungsstunden angezeigt werden. Entwerfen Sie Ihr Programm so, dass Benutzern keine solchen Benachrichtigungen angezeigt werden.

 

