---
title: Cursor (MSAA UI-Element Referenz)
description: Ein Cursor ist ein kleines Bild, dessen Position auf dem Bildschirm von einem Zeigegerät gesteuert wird, z. b. mit einer Maus, einem Stift oder einem Trackball. Wenn der Benutzer das Zeigegerät bewegt, verschiebt das Windows-Betriebssystem den Cursor.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309467"
---
# <a name="cursor-msaa-ui-element-reference"></a>Cursor (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden die Cursor für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Die Verwendung von Cursorn in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein Cursor ist ein kleines Bild, dessen Position auf dem Bildschirm von einem Zeigegerät gesteuert wird, z. b. mit einer Maus, einem Stift oder einem Trackball. Wenn der Benutzer das Zeigegerät bewegt, verschiebt das Windows-Betriebssystem den Cursor.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Cursor unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Cursor unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)– die **childCount** -Eigenschaft ist 0 (null).
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– Entwickler können benutzerdefinierte Cursor erstellen oder die vordefinierten Cursor verwenden, die mit ihrer Cursor-ID identifiziert werden. Die **Name** -Eigenschaft des Cursors hängt von ihrer Form ab und ist einer der folgenden: 

    | Cursorform     | Name              |
    |------------------|-------------------|
    | Benutzerdefinierter Cursor    | Unbekannter         |
    | IDC- \_ Pfeil       | "Normal"          |
    | IDC- \_ IBeam       | Bearbeiten            |
    | IDC- \_ Wartezeit        | Warten            |
    | IDC- \_ Kreuz       | Biografischen         |
    | IDC- \_ upartrow     | Gegründet              |
    | IDC \_ sizenwse    | "NWSE size"       |
    | IDC \_ sizenesw    | "Größe der Größe"       |
    | IDC \_ SizeWE      | "Horizontale Größe" |
    | IDC- \_ SizeNS      | "Vertikale Größe"   |
    | IDC \_ SizeAll     | Voranschreiten            |
    | IDC- \_ Nr.          | Tener       |
    | IDC- \_ AppStarting | "App-Start"       |
    | IDC- \_ Hilfe        | Hilft            |

    

     

-   [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– die **Role** -Eigenschaft ist ein [**Rollen System- \_ \_ Cursor**](object-roles.md).
-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)– die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md):

    [**Status \_ System \_ unsichtbar**](object-state-constants.md) - \| [ **Zustands \_ System \_** ist nicht verankert](object-state-constants.md)

## <a name="notes"></a>Notizen

-   Anders als andere Elemente der Benutzeroberfläche verfügt das Cursor Objekt nicht über ein zugeordnetes Fenster handle. Um Zugriff auf das Cursor Objekt zu erhalten, müssen Clients ein [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) festlegen und darauf warten, dass das Cursor Objekt Ereignisse generiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




