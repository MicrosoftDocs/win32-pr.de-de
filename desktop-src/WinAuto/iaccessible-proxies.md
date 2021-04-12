---
title: Ibarrierefreie Proxys
description: Ibarrierefreie-Proxys bieten standardmäßige Barrierefreiheits Informationen für Benutzer Steuerelemente der Standardbenutzer Oberfläche, Benutzermenüs und allgemeine Steuerelemente von COMCTL und Comctl32.
ms.assetid: 236c2064-de44-4021-8825-f1519312dbfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dcb4cae8980e4003d9915c6783e4ddb043a8c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315675"
---
# <a name="iaccessible-proxies"></a>Ibarrierefreie Proxys

[**Ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Proxys bieten standardmäßige Barrierefreiheits Informationen für Standardbenutzer Oberflächen Elemente: Benutzer Steuerelemente, Benutzermenüs und allgemeine Steuerelemente von COMCTL und Comctl32. Diese Standardunterstützung wird durch **ibarrierefreie Objekte verfügbar** gemacht, die von Oleacc.dll erstellt wurden, und bietet Microsoft Active Accessibility Support ohne zusätzliche Server Entwicklungsarbeiten. Der Server kann dann mithilfe der [dynamischen Annotation-API](dynamic-annotation-api.md) einen Großteil der von Oleacc.dll verfügbar gemachten Informationen ändern, verfügt jedoch nicht über die komplette Kontrolle.

## <a name="creating-a-proxy"></a>Erstellen eines Proxys

Um zu ermitteln, ob ein UI-Element die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle nativ unterstützt, sendet Oleacc.dll eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht. Ein Rückgabewert ungleich NULL bedeutet, dass das Element System intern Microsoft Active Accessibility unterstützt und seine eigene **IAccessible** -Unterstützung bietet. Wenn der Rückgabewert jedoch 0 (null) ist, stellt Oleacc.dll ein Proxy Objekt für das UI-Element bereit und versucht, aussagekräftige Informationen in seinem Namen zurückzugeben. Weitere Informationen zu **WM \_ GetObject** finden Sie unter [Funktionsweise von "WM \_ GetObject](how-wm-getobject-works.md)".

## <a name="what-information-is-exposed"></a>Welche Informationen verfügbar gemacht werden?

Oleacc.dll verwendet den Windows-Klassennamen des Benutzeroberflächen Elements, um zu bestimmen, welche Informationen für die einzelnen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften verfügbar gemacht werden sollen und wie diese Informationen erfasst werden sollen. Oleacc.dll ruft z. b. die [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) -Funktion auf, um die [**Name**](name-property.md) -Eigenschaft für eine Standard-Push-Schaltfläche abzurufen, ruft aber dieselbe Funktion auf, um die [**value**](value-property.md) -Eigenschaft für ein Standardmäßiges Bearbeitungs Steuerelement abzurufen. In der Tat ordnet Oleacc.dll jede **IAccessible** -Methode einer entsprechenden Microsoft Win32-oder-Steuerungs spezifischen Nachricht oder einem entsprechenden Funktionsaufruf zu. Durch die Verwendung dieser auf einem Klassennamen basierenden sonderschreibung können aussagekräftige Informationen über **ibarrierefreie** Proxys ohne Unterstützung von Microsoft Active Accessibility auf dem Server zurückgegeben werden.

Anwendungen, die mit standardmäßigen Benutzeroberflächen Elementen erstellt werden, erhalten in der Regel vollständige Microsoft-Active Accessibility Support ohne zusätzliche Die Ausnahmen für diese Regel sind untergeordnete Steuerelemente, die keine eigenen Zeichen folgen speichern (Abwesenheit des **hasstrings** -Stils) oder die vom Besitzer gezeichnet werden. In diesen Fällen können Oleacc.dll die benötigten Informationen nicht erfassen, da die Informationen außerhalb des Steuer Elements gespeichert werden. In vielen dieser Szenarien, bei der Feststellung von Problem Umgehungen oder der Verwendung dynamischer Anmerkungen, kann der Server jedoch mit den von Oleacc.dll bereitgestellten Proxys zusammenarbeiten.

## <a name="generic-proxy-objects"></a>Generische Proxy Objekte

Wenn Oleacc.dll den Klassennamen des Benutzeroberflächen Elements nicht erkennt, erstellt er einen generischen Proxy, der so viele Informationen wie möglich verfügbar macht. Dies schließt höchstens das umgebende Rechteck des Objekts, das übergeordnete Objekt, den Namen (aus [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)) und alle untergeordneten Elemente in der Fenster Hierarchie ein.

 

 