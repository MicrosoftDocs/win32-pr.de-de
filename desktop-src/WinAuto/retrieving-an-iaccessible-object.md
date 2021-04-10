---
title: Abrufen eines IAccessible-Objekts
description: Microsoft Active Accessibility bietet Funktionen wie accessibleobjectfromwindow und accessibleobjectfrompoint, mit denen Clients barrierefreie Objekte abrufen können.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309436"
---
# <a name="retrieving-an-iaccessible-object"></a>Abrufen eines IAccessible-Objekts

Microsoft Active Accessibility bietet Funktionen wie [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) und [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) , mit denen Clients barrierefreie Objekte abrufen können. Diese Funktionen geben entweder einen [**IDispatch**](idispatch-interface.md) -oder [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger zurück, über den Clients Informationen über das barrierefreie Objekt erhalten.

Wenn ein Client [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) oder eine der anderen **accessibleobjectfrom * * * X* -Funktionen aufruft, die eine Schnittstelle zu einem Objekt abrufen, sendet Microsoft Active Accessibility die [**WM- \_ GetObject**](wm-getobject.md) -Fenster Meldung an die entsprechende Fenster Prozedur innerhalb der entsprechenden Anwendung. Zum Bereitstellen von Informationen für Clients müssen Server auf die **WM- \_ GetObject** -Nachricht antworten.

Um bestimmte Informationen über ein UI-Element zu erfassen, müssen Clients zuerst eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das Element abrufen. Um das **IAccessible** -Objekt eines Elements abzurufen, können Clients eine der folgenden Funktionen verwenden:

-   [**Accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**Accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**Accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

**So rufen Sie einen IAccessible-Schnittstellen Zeiger ab**

1.  Client ruft eine der **accessibleobjectfrom * * * X* -Funktionen auf.
2.  Oleacc.dll sendet eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht an den Server.
3.  Der Server bestimmt, welches Benutzeroberflächen Element der Anforderung entspricht.
4.  Der Server gibt entweder 0 (null) zurück, um einen Oleacc.dll Proxy anzufordern.

    oder

    Gibt ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt (Native Implementierung) zurück. Gehen Sie dazu wie folgt vor:

    -   Erstellt ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt für das-Element.
    -   Ruft [**lresultfromujekt**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) auf, um den Zeiger des Objekts zu Mars Hallen.
    -   Gibt das LRESULT an Oleacc.dll zurück.

5.  Oleacc.dll überprüft den Rückgabewert von [**WM \_ GetObject**](wm-getobject.md).

    Wenn Sie 0 (null) ist, wird Oleacc.dll ein Proxy Objekt erstellt und an den Client zurückgegeben.

    oder

    Wenn der Wert ungleich NULL ist, wird von Oleacc.dll [**objectfromlresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) aufgerufen, um das Marshalling des systemeigenen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt Zeigers aufzurufen und an den Client zurückgegeben.

 

 




