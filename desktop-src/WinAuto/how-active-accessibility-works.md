---
title: Funktionsweise von Active Accessibility
description: Microsoft Active Accessibility ist so konzipiert, dass Hilfe Hilfen, so genannte Clients, mit standardmäßigen und benutzerdefinierten Benutzeroberflächen Elementen von anderen Anwendungen und dem Betriebssystem interagieren können.
ms.assetid: 29325f0a-c6ca-42b1-b85d-2671f7041034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdeffcebd96ffba804bfc24672bf867028e9b0c7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103857959"
---
# <a name="how-active-accessibility-works"></a>Funktionsweise von Active Accessibility

Microsoft Active Accessibility ist so konzipiert, dass Hilfe Hilfen, so genannte *Clients*, mit standardmäßigen und benutzerdefinierten Benutzeroberflächen Elementen von anderen Anwendungen und dem Betriebssystem interagieren können. Ein Microsoft Active Accessibility-Client ist ein beliebiges Programm, das Microsoft Active Accessibility verwendet, um auf die Benutzeroberflächen Elemente einer Anwendung zuzugreifen, Sie zu identifizieren oder zu bearbeiten. Zu den Clients gehören Barrierefreiheits Hilfen, automatisierte Testtools und einige computerbasierte Schulungs Anwendungen.

Bei Verwendung von Microsoft Active Accessibility kann eine Client Anwendung folgende Aktionen ausführen:

-   Abfrage nach Informationen beispielsweise über ein UI-Element an einer bestimmten Position.
-   Benachrichtigungen empfangen, wenn sich Informationen ändern beispielsweise, wenn ein Steuerelement ausgegraut wird oder wenn sich eine Text Zeichenfolge ändert.
-   Ausführen von Aktionen, die sich auf die Benutzeroberfläche oder den Dokumentinhalt auswirken; Klicken Sie z. b. auf eine Schaltfläche "Push", Dropdown Menü, und wählen Sie einen Menübefehl aus.

Die Anwendungen, die mit Informationen für Clients interagieren und Informationen bereitstellen, werden als *Server* bezeichnet. Ein Server verwendet Microsoft Active Accessibility, um Informationen zu seinen Benutzeroberflächen Elementen für Clients bereitzustellen. Alle Steuerelemente, Module oder Anwendungen, die Microsoft Active Accessibility verwenden, um Informationen über Ihre Benutzeroberfläche verfügbar zu machen, werden als Microsoft-Active Accessibility Server betrachtet. Server kommunizieren mit Clients, indem Ereignis Benachrichtigungen gesendet werden (z. b. der Aufruf von [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)) und auf Client Anforderungen für den Zugriff auf Benutzeroberflächen Elemente (z. b. das Verarbeiten von [**WM- \_ GetObject**](wm-getobject.md) -Nachrichten von [*oleacc*](uiauto-glossary.md)) Server machen Informationen über die Schnittstelle [**IAccessible verfügbar**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Bei Verwendung von Microsoft Active Accessibility kann eine Serveranwendung folgende Aktionen ausführen:

-   Stellen Sie Informationen über die benutzerdefinierten Benutzeroberflächen Objekte und den Inhalt der Client Fenster bereit.
-   Senden Sie Benachrichtigungen, wenn sich die Benutzeroberfläche ändert.

Beispielsweise muss ein sprach Erkennungs Programminformationen zu dieser Symbolleiste enthalten, damit ein Benutzer die Befehle auf einer benutzerdefinierten Word-Prozessor-Symbolleiste auf die gleiche Weise auswählen kann. Daher muss das Textverarbeitungs Tool diese Informationen verfügbar machen. Microsoft Active Accessibility bietet die Möglichkeit, dass das Textverarbeitungsprogramm Informationen über seine benutzerdefinierte Symbolleiste verfügbar macht und das sprach Erkennungs Programm diese Informationen erhält.

### <a name="client-applications-and-active-accessibility"></a>Client Anwendungen und Active Accessibility

Ein Microsoft Active Accessibility-Client muss benachrichtigt werden, wenn die Server Benutzeroberfläche geändert wurde, sodass diese Informationen an den Benutzer übermittelt werden können. Um sicherzustellen, dass der Client über Änderungen der Benutzeroberfläche informiert wird, verwendet er einen Mechanismus namens "Fenster Ereignisse" oder "WinEvents", um sich für den Empfang von Benachrichtigungen zu registrieren Weitere Informationen finden Sie unter [WinEvents](winevents-infrastructure.md).

Zum Erlernen und Bearbeiten eines bestimmten UI-Elements verwenden Clients die Microsoft Active Accessibility Component Object Model (com)-Schnittstelle ( [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)).

Ein Client kann ein [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt für ein UI-Element auf die folgenden vier Arten abrufen:

-   Aufrufen von [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) und übergeben des Fenster Handles des UI-Elements.
-   " [**Accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) " aufrufen und eine Bildschirmposition übergeben, die sich innerhalb des umgebenden Rechtecks des Benutzeroberflächen Elements befindet.
-   Legen Sie einen WinEvent-Hook fest, empfangen Sie eine Benachrichtigung, und rufen Sie [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) auf, um einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger für das UI-Element abzurufen, das das Ereignis generiert hat.
-   Rufen Sie eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methode auf, z. b. [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) oder [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) , um zu **einem anderen Objekt** zu wechseln

 

 




