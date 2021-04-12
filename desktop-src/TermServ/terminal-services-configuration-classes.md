---
title: Remotedesktopdienste Konfigurations Klassen
description: Der WMI-Anbieter für die Remotedesktopdienste Konfiguration stellt die folgenden Klassen bereit. Es folgt eine Abbildung.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc9c58be85b8b4efc35495f35902ab67b35ad153
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390362"
---
# <a name="remote-desktop-services-configuration-classes"></a>Remotedesktopdienste Konfigurations Klassen

Der WMI-Anbieter für die Remotedesktopdienste Konfiguration stellt die folgenden Klassen bereit. Es folgt eine Abbildung.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**CIM- \_ Element Setting**](cim-elementsetting.md)
</dt> <dd>

Stellt die Zuordnung zwischen verwalteten Systemelementen und der Einstellungs Klasse dar, die für Sie definiert ist.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

Die Basisklasse für alle Systemkomponenten, die abstrakte Systemkomponenten, z. b. profile, Prozesse oder Systemfunktionen, in Form logischer Geräte darstellen.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

Die Basisklasse für die System Element Hierarchie.

</dd> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dd>

Stellt Konfigurations bezogene und operative Parameter für ein oder mehrere verwaltete Systemelemente dar.

</dd> <dt>

[**Win32- \_ Terminal**](win32-terminal.md)
</dt> <dd>

stellt ein Terminal dar.

</dd> <dt>

[**Win32 \_ terminalerror**](win32-terminalerror.md)
</dt> <dd>

Stellt einen Terminal Fehler dar.

</dd> <dt>

[**Win32 \_ Terminalservice**](win32-terminalservice.md)
</dt> <dd>

eine Unterklasse der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse. [**Win32 \_ Terminalservice**](win32-terminalservice.md) stellt die- **Element** Eigenschaft der [**Win32 \_ terminalservicedesetting**](win32-terminalservicetosetting.md) -Zuordnung dar.

</dd> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> <dd>

stellt die Konfiguration für einen Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) dar.

</dd> <dt>

[**Win32 \_ terminalservicede Setting**](win32-terminalservicetosetting.md)
</dt> <dd>

stellt die Zuordnung zwischen einer Instanz der [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Klasse und der Einstellung einer bestimmten [**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md) -Eigenschaft dar.

</dd> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dd>

stellt die Einstellungen dar, die auf ein Terminal angewendet werden können.

</dd> <dt>

[**Win32 \_ terminalterminalsetting**](win32-terminalterminalsetting.md)
</dt> <dd>

stellt die Zuordnung zwischen einem Terminal und seinen Konfigurationseinstellungen dar.

</dd> <dt>

[**Win32- \_ Konto**](win32-tsaccount.md)
</dt> <dd>

ermöglicht das Löschen eines Kontos, das im [**Win32- \_ Terminal**](win32-terminal.md) vorhanden ist, sowie das Ändern vorhandener Berechtigungen.

</dd> <dt>

[**Win32- \_ tsclientsetting**](win32-tsclientsetting.md)
</dt> <dd>

definiert Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse, die mit der Verbindungsrichtlinie verknüpft ist.

</dd> <dt>

[**Win32-Server für die Ermittlung von "t" \_**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

Enthält Details zum ermittelten Remotedesktop-Lizenzserver.

</dd> <dt>

[**Win32- \_ tsenvironmentsetting**](win32-tsenvironmentsetting.md)
</dt> <dd>

definiert die Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse einschließlich der ersten Programm Richtlinie.

</dd> <dt>

[**Win32-Einstellung für "" \_**](win32-tsgeneralsetting.md)
</dt> <dd>

stellt allgemeine Einstellungen des Terminals dar, z. b. die Verschlüsselungs Stufe und das Transportprotokoll.

</dd> <dt>

[**Win32-Anmelde \_ Einstellung**](win32-tslogonsetting.md)
</dt> <dd>

definiert Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse im Zusammenhang mit der Client Anmeldung.

</dd> <dt>

[**Win32-Datei "t-Network \_ adapterlistsetting"**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

Listet die Netzwerkadapter auf, die auf der Grundlage des angegebenen Terminal Protokolls und der Transportmethode für ein [**Win32- \_ Terminal**](win32-terminal.md)konfiguriert werden können.

</dd> <dt>

[**Win32-Datei "t-Network \_ adaptersetting"**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

definiert verschiedene Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse einschließlich Eigenschaften im Zusammenhang mit dem Netzwerkadapter und die maximal zulässige Anzahl von Verbindungen.

</dd> <dt>

[**Win32- \_ tspermissionssetting**](win32-tspermissionssetting.md)
</dt> <dd>

enthält eine Methode zum Hinzufügen neuer Konten zum Terminal und eine Methode zum Wiederherstellen der Standard Berechtigungen für ein Terminal.

</dd> <dt>

[**Win32-"t- \_ remotecontrolsetting"**](win32-tsremotecontrolsetting.md)
</dt> <dd>

definiert die Konfigurationseinstellungen für die Remote Steuerung für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse.

</dd> <dt>

[**Win32- \_ tssessiondirectory**](win32-tssessiondirectory.md)
</dt> <dd>

Definiert die Konfigurationseinstellungen für den Remotedesktopverbindung Broker (RD-Verbindungsbroker) für die Win32-Klasse " [**\_ tssessiondirectorysetting**](win32-tssessiondirectorysetting.md) ".

</dd> <dt>

[**Win32- \_ tssessiondirectorysetting**](win32-tssessiondirectorysetting.md)
</dt> <dd>

Stellt die Zuordnung zwischen einer Instanz der [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Klasse und einer Instanz der [**Win32 \_ tssessiondirectory**](win32-tssessiondirectory.md) -Klasse dar.

</dd> <dt>

[**Win32- \_ tssessionsetting**](win32-tssessionsetting.md)
</dt> <dd>

definiert Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse, z. b. Zeitlimits und Aktionen zum Trennen und Wiederherstellen von Verbindungen.

</dd> <dt>

[**Win32- \_ virtualialip**](win32-tsvirtualip.md)
</dt> <dd>

Definiert IP (Internet Protocol)-Virtualisierungseinstellungen für einen RD-Sitzungshost Server.

</dd> <dt>

[**Win32-Datei " \_ tvirtualipsetting"**](win32-tsvirtualipsetting.md)
</dt> <dd>

Stellt die Zuordnung zwischen einer [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Element Klasse und einer Win32-Klasse für die Klasse " [**\_ tvirtualip**](win32-tsvirtualip.md) Setting" dar.

</dd> </dl>

In der folgenden Abbildung werden die Beziehungen zwischen diesen Klassen gezeigt.

![die Beziehungen zwischen unterstützten Klassen](images/tswmi.png)

 

 