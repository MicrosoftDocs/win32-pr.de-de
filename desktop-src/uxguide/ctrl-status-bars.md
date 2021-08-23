---
title: Statusleisten (Entwurfsgrundinformationen)
description: Eine Statusleiste ist ein Bereich am unteren Rand eines primären Fensters, in dem Informationen über den Zustand des aktuellen Fensters (z. B. was angezeigt wird und wie), Hintergrundaufgaben (z. B. Drucken, Scannen und Formatieren) oder andere Kontextinformationen (z. B. Auswahl und Tastaturzustand) angezeigt werden.
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: fa76563adbd3810b48339cc49014441512e3d76a0ac7484ff632f64f635b4cf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934177"
---
# <a name="status-bars-design-basics"></a>Statusleisten (Entwurfsgrundinformationen)

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Eine Statusleiste ist ein Bereich am unteren Rand eines primären Fensters, in dem Informationen über den Zustand des aktuellen Fensters (z. B. was angezeigt wird und wie), Hintergrundaufgaben (z. B. Drucken, Scannen und Formatieren) oder andere Kontextinformationen (z. B. Auswahl und Tastaturzustand) angezeigt werden.

Statusleisten geben in der Regel den Status über Text und Symbole an, können aber auch Statusindikatoren sowie Menüs für Befehle und Optionen im Zusammenhang mit dem Status enthalten.

![Screenshot der typischen Statusleiste ](images/ctrl-status-bars-image1.png)

Eine typische Statusleiste.

> [!Note]  
> Richtlinien im Zusammenhang mit [dem Benachrichtigungsbereich](winenv-notification.md) werden in einem separaten Artikel vorgestellt.

 

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Ist der Status relevant, wenn Benutzer aktiv andere Programme verwenden?** Verwenden Sie in diesem Bereich ein [Symbol für den Benachrichtigungsbereich.](winenv-notification.md)
-   **Muss das Statuselement Benachrichtigungen anzeigen?** Wenn ja, müssen Sie ein Symbol für den Benachrichtigungsbereich verwenden.
-   **Ist das Fenster ein primäres Fenster?** Wenn nicht, verwenden Sie keine Statusleiste. Dialogfelder, Assistenten, Systemsteuerungen und Eigenschaftenblätter sollten keine Statusleisten haben.
-   **Sind die Informationen in erster Linie Status?** Wenn nicht, verwenden Sie keine Statusleiste. Statusleisten dürfen nicht als sekundäre Menüleiste [oder](cmd-menus.md) Symbolleiste [verwendet werden.](cmd-toolbars.md)
-   **Wird in den Informationen erläutert, wie das ausgewählte Steuerelement verwendet wird?** Wenn ja, zeigen Sie die Informationen neben dem zugeordneten Steuerelement stattdessen mit einer ergänzenden Erklärung oder Anweisungsbezeichnung an.
-   **Ist der Status nützlich und relevant? Das heißt, werden Benutzer wahrscheinlich ihr Verhalten als Folge dieser Informationen ändern?** Falls nicht, zeigen Sie den Status entweder nicht an, oder speichern Sie ihn in einer Protokolldatei.
-   **Ist der Status kritisch? Ist sofortiges Handeln erforderlich?** Wenn ja, zeigen Sie die Informationen in einem Formular an, [](win-dialog-box.md) das Aufmerksamkeit erfordert und nicht einfach ignoriert werden kann, z. B. in einem Dialogfeld oder im primären Fenster selbst.

    ![Screenshot der roten Statusleiste "Zertifikatfehler" ](images/ctrl-status-bars-image2.png)

    Eine rote Adressleiste in Windows Internet Explorer.

-   **Ist das Programm in erster Linie für erfahrene Benutzer vorgesehen?** Unerfahrene Benutzer kennen in der Regel keine Statusleisten, daher sollten Sie in diesem Fall die Verwendung von Statusleisten durchdenken.

## <a name="design-concepts"></a>Entwurfskonzepte

