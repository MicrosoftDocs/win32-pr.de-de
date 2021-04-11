---
title: Funktionsweise von WM_GETOBJECT
description: Microsoft Active Accessibility sendet die WM- \_ GetObject-Nachricht an die entsprechende Serveranwendung, wenn ein Client eine der accessibleobjectfromx-Funktionen aufruft.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe287bca68c925cb7be95ff52d2dac547ed097
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315284"
---
# <a name="how-wm_getobject-works"></a>Funktionsweise von WM- \_ GetObject

Microsoft Active Accessibility sendet die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht an die entsprechende Serveranwendung, wenn ein Client eine der **accessibleobjectfrom * * * X* -Funktionen aufruft. In der folgenden Liste werden die verschiedenen Szenarien beschrieben, die auftreten:

-   Wenn das Fenster oder Steuerelement, das das WM-Element empfängt, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert, gibt das Fenster mithilfe von [**\_**](wm-getobject.md) [**lresultfromubject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)einen Verweis auf die **IAccessible** -Schnittstelle zurück. Microsoft Active Accessibility führt in Verbindung mit der Component Object Model (com)-Bibliothek das entsprechende Marshalling durch und übergibt den Schnittstellen Zeiger vom Server an den Client zurück.
-   Wenn das Fenster, das die Nachricht empfängt, nicht [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert, sollte es 0 (null) zurückgeben.
-   Wenn das Fenster die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht nicht verarbeitet, gibt die [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion 0 (null) zurück.

Auch wenn der Server NULL zurückgibt, stellt Microsoft Active Accessibility dem Client weiterhin Informationen über das Objekt zur Verfügung. Für die meisten vom System bereitgestellten Objekte (z. b. Listenfelder und Schaltflächen) stellt Microsoft Active Accessibility umfassende Informationen bereit. bei anderen Objekten sind die Informationen eingeschränkt. Beispielsweise stellt Microsoft Active Accessibility keine Informationen für Steuerelemente bereit, die nicht über ein Fenster Handle verfügen. Microsoft Active Accessibility gibt einen über die Schnittstelle [**zugänglichen ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger zurück, den der Client verwendet, um Informationen über das Objekt zu erhalten.

Weitere Informationen finden Sie in [der WM- \_ GetObject-Nachricht](the-wm-getobject-message.md).

 

 