---
title: Zwischenspeichern Benutzeroberflächenautomatisierung Eigenschaften und Steuerelementmustern
description: Bei Verwendung von Microsoft Benutzeroberflächenautomatisierung müssen Clients häufig mehrere Eigenschaften für mehrere Automatisierungselemente abrufen.
ms.assetid: 948b3bb9-75a9-4197-9680-e6fe7bb86feb
keywords:
- Zwischenspeichern, Benutzeroberflächenautomatisierung Eigenschaften
- Caching, Eigenschaften
- Zwischenspeichern, Benutzeroberflächenautomatisierung Steuerelementmuster
- Zwischenspeichern, Steuern von Mustern
- Benutzeroberflächenautomatisierung,Zwischenspeichern von Eigenschaften
- Benutzeroberflächenautomatisierung, Zwischenspeichern von Eigenschaften
- Clients, Zwischenspeichern Benutzeroberflächenautomatisierung Eigenschaften
- Clients, Zwischenspeichern Benutzeroberflächenautomatisierung Steuerelementmuster
- Benutzeroberflächenautomatisierung,Zwischenspeichern von Steuerelementmustern
- Benutzeroberflächenautomatisierung, Steuern der Musterzwischenspeicherung
- Steuerelementmuster, Zwischenspeichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae14fb607dd66ab1a4ea99cd9836f2f74e5c863afef8465843d3ea174186ef29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324974"
---
# <a name="caching-ui-automation-properties-and-control-patterns"></a>Zwischenspeichern Benutzeroberflächenautomatisierung Eigenschaften und Steuerelementmustern

Bei Verwendung von Microsoft Benutzeroberflächenautomatisierung müssen Clients häufig mehrere Eigenschaften für mehrere Automatisierungselemente abrufen. Ein Client kann einzelne Eigenschaften elementweise abrufen, indem er die Methoden zum Abrufen von Eigenschaften wie [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) oder [**CurrentAccessKey verwendet.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey) Diese Methode ist jedoch langsam und ineffizient, da sie einen prozessübergreifenden Aufruf für jede abzurufende Eigenschaft erfordert. Zur Verbesserung der Leistung können Clients die Zwischenspeicherungsfunktionen (auch als Massenabruf bezeichnet) von Benutzeroberflächenautomatisierung verwenden. Durch das Zwischenspeichern kann ein Client alle gewünschten Eigenschaften für alle gewünschten Elemente mit einem einzigen Methodenaufruf abrufen. Der Client kann dann die einzelnen Eigenschaften nach Bedarf aus dem Cache abrufen und regelmäßig eine neue Momentaufnahme des Caches abrufen, in der Regel als Reaktion auf Ereignisse, die Änderungen in der Benutzeroberfläche kennzeichnen.

Die Anwendung kann das Zwischenspeichern anfordern, wenn sie ein Benutzeroberflächenautomatisierung Element mithilfe einer Methode wie [**IUIAutomation::ElementFromPointBuildCache,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache) [**IUIAutomationTreeWalker::GetFirstChildElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache)oder [**IUIAutomationElement::FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache)abruft.

Das Zwischenspeichern erfolgt auch, wenn Sie beim Abonnieren von Ereignissen eine Cacheanforderung angeben. Das Benutzeroberflächenautomatisierung -Element, das an Ihren Ereignishandler als Quelle eines Ereignisses übergeben wird, enthält die zwischengespeicherten Eigenschaften und Steuerelementmuster, die von der Cacheanforderung angegeben werden. Alle Änderungen, die an der Cacheanforderung vorgenommen werden, nachdem Sie das Ereignis abonniert haben, haben keine Auswirkungen.

Dieses Thema enthält folgende Abschnitte:

