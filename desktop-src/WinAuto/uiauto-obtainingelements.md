---
title: Abrufen von Benutzeroberflächenautomatisierungs-Elementen
description: In diesem Thema werden verschiedene Möglichkeiten zum Abrufen von iuiautomationelement-Schnittstellen für Benutzeroberflächen Elemente beschrieben.
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- Clients, Abrufen von Benutzeroberflächenautomatisierungs-Elementen
- Clients, Benutzeroberflächenautomatisierungs-Elemente
- Clients, Stamm Elemente
- Clients, Suchbereich
- Benutzeroberflächen Automatisierung, Abrufen von Elementen
- Benutzeroberflächen Automatisierung, Elemente
- Benutzeroberflächenautomatisierungs, Root-Elemente
- Benutzeroberflächenautomatisierungs, Bedingungen
- Benutzeroberflächen Automatisierung, Suchbereich
- Abrufen von Elementen der Benutzeroberflächen Automatisierung
- Stammelemente
- Suchbereich
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: a1adbcea5cea81f97350ef15c491b289e07d3ee6
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106355854"
---
# <a name="obtaining-ui-automation-elements"></a>Abrufen von Benutzeroberflächenautomatisierungs-Elementen

In diesem Thema werden verschiedene Möglichkeiten zum Abrufen von [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstellen für Benutzeroberflächen Elemente beschrieben.

**Iuiautomationelement** wird in der Benutzeroberflächenautomatisierungs- [Client-Beispiel-App für Dokumentinhalte](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)verwendet.

## <a name="root-element"></a>Root-Element

Obwohl Elemente direkt mithilfe von-Methoden abgerufen werden können, wie z. b. [**iuiautomation:: getfocucment**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), benötigen einige Client Anwendungen eine Ansicht der hierarchischen Struktur von Elementen, die als Benutzeroberflächenautomatisierungs-Struktur bezeichnet wird. Das Stamm Element dieser Hierarchie ist der Desktop. Sie können dieses Element mithilfe der [**iuiautomation:: getrootelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) -Methode oder der [**iuiautomation:: getrootelementbuildcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) -Methode abrufen. Beide Methoden rufen einen [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstellen Zeiger ab. Sie können nachfolgende Elemente mithilfe von Methoden suchen, wie z. b. [**iuiautomationelement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) und [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall).

> [!Note]  
> Im Allgemeinen sollten Sie versuchen, nur direkte untergeordnete Elemente des Root-Elements abzurufen. Bei einer Suche nach Nachfolgern können Hunderte oder Tausende von Elementen durchlaufen werden. Wenn Sie versuchen, ein bestimmtes Element auf einer niedrigeren Ebene abzurufen, sollten Sie die Suche aus dem Anwendungsfenster oder aus einem Container auf niedrigerer Ebene starten.

 

## <a name="conditions"></a>Bedingungen

Für die meisten Techniken, die Sie verwenden, um Benutzeroberflächenautomatisierungs-Elemente abzurufen, müssen Sie eine Bedingung angeben. Eine Bedingung besteht aus einer Reihe von Kriterien, die die Elemente definieren, die Sie abrufen möchten. Eine Bedingung wird durch die [**iuiautomationcondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition) -Schnittstelle dargestellt.

Die einfachste Bedingung ist die true-Bedingung, bei der es sich um ein vordefiniertes Objekt handelt, das angibt, dass alle Elemente im Suchbereich zurückgegeben werden sollen. Die false-Bedingung ist die Umkehrung der true-Bedingung und ist weniger nützlich, da Sie verhindert, dass Elemente gefunden werden. Sie können eine Schnittstelle zu der true-Bedingung mithilfe von [**iuiautomation:: kreatetruecondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition)abrufen.

Drei weitere vordefinierte Bedingungen, die als Eigenschaften für das [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Objekt verfügbar sind, können allein oder in Kombination mit anderen Bedingungen verwendet werden: [**iuiautomation:: ContentViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition), [**ControlViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)und [**RawViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition). **RawViewCondition**, das von sich selbst verwendet wird, entspricht der true-Bedingung, da es keine Elemente nach [**den Eigenschaften**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) [**iuiautomationelement::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) Currency.

Andere Bedingungen werden aus Bedingungs Objekten erstellt, von denen jedes einen Eigenschafts Wert angibt. Beispielsweise kann eine Eigenschafts Bedingung angeben, dass das Element aktiviert ist oder ein bestimmtes Steuerelement Muster unterstützt.

Bedingungen, die boolesche Logik verwenden, können kombiniert werden, indem [**iuiautomation:: createandcondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition), [**createorcondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition), [**createnotcondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)und verwandte Methoden aufgerufen werden.

## <a name="search-scope"></a>Suchbereich

Suchvorgänge, die mit [**iuiautomationelement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) oder [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) ausgeführt werden, müssen über einen Bereich und einen Ausgangspunkt verfügen.

> [!Note]  
> Alle Kommentare zu diesen beiden Methoden gelten auch für [**iuiautomationelement:: findfirstbuildcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) und [**findallbuildcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache).

 

Der Bereich definiert den Leerraum um den Startort, der durchsucht werden soll. Dies kann das Element selbst, seine gleich geordneten Elemente, das übergeordnete Element, seine unmittelbaren untergeordneten Elemente und seine Nachfolger enthalten. Beachten Sie, dass die **Suchmethoden das Durchsuchen der Microsoft** UI Automation-Struktur nicht unterstützen. Das heißt, dass die Suche nach Vorgänger Elementen nicht unterstützt wird.

Der Bereich einer Suche wird durch eine bitweise Kombination von Werten aus dem [**TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) -enumerierten Typ definiert.

## <a name="finding-a-known-element"></a>Suchen nach einem bekannten Element

Um nach einem bekannten Element zu suchen, das anhand des Namens, der Automatisierungs-ID oder einer anderen Eigenschaft oder Kombination von Eigenschaften identifiziert wird, ist es am einfachsten, die [**iuiautomationelement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) -Methode zu verwenden. Wenn das gesuchte Element ein Anwendungsfenster ist, kann der Ausgangspunkt der Suche das Stamm Element sein.

Diese Art der Suche nach Benutzeroberflächenautomatisierungs-Elementen ist in automatisierten Testszenarien besonders nützlich.

Ein Codebeispiel, in dem gezeigt wird, wie ein Wissenselement gefunden wird, finden Sie untersuchen [eines Elements nach Namen](uiauto-howto-find-ui-elements.md).

## <a name="finding-elements-in-a-subtree"></a>Suchen nach Elementen in einer Unterstruktur

Um alle Elemente zu finden, die bestimmte Kriterien erfüllen und mit einem bekannten Element verknüpft sind, können Sie [**iuiautomationelement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) für das bekannte Element aufzurufen. Verwenden Sie diese Methode z. b., um Listenelemente oder Menü Elemente aus einer Liste oder einem Menü abzurufen oder um alle Steuerelemente in einem Dialogfeld zu identifizieren.

Ein Codebeispiel, das zeigt, wie Elemente in einer Unterstruktur gesucht werden, finden Sie untersuchen [verwandter Elemente](uiauto-howto-find-ui-elements.md).

## <a name="walking-a-subtree"></a>Durchlaufen einer Unterstruktur

Wenn Sie keine Vorkenntnisse zu den Anwendungen haben, mit denen Ihr Client möglicherweise verwendet wird, können Sie mithilfe von [**iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)eine Unterstruktur aller relevanten Elemente erstellen. Der Client kann dies beispielsweise als Reaktion auf ein Ereignis mit Fokus Änderung durchführen. Das heißt, wenn eine Anwendung oder ein Steuerelement den Eingabefokus erhält, überprüft der Benutzeroberflächenautomatisierungs-Client untergeordnete Elemente und möglicherweise alle nachfolgenden Elemente des Fokus Elements

Beachten Sie, dass das Durchlaufen der Benutzeroberflächenautomatisierungs-strukturressourcen intensiv ist. Durchlaufen Sie die Struktur nur, wenn es nicht möglich ist, die [**iuiautomationelement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)-, [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)-oder [**buildupdatedcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache) -Methoden zu verwenden.

Sie können einen eigenen Baum Durchlauf definieren, indem Sie eine benutzerdefinierte Bedingung an [**iuiautomation:: | atetreewalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker)übergeben, oder Sie können eines der folgenden vordefinierten Objekte verwenden, die als Eigenschaften der [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)-Basis definiert sind.



| Object                                                              | Zweck                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | Sucht nur nach Elementen, deren [**iuiautomationelement:: Currency-ContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) -Eigenschaft den Wert **true** hat. |
| [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | Sucht nur nach Elementen, deren [**iuiautomationelement::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) -Eigenschaft auf **true** festgelegt ist. |
| [**RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | Sucht nach allen Elementen.                                                                                                                                          |



 

Nachdem Sie einen [**iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)erhalten haben, rufen Sie die **iuiautomationtreewalker:: GetXXX** -Methoden auf, um die Elemente der Unterstruktur zu navigieren, und übergeben Sie das-Element, von dem Sie mit dem durchlaufen beginnen.

Die [**iuiautomationtreewalker:: normalize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement) -Methode kann verwendet werden, um zu einem Element in der Teilstruktur von einem anderen Element zu navigieren, das nicht Teil der Ansicht ist. Nehmen Sie beispielsweise an, Sie erstellen eine Ansicht einer Unterstruktur mithilfe von [**iuiautomation:: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker). Die Anwendung empfängt eine Benachrichtigung, dass eine Scrollleiste den Eingabefokus erhalten hat. Weil eine Scrolllaufleiste aber kein Inhaltselement ist, fehlt sie in Ihrer Ansicht der Unterstruktur. Sie können jedoch das [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) , das die Bild Lauf Leiste darstellt, an **iuiautomationtreewalker:: normalize** übergeben und den nächsten Vorgänger in der Inhaltsansicht abrufen.

Codebeispiele, die zeigen, wie die [**iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) -Schnittstelle verwendet wird, finden Sie unter Gewusst wie: durch [laufen der Benutzeroberflächenautomatisierungs](uiauto-howto-walk-uiautomation-tree.md)-Struktur

## <a name="other-ways-to-retrieve-an-element"></a>Weitere Möglichkeiten zum Abrufen eines Elements

Zusätzlich zu Such Vorgängen und Navigation können Sie ein [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) wie folgt abrufen.

### <a name="from-an-event"></a>Über ein Ereignis

Wenn Ihre Anwendung ein Benutzeroberflächenautomatisierungs-Ereignis empfängt, wird das an den Ereignishandler über gegebene Quell Objekt durch ein [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)dargestellt. Wenn Sie z. b. Ereignisse mit Fokus Änderung abonnieren, ist die an [**iuiautomationfocuschangedeventhandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) über gegebene Quelle das Element, das den Fokus erhalten hat. Weitere Informationen finden Sie unter [Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen](uiauto-eventsforclients.md).

### <a name="from-a-point"></a>Über einen Punkt

Wenn Sie ein [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) von Bildschirm Koordinaten abrufen möchten, z. b. eine Cursorposition, verwenden Sie die [**iuiautomation:: elementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) -Methode.

### <a name="from-a-window-handle"></a>Über ein Fensterhandle

Um ein [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) aus einem **HWND** abzurufen, verwenden Sie die [**iuiautomation:: elementfromhandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) -Methode.

### <a name="from-the-focused-control"></a>Über das Steuerelement mit Fokus

Zum Abrufen eines [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) , das das Steuerelement mit Fokus darstellt, verwenden Sie die [**iuiautomation:: getfocumindelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement) -Methode.

## <a name="related-topics"></a>Zugehörige Themen

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)

[Benutzeroberflächenautomatisierungs-Dokument Inhalts Client-Beispiel-App](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
