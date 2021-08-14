---
title: WinRM-Dienst-Plug-In-Konfiguration
description: Ein winRM-Plug-In (Windows Remote Management) muss im WinRM-Katalog registriert werden, damit die Infrastruktur die verfügbaren Plug-Ins und ressourcen-URIs, die sie unterstützen, dynamisch bestimmen kann.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b82b24b8631cd6a47a879a6fa0684b9b2ac9c542699396d0f0997afe14cac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323719"
---
# <a name="winrm-service-plug-in-configuration"></a>WinRM-Dienst-Plug-In-Konfiguration

Ein winRM-Plug-In (Windows Remote Management) muss im WinRM-Katalog registriert werden, damit die Infrastruktur die verfügbaren Plug-Ins und [*ressourcen-URIs,*](windows-remote-management-glossary.md) die sie unterstützen, dynamisch bestimmen kann. Alle [*Ressourcen-URIs*](windows-remote-management-glossary.md) für WinRM-Plug-Ins müssen dem format entsprechen, das in RFC 3986 ( ) definiert [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ist. Die Konfiguration erfolgt über den WinRM-Hauptdienst.

Der folgende Befehl registriert eine Plug-In-Konfiguration beim WinRM-Dienst:

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> Der WinRM-Dienst muss neu gestartet werden, um die neu registrierten Plug-Ins verfügbar zu machen.

Die Plug-In-Konfiguration wird in XML angegeben. Im Folgenden finden Sie ein Beispiel.

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



In der folgenden Liste werden die XML-Elemente ausführlicher beschrieben, gefolgt von dem als XSD angegebenen Konfigurationsschema.

<dl> <dt>

<span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**
</dt> <dd>

Gibt den Dateinamen des Operations-Plug-Ins an. Alle Umgebungsvariablen, die in diesem Eintrag enthalten sind, werden im Kontext des Benutzers erweitert, wenn eine Anforderung eingeht. Jeder Benutzer kann über eine andere Version derselben Umgebungsvariablen verfügen, sodass jeder Benutzer ein anderes Plug-In verwenden kann. Dieser Eintrag darf nicht leer sein und muss auf ein gültiges Plug-In verweisen.

</dd> <dt>

<span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Name**
</dt> <dd>

Gibt den Anzeigenamen an, der für das Plug-In verwendet werden soll. Wenn vom Plug-In ein Fehler zurückgegeben wird, wird dieser Name in die Fehler-XML-Datei aufgenommen, die an die Clientanwendung zurückgegeben wird. Der Name gilt für kein bestimmtes Gebietsschema.

</dd> <dt>

<span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Architektur**
</dt> <dd>

Gibt an, ob das Betriebs-Plug-In 32-Bit oder 64-Bit ist. Wenn dieses Element nicht angegeben ist, wird der Wert auf x86-Systemen standardmäßig auf "32" und auf 64-Bit-Systemen auf "64" festgelegt. Für x86-Systeme ist der einzige gültige Wert "32". Wenn der Wert in einem 64-Bit-System "32" ist, muss bei der Eingabe der **Dateinameninformationen** die Wow64-Umleitung berücksichtigt werden. Das zugrunde liegende Dateisystem verwendet die Wow64-Umleitung, um system32 in syswow64 zu übersetzen. Wenn der **Dateiname** beispielsweise "%windir% \\ system32 \\myplugin.dll" und die **Architektur** "32" lautet, befindet sich die tatsächliche Plug-In-Datei unter "%windir% \\ syswow64 \\myplugin.dll".

</dd> <dt>

<span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **XmlRenderingType**
</dt> <dd>

Konfiguriert das Format, in dem XML über das [**WSMAN \_ DATA-Objekt**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) an Plug-Ins übergeben wird. Folgende Dateitypen sind verfügbar:

<dl> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Eingehende XML-Daten sind in einer WSMAN \_ DATA \_ TYPE \_ TEXT-Struktur enthalten, die den XML-Code als **PCWSTR-Speicherpuffer** darstellt.

</dd> <dt>

<span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>Xmlreader
</dt> <dd>

Eingehende XML-Daten sind in einer \_ WSMAN DATA \_ TYPE \_ WS XML \_ \_ READER-Struktur enthalten, die den XML-Code als **XmlReader-Objekt** darstellt, das in der WebServices.h-Headerdatei definiert ist.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**
</dt> <dd>

Dieser Knoten ist optional und ermöglicht einem Plug-In die Konfiguration zusätzlicher XML-Daten, die an die [**WSManPluginStartup-Methode**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)übergeben werden. Die meisten Plug-Ins benötigen diese zusätzlichen Informationen nicht, aber wenn ein Plug-In in mehr als einem Szenario verwendet werden muss, das eine andere Laufzeitsemantik erfordert, bietet dieses XML dem Plug-In die Flexibilität, dies zu tun.

</dd> <dt>

<span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Ressourcen**
</dt> <dd>

Gibt eine Liste der [*Ressourcen-URIs*](windows-remote-management-glossary.md)an, die dieses Plug-In unterstützt. Mindestens ein **ResourceUri-Eintrag** muss angegeben werden. Andernfalls wird der XML-Code abgelehnt.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Ressourcen** / **Ressource**
</dt> <dd>

Stellt eine einzelne [*Ressourcen-URI-Konfiguration*](windows-remote-management-glossary.md)dar.

> [!Note]  
> Das **SupportsOptions-Attribut** kann auf FALSE festgelegt werden. Wenn **SupportsOptions** auf FALSE festgelegt ist, wird dieses Attribut nicht aufgelistet, wenn die Ressource aufgezählt wird.

 

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Ressourcen** / **Ressource** / **ResourceUri**
</dt> <dd>

Gibt einen einzelnen [*Ressourcen-URI*](windows-remote-management-glossary.md) entweder vollständig oder als partielle Übereinstimmungszeichenfolge basierend auf dem **ExactMatch-Attribut** an. Wenn **ExactMatch** nicht vorhanden ist, wird standardmäßig **False** verwendet. Dies bedeutet, dass der WinRM-SOAP-Prozessor eine partielle Übereinstimmung mit dem Anfang des *Ressourcen-URI* vorgibt und diese an das Plug-In übergibt, wenn eine Übereinstimmung vorhanden ist. Das **SupportsOptions-Attribut** kann angegeben werden, wenn für diesen *Ressourcen-URI* Optionen übergeben werden dürfen. Standardmäßig werden keine Optionen unterstützt, und wenn eine der Optionen in der Clientanforderung vorhanden ist, wird ein Fehler zurückgegeben. Wenn Optionen vom Plug-In unterstützt werden, ist es wichtig, dass das Plug-In den richtigen Fehler zurückgibt, wenn eine Option vorhanden ist, die das Plug-In nicht versteht, wenn das **mustUnderstand-Flag** auf **True** festgelegt ist.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Ressourcen** / **Ressource** / **Funktion**
</dt> <dd>

Gibt eine Funktion an, die für diesen [*Ressourcen-URI*](windows-remote-management-glossary.md)verfügbar ist. Es gibt einen Eintrag für jeden Vorgangstyp, der unterstützt wird. Die folgenden Optionen sind verfügbar:

<dl> <dt>

<span id="Get"></span><span id="get"></span><span id="GET"></span>Erhalten
</dt> <dd>

Get-Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **Attribut SupportFragment** wird verwendet, wenn der get-Vorgang das Konzept unterstützt. Das **SupportFiltering-Attribut** ist ungültig und sollte auf FALSE festgelegt werden. Diese Funktion ist für einen *Ressourcen-URI* ungültig, wenn auch Shellvorgänge unterstützt werden.

</dd> <dt>

<span id="Put"></span><span id="put"></span><span id="PUT"></span>Put
</dt> <dd>

Put-Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **Attribut SupportFragment** wird verwendet, wenn der Put-Vorgang das Konzept unterstützt. Das **SupportFiltering-Attribut** ist ungültig und sollte auf **False** festgelegt werden. Diese Funktion ist für einen *Ressourcen-URI* ungültig, wenn auch Shellvorgänge unterstützt werden.

</dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>Erstellen
</dt> <dd>

Erstellungsvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **Attribut SupportFragment** wird verwendet, wenn der Erstellungsvorgang das Konzept unterstützt. Das **SupportFiltering-Attribut** ist ungültig und sollte auf **False** festgelegt werden. Diese Funktion ist für einen *Ressourcen-URI* ungültig, wenn auch Shellvorgänge unterstützt werden.

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Löschen
</dt> <dd>

Löschvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **Attribut SupportFragment** wird verwendet, wenn der Löschvorgang das Konzept unterstützt. Das **SupportFiltering-Attribut** ist ungültig und sollte auf **False** festgelegt werden. Diese Funktion ist für einen *Ressourcen-URI* ungültig, wenn auch Shellvorgänge unterstützt werden.

</dd> <dt>

<span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Aufrufen
</dt> <dd>

Aufrufvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **Attribut SupportFragment** wird für Aufrufvorgänge nicht unterstützt und sollte auf FALSE festgelegt werden. Das **SupportFiltering-Attribut** ist ungültig und sollte auf **False** festgelegt werden. Diese Funktion ist für einen *Ressourcen-URI* ungültig, wenn auch Shellvorgänge unterstützt werden.

</dd> <dt>

<span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Auflisten
</dt> <dd>

Aufzählvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **Attribut SupportFragment** wird für Aufzählungsvorgänge nicht unterstützt und sollte auf **False** festgelegt werden. Das **SupportFiltering-Attribut** ist gültig, und wenn das Plug-In das Filtern unterstützt, sollte dieses Attribut auf **True** festgelegt werden. Diese Funktion ist für einen *Ressourcen-URI* ungültig, wenn auch Shellvorgänge unterstützt werden.

</dd> <dt>

<span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Abonnieren
</dt> <dd>

Abonnieren-Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **Attribut SupportFragment** wird für Subscribe-Vorgänge nicht unterstützt und sollte auf **FALSE** festgelegt werden. Das **SupportFiltering-Attribut** ist ungültig und sollte auf **False** festgelegt werden. Diese Funktion ist für einen *Ressourcen-URI* ungültig, wenn auch Shellvorgänge unterstützt werden.

</dd> <dt>

<span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Muschel
</dt> <dd>

Shellvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **Attribut SupportFragment** wird für Shellvorgänge nicht unterstützt und sollte auf **False** festgelegt werden. Das **SupportFiltering-Attribut** ist ungültig und sollte auf **False** festgelegt werden. Diese Funktion ist für einen *Ressourcen-URI* ungültig, wenn auch eine andere Vorgangsfunktion unterstützt wird. Wenn eine Shell-Vorgangsfunktion für einen *Ressourcen-URI* konfiguriert ist, werden Vorgänge zum Abrufen, Put, Erstellen, Löschen, Aufrufen und Aufzählen intern innerhalb des WinRm-Diensts verarbeitet, um Shells zu verwalten. Daher kann das Plug-In die Vorgänge selbst nicht behandeln.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Ressourcen** / **Ressource** / **Sicherheit**
</dt> <dd>

Dieses Element definiert den Sicherheitsdeskriptor (über das **Sddl-Attribut),** der angewendet werden soll, um den Zugriff auf einen bestimmten [*Ressourcen-URI*](windows-remote-management-glossary.md) (über das **URI-Attribut)** zu bestimmen. Wenn **ExactMatch** nicht vorhanden ist, wird das **Security-Element** standardmäßig auf **False** festgelegt. Dies bedeutet, dass die **Sddl** für alle *Ressourcen-URIs* gilt, die **den URI** als Präfix verwenden. Wenn **ExactMatch** auf TRUE festgelegt ist, gilt **die Sddl** nur für den genauen angegebenen **URI.** Wenn mehrere **Sicherheitseinträge** vorhanden sind, die auf eine bestimmte *Ressourcen-URIs* angewendet werden können, wird die längste Präfixübereinsprechung verwendet, um die entsprechende **Sddl** zu bestimmen. Wenn ein **URI-Eintrag** mit exakter Übereinstimmung vorhanden ist, wird er aufgrund der längsten Präfixübereinführung immer als entsprechendes Security-Element ausgewählt.

</dd> </dl>

Im Folgenden wird das Plug-In-Konfigurationsschema als XSD angegeben.

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