Statusleisten sind eine hervorragende Möglichkeit, um Statusinformationen zur Verfügung zu stellen, ohne Benutzer zu unterbrechen oder ihren Flow zu unterbrechen. Statusleisten sind jedoch leicht zu übersehen. So einfach, dass viele Benutzer überhaupt keine Statusleisten bemerken.

Die Lösung für dieses Problem besteht nicht in der Anforderung der Aufmerksamkeit des Benutzers durch die Verwendung von Symbolen, Animationen oder Flashen, sondern im Entwurf für diese Einschränkung. Gehen Sie dafür so vor:

-   **Stellen Sie sicher, dass die Statusinformationen nützlich und relevant sind.** Falls nicht, geben Sie keine Statusleiste an.
-   **Verwenden Sie keine Statusleisten für wichtige Informationen.** Benutzer sollten nie wissen müssen, was sich in der Statusleiste befindet. Wenn Benutzer sie sehen müssen, sollten Sie sie nicht in eine Statusleiste setzen.

**Wenn Sie nur eins tun...**

Stellen Sie sicher, dass die Statusleisteninformationen nützlich und relevant, aber nicht entscheidend sind.

## <a name="usage-patterns"></a>Verwendungsmuster

Statusleisten haben mehrere Verwendungsmuster:



|   Verwendung                                                                                                                                 |    Beispiel                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aktueller Fensterstatus**<br/> Anzeigen der Quelle der angezeigten Inhalte zusammen mit allen Ansichtsmodi <br/>              | ![Screenshot der Statusleiste "Standort" ](images/ctrl-status-bars-image3.png)<br/> In diesem Beispiel zeigt die Statusleiste den Pfad zum Dokument an.<br/>                                                         |
| **Progress**<br/> Zeigen Sie den Fortschritt von Hintergrundaufgaben an, entweder mit einer bestimmten Statusleiste oder einer Animation. <br/> | ![Screenshot der Statusleiste mit Statusleiste ](images/ctrl-status-bars-image4.png)<br/> In diesem Beispiel enthält die Statusleiste eine Statusleiste, um das Laden der Webseite in ein Internet Explorer anzuzeigen.<br/> |
| **Kontextinformationen**<br/> Anzeigen von Kontextinformationen darüber, was der Benutzer gerade tut. <br/>              | ![Screenshot der Statusleiste mit der Anzahl von Pixeln ](images/ctrl-status-bars-image5.png)<br/> In diesem Beispiel Microsoft Paint die Auswahlgröße in Pixeln.<br/>                                           |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   Erwägen Sie die Bereitstellung eines Befehls "Statusleiste anzeigen", wenn nur einige Benutzer die Statusleisteninformationen benötigen. Blenden Sie die Statusleiste standardmäßig aus, wenn die meisten Benutzer sie nicht benötigen.
-   Verwenden Sie nicht die Statusleiste, um Menüleistenelemente zu erläutern. Dieses Hilfemuster ist nicht erkennbar.

### <a name="presentation"></a>Präsentation

-   Deaktivieren Sie den modalen Status, der nicht gilt. Der modale Status umfasst Tastatur- und Dokumentzustände.
-   Entfernen Sie den nicht modalen Status, der nicht gilt.
-   Statusinformationen in der folgenden Reihenfolge anzeigen: aktueller Fensterstatus; progress; und Kontextinformationen.

### <a name="icons"></a>Symbole

-   Wählen Sie leicht erkennbare Statussymbolentwürfe aus. Bevorzugen Sie Symbole mit eindeutigen Konturen gegenüber quadratischen oder rechteckigen, formten Symbolen.
-   Verwenden Sie Nur Swaths von rein rot, gelb und grün, um Statusinformationen zu übermitteln. Andernfalls sind solche Symbole verwirrend.

    **Richtig:**

    ![Screenshot der Statusleiste mit blauen Symbolen ](images/ctrl-status-bars-image6.png)

    **Falsch:**

    ![Screenshot der Statusleiste mit einem roten Symbol ](images/ctrl-status-bars-image7.png)

    Im falschen Beispiel schlägt das rote Symbol unbeabsichtigt einen Fehler vor, was zu Verwirrung führt.

