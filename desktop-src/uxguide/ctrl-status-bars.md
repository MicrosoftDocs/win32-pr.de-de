---
title: Status leisten (Entwurfs Grundlagen)
description: Eine Statusleiste ist ein Bereich am unteren Rand eines primären Fensters, in dem Informationen zum Zustand des aktuellen Fensters angezeigt werden (z. b. was angezeigt wird und wie), Hintergrundaufgaben (z. b. Drucken, Scannen und Formatierungen) oder andere Kontextinformationen (z. b. Auswahl-und Tastatur Status).
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8f65d104f59cd0aec0c242d623f83c410c22f48d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218935"
---
# <a name="status-bars-design-basics"></a>Status leisten (Entwurfs Grundlagen)

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Eine Statusleiste ist ein Bereich am unteren Rand eines primären Fensters, in dem Informationen zum Zustand des aktuellen Fensters angezeigt werden (z. b. was angezeigt wird und wie), Hintergrundaufgaben (z. b. Drucken, Scannen und Formatierungen) oder andere Kontextinformationen (z. b. Auswahl-und Tastatur Status).

Status leisten zeigen in der Regel den Status über Text und Symbole an, Sie können jedoch auch Status Indikatoren und Menüs für Befehle und Optionen im Zusammenhang mit dem Status aufweisen.

![Screenshot der typischen Statusleiste ](images/ctrl-status-bars-image1.png)

Eine typische Statusleiste.

> [!Note]  
> Die Richtlinien im Zusammenhang mit dem [Benachrichtigungsbereich](winenv-notification.md) werden in einem separaten Artikel dargestellt.

 

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Ist der Status relevant, wenn Benutzer aktiv andere Programme verwenden?** Wenn dies der Fall ist, verwenden Sie ein [Benachrichtigungs Bereichs Symbol](winenv-notification.md).
-   **Muss das Status Element Benachrichtigungen anzeigen?** Wenn dies der Fall ist, müssen Sie ein Benachrichtigungs Bereichs Symbol verwenden.
-   **Ist das Fenster ein primäres Fenster?** Wenn dies nicht der Wert ist, verwenden Sie keine Statusleiste. Dialog Felder, Assistenten, Steuerelemente und Eigenschaften Blätter sollten keine Status leisten haben.
-   **Liegen die Informationen primär vor?** Wenn dies nicht der Wert ist, verwenden Sie keine Statusleiste. Status leisten dürfen nicht als sekundäre [Menüleiste](cmd-menus.md) oder [Symbolleiste](cmd-toolbars.md)verwendet werden.
-   **Erläutern die Informationen, wie das ausgewählte Steuerelement verwendet werden soll?** Wenn dies der Fall ist, zeigen Sie die Informationen neben dem zugeordneten Steuerelement mithilfe einer ergänzenden Erklärung oder Anweisungsbezeichnung an.
-   **Ist der Status hilfreich und relevant? Das heißt, Benutzer können Ihr Verhalten wahrscheinlich aufgrund dieser Informationen ändern?** Wenn dies nicht der Fall ist, wird der Status entweder nicht angezeigt oder in eine Protokolldatei eingefügt.
-   **Ist der Status kritisch? Ist eine sofortige Aktion erforderlich?** Wenn dies der Fall ist, zeigen Sie die Informationen in einem Formular an, das eine Aufmerksamkeit erfordert und nicht leicht ignoriert werden kann, z. b. ein [Dialogfeld](win-dialog-box.md) oder im primären Fenster selbst.

    ![Screenshot der roten "Zertifikat Fehler"-Statusleiste ](images/ctrl-status-bars-image2.png)

    Eine rote Adressleiste in Windows Internet Explorer.

-   **Ist das Programm hauptsächlich für Einsteiger vorgesehen?** Unerfahrene Benutzer sind in der Regel nicht mit Status leisten bekannt, daher sollten Sie in diesem Fall die Verwendung von Status leisten überdenken.

## <a name="design-concepts"></a>Entwurfskonzepte

