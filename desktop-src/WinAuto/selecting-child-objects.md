---
title: Auswählen von untergeordneten Objekten
description: Clients rufen die IAccessible accSelect-Methode auf, um die Auswahl oder den Tastaturfokus unter den in einem -Objekt vorhandenen -Objekten zu ändern. Die mit dem Aufruf angegebenen SELFLAG-Konstanten definieren den durchzuführenden Vorgang.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc15ab48a42be44c62c8c7bc2b9151158875509a2e43010c5da70830b2f2973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133683"
---
# <a name="selecting-child-objects"></a>Auswählen von untergeordneten Objekten

Clients rufen die [**IAccessible::accSelect-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) auf, um die Auswahl oder den Tastaturfokus zwischen den in einem -Objekt vorhandenen unteren Objekten zu ändern. Die [mit dem Aufruf angegebenen SELFLAG-Konstanten](selflag.md) definieren den durchzuführenden Vorgang.

Wenn [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) mit dem [**SELFLAG \_ TAKEFOCUS-Flag**](selflag.md) für ein untergeordnetes Objekt aufgerufen wird, das über ein **HWND** verfügt, wird das Flag nur wirksam, wenn das übergeordnete Element des Objekts den Fokus besitzt.

## <a name="performing-complex-selection-operations"></a>Ausführen komplexer Auswahlvorgänge

Im Folgenden wird beschrieben, welche SELFLAG-Werte beim Aufrufen von [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) angegeben werden müssen, um komplexe Auswahlvorgänge durchzuführen.

**So simulieren Sie einen Klick**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)

**So wählen Sie ein Zielelement aus, indem Sie STRG+Klick simulieren**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)

**So brechen Sie die Auswahl eines Zielelements ab, indem Sie STRG+Klick simulieren**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)

**So simulieren Sie UMSCHALT+Klick**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)

**So wählen Sie einen Bereich von Objekten aus und legen den Fokus auf das letzte Objekt**

1.  Geben [**Sie SELFLAG \_ TAKEFOCUS für**](selflag.md) das Startobjekt an, um den Auswahlanker festzulegen.
2.  Rufen [**Sie IAccessible::accSelect erneut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) auf, und geben Sie [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) für das letzte Objekt an.

**So deaktivieren Sie alle Objekte**

1.  Geben [**Sie SELFLAG \_ TAKESELECTION für**](selflag.md) ein beliebiges Objekt an. Dieses Flag deaktiviert alle ausgewählten Objekte außer dem soeben ausgewählten.
2.  Rufen [**Sie IAccessible::accSelect erneut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) auf, und geben Sie [**SELFLAG \_ REMOVESELECTION**](selflag.md) für das verbleibende Objekt an.

 

 




