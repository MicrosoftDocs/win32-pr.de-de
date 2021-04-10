---
description: Ab Windows Vista erstellt dieser Anbieter die WMI-Leistungs Leistungs Ereignis Klassen.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Wmiperfclass-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042362"
---
# <a name="wmiperfclass-provider"></a>Wmiperfclass-Anbieter

Ab Windows Vista erstellt dieser Anbieter die WMI- [Leistungs Leistungs Ereignis Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes). Daten werden vom [wmiperfinst](wmiperfinst-provider.md) -Anbieter dynamisch für diese WMI-Leistungsklassen bereitgestellt. Der AutoDiscovery/AUTOPURGE-Prozess (ADAP) überträgt Leistungs Objekt Objekte nicht mehr in WMI-Leistungsklassen im WMI-Repository. Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md).

Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md).

Es wird zwar nicht empfohlen, neue Leistungs Objekte zu entwickeln, indem Sie einen leistungsfähigen WMI-Anbieter erstellen und vom [*ADAP-Reverse-Adapter*](gloss-r.md) -Prozess abhängig sind, um die Daten in die Leistungs Bibliotheken zu übertragen. die Ausnahme bildet die Entwicklung eines Windows-Treibermodell Treibers, der Leistungsdaten bereitstellt. Während der reverseadapterprozess weiterhin aus Gründen der Abwärtskompatibilität funktioniert, empfiehlt es sich, die [Leistungsindikatoren Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal)zu verwenden.

Der [**\_ \_ Win32Provider**](--win32provider.md) -Instanzname dieses Anbieters lautet "wmiperfclass".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> <dt>

[Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 

 
