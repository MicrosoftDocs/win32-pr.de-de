---
title: URI-Präfixe
description: Das Ressourcen-URI-Präfix ist abhängig vom XML-Schema, das die Ressource beschreibt, unterschiedlich.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103858538"
---
# <a name="uri-prefixes"></a>URI-Präfixe

Das [*Ressourcen-URI*](windows-remote-management-glossary.md) -Präfix ist abhängig vom XML-Schema, das die Ressource beschreibt, unterschiedlich.

## <a name="prefixes"></a>Präfixe

Wenn Sie auf eine [*CIM*](windows-remote-management-glossary.md) 2,1-Klasse (z. b. [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile)) zugreifen, unterscheidet sich das Präfix des URI vom Präfix für eine CIM 2,9-Klasse, z. b. **CIM \_ admindomain**. CIM 2,1-Klassen sind im Abschnitt [CIM-Klassen](/windows/desktop/WmiSdk/cimclas) von Windows-Verwaltungsinstrumentation (WMI) dokumentiert.

Die meisten [WMI-Klassen](/windows/desktop/WmiSdk/wmi-classes) befinden sich im Stamm- **\\ CIMV2** -WMI-Namespace. Die Klassen für den Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider))-Anbieter befinden sich in der Stamm **\\ Hardware**.

Die folgende Liste enthält die Ressourcen-URI-Präfixe für diese Schemas:

-   WMI-oder CIM 2,1-Klassen im **root \\ CIMV2** -Namespace

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   CIM 2,9-Klassen oder IPMI-Klassen

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   Alternative Methode für den Zugriff auf IPMI-Anbieter Klassen

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

Weitere Informationen finden Sie unter [Ressourcen-URIs](resource-uris.md) und [URLPrefix](/windows/desktop/Http/urlprefix-strings)-Zeichen folgen. Weitere Informationen zum Erstellen eines URI für eine WMI-Klasse oder-Methode finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).

## <a name="prefix-aliases"></a>Präfix Aliase

Ein Präfix-Alias ist eine Verknüpfung, die das lange Ressourcen-URI-Präfix darstellt. Sie können auch Aliase in der **WinRM** -Befehlszeile verwenden. Geben Sie **WinRM-Hilfe Aliase** ein, um eine Liste der verfügbaren Aliase anzuzeigen.

Beachten Sie, dass ein Alias nicht innerhalb eines Endpunkt Verweises (EPR) verwendet werden kann, wenn ein Ressourcen-URI angegeben wird. Windows-Remoteverwaltung kann den Alias nicht erweitern, wenn er in XML eingebettet ist.

Im folgenden Codebeispiel wird der WinRM-Alias in einem EPR anstelle des gesamten Ressourcen-URI verwendet, der ist `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` . In diesem Fall gibt WinRM einen Fehler zurück, der angibt, dass der Dienst die Anforderung nicht verarbeiten kann.


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



In der folgenden Liste sind die definierten Aliase und Ressourcen-URIs aufgeführt, deren Ersatz Sie ersetzen.

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>WMI
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span id="cimv2"></span><span id="CIMV2"></span>CIMV2
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span id="winrm"></span><span id="WINRM"></span>WinRM
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>WSMAN
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>schel
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[Ressourcen-URIs](resource-uris.md)
</dt> </dl>
