---
title: Verwenden Sie objID \_ nativeom, um eine native Schnittstelle für ein Fenster verfügbar zu machen.
description: Diese Technik ermöglicht es Clients, ein benutzerdefiniertes-Objekt für ein Fenster zu erhalten. -Server können diese verwenden, um einen Zeiger auf ein benutzerdefiniertes Dokument Objekt für ein Fenster verfügbar zu machen.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2c5c6ec194ca643475444feb5839c02d3fa890
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104389469"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a>Verwenden Sie objID \_ nativeom, um eine native Schnittstelle für ein Fenster verfügbar zu machen.

Diese Technik ermöglicht es Clients, ein benutzerdefiniertes-Objekt für ein Fenster zu erhalten. -Server können diese verwenden, um einen Zeiger auf ein benutzerdefiniertes Dokument Objekt für ein Fenster verfügbar zu machen.

**So machen Sie eine systemeigene Objektmodell Schnittstelle für ein Fenster (Server) verfügbar**

1.  Behandelt die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht in der Fenster Prozedur. Wenn der *LPARAM* -Wert " [**objID \_ nativeom**](object-identifiers.md)" ist, geben Sie einen Schnittstellen Zeiger auf das benutzerdefinierte Objekt mithilfe von " [**lresultfrofubject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)" zurück.
2.  Geben Sie ggf. den Schnittstellen Zeiger nach dem Aufrufen von [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)frei. Weitere Informationen finden Sie unter **lresultfrobugbject**.

Clients können einen Zeiger auf dieses benutzerdefinierte Objekt abrufen.

**So rufen Sie einen Zeiger für ein benutzerdefiniertes Objekt für ein Fenster (Clients) ab**

-   Aufrufen von [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) und übergeben von [**objID \_ nativeom**](object-identifiers.md) als zweiten Parameter.

Beachten Sie die folgenden Probleme bei dieser Technik:

-   Diese Vorgehensweise ähnelt der Rückgabe eines [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeigers, außer der verwendeten Objekt-ID und der Tatsache, dass [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) anstelle von **IAccessible** ein benutzerdefiniertes Objekt zurückgibt.
-   Server Entwickler müssen möglicherweise Informationen veröffentlichen, die es Clients ermöglichen, das **HWND** eindeutig zu identifizieren, damit Sie es finden, bevor Sie [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) auf dem zugehörigen Fenster Handle aufrufen.
-   Implementieren Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle nicht für das benutzerdefinierte Objekt, das zurückgegeben wird. Wenn Sie dies tun, behandelt oleacc es als Standard- **IAccessible** und kann verhindern, dass die benutzerdefinierten Schnittstellen verwendet werden.
-   Um Prozess übergreifend verwendet zu werden, müssen die Schnittstellen des zurückgegebenen Objekts möglicherweise bei Component Object Model (com) registriert werden.

Diese Technik wird von mehreren Microsoft Office Komponenten unterstützt. Weitere Informationen finden Sie unter [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

 

 




