---
title: Konfiguration des WinRM-Dienst-Plug-ins
description: Ein Windows-Remoteverwaltung-Plug-in (WinRM) muss im WinRM-Katalog registriert sein, damit die Infrastruktur den Satz der verfügbaren Plug-ins und die von Ihnen unterstützten Ressourcen-URIs dynamisch ermitteln kann.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316736"
---
# <a name="winrm-service-plug-in-configuration"></a>Konfiguration des WinRM-Dienst-Plug-ins

Ein Windows-Remoteverwaltung-Plug-in (WinRM) muss im WinRM-Katalog registriert sein, damit die Infrastruktur den Satz der verfügbaren Plug-ins und die von Ihnen unterstützten [*Ressourcen-URIs*](windows-remote-management-glossary.md) dynamisch ermitteln kann. Alle [*Ressourcen-URIs*](windows-remote-management-glossary.md) für WinRM-Plug-Ins müssen dem Format entsprechen, das in RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ) definiert ist. Die Konfiguration erfolgt über den WinRM-Hauptdienst.

Der folgende Befehl registriert eine Plug-in-Konfiguration beim WinRM-Dienst:

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> Der WinRM-Dienst muss neu gestartet werden, um die neu registrierten Plug-Ins verfügbar zu machen.

Die Plug-in-Konfiguration ist in XML angegeben. Im Folgenden finden Sie ein Beispiel.

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



In der folgenden Liste werden die XML-Elemente ausführlicher beschrieben, und es folgt das als XSD angegebene Konfigurations Schema.

<dl> <dt>

<span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**Pluginconfiguration** / **Operationsconfiguration**
</dt> <dd>

Gibt den Dateinamen des Vorgangs-Plug-ins an. Alle Umgebungsvariablen, die in diesen Eintrag eingefügt werden, werden im Kontext des Benutzers erweitert, wenn eine Anforderung empfangen wird. Jeder Benutzer kann über eine andere Version derselben Umgebungsvariablen verfügen, sodass jeder Benutzer ein anderes Plug-in haben könnte. Dieser Eintrag darf nicht leer sein und muss auf ein gültiges Plug-in zeigen.

</dd> <dt>

<span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**Pluginconfiguration** / **Name**
</dt> <dd>

Gibt den anzeigen Amen an, der für das Plug-in verwendet werden soll. Wenn vom Plug-in ein Fehler zurückgegeben wird, wird dieser Name in die Fehler-XML-Datei eingefügt, die an die Client Anwendung zurückgegeben wird. Der Name gilt für kein bestimmtes Gebietsschema.

</dd> <dt>

<span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**Pluginconfiguration** / **Architektur**
</dt> <dd>

Gibt an, ob das Operations-Plug-in 32-Bit oder 64-Bit ist. Wenn dieses Element nicht angegeben ist, wird der Wert standardmäßig auf x86-Systemen auf "32" und auf 64-Bit-Systemen auf "64" festgelegt. Für x86-Systeme ist der einzige gültige Wert "32". Wenn der Wert "32" auf einem 64-Bit-System ist, muss die WOW64-Umleitung beim Eingeben der **Dateiname** -Informationen berücksichtigt werden. Das zugrunde liegende Dateisystem verwendet die WOW64-Umleitung zum Übersetzen von system32 in syswow64. Wenn der **Dateiname** z. b. "% windir% \\ system32 \\myplugin.dll" und die **Architektur** den Wert "32" hat, befindet sich die tatsächliche Plug-in-Datei unter "% windir% \\ syswow64 \\myplugin.dll".

</dd> <dt>

<span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**Pluginconfiguration** / **Xmlrenderingtype**
</dt> <dd>

Konfiguriert das Format, in dem XML an Plug-ins über das [**WSMAN- \_ Daten**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) Objekt übermittelt wird. Folgende Dateitypen sind verfügbar:

<dl> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Eingehende XML-Daten sind in der Text Struktur eines WSMAN- \_ \_ Datentyps enthalten \_ , der den XML-Code als **pcwstr** -Arbeitsspeicher Puffer darstellt.

</dd> <dt>

<span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XmlReader
</dt> <dd>

Eingehende XML-Daten sind in \_ der WS XML Reader-Struktur eines WSMAN- \_ Datentyps enthalten \_ , der \_ den XML-Code \_ als **XmlReader** -Objekt darstellt, das in der Header Datei "Webservices. h" definiert ist.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**Pluginconfiguration** / **Initializationxml**
</dt> <dd>

Dieser Knoten ist optional und ermöglicht einem Plug-in das Konfigurieren zusätzlicher XML-Daten, die an die [**wsmanpluginstartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)-Methode übermittelt werden. Die meisten Plug-Ins benötigen diese zusätzlichen Informationen nicht. Wenn jedoch ein Plug-in in mehr als einem Szenario verwendet werden muss, das eine andere Lauf Zeit Semantik erfordert, gibt dieser XML-Code dem Plug-in die Flexibilität.

</dd> <dt>

<span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**Pluginconfiguration** / **Ressourcen**
</dt> <dd>

Gibt eine Liste von [*Ressourcen-URIs*](windows-remote-management-glossary.md)an, die dieses Plug-in unterstützt. Mindestens ein **resourceUri**-Eintrag muss angegeben werden. Andernfalls wird der XML-Code zurückgewiesen.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**Pluginconfiguration** / **Ressourcen** / **Ressource**
</dt> <dd>

Stellt eine einzelne [*Ressourcen-URI*](windows-remote-management-glossary.md)-Konfiguration dar.

> [!Note]  
> Das **supportsoptions**-Attribut kann auf "false" festgelegt werden. Wenn **supportsoptions** auf false festgelegt ist, wird dieses Attribut nicht aufgelistet, wenn die Ressource aufgezählt wird.

 

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**Pluginconfiguration** / **Ressourcen** / **Ressource** / **ResourceUri**
</dt> <dd>

