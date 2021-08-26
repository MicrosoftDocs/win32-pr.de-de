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
ms.openlocfilehash: b9ea1de5a0b9f7be9598a4011cbb6cd76f49e6d4bcc3d468093be1479ee2b59e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004600"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a>Schreiben eines Skripts zum Konfigurieren des virtuellen Verzeichnisses

Sie können die STANDARDMÄßIGEN BITS IIS-Eigenschaftswerte verwenden, um eine Datei auf den Server hochzuladen. Die Uploaddatei wird in die URL geschrieben, wie im Remotedateinamen des Auftrags angegeben. Um die Datei in eine Serveranwendung hochzuladen und eine Antwort zu erhalten, ändern Sie die [BITSServerNotificationType-Eigenschaft,](bits-iis-extension-properties.md) um die Daten als Verweis zu senden (sendet den Namen der Datei, die die Daten enthält) oder als Wert (sendet die Daten im Text der Anforderung).

Eine Liste und Eine Beschreibung der Eigenschaften, die Sie ändern können, finden Sie unter [BITS IIS Extension Properties](bits-iis-extension-properties.md). Verwenden Sie die Methoden der [**IBITSExtensionSetup-Schnittstelle,**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) um das virtuelle Verzeichnis für Uploads zu aktivieren und zu deaktivieren.

Das folgende Beispiel zeigt, wie sie Windows Skripthost verwenden, um ein virtuelles IIS-Verzeichnis für BITS-Uploads zu erstellen, zu konfigurieren und zu aktivieren.


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



Um das vorherige Beispiel so zu ändern, dass die Daten in eine Serveranwendung hochgeladen werden, fügen Sie vor SetInfo den folgenden **Code hinzu.**


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



Der Speicherort der Uploaddatei wird im HEADER BITS-Request-DataFile-Name an die Serveranwendung myasp.asp übergeben. Um die Uploaddatei im Text der Anforderung zu empfangen, legen Sie die [BITSServerNotificationType-Eigenschaft](bits-iis-extension-properties.md) auf 2 fest.

Informationen zum Empfangen der Uploaddaten in Ihrer Serveranwendung finden Sie unter [Verwenden von BITS-Benachrichtigungsanforderungs-/Antwortheadern.](using-bits-notification-request-response-headers.md)

 

 




