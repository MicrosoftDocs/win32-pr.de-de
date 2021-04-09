---
description: Leistungs Bestellungs Klassen erlauben Skript-und Programm Zugriff auf Systemleistungs Daten, die von vorhandenen Hochleistungs Anbietern berechnet werden.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Leistungs Leistungsdaten-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861747"
---
# <a name="performance-counter-classes"></a>Leistungs Leistungsdaten-Klassen

Leistungs Bestellungs Klassen erlauben Skript-und Programm Zugriff auf Systemleistungs Daten, die von vorhandenen Hochleistungs Anbietern berechnet werden. Diese Klassen bestehen aus reinen Leistungsdaten und formatierten Leistungs Leistungs Zählers.

Verschiedene Anbieter stellen Leistungs Bibliotheksdaten über WMI bereit. Die Anbieter [wmiperfclass](/windows/desktop/WmiSdk/wmiperfclass-provider) und [wmiperfinst](/windows/desktop/WmiSdk/wmiperfinst-provider) stellen Klassen für die [Leistungsindikatoren](/windows/desktop/PerfCtrs/performance-counters-portal)Version 1 und Version 2 bereit. Diese Anbieter gewährleisten die Kompatibilität mit den in früheren Betriebssystemen verfügbaren Klassen.

Die Klassen in diesem Abschnitt sind die abstrakten Basisklassen, die zum Erstellen von Leistungs Zählers verwendet werden. Dies ist keine komplette Liste der Klassen, die Sie möglicherweise auf Ihrem Betriebssystem finden. Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Win32 \_ -Leistung**](win32-perf.md)
</dt> <dd>

Die Basisklasse für die Leistungs Zählers-Klassen [**Win32 \_ perfrawdata**](win32-perfrawdata.md) und [**Win32 \_ perfformatteddata**](win32-perfformatteddata.md).

</dd> <dt>

[**Win32 \_ perfformatteddata**](win32-perfformatteddata.md)
</dt> <dd>

eine abstrakte Basisklasse für die vorinstallierten, berechneten Daten Klassen.

</dd> <dt>

[**Win32- \_ perfrawdata**](win32-perfrawdata.md)
</dt> <dd>

Die abstrakte Basisklasse für alle konkreten Klassen des-rohleistungs Zählers.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Win32-Klassen](win32-provider.md)
</dt> </dl>

 

 
