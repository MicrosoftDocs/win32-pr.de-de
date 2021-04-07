---
description: Sie können Win32 \_ Process. Create verwenden, um ein Skript oder eine Anwendung auf einem Remote Computer auszuführen. Aus Sicherheitsgründen kann der Prozess jedoch nicht interaktiv sein. Wenn Win32 \_ Process. Create auf dem lokalen Computer aufgerufen wird, kann der Prozess interaktiv sein.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Remote Erstellung von Prozessen mithilfe von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758748"
---
# <a name="creating-processes-remotely-using-wmi"></a>Remote Erstellung von Prozessen mithilfe von WMI

Sie können [**Win32 \_ Process. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) verwenden, um ein Skript oder eine Anwendung auf einem Remote Computer auszuführen. Aus Sicherheitsgründen kann der Prozess jedoch nicht interaktiv sein. Wenn **Win32 \_ Process. Create** auf dem lokalen Computer aufgerufen wird, kann der Prozess interaktiv sein.

> [!WARNING]
> In diesem Thema wird das allgemeine Verfahren zum Erstellen eines Remote Prozesses mit WMI beschrieben. Wenn Sie einfach ein Skript auf einem Remote System ausführen möchten, finden Sie weitere Informationen unter Herstellen einer Remote [Verbindung mit WMI ab Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)oder [Herstellen einer Verbindung mit WMI auf einem Remote Computer mithilfe von Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md). Weitere allgemeine Informationen zum Remoting mit PowerShell finden Sie unter [Ausführen von Remote Befehlen](https://technet.microsoft.com/library/dd819505.aspx).

 

Der Remote Prozess hat keine Benutzeroberfläche, wird aber im Task- **Manager** aufgeführt. Ein lokal erstelltes Prozess kann unter jedem Konto ausgeführt werden, wenn das Konto über die **Execute Method** -Berechtigung für den root \\ CIMV2-Namespace verfügt. Ein Remote erstellter Prozess kann unter jedem Konto ausgeführt werden, wenn das Konto über die **Execute-Methode** und die **Remote enable** -Berechtigung für root \\ CIMV2 verfügt. Die **Execute-Methode** und die **Remote Aktivierungs** Berechtigungen werden in der Systemsteuerung in der WMI-Steuerung festgelegt. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.

Sie können [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) verwenden, um einen interaktiven Prozess Remote zu erstellen. Prozesse, die von **Win32 \_ ScheduledJob. Create** gestartet werden, werden jedoch unter dem Konto LocalSystem ausgeführt, das zu viele Berechtigungen gewähren kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Herstellen einer Verbindung mit einer dritten Computer Delegierung](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