Status leisten sind eine gute Möglichkeit, Statusinformationen bereitzustellen, ohne Benutzer zu unterbrechen oder den Flow zu unterbrechen. Status leisten können jedoch leicht übersehen werden. So einfach, dass viele Benutzer die Status leisten überhaupt nicht bemerken.

Die Lösung für dieses Problem ist nicht, die Aufmerksamkeit des Benutzers durch die Verwendung von grelle-Symbolen,-Animationen oder-blinken, aber zum Entwerfen dieser Einschränkung zu fordern. Gehen Sie dafür so vor:

-   **Stellen Sie sicher, dass die Statusinformationen hilfreich und relevant sind.** Wenn dies nicht der Wert ist, geben Sie keine Statusleiste an.
-   **Es werden keine Status leisten für wichtige Informationen verwendet.** Benutzer sollten nie wissen müssen, was sich in der Statusleiste befindet. Wenn Benutzer dies sehen müssen, sollten Sie Sie nicht in eine Statusleiste einfügen.

**Wenn Sie nur eine Aktion ausführen...**

Stellen Sie sicher, dass die Status leisten Informationen hilfreich und relevant, aber nicht entscheidend sind.

## <a name="usage-patterns"></a>Verwendungsmuster

Status leisten weisen mehrere Verwendungs Muster auf:



|                                                                                                                                    |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aktueller Fenster Status**<br/> Anzeigen der Quelle der angezeigten Elemente zusammen mit allen Ansichtsmodi <br/>              | ![Screenshot der Statusleiste "Standort" ](images/ctrl-status-bars-image3.png)<br/> In diesem Beispiel wird in der Statusleiste der Pfad zum Dokument angezeigt.<br/>                                                         |
| **Progress**<br/> Zeigen Sie den Fortschritt von Hintergrundaufgaben entweder mit einer bestimmte-Statusanzeige oder einer Animation an. <br/> | ![Screenshot der Statusleiste mit Fortschrittsanzeige ](images/ctrl-status-bars-image4.png)<br/> In diesem Beispiel enthält die Statusleiste eine Statusanzeige, in der das Laden der Webseite in ein Internet Explorer-Fenster angezeigt wird.<br/> |
| **Kontextinformationen**<br/> Zeigen Sie Kontextinformationen zum aktuellen Benutzer an. <br/>              | ![Screenshot der Statusleiste, die die Anzahl der Pixel anzeigt ](images/ctrl-status-bars-image5.png)<br/> In diesem Beispiel zeigt Microsoft Paint die Auswahl Größe in Pixel an.<br/>                                           |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   Wenn nur einige Benutzer die Status leisten Informationen benötigen, sollten Sie einen Befehl zum Anzeigen der Statusleiste angeben. Blenden Sie die Statusleiste standardmäßig aus, wenn Sie von den meisten Benutzern nicht benötigt wird.
-   Verwenden Sie die Statusleiste nicht, um Menüleisten Elemente zu erläutern. Dieses Hilfe Muster ist nicht erkennbar.

### <a name="presentation"></a>Präsentation

-   Deaktivieren Sie den modalen Status nicht. Der modale Status schließt Tastatur-und Dokument Zustände ein.
-   Entfernen Sie nicht modalen Status, der nicht zutrifft.
-   Statusinformationen in der folgenden Reihenfolge präsentieren: aktueller Fenster Status; Progress und Kontextinformationen.

### <a name="icons"></a>Symbole

-   Wählen Sie leicht erkennbare Statussymbol Entwürfe aus. Symbole mit eindeutigen Gliederungen über quadratische oder rechteckige förmige Symbole bevorzugen.
-   Verwenden Sie nur die Spitzen der reinen roten, gelben und grünen, um Statusinformationen zu kommunizieren. Andernfalls sind solche Symbole verwirrend.

    **Richtig:**

    ![Screenshot der Statusleiste mit blauen Symbolen ](images/ctrl-status-bars-image6.png)

    **Falsch:**

    ![Screenshot der Statusleiste mit einem roten Symbol ](images/ctrl-status-bars-image7.png)

    Im falschen Beispiel schlägt das rote Symbol versehentlich einen Fehler vor, was zu Verwechslungen führt.

