---
title: Zwischenspeichern von Eigenschaften der Benutzeroberflächen Automatisierung und Steuerelement Mustern
description: Bei der Verwendung von Microsoft UI Automation müssen Clients häufig mehrere Eigenschaften für mehrere Automatisierungselemente abrufen.
ms.assetid: 948b3bb9-75a9-4197-9680-e6fe7bb86feb
keywords:
- Caching, Eigenschaften der Benutzeroberflächen Automatisierung
- Caching, Eigenschaften
- Caching, Steuerelement Muster für die Benutzeroberflächen Automatisierung
- Caching, Steuerelement Muster
- Benutzeroberflächenautomatisierungs, Caching-Eigenschaften
- Benutzeroberflächen Automatisierung, Zwischenspeichern von Eigenschaften
- Clients, Eigenschaften der Benutzeroberflächen Automatisierung
- Clients, Caching-Steuerelement Muster für die Benutzeroberflächen Automatisierung
- Benutzeroberflächenautomatisierungs, cachingsteuerungmuster
- Benutzeroberflächen Automatisierung, Zwischenspeichern von Steuerelement Mustern
- Steuerelement Muster, Zwischenspeichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f75a7dc9491565fdfdc0ecc73808c2fb6a9d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388123"
---
# <a name="caching-ui-automation-properties-and-control-patterns"></a>Zwischenspeichern von Eigenschaften der Benutzeroberflächen Automatisierung und Steuerelement Mustern

Bei der Verwendung von Microsoft UI Automation müssen Clients häufig mehrere Eigenschaften für mehrere Automatisierungselemente abrufen. Ein Client kann einzelne Eigenschaften einzeln abrufen, indem er die Methoden zum Abrufen von Eigenschaften wie z. b. [**iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) oder [**currentaccesskey**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey)verwendet. Diese Methode ist jedoch langsam und ineffizient, da für jede abgerufene Eigenschaft ein Prozess übergreifender Abruf erforderlich ist. Um die Leistung zu verbessern, können Clients die Funktionen zum Zwischenspeichern (auch als Massen Abruf bezeichnet) für die Benutzeroberflächen Automatisierung verwenden. Durch das Caching kann ein Client alle gewünschten Eigenschaften für alle gewünschten Elemente mit einem einzelnen Methoden aufzurufen abrufen. Der Client kann dann die einzelnen Eigenschaften nach Bedarf aus dem Cache abrufen und eine neue Momentaufnahme des Caches regelmäßig abrufen, als Reaktion auf Ereignisse, die Änderungen in der Benutzeroberfläche bedeuten.

Die Anwendung kann beim Abrufen eines Benutzeroberflächenautomatisierungs-Elements mithilfe einer Methode, z. b. [**iuiautomation:: elementfrompointbuildcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache), [**iuiautomationtreewalker:: getfirstchildelementbuildcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache)oder [**iuiautomationelement:: findfirstbuildcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache), Caching anfordern.

Zwischenspeichern erfolgt auch, wenn Sie beim Abonnieren von Ereignissen eine Cache Anforderung angeben. Das Benutzeroberflächenautomatisierungs-Element, das als Quelle eines Ereignisses an Ihren Ereignishandler übermittelt wird, enthält die zwischengespeicherten Eigenschaften und Steuerelement Muster, die von der Cache Anforderung angegeben werden. Alle Änderungen, die an der Cache Anforderung vorgenommen werden, nachdem Sie das Ereignis abonniert haben, haben keine Auswirkungen.

Dieses Thema enthält folgende Abschnitte:

