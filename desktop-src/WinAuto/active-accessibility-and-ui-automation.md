---
title: Active Accessibility und Benutzeroberflächen Automatisierung
description: Microsoft Active Accessibility ist für die Verwendung mit Windows XP und früheren Betriebssystemen konzipiert.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341885"
---
# <a name="active-accessibility-and-ui-automation"></a>Active Accessibility und Benutzeroberflächen Automatisierung

Microsoft Active Accessibility ist für die Verwendung mit Windows XP und früheren Betriebssystemen konzipiert. Entwickler von benutzerdefinierten Steuerelementen und zugänglichen Technologie Client Anwendungen für Windows XP und Windows Vista sollten stattdessen die Verwendung von Microsoft [UI Automation](entry-uiauto-win32.md) in Erwägung gezogen.

Microsoft UI Automation ist ein System mit vollem Funktionsumfang, das präzisere Informationen über die Benutzeroberfläche bereitstellt und dem Benutzer die Interaktion mit Steuerelementen ermöglicht. Insbesondere bietet Sie eine stark verbesserte Unterstützung für Text.

Ein Satz von Proxy Objekten bietet Unterstützung für die Benutzeroberflächen Automatisierung für standardmäßige Microsoft Win32-und Windows Forms-Steuerelemente Umfangreichere Unterstützung ist für Steuerelemente verfügbar, die speziell im Hinblick auf die Benutzeroberflächen Automatisierung geschrieben wurden, einschließlich System eigener Windows Presentation Foundation (WPF)-Elemente, die Microsoft Active Accessibility nicht direkt unterstützen. Benutzerdefinierte Steuerelemente, die Benutzeroberflächen Automatisierung unterstützen, können in verwaltetem oder nicht verwaltetem Code geschrieben werden.

Microsoft Active Accessibility-Clients haben über eine Überbrückungs Schicht eingeschränkten Zugriff auf Benutzeroberflächen Elemente, die nur die Automatisierung der Benutzeroberfläche unterstützen. Weitere Informationen finden Sie unter [Anhang G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).

Weitere Informationen zu den Ähnlichkeiten und unterschieden zwischen Microsoft Active Accessibility und der Automatisierung der Benutzeroberfläche finden Sie [im Vergleich zu Microsoft Active Accessibility und UI-Automatisierung](microsoft-active-accessibility-and-ui-automation-compared.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[Benutzeroberflächenautomatisierung](entry-uiauto-win32.md)
</dt> </dl>

 

 




