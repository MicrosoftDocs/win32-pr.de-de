---
description: Windows-Explorer bietet eine grafische Darstellung des Shell-Namespace in Kombination mit Tools, mit denen Benutzer mit shellobjekten interagieren können.
ms.assetid: cc387338-15fa-4350-b039-61a0f1c5030a
title: Grundlegendes zu Shellnamespace-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0150092a25708c1f079160a9d106a7b8205e231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979976"
---
# <a name="understanding-shell-namespace-extensions"></a>Grundlegendes zu Shellnamespace-Erweiterungen

Windows-Explorer bietet eine grafische Darstellung des Shell-Namespace in Kombination mit Tools, mit denen Benutzer mit shellobjekten interagieren können. Mit einer Namespace Erweiterung können Sie einen beliebigen Textteil annehmen und Windows Explorer dem Benutzer als virtuellen Ordner präsentieren lassen. Wenn ein Benutzer diesen Ordner durchsucht, werden Ihre Daten als Struktur strukturierte Hierarchie von Ordnern und Dateien dargestellt, ähnlich wie der Rest des Shell-Namespace. Benutzer und Anwendungen können mit dem Inhalt dieses virtuellen Ordners auf die gleiche Weise wie mit allen anderen Namespace Objekten interagieren. In diesem Dokument wird erläutert, wie Sie eine Namespace Erweiterung erstellen.

