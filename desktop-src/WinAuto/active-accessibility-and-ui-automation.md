---
title: Active Accessibility und Benutzeroberflächenautomatisierung
description: Microsoft Active Accessibility ist für die Verwendung mit Windows XP und früheren Betriebssystemen konzipiert.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fa4c06d528281552c47b987a07fba416376b3291f40315770ed98be944554e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071910"
---
# <a name="active-accessibility-and-ui-automation"></a>Active Accessibility und Benutzeroberflächenautomatisierung

Microsoft Active Accessibility ist für die Verwendung mit Windows XP und früheren Betriebssystemen konzipiert. Entwickler von benutzerdefinierten Steuerelementen und barrierefreien Technologieclientanwendungen für Windows XP und Windows Vista sollten stattdessen die Verwendung von Microsoft [Benutzeroberflächenautomatisierung](entry-uiauto-win32.md) in Betracht ziehen.

Microsoft Benutzeroberflächenautomatisierung ist ein System mit vollem Funktionsumfang, das genauere Informationen über die Benutzeroberfläche bereitstellt und dem Benutzer mehr Möglichkeiten bietet, mit Steuerelementen zu interagieren. Insbesondere bietet sie eine erheblich verbesserte Unterstützung für Text.

Ein Satz von Proxyobjekten bietet Benutzeroberflächenautomatisierung Unterstützung für Standardmäßige Microsoft Win32- und Windows Forms-Steuerelemente. Umfangreichere Unterstützung ist für Steuerelemente verfügbar, die speziell mit Benutzeroberflächenautomatisierung geschrieben wurden, einschließlich nativer WPF-Elemente (Windows Presentation Foundation), die Microsoft Active Accessibility nicht direkt unterstützen. Benutzerdefinierte Steuerelemente, die Benutzeroberflächenautomatisierung unterstützen, können entweder in verwaltetem oder nicht verwaltetem Code geschrieben werden.

Microsoft Active Accessibility Clients haben über eine Überbrückungsebene eingeschränkten Zugriff auf Benutzeroberflächenelemente, die nur Benutzeroberflächenautomatisierung unterstützen. Weitere Informationen finden Sie in [Anhang G: Active Accessibility Bridge to Benutzeroberflächenautomatisierung](appendix-g--active-accessibility-bridge-to-ui-automation.md).

Weitere Informationen zu den Ähnlichkeiten und Unterschieden zwischen Microsoft Active Accessibility und Benutzeroberflächenautomatisierung finden Sie unter [Microsoft Active Accessibility und Benutzeroberflächenautomatisierung Vergleich.](microsoft-active-accessibility-and-ui-automation-compared.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[Benutzeroberflächenautomatisierung](entry-uiauto-win32.md)
</dt> </dl>

 

 




