---
description: Leistungsindikatorklassen ermöglichen Skript- und Programmzugriff auf Systemleistungsdaten, die von vorhandenen Hochleistungsanbietern berechnet werden.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Leistungsindikatorklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc66020fc7863153e3e663c7552ee6805b2a676772fdcbf01cd9683a9ec05486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701650"
---
# <a name="performance-counter-classes"></a>Leistungsindikatorklassen

Leistungsindikatorklassen ermöglichen Skript- und Programmzugriff auf Systemleistungsdaten, die von vorhandenen Hochleistungsanbietern berechnet werden. Diese Klassen bestehen aus unformatierten Leistungsindikatorklassen und formatierten Leistungsindikatorklassen.

Verschiedene Anbieter stellen Leistungsbibliotheksdaten über WMI bereit. Die Anbieter [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) und [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) stellen Klassen für [Leistungsindikatoren](/windows/desktop/PerfCtrs/performance-counters-portal)der Version 1 und Version 2 bereit. Diese Anbieter aufrechterhalten die Kompatibilität mit den Klassen, die in früheren Betriebssystemen verfügbar sind.

Die Klassen in diesem Abschnitt sind die abstrakten Basisklassen, die zum Erstellen von Leistungsindikatorklassen verwendet werden. Dies ist keine vollständige Liste der Klassen, die sie möglicherweise auf Ihrem Betriebssystem finden. Weitere Informationen finden Sie unter [Leistungsbibliotheken und WMI.](/windows/desktop/WmiSdk/performance-libraries-and-wmi)

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Win32 \_ Perf**](win32-perf.md)
</dt> <dd>

Die Basisklasse für die Leistungsindikatorklassen [**Win32 \_ PerfRawData**](win32-perfrawdata.md) und [**Win32 \_ PerfFormattedData.**](win32-perfformatteddata.md)

</dd> <dt>

[**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md)
</dt> <dd>

eine abstrakte Basisklasse für die vorinstallierten, berechneten Datenklassen.

</dd> <dt>

[**Win32 \_ PerfRawData**](win32-perfrawdata.md)
</dt> <dd>

Die abstrakte Basisklasse für alle konkreten unformatierten Leistungsindikatorklassen.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Win32-Klassen](win32-provider.md)
</dt> </dl>

 

 
