---
title: Windows Remoteverwaltung und WMI
description: Windows Mit der Remoteverwaltung können Daten abgerufen werden, die von der Windows verfügbar gemacht werden.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d4fab5cd1ee27f664fc43838a62db949c5892147818466edf649641eff203b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642470"
---
# <a name="windows-remote-management-and-wmi"></a>Windows Remoteverwaltung und WMI

Windows Die Remoteverwaltung kann zum Abrufen von Daten verwendet werden, die von der Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) und MI ) verfügbar [gemacht werden.](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) Sie können WMI-Daten mit Skripts oder Anwendungen abrufen, die die [WinRM-Skripterstellungs-API](winrm-scripting-api.md) verwenden, oder über das Winrm-Befehlszeilentool. 

WinRM unterstützt die meisten vertrauten WMI-Klassen und -Vorgänge, einschließlich eingebetteter Objekte. WinRM kann WMI nutzen, um Daten zu Ressourcen zu [*sammeln*](windows-remote-management-glossary.md) oder Ressourcen auf einem Windows betriebssystembasierten Betriebssystem zu verwalten. Das bedeutet, dass Sie Daten zu Objekten wie Datenträgern, Netzwerkadaptern, Diensten oder Prozessen in Ihrem Unternehmen über den vorhandenen Satz von [WMI-Klassen abrufen können.](/windows/desktop/WmiSdk/wmi-classes) Sie können auch auf die Hardwaredaten zugreifen, die über den [Standard-WMI-IPMI-Anbieter verfügbar sind.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)

## <a name="identifying-a-wmi-resource"></a>Identifizieren einer WMI-Ressource

Sie können auf eine WMI-Klasse [*als*](windows-remote-management-glossary.md) Ressource in WinRM und im WS-Management-Protokoll verweisen: ein Typ einer verwalteten Entität, z. B. ein Dienst oder ein Datenträger.

Eine WMI-Klasse oder -Methode wird durch einen [*URI*](windows-remote-management-glossary.md)identifiziert, genau wie jede andere Ressource, wenn das WS-Management verwendet wird. Der URI kann eine WMI-Ressource (Klasse), eine WMI-Aktion (Methode) angeben oder [*eine*](windows-remote-management-glossary.md) bestimmte Instanz einer Klasse in Nachrichten identifizieren, die über ein Netzwerk gesendet werden. Weitere Informationen finden Sie unter [Ressourcen-URIs.](resource-uris.md)

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Erstellen des URI-Präfix für WMI-Klassen

