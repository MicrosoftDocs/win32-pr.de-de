---
title: Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen
description: Wenn Sie in der Remotedesktopdienste-Bereitstellung eine virtuelle Channels-Anwendung aktiviert haben, können Sie diese Anwendung für Client Computer zur Verfügung stellen.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c8fa23f1498270bd0d2a29c5f48d50f0b2463
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856288"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen

Wenn Sie in der Remotedesktopdienste-Bereitstellung eine virtuelle Channels-Anwendung aktiviert haben, können Sie diese Anwendung für Client Computer zur Verfügung stellen, die über das Remotedesktop ActiveX-Steuerelement auf den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) zugreifen.

**So machen Sie eine Virtual Channel-Anwendung verfügbar**

1.  Stellen Sie das serverseitige Modul der Anwendung bereit, und stellen Sie sicher, dass es auf dem RD-Sitzungshost-Server ausgeführt wird. Greifen Sie auf der Seite Verbindung der Remotedesktopdienste-Webanwendung, die auf dem Webserver ausgeführt wird, auf die **plugindlls** -Eigenschaft der [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstelle zu, um den Namen der virtuellen Channel-DLL anzugeben. Wenn Sie über mehr als ein Plug-in verfügen, geben Sie eine durch Trennzeichen getrennte Liste von DLL-Namen an. Wenn das Plug-in für virtuelle Kanäle beispielsweise den Namen "MyPlugin.dll" hat, verwenden Sie den folgenden Code:

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    Verwenden Sie den folgenden Code, wenn Sie über zwei virtuelle Channel-DLLs verfügen. In diesem Beispiel lauten die DLL-Dateinamen "MyPlugin.dll" und "Vdriver.dll":

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    Aus Sicherheitsgründen akzeptiert die **plugindlls** -Eigenschaft nur eine benannte Liste von virtuellen channeldlls. Das-Steuerelement gibt einen Fehler zurück, wenn eine beliebige Art von Dateisystem oder UNC-Pfad angegeben wird. Außerdem dürfen die Namen der DLLs nur alphanumerische Zeichen enthalten.

2.  Stellen Sie sicher, dass das Client seitige Modul im Verzeichnis% windir% \\ System32 installiert ist.

Die virtuelle Channel-API ermöglicht nicht, dass mehrere Instanzen derselben virtuellen Channel-DLL innerhalb eines einzelnen Prozesses geladen werden. Wenn mehrere Instanzen des Remotedesktop ActiveX-Steuer Elements innerhalb desselben Prozesses ausgeführt werden, kann daher nur die erste Instanz des Steuer Elements die DLL des virtuellen Kanals laden. Wenn Sie eine virtuelle channelanwendung entwerfen, die mehrere Instanzen innerhalb eines einzelnen Prozesses unterstützen muss, müssen Sie die [Dynamic Virtual Channels](dynamic-virtual-channels.md) -API verwenden, um die virtuelle Kanal Anwendung zu implementieren.

> [!Note]  
> Standardmäßig lädt das Remotedesktop ActiveX-Steuerelement virtuelle Channel-Client-DLLs aus dem Verzeichnis% windir% \\ system32. Ein Administrator kann dieses Standard Client-Plug-in-DLL-Verzeichnis ändern. Zu diesem Zweck bearbeiten Sie den Registrierungsschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** auf dem Client Computer. Dieser Verzeichnispfad kann nicht im UNC-Format angegeben werden.

 

 

 




