---
title: Remotehardwareverwaltung
description: Remotehardwareverwaltung
ms.assetid: 0ea6d075-6154-4ab9-adcb-e599e5aee614
ms.tgt_platform: multiple
keywords:
- Remotehardwareverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db94c1f50b05f5180504ecef68bf10b1a5a596c9a9f88b96e7c5efb9faaa89bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858730"
---
# <a name="remote-hardware-management"></a>Remotehardwareverwaltung

Windows Die Hardwareverwaltung der Remoteverwaltung soll die Gesamtkosten für die IT-Verwaltung reduzieren, indem die Überwachung und Steuerung von Remotehardwarekomponenten ermöglicht wird, insbesondere vor dem Starten des Systems und nach einem Betriebssystemausfall.

OeMs (Original Equipment Manufacturers) haben eine gemeinsame Architektur entwickelt, um die Notwendigkeit der Hardwareverwaltung zu bewältigen. Ein wichtiger Bestandteil dieser Architektur ist der [*Baseboard-Verwaltungscontroller (Baseboard Management Controller,*](windows-remote-management-glossary.md) BMC). Ein BMC ist ein spezialisiertes Gerät, das den Zustand des Servercomputers überwacht. Der BMC ermöglicht die Remotesteuerung der Serverhardware, ruft Statusdaten ab und empfängt Benachrichtigungen zu kritischen Fehlern und anderen Hardwarestatusänderungen. Ein Skript oder eine Anwendung, das bzw. die einen Remoteserver überwacht, kann Daten vom Server entweder [*in-band,*](windows-remote-management-glossary.md)über das Remotebetriebssystem oder [*out-of-band*](windows-remote-management-glossary.md)direkt vom BMC abrufen.

Ein BMC verfügt über Sensoren, die z. B. erkennen können, wenn der Servercomputer überhintert oder die Stromversorgung außerhalb des zulässigen Bereichs liegt. Es gibt mehrere Standards, um die Architektur von BMC zu definieren. Die [*Intelligente Plattformverwaltungsschnittstelle (Intelligent Platform Management Interface, IPMI)*](windows-remote-management-glossary.md) ist ein solcher Standard, der häufig verwendet wird. Trotz des IPMI-Standards ist der Verwaltungszugriff auf Serverhardware jedoch proprietär und erfordert die Verwendung von Verwaltungstools, die von OEMs bereitgestellt werden. Außerdem wird der Remotezugriff auf einen BMC mithilfe eines speziellen Wire Protocol(RMCP) bereitgestellt, das über nicht dem Standard entsprechende Sicherheitsmechanismen für die Authentifizierung des Zugriffs verfügt.

Mit dem Microsoft [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) und dem IPMI-Treiber können Sie BMC-Daten von Remoteservercomputern über einen WMI-Standardanbieter mit WMI-Klassen abrufen. [](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Sie können zwar ein normales WMI-Skript schreiben, das Remotedaten über DCOM erhält, aber  in vielen Fällen wird die bevorzugte Methode zum Abrufen von IPMI-Daten über das Winrm-Befehlszeilenprogramm oder die [WinRM Scripting-API](winrm-scripting-api.md) oder [die WinRM C++-API](winrm-c---api.md)verwendet. Das Winrm-Hilfsprogramm und die WinRM-Dienst-APIs basieren auf dem WS-Management-Protokoll und können IPMI-Daten von einem lokalen oder Remotecomputer abrufen, ohne DCOM zu verwenden.

Der BMC verfügt auch über eine Ereignisdatenbank namens Systemereignisprotokoll (SEL), die Ereignisse auf dem überwachten Computer aufzeichnet. Sie können nicht abonnieren, dass diese Ereignisse wie mit WMI-Ereignisklassen an ein Skript übermittelt werden. Sie können sie jedoch mithilfe des befehlszeilentools Wecutil.exe abonnieren. Um weitere Informationen zur Verwendung dieses Tools zu erhalten, geben Sie an einer Eingabeaufforderung **wecutil /?** ein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WS-Verwaltungsprotokoll](ws-management-protocol.md)
</dt> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> </dl>

 

 