---
title: Verwenden von BITS
description: Verwenden von BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Background Intelligent Transfer Service,tasks
- Bits für die Dateiübertragung
- Verwenden von BITS-BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b301c1d96956bca924d99ef41ade3032f58dc4e194b420069cbae1071c916b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801160"
---
# <a name="using-bits"></a>Verwenden von BITS

Die folgenden Schritte zeigen, wie sie eine Dateiübertragung mithilfe [](bits-interfaces.md)der BITS-Schnittstellen (Background Intelligent Transfer Service) durchführen.

**So führen Sie eine Dateiübertragung aus**

1.  [Verbinden zum BITS-Dienst](connecting-to-the-bits-service.md)
2.  [Erstellen eines Übertragungsauftrags](creating-a-job.md)
3.  [Hinzufügen von Dateien zum Auftrag](adding-files-to-a-job.md)
4.  [Starten des Auftrags](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Ermitteln, ob bits die Dateien erfolgreich übertragen hat](determining-the-status-of-a-job.md)
6.  [Abschließen des Auftrags](completing-and-canceling-a-job.md)

Die vorherigen Schritte zeigen, wie Dateien mithilfe der Standardeigenschaftswerte für einen Auftrag übertragen werden. Sie können das Standardverhalten ändern, indem Sie einen oder mehrere Eigenschaftswerte des Auftrags ändern. Beispielsweise können Sie die Priorität ändern, mit der der Auftrag relativ zu anderen Aufträgen in der Warteschlange verarbeitet wird, Eine eigene Proxyeinstellung angeben und sich registrieren, um ereignisbenachrichtigungen zu erhalten, wenn BITS die Dateien übertragen hat. Weitere Informationen finden Sie unter [Festlegen und Abrufen der Eigenschaften eines Auftrags.](setting-and-retrieving-the-properties-of-a-job.md)

Windows PowerShell bietet einen einfachen Mechanismus zum Verwalten vieler BITS-Aufgaben. Dieser Abschnitt enthält die folgenden Themen, in denen die Verwendung Windows PowerShell Cmdlets mit BITS veranschaulicht wird:

-   [Erstellen von BITS-Übertragungsaufträgen mithilfe von Windows PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Verwenden von WinRM Windows PowerShell-Cmdlets zum Verwalten von BITS-Übertragungsaufträgen](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [Verwenden von WMI Windows PowerShell Cmdlets zum Verwalten des BITS Compact-Servers](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> Ab Windows 10 Version 1607 können Sie auch PowerShell-Cmdlets ausführen und BITSAdmin oder andere [](bits-interfaces.md) Anwendungen verwenden, die die BITS-Schnittstellen über eine PowerShell-Remotebefehlszeile verwenden, die mit einem anderen Computer verbunden ist (physisch oder virtuell). Diese Funktion ist nicht verfügbar, wenn Sie eine [PowerShell Direct-Befehlszeile](/virtualization/hyper-v-on-windows/user_guide/vmsession) für einen virtuellen Computer auf demselben physischen Computer verwenden, und sie ist nicht verfügbar, wenn Sie WinRM-Cmdlets verwenden.
>
> Ein BITS-Auftrag, der aus einer Remote-PowerShell-Sitzung erstellt wurde, wird im Benutzerkontokontext dieser Sitzung ausgeführt und wird nur dann ausgeführt, wenn diesem Benutzerkonto mindestens eine aktive lokale Anmeldesitzung oder Remote-PowerShell-Sitzung zugeordnet ist. Weitere Informationen finden Sie unter [So verwalten Sie PowerShell-Remotesitzungen.](using-windows-powershell-to-create-bits-transfer-jobs.md)

 

Dieser Abschnitt enthält auch die folgenden Themen:

-   [Bewährte Methoden bei der Verwendung von BITS](best-practices-when-using-bits.md)
-   [Auflisten von Aufträgen in der Übertragungswarteschlange](enumerating-jobs-in-the-transfer-queue.md)
-   [Aufzählen von Dateien in einem Auftrag](enumerating-files-in-a-job.md)
-   [Behandlung von Fehlern](handling-errors.md)
-   [Abrufen der Antwort aus einem Upload-Antwort-Auftrag](retrieving-the-reply-from-an-upload-reply-job.md)

Beispielcode, der die BITS-Schnittstellen verwendet, finden Sie unter [BITS-Beispiele und -Tools.](bits-samples-and-tools.md)

 

 