---
description: Der WMI-Anbieter für den Startereignissammler bietet Zugriff auf Verbindungs- und Konfigurationsinformationen für das Setup- und Startereignissammlungsfeature auf Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: WMI-Anbieter für den Startereignissammler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccebb4c4408aaa0ce58ad6ab412e4ca85fbb291c8da14ba764dfe3b19e2cbfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579860"
---
# <a name="boot-event-collector-wmi-provider"></a>WMI-Anbieter für den Startereignissammler

## <a name="purpose"></a>Zweck

Der WMI-Anbieter für den Startereignissammler bietet Zugriff auf Verbindungs- und Konfigurationsinformationen für das Setup- und Startereignissammlungsfeature auf Windows Server. Dadurch können Sie eine Liste der aktuellen Verbindungen und den Verbindungsverlauf zwischen einem Collectorserver und dessen Zielcomputern anzeigen. Darüber hinaus können Sie mit diesem Anbieter die Konfiguration eines Collectorservers verwalten.

> [!Note]  
> Der WMI-Anbieter für den Startereignissammler wird in BEvtCol.exe.

 

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**TargetForwarding**](targetforwarding.md)
</dt> <dd>

Ruft die Weiterleitungsdaten von einem Zielcomputer ab.

</dd> <dt>

[**TargetForwardingDestination**](targetforwardingdestination.md)
</dt> <dd>

Die bekannten Ziele, die die gesammelten Daten enthalten. Nur verfügbar, wenn der Collector mit aktivierten Statusprotokollen ausgeführt wird.

</dd> <dt>

[**TargetForwardingHistory**](targetforwardinghistory.md)
</dt> <dd>

Der aktuelle Verlauf der Änderungen an den Weiterleitungsdaten für einen Zielcomputer.

</dd> <dt>

[**Control**](control.md)
</dt> <dd>

Steuerung der Collectorinstanz. Erfordert die Administratorrechte (BA).

</dd> </dl>

 

 



