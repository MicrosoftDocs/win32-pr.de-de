---
description: WMI wird als Dienst mit dem Anzeigenamen &\# 0034;Windows-Verwaltungsinstrumentation&0034; und dem Dienstnamen \# &\# 0034;winmgmt&\# 0034; ausgeführt.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Starten und Beenden des WMI-Diensts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b22524d356bad5f23f4ca1cc8a3e7c68e69fd83f0dc38e64eba70bc1812436f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315008"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Starten und Beenden des WMI-Diensts

WMI wird als Dienst mit dem Anzeigenamen "Windows Verwaltungsinstrumentation" und dem Dienstnamen "winmgmt" ausgeführt. WMI wird automatisch beim Systemstart unter dem Konto LocalSystem ausgeführt. Wenn WMI nicht ausgeführt wird, wird es automatisch gestartet, wenn die erste Verwaltungsanwendung oder das erste Skript eine Verbindung mit einem WMI-Namespace an fordert.

Abhängig von der Betriebssystemversion, unter der das System ausgeführt wird, sind mehrere andere Dienste vom WMI-Dienst abhängig.

## <a name="starting-winmgmt-service"></a>Starten des Winmgmt-Diensts

Im folgenden Verfahren wird das Starten des WMI-Diensts beschrieben.

**So starten Sie den Winmgmt-Dienst**

1.  Geben Sie an einer Eingabeaufforderung **net** **start** **winmgmt** \[ */<switch>* \] ein.

    Weitere Informationen zu den verfügbaren Switches finden Sie unter [winmgmt](winmgmt.md). Sie verwenden das integrierte Administratorkonto oder ein Konto in der Gruppe Administratoren, das mit erhöhten Rechten ausgeführt wird, um den WMI-Dienst zu starten. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](user-account-control-and-wmi.md)

2.  Andere Dienste, die vom WMI-Dienst abhängig sind, z. B. sms agent host oder Windows Firewall, werden nicht automatisch neu gestartet.

## <a name="stopping-winmgmt-service"></a>Beenden des Winmgmt-Diensts

Im folgenden Verfahren wird beschrieben, wie sie den WMI-Dienst beenden.

**So beenden Sie den Winmgmt-Dienst**

1.  Geben Sie an einer Eingabeaufforderung **net stop winmgmt ein.**

2.  Andere Dienste, die vom WMI-Dienst abhängig sind, werden ebenfalls anhalten, z. B. SMS-Agent-Host oder Windows Firewall.

## <a name="examples"></a>Beispiele

Der TechNet-Katalog enthält das [Watchdogskript](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282)für den WMI-Dienst, das beschreibt, wie der winmgmt-Dienst mit PowerShell programmgesteuert heruntergefahren und neu gestartet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der WMI-Command-Line Tools](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



