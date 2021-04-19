---
description: WMI wird als Teil eines Hosts für gemeinsame Dienste ausgeführt, wobei Ports standardmäßig über DCOM zugewiesen werden. Sie können jedoch den WMI-Dienst so einrichten, dass er als einziger Prozess auf einem separaten Host ausgeführt wird, und einen festgelegten Port angeben.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Einrichten eines festgelegten Ports für WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362720"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a>Einrichten eines festgelegten Ports für WMI

WMI wird als Teil eines Hosts für gemeinsame Dienste ausgeführt, wobei Ports standardmäßig über DCOM zugewiesen werden. Sie können jedoch den WMI-Dienst so einrichten, dass er als einziger Prozess auf einem separaten Host ausgeführt wird, und einen festgelegten Port angeben.

Das folgende Verfahren ist ein automatisiertes Setup, mit dem WMI über einen Fixed-Port verfügen kann. Die Prozedur verwendet das [**WinMgmt**](winmgmt.md) -Befehlszeilen Tool.

**So richten Sie einen Fixed-Port für WMI ein**

1.  Geben Sie an der Eingabeaufforderung **winmgmt-standalonehost** ein.
2.  Geben Sie den WMI-Dienst an, indem Sie den Befehl **net-"Windows-Verwaltungsinstrumentation"** eingeben, oder verwenden Sie den Kurznamen von net-" **WinMgmt** ".
3.  Starten Sie den WMI-Dienst erneut auf einem neuen Dienst Host, indem Sie **net Start "Windows-Verwaltungsinstrumentation" oder "** **net Start WinMgmt** " eingeben.
4.  Richten Sie eine neue Portnummer für den WMI-Dienst ein, indem **Sie netsh Firewall Add portopening TCP 24158 wmifixedport** eingeben.

Wenn Sie an WMI vorgenommene Änderungen rückgängig machen möchten, geben Sie **WinMgmt/sharedhost** ein, und starten Sie dann den WinMgmt-Dienst erneut.

## <a name="examples"></a>Beispiele

Ein Skript, in dem ein fester Port für WMI eingerichtet wird, finden Sie im folgenden Skript Katalog- [Codebeispiel](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).

oder ein PowerShell-Codebeispiel, das die WMI-Port Einstellungen aktiviert oder deaktiviert, finden Sie im Beispiel für [Set-wmisingleport](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) in der TechNet Gallery.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Problembehandlung bei WMI-Remote Verbindungen](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md)
</dt> </dl>

 

 



