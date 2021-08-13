---
title: IAccessible-Proxys
description: IAccessible-Proxys bieten Standardmäßige Barrierefreiheitsinformationen für Standardelemente der Benutzeroberfläche USER-Steuerelemente, BENUTZERmenüs und allgemeine Steuerelemente aus COMCTL und COMCTL32.
ms.assetid: 236c2064-de44-4021-8825-f1519312dbfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a416c29021aca0dd99356792ae96f6a77e137e8c0ca0c884ba941229dd4b83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566055"
---
# <a name="iaccessible-proxies"></a>IAccessible-Proxys

[**IAccessible-Proxys**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) bieten Standardmäßige Barrierefreiheitsinformationen für Standardelemente der Benutzeroberfläche: USER-Steuerelemente, BENUTZERmenüs und allgemeine Steuerelemente aus COMCTL und COMCTL32. Diese Standardunterstützung wird über **IAccessible-Objekte** verfügbar gemacht, die von Oleacc.dll erstellt wurden, und bietet Microsoft Active Accessibility Unterstützung ohne zusätzliche Serverentwicklung. Der Server kann dann die API für dynamische [Anmerkungen verwenden,](dynamic-annotation-api.md) um einen großen Teil der informationen zu ändern, die von Oleacc.dll verfügbar gemacht werden, hat jedoch keine vollständige Kontrolle.

## <a name="creating-a-proxy"></a>Erstellen eines Proxys

Um zu bestimmen, ob ein Benutzeroberflächenelement die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativ unterstützt, sendet Oleacc.dll [**eine WM \_ GETOBJECT-Nachricht.**](wm-getobject.md) Ein Rückgabewert ungleich 0 (null) bedeutet, dass das Element Microsoft Active Accessibility unterstützt und eine eigene **IAccessible-Unterstützung** bietet. Wenn der Rückgabewert jedoch 0 (null) ist, stellt Oleacc.dll ein Proxyobjekt für das Benutzeroberflächenelement zur Verfügung und versucht, aussagekräftige Informationen in seinem Namen zurück zu geben. Weitere Informationen zu **WM \_ GETOBJECT finden Sie** unter Funktionsweise von WM [ \_ GETOBJECT.](how-wm-getobject-works.md)

## <a name="what-information-is-exposed"></a>Welche Informationen werden verfügbar gemacht?

Oleacc.dll verwendet den Namen der Windows-Klasse des Benutzeroberflächenelements, um zu bestimmen, welche Informationen für die einzelnen [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) verfügbar gemacht werden sollen und wie diese Informationen gesammelt werden sollen. Beispielsweise ruft Oleacc.dll die [**GetWindowText-Funktion**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) auf, um die [**Name-Eigenschaft**](name-property.md) für eine Standard-Pushschaltfläche abzurufen, ruft jedoch dieselbe Funktion auf, um die [**Value-Eigenschaft**](value-property.md) für ein Standardbearbeitungssteuerfeld abzurufen. Tatsächlich wird Oleacc.dll **IAccessible-Methode** einer entsprechenden Microsoft Win32- oder steuerelementspezifischen Nachricht oder einem funktionsspezifischen Aufruf zuordnen. Durch die Verwendung dieser speziellen, auf Klassennamen basierenden Casing-Klasse kann sie aussagekräftige Informationen über **IAccessible-Proxys** zurückgeben, ohne dass Microsoft Active Accessibility serverseitige Unterstützung bietet.

Anwendungen, die mit standardmäßigen Benutzeroberflächenelementen erstellt wurden, erhalten in der Microsoft Active Accessibility unterstützung ohne zusätzliche Entwicklungsarbeit. Die Ausnahmen von dieser Regel sind Steuerelemente, die untergliedert wurden, die keine eigenen Zeichenfolgen speichern (Fehlen des **HASSTRINGS-Stils)** oder vom Besitzer gezeichnet werden. In diesen Fällen kann Oleacc.dll die benötigten Informationen nicht erfassen, da die Informationen außerhalb des Steuerelements gespeichert werden. In vielen dieser Szenarien ermöglichen eingerichtete Problemumgehungen oder die Verwendung der dynamischen Anmerkung jedoch, dass der Server mit den proxys zusammenarbeiten kann, die von Oleacc.dll.

## <a name="generic-proxy-objects"></a>Generische Proxyobjekte

Wenn Oleacc.dll klassennamen des Benutzeroberflächenelements nicht erkennt, wird ein generischer Proxy erstellt, der so viele Informationen wie möglich verfügbar macht. Dies schließt das umgebundene Rechteck des Objekts, das übergeordnete Objekt, den Namen (aus [**WM \_ GETTEXT)**](/windows/desktop/winmsg/wm-gettext)und alle übergeordneten Objekte in der Fensterhierarchie ein.

 

 