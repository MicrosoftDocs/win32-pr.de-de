---
title: Virtual Disk Service geht auf Windows Storage Verwaltungs-API
description: Virtual Disk Service geht auf Windows Storage Verwaltungs-API
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45e25452ae0b6bb20e0ca04130b7fa2fd64f2a191d504380f973f663b7931ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852037"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>Virtual Disk Service geht auf Windows Storage Verwaltungs-API

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des Virtual Disk Service durch die Storage Verwaltungs-API ersetzt, eine WMI-basierte Programmierschnittstelle. Für die Verwaltung von Speichersubsystemen, (Windows) Datenträgern, Partitionen und Volumes wird dringend empfohlen, die Storage Verwaltungs-API zu verwenden. Weitere Informationen finden Sie unter [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Für alle Verwendungen mit Ausnahme von Spiegelstartvolumes (mit einem Spiegelvolume zum Hosten des Betriebssystems) sind dynamische Datenträger veraltet. Verwenden Sie für Daten, die Resilienz bei Laufwerkausfällen erfordern, Speicherplätze, eine robuste Speichervirtualisierungslösung. Weitere Informationen finden Sie unter [Speicherplätze Technical Preview.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11))

Sie können DiskPart, DiskRAID und Die Datenträgerverwaltung während des Veralteten Zeitraums weiterhin verwenden, aber diese Tools funktionieren nicht mit Speicherplätze oder anderen neuen WMI-basierten (Windows Management Instrumentation)-basierten Windows Storage Management-APIs oder in-box-Speicherverwaltungshilfsprogrammen oder -clients.


| APIs | Speicher-Subsysteme | Basisdatenträger | Dynamische Datenträger | Speicherplätze |
| --- | --- | --- | --- | --- |
| Vds | Ja | Ja | Ja | Nein |
| WMI | Ja | Ja | Nein | Ja |
| DiskPart | – | Ja | Ja | Nein |
| DiskRAID |  Ja | – | – | – |
| Gui des Datenträgers mgmt | – | Ja | Ja | Nein |
| PowerShell | Ja | Ja | Nein | Ja |
| Speicherplätze Systemsteuerung | – | Nein | Nein | Ja |


Das Ergebnis dieses Übergangs ist eine höhere Speicherresilienz, Verfügbarkeit und Skalierbarkeit. eine einheitliche Skript- und Programmiersprache, reduzierte Speicherverwaltungskosten und eine einfachere Remotespeicherverwaltung.

## <a name="manifestation"></a>Manifestation

Die in der VDS-Umgebung verwendeten Hilfsprogramme DiskPart und DiskRAID unterstützen die neuen Speicherplätze nicht. Ebenso unterstützt das neue Storage PowerShell-Hilfsprogramm die veralteten dynamischen Datenträger nicht.

## <a name="mitigation"></a>Minderung

Microsoft empfiehlt dringend, dass Sie alle neuen Speicherverwaltungs-Apps auf dem Windows Storage Verwaltungs-API basieren und planen, vorhandene Apps, die auf der VDS-Infrastruktur basieren, während Ihrer Standardaktualisierungszyklen auf die Windows Storage Verwaltungs-API umgestellt zu werden.

## <a name="resources"></a>Ressourcen

-   [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Speicher-Cmdlets in Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Windows-Verwaltungsinstrumentation](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 