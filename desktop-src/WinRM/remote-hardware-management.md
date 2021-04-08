---
title: Remote Hardware Verwaltung
description: Remote Hardware Verwaltung
ms.assetid: 0ea6d075-6154-4ab9-adcb-e599e5aee614
ms.tgt_platform: multiple
keywords:
- Remote Hardware Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bbb470d513b49d2158865c4c42051cc16856ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727393"
---
# <a name="remote-hardware-management"></a>Remote Hardware Verwaltung

Windows-Remoteverwaltung Hardware Verwaltung soll die Gesamtkosten für die IT-Verwaltung verringern, indem Sie die Überwachung und Steuerung von Remote Hardwarekomponenten bereitstellt, insbesondere vor dem Start des Systems und nach einem Betriebssystem Fehler.

OEMs (Original Equipment Manufacturers) haben eine gängige Architektur entwickelt, die den Bedarf an Hardware Verwaltung gerecht wird. Ein wichtiger Teil dieser Architektur ist der [*Baseboard-Verwaltungs Controller*](windows-remote-management-glossary.md) (BMC). Ein BMC ist ein spezielles Gerät, das den Status des Server Computers überwacht. Der BMC bietet Remote Steuerung der Server Hardware, ruft Statusdaten ab und empfängt Benachrichtigungen zu kritischen Fehlern und anderen Hardware Statusänderungen. Skripts oder Anwendungen, die einen Remote Server überwachen, können Daten vom Server entweder [*in-Band*](windows-remote-management-glossary.md), über das Remote Betriebssystem oder [*out-of-Band*](windows-remote-management-glossary.md)direkt vom BMC abrufen.

Ein BMC verfügt über Sensoren, die erkennen können, z. b. wenn der Server Computer eine Überhitzung aufweist oder die Spannung außerhalb des zulässigen Bereichs liegt. Zum Definieren der Architektur von BMC gibt es mehrere Standards. Die [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) ist ein solcher Standard, der häufig verwendet wird. Trotz des IPMI-Standards ist der Verwaltungs Zugriff auf die Server Hardware proprietäre und erfordert die Verwendung von Verwaltungs Tools, die von OEMs bereitgestellt werden. Außerdem wird der Remote Zugriff auf einen BMC mithilfe eines spezialisierten Wire-Protokolls (Remote Management Control Protocol, RMCP) bereitgestellt, das über nicht standardmäßige Sicherheitsmechanismen für die Authentifizierung des Zugriffs verfügt.

Mit dem Microsoft [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) und dem IPMI-Treiber können Sie BMC-Daten von Remote Server Computern über einen standardmäßigen WMI-Anbieter mit WMI- [Klassen](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)abrufen. Sie können zwar ein normales WMI-Skript schreiben, das Remote Daten über DCOM erhält, aber in vielen Fällen ist die bevorzugte Methode zum Abrufen von IPMI-Daten das **WinRM** -Befehlszeilen Dienstprogramm oder die [WinRM-Skript-API](winrm-scripting-api.md) oder die [WinRM-C++-API](winrm-c---api.md). Das WinRM-Hilfsprogramm und die WinRM-Dienst-APIs basieren auf dem WS-Management-Protokoll und können IPMI-Daten von lokalen Computern oder Remote Computern abrufen, ohne DCOM zu verwenden.

Der BMC verfügt auch über eine Ereignis Datenbank mit dem Namen System Ereignisprotokoll (SEL), das Ereignisse auf dem überwachten Computer aufzeichnet. Sie können nicht abonnieren, dass diese Ereignisse wie bei WMI-Ereignis Klassen an ein Skript übermittelt werden. Sie können Sie jedoch mit dem Befehlszeilen Tool Wecutil.exe abonnieren. Weitere Informationen zur Verwendung dieses Tools erhalten Sie, wenn Sie an einer Eingabeaufforderung **wecutil/?** eingeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WS-Verwaltungsprotokoll](ws-management-protocol.md)
</dt> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> </dl>

 

 