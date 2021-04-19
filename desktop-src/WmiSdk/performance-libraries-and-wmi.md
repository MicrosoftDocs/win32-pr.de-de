---
description: Der wmiperfclass-Anbieter und der WMIPerfInst-Anbieter stellen dynamische Leistungsdaten für die WMI-Leistungs Leistungs Leistungsgruppen bereit.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Leistungs Bibliotheken und WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359923"
---
# <a name="performance-libraries-and-wmi"></a>Leistungs Bibliotheken und WMI

Der [wmiperfclass-Anbieter](wmiperfclass-provider.md) und der [WMIPerfInst-Anbieter](wmiperfinst-provider.md) stellen dynamische Leistungsdaten für die WMI- [Leistungs Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes)Gruppen bereit.

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>Wmiperfclass-und WMIPerfInst-Anbieter

Der [wmiperfclass-Anbieter](wmiperfclass-provider.md) erstellt bei der Systeminitialisierung WMI- [Leistungs Leistungs Zählers](/windows/desktop/CIMWin32Prov/performance-counter-classes) . Der [WMIPerfInst-Anbieter](wmiperfinst-provider.md) stellt dynamisch Leistungsdaten für diese Klassen bereit. Der Anbieter des wmiperfclass-Anbieters liefert Klassen für [Leistungsindikatoren](/windows/desktop/PerfCtrs/performance-counters-portal)der Versionen 1 und Version 2.

Leistungsindikatoren der Version 1 finden Sie in der Registrierung unter **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**. Dienste, die Leistungsdaten bereitstellen, verfügen über einen **Leistungs** Unterschlüssel. WMI-Leistungsklassen, die aus den Leistungsindikatoren der Version 1 erstellt wurden, haben nicht als Teil Ihres Namens "Indikatoren".

Die **GUID** s, die einen Leistungs Anbieter für die Version 2 identifizieren, finden Sie in der Registrierung unter **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.

Wmiperfclass ist als normaler WMI-Klassen Anbieter registriert. Wmiperfinst ist ein WMI-Instanzanbieter, der Daten aus dem Leistungsdaten-Hilfsprogramm (PDH) für die Leistungsindikatoren Version 1 und Version 2 bereitstellt. Weitere Informationen finden Sie unter [Verwenden der PDH-Funktionen zum](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)verarbeiten von Counter-Daten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 

 
