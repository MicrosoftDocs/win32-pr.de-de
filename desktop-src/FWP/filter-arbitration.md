---
title: Filtern der Vermittlung
description: Filterausschlüsse sind die Logik, die in die Windows Filtering Platform (WFP) integriert ist, die verwendet wird, um zu bestimmen, wie Filter miteinander interagieren, wenn Entscheidungen zur Filterung des Netzwerkdatenverkehrs getroffen werden.
ms.assetid: d097f307-113e-4dc3-ad59-ddfb85061583
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7640e94440cf040d9ca51b6c639dc66e3e8a767024d6dbcd01b9c0cd2b87a24b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151188"
---
# <a name="filter-arbitration"></a>Filtern der Vermittlung

Filterausschlüsse sind die Logik, die in die Windows Filtering Platform (WFP) integriert ist, die verwendet wird, um zu bestimmen, wie Filter miteinander interagieren, wenn Entscheidungen zur Filterung des Netzwerkdatenverkehrs getroffen werden.

## <a name="filter-arbitration-behaviors"></a>Filtern von Vermittlungsverhalten

Die folgenden Verhaltensweisen charakterisieren das Filterschlichtungssystem:

-   Der ganze Datenverkehr kann überprüft werden. Kein Datenverkehr kann Filter auf einer bestimmten Ebene umgehen.
-   Datenverkehr kann auch dann durch einen Aufruffilter über **eine -Sperre** blockiert werden, wenn ein Filter mit höherer Priorität dies zugelassen hat.
-   Mehrere Anbieter können den Datenverkehr auf derselben Ebene überprüfen. Beispielsweise können Firewallfilter gefolgt von Angriffserkennungssystemfiltern (IDS) oder IPsec gefolgt von Quality of Service-Filtern (QoS) den Datenverkehr auf derselben Ebene untersuchen.

## <a name="filtering-model"></a>Filtermodell

Jede Filterebene wird in Unterebenen unterteilt, die nach Priorität (auch Gewichtung genannt) geordnet sind. Der Netzwerkdatenverkehr durchläuft Unterebenen von der höchsten bis zur niedrigsten Priorität. Unterebenen werden von den Entwicklern mithilfe der WFP-API erstellt und verwaltet.

Innerhalb jeder Unterebene werden Filter nach Gewichtung geordnet. Der Netzwerkdatenverkehr wird für übereinstimmende Filter von der höchsten gewichteten zur niedrigsten Gewichtung angezeigt.

Der Filterausschlussalgorithmus wird auf alle Unterebenen innerhalb einer Ebene angewendet, und die endgültige Filterungsentscheidung wird getroffen, nachdem alle Unterebenen ausgewertet wurden. Dies bietet mehrere Abgleichsfunktionen.

Innerhalb einer Unterschicht wird die Filterschlichtung wie folgt durchgeführt:

-   Berechnen Sie die Liste der übereinstimmenden Filter, die nach Gewichtung von der höchsten zur niedrigsten geordnet sind.
-   Werten Sie übereinstimmende Filter so lange aus, bis "Zulassen" oder "Blockieren" zurückgegeben wird (Filter können auch "Continue" zurückgeben) oder bis die Liste erschöpft ist.
-   Überspringen Sie die verbleibenden Filter, und geben Sie die Aktion aus dem zuletzt ausgewerteten Filter zurück.

Innerhalb einer Ebene wird die Filterschlichtung wie folgt durchgeführt:

-   Führen Sie filterbasierte Vermittlungen auf jeder Unterebene durch, um von der höchsten priorität zur niedrigsten Priorität zu kommen.
-   Werten Sie alle Unterebenen aus, auch wenn eine untere Ebene mit höherer Priorität entschieden hat, den Datenverkehr zu blockieren.
-   Gibt die resultierende Aktion basierend auf den im folgenden Abschnitt beschriebenen Richtlinienregeln zurück.

Das folgende Diagramm veranschaulicht eine Beispielkonfiguration auf unterer Ebene. Die äußeren Felder stellen Ebenen dar. Die inneren Felder stellen Unterebenen dar, die Filter enthalten. Der Platzhalter ( \* ) in einem Filter bedeutet, dass der ganze Datenverkehr dem Filter entspricht.

![Beispielkonfiguration auf unterer Ebene](images/fwp-sub-config2.png)

