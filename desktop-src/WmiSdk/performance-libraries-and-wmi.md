---
description: Der WMIPerfClass-Anbieter und der WMIPerfInst-Anbieter stellen dynamisch Leistungsindikatordaten für die WMI-Leistungsindikatorklassen zur Verfügung.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Leistungsbibliotheken und WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877623bcf27dffe71146df4f9c117da83941bd1d8e2ed46436a04c1d7ace95df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996410"
---
# <a name="performance-libraries-and-wmi"></a>Leistungsbibliotheken und WMI

Der [WMIPerfClass-Anbieter](wmiperfclass-provider.md) und [der WMIPerfInst-Anbieter](wmiperfinst-provider.md) stellen dynamisch Leistungsindikatordaten für die WMI-Leistungsindikatorklassen [zur Verfügung.](/windows/desktop/CIMWin32Prov/performance-counter-classes)

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>WMIPerfClass- und WMIPerfInst-Anbieter

[Der WMIPerfClass-Anbieter](wmiperfclass-provider.md) erstellt [WMI-Leistungsindikatorklassen bei](/windows/desktop/CIMWin32Prov/performance-counter-classes) der Systemin initialisierung. Der [WMIPerfInst-Anbieter](wmiperfinst-provider.md) stellt für diese Klassen dynamisch Leistungsindikatordaten zur Hand. Der WMIPerfClass-Anbieteranbieter stellt Klassen für die Leistungsindikatoren Version 1 und Version 2 [zur Hand.](/windows/desktop/PerfCtrs/performance-counters-portal)

Leistungsindikatoren der Version 1 befinden sich in der Registrierung unter **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services.** Dienste, die Leistungsdaten  bereitstellen, verfügen über einen Leistungsunterschlüssel. WMI-Leistungsklassen, die aus Leistungsindikatoren der Version 1 erstellt wurden, verfügen nicht über "Counters" als Teil ihres Namens.

Die **GUIDs,** die einen Leistungsindikatoranbieter der Version 2 identifizieren, befinden sich in der Registrierung unter **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Perflib \\ \_ V2Providers.**

WMIPerfClass wird als normaler WMI-Klassenanbieter registriert. WMIPerfInst ist ein WMI-Instanzanbieter, der Daten des Leistungsdaten-Hilfsers (PERFORMANCE Data Helper, PDH) für Leistungsindikatoren der Version 1 und Version 2 liefert. Weitere Informationen finden Sie unter [Verwenden der PDH-Funktionen zum Nutzen von Indikatordaten.](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 

 
