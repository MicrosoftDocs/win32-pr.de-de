---
title: Filterung Filtern
description: Die Filter-Schiedsgerichtsbarkeit ist die in die Windows-Filter Plattform (WFP) integrierte Logik, mit der bestimmt wird, wie Filter miteinander interagieren, wenn Entscheidungen zum Filtern von Netzwerk Datenverkehr getroffen werden.
ms.assetid: d097f307-113e-4dc3-ad59-ddfb85061583
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd7df778d1c24b7480de3321e7a1ec126d8e642
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727008"
---
# <a name="filter-arbitration"></a>Filterung Filtern

Die Filter-Schiedsgerichtsbarkeit ist die in die Windows-Filter Plattform (WFP) integrierte Logik, mit der bestimmt wird, wie Filter miteinander interagieren, wenn Entscheidungen zum Filtern von Netzwerk Datenverkehr getroffen werden.

## <a name="filter-arbitration-behaviors"></a>Filtern von Schiedsgerichts Verhalten

Die folgenden Verhaltensweisen bezeichnen das Filter-schiedsrichtersystem:

-   Der gesamte Datenverkehr kann überprüft werden. Der Datenverkehr kann Filter auf einer bestimmten Ebene nicht umgehen.
-   Der Datenverkehr kann durch einen Legenden Filter über ein **Veto** blockiert werden, auch wenn er von einem Filter mit höherer Priorität zugelassen wurde.
-   Mehrere Anbieter können den Datenverkehr auf derselben Ebene überprüfen. Beispielsweise kann der Datenverkehr auf derselben Ebene von der Firewall, gefolgt von den Filtern von Angriffs Erkennungssystemen (ID) oder IPSec gefolgt von Quality of Service (QoS), überprüft werden.

## <a name="filtering-model"></a>Filter Modell

Jede Filter Ebene ist in untergeordnete Ebenen unterteilt nach Priorität (auch als Gewichtung bezeichnet). Der Netzwerk Datenverkehr durchläuft untergeordnete Schichten von der höchsten Priorität bis zur niedrigsten Priorität. Untergeordnete Ebenen werden von Entwicklern erstellt und verwaltet, die die WFP-API verwenden.

In jeder Unterebene werden Filter nach Gewichtung geordnet. Der Netzwerk Datenverkehr wird für den Abgleich von Filtern von der höchsten Gewichtung zum niedrigsten Gewicht angegeben.

Der Algorithmus für die Filter Schiedsgerichtsbarkeit wird auf alle Unterebenen innerhalb einer Ebene angewendet, und die endgültige Filter Entscheidung wird vorgenommen, nachdem alle Unterebenen ausgewertet wurden. Dies bietet mehrere abgleichsfunktionen.

In einer untergeordneten Ebene wird die Filterung von Filtern wie folgt durchgeführt:

-   Berechnen Sie die Liste der übereinstimmenden Filter nach Gewichtung von der höchsten zur niedrigsten.
-   Vergleichen Sie die übereinstimmenden Filter so lange, bis ein "zulassen" oder ein "Block" zurückgegeben wird (Filter können auch "Continue" zurückgeben) oder bis die Liste erschöpft ist.
-   Überspringen Sie die restlichen Filter, und geben Sie die Aktion vom zuletzt ausgewerteten Filter zurück.

Innerhalb einer Ebene wird die Filterung von Filtern wie folgt durchgeführt:

-   Führen Sie eine Filter-Schiedsgerichtsbarkeit auf jeder Unterebene aus, von der höchsten Priorität bis zur niedrigsten Priorität.
-   Wertet alle Unterebenen aus, auch wenn sich die Unterebene mit höherer Priorität für die Blockierung des Datenverkehrs entschieden hat.
-   Gibt die resultierende Aktion auf der Grundlage der im folgenden Abschnitt beschriebenen Richtlinien Regeln zurück.

Das folgende Diagramm zeigt eine Beispielkonfiguration der untergeordneten Ebene. Die äußeren Felder stellen Ebenen dar. Die inneren Felder stellen Unterebenen dar, die Filter enthalten. Der Platzhalter ( \* ) in einem Filter bedeutet, dass der gesamte Datenverkehr dem Filter entspricht.

![Beispielkonfiguration der untergeordneten Ebene](images/fwp-sub-config2.png)

