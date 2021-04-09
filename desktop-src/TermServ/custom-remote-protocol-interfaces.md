---
title: Remotedesktopprotokoll Anbieter Schnittstellen
description: Schnittstellen, die von der Remotedesktopprotokoll Anbieter-API unterstützt werden.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947304"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>Remotedesktopprotokoll Anbieter Schnittstellen

Die folgenden Schnittstellen werden von der Remotedesktopprotokoll Anbieter-API unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Iwrdsprodecolconnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

Macht Methoden verfügbar, die vom Remotedesktopdienste-Dienst aufgerufen werden, um eine Client Verbindung zu konfigurieren.

</dd> <dt>

[**Iwrdsproprocolconnectioncallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

Macht Methoden verfügbar, die Informationen über den Status einer Client Verbindung bereitstellen und Aktionen für den Client ausführen. Diese Schnittstelle wird vom Remotedesktopdienste-Dienst implementiert und durch das-Protokoll aufgerufen.

</dd> <dt>

[**Iwrdspro| collicenseconnetction**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

Macht Methoden verfügbar, die vom Remotedesktopdienste-Dienst verwendet werden, um während einer Verbindungs Sequenz den Lizenzierungs Hand Shake auszuführen.

</dd> <dt>

[**Iwrdsprotekollistener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

Macht Methoden verfügbar, die anfordern, dass das Protokoll auf Client Verbindungsanforderungen lauscht und die Überwachung beendet.

</dd> <dt>

[**Iwrdspro| collistenercallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

Macht Methoden verfügbar, die den Remotedesktopdienste Dienst Benachrichtigen, dass ein Client eine Verbindung hergestellt hat.

</dd> <dt>

[**Iwrdsproweredirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

Macht Methoden verfügbar, die vom Remotedesktopdienste Dienst aufgerufen werden, um den Anmeldestatus zu aktualisieren und zu bestimmen, wie Anmelde Fehlermeldungen umgeleitet werden.

</dd> <dt>

[**Iwrdsproum colmanager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

Macht Methoden verfügbar, die der Remotedesktopdienste-Dienst für die Kommunikation mit dem Protokoll Anbieter verwendet.

</dd> <dt>

[**Iwrdsprodecolsettings**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

Macht Methoden zum Abrufen und Hinzufügen von Richtlinien bezogenen Einstellungen verfügbar.

</dd> <dt>

[**Iwrdsprotrocolshadowcallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

Macht Methoden verfügbar, die vom Protokoll aufgerufen werden, um den Remotedesktopdienste Dienst zu benachrichtigen, dass die Zielseite eines Schattens gestartet oder beendet wird.

</dd> <dt>

[**Iwrdsprodecolshadowconnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

Macht Methoden verfügbar, die den Protokoll Anbieter über den Status des Sitzungs shadoings benachrichtigen.

</dd> <dt>

[**Iwrdsremotefxgraphicsconnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

Macht Methoden verfügbar, die sich auf die Bearbeitung und das Verständnis von Grafiken in der Client Verbindung beziehen.

</dd> <dt>

[Veraltete Desktop Protokoll-Anbieter Schnittstellen](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

Die folgenden Schnittstellen sind veraltet und sollten nicht mehr verwendet werden. Verwenden Sie für neue Projekte stattdessen die Schnittstellen der Schnittstellen für Remotedesktopprotokoll-Anbieter.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Remotedesktopprotokoll Anbieter Referenz](custom-remote-protocol-reference.md)
</dt> <dt>

[Remotedesktopprotokoll Anbieter Enumerationen](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Remotedesktopprotokoll Anbieter Strukturen](custom-remote-protocol-structures.md)
</dt> <dt>

[Remotedesktopprotokoll Anbieter-Unions](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




