---
title: Remotedesktopprotokoll-Anbieterschnittstellen
description: Schnittstellen, die von der Remotedesktopprotokoll-Anbieter-API unterstützt werden.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bde36cb70f937559dce20a73a485ec109a2cf6c6ae6c687655963c70e6ce22b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681230"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>Remotedesktopprotokoll-Anbieterschnittstellen

Die folgenden Schnittstellen werden von der Remotedesktopprotokoll Provider-API unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

Macht Methoden verfügbar, die vom Remotedesktopdienste aufgerufen werden, um eine Clientverbindung zu konfigurieren.

</dd> <dt>

[**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

Macht Methoden verfügbar, die Informationen zum Status einer Clientverbindung bereitstellen und Aktionen für den Client ausführen. Diese Schnittstelle wird vom Remotedesktopdienste implementiert und vom Protokoll aufgerufen.

</dd> <dt>

[**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

Macht Methoden verfügbar, die vom Remotedesktopdienste, um den Lizenzierungshandshake während einer Verbindungssequenz durchzuführen.

</dd> <dt>

[**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

Macht Methoden verfügbar, die anfordern, dass das Protokoll auf Clientverbindungsanforderungen startet und abhört.

</dd> <dt>

[**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

Macht Methoden verfügbar, die den Remotedesktopdienste, dass ein Client verbunden ist.

</dd> <dt>

[**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

Macht methoden verfügbar, die vom Remotedesktopdienste aufgerufen werden, um den Anmeldestatus zu aktualisieren und zu bestimmen, wie Anmeldefehlermeldungen direkt angezeigt werden.

</dd> <dt>

[**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

Macht Methoden verfügbar, die Remotedesktopdienste dienst verwendet, um mit dem Protokollanbieter zu kommunizieren.

</dd> <dt>

[**IWRdsProtocolSettings**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

Macht Methoden zum Abrufen und Hinzufügen richtlinienbezogener Einstellungen verfügbar.

</dd> <dt>

[**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

Macht methoden verfügbar, die vom Protokoll aufgerufen werden, um den Remotedesktopdienste zu benachrichtigen, die Zielseite eines Schattens zu starten oder zu beenden.

</dd> <dt>

[**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

Macht Methoden verfügbar, die den Protokollanbieter über den Status des Sitzungsschattens benachrichtigen.

</dd> <dt>

[**IWRdsRemoteFXGraphicsConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

Macht Methoden verfügbar, die im Zusammenhang mit der Bearbeitung und dem Verständnis von Grafiken auf der Clientverbindung stehen.

</dd> <dt>

[Veraltete Schnittstellen des Desktopprotokollanbieters](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

Die folgenden Schnittstellen sind veraltet und sollten nicht mehr verwendet werden. Verwenden Sie für neue Projekte stattdessen die schnittstellen Remotedesktopprotokoll Anbieterschnittstellen.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Remotedesktopprotokoll Anbieterreferenz](custom-remote-protocol-reference.md)
</dt> <dt>

[Remotedesktopprotokoll Anbieterenumeration](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Remotedesktopprotokoll Anbieterstrukturen](custom-remote-protocol-structures.md)
</dt> <dt>

[Remotedesktopprotokoll Anbieter-Unions](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




