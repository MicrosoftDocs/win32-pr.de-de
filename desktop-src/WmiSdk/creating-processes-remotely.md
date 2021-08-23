---
description: Sie können Win32 \_ Process.Create verwenden, um ein Skript oder eine Anwendung auf einem Remotecomputer auszuführen. Aus Sicherheitsgründen kann der Prozess jedoch nicht interaktiv sein. Wenn Win32 \_ Process.Create auf dem lokalen Computer aufgerufen wird, kann der Prozess interaktiv sein.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Remoteerstellung von Prozessen mithilfe von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152afa1dba2e745665526ca1628f2a80b8fc8a527d16abebc4b9082d4c5c4341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568850"
---
# <a name="creating-processes-remotely-using-wmi"></a>Remoteerstellung von Prozessen mithilfe von WMI

Sie können [**Win32 \_ Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) verwenden, um ein Skript oder eine Anwendung auf einem Remotecomputer auszuführen. Aus Sicherheitsgründen kann der Prozess jedoch nicht interaktiv sein. Wenn **Win32 \_ Process.Create** auf dem lokalen Computer aufgerufen wird, kann der Prozess interaktiv sein.

> [!WARNING]
> In diesem Thema wird das allgemeine Verfahren zum Erstellen eines Remoteprozesses mit WMI beschrieben. Wenn Sie einfach nur ein Skript auf einem Remotesystem ausführen möchten, finden Sie weitere Informationen unter Herstellen einer [Remoteverbindung mit WMI ab Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)oder [Herstellen einer Verbindung mit WMI auf einem Remotecomputer mithilfe von Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md). Weitere allgemeine Informationen zum Remoting mit PowerShell finden Sie unter [Ausführen von Remotebefehlen.](https://technet.microsoft.com/library/dd819505.aspx)

 

Der Remoteprozess verfügt über keine Benutzeroberfläche, ist aber im **Task-Manager** aufgeführt. Ein lokal erstellter Prozess kann unter einem beliebigen Konto ausgeführt werden, wenn das Konto über die Berechtigung **Execute Method** für den \\ Cimv2-Stammnamespace verfügt. Ein remote erstellter Prozess kann unter einem beliebigen Konto ausgeführt werden, wenn das Konto über die Berechtigungen **Execute Method** und **Remote Enable** für \\ root cimv2 verfügt. Die Berechtigungen **Execute Method (Methode ausführen)** und **Remote Enable (Remote aktivieren)** werden in der WMI-Steuerung im Systemsteuerung festgelegt. Weitere Informationen finden Sie unter [Festlegen der Namespacesicherheit mit dem WMI-Steuerelement](setting-namespace-security-with-the-wmi-control.md).

Sie können [**Win32 \_ ScheduledJob.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) verwenden, um einen interaktiven Prozess remote zu erstellen. Prozesse, die von **Win32 \_ ScheduledJob.Create** gestartet wurden, werden jedoch unter dem LocalSystem-Konto ausgeführt, das zu viele Berechtigungen gewähren kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sichern einer WMI-Remoteverbindung](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Herstellen einer Verbindung mit einer dritten Computerdelegierung](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
