---
title: Verwenden von OBJID \_ NATIVEOM zum Verfügbar machen einer nativen Schnittstelle für ein Fenster
description: Mit dieser Technik können Clients ein benutzerdefiniertes Objekt für ein Fenster erhalten. Server können damit einen Zeiger auf ein benutzerdefiniertes Dokumentobjekt für ein Fenster verfügbar machen.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed99db4641235ceee57688865710c19a41f0a517d70d4601d138150cb88dd470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098090"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a>Verwenden von OBJID \_ NATIVEOM zum Verfügbar machen einer nativen Schnittstelle für ein Fenster

Mit dieser Technik können Clients ein benutzerdefiniertes Objekt für ein Fenster erhalten. Server können damit einen Zeiger auf ein benutzerdefiniertes Dokumentobjekt für ein Fenster verfügbar machen.

**So machen Sie eine systemeigene Objektmodellschnittstelle für ein Fenster (Server) verfügbar**

1.  Behandeln Sie die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) in der Fensterprozedur. Wenn der *lParam-Wert* [**OBJID \_ NATIVEOM ist,**](object-identifiers.md)geben Sie mithilfe von [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)einen Schnittstellenzeiger auf das benutzerdefinierte Objekt zurück.
2.  Geben Sie den Schnittstellenzeiger nach dem Aufruf [**von LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)frei, falls zutreffend. Weitere Informationen finden Sie unter **LresultFromObject**.

Clients können einen Zeiger auf dieses benutzerdefinierte Objekt abrufen.

**So erhalten Sie einen Zeiger für ein benutzerdefiniertes Objekt für ein Fenster (Clients)**

-   Rufen Sie [**AccessibleObjectFromWindow auf,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) und übergeben [**Sie OBJID \_ NATIVEOM**](object-identifiers.md) als zweiten Parameter.

Beachten Sie die folgenden Probleme bei dieser Technik:

-   Diese Technik ähnelt der [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Rückgabe eines IAccessible-Schnittstellenzeigers, mit Ausnahme der verwendeten Objekt-ID und der Tatsache, dass [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) anstelle von IAccessible ein benutzerdefiniertes **Objekt zurückgibt.**
-   Serverentwickler müssen möglicherweise Informationen veröffentlichen, die es Clients ermöglichen, das **HWND** eindeutig zu identifizieren, damit sie es finden können, bevor [**sie AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) auf seinem Fensterhand handle aufrufen.
-   Implementieren Sie die [**IAccessible-Schnittstelle nicht**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für das zurückgegebene benutzerdefinierte Objekt. Wenn Sie dies tun, behandelt OLEACC dies als **IAccessible-Standard** und verhindert möglicherweise die Verwendung der benutzerdefinierten Schnittstellen.
-   Damit die Schnittstellen für das zurückgegebene Objekt prozessübergreifend verwendet werden können, müssen sie möglicherweise bei Component Object Model (COM) registriert werden.

Diese Technik wird von mehreren Komponenten Microsoft Office unterstützt. Weitere Informationen finden Sie unter [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

 

 




