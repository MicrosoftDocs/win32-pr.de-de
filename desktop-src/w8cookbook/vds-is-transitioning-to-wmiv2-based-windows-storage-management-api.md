---
title: Der virtuelle Datenträger Dienst wechselt zur Windows-Speicherverwaltungs-API.
description: Der virtuelle Datenträger Dienst wechselt zur Windows-Speicherverwaltungs-API.
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceea3ffe82358737ca8f39e9ef6db0bdb1f116ef
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104391103"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>Der virtuelle Datenträger Dienst wechselt zur Windows-Speicherverwaltungs-API.

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des virtuellen Datenträger Dienstanbieter durch die Speicherverwaltungs-API ersetzt, eine WMI-basierte Programmierschnittstelle. Zum Verwalten von Speicher Subsystemen, (Windows)-Datenträgern, Partitionen und Volumes wird dringend empfohlen, die-Speicherverwaltungs-API zu verwenden. Weitere Informationen finden Sie unter [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Für alle Verwendungen mit Ausnahme von Spiegelungs Start Volumes (mit einem Spiegelungs Volume zum Hosten des Betriebssystems) sind dynamische Datenträger veraltet. Verwenden Sie für Daten, die Resilienz vor Laufwerks Fehlern erfordern, Speicherplätze, eine robuste Lösung für die Speichervirtualisierung. Weitere Informationen finden Sie unter [Speicherplätze Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Sie können Diskpart, Diskraid und die Datenträgerverwaltung während des veralteten Zeitraums weiterhin verwenden. diese Tools funktionieren jedoch nicht mit Speicherplätzen oder mit anderen neuen Windows-Verwaltungsinstrumentation (WMI)-basierten Windows-Speicherverwaltungs-APIs oder in-Box-Speicher Verwaltungs Dienstprogrammen oder-Clients.


| APIs | Speicher-Subsysteme | Grundlegende Datenträger | Dynamische Datenträger | Speicherplätze |
| --- | --- | --- | --- | --- |
| VDS | Ja | Ja | Ja | Nein |
| WMI | Ja | Ja | Nein | Ja |
| DiskPart | – | Ja | Ja | Nein |
| DiskRAID |  Ja | – | – | – |
| Datenträger-Mgmt-GUI | – | Ja | Ja | Nein |
| PowerShell | Ja | Ja | Nein | Ja |
| Speicherplätze-Systemsteuerung | – | Nein | Nein | Ja |


Das Ergebnis dieses Übergangs ist eine höhere speicherresilienz, Verfügbarkeit und Skalierbarkeit. eine einheitliche Skript-und Programmiersprache, geringere Speicher Verwaltungskosten und eine einfachere Remote Speicherverwaltung.

## <a name="manifestation"></a>Ausstrahlung

Die in der VDS-Umgebung verwendeten Diskpart-und Diskraid-Hilfsprogramme unterstützen nicht die neuen Speicherplätze. Ebenso unterstützt das neue Storage PowerShell-Hilfsprogramm die veralteten dynamischen Datenträger nicht.

## <a name="mitigation"></a>Minderung

Microsoft empfiehlt dringend, dass Sie neue Speicher Verwaltungs-apps auf der Windows-Speicherverwaltungs-API als Grundlage für vorhandene apps, die auf der VDS-Infrastruktur basieren, auf die Windows-Speicherverwaltungs-API auf der Windows-Speicherverwaltungs-API in den standardmäßigen Aktualisierungszyklen umstellen.

## <a name="resources"></a>Ressourcen

-   [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Speicher-Cmdlets in Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Windows-Verwaltungsinstrumentation](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 