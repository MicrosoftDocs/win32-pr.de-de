---
title: Clientrichtlinien
description: Cliententwickler sollten die folgenden Funktionen verwenden, um Informationen zu den Elementen der Benutzeroberfläche abzurufen.
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3cfa9a269d796d7071b2107bba2fde6717f42928b9c9dc8074f94afbdbe15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133943"
---
# <a name="client-guidelines"></a>Clientrichtlinien

Cliententwickler sollten die folgenden Funktionen verwenden, um Informationen zu den Elementen der Benutzeroberfläche abzurufen:

-   Um eine [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für Objekte abzurufen, rufen [**Sie AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)auf.
-   Verwenden Sie die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Methoden, um barrierefreie Objekte zu untersuchen und zu bearbeiten.
-   Um [WinEvents](winevents-overview.md)zu empfangen, rufen [**Sie SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) auf, um eine WinEvent-Rückruffunktion für die Ereignisse zu registrieren, die für die Clientanwendung relevant sind.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Abrufen untergeordneter IDs durch Clients](how-clients-obtain-child-ids.md)

 

 




