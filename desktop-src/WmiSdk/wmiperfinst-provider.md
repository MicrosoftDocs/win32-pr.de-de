---
description: Ab Windows Vista liefert der WMIPerfInst-Anbieter Rohdaten und formatierte Leistungsdaten von Leistungsdaten dynamisch in WMI-Leistungs Leistungsdaten-Klassen, die von Win32 \_ perf abgeleitet werden.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: WMIPerfInst-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343431"
---
# <a name="wmiperfinst-provider"></a>WMIPerfInst-Anbieter

Ab Windows Vista liefert der WMIPerfInst-Anbieter Rohdaten und formatierte Leistungsdaten von Leistungsdaten dynamisch in WMI- [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes) Daten-Klassen, die von [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf)abgeleitet werden. Dieser Anbieter ersetzt das [formatierte Leistungs Datenanbieter](formatted-performance-data-provider.md), das auch als "gekochte Leistungs Anbieter" bezeichnet wird, und den [Leistungsindikatorenanbieter](performance-counter-provider.md).

Der WMIPerfInst-Anbieter liefert Daten für die WMI-Klassen, die vom [wmiperfclass](wmiperfclass-provider.md) -Anbieter bereitgestellt werden. Bei diesem Anbieter handelt es sich um eine Brücke zwischen den PDH-Instanzen (Performance Data Helper) und den vom wmiperfclass-Anbieter bereitgestellten WMI-Leistungsklassen. Wenn wmiperfinst eine Abfrage für Daten empfängt, lädt es die-Klasse und verwendet die Klassen-und Eigenschafts [Qualifizierer](qualifiers-specific-to-wmi-performance-classes.md) , um die PDH-Instanzen zu suchen. Weitere Informationen finden Sie unter [Verwenden der PDH-Funktionen zum](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)verarbeiten von Counter-Daten.

Es wird nicht empfohlen, neue Leistungs Objekte zu entwickeln, indem Sie einen leistungsfähigen WMI-Anbieter erstellen und vom [*ADAP-Reverse-Adapter*](gloss-r.md) -Prozess abhängig sind, um die Daten in die Leistungs Bibliotheken zu übertragen. Die Ausnahme ist, wenn Sie einen Windows-Treibermodell Treiber entwickeln und Leistungsdaten bereitstellen möchten. Während der reverseadapterprozess weiterhin aus Gründen der Abwärtskompatibilität funktioniert, empfiehlt es sich, die [Leistungsindikatoren Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal)zu verwenden.

Der [**\_ \_ Win32Provider**](--win32provider.md) -Instanzname dieses Anbieters lautet "wmiperfinst".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> <dt>

[Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 

 