Das URI-Präfix enthält einen festen Teil und den WMI-Namespace. Beispielsweise ist das URI-Präfix in Windows Server, das den festen Teil des Präfixes enthält: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . Dadurch kann das URI-Präfix für jeden WMI-Namespace generiert werden. Verwenden Sie beispielsweise das folgende URI-Präfix, um auf den WMI-Standardnamespace des Stamms zuzugreifen: **\\** `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

Die meisten WMI-Klassen für die Verwaltung befinden sich im **\\ Cimv2-Stammnamespace.** Verwenden Sie das URI-Präfix, um auf Klassen und Instanzen im **\\ Cimv2-Stammnamespace** `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` zuzugreifen: . Weitere Informationen finden Sie unter [Ressourcen-URIs.](resource-uris.md)

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Generieren eines vollständigen URI für WMI-Klassen

Der URI, den Sie  entweder für das Winrm-Befehlszeilentool oder für ein Skript angeben, besteht aus dem Präfix und der Ressourcenspezifikation.

Im folgenden Verfahren wird beschrieben, wie Sie einen Ressourcen-URI generieren, um eine WMI-Klasse zu erhalten oder in einem Enumerate-Vorgang zu verwenden.

**So generieren Sie einen Ressourcen-URI für eine WMI-Klasse**

1.  Beginnen Sie mit dem Präfix, das angibt, WS-Management Protokollschema verwendet werden soll.

    https://schemas.microsoft.com/wbem/wsman/1

    Das Ressourcen-URI-Präfix für WMI-Klassen ist immer identisch. Weitere Informationen finden Sie unter [URI-Präfixe.](uri-prefixes.md)

2.  Fügen Sie dem Präfix den WMI-Namespace hinzu.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Fügen Sie den Klassennamen hinzu.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Fügen Sie zum Festlegen des Werts einer Eigenschaft oder zum Aufrufen einer bestimmten Methode den oder die erforderlichen Schlüsselwerte für die Klasse hinzu.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Wenn Sie den Schlüsselwert leer lassen, ändern Sie den ursprünglichen Eigenschaftswert nicht.

    > [!Note]  
    > Wenn sie den Schlüsselwert leer lassen, wird der Eigenschaftswert auf **NULL festgelegt.**

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Suchen einer WMI-Ressource mit WinRM

Sie können WMI-Daten entweder über das Befehlszeilentool **Winrm** oder über ein Visual Basic-Skript abrufen, das die [WinRM-Skript-API verwendet.](winrm-scripting-api.md) Sie verwenden keinen [WMI-Pfad, um](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) eine Ressource zu suchen. Stattdessen konvertieren Sie den WMI-Namespace und die WMI-Hierarchie in einen [*URI.*](windows-remote-management-glossary.md)

Der WinRM-URI für eine WMI-Klasse besteht aus zwei Teilen: dem [URI-Präfix](uri-prefixes.md) und der Klasse, auf die Sie zugreifen möchten.

Beispielsweise kann der folgende URI für die [**Session.Enumerate-Methode**](session-enumerate.md) angegeben werden, um alle Dienste auf einem Computer auflisten zu können. Das URI-Präfix ist `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` , und die -Klasse ist [**Win32 \_ Service**](/windows/desktop/CIMWin32Prov/win32-service).

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

Listen Sie in WMI die Daten für alle Instanzen einer Ressource oder Klasse auf verschiedene Arten auf:

-   Eine Abfrage für alle Instanzen dieser Ressource.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Ein Aufruf von [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) oder [**SWbemObject.Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).

    `Set colServices = InstancesOf("Win32_Service")`

In WinRM gibt es eine Möglichkeit, alle Instanzen einer Ressource auflisten: [**Session.Enumerate**](session-enumerate.md).


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Suchen einer bestimmten Instanz einer WMI-Ressource

In WMI können Sie eine bestimmte Instanz einer Klasse festlegen, indem Sie entweder Werte für die Schlüsseleigenschaften angeben oder eine -Instanz abfragen, die einer Liste von Eigenschaftswerten entspricht. Schlüsseleigenschaften verfügen über den [**WMI-Schlüsselqualifizierer**](/windows/desktop/WmiSdk/key-qualifier).

Sie können eine bestimmte Instanz einer Klasse auf verschiedene Weise abrufen:

-   Ein Aufruf von [**Session.Enumerate mit**](session-enumerate.md) den *Filter-* und *Dialektparametern,* um eine Abfrage zu erstellen.

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Ein Aufruf von [**SWbemServices.Get.**](/windows/desktop/WmiSdk/swbemservices-get) Für [**Session.Get**](session-get.md)müssen Sie einen oder mehrere bestimmte Schlüsselwerte vor einem Fragezeichen (?) angegeben.

    Das Format des URI für eine bestimmte Instanz ist `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Eine WMI-Klasse kann mehrere Schlüssel haben. Schlüsselname-Wert-Paare werden durch ein "+"-Zeichen getrennt. In diesem Fall ist das Format `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` : .

    Die WinRM-Syntax zum Abrufen eines Singleton-WMI-Objekts ist anders als WMI. Ein Singleton ist eine WMI-Klasse, die so definiert ist, dass nur eine Instanz zulässig ist. [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) oder [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) sind Beispiele für eine WMI-Singletonklasse.

    Die WMI-Syntax für Singletons wird im folgenden VBScript-Codebeispiel gezeigt.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    Das folgende Beispiel zeigt die WinRM-Singletonsyntax, die "@" nicht verwendet.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Hinzufügen eines [*Selektors*](windows-remote-management-glossary.md) zu einem [**ResourceLocator- oder**](resourcelocator.md) [**IWSManResourceLocator-Objekt.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

    Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie sie einen Selektor verwenden, um eine bestimmte Instanz des [**Win32-Prozessors \_ zu erhalten.**](/windows/desktop/CIMWin32Prov/win32-processor)

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[URI-Präfixe](uri-prefixes.md)
</dt> <dt>

[Ressourcen-URIs](resource-uris.md)
</dt> <dt>

[Skripterstellung in Windows Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> </dl>
