---
title: Remotedesktopdienste-Konfigurationsklassen
description: Der Remotedesktopdienste Configuration WMI-Anbieter bietet die folgenden Klassen. Es folgt eine Abbildung.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40784e1e0c9e0387b8d6ff60193639032f7e0cbe5e34c4a8b35aeb32cc37cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000125"
---
# <a name="remote-desktop-services-configuration-classes"></a>Remotedesktopdienste-Konfigurationsklassen

Der Remotedesktopdienste Configuration WMI-Anbieter bietet die folgenden Klassen. Es folgt eine Abbildung.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**\_CIM-ElementSetting**](cim-elementsetting.md)
</dt> <dd>

Stellt die Zuordnung zwischen verwalteten Systemelementen und der für sie definierten Einstellungsklasse dar.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

Die Basisklasse für alle Systemkomponenten, die abstrakte Systemkomponenten wie Profile, Prozesse oder Systemfunktionen in Form von logischen Geräten darstellen.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

Die Basisklasse für die Systemelementhierarchie.

</dd> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dd>

Stellt konfigurationsbezogene und betriebsbezogene Parameter für ein oder mehrere verwaltete Systemelemente dar.

</dd> <dt>

[**Win32-Terminal \_**](win32-terminal.md)
</dt> <dd>

stellt ein Terminal dar.

</dd> <dt>

[**Win32 \_ TerminalError**](win32-terminalerror.md)
</dt> <dd>

Stellt einen Terminalfehler dar.

</dd> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dd>

eine Unterklasse der [**Win32 \_ Service-Klasse.**](/windows/desktop/CIMWin32Prov/win32-service) [**Win32 \_ TerminalService**](win32-terminalservice.md) stellt die **Element-Eigenschaft** der [**Win32 \_ TerminalServiceToSetting-Zuordnung**](win32-terminalservicetosetting.md) dar.

</dd> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> <dd>

stellt die Konfiguration für einen Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server dar.

</dd> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dd>

stellt die Zuordnung zwischen einer Instanz der [**Win32 \_ TerminalService-Klasse**](win32-terminalservice.md) und der Einstellung einer bestimmten [**Win32 \_ TerminalServiceSetting-Eigenschaft**](win32-terminalservicesetting.md) dar.

</dd> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dd>

stellt die Einstellungen dar, die auf ein Terminal angewendet werden können.

</dd> <dt>

[**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dd>

stellt die Zuordnung zwischen einem Terminal und seinen Konfigurationseinstellungen dar.

</dd> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> <dd>

ermöglicht das Löschen eines Kontos, das im [**\_ Win32-Terminal**](win32-terminal.md) vorhanden ist, und das Ändern vorhandener Berechtigungen.

</dd> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> <dd>

definiert Konfigurationseinstellungen für die [**Win32 \_ Terminal-Klasse**](win32-terminal.md) im Zusammenhang mit der Verbindungsrichtlinie.

</dd> <dt>

[**Win32 \_ TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

Enthält Details zum gefundenen Remotedesktop Lizenzservers.

</dd> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> <dd>

definiert die Konfigurationseinstellungen für die [**Win32 \_ Terminal-Klasse,**](win32-terminal.md) einschließlich der anfänglichen Programmrichtlinie.

</dd> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dd>

stellt allgemeine Einstellungen des Terminals dar, z. B. die Verschlüsselungsebene und das Transportprotokoll.

</dd> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> <dd>

definiert Konfigurationseinstellungen für die [**Win32 \_ Terminal-Klasse**](win32-terminal.md) im Zusammenhang mit der Clientanmeldung.

</dd> <dt>

[**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

Listet die Netzwerkadapter auf, die basierend auf dem angegebenen Terminalprotokoll und der angegebenen Transportmethode für ein [**\_ Win32-Terminal**](win32-terminal.md)konfiguriert werden können.

</dd> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

definiert verschiedene Konfigurationseinstellungen für die [**Win32 \_ Terminal-Klasse,**](win32-terminal.md) einschließlich Eigenschaften im Zusammenhang mit dem Netzwerkadapter und der maximalen Anzahl zulässiger Verbindungen.

</dd> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> <dd>

enthält eine Methode zum Hinzufügen neuer Konten zum Terminal und eine Methode zum Wiederherstellen der Standardberechtigungen für ein Terminal.

</dd> <dt>

[**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md)
</dt> <dd>

definiert die Konfigurationseinstellungen für die Remotesteuerung für die [**Win32 \_ Terminal-Klasse.**](win32-terminal.md)

</dd> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dd>

Definiert die Remotedesktopverbindung Broker-Konfigurationseinstellungen (RD-Verbindungsbroker) für die [**Win32 \_ TSSessionDirectorySetting-Klasse.**](win32-tssessiondirectorysetting.md)

</dd> <dt>

[**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md)
</dt> <dd>

Stellt die Zuordnung zwischen einer Instanz der [**Win32 \_ TerminalService-Klasse**](win32-terminalservice.md) und einer Instanz der [**Win32 \_ TSSessionDirectory-Klasse**](win32-tssessiondirectory.md) dar.

</dd> <dt>

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> <dd>

definiert Konfigurationseinstellungen für die [**Win32 \_ Terminal-Klasse,**](win32-terminal.md) z. B. Zeitlimits und Aktionen zum Trennen und Wiederherstellen der Verbindung.

</dd> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> <dd>

Definiert IP-Virtualisierungseinstellungen (Internetprotokoll) für einen RD-Sitzungshost Server.

</dd> <dt>

[**Win32 \_ TSVirtualIPSetting**](win32-tsvirtualipsetting.md)
</dt> <dd>

Stellt die Zuordnung zwischen einer [**Win32 \_ TerminalService-Elementklasse**](win32-terminalservice.md) und einer [**Win32 \_ TSVirtualIP-Einstellungsklasse**](win32-tsvirtualip.md) dar.

</dd> </dl>

Die folgende Abbildung zeigt die Beziehungen zwischen diesen Klassen.

![die Beziehungen zwischen unterstützten Klassen](images/tswmi.png)

 

 