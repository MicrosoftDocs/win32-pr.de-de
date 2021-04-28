---
description: Sicherheit (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicherheit (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f320f4cb561079380e19a969eba95f3f6b321fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116228"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Sicherheit (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)

Ab Windows Internet Explorer 7 wird Windows Internet Explorer in einem Sicherheitskontext namens *Geschützter Modus* ausgeführt, wenn Benutzer sie unter dem Betriebssystem Windows Vista oder einer neueren Version ausführen. Dieser Modus wird Internet Explorer in einer Einstellung mit niedrigeren Berechtigungen als eine Standardbenutzeranwendung ausgeführt, sodass bestimmte Funktionen eingeschränkt sind, insbesondere ActiveX-Steuerelemente und bestimmte Arten von Plug-Ins. Weitere Informationen zum geschützten Modus in Internet Explorer und seinen Auswirkungen auf die Kompatibilität finden Sie unter [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in der MSDN Library.

Standardmäßig ermöglicht Windows Internet Explorer 8 auch die Verhinderung der Datenausführung (Data Execution Prevention, DEP), wodurch Anwendungen das Ausführen von beliebigem Code bei Onlineangriffen vermeiden können. Einige Add-Ons verwenden diese Sicherheitsfunktion jedoch möglicherweise nicht (z. B. alle Add-Ons, die nicht nur codeausgeführt werden sollen, der sich im Arbeitsspeicher befindet, der speziell als ausführbare Datei markiert wurde, z. B. Anwendungen, die mit einer älteren Version des ATL-Frameworks (ActiveX Template Library) erstellt wurden).

Internet Explorer 8 schützt Benutzer auch vor potenziellen Sicherheitsrisiken, die Skripts verwenden. Beispielsweise können Sie nur durch explizite Benutzerinteraktion von einer URL in einer weniger vertrauenswürdigen Zone zu einer URL in einer vertrauenswürdigeren Zone navigieren. Sie können auch bestimmte Elemente der Benutzeroberfläche des Browsers (z. B. die Adressleiste) nicht in einer nicht vertrauenswürdigen Zone (Internetzone) ausblenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwurfsupdates, die sich auf die Kompatibilität zwischen Browsern auswirken](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
