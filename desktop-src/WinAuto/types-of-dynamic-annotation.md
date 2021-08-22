---
title: Typen dynamischer Anmerkungen
description: Es gibt drei Typen von dynamischen Anmerkungen, die in Microsoft Active Accessibility direkten Anmerkung, der Wertzuordnung und der Serveranmerkung unterstützt werden. Jeder Typ bietet bestimmte Vorteile, daher ist es wichtig, die Unterschiede zu verstehen.
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58d30abe3d34fc61a9c85ebce0f6f6e38d51a43b70bef7d28f82adc4b476d74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570930"
---
# <a name="types-of-dynamic-annotation"></a>Typen dynamischer Anmerkungen

In Microsoft Active Accessibility werden drei Typen dynamischer Anmerkungen unterstützt: *direkte Anmerkung,* *wertzuordnungsbasierte Anmerkung* und *Serveranmerkung.* Jeder Typ bietet bestimmte Vorteile, daher ist es wichtig, die Unterschiede zu verstehen.

## <a name="direct-annotation"></a>Direkte Anmerkung

Die direkte Anmerkung ist die einfachste Form der dynamischen Anmerkung. Sie eignet sich am besten für barrierefreie Elemente, deren kommentierte Eigenschaft nicht vom Zustand des Steuerelements abhängig ist und keine zusätzliche Unterstützung durch die wertzuordnungsbasierte Anmerkung und die Serveranmerkung erfordert. Die direkte Anmerkung wird verwendet, um den Wert einer oder mehrerer Microsoft Active Accessibility Eigenschaften eines barrierefreien Elements zu überschreiben und eine Microsoft Benutzeroberflächenautomatisierung-Eigenschaft zum Steuerelement zu überschreiben oder hinzuzufügen. Alle Anmerkungen, die in einer Microsoft Active Accessibility -Eigenschaft vorgenommen werden, werden sowohl in der Benutzeroberflächenautomatisierung übersetzung als auch im proxy-Microsoft Active Accessibility-to-Benutzeroberflächenautomatisierung widergespiegelt. Weitere Informationen finden Sie unter [Direkte Anmerkung.](direct-annotation.md)

## <a name="value-map-annotation"></a>Wertzuordnungsanmerkung

Zusätzlich zum direkten Kommentieren von [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ist es häufig erforderlich, einen steuerelementspezifischen Wert in eine Zeichenfolge zu konvertieren, die von einem Endbenutzer verstanden werden kann. Ein Beispiel ist das Bildschirmauflösungs-Schieberegler-Steuerelement auf der Registerkarte **Einstellungen** im **Anzeigeeigenschaften** Fenster (aus **Systemsteuerung**). Während jede Schiebereglerposition einer anderen Auflösung entspricht (z. B. 640 x 480, 1024 x 768), hat das Steuerelement keine Kenntnis dieser Beziehung und kann diese Informationen nicht an Microsoft Active Accessibility übermitteln.

Die Wertzuordnungsanmerkung vereinfacht diese Aufgabe. Mit dieser Form der Anmerkung können Sie Zeichenfolgen für Schiebereglerwerte und Rollen, Zustände und Beschreibungen für Symbole in Listen- und Strukturansichten angeben. Weitere Informationen finden Sie unter [Wertzuordnungsanmerkung.](value-map-annotation.md)

## <a name="server-annotation"></a>Serveranmerkung

Mit der Serveranmerkung können Entwickler ein Rückrufobjekt registrieren, um Clientanforderungen für die mit Anmerkungen versehene Eigenschaft eines Elements zu bedienen. Dieses Rückrufobjekt muss die [**IAccPropServer-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) implementieren und bei Microsoft Active Accessibility Anmerkungsdiensten registriert sein. Nach der Registrierung wird er aufgefordert, alle Clientanforderungen für den Eigenschaftswert dieses barrierefreien Elements zu warten.

Ein besonders nützliches Feature der Serveranmerkung ist, dass ein Server einmal registriert werden kann, um Anforderungen für einen Container und alle untergeordneten Elemente zu verarbeiten. Ein einzelner Server kann also beispielsweise einmal eingerichtet werden, um Anforderungen für alle Elemente zu verarbeiten, ist ein Listenfeld. Weitere Informationen finden Sie unter [Serveranmerkung.](server-annotation.md)

 

 




