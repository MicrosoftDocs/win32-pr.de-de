---
title: Verwenden des Remotedesktop ActiveX-Steuerelements mit virtuellen Kanälen
description: Wenn Sie eine Anwendung für virtuelle Kanäle in Ihrer Remotedesktopdienste-Bereitstellung aktiviert haben, können Sie diese Anwendung clientcomputern zur Verfügung stellen.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dae33c059a84422788bc49d47f95e0011f78930054ed3884669e8f35763461b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868730"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>Verwenden des Remotedesktop ActiveX-Steuerelements mit virtuellen Kanälen

Wenn Sie eine Anwendung für virtuelle Kanäle in Ihrer Remotedesktopdienste-Bereitstellung aktiviert haben, können Sie diese Anwendung über das Remotedesktop ActiveX-Steuerelement für Clientcomputer verfügbar machen, die auf den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) zugreifen.

**So stellen Sie eine Anwendung für den virtuellen Kanal zur Verfügung**

1.  Stellen Sie das serverseitige Modul der Anwendung sicher, dass es auf dem serverseitigen RD-Sitzungshost wird. Greifen Sie auf der Verbindungsseite der Remotedesktopdienste-Webanwendung, die auf Ihrem Webserver ausgeführt wird, auf die **PluginDlls-Eigenschaft** der [**IMsTscAdvancedSettings-Schnittstelle**](imstscadvancedsettings-interface.md) zu, um den Namen Ihrer DLL des virtuellen Kanals anzugeben. Wenn Sie über mehrere Plug-Ins verfügen, geben Sie eine durch Trennzeichen getrennte Liste von DLL-Namen an. Wenn Ihr Plug-In für den virtuellen Kanal beispielsweise den Namen "MyPlugin.dll" hat, verwenden Sie den folgenden Code:

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    Verwenden Sie den folgenden Code, wenn Sie über zwei DLLs für virtuelle Kanäle verfügen. In diesem Beispiel sind die DLL-Dateinamen "MyPlugin.dll" und "Vdriver.dll":

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    Aus Sicherheitsgründen akzeptiert die **PluginDlls-Eigenschaft** nur eine benannte Liste virtueller Kanal-DLLs. Das -Steuerelement gibt einen Fehler zurück, wenn eine Form von Dateisystem oder UNC-Pfad angegeben ist. Darüber hinaus dürfen die Namen der DLLs nur alphanumerische Zeichen enthalten.

2.  Stellen Sie sicher, dass das clientseitige Modul im Verzeichnis %windir% \\ system32 installiert ist.

Die API für virtuelle Kanäle lässt nicht zu, dass mehrere Instanzen derselben DLL des virtuellen Kanals innerhalb eines einzelnen Prozesses geladen werden. Wenn daher mehrere Instanzen des Remotedesktop ActiveX-Steuerelements innerhalb desselben Prozesses ausgeführt werden, kann nur die erste Instanz des Steuerelements die DLL des virtuellen Kanals laden. Wenn Sie eine Anwendung für virtuelle Kanäle entwerfen, die mehrere Instanzen [](dynamic-virtual-channels.md) innerhalb eines einzelnen Prozesses unterstützen muss, müssen Sie die API für dynamische virtuelle Kanäle verwenden, um Ihre Anwendung für virtuelle Kanäle zu implementieren.

> [!Note]  
> Standardmäßig lädt das Remotedesktop ActiveX Client-DLLs des virtuellen Kanals aus dem Verzeichnis %windir% \\ system32. Es ist möglich, dass ein Administrator dieses DLL-Standardverzeichnis des Client-Plug-Ins ändert. Bearbeiten Sie dazu den **Registrierungsschlüssel HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** auf dem Clientcomputer. Dieser Verzeichnispfad kann nicht im UNC-Format angegeben werden.

 

 

 




