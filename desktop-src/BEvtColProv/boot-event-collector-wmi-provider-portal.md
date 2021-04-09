---
description: Der WMI-Anbieter des Start Ereignis Sammlers ermöglicht den Zugriff auf Verbindungs-und Konfigurationsinformationen für das Setup-und Start Ereignis Sammlungs Feature unter Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: WMI-Anbieter für Start Ereignis Sammler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860596"
---
# <a name="boot-event-collector-wmi-provider"></a>WMI-Anbieter für Start Ereignis Sammler

## <a name="purpose"></a>Zweck

Der WMI-Anbieter des Start Ereignis Sammlers ermöglicht den Zugriff auf Verbindungs-und Konfigurationsinformationen für das Setup-und Start Ereignis Sammlungs Feature unter Windows Server. Auf diese Weise können Sie eine Liste der aktuellen Verbindungen und den Verbindungs Verlauf zwischen einem Collector-Server und den zugehörigen Ziel Computern anzeigen. Außerdem können Sie mit diesem Anbieter die Konfiguration eines Collector-Servers verwalten.

> [!Note]  
> Der WMI-Anbieter des Start Ereignis Sammlers wird in BEvtCol.exe implementiert.

 

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Targetforwarding**](targetforwarding.md)
</dt> <dd>

Ruft Weiterleitungs Daten von einem Bereitstellungs Zielcomputer ab.

</dd> <dt>

[**Targetforwardingdestination**](targetforwardingdestination.md)
</dt> <dd>

Die bekannten Ziele, die die gesammelten Daten enthalten. Nur verfügbar, wenn der Collector mit aktiviertem Status Protokoll ausgeführt wird.

</dd> <dt>

[**Targetforwardinghistory**](targetforwardinghistory.md)
</dt> <dd>

Aktueller Verlauf der Änderungen an den Weiterleitungs Daten für einen Bereitstellungs Zielcomputer.

</dd> <dt>

[**Control**](control.md)
</dt> <dd>

Steuerung der Collector-Instanz. Erfordert die Administrator Rechte (BA).

</dd> </dl>

 

 



