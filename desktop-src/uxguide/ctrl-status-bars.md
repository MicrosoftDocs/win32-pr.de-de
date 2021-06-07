---
title: Statusleisten (Entwurfsgrundlage)
description: Eine Statusleiste ist ein Bereich am unteren Rand eines primären Fensters, der Informationen zum Zustand des aktuellen Fensters (z. B. was angezeigt wird und wie), Hintergrundaufgaben (z. B. Drucken, Scannen und Formatieren) oder andere Kontextinformationen (z. B. Auswahl und Tastaturzustand) anzeigt.
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 3458b301c10cb4b9d6ca3a26a71b59e1011ec5a9
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524484"
---
# <a name="status-bars-design-basics"></a>Statusleisten (Entwurfsgrundlage)

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine Statusleiste ist ein Bereich am unteren Rand eines primären Fensters, der Informationen zum Zustand des aktuellen Fensters (z. B. was angezeigt wird und wie), Hintergrundaufgaben (z. B. Drucken, Scannen und Formatieren) oder andere Kontextinformationen (z. B. Auswahl und Tastaturzustand) anzeigt.

Statusleisten zeigen den Status in der Regel über Text und Symbole an, können aber auch Statusindikatoren sowie Menüs für Befehle und Optionen im Zusammenhang mit dem Status enthalten.

![Screenshot der typischen Statusleiste ](images/ctrl-status-bars-image1.png)

Eine typische Statusleiste.

> [!Note]  
> Richtlinien im Zusammenhang mit dem [Benachrichtigungsbereich](winenv-notification.md) werden in einem separaten Artikel vorgestellt.

 

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Ist der Status relevant, wenn Benutzer aktiv andere Programme verwenden?** Wenn ja, verwenden Sie ein Symbol für den [Benachrichtigungsbereich](winenv-notification.md).
-   **Muss das Statuselement Benachrichtigungen anzeigen?** In diesem Falle müssen Sie ein Symbol für den Benachrichtigungsbereich verwenden.
-   **Ist das Fenster ein primäres Fenster?** Falls nicht, verwenden Sie keine Statusleiste. Dialogfelder, Assistenten, Steuerelementpanels und Eigenschaftenblätter sollten keine Statusleisten aufweisen.
-   **Sind die Informationen in erster Linie status?** Falls nicht, verwenden Sie keine Statusleiste. Statusleisten dürfen nicht als sekundäre [Menüleiste](cmd-menus.md) oder [Symbolleiste](cmd-toolbars.md)verwendet werden.
-   **Wird in den Informationen erläutert, wie das ausgewählte Steuerelement verwendet wird?** Wenn ja, zeigen Sie die Informationen neben dem zugeordneten Steuerelement stattdessen mit einer ergänzenden Erklärung oder Anweisungsbezeichnung an.
-   **Ist der Status nützlich und relevant? Das heißt, sind Benutzer aufgrund dieser Informationen wahrscheinlich in der Lage, ihr Verhalten zu ändern?** Wenn nicht, zeigen Sie entweder den Status nicht an, oder speichern Sie ihn in einer Protokolldatei.
-   **Ist der Status kritisch? Ist sofortige Aktion erforderlich?** Wenn ja, zeigen Sie die Informationen in einem Formular an, das Aufmerksamkeit erfordert und nicht einfach ignoriert werden kann, z. B. ein [Dialogfeld](win-dialog-box.md) oder innerhalb des primären Fensters selbst.

    ![Screenshot der roten Statusleiste "Zertifikatfehler" ](images/ctrl-status-bars-image2.png)

    Eine rote Adressleiste in Windows Internet Explorer.

-   **Ist das Programm in erster Linie für erfahrene Benutzer vorgesehen?** Unerfahrene Benutzer sind in der Regel nicht über Statusleisten informiert, weshalb Sie die Verwendung von Statusleisten in diesem Fall erwägen.

## <a name="design-concepts"></a>Entwurfskonzepte

Statusleisten sind eine hervorragende Möglichkeit, Statusinformationen bereitzustellen, ohne Benutzer zu unterbrechen oder ihren Flow zu unterbrechen. Statusleisten sind jedoch leicht zu übersehen. So einfach, dass viele Benutzer überhaupt keine Statusleisten bemerken.

Die Lösung für dieses Problem besteht nicht darin, die Aufmerksamkeit des Benutzers mithilfe von grellen Symbolen, Animationen oder Flashing aufzufordern, sondern um diese Einschränkung zu entwerfen. Gehen Sie dafür so vor:

-   **Stellen Sie sicher, dass die Statusinformationen nützlich und relevant sind.** Falls nicht, geben Sie keine Statusleiste an.
-   **Keine Verwendung von Statusleisten für wichtige Informationen.** Benutzer sollten nie wissen müssen, was sich in der Statusleiste befindet. Wenn Benutzer sie sehen müssen, legen Sie sie nicht in eine Statusleiste ein.

