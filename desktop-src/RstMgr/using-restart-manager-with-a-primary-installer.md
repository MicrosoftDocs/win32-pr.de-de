---
title: Verwenden des Neustart-Managers mit einem primären Installationsprogramm
description: Im folgenden Verfahren wird beschrieben, wie Sie den Neustart-Manager verwenden, um Anwendungen und Dienste herunterzufahren und neu zu starten. Wenn Sie den Neustart-Manager mit einem einzigen Installationsprogramm verwenden, ist dieses Installationsprogramm auch das primäre Installationsprogramm, das die Benutzeroberfläche steuert.
ms.assetid: 8d2b4129-c595-4b11-9771-6dc953f4db40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764086166fc895d44f1a555f453d2941487c5d999adfa8d38581a12f07c9c45c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010008"
---
# <a name="using-restart-manager-with-a-primary-installer"></a>Verwenden des Neustart-Managers mit einem primären Installationsprogramm

Im folgenden Verfahren wird beschrieben, wie Sie den Neustart-Manager verwenden, um Anwendungen und Dienste herunterzufahren und neu zu starten. Wenn Sie den Neustart-Manager mit einem einzigen Installationsprogramm verwenden, ist dieses Installationsprogramm auch das primäre Installationsprogramm, das die Benutzeroberfläche steuert.

**So verwenden Sie den Neustart-Manager mit einem primären Installationsprogramm**

1.  Das Installationsprogramm ruft die [**RmStartSession-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) auf, um die Neustart-Manager-Sitzung zu starten und ein Sitzungshandle und einen Schlüssel abzurufen.
2.  Das Installationsprogramm ruft die [**RmRegisterResources-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) auf, um Ressourcen zu registrieren. Der Neustart-Manager kann nur registrierte Ressourcen verwenden, um zu bestimmen, welche Anwendungen und Dienste heruntergefahren und neu gestartet werden müssen. Alle Ressourcen, die von der Installation betroffen sein können, sollten bei der Sitzung registriert werden. Ressourcen können anhand des Dateinamens, des Kurznamens des Diensts oder einer [**RM \_ UNIQUE \_ PROCESS-Struktur**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) identifiziert werden.
3.  Das Installationsprogramm ruft die [**RmGetList-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) auf, um ein Array von [**RM PROCESS \_ \_ INFO-Strukturen**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) abzurufen, das alle Anwendungen und Dienste auflistet, die heruntergefahren und neu gestartet werden müssen.

    Wenn der Wert des *lpdwRebootReason-Parameters,* der von der [**RmGetList-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) zurückgegeben wird, ungleich 0 (null) ist, kann der Neustart-Manager eine registrierte Ressource nicht freigeben, indem eine Anwendung oder ein Dienst heruntergefahren wird. In diesem Fall ist ein Herunterfahren und Neustarten des Systems erforderlich, um die Installation fortzusetzen. Das Installationsprogramm sollte den Benutzer zur Eingabe einer Aktion auffordern, Programme oder Dienste beenden oder ein Herunterfahren und Neustarten des Systems planen.

    Wenn der Wert des *lpdwRebootReason-Parameters,* der von der [**RmGetList-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) zurückgegeben wird, 0 (null) ist, sollte das Installationsprogramm die [**RmShutdown-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) aufrufen. Dadurch werden die Dienste und Anwendungen heruntergefahren, die registrierte Ressourcen verwenden. Das Installationsprogramm sollte dann Systemänderungen vornehmen, die zum Abschließen der Installation erforderlich sind. Schließlich sollte das Installationsprogramm die [**RmRestart-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) aufrufen, damit der Neustart-Manager die heruntergefahrenen Anwendungen neu starten kann, die für einen Neustart registriert wurden.

4.  Das Installationsprogramm kann die [**RmAddFilter-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter) verwenden, um zu verhindern, dass bestimmte Anwendungen und Dienste von Neustart-Manager-Vorgängen heruntergefahren oder neu gestartet werden. Die [**RmGetFilterList-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist) gibt eine Liste der Anwendungen und Dienste zurück, die vor dem Herunterfahren und Neustart gefiltert werden sollen. Die [**RmRemoveFilter-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter) entfernt einen Filter.
5.  Das Installationsprogramm ruft die [**RmEndSession-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) auf, um die Neustart-Manager-Sitzung zu schließen.

Ein Beispielcodeausschnitt, der das Starten und Verwenden einer Restart Manager-Sitzung mit einem primären Installationsprogramm und dem anschließenden Verknüpfen eines sekundären Installationsprogramms mit der vorhandenen Sitzung zeigt, finden Sie unter [Verwenden des Neustart-Managers mit einem sekundären Installationsprogramm.](using-restart-manager-with-a-secondary-installer.md)

 

 




