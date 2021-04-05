---
title: Verwenden des Neustart-Managers mit einem primären Installer
description: Im folgenden Verfahren wird beschrieben, wie Sie den Neustart-Manager verwenden, um Anwendungen und Dienste herunterzufahren und neu zu starten. Wenn Sie den Neustart-Manager mit einem einzelnen Installationsprogramm verwenden, ist dieses Installationsprogramm auch das primäre Installationsprogramm, das die Benutzeroberfläche steuert.
ms.assetid: 8d2b4129-c595-4b11-9771-6dc953f4db40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38956ee8d04bc377809e93579080d9b767c3da3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947542"
---
# <a name="using-restart-manager-with-a-primary-installer"></a>Verwenden des Neustart-Managers mit einem primären Installer

Im folgenden Verfahren wird beschrieben, wie Sie den Neustart-Manager verwenden, um Anwendungen und Dienste herunterzufahren und neu zu starten. Wenn Sie den Neustart-Manager mit einem einzelnen Installationsprogramm verwenden, ist dieses Installationsprogramm auch das primäre Installationsprogramm, das die Benutzeroberfläche steuert.

**So verwenden Sie den Neustart-Manager mit einem primären Installer**

1.  Das Installationsprogramm ruft die [**rmstartession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) -Funktion auf, um die Neustart-Manager-Sitzung zu starten und ein Sitzungs Handle und einen Schlüssel zu erhalten.
2.  Das Installationsprogramm ruft die [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) -Funktion auf, um Ressourcen zu registrieren. Mit dem Neustart-Manager können nur registrierte Ressourcen verwendet werden, um zu bestimmen, welche Anwendungen und Dienste heruntergefahren und neu gestartet werden müssen. Alle Ressourcen, die von der Installation betroffen sein können, sollten bei der Sitzung registriert werden. Ressourcen können anhand des Datei namens, des Dienst Kurznamens oder einer [**eindeutigen RM- \_ \_ Prozess**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) Struktur identifiziert werden.
3.  Das Installationsprogramm ruft die [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) -Funktion auf, um ein Array von [**RM- \_ Prozess \_ Info**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) Strukturen abzurufen, das alle Anwendungen und Dienste auflistet, die heruntergefahren und neu gestartet werden müssen.

    Wenn der Wert des *lpdwrebooverrat* -Parameters, der von der [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) -Funktion zurückgegeben wird, nicht NULL ist, kann der Neustart-Manager eine registrierte Ressource nicht durch das Herunterfahren einer Anwendung oder eines Dienstanbieter freigeben. In diesem Fall ist das Herunterfahren und Neustarten des Systems erforderlich, um die Installation fortzusetzen. Das Installationsprogramm muss den Benutzer zur Eingabe einer Aktion auffordern, Programme oder Dienste beenden oder das Herunterfahren und Neustarten des Systems planen.

    Wenn der Wert des *lpdwrebooverrat* -Parameters, der von der [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) -Funktion zurückgegeben wird, 0 (null) ist, sollte das Installationsprogramm die [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) -Funktion aufrufen. Dadurch werden die Dienste und Anwendungen heruntergefahren, die registrierte Ressourcen verwenden. Der Installer sollte dann Systemänderungen ausführen, die zum Abschluss der Installation erforderlich sind. Zum Schluss sollte das Installationsprogramm die [**rmrestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) -Funktion anrufen, damit der Neustart-Manager die herunter gefahrenen Anwendungen neu starten kann, die für einen Neustart registriert wurden.

4.  Das Installationsprogramm kann die [**rmaddfilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter) -Funktion verwenden, um zu verhindern, dass bestimmte Anwendungen und Dienste durch Neustart-Manager-Vorgänge heruntergefahren oder neu gestartet werden. Die [**rmgetfilterlist**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist) -Funktion gibt eine Liste der Anwendungen und Dienste zurück, die beim Herunterfahren und Neustart gefiltert werden sollen. Die [**rmremovefilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter) -Funktion entfernt einen Filter.
5.  Das Installationsprogramm ruft die [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) -Funktion auf, um die Neustart-Manager-Sitzung zu schließen.

Ein Beispiel für einen Code Ausschnitt, der das Starten und Verwenden einer Neustart-Manager-Sitzung mithilfe eines primären Installers anzeigt und dann ein sekundäres Installationsprogramm mit der vorhandenen Sitzung verbindet, finden [Sie unter Verwenden des Neustart-Managers mit einem sekundären Installations](using-restart-manager-with-a-secondary-installer.md)Programm.

 

 