-   [Cacheanforderungen](#cache-requests)
    -   [Angeben von Eigenschaften- und Steuerelementmustern, die zwischengespeichert werden sollen](#specifying-property-and-control-patterns-to-cache)
    -   [Angeben des Bereichs und der Filterung einer Cacheanforderung](#specifying-the-scoping-and-filtering-of-a-caching-request)
    -   [Stärke von Elementverweisen](#strength-of-element-references)
-   [Abrufen von zwischengespeicherten untergeordneten und übergeordneten Elementen](#retrieving-cached-children-and-parents)
-   [Abrufen einer neuen Momentaufnahme des Caches](#retrieving-a-new-snapshot-of-the-cache)
-   [Beispiele](#examples)
-   [Zugehörige Themen](#related-topics)

## <a name="cache-requests"></a>Cacheanforderungen

Das Zwischenspeichern umfasst das Bestimmen der abzurufenden Eigenschaften und der Elemente, aus denen sie abgerufen werden sollen, und die anschließende Verwendung dieser Informationen zum Erstellen einer Cacheanforderung. Wenn der Client eine [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für ein Benutzeroberflächenelement abruft, speichert Benutzeroberflächenautomatisierung die in der Cacheanforderung angegebenen Informationen zwischen.

Um eine Cacheanforderung zu erstellen, verwenden Sie zunächst die [**IUIAutomation::CreateCacheRequest-Methode,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createcacherequest) um einen [**IUIAutomationCacheRequest-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) abzurufen. Konfigurieren Sie als Nächstes die Cacheanforderung mithilfe der Methoden von **IUIAutomationCacheRequest.**

### <a name="specifying-property-and-control-patterns-to-cache"></a>Angeben von Eigenschaften- und Steuerelementmustern, die zwischengespeichert werden sollen

Sie können Eigenschaften angeben, die zwischengespeichert werden sollen, indem [**Sie IUIAutomationCacheRequest::AddProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addproperty)aufrufen. Sie können Steuerelementmuster angeben, die zwischengespeichert werden sollen, indem [**Sie IUIAutomationCacheRequest::AddPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addpattern)aufrufen. Wenn ein Steuerelementmuster zwischengespeichert wird, werden seine Eigenschaften nicht automatisch zwischengespeichert. Sie müssen die Eigenschaften angeben, die Sie zwischenspeichern möchten, indem **Sie AddProperty verwenden.**

Sie können eine Steuerelementmustereigenschaft abrufen (z. [](uiauto-implementingvalue.md) B. die Value-Eigenschaft des Value-Steuerelementmusters), ohne das gesamte Steuerelementmuster in den Cache abrufen zu müssen. Sie müssen das Steuerelementmuster nur abrufen, wenn Sie eine Steuerelementmustermethode verwenden müssen.

### <a name="specifying-the-scoping-and-filtering-of-a-caching-request"></a>Angeben des Bereichs und der Filterung einer Cacheanforderung

Sie können die Elemente angeben, deren Eigenschaften und Steuerelementmuster Sie zwischenspeichern möchten, indem Sie die [**IUIAutomationCacheRequest::TreeScope-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) festlegen, bevor Sie die Anforderung verwenden. Der Bereich ist relativ zu den Elementen, die von der Methode abgerufen werden, an die die Cacheanforderung übergeben wird. Wenn Sie z. B. nur [**TreeScope \_ Children**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)festlegen und dann ein Benutzeroberflächenautomatisierung Element abrufen, werden die Eigenschaften und Steuerelementmuster der untergeordneten Elemente dieses Elements zwischengespeichert, aber die Eigenschaften und Steuerelementmuster des Elements selbst werden nicht zwischengespeichert. Um sicherzustellen, dass die Zwischenspeicherung für das abgerufene Element selbst durchgeführt wird, müssen Sie **\_ treeScope-Element** in die **IUIAutomationCacheRequest::TreeScope-Eigenschaft** einschließen. Es ist nicht möglich, den Bereich auf **TreeScope \_ Parent** oder **TreeScope \_ Ancestors** festzulegen. Ein übergeordnetes Element kann jedoch zwischengespeichert werden, wenn ein untergeordnetes Element zwischengespeichert wird. Weitere Informationen hierzu finden Sie in diesem Thema unter „Abrufen von zwischengespeicherten untergeordneten und übergeordneten Elementen“.

Der Umfang der Zwischenspeicherung wird auch von der [**IUIAutomationCacheRequest::TreeFilter-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter) beeinflusst. Standardmäßig wird das Zwischenspeichern nur für Elemente ausgeführt, die in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur angezeigt werden. Sie können diese Eigenschaft jedoch ändern, sodass alle Elemente oder nur in der Inhaltsansicht angezeigte Elemente zwischengespeichert werden.

### <a name="strength-of-element-references"></a>Stärke von Elementverweisen

Wenn Sie ein Automatisierungselement abrufen, haben Sie standardmäßig Zugriff auf alle Eigenschaften und Steuerelementmuster dieses Elements, einschließlich der Eigenschaften und Steuerelementmuster, die nicht zwischengespeichert wurden. Sie können jedoch angeben, dass der Verweis auf das Element nur auf zwischengespeicherte Daten verweist, indem Sie die [**IUIAutomationCacheRequest::AutomationElementMode-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode) auf **AutomationElementMode \_ None** festlegen. In diesem Fall haben Sie keinen Zugriff auf nicht zwischenspeicherte Eigenschaften und Steuerelementmuster der abgerufenen Elemente. Dies bedeutet, dass Sie nicht auf aktuelle Eigenschaften wie [**IUIAutomationElement::CurrentIsEnabled**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled) zugreifen oder ein Steuerelementmuster mit [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)abrufen können. Bei zwischengespeicherten Steuerelementmustern können Sie keine Methoden aufrufen, die Aktionen für das Steuerelement ausführen, z. [**B. IUIAutomationInvokePattern::Invoke.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke)

Ein Beispiel für eine Anwendung, die möglicherweise keine vollständigen Verweise auf Objekte benötigt, ist eine Sprachausgabe, die die Eigenschaften des Namens und des Steuerelementtyps von Elementen in einem Fenster vorab abrufen kann, ohne dass die Automatisierungselementobjekte selbst benötigt werden.

## <a name="retrieving-cached-children-and-parents"></a>Abrufen von zwischengespeicherten untergeordneten und übergeordneten Elementen

Wenn Sie ein Automatisierungselement abrufen und das Zwischenspeichern von Anforderungen für untergeordnete Elemente dieses Elements über die [**IUIAutomationCacheRequest::TreeScope-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) der Anforderung anfordern, ist es möglich, die untergeordneten Elemente abzurufen, indem [**Sie IUIAutomationElement::GetCachedChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedchildren) für das element aufrufen, das Sie abgerufen haben.

Wenn [**das \_ TreeScope-Element**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) im Bereich der Cacheanforderung enthalten war, kann das Stammelement der Anforderung abgerufen werden, indem [**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent) für eines der untergeordneten Elemente aufgerufen wird.

> [!Note]  
> Sie können keine übergeordneten Elemente des Stammelements der Anforderung zwischenspeichern.

 

## <a name="retrieving-a-new-snapshot-of-the-cache"></a>Abrufen einer neuen Momentaufnahme des Caches

Der Cache ist nur gültig, solange sich auf der Benutzeroberfläche nichts ändert. Ihre Anwendung ist für das Abrufen einer neuen Momentaufnahme des Caches verantwortlich, in der Regel als Reaktion auf Ereignisse.

Wenn Sie ein Ereignis mit einer Cacheanforderung abonnieren, erhalten Sie eine neue [**IUIAutomationElement-Momentaufnahme**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) des Caches als Quelle des Ereignisses, wenn Der Ereignishandler aufgerufen wird. Sie können auch eine neue Momentaufnahme zwischengespeicherter Informationen für ein Element abrufen, indem [**Sie IUIAutomationElement::BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache)aufrufen. Sie können die ursprüngliche [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) übergeben, um eine neue Momentaufnahme aller zuvor zwischengespeicherten Informationen zu erhalten.

Durch das Abrufen einer neuen Momentaufnahme des Caches werden die Eigenschaften vorhandener [**IUIAutomationElement-Verweise**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) nicht geändert.

## <a name="examples"></a>Beispiele

Codebeispiele, die zeigen, wie die Zwischenspeicherungsfunktionen von Benutzeroberflächenautomatisierung verwendet werden, finden Sie unter [Verwenden von Caching.](uiauto-howto-use-caching.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Abrufen von Benutzeroberflächenautomatisierungs-Elementen](uiauto-obtainingelements.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> </dl>

 

 




