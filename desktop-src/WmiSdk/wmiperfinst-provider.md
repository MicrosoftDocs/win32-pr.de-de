---
description: Ab Windows Vista stellt der WmiPerfInst-Anbieter unformatierte und formatierte Leistungsindikatordaten dynamisch für von Win32 Perf abgeleitete WMI-Leistungsindikatorklassen \_ bereit.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: WmiPerfInst-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a781fc1dc48f0e16d1c25e03eff1b2ab3c80fcd7058d1b49f95912b392d241
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049748"
---
# <a name="wmiperfinst-provider"></a>WmiPerfInst-Anbieter

Ab Windows Vista stellt der WmiPerfInst-Anbieter unformatierte und formatierte Leistungsindikatordaten dynamisch für [WMI-Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes) bereit, die von [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf)abgeleitet wurden. Dieser Anbieter ersetzt die [formatierte Leistung Datenanbieter](formatted-performance-data-provider.md), auch als "Cooked Counter Provider" bezeichnet, und den [Leistungsindikatoranbieter](performance-counter-provider.md).

Der WmiPerfInst-Anbieter stellt Daten für die WMI-Klassen bereit, die vom [WMIPerfClass-Anbieter](wmiperfclass-provider.md) bereitgestellt werden. Dieser Anbieter ist eine Brücke zwischen PDH-Instanzen (Performance Data Helper) und den WMI-Leistungsklassen, die vom WmiPerfClass-Anbieter bereitgestellt werden. Wenn WmiPerfInst eine Datenabfrage empfängt, lädt es die -Klasse und verwendet die Klassen- und [Eigenschaftsqualifizierer,](qualifiers-specific-to-wmi-performance-classes.md) um die PDH-Instanzen zu suchen. Weitere Informationen finden Sie unter [Verwenden der PDH-Funktionen zum Nutzen von Indikatordaten.](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)

Es wird nicht empfohlen, neue Leistungsobjekte zu entwickeln, indem Sie einen WMI-Hochleistungsanbieter erstellen und vom [*ADAP-Reverseadapterprozess*](gloss-r.md) abhängen, um die Daten an die Leistungsbibliotheken zu übertragen. Die Ausnahme besteht darin, dass Sie einen Windows Treibermodelltreiber entwickeln und Leistungsdaten bereitstellen möchten. Während der Reverseadapterprozess aus Gründen der Abwärtskompatibilität weiterhin funktioniert, empfiehlt sich die Verwendung von [Leistungsindikatoren, Version 6.0.](/windows/desktop/PerfCtrs/performance-counters-portal)

Der [**\_ \_ Win32Provider-Instanzname**](--win32provider.md) dieses Anbieters lautet "WmiPerfInst".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> <dt>

[Leistungsbibliotheken und WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 

 
