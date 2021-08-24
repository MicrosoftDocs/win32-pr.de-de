---
title: URI-Präfixe
description: Das Ressourcen-URI-Präfix ist abhängig davon, welches XML-Schema die Ressource beschreibt.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b44744d7ac7d158bd7d00423396681fef1499c94d61b5cb74a1dee48dad5c784
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898670"
---
# <a name="uri-prefixes"></a>URI-Präfixe

Das [*Ressourcen-URI-Präfix*](windows-remote-management-glossary.md) ist abhängig davon, welches XML-Schema die Ressource beschreibt.

## <a name="prefixes"></a>Präfixe

Wenn Sie auf eine [*CIM*](windows-remote-management-glossary.md) 2.1-Klasse wie [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile)zugreifen, unterscheidet sich das Präfix des URI vom Präfix für eine CIM 2.9-Klasse, z. B. **CIM \_ AdminDomain**. CIM 2.1-Klassen sind im Abschnitt [CIM-Klassen](/windows/desktop/WmiSdk/cimclas) der Windows Management Instrumentation (WMI) dokumentiert.

Die [meisten WMI-Klassen](/windows/desktop/WmiSdk/wmi-classes) befinden sich im WMI-Stammnamespace **\\ cimv2.** Klassen für den Anbieter von Microsoft Intelligent Platform Management Interface [(IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)befinden sich in **der \\ Stammhardware.**

Die folgende Liste enthält die Ressourcen-URI-Präfixe für diese Schemas:

-   WMI- oder CIM 2.1-Klassen im **\\ Cimv2-Stammnamespace**

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   CIM 2.9-Klassen oder IPMI-Klassen

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   Alternative Möglichkeit für den Zugriff auf IPMI-Anbieterklassen

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

Weitere Informationen finden Sie unter [Ressourcen-URIs](resource-uris.md) und [UrlPrefix-Zeichenfolgen.](/windows/desktop/Http/urlprefix-strings) Weitere Informationen zum Generieren eines URI für eine WMI-Klasse oder -Methode finden Sie unter Windows [Remoteverwaltung und WMI.](windows-remote-management-and-wmi.md)

## <a name="prefix-aliases"></a>Präfixaliase

Ein Präfixalias ist eine Verknüpfung, die das Lange Ressourcen-URI-Präfix darstellt. Aliase können auch in der **Winrm-Befehlszeile** verwendet werden. Um eine Liste der verfügbaren Aliase anzeigen zu können, geben **Sie Winrm-Hilfealiase ein.**

Beachten Sie, dass ein Alias nicht innerhalb eines Endpunktverweises (EPR) verwendet werden kann, wenn ein Ressourcen-URI angegeben wird. Windows Die Remoteverwaltung kann den Alias nicht erweitern, wenn er in XML eingebettet ist.

Im folgenden Codebeispiel wird der winrm-Alias in einer EPR anstelle des vollständigen Ressourcen-URI verwendet, der `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` ist. In diesem Fall gibt WinRM einen Fehler zurück, der angibt, dass der Dienst die Anforderung nicht verarbeiten kann.


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



Im Folgenden werden definierte Aliase und Ressourcen-URIs aufgeführt, für die sie ersetzen.

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>Wmi
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span id="cimv2"></span><span id="CIMV2"></span>cimv2
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span id="winrm"></span><span id="WINRM"></span>Winrm
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>Wsman
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>Muschel
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Windows Remoteverwaltung und WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[Ressourcen-URIs](resource-uris.md)
</dt> </dl>
