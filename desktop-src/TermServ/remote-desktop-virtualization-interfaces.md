---
title: Remotedesktop Virtualisierungsschnittstellen
description: Die Remotedesktop virtualisierungsapi unterstützt die folgenden Schnittstellen.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315740"
---
# <a name="remote-desktop-virtualization-interfaces"></a>Remotedesktop Virtualisierungsschnittstellen

Die Remotedesktop virtualisierungsapi unterstützt die folgenden Schnittstellen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Itssbbasenotifysink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

Macht Methoden verfügbar, die Status-und Fehlermeldungen an Remotedesktopverbindung Broker (RD-Verbindungsbroker) melden.

</dd> <dt>

[**Itssbclientconnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

Macht Methoden und Eigenschaften verfügbar, die Zustandsinformationen über eine eingehende Verbindungsanforderung von einem Remotedesktopverbindung-Client (RDC) speichern.

</dd> <dt>

[**Itssbclientconnectionpropertyset**](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

Kann verwendet werden, um benutzerdefinierte Eigenschaften einer Client Verbindung nach Bedarf zu definieren.

</dd> <dt>

[**Itssbenvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

Macht Methoden und Eigenschaften verfügbar, die Informationen über die Umgebung enthalten, die den Zielcomputer hostet. Diese Schnittstelle kann zum Speichern von Informationen zu einem physischen Server verwendet werden, der virtuelle Maschinen hostet.

</dd> <dt>

[**Itssbenvironmentpropertyset**](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

Kann verwendet werden, um benutzerdefinierte Eigenschaften einer Umgebung zu definieren, die Zielcomputer nach Bedarf hostet.

</dd> <dt>

[**Itssbfilterpluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

Plug-in-Speicher

</dd> <dt>

[**Itssbgenericnotifysink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

Macht Methoden verfügbar, die den Abschluss und die Wartezeit von der RD-Verbindungsbroker melden.

</dd> <dt>

[**Itssbglobalstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

Macht Methoden verfügbar, die Zielcomputer, Sitzungen, Umgebungen und Farmen Abfragen, die dem RD-Verbindungsbroker-Speicher hinzugefügt wurden.

</dd> <dt>

[**Itssbloadbalanceresult**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

Macht Methoden und Eigenschaften verfügbar, die den von einem Lasten Ausgleichs Algorithmus zurückgegebenen Zielnamen speichern.

</dd> <dt>

[**Itssbloadbalancing**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

Macht Methoden verfügbar, die Sie verwenden können, um einen benutzerdefinierten Lasten Ausgleichs Algorithmus bereitzustellen.

</dd> <dt>

[**Itssbloadbalancingnotifysink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

Macht Methoden verfügbar, die das Ergebnis eines Lasten Ausgleichs Algorithmus zum RD-Verbindungsbroker zurückgeben.

</dd> <dt>

[**Itssborchestration**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

Macht Methoden verfügbar, die von RD-Verbindungsbroker verwendet werden, um sicherzustellen, dass das Ziel bereit ist, bevor ein Client dorthin umgeleitet wird.

</dd> <dt>

[**Itssborchestrationnotifysink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

Macht Methoden verfügbar, die ein [**itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) -Objekt an RD-Verbindungsbroker zurückgeben, nachdem das Ziel erfolgreich für eine Verbindung vorbereitet wurde.

</dd> <dt>

[**Itssbplacement**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

Macht Methoden verfügbar, mit denen die Umgebung (der Computer, der die virtuelle Maschine hostet) vorbereitet wird.

</dd> <dt>

[**Itssbplacementnotifysink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

Macht Methoden verfügbar, die Informationen zu Umgebungen zurückgeben, die RD-Verbindungsbroker werden.

</dd> <dt>

[**Itssbplugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

Macht Methoden verfügbar, die Plug-ins initialisieren und beenden.

</dd> <dt>

[**Itssbpluginnotifysink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

Macht Methoden verfügbar, die RD-Verbindungsbroker über die Initialisierung oder Beendigung eines Plug-ins benachrichtigen.

</dd> <dt>

[**Itssbpluginpropertyset**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

Kann verwendet werden, um nach Bedarf benutzerdefinierte Plug-in-Eigenschaften zu definieren.

</dd> <dt>

[**Itssbpropertyset**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

Kann verwendet werden, um benutzerdefinierte Eigenschaften nach Bedarf zu definieren.

</dd> <dt>

[**Itssbprovider**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

Macht Methoden verfügbar, mit denen Standard Implementierungen von Objekten erstellt werden, die in Remotedesktop Virtualisierung verwendet werden.

</dd> <dt>

[**Itssbprovisioning**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

Macht Methoden verfügbar, mit denen virtuelle Maschinen erstellt und verwaltet werden.

</dd> <dt>

[**Itssbprovisioningpluginnotifysink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

Macht Methoden verfügbar, die RD-Verbindungsbroker über die Bereitstellung virtueller Maschinen benachrichtigen.

</dd> <dt>

[**Itssbresourcenotifizierung**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

Macht Methoden verfügbar, die von RD-Verbindungsbroker verwendet werden, um die Plug-ins von Zustandsänderungen zu benachrichtigen, die in den Sitzungs-, Ziel-und Client Verbindungs Objekten auftreten.

</dd> <dt>

[**Itssbresourcenotificationex**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

Macht Methoden verfügbar, die von RD-Verbindungsbroker verwendet werden, um die Plug-ins von Zustandsänderungen zu benachrichtigen, die in den Sitzungs-, Ziel-und Client Verbindungs Objekten auftreten.

</dd> <dt>

[**Itssbresourceplugin**](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

Macht Methoden verfügbar, mit denen die Funktionen von RD-Verbindungsbroker erweitert werden.

</dd> <dt>

[**Itssbresourcepluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

Macht Methoden verfügbar, mit denen Ressourcen-Plug-ins Objekte wie Sitzungen und Ziele speichern können.

</dd> <dt>

[**Itssbresourcepluginstoreex**](itssbresourcepluginstoreex.md)
</dt> <dd>

Macht Methoden verfügbar, mit denen Ressourcen-Plug-ins Objekte wie Sitzungen und Ziele speichern können.

</dd> <dt>

[**Itssbservicenotifizierung**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

Macht Methoden verfügbar, die von RD-Verbindungsbroker verwendet werden, um die Plug-ins von Zustandsänderungen zu benachrichtigen, die im RD-Verbindungsbroker selbst auftreten.

</dd> <dt>

[**Itssbsession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

Macht Eigenschaften verfügbar, die Informationen zu einer Benutzersitzung speichern.

</dd> <dt>

[**Itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

Macht Eigenschaften verfügbar, die Konfigurations-und Zustandsinformationen zu einem Ziel speichern.

</dd> <dt>

[**Itssbtargetex**](itssbtargetex.md)
</dt> <dd>

Macht Eigenschaften verfügbar, die Konfigurations-und Zustandsinformationen zu einem Ziel speichern.

</dd> <dt>

[**Itssbtargetpropertyset**](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

Leiten Sie von dieser Schnittstelle ab, um einen benutzerdefinierten Zieleigenschaften Satz zu definieren.

</dd> <dt>

[**Itssbtaskinfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

Macht Eigenschaften verfügbar, die vom Remotedesktopverbindung Broker zum Festlegen der Warteschlange eines Plug-ins verwendet werden.

</dd> <dt>

[**Itssbtaskplugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

Macht Methoden verfügbar, die die Aufgaben Warteschlange für Remotedesktopverbindung Broker-Plug-ins aktualisieren.

</dd> <dt>

[**Itssbtaskpluginnotifysink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

Macht Methoden verfügbar, die Status-und Fehlermeldungen zu zu RD-Verbindungsbroker Tasks melden.

</dd> <dt>

[**Iwtssbplugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

Wird verwendet, um die Funktionen des Terminal Dienste-Sitzungs Brokers (TS-Sitzungs Broker) zu erweitern. Implementieren Sie diese Schnittstelle, wenn Sie ein Plug-in bereitstellen möchten, das die Umleitungs Logik des TS-Sitzungs Brokers überschreibt.

</dd> </dl>

 

 