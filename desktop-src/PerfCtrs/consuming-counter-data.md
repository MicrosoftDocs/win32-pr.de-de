---
description: 'Leistungsdaten können mit einer der folgenden Schnittstellen genutzt werden: der PDH-Schnittstelle (Performance Data Helper), die einen Zugriff auf hoher Ebene auf Daten von den Leistungs Anbieter Anbietern der Version 1 und der Version 2 ermöglicht. Die Registrierungs Schnittstelle, die einen Low-Level-Zugriff auf Daten von leistungsindikatorenanbietern ermöglicht. Die Leistungs Bibliotheks Schnittstelle, die den direkten Zugriff auf Daten von Leistungs Anbieter Anbietern der Version 2 ermöglicht. Die PDH-Schnittstelle ist einfacher zu verwenden als die Registrierungs Schnittstelle und wird für die meisten Leistungsdaten Sammlungs Aufgaben empfohlen. Die PDH-Schnittstelle ist im Wesentlichen eine Abstraktions Ebene der Funktionalität, die die Registrierungs Schnittstelle bereitstellt. Verwenden Sie die Schnittstelle der Leistungs Bibliothek nur, wenn Sie die PDH-Abstraktions Ebenenfunktionen nicht verwenden können.'
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Verarbeiten von Counter-Daten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: c8c50b29d8f898f544b021f7fe3f3fd0d4a2094e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353462"
---
# <a name="consuming-counter-data"></a>Verarbeiten von Counter-Daten

Programme, die Windows-Leistungsdaten des Leistungs Zählers lesen und verwenden möchten, können je nach Szenario eine von mehreren Schnittstellen verwenden.

- Skripts können die [WMI-Leistungs Leistungswert Klassen](/windows/desktop/WmiSdk/monitoring-performance-data) oder das [typeperf](/windows-server/administration/windows-commands/typeperf) -Tool verwenden.
- .Net-Programme können die [Performance Counter-Klasse](/dotnet/api/system.diagnostics.performancecounter)verwenden.
- Die [PDH-Bibliothek (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) bietet über eine Win32-API (C/C++) Zugriff auf hoher Ebene auf Daten von v1-und v2-Leistungs Anbieter
- Die [Registrierungs Schnittstelle](using-the-registry-functions-to-consume-counter-data.md) ermöglicht den Zugriff auf Daten von v1-und v2-leistungsindikatorenanbietern über den speziellen `HKEY_PERFORMANCE_DATA` Registrierungsschlüssel.
- Die leistungsfähigen [Funktionen von Perflib v2](using-the-perflib-functions-to-consume-counter-data.md) bieten über eine Win32-API (C/C++) einen Low-Level-Zugriff auf Daten von V2-Leistungs Anbieter-Anbietern.

Die PDH-Schnittstelle wird für die meisten C/C++-Leistungsdaten Sammlungs Aufgaben empfohlen, da Sie einfacher zu verwenden ist als die Registrierungs-und Perflib-Schnittstellen.
