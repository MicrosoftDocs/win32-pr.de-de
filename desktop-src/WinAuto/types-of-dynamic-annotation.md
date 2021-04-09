---
title: Typen von dynamischer Anmerkung
description: Es gibt drei Arten von dynamischer Anmerkungen, die in Microsoft Active Accessibility Direct-Anmerkung, Wert zugeordnete Anmerkung und Server Anmerkung unterstützt werden. Jeder Typ bietet besondere Vorteile, daher ist es wichtig, die Unterschiede zu verstehen.
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0453d3b5d05e2713d1a57fb0f475d4ec2a481b02
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856156"
---
# <a name="types-of-dynamic-annotation"></a>Typen von dynamischer Anmerkung

Es gibt drei Arten von dynamischer Anmerkungen, die in Microsoft Active Accessibility unterstützt werden: *direkte Anmerkung*, Wert zugeordnete *Anmerkung* und *Server Anmerkung*. Jeder Typ bietet besondere Vorteile, daher ist es wichtig, die Unterschiede zu verstehen.

## <a name="direct-annotation"></a>Direkte Anmerkung

Die direkte Anmerkung ist die einfachste Form der dynamischen Anmerkung. Dies gilt besonders für barrierefreie Elemente, deren mit Anmerkungen versehene Eigenschaft nicht vom Zustand des Steuer Elements abhängt und die zusätzliche Unterstützung, die von der Wert zugeordneten Anmerkung und Server Anmerkung bereitgestellt wird, nicht benötigt. Die direkte Anmerkung wird verwendet, um den Wert einer oder mehrerer Eigenschaften von Microsoft Active Accessibility eines barrierefreien Elements zu überschreiben und um dem Steuerelement eine Microsoft UI Automation-Eigenschaft zu überschreiben oder hinzuzufügen. Alle Anmerkungen, die in einer Microsoft Active Accessibility-Eigenschaft vorgenommen werden, spiegeln sich sowohl in der Benutzeroberflächenautomatisierungs-Übersetzung als auch im Microsoft Active Accessibility-to-UI-Automatisierungs Proxy wider. Weitere Informationen finden Sie unter [direkte Anmerkung](direct-annotation.md).

## <a name="value-map-annotation"></a>Werte Zuordnungs Anmerkung

Zusätzlich zum direkten Hinzufügen von Anmerkungen zu [**ibarrierefreiheits**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Eigenschaften ist es häufig erforderlich, einen Steuerelement spezifischen Wert in eine Zeichenfolge zu konvertieren, die von einem Endbenutzer verstanden werden kann. Ein Beispiel hierfür ist das Schieberegler-Steuerelement Bildschirmauflösung auf der Registerkarte **Einstellungen** im Fenster **Eigenschaften anzeigen** (in der **Systemsteuerung**). Wenngleich die Schiebereglerposition einer anderen Auflösung entspricht (z. b. 640 x 480, 1024 x 768), hat das Steuerelement keine Kenntnis dieser Beziehung und kann diese Informationen nicht an Microsoft Active Accessibility übermitteln.

Durch Wert zugeordnete Anmerkung wird diese Aufgabe vereinfacht. Mit dieser Form der-Anmerkung können Sie Zeichen folgen für Schieberegler-Werte angeben und Rollen, Zustände und Beschreibungen für Symbole in Listen-und Struktur Ansichten angeben. Weitere Informationen finden Sie unter [Value Map](value-map-annotation.md)-Anmerkung.

## <a name="server-annotation"></a>Server Anmerkung

Die Server Anmerkung ermöglicht Entwicklern das Registrieren eines Rückruf Objekts für den Dienst von Client Anforderungen für die mit Anmerkungen versehene Eigenschaft eines Elements. Dieses Rückruf Objekt muss die [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) -Schnittstelle implementieren und bei Microsoft Active Accessibility Anmerkung-Diensten registriert sein. Nach der Registrierung wird der Dienst aufgefordert, alle Client Anforderungen für den Eigenschafts Wert dieses zugänglichen Elements zu bedienen.

Ein besonders nützliches Feature der Server Anmerkung ist, dass ein Server einmal registriert werden kann, um Anforderungen für einen Container und alle seine untergeordneten Elemente zu verarbeiten. So kann beispielsweise ein einzelner Server einmal eingerichtet werden, um Anforderungen für alle Elemente zu verarbeiten, ist ein Listenfeld. Weitere Informationen finden Sie unter [Server Anmerkung](server-annotation.md).

 

 




