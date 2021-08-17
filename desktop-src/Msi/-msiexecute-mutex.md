---
description: '\_MSIExecute Mutex wird nur bei der Verarbeitung der Tabelle InstallExecuteSequence, der Tabelle AdminExecuteSequence oder der Tabelle AdvtExecuteSequence festgelegt.'
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbca288c2d75051c1d6247a1123c453509c635df2872c3724d27d9a2fa27cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066550"
---
# <a name="_msiexecute-mutex"></a>\_MSIExecute Mutex

\_MSIExecute Mutex wird nur beim Verarbeiten der [Tabelle InstallExecuteSequence,](installexecutesequence-table.md) [der Tabelle AdminExecuteSequence](adminexecutesequence-table.md)oder der [Tabelle AdvtExecuteSequence](advtexecutesequence-table.md)festgelegt.

Da zwei Installationen nicht im gleichen Prozess ausgeführt werden können, gibt der Versuch, die Anwendungsprogrammierschnittstelle (API) des Installationsprogramms aufzurufen, in zwei Fällen ERROR \_ INSTALL \_ ALREADY RUNNING \_ (1618) zurück:

-   Während \_ MSIExecute Mutex festgelegt ist.
-   Während der aktuelle Prozess die [Tabelle InstallUISequence](installuisequence-table.md) oder [die Tabelle AdminUISequence](adminuisequence-table.md)verarbeitet.

Informationen dazu, welche Anwendung installiert wird, finden Sie in den Meldungen zur [Ereignisprotokollierung.](event-logging.md)

In Fällen, in denen es nicht praktikabel ist, einen Fehler ERROR \_ INSTALL \_ ALREADY RUNNING \_ zurückzugeben, können Sie den aktuellen Status des Windows Installer-Diensts abrufen, bevor Sie versuchen, die Installation mithilfe der [**QueryServiceStatusEx-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) zu starten. Der Windows Installer-Dienst wird derzeit ausgeführt, wenn der Wert des **dwControlsAccepted-Members** der zurückgegebenen [**SERVICE STATUS \_ \_ PROCESS-Struktur**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) **SERVICE ACCEPT \_ \_ SHUTDOWN** lautet.

**Windows Installer 2.0:** Wird nicht unterstützt. Die Verwendung der [**QueryServiceStatusEx-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) zum Abrufen des aktuellen Status des Windows Installer-Diensts erfordert Windows Installer Version 3.0 oder höher.

 

 
