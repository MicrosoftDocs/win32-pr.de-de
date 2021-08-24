---
description: Lose gekoppelte Internet Explorer (Loosely Coupled Internet Explorer, LCIE) verbessert die Zuverlässigkeit des Browsers, indem seine Komponenten getrennt und die Abhängigkeit gelockert wird.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Architektur (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a635f686c804a6c81146f156a0b70869edf4405e8d7c86d1fab8cfad9b21c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134123"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Architektur (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)

*Lose gekoppelte* Internet Explorer (LCIE) verbessert die Zuverlässigkeit des Browsers, indem seine Komponenten getrennt und die Abhängigkeit gelockert wird.

Insbesondere versucht LCIE, den Windows Internet Explorer und seine Registerkarten in separate Prozesse zu isolieren. In Windows Internet Explorer 8 verbessert diese Isolation die Leistung und Skalierbarkeit. Diese Architekturänderung kann sich auf die Kompatibilität von Erweiterungen und Add-Ons auswirken, einschließlich ActiveX-Steuerelemente, Browser-Hilfsprogrammobjekte (Browser Helper Objects, SOLLENOs) und Ui-Symbolleistenkomponenten, die mit älteren Programmiertechniken erstellt wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwurfsupdates, die sich auf die Kompatibilität zwischen Browsern auswirken](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



