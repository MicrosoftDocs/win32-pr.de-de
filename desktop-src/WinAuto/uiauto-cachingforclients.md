---
title: Zwischenspeichern Benutzeroberflächenautomatisierung Eigenschaften und Steuerelementmustern
description: Wenn Sie Microsoft Benutzeroberflächenautomatisierung verwenden, müssen Clients häufig mehrere Eigenschaften für mehrere Automatisierungselemente abrufen.
ms.assetid: 948b3bb9-75a9-4197-9680-e6fe7bb86feb
keywords:
- Caching,Benutzeroberflächenautomatisierung Eigenschaften
- Caching,Eigenschaften
- Caching,Benutzeroberflächenautomatisierung Steuerelementmuster
- Caching,Steuerelementmuster
- Benutzeroberflächenautomatisierung,Cachingeigenschaften
- Benutzeroberflächenautomatisierung,Zwischenspeichern von Eigenschaften
- Clients,Zwischenspeichern Benutzeroberflächenautomatisierung Eigenschaften
- Clients,Zwischenspeichern Benutzeroberflächenautomatisierung Steuerelementmustern
- Benutzeroberflächenautomatisierung,Zwischenspeichern von Steuerelementmustern
- Benutzeroberflächenautomatisierung,Musterzwischenspeicherung steuern
- Steuerelementmuster,Caching
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

Wenn Sie Microsoft Benutzeroberflächenautomatisierung verwenden, müssen Clients häufig mehrere Eigenschaften für mehrere Automatisierungselemente abrufen. Ein Client kann einzelne Eigenschaften mithilfe der Methoden zum Abrufen von Eigenschaften wie [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) oder [**CurrentAccessKey**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey)einzeln abrufen. Diese Methode ist jedoch langsam und ineffizient, da sie einen prozessübergreifenden Aufruf für jede abgerufene Eigenschaft erfordert. Um die Leistung zu verbessern, können Clients die Zwischenspeicherungsfunktionen (auch als Massenabruf bezeichnet) von Benutzeroberflächenautomatisierung. Zwischenspeichern ermöglicht einem Client, alle gewünschten Eigenschaften für alle gewünschten Elemente mit einem einzigen Methodenaufruf abzurufen. Der Client kann dann die einzelnen Eigenschaften nach Bedarf aus dem Cache abrufen und in regelmäßigen Abständen eine neue Momentaufnahme des Caches abrufen, in der Regel als Reaktion auf Ereignisse, die Änderungen in der Benutzeroberfläche bedeuten.

Die Anwendung kann die Zwischenspeicherung anfordern, wenn sie ein Benutzeroberflächenautomatisierung-Element mithilfe einer Methode abruft, z.B. [**IUIAutomation::ElementFromPointBuildCache,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache) [**IUIAutomationTreeWalker::GetFirstChildElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache)oder [**IUIAutomationElement::FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache).

Die Zwischenspeicherung erfolgt auch, wenn Sie beim Abonnieren von Ereignissen eine Cacheanforderung angeben. Das Benutzeroberflächenautomatisierung element, das als Quelle eines Ereignisses an den Ereignishandler übergeben wird, enthält die zwischengespeicherten Eigenschaften und Steuerelementmuster, die von der Cacheanforderung angegeben werden. Alle Änderungen, die nach dem Abonnieren des Ereignisses an der Cacheanforderung vorgenommen werden, haben keine Auswirkungen.

Dieses Thema enthält folgende Abschnitte:

