---
description: Sicherheit (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicherheit (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d392f5bf14997962173b9054baba861003877d851d6bd62a947b15757feec23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994660"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Sicherheit (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)

Ab Version Windows Internet Explorer 7 wird Windows Internet Explorer in einem Sicherheitskontext namens Geschützter *Modus* ausgeführt, wenn Benutzer ihn unter dem Betriebssystem Windows Vista oder einer neueren Version ausführen. Dieser Modus Internet Explorer in einer Einstellung mit niedrigeren Berechtigungen als eine Standardbenutzeranwendung ausgeführt, sodass bestimmte Funktionen eingeschränkt sind, insbesondere ActiveX-Steuerelemente und bestimmte Arten von Plug-Ins. Weitere Informationen zum geschützten Modus in Internet Explorer und seinen Auswirkungen auf die Kompatibilität finden Sie unter [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in der MSDN Library.

Standardmäßig aktiviert Windows Internet Explorer 8 auch die Datenausführungsverhindung (Data Execution Prevention, DEP), mit der Anwendungen verhindern können, dass bei Onlineangriffen beliebiger Code ausgeführt wird. Einige Add-Ons verwenden dieses Sicherheitsfeature jedoch möglicherweise nicht (z. B. alle Add-Ons, die nicht für die Ausführung von nur Code im Arbeitsspeicher ausgelegt sind, der speziell als ausführbare Datei gekennzeichnet wurde, z. B. Anwendungen, die mit einer älteren Version des ATL-Frameworks (ActiveX Template Library) erstellt wurden).

Internet Explorer 8 schützt Benutzer auch vor potenziellen Sicherheitsrisiken, die Skripts verwenden. Beispielsweise können Sie nicht von einer URL in einer weniger vertrauenswürdigen Zone zu einer URL in einer vertrauenswürdigeren Zone navigieren, außer durch explizite Benutzerinteraktion. Sie können auch bestimmte Elemente der Benutzeroberfläche des Browsers (z. B. die Adressleiste) in einer nicht vertrauenswürdigen Zone (Internet) nicht ausblenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwurfsupdates, die sich auf die Kompatibilität zwischen Browsern auswirken](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
