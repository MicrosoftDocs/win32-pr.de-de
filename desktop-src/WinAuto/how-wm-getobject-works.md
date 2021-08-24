---
title: Funktionsweise WM_GETOBJECT
description: Microsoft Active Accessibility sendet die WM GETOBJECT-Nachricht an die entsprechende Serveranwendung, wenn ein Client eine der \_ AccessibleObjectFromX-Funktionen aufruft.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24309b304baede0c7b93c9e609b469991e737ca819e8014effa03a4f39b8772c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795760"
---
# <a name="how-wm_getobject-works"></a>Funktionsweise von WM \_ GETOBJECT

Microsoft Active Accessibility sendet die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) an die entsprechende Serveranwendung, wenn ein Client eine der **AccessibleObjectFrom X-Funktionen**_aufruft._ In der folgenden Liste werden die verschiedenen Szenarien beschrieben, die auftreten:

-   Wenn das Fenster oder Steuerelement, das [**WM \_ GETOBJECT**](wm-getobject.md) empfängt, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert, gibt das Fenster mithilfe von [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)einen Verweis auf die **IAccessible-Schnittstelle** zurück. Microsoft Active Accessibility führt in Verbindung mit der Component Object Model-Bibliothek (COM) das entsprechende Marshalling aus und übergibt den Schnittstellenzeiger vom Server zurück an den Client.
-   Wenn das Fenster, das die Nachricht empfängt, IAccessible nicht [**implementiert,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)sollte 0 (null) zurückgeben.
-   Wenn das Fenster die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) nicht behandelt, gibt die [DefWindowProc-Funktion](/windows/win32/api/winuser/nf-winuser-defwindowproca) 0 (null) zurück.

Auch wenn der Server null zurückgibt, Microsoft Active Accessibility dem Client weiterhin Informationen zum Objekt zur Verfügung. Für die meisten vom System bereitgestellten Objekte, z. B. Listenfelder und Schaltflächen, Microsoft Active Accessibility vollständige Informationen. für andere Objekte sind die Informationen begrenzt. Beispielsweise stellt Microsoft Active Accessibility keine Informationen für Steuerelemente zur Verfügung, die kein Fensterhand handle haben. Microsoft Active Accessibility gibt einen [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zurück, mit dem der Client Informationen zum Objekt angibt.

Weitere Informationen finden Sie unter [The WM \_ GETOBJECT Message](the-wm-getobject-message.md).

 

 