Ein Filter kann nur umgangen werden, wenn ein Filter mit höherer Gewichtung den Datenverkehr innerhalb derselben Unterschicht zugelassen oder blockiert hat. Eine Möglichkeit, um sicherzustellen, dass ein Filter immer den gesamten Datenverkehr innerhalb einer Ebene sieht, besteht darin, eine Unterebene hinzuzufügen, die einen einzelnen Filter enthält, der mit dem gesamten Datenverkehr übereinstimmt.

## <a name="configurable-override-policy"></a>Konfigurierbare Überschreibungs Richtlinie

Die nachstehend beschriebenen Regeln steuern die Entscheidungen hinsichtlich der Schiedsgerichtsbarkeit innerhalb einer Ebene. Diese Regeln werden von der Filter-Engine verwendet, um zu entscheiden, welche der untergeordneten Ebenen Aktionen auf den Netzwerk Datenverkehr angewendet werden.

Die grundlegende Richtlinie lautet wie folgt.

-   Aktionen werden in der Prioritäts Reihenfolge der untergeordneten Ebenen ausgewertet, von der höchsten Priorität bis zur niedrigsten Priorität.
-   "Block" überschreibt "zulassen".
-   "Block" ist endgültig (kann nicht überschrieben werden) und beendet die Auswertung. Das Paket wird verworfen.

Die grundlegende Richtlinie unterstützt nicht das Szenario einer Ausnahme, die von einer Firewall nicht überschrieben wird. Typische Beispiele für diese Art von Szenario:

-   Der Remote Verwaltungs Port muss geöffnet werden, auch wenn eine Drittanbieter Firewall vorhanden ist.
-   Komponenten, für die das Öffnen von Ports erforderlich ist, um zu funktionieren (z. b. Universal Plug & Play UPnP). Wenn der Administrator die Komponente explizit aktiviert hat, sollte der Datenverkehr von der Firewall nicht automatisch blockiert werden.

Um die obigen Szenarios zu unterstützen, muss eine Filter Entscheidung schwieriger zu überschreiben sein als eine andere Filter Entscheidung durch Verwalten der Aktion Überschreibungs Berechtigung. Diese Berechtigung wird als das Schreib Flag für die Rechte Berechtigung der **\_ \_ \_ vollschreibweise** implementiert und auf Filter Basis festgelegt.

Der Auswertungs Algorithmus verwaltet die aktuelle Aktion ("zulassen" oder "blockieren") zusammen mit dem Schreib Flag für die **richtige f- \_ \_ Aktion \_** . Das Flag steuert, ob eine untergeordnete Ebene mit niedrigerer Priorität die Aktion überschreiben darf. Durch Festlegen oder Zurücksetzen des Schreib Flags für die **\_ Rechte \_ Aktion \_ "f** " in der OUT0-Struktur von " [ \_ \_](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) " wird von einem Anbieter bestimmt, wie Aktionen überschrieben werden können. Wenn das-Flag festgelegt ist, gibt es an, dass die Aktion überschrieben werden kann. Wenn das-Flag nicht vorhanden ist, kann die Aktion nicht überschrieben werden.



| Aktion | Außer Kraft Setzung zulassen ( \_ richtig geschriebene f- \_ Aktion \_ Schreiben) | BESCHREIBUNG                                                                                                          |
|--------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Zulassen | Ja                                                | Der Datenverkehr kann in einer anderen Unterschicht blockiert werden. Dies wird als weiche Zulassung bezeichnet.<br/>                            |
| Zulassen | Nein                                                 | Der Datenverkehr kann in einer anderen Unterschicht nur durch ein Legenden **Veto** blockiert werden. Dies wird als harte Zulassung bezeichnet.<br/> |
| Blockieren  | Ja                                                | Der Datenverkehr kann in einer anderen Unterebene zugelassen werden. Dies wird als weicher Block bezeichnet.<br/>                           |
| Blockieren  | Nein                                                 | Der Datenverkehr kann in einer anderen Unterschicht nicht zugelassen werden. Dies wird als hardblock bezeichnet.<br/>                        |



 

