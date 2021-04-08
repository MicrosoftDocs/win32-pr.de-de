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
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a><span data-ttu-id="7679d-103">Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen</span><span class="sxs-lookup"><span data-stu-id="7679d-103">Using the Remote Desktop ActiveX control with virtual channels</span></span>

<span data-ttu-id="7679d-104">Wenn Sie in der Remotedesktopdienste-Bereitstellung eine virtuelle Channels-Anwendung aktiviert haben, können Sie diese Anwendung für Client Computer zur Verfügung stellen, die über das Remotedesktop ActiveX-Steuerelement auf den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7679d-104">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers that access the Remote Desktop Session Host (RD Session Host) server by means of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="7679d-105">**So machen Sie eine Virtual Channel-Anwendung verfügbar**</span><span class="sxs-lookup"><span data-stu-id="7679d-105">**To make a virtual channel application available**</span></span>

1.  <span data-ttu-id="7679d-106">Stellen Sie das serverseitige Modul der Anwendung bereit, und stellen Sie sicher, dass es auf dem RD-Sitzungshost-Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7679d-106">Deploy the server-side module of the application and make sure it is running on the RD Session Host server.</span></span> <span data-ttu-id="7679d-107">Greifen Sie auf der Seite Verbindung der Remotedesktopdienste-Webanwendung, die auf dem Webserver ausgeführt wird, auf die **plugindlls** -Eigenschaft der [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstelle zu, um den Namen der virtuellen Channel-DLL anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7679d-107">In the connection page of the Remote Desktop Services web application running on your web server, access the **PluginDlls** property of the [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface to specify the name of your virtual channel DLL.</span></span> <span data-ttu-id="7679d-108">Wenn Sie über mehr als ein Plug-in verfügen, geben Sie eine durch Trennzeichen getrennte Liste von DLL-Namen an.</span><span class="sxs-lookup"><span data-stu-id="7679d-108">If you have more than one plug-in, specify a comma-delimited list of DLL names.</span></span> <span data-ttu-id="7679d-109">Wenn das Plug-in für virtuelle Kanäle beispielsweise den Namen "MyPlugin.dll" hat, verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="7679d-109">For instance, if your virtual channel plug-in is named "MyPlugin.dll", use the following code:</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    <span data-ttu-id="7679d-110">Verwenden Sie den folgenden Code, wenn Sie über zwei virtuelle Channel-DLLs verfügen.</span><span class="sxs-lookup"><span data-stu-id="7679d-110">Use the following code if you have two virtual channel DLLs.</span></span> <span data-ttu-id="7679d-111">In diesem Beispiel lauten die DLL-Dateinamen "MyPlugin.dll" und "Vdriver.dll":</span><span class="sxs-lookup"><span data-stu-id="7679d-111">In this example, the DLL file names are "MyPlugin.dll" and "Vdriver.dll":</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    <span data-ttu-id="7679d-112">Aus Sicherheitsgründen akzeptiert die **plugindlls** -Eigenschaft nur eine benannte Liste von virtuellen channeldlls.</span><span class="sxs-lookup"><span data-stu-id="7679d-112">For security reasons, the **PluginDlls** property only accepts a named list of virtual channel DLLs.</span></span> <span data-ttu-id="7679d-113">Das-Steuerelement gibt einen Fehler zurück, wenn eine beliebige Art von Dateisystem oder UNC-Pfad angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7679d-113">The control returns an error if any form of file system or UNC path is specified.</span></span> <span data-ttu-id="7679d-114">Außerdem dürfen die Namen der DLLs nur alphanumerische Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="7679d-114">In addition, the names of the DLLs must contain only alphanumeric characters.</span></span>

2.  <span data-ttu-id="7679d-115">Stellen Sie sicher, dass das Client seitige Modul im Verzeichnis% windir% \\ System32 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7679d-115">Ensure that the client-side module is installed in the %windir%\\system32 directory.</span></span>

<span data-ttu-id="7679d-116">Die virtuelle Channel-API ermöglicht nicht, dass mehrere Instanzen derselben virtuellen Channel-DLL innerhalb eines einzelnen Prozesses geladen werden.</span><span class="sxs-lookup"><span data-stu-id="7679d-116">The virtual channel API does not allow for multiple instances of the same virtual channel DLL to be loaded within a single process.</span></span> <span data-ttu-id="7679d-117">Wenn mehrere Instanzen des Remotedesktop ActiveX-Steuer Elements innerhalb desselben Prozesses ausgeführt werden, kann daher nur die erste Instanz des Steuer Elements die DLL des virtuellen Kanals laden.</span><span class="sxs-lookup"><span data-stu-id="7679d-117">Because of this, if there are multiple instances of the Remote Desktop ActiveX control running within the same process, only the first instance of the control will be able to load the virtual channel DLL.</span></span> <span data-ttu-id="7679d-118">Wenn Sie eine virtuelle channelanwendung entwerfen, die mehrere Instanzen innerhalb eines einzelnen Prozesses unterstützen muss, müssen Sie die [Dynamic Virtual Channels](dynamic-virtual-channels.md) -API verwenden, um die virtuelle Kanal Anwendung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="7679d-118">If you are designing a virtual channel application that must support multiple instances within a single process, you must use the [Dynamic Virtual Channels](dynamic-virtual-channels.md) API to implement your virtual channel application.</span></span>

> [!Note]  
> <span data-ttu-id="7679d-119">Standardmäßig lädt das Remotedesktop ActiveX-Steuerelement virtuelle Channel-Client-DLLs aus dem Verzeichnis% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="7679d-119">By default, the Remote Desktop ActiveX control loads virtual channel client DLLs from the %windir%\\system32 directory.</span></span> <span data-ttu-id="7679d-120">Ein Administrator kann dieses Standard Client-Plug-in-DLL-Verzeichnis ändern.</span><span class="sxs-lookup"><span data-stu-id="7679d-120">It is possible for an administrator to change this default client plug-in DLL directory.</span></span> <span data-ttu-id="7679d-121">Zu diesem Zweck bearbeiten Sie den Registrierungsschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** auf dem Client Computer.</span><span class="sxs-lookup"><span data-stu-id="7679d-121">To do so, edit the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**vdllpath** registry key on the client computer.</span></span> <span data-ttu-id="7679d-122">Dieser Verzeichnispfad kann nicht im UNC-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7679d-122">This directory path cannot be specified in the UNC format.</span></span>

 

 

 




