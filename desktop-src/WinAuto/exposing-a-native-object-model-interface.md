---
title: Verfügbar machen einer systemeigenen Objektmodell Schnittstelle
description: Wenn ein Benutzeroberflächen Element ein anderes System eigenes Objektmodell als Microsoft Active Accessibility oder eine Benutzeroberflächen Automatisierung unterstützt, kann es die benutzerdefinierte Schnittstelle verfügbar machen, indem auf die WM- \_ GetObject-Nachrichten reagiert wird, die den objID \_ nativeom-Objekt
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037192"
---
# <a name="exposing-a-native-object-model-interface"></a><span data-ttu-id="e7aab-103">Verfügbar machen einer systemeigenen Objektmodell Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e7aab-103">Exposing a Native Object Model Interface</span></span>

<span data-ttu-id="e7aab-104">Wenn ein Benutzeroberflächen Element ein anderes System eigenes Objektmodell als Microsoft Active Accessibility oder eine Benutzeroberflächen Automatisierung unterstützt, kann es die benutzerdefinierte Schnittstelle verfügbar machen, indem auf die [**WM- \_ GetObject**](wm-getobject.md) -Nachrichten reagiert wird, die den [**objID \_ nativeom**](object-identifiers.md) -Objekt</span><span class="sxs-lookup"><span data-stu-id="e7aab-104">If a UI element supports a native object model other than Microsoft Active Accessibility or UI Automation, it can expose the custom interface by responding to [**WM\_GETOBJECT**](wm-getobject.md) messages that include the [**OBJID\_NATIVEOM**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="e7aab-105">Um zu reagieren, sollte das UI-Element den Wert zurückgeben, der durch einen aufgerufenen der [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e7aab-105">To respond, the UI element should return the value retrieved by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

<span data-ttu-id="e7aab-106">Ein Client kann eine Schnittstelle von einem Benutzeroberflächen Element abrufen, das ein System eigenes Objektmodell unterstützt, indem die [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) -Funktion aufgerufen und [**objID \_ nativeom**](object-identifiers.md) als zweiter Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e7aab-106">A client can retrieve an interface from a UI element that supports a native object model by calling the [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) function and specifying [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

 

 