Die Filter Aktion kann festgelegt werden, indem der **Typmember** in der Struktur [**fwpm \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0) auf den **FWP- \_ Aktions \_ Block** oder die **FWP- \_ Aktion \_ zulassen** festgelegt wird. Zusammen mit dem Aktionstyp macht ein Filter auch das Flag Flag zum **Löschen von \_ rechten \_ nach \_ \_ \_ Rechts**. Wenn dieses Flag deaktiviert ist, ist der Aktionstyp schwierig und kann außer Kraft gesetzt werden, es sei denn, eine harte Zulassungs Maßnahme wird von einem **Veto** überschrieben, wie weiter unten erläutert wird. andernfalls ist es weich und kann durch eine Aktion mit hoher Priorität überschrieben werden.

In der folgenden Tabelle wird das Standardverhalten für Filter-und Legenden Aktionen aufgelistet.

| Aktion         | Standardverhalten |
|----------------|------------------|
| Filter Zulassungsberechtigung  | Weiche Zulassung      |
| Callout zulassen | Weiche Zulassung      |
| Filter Block   | Hardblock       |
| Legenden Block  | Weicher Block       |



 

Ein **Veto** ist eine "Block"-Aktion, die vom Filter zurückgegeben wird, wenn das Schreib Flag für die **fwps- \_ Rechte \_ Aktion \_** vor dem Aufrufen des Filters zurückgesetzt wurde. Ein **Veto** blockiert den Datenverkehr, der mit einer fest Zulassungsberechtigung zugelassen wurde.

Wenn ein **Veto** ausgegeben wird, ist dies ein Hinweis auf einen Konflikt in der Konfiguration. Die folgenden Aktionen werden durchgeführt, um den Konflikt zu verringern.

-   Der Datenverkehr wird blockiert.
-   Ein Audit-Ereignis wird generiert.
-   Eine Benachrichtigung wird generiert.
    > [!Note]  
    > Die Benachrichtigung wird von allen Entitäten empfangen, die Sie abonniert haben. Dies umfasst in der Regel die Firewall (zum Erkennen von Fehlkonfigurationen) oder Anwendungen (um zu ermitteln, ob der jeweilige Filter überschrieben wird).

     

    > [!Note]  
    > Es wird keine erforderliche Benutzeroberfläche (User Interface, UI) instanziiert, wenn der Filter "Hard Zulassungs" überschrieben wird. Die Benachrichtigungen der außer Kraft Setzung werden an jeden Anbieter gesendet, der für den Empfang registriert ist, sodass Firewalls oder die Anwendungen, die die Zulassungs Filter erstellt haben, die Benutzeroberfläche anzeigen können, die Benutzeraktionen anfordert. Es gibt keinen Wert, wenn eine Plattformbenutzer Oberfläche für diese Überschreibungs Ereignisse vorhanden ist, da firewallisvs, die nicht im Hintergrund blockieren möchten, dies tun können, indem Sie sich an einer anderen Stelle in WFP registrieren oder (weniger bevorzugt) Ihre gesamte Logik in einem aufrufenden Treiber verarbeiten. ISVs, die Benutzer zur Eingabe auffordern, sind eine gute Idee, die Benutzeroberfläche zu erstellen und ihre eigene Benutzeroberfläche zu erstellen.

     

Das oben beschriebene Entschärfungs Verhalten stellt sicher, dass ein "Hard-Allowed"-Filter nicht automatisch durch einen "Block"-Filter überschrieben wird, und behandelt das Szenario, in dem ein Remote Verwaltungs Port nicht durch die Firewall blockiert werden darf. Um die "Hard-Zulassungs"-Filter automatisch zu überschreiben, muss eine Firewall ihre Filter in einer Unterebene mit höherer Priorität hinzufügen.

> [!Note]  
> Da es keine Schicht übergreifende Schiedsgerichtsbarkeit gibt, kann der mit "Hard Zulassungs" zulässige Datenverkehr auf einer anderen Ebene blockiert werden. Der Richtlinien Autor muss sicherstellen, dass der Datenverkehr bei Bedarf auf jeder Ebene zulässig ist.

 

Benutzer Anwendungen, die zu öffnende Ports anfordern, fügen über schreibbare Filter zu einer Unterebene mit niedriger Priorität hinzu. Die Firewall kann den Filter zum Hinzufügen von Benachrichtigungs Ereignissen abonnieren und nach der Benutzer Validierung (oder Richtlinie) einen übereinstimmenden Filter hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filtergewichtungszuweisung](filter-weight-assignment.md)
</dt> </dl>

 

