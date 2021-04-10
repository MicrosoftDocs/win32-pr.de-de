---
description: WMI wird als Dienst mit dem anzeigen Amen &\# 0034; ausgeführt. Windows-Verwaltungsinstrumentation&\# 0034; und der Dienst Name &\# 0034; WinMgmt&\# 0034;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Starten und Beenden des WMI-Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215325"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Starten und Beenden des WMI-Dienstanbieter

WMI wird als Dienst mit dem anzeigen Amen "Windows-Verwaltungsinstrumentation" und dem Dienstnamen "winmgmt" ausgeführt. WMI wird automatisch beim Systemstart unter dem Konto "LocalSystem" ausgeführt. Wenn WMI nicht ausgeführt wird, wird es automatisch gestartet, wenn die erste Verwaltungs Anwendung oder das erste Skript eine Verbindung mit einem WMI-Namespace anfordert.

Abhängig von der Betriebssystemversion, die auf dem System ausgeführt wird, sind mehrere andere Dienste abhängig von der Betriebssystemversion, die auf dem WMI-Dienst

## <a name="starting-winmgmt-service"></a>WinMgmt-Dienst wird gestartet

Im folgenden Verfahren wird beschrieben, wie der WMI-Dienst gestartet wird.

**So starten Sie den WinMgmt-Dienst**

1.  Geben Sie an einer Eingabeaufforderung **net** **Start** **WinMgmt** ein \[ */<switch>* \] .

    Weitere Informationen zu den verfügbaren Switches finden Sie unter [WinMgmt](winmgmt.md). Verwenden Sie das integrierte Administrator Konto oder ein Konto in der Gruppe Administratoren, die mit erhöhten Rechten ausgeführt wird, um den WMI-Dienst zu starten. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).

2.  Andere Dienste, die vom WMI-Dienst abhängig sind, z. b. der SMS-Agent-Host oder die Windows-Firewall, werden nicht automatisch neu gestartet.

## <a name="stopping-winmgmt-service"></a>WinMgmt-Dienst wird beendet.

Im folgenden Verfahren wird beschrieben, wie der WMI-Dienst beendet wird.

**So verhindern Sie den WinMgmt-Dienst**

1.  Geben Sie an einer Eingabeaufforderung **net stoppt WinMgmt** ein.

2.  Andere Dienste, die vom WMI-Dienst abhängig sind, werden ebenfalls angehalten, z. b. SMS-Agent-Host oder Windows-Firewall

## <a name="examples"></a>Beispiele

Die TechNet Gallery enthält das [WMI-Service Watchdog-Skript](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), das beschreibt, wie der WinMgmt-Dienst mit PowerShell Programm gesteuert heruntergefahren und neu gestartet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der WMI-Command-Line Tools](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