Die einzige Möglichkeit, einen Filter zu umgehen, ist, wenn ein Filter mit höherer Gewichtung den Datenverkehr innerhalb derselben Unterebene zugelassen oder blockiert hat. Umgekehrt besteht eine Möglichkeit, sicherzustellen, dass ein Filter immer den ganzen Datenverkehr innerhalb einer Ebene erkennt, darin, eine Unterebene hinzuzufügen, die einen einzelnen Filter enthält, der dem ganzen Datenverkehr entspricht.

## <a name="configurable-override-policy"></a>Konfigurierbare Außerkraftsetzungsrichtlinie

Die unten beschriebenen Regeln regeln die Vermittlungsentscheidungen innerhalb einer Ebene. Diese Regeln werden von der Filter-Engine verwendet, um zu entscheiden, welche der Aktionen der unteren Ebene auf den Netzwerkdatenverkehr angewendet wird.

Die grundlegende Richtlinie lautet wie folgt.

-   Aktionen werden in der Prioritäts reihenfolge der Unterebenen von der höchsten bis zur niedrigsten Priorität ausgewertet.
-   "Blockieren" überschreibt "Zulassen".
-   "Blockieren" ist endgültig (kann nicht überschrieben werden) und beendet die Auswertung. Das Paket wird verworfen.

Die grundlegende Richtlinie unterstützt nicht das Szenario einer Ausnahme, die nicht von einer Firewall überschrieben wird. Typische Beispiele für diese Art von Szenario sind:

-   Der Remoteverwaltungsport muss auch bei Vorhandensein einer Firewall eines Drittanbieters geöffnet werden.
-   Komponenten, für die Ports geöffnet werden müssen, damit sie funktionieren (z. B. universelle Plug & Play UPnP). Wenn der Administrator die Komponente explizit aktiviert hat, sollte die Firewall den Datenverkehr nicht automatisch blockieren.

Um die oben genannten Szenarien zu unterstützen, muss die Außerkraftsetzung einer Filterentscheidung schwieriger als eine andere Filterentscheidung sein, indem die Berechtigung zum Außerkraftsetzen der Aktion verwalten wird. Diese Berechtigung wird als **FWPS \_ RIGHT ACTION \_ \_ WRITE-Flag** implementiert und auf Filterbasis festgelegt.

Der Auswertungsalgorithmus verwaltet die aktuelle Aktion ("Zulassen" oder "Blockieren") zusammen mit dem **FWPS \_ RIGHT \_ ACTION \_ WRITE-Flag.** Das Flag steuert, ob eine untergeordnete Ebene mit niedrigerer Priorität die Aktion überschreiben darf. Durch Festlegen oder Zurücksetzen des **FWPS \_ RIGHT \_ ACTION \_ WRITE-Flags** in der [FWPS \_ CLASSIFY \_ OUT0-Struktur](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) steuert ein Anbieter, wie Aktionen überschrieben werden können oder nicht. Wenn das Flag festgelegt ist, bedeutet dies, dass die Aktion überschrieben werden kann. Wenn das Flag nicht vorhanden ist, kann die Aktion nicht überschrieben werden.



| Aktion | Außerkraftsetzung zulassen (FWPS \_ RIGHT ACTION WRITE ist \_ \_ festgelegt) | Beschreibung                                                                                                          |
|--------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Zulassen | Ja                                                | Der Datenverkehr kann auf einer anderen Unterebene blockiert werden. Dies wird als "Soft Permit" bezeichnet.<br/>                            |
| Zulassen | Nein                                                 | Der Datenverkehr kann nur auf einer anderen Unterebene durch eine **Callout-Sperre blockiert werden.** Dies wird als "Hard Permit" bezeichnet.<br/> |
| Blockieren  | Ja                                                | Der Datenverkehr kann auf einer anderen Unterebene zugelassen werden. Dies wird als soft-Block bezeichnet.<br/>                           |
| Blockieren  | Nein                                                 | Der Datenverkehr kann nicht auf einer anderen Unterebene zugelassen werden. Dies wird als harter Block bezeichnet.<br/>                        |



 

