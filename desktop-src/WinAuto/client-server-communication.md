---
title: Client-/Serverkommunikation
description: Mit dem WinEvents-Mechanismus können Server problemlos mit Microsoft Active Accessibility Clients kommunizieren.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896b6f6688e0e2929ebb351fe9d7cc210803768a8031faa44a8aca8127b12002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133933"
---
# <a name="clientserver-communication"></a>Client-/Serverkommunikation

Mit dem [WinEvents-Mechanismus](winevents-overview.md) können Server problemlos mit Microsoft Active Accessibility Clients kommunizieren. Clients sammeln Häufig Informationen, indem sie auf WinEvents reagieren (z. B. nach dem Fokus), aber sie können jederzeit Informationen von einem Server anfordern.

Um Informationen für ein barrierefreies Objekt anzufordern, das ein WinEvent generiert, muss ein Client das Ereignis verarbeiten und eine Verbindung mit dem relevanten barrierefreien Objekt herstellen. Hierzu führt der Client die folgenden sechs Schritte aus:

-   Ein Server ruft [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) auf, um eine WinEvent-Benachrichtigung für jede Änderung seiner Benutzeroberflächenelemente zu generieren.
-   Der WinEvent-Verwaltungscode in USER bestimmt, ob Clientanwendungen eine [*WinEvent-Hookfunktion*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) mit [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) registriert haben, und ruft die registrierte Rückruffunktion auf.
-   In seiner Rückruffunktion fordert der Client Zugriff auf das Objekt an, das das Ereignis generiert hat, indem [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) oder andere funktionen zum Abrufen barrierefreier Objekte aufgerufen werden. Weitere Informationen finden Sie unter [Abrufen eines IAccessible-Objekts.](retrieving-an-iaccessible-object.md)
-   Diese Microsoft Active Accessibility-API sendet der Serveranwendung eine [**WM \_ GETOBJECT-Nachricht,**](wm-getobject.md) um das barrierefreie Objekt abzurufen.
-   Als Antwort auf [**WM \_ GETOBJECT**](wm-getobject.md)gibt die Serveranwendung entweder 0 (null) oder einen Wert zurück, der als einmaliger Verweis auf das Objekt fungiert, das das Ereignis generiert hat.
-   Wenn der Server 0 (null) zurückgibt, erstellt Microsoft Active Accessibility ein Proxyobjekt und gibt dessen Adresse an den Client weiter. Andernfalls verwendet Microsoft Active Accessibility diesen Verweis, um die Adresse einer Objektschnittstelle wie [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) oder [**IDispatch**](idispatch-interface.md)abzurufen, und gibt diese Adresse an den Client weiter.

Sobald der Client über eine Schnittstellenadresse verfügt, kann er die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Methoden des barrierefreien Objekts aufrufen, um Informationen abzurufen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [WinEvents und Active Accessibility](winevents-overview.md)
-   [Funktionsweise von WM \_ GETOBJECT](how-wm-getobject-works.md)
-   [Abrufen eines IAccessible-Objekts](retrieving-an-iaccessible-object.md)

 

 




