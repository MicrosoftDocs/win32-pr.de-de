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
# <a name="writing-a-script-to-configure-the-virtual-directory"></a>Schreiben eines Skripts zum Konfigurieren des virtuellen Verzeichnisses

Sie können die Standard BITS-IIS-Eigenschaftswerte verwenden, um eine Datei auf den Server hochzuladen. Die Uploaddatei wird in die URL geschrieben, wie im Remote Dateinamen des Auftrags angegeben. Um die Datei in eine Serveranwendung hochzuladen und eine Antwort zu erhalten, ändern Sie die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) so, dass die Daten nach Verweis gesendet werden (der Name der Datei, die die Daten enthält) oder nach Wert (sendet die Daten im Anforderungs Text).

Eine Liste und Beschreibung der Eigenschaften, die Sie ändern können, finden Sie unter [BITS-IIS-Erweiterungs Eigenschaften](bits-iis-extension-properties.md). Verwenden Sie die Methoden der [**ibitsextensionsetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) -Schnittstelle, um das virtuelle Verzeichnis für Uploads zu aktivieren und zu deaktivieren.

Im folgenden Beispiel wird gezeigt, wie Sie mit Windows Script Host ein virtuelles IIS-Verzeichnis für BITS-Uploads erstellen, konfigurieren und aktivieren.


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



Um das vorherige Beispiel zum Hochladen der Daten in eine Serveranwendung zu ändern, fügen Sie den folgenden Code vor **SetInfo** hinzu.


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



Der Speicherort der Uploaddatei wird an die Serveranwendung myasp. ASP im Header Bits-Request-DataFile-Name weitergegeben. Legen Sie die Eigenschaft " [bitsservernotificationtype](bits-iis-extension-properties.md) " auf "2" fest, um die Uploaddatei im Hauptteil der Anforderung zu empfangen.

Informationen zum Empfangen von uploaddaten in der Serveranwendung finden [Sie unter Verwenden von Bits-Benachrichtigungs Anforderungs-/Antwortheadern](using-bits-notification-request-response-headers.md).

 

 