-   [Cache Anforderungen](#cache-requests)
    -   [Angeben von Eigenschaften-und Steuerelement Mustern zum Zwischenspeichern](#specifying-property-and-control-patterns-to-cache)
    -   [Festlegen des Bereichs und Filterns einer Cache Anforderung](#specifying-the-scoping-and-filtering-of-a-caching-request)
    -   [Stärke der Element Verweise](#strength-of-element-references)
-   [Abrufen von zwischengespeicherten untergeordneten und übergeordneten Elementen](#retrieving-cached-children-and-parents)
-   [Abrufen einer neuen Momentaufnahme des Caches](#retrieving-a-new-snapshot-of-the-cache)
-   [Beispiele](#examples)
-   [Zugehörige Themen](#related-topics)

## <a name="cache-requests"></a>Cache Anforderungen

Zum Zwischenspeichern müssen Sie bestimmen, welche Eigenschaften abgerufen und welche Elemente abgerufen werden sollen. Anschließend können Sie diese Informationen verwenden, um eine Cache Anforderung zu erstellen. Wenn der Client eine [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für das UI-Element erhält, speichert die Benutzeroberflächen Automatisierung die in der Cache Anforderung angegebenen Informationen zwischen.

Beginnen Sie zum Erstellen einer Cache Anforderung mit der [**iuiautomation:: | atecacherequest**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createcacherequest) -Methode, um einen [**iuiautomationcacherequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) -Schnittstellen Zeiger abzurufen. Konfigurieren Sie als nächstes die Cache Anforderung mithilfe der Methoden von **iuiautomationcacherequest**.

### <a name="specifying-property-and-control-patterns-to-cache"></a>Angeben von Eigenschaften-und Steuerelement Mustern zum Zwischenspeichern

Sie können Eigenschaften für den Cache angeben, indem Sie [**iuiautomationcacherequest:: AddProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addproperty)aufrufen. Sie können durch den Aufruf von [**iuiautomationcacherequest:: addpattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addpattern)zwischengespeicherten Steuerelement Mustern angeben. Wenn ein Steuerelement Muster zwischengespeichert wird, werden dessen Eigenschaften nicht automatisch zwischengespeichert. Sie müssen die Eigenschaften, die Sie zwischenspeichern möchten, mithilfe von **AddProperty** angeben.

Sie können eine Steuerelement Muster-Eigenschaft (z. b. die Value-Eigenschaft des [value](uiauto-implementingvalue.md) -Steuerelement Musters) abrufen, ohne das gesamte Steuerelement Muster in den Cache abrufen zu müssen. Sie müssen das Steuerelement Muster nur abrufen, wenn Sie eine Steuerelement Muster Methode verwenden müssen.

### <a name="specifying-the-scoping-and-filtering-of-a-caching-request"></a>Festlegen des Bereichs und Filterns einer Cache Anforderung

Sie können die Elemente angeben, deren Eigenschaften und Steuerelement Muster Sie zwischenspeichern möchten, indem Sie die [**iuiautomationcacherequest:: TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) -Eigenschaft festlegen, bevor Sie die Anforderung verwenden. Der Gültigkeitsbereich ist relativ zu den Elementen, die von der Methode abgerufen werden, an die die Cache Anforderung übermittelt wird. Wenn Sie z. b. nur [**TreeScope \_**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)-untergeordnete Elemente festlegen und dann ein Benutzeroberflächenautomatisierungs-Element abrufen, werden die Eigenschaften und Steuerelement Muster der untergeordneten Elemente dieses Elements zwischengespeichert, die Eigenschaften und Steuerelement Muster des Elements selbst werden jedoch nicht zwischengespeichert. Um sicherzustellen, dass das Zwischenspeichern für das abgerufene Element selbst ausgeführt wird, müssen Sie ein **TreeScope- \_ Element** in die **iuiautomationcacherequest:: TreeScope** -Eigenschaft einschließen. Es ist nicht möglich, den Bereich auf " **TreeScope \_ Parent** " oder " **TreeScope \_**" festzulegen. Ein übergeordnetes Element kann jedoch zwischengespeichert werden, wenn ein untergeordnetes Element zwischengespeichert wird. Weitere Informationen hierzu finden Sie in diesem Thema unter „Abrufen von zwischengespeicherten untergeordneten und übergeordneten Elementen“.

Der Umfang des zwischen Speicherns wird auch von der [**iuiautomationcacherequest:: TreeFilter**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter) -Eigenschaft beeinflusst. Standardmäßig wird das Zwischenspeichern nur für Elemente ausgeführt, die in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt werden. Sie können diese Eigenschaft jedoch ändern, sodass alle Elemente oder nur in der Inhaltsansicht angezeigte Elemente zwischengespeichert werden.

### <a name="strength-of-element-references"></a>Stärke der Element Verweise

Wenn Sie ein Automation-Element abrufen, haben Sie standardmäßig Zugriff auf alle Eigenschaften und Steuerelement Muster dieses Elements, einschließlich der Eigenschaften und Steuerelement Muster, die nicht zwischengespeichert wurden. Sie können jedoch angeben, dass sich der Verweis auf das Element nur auf zwischengespeicherte Daten bezieht, indem Sie die [**iuiautomationcacherequest:: AutomationElementMode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode) -Eigenschaft auf **AutomationElementMode \_ None** festlegen. In diesem Fall haben Sie keinen Zugriff auf nicht zwischengespeicherte Eigenschaften und Steuerelement Muster von abgerufenen Elementen. Dies bedeutet, dass Sie nicht mit [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)auf aktuelle Eigenschaften wie z. b. [**iuiautomationelement::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled) /////-dateisenabled zugreifen oder ein Steuerelement Muster abrufen können. Bei zwischengespeicherten Steuerelement Mustern können Sie keine Methoden aufrufen, die Aktionen für das Steuerelement ausführen, wie z. b. [**iuiautomationinvokepattern:: Aufrufen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Ein Beispiel für eine Anwendung, für die möglicherweise keine vollständigen Verweise auf Objekte erforderlich sind, ist eine Bildschirm Sprachausgabe, die die Eigenschaften von "Name" und "Steuer Elementtyp" von Elementen in einem Fenster vorab abrufen kann, ohne dass die Automation-Element Objekte

## <a name="retrieving-cached-children-and-parents"></a>Abrufen von zwischengespeicherten untergeordneten und übergeordneten Elementen

Wenn Sie mithilfe der [**iuiautomationcacherequest:: TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) -Eigenschaft der Anforderung ein Automatisierungs Element abrufen und das Zwischenspeichern von untergeordneten Elementen dieses Elements anfordern, können Sie die untergeordneten Elemente abrufen, indem Sie [**iuiautomationelement:: getcachedchildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedchildren) für das Element aufrufen, das Sie abgerufen haben.

Wenn ein [**TreeScope- \_ Element**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) in den Bereich der Cache Anforderung eingeschlossen wurde, kann das Stamm Element der Anforderung durch Aufrufen von [**iuiautomationelement:: getcachedparent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent) für eines der untergeordneten Elemente abgerufen werden.

> [!Note]  
> Sie können keine übergeordneten Elemente des Stammelements der Anforderung zwischenspeichern.

 

## <a name="retrieving-a-new-snapshot-of-the-cache"></a>Abrufen einer neuen Momentaufnahme des Caches

Der Cache ist nur gültig, solange sich nichts in der Benutzeroberfläche ändert. Die Anwendung ist für das Abrufen einer neuen Momentaufnahme des Caches zuständig (in der Regel als Reaktion auf Ereignisse).

Wenn Sie ein Ereignis mit einer Cache Anforderung abonnieren, erhalten Sie eine neue [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Momentaufnahme des Caches als Quelle des Ereignisses, wenn der Ereignishandler aufgerufen wird. Sie können auch eine neue Momentaufnahme der zwischengespeicherten Informationen für ein Element abrufen, indem Sie [**iuiautomationelement:: buildupdatedcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache)aufrufen. Sie können das ursprüngliche [**iuiautomationcacherequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) übergeben, um eine neue Momentaufnahme aller zuvor zwischengespeicherten Informationen zu erhalten.

Durch das Abrufen einer neuen Momentaufnahme des Caches werden die Eigenschaften vorhandener [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Verweise nicht geändert.

## <a name="examples"></a>Beispiele

Codebeispiele, die zeigen, wie die zwischen Speicherungs Funktionen der Benutzeroberflächen Automatisierung verwendet werden, finden Sie unter [verwenden](uiauto-howto-use-caching.md)der Zwischenspeicherung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Abrufen von Benutzeroberflächenautomatisierungs-Elementen](uiauto-obtainingelements.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> </dl>

 

 




