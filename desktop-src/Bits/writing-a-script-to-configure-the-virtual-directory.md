---
title: Schreiben eines Skripts zum Konfigurieren des virtuellen Verzeichnisses
description: Schreiben eines Skripts zum Konfigurieren des virtuellen Verzeichnisses
ms.assetid: 0324fbc8-1d64-454c-b021-4e010edcac8d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae23a33c2c91dc0a141c6f377daf89708499aae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947413"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a><span data-ttu-id="18cf4-103">Schreiben eines Skripts zum Konfigurieren des virtuellen Verzeichnisses</span><span class="sxs-lookup"><span data-stu-id="18cf4-103">Writing a Script to Configure the Virtual Directory</span></span>

<span data-ttu-id="18cf4-104">Sie können die Standard BITS-IIS-Eigenschaftswerte verwenden, um eine Datei auf den Server hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="18cf4-104">You can use the default BITS IIS property values to upload a file to the server.</span></span> <span data-ttu-id="18cf4-105">Die Uploaddatei wird in die URL geschrieben, wie im Remote Dateinamen des Auftrags angegeben.</span><span class="sxs-lookup"><span data-stu-id="18cf4-105">The upload file is written to the URL as specified in the remote file name of the job.</span></span> <span data-ttu-id="18cf4-106">Um die Datei in eine Serveranwendung hochzuladen und eine Antwort zu erhalten, ändern Sie die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) so, dass die Daten nach Verweis gesendet werden (der Name der Datei, die die Daten enthält) oder nach Wert (sendet die Daten im Anforderungs Text).</span><span class="sxs-lookup"><span data-stu-id="18cf4-106">To upload the file to a server application and receive a reply, change the [BITSServerNotificationType](bits-iis-extension-properties.md) property to send the data by reference (sends the name of the file that contains the data) or by value (sends the data in the body of the request).</span></span>

<span data-ttu-id="18cf4-107">Eine Liste und Beschreibung der Eigenschaften, die Sie ändern können, finden Sie unter [BITS-IIS-Erweiterungs Eigenschaften](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="18cf4-107">For a list and description of the properties that you can modify, see [BITS IIS Extension Properties](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="18cf4-108">Verwenden Sie die Methoden der [**ibitsextensionsetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) -Schnittstelle, um das virtuelle Verzeichnis für Uploads zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="18cf4-108">Use the methods of the [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) interface to enable and disable the virtual directory for uploads.</span></span>

<span data-ttu-id="18cf4-109">Im folgenden Beispiel wird gezeigt, wie Sie mit Windows Script Host ein virtuelles IIS-Verzeichnis für BITS-Uploads erstellen, konfigurieren und aktivieren.</span><span class="sxs-lookup"><span data-stu-id="18cf4-109">The following example shows how to use Windows Script Host to create, configure, and enable an IIS virtual directory for BITS uploads.</span></span>


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

//Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



<span data-ttu-id="18cf4-110">Um das vorherige Beispiel zum Hochladen der Daten in eine Serveranwendung zu ändern, fügen Sie den folgenden Code vor **SetInfo** hinzu.</span><span class="sxs-lookup"><span data-stu-id="18cf4-110">To change the previous example to upload the data to a server application, add the following code before **SetInfo**.</span></span>


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



<span data-ttu-id="18cf4-111">Der Speicherort der Uploaddatei wird an die Serveranwendung myasp. ASP im Header Bits-Request-DataFile-Name weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="18cf4-111">The location of the upload file is passed to the server application, myasp.asp, in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="18cf4-112">Legen Sie die Eigenschaft " [bitsservernotificationtype](bits-iis-extension-properties.md) " auf "2" fest, um die Uploaddatei im Hauptteil der Anforderung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="18cf4-112">To receive the upload file in the body of the request, set the [BITSServerNotificationType](bits-iis-extension-properties.md) property to 2.</span></span>

<span data-ttu-id="18cf4-113">Informationen zum Empfangen von uploaddaten in der Serveranwendung finden [Sie unter Verwenden von Bits-Benachrichtigungs Anforderungs-/Antwortheadern](using-bits-notification-request-response-headers.md).</span><span class="sxs-lookup"><span data-stu-id="18cf4-113">For information on receiving the upload data in your server application, see [Using BITS Notification Request/Response Headers](using-bits-notification-request-response-headers.md).</span></span>

 

 




