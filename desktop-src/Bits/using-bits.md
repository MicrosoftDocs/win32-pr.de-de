---
title: Verwenden von Bits
description: Verwenden von Bits
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Background Intelligent Transfer Service, Aufgaben
- Datei Übertragungs Bits
- Verwenden von Bits-Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340523"
---
# <a name="using-bits"></a>Verwenden von Bits

In den folgenden Schritten wird gezeigt, wie eine Dateiübertragung mithilfe der  [Schnittstellen](bits-interfaces.md)Background Intelligent Transfer Service (Bits) ausgeführt wird.

**So führen Sie eine Dateiübertragung aus**

1.  [Herstellen einer Verbindung mit dem BITS-Dienst](connecting-to-the-bits-service.md)
2.  [Erstellen eines Übertragungs Auftrags](creating-a-job.md)
3.  [Hinzufügen von Dateien zum Auftrag](adding-files-to-a-job.md)
4.  [Starten des Auftrags](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Ermitteln, ob Bits die Dateien erfolgreich übertragen haben](determining-the-status-of-a-job.md)
6.  [Auftrag beenden](completing-and-canceling-a-job.md)

In den vorherigen Schritten wird gezeigt, wie Sie Dateien mithilfe der Standardeigenschaftswerte für einen Auftrag übertragen. Sie können das Standardverhalten ändern, indem Sie einen oder mehrere der Eigenschaftswerte des Auftrags ändern. Beispielsweise können Sie die Priorität ändern, mit der der Auftrag in Bezug auf andere Aufträge in der Warteschlange verarbeitet wird, eine eigene Proxy Einstellung angeben und registrieren, um eine Ereignis Benachrichtigung zu erhalten, wenn die Dateien von Bits übertragen wurden. Weitere Informationen finden Sie unter [festlegen und Abrufen der Eigenschaften eines Auftrags](setting-and-retrieving-the-properties-of-a-job.md).

Windows PowerShell bietet einen einfachen Mechanismus zum Verwalten von vielen Bits-Aufgaben. Dieser Abschnitt enthält die folgenden Themen, die zeigen, wie Windows PowerShell-Cmdlets mit Bits verwendet werden:

-   [Erstellen von BITS-Übertragungsaufträgen mithilfe von Windows PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Verwenden von WinRM Windows PowerShell-Cmdlets zum Verwalten von BITS-Übertragungsaufträgen](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [Verwenden von WMI-Windows PowerShell-Cmdlets zum Verwalten des BITS Compact-Servers](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> Ab Windows 10, Version 1607, können Sie auch PowerShell-Cmdlets ausführen und BITSAdmin oder andere Anwendungen verwenden, die die Bits- [Schnittstellen](bits-interfaces.md) über eine PowerShell-Remote Befehlszeile verwenden, die mit einem anderen Computer (physisch oder virtuell) verbunden ist. Diese Funktion ist nicht verfügbar, wenn Sie eine [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) -Befehlszeile für eine virtuelle Maschine auf demselben physischen Computer verwenden, und Sie ist nicht verfügbar, wenn Sie WinRM-Cmdlets verwenden.
>
> Ein aus einer PowerShell-Remote Sitzung erstellter BITS-Auftrag wird unter dem Benutzerkonto Kontext der Sitzung ausgeführt und wird nur fortgesetzt, wenn mindestens eine aktive lokale Anmelde Sitzung oder eine PowerShell-Remote Sitzung mit diesem Benutzerkonto verknüpft ist. Weitere Informationen finden [Sie unter So verwalten Sie PowerShell-Remote Sitzungen](using-windows-powershell-to-create-bits-transfer-jobs.md).

 

Dieser Abschnitt enthält auch die folgenden Themen:

-   [Bewährte Methoden bei der Verwendung von Bits](best-practices-when-using-bits.md)
-   [Auflisten von Aufträgen in der Übertragungs Warteschlange](enumerating-jobs-in-the-transfer-queue.md)
-   [Auflisten von Dateien in einem Auftrag](enumerating-files-in-a-job.md)
-   [Behandlung von Fehlern](handling-errors.md)
-   [Abrufen der Antwort von einem Upload-Antwort-Auftrag](retrieving-the-reply-from-an-upload-reply-job.md)

Beispielcode, der die Bits-Schnittstellen verwendet, finden Sie unter [Bits-Beispiele und-Tools](bits-samples-and-tools.md).

 

 