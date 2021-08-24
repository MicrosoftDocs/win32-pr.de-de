---
description: 'Sie können Leistungsdaten nutzen, indem Sie eine der folgenden Schnittstellen verwenden: die PDH-Schnittstelle (Performance Data Helper), die zugriff auf hoher Ebene auf Daten von Leistungsindikatoranbietern der Version 1 und Version 2 bietet. Die Registrierungsschnittstelle, die Zugriff auf Daten von Leistungsindikatoranbietern auf niedriger Ebene bietet. Die Schnittstelle der Leistungsbibliothek, die direkten Zugriff auf Daten von Leistungsindikatoranbietern der Version 2 bietet. Die PDH-Schnittstelle ist einfacher zu verwenden als die Registrierungsschnittstelle und wird für die meisten Leistungsdatensammlungsaufgaben empfohlen. Die PDH-Schnittstelle ist im Wesentlichen eine abstraktion auf höherer Ebene der Funktionalität, die die Registrierungsschnittstelle bereitstellt. Verwenden Sie die Schnittstelle der Leistungsbibliothek nur, wenn Sie die PDH-Abstraktionsebenenfunktionen nicht verwenden können.'
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Nutzen von Indikatordaten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: f3abcc6dd5a385ebffdc887516613efb76b53359e5f8995bc28ba7f6239187b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775680"
---
# <a name="consuming-counter-data"></a>Nutzen von Indikatordaten

Programme, die Windows Leistungsindikatordaten lesen und verwenden möchten, können je nach Szenario eine von mehreren Schnittstellen verwenden.

- Skripts können die [WMI-Leistungsindikatorklassen](/windows/desktop/WmiSdk/monitoring-performance-data) oder das [TypePerf-Tool](/windows-server/administration/windows-commands/typeperf) verwenden.
- .NET-Programme können die [PerformanceCounter-Klasse](/dotnet/api/system.diagnostics.performancecounter)verwenden.
- Die [PDH-Bibliothek (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) bietet über eine Win32-API (C/C++) zugriff auf Daten sowohl von V1- als auch von V2-Leistungsindikatoranbietern.
- Die [Registrierungsschnittstelle](using-the-registry-functions-to-consume-counter-data.md) ermöglicht den Zugriff auf Daten von V1- und V2-Leistungsindikatoranbietern über den speziellen `HKEY_PERFORMANCE_DATA` Registrierungsschlüssel.
- Die [PerfLib V2-Consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md) bieten über eine Win32-API (C/C++) zugriff auf Daten von V2-Leistungsindikatoranbietern auf niedriger Ebene.

Die PDH-Schnittstelle wird für die meisten Leistungsdatensammlungsaufgaben in C/C++ empfohlen, da sie einfacher zu verwenden ist als die Registrierungs- und PerfLib-Schnittstellen.
