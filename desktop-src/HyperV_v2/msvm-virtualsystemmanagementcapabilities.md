---
description: Beschreibt die Funktionen des zugeordneten MSVM \_ virtualsystemmanagementservice.
ms.assetid: 3a167b06-bddd-4bac-95c0-ecf14e01eec0
title: Msvm_VirtualSystemManagementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementCapabilities
- Msvm_VirtualSystemManagementCapabilities.InstanceID
- Msvm_VirtualSystemManagementCapabilities.Caption
- Msvm_VirtualSystemManagementCapabilities.Description
- Msvm_VirtualSystemManagementCapabilities.ElementName
- Msvm_VirtualSystemManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemManagementCapabilities.MaxElementNameLen
- Msvm_VirtualSystemManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemManagementCapabilities.ElementNameMask
- Msvm_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24bc8ce66393a5e9ccd13848ab74640aec8d1760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342789"
---
# <a name="msvm_virtualsystemmanagementcapabilities-class"></a>MSVM \_ virtualsystemmanagementfunktionalitäten-Klasse

Beschreibt die Funktionen des zugeordneten [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md).

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Management Service Capabilities";
  string  Description = "Defines Virtual System Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual System Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemmanagementfunktionsklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemmanagementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Asynchronousmethodssupported**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ virtualsystemmanagementfunktionalitäten. asynchronousmethodssupported")
</dt> </dl>

Gibt die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Methoden an, die asynchron von der-Implementierung unterstützt werden.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

**[**Validateplannedsystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

**[**Importsystemdefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

**[**Importsnapshotdefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

**[**Realizeplannedsystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

**[**Exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

**[**Addfeaturesettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

**[**Modifyfeaturesettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

**[**Removefeaturesettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

**[**Getvirtualsystemthumbnailimage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

**[**Modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

**[**Getsummaryinformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

**[**Addkvpitems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

**[**Modifykvpitems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

**[**Removekvpitems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

**[**Formaterror**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

**Requeststatechangesupported** (32789)


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

**Startservicesupportiert** (32790)


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

**Stopservicesupportiert** (32791)


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

**[**Modifydiskmergesettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

**[**Generatewwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

**[**Addspbrechannelchap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

**[**Removefbrechannelchap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

**[**Setguestnetworkadapterconfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

**[**Getsizeofsystemfiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

**[**Getcurrentwwpnfromgenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32799.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Elementnameeditsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **ElementName** -Eigenschaft geändert werden kann. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.

</dd> <dt>

**Elementnamemask**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Einschränkungen für **ElementName** an, ausgedrückt als regulärer Ausdruck. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.

</dd> <dt>

**Unterstützt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ virtualsystemmanagementfunktionalitäten. indicationssupported")
</dt> </dl>

Gibt die von der-Implementierung unterstützten Hinweise an.

Enumeration von Indikator Bezeichner, die jeweils einen von der-Implementierung unterstützten Hinweis identifizieren.

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**Virtualresourcestatus echanginditerationssupported** (2)


</dt> <dd>

Die-Implementierung unterstützt Benachrichtigungen über Zustandsänderungen von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Instanzen, die Ressourcen virtueller Systeme darstellen.

</dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>" **Concretejobstatus echangein" unterstützt** (3)


</dt> <dd>

Die-Implementierung unterstützt Benachrichtigungen über Zustandsänderungen von [**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85)) -Instanzen.

</dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**Virtualsystemstatus echangin-Unterstützung** (4)


</dt> <dd>

Die-Implementierung unterstützt Benachrichtigungen über Zustandsänderungen von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanzen, die virtuelle Systeme darstellen.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Hersteller reserviert** (32767.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Maxelementnamelen**
</dt> <dd> <dl> <dt>

Datentyp: **unit16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxValue** (256)
</dt> </dl>

Gibt die maximal unterstützte Länge der **ElementName** -Eigenschaft an. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.

</dd> <dt>

**Requestedstaatunter stützt**
</dt> <dd> <dl> <dt>

Datentyp: **unit16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Zustände an, die bei Verwendung der **requestStateChange** -Methode für das aktivierte logische Element angefordert werden können. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.



| Wert                                                                         | Bedeutung              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | Aktiviert<br/>   |
| <dl> <dt>3</dt> </dl>  | Deaktiviert<br/>  |
| <dl> <dt>4</dt> </dl>  | Herunterfahren<br/> |
| <dl> <dt>6</dt> </dl>  | Offline<br/>   |
| <dl> <dt>7</dt> </dl>  | Test<br/>      |
| <dl> <dt>8</dt> </dl>  | Wickeln<br/>     |
| <dl> <dt>9</dt> </dl>  | Stilllegen<br/>   |
| <dl> <dt>10</dt> </dl> | Reboot<br/>    |
| <dl> <dt>11</dt> </dl> | Reset<br/>     |



 

</dd> <dt>

**Synchronousmethodssupported**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ virtualsystemmanagementfunktionalitäten. synchronousmethodssupported")
</dt> </dl>

Gibt die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Methoden an, die von der-Implementierung synchron unterstützt werden.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

**[**Validateplannedsystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

**[**Importsystemdefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

**[**Importsnapshotdefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

**[**Realizeplannedsystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

**[**Exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

**[**Addfeaturesettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

**[**Modifyfeaturesettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

**[**Removefeaturesettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

**[**Getvirtualsystemthumbnailimage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

**[**Modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

**[**Getsummaryinformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

**[**Addkvpitems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

**[**Modifykvpitems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

**[**Removekvpitems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

**[**Formaterror**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

**Requeststatechangesupported** (32789)


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

**Startservicesupportiert** (32790)


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

**Stopservicesupportiert** (32791)


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

**[**Modifydiskmergesettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

**[**Generatewwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

**[**Addspbrechannelchap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

**[**Removefbrechannelchap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

**[**Setguestnetworkadapterconfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

**[**Getsizeofsystemfiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

**[**Getcurrentwwpnfromgenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32799.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Virtualsystemtypessupported**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichen folgen, die jeweils einen Typ eines virtuellen Systems festlegen, das von der Implementierung unterstützt wird. Der Wert jedes Array Elements, das nicht **null** ist, muss den Zeichen folgen entsprechen, die für die Eigenschaft " [**MSVM \_ virtualsystemsettingdata. virtualsystemtype**](msvm-virtualsystemsettingdata.md) " definiert sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