-   Verwenden Sie Symbol Variationen oder Überlagerungen, um Status-oder Statusänderungen anzugeben. Verwenden Sie Symbol Variationen, um Änderungen in Mengen oder stärken anzuzeigen. Verwenden Sie für andere Arten von Status diese Standard Überlagerungen: 

    |                                                                                               |                                  |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | **Überlagerung**<br/>                                                                        | **Status**<br/>            |
    | ![Screenshot des Warn Symbols ](images/ctrl-status-bars-image8.png)<br/>                | Warnung<br/>               |
    | ![Screenshot des Fehler Symbols ](images/ctrl-status-bars-image9.png)<br/>                  | Fehler<br/>                 |
    | ![Screenshot des Symbols "deaktiviert/getrennt" ](images/ctrl-status-bars-image10.png)<br/> | Deaktiviert/getrennt<br/> |
    | ![Screenshot des Symbols "blockiert/offline" ](images/ctrl-status-bars-image11.png)<br/>       | Blockiert/offline<br/>       |

    

     

-   Ändern Sie den Status nicht zu häufig. Symbole der Status Leiste sollten nicht laut, instabil oder nach Bedarf angezeigt werden. Das Auge ist von den Änderungen im Peripherie Feld der Vision abhängig, sodass Statusänderungen gering sein müssen.
-   Bei Symbolen, die wichtige Statusinformationen bereitstellen, bevorzugen Sie direkte Bezeichnungen.
-   Nicht beschriftete Status leisten Symbole sollten Quick Infos aufweisen.

Weitere Informationen finden Sie unter [Symbole](vis-icons.md).

### <a name="interaction"></a>Interaktion

-   Machen Sie einen Status Leistenbereich interaktiv, damit Benutzer direkt auf verwandte Befehle und Optionen zugreifen können.
    -   Verwenden Sie ein Steuerelement, das wie eine [Menü](ctrl-command-buttons.md) Schaltfläche oder eine Trenn Schaltfläche aussieht und verhält. Diese Status leisten Bereiche müssen einen Dropdown Pfeil aufweisen, um anzugeben, dass Sie klickbar sind.
    -   Klicken Sie mit der linken Maustaste auf das Menü mit der linken Maustaste, und klicken Sie nicht auf die Maustaste.
    -   Unterstützen Sie kein Rechtsklick oder doppelklicken. Benutzer erwarten solche Interaktionen nicht in einer Statusleiste, sodass Sie Sie wahrscheinlich nicht versuchen.
-   Quick Infos anzeigen, wenn darauf gezeigt wird.

## <a name="text"></a>Text

-   Verwenden Sie im allgemeinen präzise Bezeichnungen. Schneiden Sie den Text aus, der entfernt werden kann.
-   Ziehen Sie Satzfragmente ohne das Beenden der Interpunktions Zeichen vor. Verwenden Sie vollständige Sätze (mit endinterpunktions Zeichen) nur, wenn Satzfragmente nicht wesentlich kürzer sind.
-   Geben Sie bei optionalen Status Bezeichnungen an, was der Vorgang mit einer Bezeichnung bewirkt, die mit einem Verb beginnt (Gerund-Formular) und mit einem Auslassungs Zeichen endet. Beispiel: "kopieren...". Diese Bezeichnung kann sich dynamisch ändern, wenn der Vorgang mehrere Schritte umfasst oder mehrere Objekte verarbeitet.
-   Verwenden Sie Farbe, Fett oder kursiv, um den Text der Statusleiste hervorzuheben.
-   Hinweise zur QuickInfo-Formulierung finden Sie unter Quick [Infos und infotips](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Dokumentation

Weitere Informationen finden Sie unter Status leisten, nicht Status Zeilen oder andere Variationen. Beispiel: "die aktuelle Seitenzahl wird auf der Statusleiste angezeigt."

 