Die Filteraktion kann festgelegt  werden, indem der Typ member in der Struktur [**FWPM \_ ACTION0 entweder**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0) auf **FWP \_ ACTION \_ BLOCK** oder **FWP ACTION PERMIT festgelegt \_ \_ wird.** Neben dem Aktionstyp macht ein Filter auch das **Flag FWPM \_ FILTER FLAG CLEAR ACTION RIGHT \_ \_ \_ \_ verfügbar.** Wenn dieses Flag aufgehoben wird, ist der Aktionstyp hart und kann nicht außer Kraft gesetzt werden, es sei denn, eine harte Genehmigung wird wie später erläutert von **einem Gegenüber** außer Kraft gesetzt, ander denn er ist weich, der durch eine Aktion mit hoher Priorität überschrieben werden kann.

In der folgenden Tabelle wird das Standardverhalten für Filter- und Calloutaktionen aufgeführt.

| Aktion         | Standardverhalten |
|----------------|------------------|
| Filtergenehmigung  | Soft Permit      |
| Callout-Zulassung | Soft Permit      |
| Filterblock   | Harter Block       |
| Calloutblock  | Softblock       |



 

Eine  "Block"-Aktion, die vom Filter zurückgegeben wird, als das **FWPS \_ RIGHT ACTION \_ \_ WRITE-Flag** vor dem Aufrufen des Filters zurückgesetzt wurde. Ein **-Block** blockiert Datenverkehr, der mit einer hard-Zulassung zugelassen wurde.

Wenn ein **-Zeichen** ausgegeben wird, ist dies ein Hinweis auf einen Konflikt in der Konfiguration. Die folgenden Aktionen werden zur Entschärfung des Konflikts durchgeführt.

-   Der Datenverkehr wird blockiert.
-   Ein Überwachungsereignis wird generiert.
-   Eine Benachrichtigung wird generiert.
    > [!Note]  
    > Die Benachrichtigung wird von allen Entitäten empfangen, die sie abonniert haben. Dies umfasst in der Regel die Firewall (um Fehlkonfigurationen zu erkennen) oder Anwendungen (um zu ermitteln, ob ihr bestimmter Filter überschrieben wird).

     

    > [!Note]  
    > Es ist keine obligatorische Benutzeroberfläche (UI) instanziiert, wenn ein Filter "Hard Permit" überschrieben wird. Die Benachrichtigungen über die Außerkraftsetzung werden an jeden Anbieter gesendet, der sich für den Empfang registriert hat. Dadurch können Firewalls oder die Anwendungen, die die Filter "Zulassen" erstellt haben, die Benutzeroberfläche anzeigen, die nach Benutzeraktion fragt. Es hat keinen Nutzen, eine Plattformbenutzeroberflächenbenachrichtigung für diese Überschreibungsereignisse zu verwenden, da Firewall-ISVs, die nicht automatisch blockieren möchten, dies tun können, indem sie sich an einem anderen Ort im WFP registrieren oder (weniger bevorzugt) ihre ganze Logik in einem Rückruftreiber verarbeiten. ISVs, die denken, dass die Eingabeaufforderung von Benutzern eine gute Idee ist, sollten die Benutzererfahrung besitzen und ihre eigene Benutzeroberfläche erstellen.

     

Das oben beschriebene Entschärfungsverhalten stellt sicher, dass ein Filter "Hard Permit" nicht automatisch durch einen Blockfilter überschrieben wird, und deckt das Szenario ab, in dem ein Remoteverwaltungsport von der Firewall nicht blockiert werden darf. Um "Hard Permit"-Filter automatisch außer Kraft zu setzen, muss eine Firewall ihre Filter innerhalb einer unteren Ebene mit höherer Priorität hinzufügen.

> [!Note]  
> Da es keine ebenenübergreifende Vermittlung gibt, kann der mit "Hard Permit" zugelassene Datenverkehr weiterhin auf einer anderen Ebene blockiert werden. Es liegt in der Verantwortung des Richtlinienautors, sicherzustellen, dass Datenverkehr bei Bedarf auf jeder Ebene zugelassen wird.

 

Benutzeranwendungen, die Ports zum Öffnen anfordern, fügen überschreibbare Filter zu einer unteren Ebene mit niedriger Priorität hinzu. Die Firewall kann den Filter zum Hinzufügen von Benachrichtigungsereignissen abonnieren und nach der Überprüfung durch den Benutzer (oder die Richtlinie) einen übereinstimmenden Filter hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filtergewichtungszuweisung](filter-weight-assignment.md)
</dt> </dl>

 

