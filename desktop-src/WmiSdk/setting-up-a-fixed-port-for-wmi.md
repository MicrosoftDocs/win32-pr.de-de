---
description: WMI wird als Teil eines Freigegebenen Diensthosts mit Ports ausgeführt, die standardmäßig über DCOM zugewiesen sind. Sie können den WMI-Dienst jedoch so einrichten, dass er als einziger Prozess auf einem separaten Host ausgeführt wird, und einen festen Port angeben.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Einrichten eines festen Ports für WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b97ee9d0f2f407c0cae2c9c1466a1904cf79eaecb353b94ac11bb3373367ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050248"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a>Einrichten eines festen Ports für WMI

WMI wird als Teil eines Freigegebenen Diensthosts mit Ports ausgeführt, die standardmäßig über DCOM zugewiesen sind. Sie können den WMI-Dienst jedoch so einrichten, dass er als einziger Prozess auf einem separaten Host ausgeführt wird, und einen festen Port angeben.

Das folgende Verfahren ist ein automatisiertes Setup, mit dem WMI über einen festen Port verfügen kann. Die Prozedur verwendet das [**Befehlszeilentool winmgmt.**](winmgmt.md)

**So richten Sie einen festen Port für WMI ein**

1.  Geben Sie an der Eingabeaufforderung **winmgmt -standalonehost ein.**
2.  Beenden Sie den WMI-Dienst, indem Sie den Befehl **net stop "Windows Management Instrumentation"** eingeben, oder verwenden Sie den Kurznamen **net stop winmgmt.**
3.  Starten Sie den WMI-Dienst erneut auf einem neuen Diensthost neu, indem Sie **net start "Windows Management Instrumentation"** oder **net start winmgmt eingeben.**
4.  Richten Sie eine neue Portnummer für den WMI-Dienst ein, indem Sie **netsh firewall add tcp 24158 WMIFixedPort eingeben.**

Um alle Änderungen rückgängig zu machen, die Sie an WMI vornehmen, geben Sie **winmgmt /sharedhost** ein, beenden und starten Sie dann den winmgmt-Dienst erneut.

## <a name="examples"></a>Beispiele

Ein Skript, das einen festen Port für WMI ein richtet, finden Sie im folgenden [Skriptkatalog-Codebeispiel.](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )

oder ein PowerShell-Codebeispiel, das die WMI-Porteinstellungen aktiviert oder deaktiviert, finden Sie im [Beispiel Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) im TechNet-Katalog.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Problembehandlung bei WMI-Remoteverbindungen](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[Anbieterhosting und -sicherheit](provider-hosting-and-security.md)
</dt> </dl>

 

 