Gibt einen einzelnen [*Ressourcen-URI*](windows-remote-management-glossary.md) entweder vollständig oder als partielle Vergleichs Zeichenfolge basierend auf dem **exactMatch** -Attribut an. Wenn " **exactMatch** " nicht vorhanden ist, wird standardmäßig " **false**" verwendet. Dies bedeutet, dass der WinRM-SOAP-Prozessor eine partielle Entsprechung zum Anfang des *Ressourcen-URI* findet und eine Entsprechung an das Plug-in übergibt. Das **supportsoptions** -Attribut kann angegeben werden, wenn für diesen *Ressourcen-URI* alle Optionen übermittelt werden dürfen. Standardmäßig werden keine Optionen unterstützt, und wenn in der Client Anforderung eine vorhanden ist, wird ein Fehler zurückgegeben. Wenn Optionen vom Plug-in unterstützt werden, ist es wichtig, dass das Plug-in den korrekten Fehler zurückgibt, wenn eine Option vorhanden ist, die das Plug-in nicht versteht, wenn das **MustUnderstand** -Flag auf **true** festgelegt ist.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**Pluginconfiguration** / **Ressourcen** / **Ressource** / **Funktion**
</dt> <dd>

Gibt eine Funktion an, die für diesen [*Ressourcen-URI*](windows-remote-management-glossary.md)verfügbar ist. Es gibt einen Eintrag für jeden Vorgangstyp, den er unterstützt. Die folgenden Optionen sind verfügbar:

<dl> <dt>

<span id="Get"></span><span id="get"></span><span id="GET"></span>Erhalten
</dt> <dd>

Get-Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **supportfragment** -Attribut wird verwendet, wenn der Get-Vorgang das Konzept unterstützt. Das **supportfiltering** -Attribut ist ungültig und sollte auf false festgelegt werden. Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.

</dd> <dt>

<span id="Put"></span><span id="put"></span><span id="PUT"></span>Stellte
</dt> <dd>

Put-Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **supportfragment**-Attribut wird verwendet, wenn der Put-Vorgang das Konzept unterstützt. Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden. Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.

</dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>Stelle
</dt> <dd>

Erstellungs Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **supportfragment** -Attribut wird verwendet, wenn der Create-Vorgang das Konzept unterstützt. Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden. Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Lösch
</dt> <dd>

Löschvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **supportfragment** -Attribut wird verwendet, wenn der DELETE-Vorgang das Konzept unterstützt. Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden. Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.

</dd> <dt>

<span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Blaze
</dt> <dd>

Startvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **supportfragment** -Attribut wird für Aufruf Vorgänge nicht unterstützt und sollte auf false festgelegt werden. Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden. Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.

</dd> <dt>

<span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Auflisten
</dt> <dd>

Enumeringvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **supportfragment** -Attribut wird für auflisten-Vorgänge nicht unterstützt und sollte auf **false** festgelegt werden. Das **supportfiltering** -Attribut ist gültig, und wenn das Plug-in das Filtern unterstützt, sollte dieses Attribut auf " **true**" festgelegt werden. Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.

</dd> <dt>

<span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Abonnieren
</dt> <dd>

Abonnement Vorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **supportfragment** -Attribut wird für abonnieren-Vorgänge nicht unterstützt und sollte auf **false** festgelegt werden. Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden. Diese Funktion ist für einen Ressourcen- *URI* ungültig, wenn Shellvorgänge ebenfalls unterstützt werden.

</dd> <dt>

<span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Schel
</dt> <dd>

Shellvorgänge werden für den [*Ressourcen-URI*](windows-remote-management-glossary.md)unterstützt. Das **supportfragment** -Attribut wird für Shellvorgänge nicht unterstützt und sollte auf **false** festgelegt werden. Das **supportfiltering** -Attribut ist ungültig und sollte auf **false** festgelegt werden. Diese Funktion ist für einen Ressourcen- *URI* nicht gültig, wenn eine andere Vorgangs Funktion ebenfalls unterstützt wird. Wenn eine shellvorgangsaktionen für einen *Ressourcen-URI* konfiguriert ist, werden Get-, Put-, CREATE-, DELETE-, Aufruf-und auflisten-Vorgänge intern im WinRM-Dienst verarbeitet, um Shells zu verwalten. Folglich kann das Plug-in nicht mit den Vorgängen selbst umgehen.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**Pluginconfiguration** / **Ressourcen** / **Ressource** / **Sicherheit**
</dt> <dd>

Dieses Element definiert die Sicherheits Beschreibung (über das **SDDL** -Attribut), die angewendet werden soll, um den Zugriff auf einen bestimmten [*Ressourcen-URI*](windows-remote-management-glossary.md) zu bestimmen (über das **URI** -Attribut). Wenn **exactMatch** nicht vorhanden ist, wird das **Sicherheits** Element standardmäßig auf **false** festgelegt. Dies bedeutet, dass die **SDDL** für alle *Ressourcen-URIs* gilt, die **URI** als Präfix freigeben. Wenn **exactMatch** auf true festgelegt ist, gilt die **SDDL** nur für den angegebenen **URI** . Wenn mehrere **Sicherheits** Einträge vorhanden sind, die auf einen bestimmten *Ressourcen-URIs* angewendet werden können, wird der entsprechende **SDDL** mit der längsten Präfix Übereinstimmung bestimmt. Wenn ein **URI** -Eintrag mit dem längsten Präfix vorhanden ist, wird er immer als entsprechendes Sicherheitselement ausgewählt.

</dd> </dl>

Im folgenden wird das Plug-in-Konfigurations Schema als XSD angegeben.

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

 

 