-   Verwenden Sie Symbolvarianten oder Überlagerungen, um Status- oder Statusänderungen anzuzeigen. Verwenden Sie Symbolvarianten, um Änderungen an Mengen oder Stärken anzuzeigen. Verwenden Sie für andere Statustypen die folgenden Standardüberlagerungen: 

    | Überlagerung                 | Status            |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | ![Screenshot des Warnsymbols ](images/ctrl-status-bars-image8.png)<br/>                | Warnung<br/>               |
    | ![Screenshot des Fehlersymbols ](images/ctrl-status-bars-image9.png)<br/>                  | Fehler<br/>                 |
    | ![Screenshot des Symbols "Deaktiviert/Getrennt" ](images/ctrl-status-bars-image10.png)<br/> | Deaktiviert/Getrennt<br/> |
    | ![Screenshot des Symbols "Blockiert/Offline" ](images/ctrl-status-bars-image11.png)<br/>       | Blockiert/Offline<br/>       |

    

     

-   Ändern Sie den Status nicht zu häufig. Statusleistensymbole sollten nicht laut oder instabil sein und keine Aufmerksamkeit erfordern. Das Auge ist empfindlich auf Änderungen im Peripheriebereich des Sehens, daher müssen Statusänderungen dezent sein.
-   Für Symbole, die wichtige Statusinformationen bereitstellen, bevorzugen Sie ortsspezifische Bezeichnungen.
-   Nicht gekennzeichnete Statusleistensymbole sollten QuickInfos enthalten.

Weitere Informationen finden Sie unter [Symbole](vis-icons.md).

### <a name="interaction"></a>Interaktion

-   Gestalten Sie einen Statusleistenbereich interaktiv, um Benutzern den direkten Zugriff auf verwandte Befehle und Optionen zu ermöglichen.
    -   Verwenden Sie ein Steuerelement, das [](ctrl-command-buttons.md) wie eine Menüschaltfläche oder eine geteilte Schaltfläche aussieht und sich verhält. Diese Statusleistenbereiche müssen über einen Dropdownpfeil verfügen, um anzugeben, dass sie angeklickt werden können.
    -   Zeigen Sie das Menü beim Klicken mit der linken Maustaste nach unten an, nicht mit der Maus nach oben.
    -   Rechtsklick oder Doppelklicken werden nicht unterstützt. Benutzer erwarten solche Interaktionen in einer Statusleiste nicht, sodass sie sie wahrscheinlich nicht versuchen.
-   Zeigen Sie QuickInfos an, wenn Sie darauf zeigen.

## <a name="text"></a>Text

-   Verwenden Sie im Allgemeinen präzise Bezeichnungen. Schneiden Sie beliebigen Text aus, der entfernt werden kann.
-   Ziehen Sie Satzfragmente vor, ohne die Interpunktion zu beenden. Verwenden Sie vollständige Sätze (mit endender Interpunktion) nur, wenn Satzfragmente nicht deutlich kürzer sind.
-   Geben Sie für optionale Statusbezeichnungen an, was der Vorgang mit einer Bezeichnung macht, die mit einem Verb (Gerundform) beginnt und mit einem Auslassungszeichen endet. Beispiel: "Kopieren...". Diese Bezeichnung kann sich dynamisch ändern, wenn der Vorgang mehrere Schritte auf sich hat oder mehrere Objekte verarbeitet.
-   Verwenden Sie keine Farben, Fett- oder Italic-Striche, um Statusleistentext zu hervorheben.
-   Richtlinien für QuickInfo-Formulierungen finden Sie unter [QuickInfos und Infotips.](ctrl-tooltips-and-infotips.md)

## <a name="documentation"></a>Dokumentation

Statusleisten werden als Statusleisten bezeichnet, nicht als Statuszeilen oder andere Variationen. Beispiel: "Die aktuelle Seitenzahl wird auf der Statusleiste angezeigt."

 

