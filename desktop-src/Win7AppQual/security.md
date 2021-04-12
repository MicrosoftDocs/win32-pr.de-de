---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicherheit (Cookbook zur Anwendungsqualität in Windows 7 und Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218826"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Sicherheit (Cookbook zur Anwendungsqualität in Windows 7 und Windows Server 2008 R2)

Ab Windows Internet Explorer 7 wird Windows Internet Explorer in einem Sicherheitskontext mit dem Namen *geschützter Modus* ausgeführt, wenn Benutzer es unter dem Betriebssystem Windows Vista oder einer höheren Version ausführen. Dieser Modus führt Internet Explorer mit einer niedrigeren Berechtigung als einer Standardbenutzer Anwendung aus, sodass bestimmte Funktionen eingeschränkt sind, insbesondere ActiveX-Steuerelemente und bestimmte Plug-in-Typen. Weitere Informationen zum geschützten Modus in Internet Explorer und dessen Auswirkungen auf die Kompatibilität finden Sie unter [Understanding and working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in der MSDN Library.

Windows Internet Explorer 8 ermöglicht standardmäßig auch die Daten Ausführungs Verhinderung (Data Execution Prevention, DEP), mit der Anwendungen vermeiden können, beliebigen Code in Online Angriffen auszuführen. Einige Add-ons verwenden diese Sicherheitsfunktion jedoch möglicherweise nicht (z. b. alle Add-ons, die nicht für die Ausführung von Code verwendet werden, der sich im Arbeitsspeicher befindet, der speziell als ausführbare Datei gekennzeichnet wurde, wie z. b. Anwendungen, die mit einer älteren Version des ATL-Frameworks (ActiveX Template Library) erstellt wurden).

Internet Explorer 8 schützt Benutzer auch vor potenziellen Sicherheitsrisiken, die Skripts verwenden. Beispielsweise können Sie nicht von einer URL in einer weniger vertrauenswürdigen Zone zu einer URL in einer vertrauenswürdigeren Zone navigieren, außer durch explizite Benutzerinteraktion. Sie können auch bestimmte Elemente der Benutzeroberfläche des Browsers (z. b. die Adressleiste) nicht in einer nicht vertrauenswürdigen Zone (Internet) ausblenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von Updates, die sich auf die Kompatibilität zwischen Browsern auswirken](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