-   [Funktionsweise einer Namespace Erweiterung](#how-a-namespace-extension-works)
-   [Das Standard Objekt für die System Ordneransicht (defview)](#the-default-system-folder-view-object-defview)
-   [Interaktion von Windows-Explorer mit einer Namespace Erweiterung](#how-windows-explorer-interacts-with-a-namespace-extension)
    -   [Strukturansicht](#tree-view)
    -   [Ordneransicht](#folder-view)
    -   [Menüleiste und Symbolleisten](#menu-bar-and-toolbars)
    -   [Statusleiste](#status-bar)

## <a name="how-a-namespace-extension-works"></a>Funktionsweise einer Namespace Erweiterung

Im Hintergrund wird jeder Ordner, der in Windows Explorer angezeigt wird, durch ein COM-Objekt (Component Object Model) dargestellt, das als *Ordner Objekt* bezeichnet wird. Jedes Mal, wenn der Benutzer mit einem Ordner oder seinem Inhalt interagiert, kommuniziert die Shell über eine Reihe von Standardschnittstellen mit dem zugeordneten Ordner Objekt. Das Ordner Objekt übernimmt dann die für die Reaktion auf die Benutzeraktion erforderlichen Änderungen, und die Shell aktualisiert die Windows Explorer-Anzeige.

Der Großteil der Dateien und Ordner, mit denen Benutzer interagieren, ist Teil des Dateisystems oder eines virtuellen System Ordners, z. b. der Papierkorb. In der anderen Dokumentation wurde erläutert, wie Sie das Verhalten dieser Standardordner anpassen können, um die Anforderungen Ihrer Anwendung zu erfüllen, indem Sie die Registrierung ändern oder [Shellerweiterungs Handler](handlers.md)implementieren. Die Erweiterung der Shell auf diese Weise ist jedoch besonders nützlich, wenn Ihre Informationen problemlos in Form von normalen Dateisystem Dateien oder-Ordnern verpackt werden können.

Es gibt eine Reihe von Situationen, in denen das Speichern von Daten als Sammlung von Dateisystem Ordnern und-Dateien möglicherweise unerwünscht oder sogar unmöglich ist. Einige Beispiele für diese Art von Daten sind:

-   Eine Auflistung von Elementen, die am effektivsten in einer einzelnen Datei (z. b. in einer Datenbank) verpackt ist.
-   Eine Auflistung von Elementen, die auf einem Remote Computer gespeichert sind, der nicht über ein standardmäßiges Windows-Dateisystem verfügt. Ein Beispiel für solche Daten sind die Informationen, die auf einem persönlichen Digital Assistant (PDA) oder einer digitalen Kamera gespeichert sind.
-   Eine Auflistung von Elementen, die keine gespeicherten Daten darstellt. Ein Beispiel für solche Daten sind die Drucker Links, die im Ordner Standarddrucker enthalten sind.

Eine Möglichkeit, diese Art von Daten für einen Benutzer darzustellen, besteht darin, eine Anwendung zu schreiben, die es Benutzern ermöglicht, die verschiedenen Elemente anzuzeigen und mit Ihnen zu interagieren. Wenn die Daten jedoch als Ordner-/Dateihierarchie dargestellt werden können, sind viele der Funktionen, die Sie implementieren müssen, möglicherweise Benutzeroberflächen Dienste, die bereits von Windows Explorer bereitgestellt werden. Ein weitaus effizienterer Ansatz könnte darin bestehen, eine Namespace Erweiterung zu schreiben und Windows-Explorer zu ihrer GUI zu machen.

Um eine Namespace Erweiterung zu implementieren, müssen Ihre Informationen als Struktur strukturierter Namespace angeordnet werden. Der *Namespace* Stamm wird als virtueller Ordner im Shell-Namespace dargestellt. Der Stamm Ordner und alle zugehörigen Unterordner und Datenelemente werden Teil des Shell-Namespace, und Windows-Explorer wird zu Ihrer Benutzeroberfläche. Auf diese Weise können Sie die Informationen dem Benutzer in einer vertrauten und leicht zugänglichen Weise mit weniger Benutzeroberflächen Programmierung präsentieren, als dies für eine benutzerdefinierte Anwendung erforderlich wäre.

Eine Namespace Erweiterung besteht aus zwei grundlegenden Komponenten:

-   Ein Daten-Manager
-   Eine Schnittstelle zwischen dem Daten-Manager und Windows-Explorer

Die erste Komponente in der Liste ist vollständig auf dem neuesten Stand. Sie können Ihre Daten in einer beliebigen Weise speichern und verwalten. Die zweite Komponente ist der Code, der benötigt wird, um Ihre Daten als Ordner Objekte zu verpacken und die Interaktion mit Windows-Explorer zu verarbeiten. Windows-Explorer kann dann diese Objekte aufzurufen, damit Benutzer Ihre Daten anzeigen und mit ihnen interagieren können, als ob es sich um eine Sammlung von Ordnern und Dateien handelt. Die Ordner Objekte der Namespace Erweiterung müssen mit Windows-Explorer interagieren, als wären Sie normale Ordner. Bevor Sie versuchen, eine Namespace Erweiterung zu implementieren, müssen Sie zunächst verstehen, wie Windows Explorer ein Ordner Objekt behandelt.

## <a name="the-default-system-folder-view-object-defview"></a>Das Standard Objekt für die System Ordneransicht (defview)

Die Shell stellt eine Standard Implementierung der Ordneransicht bereit, die als defview bezeichnet wird, sodass Sie einen Großteil der Arbeit bei der Implementierung Ihrer eigenen Namespace Erweiterung vermeiden können. Da einige Ansichts Features nicht durch benutzerdefinierte Ansichten erreicht werden können, wird häufig empfohlen, anstelle einer benutzerdefinierten Ansicht das standardmäßige Systemordner-Ansichts Objekt zu verwenden. Weitere Informationen finden Sie unter [**shkreateshellfolderview**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview).

## <a name="how-windows-explorer-interacts-with-a-namespace-extension"></a>Interaktion von Windows-Explorer mit einer Namespace Erweiterung

Windows-Explorer bietet Benutzern eine GUI, mit der Sie eine Vielzahl von Aufgaben ausführen können, darunter:

-   [Navigieren](navigate.md) in der Namespace Hierarchie und Anzeigen des Inhalts von Ordnern.
-   [Verwalten](manage.md) des Inhalts des-Namespace durch verschieben, löschen und Kopieren von Objekten.
-   [Abrufen](folder-info.md) verschiedener Informationen zu-Objekten.
-   Anwendungen werden [gestartet](launch.md) .

Die Windows-Explorer-GUI verfügt über fünf grundlegende Komponenten. In der folgenden Abbildung werden die-Komponenten benannt und angezeigt, wo Sie in der Regel in Windows-Explorer angezeigt werden.

![Abbildung der Komponenten der Windows Explorer-Benutzeroberfläche ](images/nse1.png)

Wenn ein Benutzer einen Ordner anzeigt, der zu einer Namespace Erweiterung in Windows-Explorer gehört, hat das Ordner Objekt mindestens eine partielle Kontrolle über den Inhalt aller fünf Bereiche.

### <a name="tree-view"></a>Strukturansicht

Die Strukturansicht bietet eine allgemeine Übersicht über den-Namespace. Dieser Bereich hostet ein Struktur [Ansicht-Steuer](../controls/tree-view-controls.md) Element, mit dem jeder Namespace Ordner und die Position des Ordners in der Namespace Hierarchie angezeigt werden können. Ein Benutzer kann mit dem Struktur Ansichts Bereich mehrere Vorgänge ausführen, einschließlich:

-   Anzeigen oder Ausblenden der nächsten Ebene im Namespace.
-   Kopieren, verschieben oder Löschen von Ordnern.
-   Klicken Sie mit der rechten Maustaste auf einen Ordner, um ein Kontextmenü anzuzeigen.
-   Auswählen eines Ordners und anzeigen seiner Inhalte in der Ordneransicht.

Die Strukturansicht kommuniziert mit Ordner Objekten primär über Ihre [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle. Wenn ein Benutzer beispielsweise auf das Pluszeichen (+) neben dem Ordnersymbol klickt, erweitert Windows Explorer die Anzeige, um die Unterordner des Ordners anzuzeigen. Zum Abrufen der zum Aktualisieren der Strukturansicht benötigten Informationen führt die Shell mehrere Aufrufe an die **IShellFolder** -Schnittstelle des Ordner Objekts aus, um Folgendes zu erreichen:

-   Fordern Sie die Attribute des Ordners an.
-   Listet den Inhalt des Ordners auf.
-   Anzeigen Amen für jeden Unterordner anfordern.
-   Fordern Sie ein Symbol an, das neben den einzelnen Ordnern angezeigt werden soll.

Windows-Explorer aktualisiert dann die Strukturansicht, um die Unterordner des ausgewählten Ordners anzuzeigen. Wenn die Unterordner Unterordner aufweisen, wird neben dem zugehörigen Ordnersymbol das Zeichen "+" angezeigt. Es gibt eine Reihe von anspruchsvolleren Aufgaben, die ein Benutzer auch mit der Strukturansicht ausführen kann, einschließlich:

-   Verwenden der Zwischenablage zum Ausschneiden oder Kopieren eines Ordners und Einfügen in einen anderen Ordner.
-   Verwenden von Drag & amp; Drop zum Ausschneiden oder Kopieren eines Ordners und ablegen dieses Ordners in einem anderen Ordner.
-   Suchen nach Elementen in einem Ordner oder seinen Unterordnern mithilfe einer Suchmaschine.
-   Ändern der Ordnereigenschaften.

Eine ausführlichere Erläuterung dazu, wie eine Namespace Erweiterung diese Benutzeraktionen behandelt, finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](nse-implement.md).

### <a name="folder-view"></a>Ordneransicht

Wenn ein Benutzer einen Ordner auswählt, wird der Inhalt des Ordners in der Ordneransicht angezeigt. In gewissem Umfang überlappt sich die normale Funktionalität der Ordneransicht mit der Strukturansicht. Benutzer können Ordner verschieben oder kopieren, Ordnereigenschaften ändern, den Inhalt eines unter Ordners anzeigen, ein Kontextmenü für einen Ordner anzeigen usw. Es gibt jedoch einige Unterschiede zwischen Strukturansicht und Ordneransicht:

-   In der Ordneransicht wird nur der Inhalt eines einzelnen Ordners angezeigt, nicht der Teil der Namespace Hierarchie.
-   In der Ordneransicht werden Datei Objekte und Ordner Objekte angezeigt.
-   In der Ordneransicht können viel mehr Informationen zu Objekten als in der Strukturansicht angezeigt werden.
-   Mit der Ordneransicht können Namespace Erweiterungen fast ganz genau steuern, welche Informationen angezeigt werden und wie Sie angezeigt werden. Nur geringfügige Aspekte der Strukturansicht, z. b. Ordner Symbole, können geändert werden.

Anders als in der Strukturansicht wird der Inhalt der Ordneransicht von Windows-Explorer nicht direkt gesteuert. Die Ordneransicht ist ein Bereich, den Windows-Explorer für Ordner Objekte bereitstellt. Das anzeigen und Verwalten der Inhalte eines Ordners in der Ordneransicht liegt in der Verantwortung des Ordner Objekts. Obwohl die meisten Ordner Sichten ein Recht standardmäßiges Format aufweisen, gibt es einige Einschränkungen hinsichtlich der Art und Weise, wie Sie angezeigt werden können. Ein Extremfall ist der Internet Ordner, bei dem es sich um einen Browser mit vollem Funktionsumfang handelt.

Wenn ein Benutzer einen Ordner auswählt, der zu ihrer Namespace Erweiterung gehört, erstellen Sie ein Fenster und übergeben das zugehörige Handle an Windows Explorer. Dieses Fenster wird ein untergeordnetes Element des Fensters Ordneransicht. Windows-Explorer stellt die Dimensionen des Fensters "Ordneransicht" bereit, legt jedoch keine Einschränkungen für den Inhalt des untergeordneten Fensters. Sie können dann das untergeordnete Fenster verwenden, um die Ordneransicht des Ordners anzuzeigen.

Namespace Erweiterungen verwenden einen von zwei Ansätzen zum Erstellen einer Ordneransicht:

-   Verwenden Sie das untergeordnete Fenster zum Hosten eines [Listenansicht](../controls/list-view-control-reference.md) -Steuer Elements. Dieses Steuerelement ermöglicht es Ihnen, den Inhalt eines Ordners auf die gleiche Weise wie in der klassischen Windows-Explorer- [Ansicht](../lwef/web-view.md)anzuzeigen.
-   Verwenden Sie das untergeordnete Fenster, um ein [Webbrowser-Steuer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752044(v=vs.85)) Element zu hosten und ein dynamisches HTML-Dokument (DHTML) zu verwenden, um den Inhalt des Ordners anzuzeigen

Beide Ansätze zeigen eine Ordneransicht an, die in etwa so aussieht, wie Sie für Systemordner angezeigt wird. Wenn Sie jedoch ein anderes Anzeige Schema verwenden möchten, können Sie dies tun.

### <a name="menu-bar-and-toolbars"></a>Menüleiste und Symbolleisten

Wie die meisten Windows-Anwendungen stellt Windows Explorer dem Benutzer eine Reihe von Tools zur Verfügung. Eine komplette Auswahl von Tools ist über die Menüleiste verfügbar. Die häufig verwendeten Tools werden auch durch Schaltflächen oder Bearbeitungsfelder auf einer Symbolleiste dargestellt. Anders als bei vielen Windows-Anwendungen ist die Windows Explorer-Menüleiste ein Symbolleisten- [Steuer](../controls/toolbar-control-reference.md) Element, das so angepasst wurde, dass es wie ein herkömmliches Menü verhält. Sowohl die Menüleiste als auch die Symbolleiste werden in ein Grund leisten- [Steuer](../controls/rebar-control-reference.md) Element integriert, damit Benutzer die einzelnen Steuerelemente entsprechend Ihren Anforderungen organisieren können.

Standardmäßig unterstützt Windows-Explorer eine Standardgruppe von Schaltflächen und Menü Elementen, z. b. "Kopieren" und "Eigenschaften". Die-Namespace Erweiterung kann die Menüleiste und Symbolleisten anpassen, indem Standard Tools gelöscht und benutzerdefinierte Tools hinzugefügt werden. Wenn das Ordner Ansichts Objekt initialisiert wird, übergibt Windows-Explorer einen Zeiger auf seine [**ishellbrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) -Schnittstelle. Diese Schnittstelle unterstützt mehrere Methoden, die aufgerufen werden können, um die Menüleiste und die Symbolleiste anzupassen. Wenn der Benutzer eine benutzerdefinierte Menü-oder Symbolleisten Schaltfläche auswählt, leitet Windows-Explorer WM \_ -Befehls Meldungen für benutzerdefinierte Menü-und Symbolleisten Elemente an die Fenster Prozedur des untergeordneten Fensters weiter.

### <a name="status-bar"></a>Statusleiste

In der Windows-Explorer-Statusleiste werden Informationen zum aktuell ausgewählten Objekt angezeigt. Die-Namespace Erweiterung kann in der Statusleiste Statusinformationen anzeigen, z. b. eine Text Zeichenfolge. Sie können die Statusleiste anpassen, indem Sie [**ishellbrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser)aufrufen.

 

 
