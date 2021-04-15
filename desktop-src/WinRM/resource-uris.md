---
title: Ressourcen-URIs
description: Ein Ressourcen-URI ist ein Bezeichner für einen unterschiedlichen Typ von Verwaltungsvorgang oder Wert, der von Verwaltungsdiensten verwendet wird, die das WS-Management Protokoll implementieren.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516811"
---
# <a name="resource-uris"></a>Ressourcen-URIs

Ein [*Ressourcen-URI*](windows-remote-management-glossary.md) ist ein Bezeichner für einen unterschiedlichen Typ von Verwaltungsvorgang oder Wert, der von Verwaltungsdiensten verwendet wird, die das WS-Management Protokoll implementieren. Ein Verwaltungs Wert kann die Temperatur innerhalb eines Computers sein. Ein Beispiel für einen Verwaltungsvorgang ist das Starten eines beendeten dienbes oder das Festlegen eines Benutzer Kontingents für das Datenträger Volume.

## <a name="resource-uri-format"></a>Ressourcen-URI-Format

Ein URI besteht aus einem Präfix und einem Pfad zu einer Ressource, wie im folgenden Beispiel gezeigt:

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Diese Schema Spezifikation gibt an, dass der URI auf Version 1 des offiziellen WS-Management Protokolls basiert und dass es sich bei der Ressource um einen [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) im \\ Namespace "root cimv2" des WMI-Repository handelt. URI-Präfixe enthalten eine Schema Spezifikation, z. b. "Schemas.Microsoft.com/wbem/wsman/1/WMI", und einen bestimmten Ressourcentyp, z. b. **Win32 \_ LogicalDisk**. Weitere Informationen zum Identifizieren einer bestimmten Instanz einer WMI-Klasse finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).

Weitere Informationen finden Sie unter [URI-Präfixe](uri-prefixes.md).

## <a name="types-of-resource-uris"></a>Typen von Ressourcen-URIs

Während [*Windows-Verwaltungsinstrumentation (WMI)*](windows-remote-management-glossary.md) die primäre Quelle von Verwaltungsdaten für Windows-basierte Betriebssysteme ist, sind auch andere Quellen für das Verwaltungs Schema vorhanden.

In der folgenden Liste werden verschiedene Typen von Ressourcen-URIs beschrieben, die von Windows-Remoteverwaltung verwendet werden:

-   WMI-URIs

    Diese Gruppe von URIs stellt einen [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) Klassenpfad dar, der den Namespace und die Klasse enthält.

    WMI-URIs können in verwendet werden:

    -   [**Sitzungs**](session.md) Methoden
    -   [**Iwsmansession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) -Methoden
    -   [**WSMAN. kreateresourcelocator**](wsman-createresourcelocator.md) -Methode oder [**iwsman. kreateresourcelocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) -Methode
    -   [**ResourceLocator**](resourcelocator.md) -Methode oder [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) -Methode

-   IPMI-URIs

    Diese Gruppe von URIs stellt Branchenstandard-URIs dar, die auf CIM-Version 2,9 basieren. IPMI-URIs können in den [**Sitzungs**](session.md) Methoden [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) und [**aufrufen**](session-invoke.md)verwendet werden.

    z. B. https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Diese Ressource wird gemäß dem [DMTF.org](https://www.dmtf.org/home) CIM-Schema definiert.

-   WinRM-Konfigurations-URIs

    Diese Gruppe von URIs sind Konfigurations Vorgänge für die WinRM-[*Listenerkonfiguration*](windows-remote-management-glossary.md) .

    https://schemas.microsoft.com/wbem/wsman/1/config/listener kann in den [**Sitzungs**](session.md) Methoden [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md)und [**Enumerate**](session-enumerate.md)verwendet werden.

-   [*System Ereignisprotokoll*](windows-remote-management-glossary.md) -URIs (SEL)

    Diese Gruppe von URIs abonniert Ereignis Sammler Ereignisse aus dem BMC. Sie können diese Ereignisse mithilfe des Befehlszeilen Tools **wevtutil** abonnieren. Weitere Informationen finden Sie unter https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Groß- und Kleinschreibung

Das [*WMI-Plug-in*](windows-remote-management-glossary.md) behält die Groß-/Kleinschreibung des in einer Anforderung empfangenen Ressourcen-URI bei. Um die Interoperabilität mit anderen Implementierungen WS-Management Protokolls sicherzustellen, sollten Sie jedoch im Ressourcen-URI die richtige Groß-/Kleinschreibung für die angeforderte Ressource verwenden. Die richtige Groß-/Kleinschreibung ist die vom Ressourcenanbieter definierte Schreibweise.

Obwohl bei Ressourcen-URIs die Groß-/Kleinschreibung nicht beachtet werden muss, bewirkt XML- [*Fragment*](windows-remote-management-glossary.md) Ein Fragment gibt anstelle des gesamten Eigenschaften Satzes für eine Ressource nur eine Eigenschaft an. Im Fall von WMI-Ressourcen Ruft die fragmentsyntax eine Eigenschaft aus einer Ressourcen Instanz ab. Wenn Sie z. b. nur die **Version** -Eigenschaft von [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) erhalten, muss ein Fragment verwendet werden. Weitere Informationen zu Fragmenten finden Sie unter "Hinzufügen eines Selektor zu einem ResourceLocator-oder iwsmanresourcelocator-Objekt" in [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).

Nach den XML-und [*XPath*](windows-remote-management-glossary.md) -Standards erzwingt das [*WMI-Plug-in*](windows-remote-management-glossary.md) die Unterscheidung nach Groß-/Kleinschreibung für Fragmente und XML, die die Eingabeparameter für eine Methode definiert. Die Unterscheidung nach Groß-/Kleinschreibung ist für die Unterstützung von XPath 1.0/Level 1 erforderlich. Um WMI-Daten über WinRM zu erhalten, bedeutet die Unterscheidung nach Groß-/Kleinschreibung, dass die Namen von WMI-Klassen,-Eigenschaften und-Methoden mit der Groß-/Kleinschreibung des im WMI-Repository gefundenen namens

Weitere Informationen finden Sie unter [XPath-Syntax](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).

## <a name="case-sensitivity-examples"></a>Beispiele für die groß-

Beispielsweise kann ein Skript, das die **\_ sicherheitsbeschreibungenschaft** aus einer Instanz der WMI- [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse abruft, keine Großbuchstaben für die Namen im Fragmentpfad verwenden, sondern nur den URI. Das WinRM- [*WMI-Plug-in*](windows-remote-management-glossary.md) gibt für das folgende VBScript-Beispiel einen Fehler zurück, da die für den **fragmentpath** angegebene XPath-XML-Datei nicht die richtige Groß-/Kleinschreibung verwendet. Im WMI-Repository ist die Klasse "Win32- \_ Dienst".


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



Die folgende Version desselben Beispiels zeigt die korrekte Verwendung von Case für die Win32- [**\_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse und die **Sicherheits \_ deskriptoreigenschaft** .


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

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Remote Hardware Verwaltung](remote-hardware-management.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 