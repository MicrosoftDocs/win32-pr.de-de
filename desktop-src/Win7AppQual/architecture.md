---
description: Eine lose gekoppelte Internet Explorer (LCIE) verbessert die Zuverlässigkeit des Browsers, indem seine Komponenten getrennt und die Abhängigkeiten gelockert werden.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Architektur (Cookbook zur Anwendungsqualität von Windows 7 und Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760081"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Architektur (Cookbook zur Anwendungsqualität von Windows 7 und Windows Server 2008 R2)

Eine *lose gekoppelte Internet Explorer* (LCIE) verbessert die Zuverlässigkeit des Browsers, indem seine Komponenten getrennt und die Abhängigkeiten gelockert werden.

Insbesondere versucht LCIE, den Windows Internet Explorer-Frame und seine Registerkarten in separaten Prozessen zu isolieren. In Windows Internet Explorer 8 verbessert diese Isolation die Leistung und Skalierbarkeit. Diese Architektur Änderung kann sich auf die Kompatibilität von Erweiterungen und Add-ons auswirken, einschließlich ActiveX-Steuerelementen, Browserhilfsobjekte (BHOs) und UI-Komponenten, die mit älteren Programmiertechniken erstellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von Updates, die sich auf die Kompatibilität zwischen Browsern auswirken](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



