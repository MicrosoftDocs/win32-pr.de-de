---
title: Sprachbefehle (Fenster)
description: Sprachbefehle (Fenster)
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4ad0a1521e8dacc941ba5b2ce5f6c264c65a31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340901"
---
# <a name="voice-commands-window"></a>Sprachbefehle (Fenster)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Das Fenster "Sprachbefehle" zeigt die aktuellen aktiven Sprachbefehle an, die für das Zeichen verfügbar sind. Das Fenster wird angezeigt, wenn der Befehl Befehle öffnen und die Eigenschaft [**sichtbar**](visible-property.md) des Objekts [**commandswindow**](/windows/desktop/lwef/the-commandswindow-object) auf **true** festgelegt ist. Wenn die Sprach-Engine noch nicht geladen wurde, versucht die Abfrage oder das Festlegen dieser Eigenschaft, den Microsoft-Agent zu initialisieren. Wenn der Benutzer die Sprache deaktiviert, kann das Fenster weiterhin angezeigt werden. Es enthält jedoch eine Text Meldung, die den Benutzer darüber informiert, dass die Sprache aktuell deaktiviert ist.

Die Befehle der Eingabe des aktiven Clients werden auf der Grundlage der [**sprach**](voice-property.md)[**Beschriftung**](caption-property.md) und der **sprach** Eigenschafts Einstellungen, die unter der [**voicecaption**](voicecaption-property.md) der [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung aufgeführt sind, im Fenster Sprachbefehle angezeigt.

**Abbildung 1. Sprachbefehle (Fenster)**

Das Fenster "Sprachbefehle" wird angezeigt, wenn der Befehl "Befehle Öffnen" ausgewählt wird. Die Befehle der Eingabe des aktiven Clients werden auf der Grundlage der [**sprach**](voice-property.md)[**Beschriftung**](caption-property.md) und der **sprach** Eigenschafts Einstellungen, die unter **Stimme** der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung aufgelistet sind, im Fenster Sprachbefehle angezeigt.

Das Fenster Sprachbefehle listet außerdem die [**voicecaption**](voicecaption-property.md) der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung für andere Clients des Zeichens auf und die folgenden vom Server generierten Sprachbefehle für allgemeine Interaktionen unter dem Eintrag globale Befehle:



| Sprach Beschriftung                       | Sprachgrammatik                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \|Fenster "Schließen von Sprachbefehlen öffnen" | (Öffnen Sie \| anzeigen) \[ das Fenster "Befehle", \] \[ \] \| was ich jetzt sagen kann \[ .\] <br/> schaltet mit: <br/> \[Fenster " \] Befehle" schließen \[\] <br/> |
| Ausblenden                                | barg \*                                                                                                                                                  |
| *Zeichenname*                     | *Zeichenname*\*\*                                                                                                                                      |
| Globale Befehle                     | \[\] \[ \] globale Befehle anzeigen                                                                                                                          |



 

\* Hier wird nur ein Zeichen aufgelistet, wenn es zurzeit sichtbar ist.

\*\* Alle geladenen Zeichen werden aufgelistet.

Wenn Sie mit dem Voice-Befehl für die [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung eines anderen Clients zu diesem Client wechseln, werden im Fenster "Sprachbefehle" die Befehle dieses Clients angezeigt. Es werden keine weiteren Einträge erweitert. Wenn der Benutzer Zeichen wechselt, ändert sich auch das Fenster "Sprachbefehle", um die Befehle seines Eingabe aktiven Clients anzuzeigen. Wenn der Client bereits Eingabe aktiv ist, hat eine seiner Sprachbefehle keine Auswirkung. (Wenn der Benutzer jedoch die Unterstruktur des aktiven Clients mit der Maus reduziert, zeigt der Client Name die Unterstruktur des Clients erneut an.)

Wenn ein Client Sprachbefehle, aber keine [**sprach**](voice-property.md) Einstellung für das [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Objekt (oder keine **sprach**[**Beschriftung**](caption-property.md)) hat, wird in der Struktur "(Befehl nicht definiert)" als übergeordneter Eintrag angezeigt. Dies gilt jedoch nur, wenn der Client aktiv ist und der Client Befehle in der Auflistung mit den **Beschriftungs** -und **sprach** Einstellungen aufweist.

Der Server zeigt automatisch die Befehle des aktuellen Eingabe aktiven Clients an und führt ggf. im Fenster einen Bildlauf durch, um so viele der Client Befehle wie möglich anzuzeigen, basierend auf der Größe des Fensters. Wenn das Zeichen keine Client Einträge enthält, wird der Eintrag für globale Befehle erweitert.

Wenn der Benutzer "globale Befehle" spricht, zeigt das Fenster "Sprachbefehle" immer die zugehörigen untergeordneten Struktur Einträge an. Wenn Sie bereits angezeigt werden, hat der Befehl keine Auswirkungen.

Obwohl Sie das Fenster "Sprachbefehle" mithilfe der [**Visible**](visible-property.md) -Eigenschaft im Code der Anwendung anzeigen oder ausblenden können, können Sie die Fenstergröße oder den Speicherort des sprach Befehls nicht ändern. Der Server verwaltet die Eigenschaften des sprach Befehls Fensters basierend auf der Interaktion des Benutzers mit dem Fenster. Der ursprüngliche Speicherort befindet sich unmittelbar neben dem Task leisten Symbol des Zeichens.

Das Fenster "Sprachbefehle" ist in der Reihenfolge des Alt + Tab-Fensters enthalten. Dadurch kann ein Benutzer zum Fenster wechseln, um den Bildlauf durchführen, die Größe ändern oder das Fenster mit der Tastatur neu positionieren.

-   [Der Abhör Tipp](the-listening-tip.md)
-   [Das Fenster "erweiterte Zeichen Optionen"](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

