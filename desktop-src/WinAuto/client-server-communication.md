---
title: Client/Server-Kommunikation
description: Mit dem WinEvents-Mechanismus können Server problemlos mit Microsoft Active Accessibility-Clients kommunizieren.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "106341910"
---
# <a name="clientserver-communication"></a>Client/Server-Kommunikation

Mit dem [WinEvents](winevents-overview.md) -Mechanismus können Server problemlos mit Microsoft Active Accessibility-Clients kommunizieren. Clients erfassen häufig Informationen, indem Sie auf WinEvents (z. b. den folgenden Fokus) reagieren, aber Sie können jederzeit jederzeit Informationen von einem Server anfordern.

Um Informationen für ein Barrierefreies Objekt anzufordern, das ein WinEvent generiert, muss ein Client das Ereignis verarbeiten und eine Verbindung mit dem entsprechenden zugänglichen Objekt herstellen. Zu diesem Zweck führt der Client die folgenden sechs Schritte aus:

-   Ein Server ruft [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) auf, um eine WinEvent-Benachrichtigung für jede Änderung an den Benutzeroberflächen Elementen zu generieren.
-   Der WinEvent Management-Code im Benutzer bestimmt, ob Client Anwendungen eine WinEvent- [*Hook-Funktion*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) mithilfe von [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) registriert haben und die registrierte Rückruffunktion aufrufen.
-   In der Rückruffunktion fordert der Client den Zugriff auf das Objekt an, das das Ereignis generiert hat, indem er [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) oder andere barrierefreie Objekt Abruf Funktionen aufruft. Weitere Informationen finden Sie unter [Abrufen eines IAccessible-Objekts](retrieving-an-iaccessible-object.md).
-   Diese Microsoft Active Accessibility-API sendet der Serveranwendung eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht, um das barrierefreie Objekt abzurufen.
-   Als Antwort auf [**WM \_ GetObject**](wm-getobject.md)gibt die Serveranwendung entweder NULL zurück oder gibt einen Wert zurück, der als einmalige Referenz zu dem Objekt fungiert, das das Ereignis generiert hat.
-   Wenn der Server NULL zurückgibt, erstellt Microsoft Active Accessibility ein Proxy Objekt und übergibt seine Adresse an den Client. Andernfalls verwendet Microsoft Active Accessibility diese Referenz, um die Adresse einer Objektschnittstelle (z. b. [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) oder [**IDispatch**](idispatch-interface.md)) abzurufen, und gibt diese Adresse an den Client weiter.

Wenn der Client über eine Schnittstellen Adresse verfügt, kann er die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften und-Methoden des barrierefreien Objekts aufrufen, um Informationen abzurufen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [WinEvents und Active Accessibility](winevents-overview.md)
-   [Funktionsweise von WM- \_ GetObject](how-wm-getobject-works.md)
-   [Abrufen eines IAccessible-Objekts](retrieving-an-iaccessible-object.md)

 

 




