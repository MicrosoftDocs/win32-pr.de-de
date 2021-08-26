---
title: Abrufen von Benutzeroberflächenautomatisierungs-Elementen
description: In diesem Thema werden verschiedene Möglichkeiten zum Abrufen von IUIAutomationElement-Schnittstellen für Benutzeroberflächenelemente beschrieben.
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- Clients,Abrufen von Benutzeroberflächenautomatisierung Elementen
- clients,Benutzeroberflächenautomatisierung-Elemente
- Clients, Stammelemente
- Clients, Suchbereich
- Benutzeroberflächenautomatisierung,Abrufen von Elementen
- Benutzeroberflächenautomatisierung,elements
- Benutzeroberflächenautomatisierung,Stammelemente
- Benutzeroberflächenautomatisierung,Bedingungen
- Benutzeroberflächenautomatisierung, Suchbereich
- Abrufen von Benutzeroberflächenautomatisierung Elementen
- Stammelemente
- Suchbereich
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: f2ecf8a30f468e7a7ca4df60465993fa7acdc1e8eef1c8537d8c3d796132cb82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997740"
---
# <a name="obtaining-ui-automation-elements"></a>Abrufen von Benutzeroberflächenautomatisierungs-Elementen

In diesem Thema werden verschiedene Möglichkeiten zum Abrufen von [**IUIAutomationElement-Schnittstellen**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für Benutzeroberflächenelemente beschrieben.

**IUIAutomationElement** wird in der [Clientbeispiel-App für Benutzeroberflächenautomatisierung Dokumentinhalt](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)verwendet.

## <a name="root-element"></a>Root-Element

Obwohl Elemente direkt mithilfe von Methoden wie [**IUIAutomation::GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)abgerufen werden können, benötigen einige Clientanwendungen eine Ansicht der hierarchischen Struktur von Elementen, die als Benutzeroberflächenautomatisierung Struktur bezeichnet wird. Das Stammelement dieser Hierarchie ist der Desktop. Sie können dieses Element mithilfe der [**IUIAutomation::GetRootElement-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) oder der [**IUIAutomation::GetRootElementBuildCache-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) abrufen. Beide Methoden rufen einen [**IUIAutomationElement-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ab. Sie können nach Nachfolgerelementen suchen, indem Sie Methoden wie [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) und [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)verwenden.

> [!Note]  
> Im Allgemeinen sollten Sie versuchen, nur direkte untergeordnete Elemente des Stammelements abzurufen. Eine Suche nach Nachfolgern kann Hunderte oder Tausende von Elementen durchlaufen. Wenn Sie versuchen, ein bestimmtes Element auf einer niedrigeren Ebene abzurufen, sollten Sie die Suche aus dem Anwendungsfenster oder aus einem Container auf niedrigerer Ebene starten.

 

## <a name="conditions"></a>Bedingungen

Für die meisten Techniken, die Sie verwenden, um Benutzeroberflächenautomatisierung Elemente abzurufen, müssen Sie eine Bedingung angeben. Eine Bedingung ist ein Satz von Kriterien, der die Elemente definiert, die Sie abrufen möchten. Eine Bedingung wird durch die [**IUIAutomationCondition-Schnittstelle**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition) dargestellt.

Die einfachste Bedingung ist die "true"-Bedingung. Dabei handelt es sich um ein vordefiniertes Objekt, das angibt, dass alle Elemente im Suchbereich zurückgegeben werden sollen. Die false-Bedingung ist die Umkehrung der true-Bedingung und ist weniger nützlich, da sie verhindern würde, dass Elemente gefunden werden. Sie können mit [**IUIAutomation::CreateTrueCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition)eine Schnittstelle für die true-Bedingung abrufen.

Drei weitere vordefinierte Bedingungen, die als Eigenschaften für das [**IUIAutomation-Objekt**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) verfügbar sind, können allein oder in Kombination mit anderen Bedingungen verwendet werden: [**IUIAutomation::ContentViewCondition,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition) [**ControlViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)und [**RawViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition). **RawViewCondition,** das selbst verwendet wird, entspricht der true-Bedingung, da elemente nicht nach den Eigenschaften [**IUIAutomationElement::CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) oder [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) gefiltert werden.

Andere Bedingungen werden aus Bedingungsobjekten erstellt, von denen jede einen Eigenschaftswert angibt. Eine Eigenschaftsbedingung kann beispielsweise angeben, dass das Element aktiviert ist oder ein bestimmtes Steuerelementmuster unterstützt.

Bedingungen, die boolesche Logik verwenden, können kombiniert werden, indem [**IUIAutomation::CreateAndCondition,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition) [**CreateOrCondition,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition) [**CreateNotCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)und verwandte Methoden aufgerufen werden.

## <a name="search-scope"></a>Suchbereich

Suchvorgänge, die mit [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) oder [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) ausgeführt werden, müssen einen Bereich und einen Ausgangspunkt haben.

> [!Note]  
> Alle Kommentare zu diesen beiden Methoden gelten auch für [**IUIAutomationElement::FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) und [**FindAllBuildCache.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache)

 

Der Bereich definiert den Bereich um den Startort, der durchsucht werden soll. Dies kann das Element selbst, seine gleichgeordneten Elemente, sein übergeordnetes Element, seine unmittelbar untergeordneten Elemente und seine Nachfolgerelemente umfassen. Beachten Sie, dass die **Find-Methoden** das Suchen der Microsoft Benutzeroberflächenautomatisierung-Struktur nicht unterstützen. Das heißt, die Suche nach übergeordneten Elementen wird nicht unterstützt.

Der Bereich einer Suche wird durch eine bitweise [](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) Kombination von Werten aus dem TreeScope-Enumerationstyp definiert.

## <a name="finding-a-known-element"></a>Suchen nach einem bekannten Element

Um ein bekanntes Element zu finden, das anhand des Namens, der Automatisierungs-ID oder einer anderen Eigenschaft oder Kombination von Eigenschaften identifiziert wird, ist es am einfachsten, die [**IUIAutomationElement::FindFirst-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) zu verwenden. Wenn das gesuchte Element ein Anwendungsfenster ist, kann der Ausgangspunkt der Suche das Stammelement sein.

Diese Möglichkeit, Benutzeroberflächenautomatisierung Elemente zu finden, ist in automatisierten Testszenarien am nützlichsten.

Ein Codebeispiel, das zeigt, wie sie ein bekanntes Element finden, finden Sie unter [Finding an Element by Name (Suchen eines Elements anhand des Namens](uiauto-howto-find-ui-elements.md)).

## <a name="finding-elements-in-a-subtree"></a>Suchen nach Elementen in einer Unterstruktur

Um alle Elemente zu finden, die bestimmte Kriterien erfüllen und mit einem bekannten Element verknüpft sind, können Sie [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) für das bekannte Element aufrufen. Verwenden Sie diese Methode beispielsweise, um Listenelemente oder Menüelemente aus einer Liste oder einem Menü abzurufen oder alle Steuerelemente in einem Dialogfeld zu identifizieren.

Ein Codebeispiel, das zeigt, wie Elemente in einer Unterstruktur gesucht werden, finden Sie unter [Suchen verwandter Elemente.](uiauto-howto-find-ui-elements.md)

## <a name="walking-a-subtree"></a>Durchlaufen einer Unterstruktur

Wenn Sie keine Vorkenntnisse über die Anwendungen haben, mit denen Ihr Client verwendet werden kann, können Sie mithilfe von [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)eine Teilstruktur aller von Interesse seinden Elemente erstellen. Ihr Client kann dies z. B. als Reaktion auf ein Ereignis mit Fokusveränderung durchführen. Das heißt, wenn eine Anwendung oder ein Steuerelement den Eingabefokus erhält, untersucht der Benutzeroberflächenautomatisierung Client untergeordnete Elemente und möglicherweise alle Nachfolgerelemente des fokussierten Elements.

Beachten Sie, dass das Gehen der Benutzeroberflächenautomatisierung-Struktur ressourcenintensiv ist. Gehen Sie die Struktur nur dann durch, wenn es nicht möglich ist, die Methoden [**IUIAutomationElement::FindFirst,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)oder [**BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache) zu verwenden.

Sie können Ihren eigenen Baumwanderer definieren, indem Sie eine benutzerdefinierte Bedingung an [**IUIAutomation::CreateTreeWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker)übergeben, oder Sie können eines der folgenden vordefinierten Objekte verwenden, die als Eigenschaften der [**IUIAutomation-Basis**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)definiert sind.



| Object                                                              | Zweck                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | Sucht nur Elemente, deren [**IUIAutomationElement::CurrentIsContentElement-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) **TRUE** ist. |
| [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | Sucht nur Elemente, deren [**IUIAutomationElement::CurrentIsControlElement-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) **TRUE** ist. |
| [**RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | Sucht nach allen Elementen.                                                                                                                                          |



 

Nachdem Sie eine [**IUIAutomationTreeWalker-Methode**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)erhalten haben, rufen Sie die **IUIAutomationTreeWalker::GetXxx-Methoden** auf, um durch Elemente der Unterstruktur zu navigieren, und übergeben Sie das Element, von dem aus mit dem Gehen begonnen werden soll.

Die [**IUIAutomationTreeWalker::Normalize-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement) kann verwendet werden, um von einem anderen Element, das nicht Teil der Ansicht ist, zu einem Element in der Unterstruktur zu navigieren. Angenommen, Sie erstellen eine Ansicht einer Unterstruktur mit [**IUIAutomation::ContentViewWalker.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) Ihre Anwendung erhält die Benachrichtigung, dass eine Bildlaufleiste den Eingabefokus erhalten hat. Weil eine Scrolllaufleiste aber kein Inhaltselement ist, fehlt sie in Ihrer Ansicht der Unterstruktur. Sie können jedoch das [**IUIAutomationElement,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) das die Bildlaufleiste darstellt, an **IUIAutomationTreeWalker::Normalize** übergeben und den nächstgelegenen Vorgänger in der Inhaltsansicht abrufen.

Codebeispiele, die die Verwendung der [**IUIAutomationTreeWalker-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) einsehen, finden Sie unter [Walk the Benutzeroberflächenautomatisierung Tree](uiauto-howto-walk-uiautomation-tree.md).

## <a name="other-ways-to-retrieve-an-element"></a>Weitere Möglichkeiten zum Abrufen eines Elements

Zusätzlich zu Suchen und Navigation können Sie ein [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) auf folgende Weise abrufen.

### <a name="from-an-event"></a>Über ein Ereignis

Wenn Ihre Anwendung ein Benutzeroberflächenautomatisierung Ereignis empfängt, wird das an Ihren Ereignishandler übergebene Quellobjekt durch ein [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)dargestellt. Wenn Sie z. B. Ereignisse mit Fokusänderung abonnieren, ist die Quelle, die an [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) übergeben wird, das Element, das den Fokus erhalten hat. Weitere Informationen finden Sie unter [Abonnieren von Benutzeroberflächenautomatisierung Ereignissen.](uiauto-eventsforclients.md)

### <a name="from-a-point"></a>Über einen Punkt

Verwenden Sie die [**IUIAutomation::ElementFromPoint-Methode,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) um ein [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) aus Bildschirmkoordinaten abzurufen, z. B. einer Cursorposition.

### <a name="from-a-window-handle"></a>Über ein Fensterhandle

Um ein [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) aus einem **HWND** abzurufen, verwenden Sie die [**IUIAutomation::ElementFromHandle-Methode.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle)

### <a name="from-the-focused-control"></a>Über das Steuerelement mit Fokus

Um ein [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) abzurufen, das das fokussierte Steuerelement darstellt, verwenden Sie die [**IUIAutomation::GetFocusedElement-Methode.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)

## <a name="related-topics"></a>Zugehörige Themen

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)

[Beispiel-App für Benutzeroberflächenautomatisierung Dokumentinhaltsclient](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