-   [Cacheanforderungen](#cache-requests)
    -   [Angeben von Eigenschaften- und Steuerelementmustern für den Cache](#specifying-property-and-control-patterns-to-cache)
    -   [Angeben des Bereichs und der Filterung einer Cacheanforderung](#specifying-the-scoping-and-filtering-of-a-caching-request)
    -   [Stärke von Elementverweisen](#strength-of-element-references)
-   [Abrufen von zwischengespeicherten untergeordneten und übergeordneten Elementen](#retrieving-cached-children-and-parents)
-   [Abrufen einer neuen Momentaufnahme des Caches](#retrieving-a-new-snapshot-of-the-cache)
-   [Beispiele](#examples)
-   [Zugehörige Themen](#related-topics)

## <a name="cache-requests"></a>Cacheanforderungen

Beim Zwischenspeichern wird bestimmt, welche Eigenschaften abgerufen werden sollen und von welchen Elementen sie abgerufen werden sollen. Anschließend wird anhand dieser Informationen eine Cacheanforderung erstellt. Wenn der Client eine [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für das Benutzeroberflächenelement erhält, speichert Benutzeroberflächenautomatisierung die in der Cacheanforderung angegebenen Informationen zwischen.

Um eine Cacheanforderung zu erstellen, rufen Sie zunächst mithilfe der [**IUIAutomation::CreateCacheRequest-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createcacherequest) einen [**IUIAutomationCacheRequest-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) ab. Konfigurieren Sie als Nächstes die Cacheanforderung mithilfe der Methoden von **IUIAutomationCacheRequest**.

### <a name="specifying-property-and-control-patterns-to-cache"></a>Angeben von Eigenschaften- und Steuerelementmustern für den Cache

Sie können Eigenschaften angeben, die zwischengespeichert werden, indem [**Sie IUIAutomationCacheRequest::AddProperty aufrufen.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addproperty) Sie können steuerelementmuster angeben, die zwischengespeichert werden, indem [**Sie IUIAutomationCacheRequest::AddPattern aufrufen.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addpattern) Wenn ein Steuerelementmuster zwischengespeichert wird, werden seine Eigenschaften nicht automatisch zwischengespeichert. Sie müssen die Eigenschaften angeben, die Sie mit **addProperty zwischenspeichern möchten.**

Sie können eine Steuerelementmustereigenschaft (z. B. [](uiauto-implementingvalue.md) die Value-Eigenschaft des Value-Steuerelementmusters) abrufen, ohne das gesamte Steuerelementmuster in den Cache abrufen zu müssen. Sie müssen das Steuerelementmuster nur abrufen, wenn Sie eine Steuerelementmustermethode verwenden müssen.

### <a name="specifying-the-scoping-and-filtering-of-a-caching-request"></a>Angeben des Bereichs und der Filterung einer Cacheanforderung

Sie können die Elemente angeben, deren Eigenschaften und Steuerelementmuster Sie zwischenspeichern möchten, indem Sie die [**IUIAutomationCacheRequest::TreeScope-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) festlegen, bevor Sie die Anforderung verwenden. Der Bereich ist relativ zu den Elementen, die von der Methode abgerufen werden, an die die Cacheanforderung übergeben wird. Wenn Sie z. B. nur [**TreeScope \_ Children**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)festlegen und dann ein Benutzeroberflächenautomatisierung-Element abrufen, werden die Eigenschaften und Steuerelementmuster der unteren Elemente dieses Elements zwischengespeichert, aber die Eigenschaften und Steuerelementmuster des Elements selbst werden nicht zwischengespeichert. Um sicherzustellen, dass die Zwischenspeicherung für das abgerufene Element selbst erfolgt, müssen Sie **das \_ TreeScope-Element** in die **IUIAutomationCacheRequest::TreeScope-Eigenschaft** einbinden. Der Bereich kann nicht auf **TreeScope \_ Parent oder** **TreeScope Parent festgelegt \_ werden.** Ein übergeordnetes Element kann jedoch zwischengespeichert werden, wenn ein untergeordnetes Element zwischengespeichert wird. Weitere Informationen hierzu finden Sie in diesem Thema unter „Abrufen von zwischengespeicherten untergeordneten und übergeordneten Elementen“.

Der Umfang der Zwischenspeicherung wird auch von der [**IUIAutomationCacheRequest::TreeFilter-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter) beeinflusst. Standardmäßig wird die Zwischenspeicherung nur für Elemente ausgeführt, die in der Steuerelementansicht der Benutzeroberflächenautomatisierung werden. Sie können diese Eigenschaft jedoch ändern, sodass alle Elemente oder nur in der Inhaltsansicht angezeigte Elemente zwischengespeichert werden.

### <a name="strength-of-element-references"></a>Stärke von Elementverweisen

Wenn Sie ein Automatisierungselement abrufen, haben Sie standardmäßig Zugriff auf alle Eigenschaften und Steuerelementmuster dieses Elements, einschließlich der Eigenschaften und Steuerelementmuster, die nicht zwischengespeichert wurden. Sie können jedoch angeben, dass der Verweis auf das -Element nur auf zwischengespeicherte Daten verweist, indem Sie die [**IUIAutomationCacheRequest::AutomationElementMode-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode) auf **AutomationElementMode \_ None festlegen.** In diesem Fall haben Sie keinen Zugriff auf nicht zwischengespeicherte Eigenschaften und Steuerelementmuster abgerufener Elemente. Dies bedeutet, dass Sie nicht auf aktuelle Eigenschaften wie [**IUIAutomationElement::CurrentIsEnabled**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled) zugreifen oder ein Steuerelementmuster mithilfe von [**IUIAutomationElement::GetCurrentPattern abrufen können.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) Bei zwischengespeicherten Steuerelementmustern können Sie keine Methoden aufrufen, die Aktionen für das Steuerelement ausführen, z. B. [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Ein Beispiel für eine Anwendung, die möglicherweise keine vollständigen Verweise auf Objekte benötigt, ist eine Sprachausgabe, die den Namen und die Steuerelementtypeigenschaften von Elementen in einem Fenster vorab abrufen kann, ohne dass die Automatisierungselementobjekte selbst benötigt werden.

## <a name="retrieving-cached-children-and-parents"></a>Abrufen von zwischengespeicherten untergeordneten und übergeordneten Elementen

Wenn Sie ein Automatisierungselement abrufen und das Zwischenspeichern untergeordneter Elemente dieses Elements über die [**IUIAutomationCacheRequest::TreeScope-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) der Anforderung anfordern, ist es möglich, die untergeordneten Elemente durch Aufrufen von [**IUIAutomationElement::GetCachedChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedchildren) für das abgerufene Element abzurufen.

Wenn [**das \_ TreeScope-Element**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) im Bereich der Cacheanforderung enthalten war, kann das Stammelement der Anforderung durch Aufrufen von [**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent) für eines der untergeordneten Elemente abgerufen werden.

> [!Note]  
> Sie können keine übergeordneten Elemente des Stammelements der Anforderung zwischenspeichern.

 

## <a name="retrieving-a-new-snapshot-of-the-cache"></a>Abrufen einer neuen Momentaufnahme des Caches

Der Cache ist nur gültig, solange sich auf der Benutzeroberfläche nichts ändert. Ihre Anwendung ist für das Abrufen einer neuen Momentaufnahme des Caches verantwortlich, in der Regel als Reaktion auf Ereignisse.

Wenn Sie ein Ereignis mit einer Cacheanforderung abonnieren, erhalten Sie eine [**neue IUIAutomationElement-Momentaufnahme**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) des Caches als Quelle des Ereignisses, wenn Ihr Ereignishandler aufgerufen wird. Sie können auch eine neue Momentaufnahme zwischengespeicherter Informationen für ein Element abrufen, indem Sie [**IUIAutomationElement::BuildUpdatedCache aufrufen.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache) Sie können die ursprüngliche [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) übergeben, um eine neue Momentaufnahme aller Informationen zu erhalten, die zuvor zwischengespeichert wurden.

Durch das Abrufen einer neuen Momentaufnahme des Caches werden die Eigenschaften vorhandener [**IUIAutomationElement-Verweise**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) nicht geändert.

## <a name="examples"></a>Beispiele

Codebeispiele, die zeigen, wie sie die Zwischenspeicherungsfunktionen von Benutzeroberflächenautomatisierung, finden Sie unter [Verwenden der Zwischenspeicherung.](uiauto-howto-use-caching.md)

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

 

 




