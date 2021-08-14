---
title: Ressourcen-URIs
description: Ein Ressourcen-URI ist ein Bezeichner für einen bestimmten Typ von Verwaltungsvorgang oder -wert, der von Verwaltungsdiensten verwendet wird, die das WS-Management implementieren.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93f13e18abd7ea452b84043dfef3d6bf6b18be6c476c0dfff9a34e42e45dbc14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323727"
---
# <a name="resource-uris"></a>Ressourcen-URIs

Ein [*Ressourcen-URI*](windows-remote-management-glossary.md) ist ein Bezeichner für einen eindeutigen Typ von Verwaltungsvorgang oder -wert, der von Verwaltungsdiensten verwendet wird, die das WS-Management implementieren. Ein Verwaltungswert kann die Temperatur innerhalb eines Computers sein. Ein Beispiel für einen Verwaltungsvorgang ist das Starten eines beendeten Diensts oder das Festlegen eines Datenträger-Volumebenutzerkontingents.

## <a name="resource-uri-format"></a>Ressourcen-URI-Format

Ein URI besteht aus einem Präfix und einem Pfad zu einer Ressource, wie im folgenden Beispiel gezeigt:

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Diese Schemaspezifikation gibt an, dass der URI auf Version 1 des offiziellen WS-Management-Protokolls basiert und dass die Ressource ein [**logischer \_ Win32-Datenträger**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) im Namespace "root \\ cimv2" des WMI-Repositorys ist. URI-Präfixe enthalten eine Schemaspezifikation wie "schemas.microsoft.com/wbem/wsman/1/wmi" und einen bestimmten Ressourcentyp, z. B. **Win32 \_ LogicalDisk**. Weitere Informationen zum Identifizieren einer bestimmten Instanz einer WMI-Klasse finden Sie unter Windows [Remoteverwaltung und WMI.](windows-remote-management-and-wmi.md)

Weitere Informationen finden Sie unter [URI-Präfixe.](uri-prefixes.md)

## <a name="types-of-resource-uris"></a>Typen von Ressourcen-URIs

Während [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) die primäre Quelle für Verwaltungsdaten für Windows-basierte Betriebssysteme ist, gibt es auch andere Quellen des Verwaltungsschemas.

In der folgenden Liste werden verschiedene Arten von Ressourcen-URIs beschrieben, die von Windows Remoteverwaltung verwendet werden:

-   WMI-URIs

    Diese Gruppe von URIs stellt [*einen*](/windows/desktop/WmiSdk/gloss-c) Common Information Model-Klassenpfad dar, der Namespace und Klasse enthält.

    WMI-URIs können in:

    -   [**Sitzungsmethoden**](session.md)
    -   [**IWSManSession-Methoden**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
    -   [**WSMan.CreateResourceLocator- oder**](wsman-createresourcelocator.md) [**IWSMan.CreateResourceLocator-Methoden**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
    -   [**ResourceLocator-**](resourcelocator.md) [**oder IWSManResourceLocator-Methoden**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

-   IPMI-URIs

    Diese Gruppe von URIs stellt Branchenstandard-URIs dar, die auf CIM-Version 2.9 basieren. IPMI-URIs können in den [**Sitzungsmethoden**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate und**](session-enumerate.md) Invoke [**verwendet werden.**](session-invoke.md)

    z. B. https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Diese Ressource wird gemäß [](https://www.dmtf.org/home) dem DMTF.org CIM-Schema definiert.

-   WinRM-Konfigurations-URIs

    Diese Gruppe von URIs sind Konfigurationsvorgänge für die [*WinRM-Listenerkonfiguration.*](windows-remote-management-glossary.md)

    https://schemas.microsoft.com/wbem/wsman/1/config/listenerkann in den [**Sitzungsmethoden**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md)und [**Enumerate verwendet werden.**](session-enumerate.md)

-   [*URIs des Systemereignisprotokolls*](windows-remote-management-glossary.md) (SEL)

    Diese Gruppe von URIs abonniert Ereignissammlerereignisse vom BMC. Sie können diese Ereignisse mithilfe des **Befehlszeilentools Wevtutil** abonnieren. Weitere Informationen finden Sie unter https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Groß- und Kleinschreibung

Das [*WMI-Plug-In*](windows-remote-management-glossary.md) behält den Fall des in einer Anforderung empfangenen Ressourcen-URI bei. Um jedoch die Interoperabilität mit anderen Implementierungen des WS-Management sicherzustellen, verwenden Sie den richtigen Fall für die angeforderte Ressource im Ressourcen-URI. Der richtige Fall ist die vom Ressourcenanbieter definierte Rechtschreibung.

Für Ressourcen-URIs ist zwar keine Sensitivität zwischen Denk-, [*Fragment-XML-Code und*](windows-remote-management-glossary.md) -Code erforderlich. Ein Fragment gibt nur eine Eigenschaft an, nicht den gesamten Satz von Eigenschaften für eine Ressource. Im Fall von WMI-Ressourcen ruft die Fragmentsyntax eine Eigenschaft aus einer Ressourceninstanz ab. Wenn Sie beispielsweise nur die **Version-Eigenschaft** von [**Win32 \_ OperatingSystem abrufen,**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) muss ein Fragment verwendet werden. Weitere Informationen zu Fragmenten finden Sie unter "Hinzufügen eines Selektors zu einem ResourceLocator- oder IWSManResourceLocator-Objekt" in Windows [Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).

Das [*WMI-Plug-In*](windows-remote-management-glossary.md) folgt den XML- und [*XPath-Standards*](windows-remote-management-glossary.md) und erzwingt die Sensitivität zwischen Zeichenfolgen und XML, die die Eingabeparameter für eine Methode definieren. Zur Unterstützung des XPath 1.0/Level 1-Standards ist Sensitivität erforderlich. Um WMI-Daten über WinRM zu erhalten, bedeutet die Sensitivität, dass die Namen von WMI-Klassen, -Eigenschaften und -Methoden mit dem Namen im WMI-Repository übereinstimmen müssen.

Weitere Informationen finden Sie unter [XPath-Syntax.](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100))

## <a name="case-sensitivity-examples"></a>Beispiele für die Sensitivität von Fällen

Beispielsweise kann ein Skript, das die **SECURITY \_ DESCRIPTOR-Eigenschaft** von einer Instanz der WMI-Win32-Dienstklasse erhält, keine Groß-/Groß geschrieben für die Namen im Fragmentpfad verwenden, sondern nur den URI. [**\_**](/windows/desktop/CIMWin32Prov/win32-service) Das [*WinRM-WMI-Plug-In*](windows-remote-management-glossary.md) gibt einen Fehler für das folgende VBScript-Beispiel zurück, da die für **FragmentPath** bereitgestellte XPath-XML nicht den richtigen Fall verwendet. Im WMI-Repository hat die Klasse die Schreibweise \_ "Win32-Dienst".


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



Die folgende Version des gleichen Beispiels zeigt die richtige Verwendung von case für die [**\_ Win32-Dienstklasse**](/windows/desktop/CIMWin32Prov/win32-service) und die **SECURITY \_ DESCRIPTOR-Eigenschaft.**


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Remotehardwareverwaltung](remote-hardware-management.md)
</dt> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

 