---
description: Der Virtual Disk Service (VDS) verwaltet eine Vielzahl von Speicherkonfigurationen, von Desktops mit nur einem Datenträger bis zu externen Speicherarrays. Der Dienst macht eine Anwendungsprogrammierschnittstelle (API) verfügbar.
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Dienst für virtuelle Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c84217b1ca63debe3e117e33b2358e4b0e55697c02ce8e00ce7f764c1fbf692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137133"
---
# <a name="virtual-disk-service"></a>Dienst für virtuelle Datenträger

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des Virtual Disk Service durch die [Windows Storage Verwaltungs-API.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

## <a name="purpose"></a>Zweck

Der Virtual Disk Service (VDS) verwaltet eine Vielzahl von Speicherkonfigurationen, von Desktops mit nur einem Datenträger bis zu externen Speicherarrays. Der Dienst macht eine Anwendungsprogrammierschnittstelle (API) verfügbar.

## <a name="where-applicable"></a>Anwendungsbereich

Ab Windows 8 und Windows Server 8 wird die COM-Schnittstelle des Virtual Disk Service durch die Storage Verwaltungs-API ersetzt, eine WMI-basierte Programmierschnittstelle. Für die Verwaltung von Speichersubsystemen, (Windows), Partitionen und Volumes wird dringend empfohlen, die Storage Verwaltungs-API. Weitere Informationen finden Sie im [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Für alle Verwendungen außer Spiegelstartvolumes (mithilfe eines Spiegelvolumes zum Hosten des Betriebssystems) sind dynamische Datenträger veraltet. Verwenden Sie für Daten, die Resilienz gegen Laufwerkausfälle erfordern, Speicherplätze, eine robuste Speichervirtualisierungslösung. Weitere Informationen finden Sie unter [Speicherplätze Technical Preview.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11))

Anwendungsentwickler, die die in diesem Leitfaden beschriebenen Schnittstellen verwenden, können einen heterogenen Satz von vom Anbieter bereitgestellten und intern verwalteten Speicher abfragen und konfigurieren. VDS blendet die Komplexität des Speichers vor Anwendungen aus, wodurch der Dienst anbieter- und technologieneutral wird.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Dokumentation richtet sich an Anwendungsentwickler, die mit den Speicherfunktionen von Microsoft Windows-Plattformen vertraut sind und mit com-Entwicklung vertraut sind.

Das Handbuch richtet sich auch an Hersteller von Hardwaresubsystemen, die VDS-Hardwareanbieterprogramme entwickeln und unterstützen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

VDS wird auf Windows Server 2003, Windows Vista und höher unterstützt. Informationen zu Laufzeitanforderungen für ein bestimmtes Programmierelement finden Sie im Abschnitt Anforderungen der Dokumentation für dieses Element.

Das Ausführen von 32-Bit-VDS-Anwendungen unter WOW64 wird unterstützt, aber 64-Bit-VDS-Anbieter müssen als native Anwendungen auf 64-Bit-Versionen Windows werden.

VDS ist im Microsoft Windows Software Development Kit (SDK) verfügbar. Sie können das SDK für Windows 7 und Windows Server 2008 R2 aus dem [Windows Download Center installieren.](https://www.microsoft.com/download/details.aspx?id=8279) Diese Version des Windows SDK kann verwendet werden, um VDS-Anwendungen für Windows Server 2003, Windows Vista und höher zu entwickeln. Sie können auch die [ISO-Version des](https://www.microsoft.com/download/details.aspx?id=8442) SDK aus dem Windows Download Center herunterladen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                         | Beschreibung                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Informationen zu VDS](about-vds.md)<br/>         | Beschreibt das VDS-Objektmodell, Speicherkonfigurationsstrategien und VDS-Benachrichtigungen.<br/>    |
| [Verwenden von VDS](using-vds.md)<br/>         | Beschreibt die Verwendung von VDS zum Abfragen und Konfigurieren von Speichergeräten.<br/>                            |
| [VDS-Referenz](vds-reference.md)<br/> | Beschreibt VDS-Konstanten, Datentypen, Enumerationen, Schnittstellen, Strukturen und Fehlercodes.<br/> |



 

 