**Wenn Sie nur eine Sache tun...**

Stellen Sie sicher, dass die Statusleisteninformationen nützlich und relevant, aber nicht entscheidend sind.

## <a name="usage-patterns"></a>Verwendungsmuster

Statusleisten weisen mehrere Verwendungsmuster auf:



|   Verwendung                                                                                                                                 |    Beispiel                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Status des aktuellen Fensters**<br/> Anzeigen der Quelle, was angezeigt wird, zusammen mit allen Ansichtsmodi <br/>              | ![Screenshot einer Statusleiste "Location" ](images/ctrl-status-bars-image3.png)<br/> In diesem Beispiel zeigt die Statusleiste den Pfad zum Dokument an.<br/>                                                         |
| **Progress**<br/> Zeigen Sie den Fortschritt von Hintergrundaufgaben an, entweder mit einer bestimmende Statusanzeige oder einer Animation. <br/> | ![Screenshot der Statusleiste mit Statusanzeige ](images/ctrl-status-bars-image4.png)<br/> In diesem Beispiel enthält die Statusleiste eine Statusanzeige, um das Laden der Webseite in ein Internet Explorer Fenster anzuzeigen.<br/> |
| **Kontextinformationen**<br/> Zeigen Sie kontextbezogene Informationen dazu an, was der Benutzer gerade tut. <br/>              | ![Screenshot der Statusleiste mit der Anzahl von Pixeln ](images/ctrl-status-bars-image5.png)<br/> In diesem Beispiel zeigt Microsoft Paint die Auswahlgröße in Pixel an.<br/>                                           |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   Erwägen Sie die Bereitstellung eines Befehls Statusleiste anzeigen, wenn nur einige Benutzer die Statusleisteninformationen benötigen. Blenden Sie die Statusleiste standardmäßig aus, wenn sie von den meisten Benutzern nicht benötigt wird.
-   Verwenden Sie nicht die Statusleiste, um Menüleistenelemente zu erläutern. Dieses Hilfemuster ist nicht erkennbar.

### <a name="presentation"></a>Präsentation

-   Deaktivieren Sie den modalen Status, der nicht angewendet wird. Der modale Status umfasst Tastatur- und Dokumentzustände.
-   Entfernen Sie den nicht modalen Status, der nicht zutrifft.
-   Zeigen Sie Statusinformationen in der folgenden Reihenfolge an: aktueller Fensterstatus; progress; und kontextbezogene Informationen.

### <a name="icons"></a>Symbole

-   Wählen Sie leicht erkennbare Statussymbolentwürfe aus. Symbole mit eindeutigen Konturen gegenüber quadratischen oder rechteckigen Symbolen bevorzugen.
-   Verwenden Sie nur Swathen von rein rot, gelb und grün, um Statusinformationen zu kommunizieren. Andernfalls sind solche Symbole verwirrend.

    **Richtig:**

    ![Screenshot der Statusleiste mit blauen Symbolen ](images/ctrl-status-bars-image6.png)

    **Falsch:**

    ![Screenshot der Statusleiste mit einem roten Symbol ](images/ctrl-status-bars-image7.png)

    Im falschen Beispiel deutet das rote Symbol unbeabsichtigt auf einen Fehler hin, wodurch Verwirrung entsteht.

-   Verwenden Sie Symbolvariationen oder Überlagerungen, um Status- oder Statusänderungen anzuzeigen. Verwenden Sie Symbolvariationen, um Änderungen in Mengen oder Stärken anzuzeigen. Verwenden Sie für andere Statustypen die folgenden Standardüberlagerungen: 

    | Überlagerung                 | Status            |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | ![Screenshot des Warnsymbols ](images/ctrl-status-bars-image8.png)<br/>                | Warnung<br/>               |
    | ![Screenshot des Fehlersymbols ](images/ctrl-status-bars-image9.png)<br/>                  | Fehler<br/>                 |
    | ![Screenshot des Symbols "Deaktiviert/Getrennt" ](images/ctrl-status-bars-image10.png)<br/> | Deaktiviert/Getrennt<br/> |
    | ![Screenshot des Symbols "Blockiert/Offline" ](images/ctrl-status-bars-image11.png)<br/>       | Blockiert/Offline<br/>       |

    

     

-   Ändern Sie den Status nicht zu häufig. Statusleistensymbole sollten nicht laut, instabil oder aufmerksamkeitsfähig angezeigt werden. Das Auge reagiert empfindlich auf Änderungen im Peripheriebereich des Sehens, sodass Statusänderungen geringfügig sein müssen.
-   Für Symbole, die wichtige Statusinformationen bereitstellen, bevorzugen Sie ortsbezogene Bezeichnungen.
-   Nicht bezeichnete Statusleistensymbole sollten QuickInfos enthalten.

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

 

