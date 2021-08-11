---
title: Fenster "Sprachbefehle"
description: Fenster "Sprachbefehle"
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f4e5ce02ea9a964663efacbc19a3b302d6e58f0364d705491be26229b15f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245103"
---
# <a name="voice-commands-window"></a>Fenster "Sprachbefehle"

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Im Fenster Sprachbefehle werden die aktuellen aktiven Sprachbefehle angezeigt, die für das Zeichen verfügbar sind. Das Fenster wird angezeigt, wenn der Befehl "Befehlsfenster öffnen" ausgewählt oder die [**Visible-Eigenschaft**](visible-property.md) des [**CommandsWindow-Objekts**](/windows/desktop/lwef/the-commandswindow-object) auf **True** festgelegt ist. Wenn die Sprach-Engine noch nicht geladen wurde, führt das Abfragen oder Festlegen dieser Eigenschaft dazu, dass der Microsoft-Agent versucht, die Engine zu initialisieren. Wenn der Benutzer sprache deaktiviert, kann das Fenster weiterhin angezeigt werden. Sie enthält jedoch eine Textnachricht, die den Benutzer darüber informiert, dass sprache derzeit deaktiviert ist.

Die Befehle des eingabeaktiven Clients werden im Fenster Sprachbefehle basierend auf den Eigenschafteneinstellungen [**Voice**](voice-property.md)[**Caption**](caption-property.md) und **Voice** angezeigt, die unter [**voiceCaption**](voicecaption-property.md) ihrer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) aufgeführt sind.

**Abbildung 1: Fenster "Sprachbefehle"**

Das Fenster "Sprachbefehle" wird angezeigt, wenn der Befehl Befehl "Befehlsfenster öffnen" ausgewählt wird. Die Befehle des eingabeaktiven Clients werden im Fenster "Sprachbefehle" angezeigt, basierend auf den Eigenschafteneinstellungen [**"Voice**](voice-property.md)[**Caption"**](caption-property.md) und **"Voice",** die unter **Stimme** der [**Sammlung Befehle**](/windows/desktop/lwef/the-commands-collection-object) aufgeführt sind.

Das Fenster "Sprachbefehle" listet auch die [**VoiceCaption**](voicecaption-property.md) der [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) für andere Clients des Zeichens und die folgenden servergenerierten Sprachbefehle für die allgemeine Interaktion unter dem Eintrag Globale Befehle auf:



| Sprachbeschriftung                       | Sprachgrammatik                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Öffnen \| des Fensters "Sprachbefehle schließen" | (show \| öffnen) \[ Das \] \[ Befehlsfenster, was kann ich \] \| jetzt sagen? \[\] <br/> umschaltet mit: <br/> Schließen \[ des \] \[ Befehlsfensters\] <br/> |
| Ausblenden                                | Ausblenden \*                                                                                                                                                  |
| *CharacterName*                     | *CharacterName*\*\*                                                                                                                                      |
| Globale Befehle                     | \[\] \[ Show me global \] commands (Globale Befehle anzeigen)                                                                                                                          |



 

\* Ein Zeichen wird hier nur aufgeführt, wenn es derzeit sichtbar ist.

\*\* Alle geladenen Zeichen werden aufgelistet.

Wenn Sie den Sprachbefehl für die [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) eines anderen Clients sprechen, wechselt er zu diesem Client, und im Fenster "Sprachbefehle" werden die Befehle dieses Clients angezeigt. Es werden keine anderen Einträge erweitert. Wenn der Benutzer zeichenwechselt, ändert sich auch das Fenster für Sprachbefehle, um die Befehle seines eingabeaktiven Clients anzuzeigen. Wenn der Client bereits eingabeaktiv ist, hat das Sprechen eines seiner Sprachbefehle keine Auswirkungen. (Wenn der Benutzer jedoch die Unterstruktur des aktiven Clients mit der Maus reduziert, wird die Unterstruktur des Clients beim Sprechen des Clientnamens erneut angezeigt.)

Wenn ein Client Sprachbefehle, aber keine [**Spracheinstellung**](voice-property.md) für sein [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) (oder keine [**Sprachbeschriftung)**](caption-property.md)hat, zeigt die Struktur "(command undefined)" als übergeordneten Eintrag an – jedoch nur, wenn dieser Client eingabeaktiv ist und der Client Befehle in seiner Sammlung mit **Beschriftungs-** und **Spracheinstellungen** enthält. 

Der Server zeigt automatisch die Befehle des aktuellen eingabeaktiven Clients an und führt bei Bedarf einen Bildlauf im Fenster durch, um so viele Befehle des Clients wie möglich basierend auf der Größe des Fensters anzuzeigen. Wenn das Zeichen keine Clienteinträge enthält, wird der Eintrag Globale Befehle erweitert.

Wenn der Benutzer "Globale Befehle" spricht, zeigt das Fenster "Sprachbefehle" immer die zugehörigen Unterstruktureinträge an. Wenn sie bereits angezeigt werden, hat der Befehl keine Auswirkungen.

Obwohl Sie das Fenster für Sprachbefehle auch mithilfe der [**Visible-Eigenschaft**](visible-property.md) im Code Ihrer Anwendung anzeigen oder ausblenden können, können Sie die Größe oder position des Fensters für Sprachbefehle nicht ändern. Der Server verwaltet die Eigenschaften des Sprachbefehlsfensters basierend auf der Interaktion des Benutzers mit dem Fenster. Die ursprüngliche Position befindet sich direkt neben dem Taskleistensymbol des Zeichens.

Das Fenster "Sprachbefehle" ist in der Fensterreihenfolge ALT+TAB enthalten. Dadurch kann ein Benutzer zum Fenster wechseln, um das Fenster mit der Tastatur zu scrollen, seine Größe zu ändern oder die Position zu ändern.

-   [Lauschendes Trinkgeld](the-listening-tip.md)
-   [Fenster "Erweiterte Zeichenoptionen"](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

