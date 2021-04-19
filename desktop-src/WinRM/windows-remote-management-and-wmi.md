---
title: Windows-Remoteverwaltung und WMI
description: Windows-Remoteverwaltung können zum Abrufen von Daten verwendet werden, die von Windows-Verwaltungsinstrumentation bereitgestellt werden.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106357173"
---
# <a name="windows-remote-management-and-wmi"></a>Windows-Remoteverwaltung und WMI

Windows-Remoteverwaltung können zum Abrufen von Daten verwendet werden, die von Windows-Verwaltungsinstrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) und [Mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)) verfügbar gemacht werden. Sie können WMI-Daten mit Skripts oder Anwendungen abrufen, die die [WinRM-Skript-API](winrm-scripting-api.md) oder über das **WinRM** -Befehlszeilen Tool verwenden.

WinRM unterstützt den größten Teil der vertrauten WMI-Klassen und-Vorgänge, einschließlich eingebetteter Objekte. WinRM kann WMI zum Sammeln von Daten zu [*Ressourcen*](windows-remote-management-glossary.md) oder zum Verwalten von Ressourcen auf einem Windows-basierten Betriebssystem nutzen. Dies bedeutet, dass Sie Daten über Objekte wie Datenträger, Netzwerkadapter, Dienste oder Prozesse in Ihrem Unternehmen über den vorhandenen Satz von [WMI-Klassen](/windows/desktop/WmiSdk/wmi-classes)abrufen können. Sie können auch auf die Hardware Daten zugreifen, die über den standardmäßigen WMI- [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)verfügbar sind.

## <a name="identifying-a-wmi-resource"></a>Identifizieren einer WMI-Ressource

Sie können auf eine WMI-Klasse als [*Ressource*](windows-remote-management-glossary.md) in WinRM und im WS-Management-Protokoll verweisen: eine verwaltete Entität, z. b. ein Dienst oder ein Datenträger.

Eine WMI-Klasse oder-Methode wird durch einen [*URI*](windows-remote-management-glossary.md)identifiziert, ebenso wie jede andere Ressource, wenn das WS-Management Protokoll verwendet wird. Der URI kann eine WMI-Ressource (Klasse), eine WMI-Aktion (-Methode) oder eine bestimmte Instanz einer Klasse in [*Nachrichten*](windows-remote-management-glossary.md) angeben, die über ein Netzwerk gesendet werden. Weitere Informationen finden Sie unter [Ressourcen-URIs](resource-uris.md).

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Erstellen des URI-Präfixes für WMI-Klassen

Das URI-Präfix enthält einen Fixed-Part-und den WMI-Namespace. Beispielsweise lautet das URI-Präfix in Windows Server, das den fixierten Teil des Präfixes enthält, wie folgt: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . Dadurch kann das URI-Präfix für jeden WMI-Namespace generiert werden. Wenn Sie z. b. **auf \\ den WMI** -Stamm Namespace zugreifen möchten, verwenden Sie das folgende URI-Präfix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

