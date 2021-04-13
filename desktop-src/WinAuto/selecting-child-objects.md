---
title: Auswählen von untergeordneten Objekten
description: Clients wenden die Methode IAccessible accSelect an, um die Auswahl oder den Tastaturfokus unter den untergeordneten Elementen eines Objekts zu ändern. Die mit dem-Befehl angegebenen selflag-Konstanten definieren den auszuführenden Vorgang.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309496"
---
# <a name="selecting-child-objects"></a>Auswählen von untergeordneten Objekten

Clients wird die [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) -Methode aufgerufen, um die Auswahl oder den Tastaturfokus unter den untergeordneten Elementen eines Objekts zu ändern. Die mit dem-Befehl angegebenen [selflag-Konstanten](selflag.md) definieren den auszuführenden Vorgang.

Wenn [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) mit dem [**selflag-Flag \_ TakeFocus**](selflag.md) für ein untergeordnetes Objekt mit einem **HWND** aufgerufen wird, wird das Flag nur wirksam, wenn das übergeordnete Objekt den Fokus besitzt.

## <a name="performing-complex-selection-operations"></a>Ausführen komplexer Auswahl Vorgänge

Im folgenden wird beschrieben, welche selflag-Werte beim Aufrufen von [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) angegeben werden, um komplexe Auswahl Vorgänge auszuführen.

**So simulieren Sie einen Klick**

-   [**Selflag \_ "TakeFocus**](selflag.md) \| [ **selflag \_ TakeSelection** "](selflag.md)

**So wählen Sie ein Ziel Element durch Simulieren von Strg + Klick aus**

-   [**Selflag \_ Start Fokus**](selflag.md) \| [ **selflag \_ AddSelection**](selflag.md)

**So brechen Sie die Auswahl eines Ziel Elements durch Simulieren von Strg + Klick ab**

-   [**Selflag \_ Start Fokus**](selflag.md) \| [ **selflag \_ RemoveSelection**](selflag.md)

**So simulieren Sie Umschalt + Klick**

-   [**Selflag \_ "TakeFocus**](selflag.md) \| [ **selflag \_ ExtendSelection** "](selflag.md)

**So wählen Sie einen Bereich von Objekten aus und legen den Fokus auf das letzte Objekt**

1.  Geben Sie [**selflag \_ TakeFocus**](selflag.md) für das Start Objekt an, um den Auswahl Anker festzulegen.
2.  Nennen [**Sie IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) erneut, und geben Sie [**selflag \_ ExtendSelection**](selflag.md) \| [**selflag \_ TakeFocus**](selflag.md) für das letzte Objekt an.

**So deaktivieren Sie alle Objekte**

1.  Geben Sie [**selflag \_ TakeSelection**](selflag.md) für ein beliebiges Objekt an. Mit diesem Flag werden alle ausgewählten Objekte außer der gerade ausgewählten Objekte deaktiviert.
2.  Nennen [**Sie IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) erneut, und geben Sie [**selflag \_ RemoveSelection**](selflag.md) für das restliche Objekt an.

 

 




