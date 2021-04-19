---
description: Der Dienst für virtuelle Datenträger (Virtual Disk Service, VDS) verwaltet eine große Bandbreite an Speicherkonfigurationen von Desktops mit einem Datenträger bis hin zu externen Speicherarrays. Der Dienst macht eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API) verfügbar.
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Dienst für virtuelle Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362257"
---
# <a name="virtual-disk-service"></a>Dienst für virtuelle Datenträger

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des virtuellen Festplatten Dienstanbieter durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

## <a name="purpose"></a>Zweck

Der Dienst für virtuelle Datenträger (Virtual Disk Service, VDS) verwaltet eine große Bandbreite an Speicherkonfigurationen von Desktops mit einem Datenträger bis hin zu externen Speicherarrays. Der Dienst macht eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API) verfügbar.

## <a name="where-applicable"></a>Anwendungsbereich

Ab Windows 8 und Windows Server 8 wird die COM-Schnittstelle des virtuellen Datenträger Dienstanbieter durch die Speicherverwaltungs-API ersetzt, eine WMI-basierte Programmierschnittstelle. Zum Verwalten von Speicher Subsystemen, (Windows)-Datenträgern, Partitionen und Volumes wird dringend empfohlen, die-Speicherverwaltungs-API zu verwenden. Weitere Informationen finden Sie in der [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Für alle Verwendungen mit Ausnahme von Spiegelungs Start Volumes (mit einem Spiegelungs Volume zum Hosten des Betriebssystems) sind dynamische Datenträger veraltet. Verwenden Sie für Daten, die Resilienz vor Laufwerks Fehlern erfordern, Speicherplätze, eine robuste Lösung für die Speichervirtualisierung. Weitere Informationen finden Sie unter [Speicherplätze Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Anwendungsentwickler, die die in diesem Handbuch beschriebenen Schnittstellen verwenden, können eine heterogene Gruppe von Hersteller-und intern verwaltetem Speicher Abfragen und konfigurieren. VDS blendet die Komplexität von Anwendungen aus, die mit dem Speicher verbunden sind, sodass der Dienst sowohl Hersteller als auch technologieneutral ist.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Dokumentation ist für Anwendungsentwickler gedacht, die mit den Speicherfunktionen von Microsoft Windows-Plattformen vertraut sind und die sich über die com-Entwicklung informieren.

Das Handbuch richtet sich auch an Hardware-Subsystem-Hersteller, die VDS-Hardware Anbieter Programme entwickeln und unterstützen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

VDS wird unter Windows Server 2003, Windows Vista und höher unterstützt. Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" in der Dokumentation für dieses Element.

Das Ausführen von 32-Bit-VDS-Anwendungen unter WOW64 wird unterstützt, aber 64-Bit-VDS-Anbieter müssen als native Anwendungen auf 64-Bit-Windows-Versionen ausgeführt werden.

VDS ist im Microsoft Windows Software Development Kit (SDK) verfügbar. Sie können das SDK für Windows 7 und Windows Server 2008 R2 aus dem [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279)installieren. Diese Version des Windows SDK kann verwendet werden, um VDS-Anwendungen für Windows Server 2003, Windows Vista und höher zu entwickeln. Sie können auch die [ISO-Version](https://www.microsoft.com/download/details.aspx?id=8442) des SDK aus dem Windows Download Center herunterladen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                         | BESCHREIBUNG                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Informationen zu VDS](about-vds.md)<br/>         | Beschreibt das VDS-Objektmodell, Speicher Konfigurations Strategien und VDS-Benachrichtigungen.<br/>    |
| [Verwenden von VDS](using-vds.md)<br/>         | Beschreibt die Verwendung von VDS zum Abfragen und Konfigurieren von Speichergeräten.<br/>                            |
| [VDS-Referenz](vds-reference.md)<br/> | Beschreibt VDS-Konstanten, Datentypen, Enumerationen, Schnittstellen, Strukturen und Fehlercodes.<br/> |



 

 