Der Großteil der WMI-Klassen für die Verwaltung ist im **root \\ CIMV2** -Namespace. Um auf Klassen und Instanzen im **root \\ CIMV2** -Namespace zuzugreifen, verwenden Sie das URI-Präfix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` . Weitere Informationen finden Sie unter [Ressourcen-URIs](resource-uris.md).

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Erstellen eines kompletten URI für WMI-Klassen

Der URI, den Sie entweder für das **WinRM** -Befehlszeilen Tool oder für ein Skript angeben, besteht aus dem Präfix und der Ressourcen Spezifikation.

Im folgenden Verfahren wird beschrieben, wie Sie einen Ressourcen-URI generieren, um eine WMI-Klasse zu erhalten oder in einem enumeringvorgang zu verwenden.

**So generieren Sie einen Ressourcen-URI für eine WMI-Klasse**

1.  Beginnen Sie mit dem Präfix, das angibt, dass das WS-Management Protokoll Schema verwendet werden soll.

    https://schemas.microsoft.com/wbem/wsman/1

    Das Ressourcen-URI-Präfix für die WMI-Klassen ist immer identisch. Weitere Informationen finden Sie unter [URI-Präfixe](uri-prefixes.md).

2.  Fügen Sie dem Präfix den WMI-Namespace hinzu.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Fügen Sie den Klassennamen hinzu.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Um den Wert einer Eigenschaft festzulegen oder um eine bestimmte Methode aufzurufen, fügen Sie den erforderlichen Schlüsselwert bzw. die erforderlichen Werte für die Klasse hinzu.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Wenn Sie den Schlüsselwert leer lassen, wird der ursprüngliche Eigenschafts Wert nicht geändert.

    > [!Note]  
    > Wenn Sie den Schlüsselwert leer lassen, wird der Eigenschafts Wert auf **null** festgelegt.

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Suchen einer WMI-Ressource mit WinRM

Sie können WMI-Daten entweder über das Befehlszeilen Tool, mithilfe von **WinRM** oder mithilfe eines Visual Basic Skripts abrufen, das die [WinRM-Skript-API](winrm-scripting-api.md)verwendet. Sie verwenden keinen [WMI-Pfad](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) , um eine Ressource zu suchen. Stattdessen konvertieren Sie den WMI-Namespace und die Hierarchie in einen [*URI*](windows-remote-management-glossary.md).

Der WinRM-URI für eine WMI-Klasse enthält zwei Teile: das [URI-Präfix](uri-prefixes.md) und die Klasse, auf die Sie zugreifen möchten.

Beispielsweise kann der folgende URI für die [**Session. Enumerate**](session-enumerate.md) -Methode bereitgestellt werden, um alle Dienste auf einem Computer aufzulisten. Das URI-Präfix ist `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` , und die-Klasse ist der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service).

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

Auflisten der Daten für alle Instanzen einer Ressource oder Klasse in WMI auf verschiedene Weise:

-   Eine Abfrage für alle Instanzen dieser Ressource.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Einen aufzurufenden [**Austausch von "errbemservices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) " oder " [**errbemubject. Instance \_**](/windows/desktop/WmiSdk/swbemobject-instances-)".

    `Set colServices = InstancesOf("Win32_Service")`

In WinRM gibt es eine Möglichkeit, alle Instanzen einer Ressource aufzulisten: [**Session. Enumerate**](session-enumerate.md).


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Suchen einer bestimmten Instanz einer WMI-Ressource

In WMI können Sie eine bestimmte Instanz einer Klasse angeben, indem Sie Werte für die Schlüsseleigenschaften angeben oder eine Instanz Abfragen, die mit einer Liste von Eigenschafts Werten übereinstimmt. Schlüsseleigenschaften haben den WMI- [**Schlüssel Qualifizierer**](/windows/desktop/WmiSdk/key-qualifier).

Sie können eine bestimmte Instanz einer Klasse auf verschiedene Weise abrufen:

-   Einen aufzurufenden [**Sitzungs. Enumerate**](session-enumerate.md) mit den Parametern *Filter* und *Dialekt* zum Erstellen einer Abfrage.

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Einen aufzurufenden [**Swap-Dienst. Get**](/windows/desktop/WmiSdk/swbemservices-get). Für [**Session. Get**](session-get.md)müssen Sie einen oder mehrere bestimmte Schlüsselwerte angeben, denen ein Fragezeichen (?) vorangestellt ist.

    Das Format des URI für eine bestimmte Instanz ist `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Eine WMI-Klasse kann über mehr als einen Schlüssel verfügen. Schlüssel Name-Wert-Paare werden durch ein "+"-Zeichen getrennt. In diesem Fall lautet das Format: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .

    Die WinRM-Syntax zum Abrufen eines Singleton-WMI-Objekts unterscheidet sich von WMI. Ein Singleton ist eine WMI-Klasse, die so definiert ist, dass nur eine Instanz zulässig ist. [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) oder [**Win32 \_ wmisetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) sind Beispiele für eine WMI-Singleton-Klasse.

    Die WMI-Syntax für Singletons wird im folgenden VBScript-Codebeispiel gezeigt.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    Das folgende Beispiel zeigt die WinRM-Singleton-Syntax, die "@" nicht verwendet.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Hinzufügen eines [*Selektor*](windows-remote-management-glossary.md) zu einem [**ResourceLocator**](resourcelocator.md) -oder [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) -Objekt.

    Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie ein Selektor verwendet wird, um eine bestimmte Instanz des [**Win32- \_ Prozessors**](/windows/desktop/CIMWin32Prov/win32-processor)zu erhalten.

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[URI-Präfixe](uri-prefixes.md)
</dt> <dt>

[Ressourcen-URIs](resource-uris.md)
</dt> <dt>

[Skripterstellung in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> </dl>
