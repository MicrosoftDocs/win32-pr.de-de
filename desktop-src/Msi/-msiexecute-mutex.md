---
description: Der \_ msiexecute Mutex wird nur beim Verarbeiten der InstallExecuteSequence-Tabelle, der AdminExecuteSequence-Tabelle oder der AdvtExecuteSequence-Tabelle festgelegt.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864555"
---
# <a name="_msiexecute-mutex"></a>\_Msiexecute Mutex

Der \_ msiexecute Mutex wird nur beim Verarbeiten der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md), der [AdminExecuteSequence](adminexecutesequence-table.md)-Tabelle oder der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)festgelegt.

Da zwei Installationen nicht im selben Prozess ausgeführt werden können, wird beim Versuch, die API (Application Programming Interface) des Installers aufzurufen, die Fehler Installation, die \_ \_ bereits \_ ausgeführt wird (1618), in zwei Fällen zurückgegeben:

-   Während der \_ msiexecute-Mutex festgelegt ist.
-   Während der aktuelle Prozess die Tabelle " [InstallUISequence](installuisequence-table.md) " oder die [Tabelle "AdminUISequence](adminuisequence-table.md)" verarbeitet.

Informationen zu den installierten Anwendungen finden Sie in den [Ereignis Protokollierungs](event-logging.md) Meldungen.

In Fällen, in denen es nicht praktikabel ist, eine Fehlermeldung zu einer bereits aktiven Fehlermeldung zurückzugeben \_ \_ \_ , können Sie den aktuellen Status des Windows Installer Dienstanbieter abrufen, bevor Sie versuchen, die Installation mit der Funktion [**queryservicestatusex**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) zu starten. Der Windows Installer-Dienst wird zurzeit ausgeführt, wenn der Wert des **dwcontrolsaccepted** -Members der zurückgegebenen [**Dienst \_ Status- \_ Prozess**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) Struktur " **Service \_ Accept \_ Shutdown**" lautet.

**Windows Installer 2,0:** Nicht unterstützt. Die Verwendung der Funktion [**queryservicestatusex**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) zum Abrufen des aktuellen Status der Windows Installer Dienstanbieter erfordert Windows Installer Version 3,0 oder höher.

 

 
