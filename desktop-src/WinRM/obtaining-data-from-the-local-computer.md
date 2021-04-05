---
title: Abrufen von Daten vom lokalen Computer
description: Obwohl Windows-Remoteverwaltung und WS-Management Protokoll explizit für die Remote Kommunikation konzipiert sind, ist das Einrichten einer Sitzung auf dem lokalen Computer der einfachste Fall.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727408"
---
# <a name="obtaining-data-from-the-local-computer"></a>Abrufen von Daten vom lokalen Computer

Obwohl Windows-Remoteverwaltung und WS-Management Protokoll explizit für die Remote Kommunikation konzipiert sind, ist das Einrichten einer Sitzung auf dem lokalen Computer der einfachste Fall. Einige Skripts erfordern möglicherweise den Zugriff auf Daten auf dem lokalen Computer und auf Remote Computern.

**WinRM-Version 2,0:  **

Alle Vorgänge werden als Remote betrachtet, und der WinRM-Dienst muss gestartet werden, bevor ein Vorgang ausgeführt wird. Wenn kein Remote Ziel angegeben ist, wird standardmäßig localhost verwendet, und alle Vorgänge werden an den lokalen WinRM-Dienst gesendet. Weitere Informationen zum Starten des WinRM-Dienstanbieter finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).

Wenn Sie den WinRM-Dienst für lokale Vorgänge verwenden, sollten die folgenden Faktoren berücksichtigt werden:

-   Die lokale WinRM-Konfiguration kann nur von Administratoren gelesen werden.
-   Für WMI-Namespaces müssen Berechtigungen für die Remote Aktivierung festgelegt sein. Weitere Informationen finden Sie unter [Sichern einer Remote-WMI-Verbindung](../wmisdk/securing-a-remote-wmi-connection.md).
-   Wenn kein WinRM- [*Listener*](windows-remote-management-glossary.md) erstellt wird, lauscht der WinRM-Dienst auf lokale Anforderungen an Port 47001.

Jedes WinRM-Skript muss gestartet werden, indem eine Sitzung oder eine Verbindung mit einem Computer hergestellt wird, indem ein [**Sitzungs**](session.md) Objekt erstellt wird. Nachdem die Sitzung erstellt wurde, können Sie die **Sitzungs** Objektmethoden verwenden, z. b. [**Session. Enumerate**](session-enumerate.md) oder [**Session. aufrufen**](session-invoke.md) , um Daten abzurufen oder Methoden auszuführen.

Die Erstellung einer Sitzung ähnelt in gewisser Weise dem [Herstellen einer Verbindung](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) mit einem Windows-Verwaltungsinstrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page))-Namespace. Die Sitzung ist im Wesentlichen eine Ebene, die es Ihnen ermöglicht, Daten über [*SOAP*](windows-remote-management-glossary.md) -Nachrichten und das WS-Management Protokoll zu senden und zu empfangen. Weitere Informationen finden Sie unter [WS-Management-Protokoll](ws-management-protocol.md).

Wenn Sie die [**WSMAN. CreateSession**](wsman-createsession.md) -Methode aufrufen, um ein [**Sitzungs**](session.md) Objekt zu erstellen, wird eine [*Sitzung*](windows-remote-management-glossary.md) gestartet, die eine Verbindung mit dem lokalen WinRM herstellt.

**So erstellen Sie eine WSMAN-Sitzung und rufen Daten ab**

1.  Erstellen Sie ein [**WSMAN**](wsman.md) -Objekt.

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Erstellen Sie eine Sitzung, indem Sie die [**WSMAN. CreateSession**](wsman-createsession.md) -Methode aufrufen. Diese Sitzung wird mit Ihrem Anmelde Namen und Kennwort ausgeführt und kann Daten über das lokale WinRM abrufen.

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  Erstellen Sie einen Ressourcen- [*URI*](windows-remote-management-glossary.md) , um die [*Ressource*](windows-remote-management-glossary.md) zu identifizieren, die Sie verwalten möchten, oder für die Sie Daten abrufen möchten. Weitere Informationen zum Formatieren eines URIs finden Sie unter [Ressourcen-URIs](resource-uris.md). Dieser Ressourcen-URI gilt für eine bestimmte Instanz der WMI- [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse, den WinMgmt-Dienst. Weitere Informationen finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  Ruft [**Sitzungs**](session.md) Methoden auf, die Daten mit dem Ressourcen-URI Abrufen oder aufzählen. Weitere Informationen finden Sie unter [WinRM-Skript-API](winrm-scripting-api.md).

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  Informationen zum Abrufen oder Verwalten von Daten von einem anderen Computer oder zum Verwenden verschiedener Authentifizierungsmethoden finden Sie unter Abrufen [von Daten von einem Remote Computer](obtaining-data-from-a-remote-computer.md).

Das folgende VBScript-Codebeispiel zeigt das komplette Skript, das die jeweilige Instanz des WMI- [**Win32- \_ diensnamens**](/windows/desktop/CIMWin32Prov/win32-service) "winmgmt" abruft.


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



Das folgende VBScript-Codebeispiel zeigt das komplette Skript mit der Datentransformation. Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md).


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> </dl>

 

 