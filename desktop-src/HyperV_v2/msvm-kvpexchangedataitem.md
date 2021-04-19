---
description: Stellt ein Schlüssel-Wert-Paar dar.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Msvm_KvpExchangeDataItem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362963"
---
# <a name="msvm_kvpexchangedataitem-class"></a>MSVM- \_ kvpexchangedataitem-Klasse

Stellt ein Schlüssel-Wert-Paar dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a>Member

Die **MSVM- \_ kvpexchangedataitem** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ kvpexchangedataitem** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Daten**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Der Wertteil des Schlüssel-Wert-Paars.

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

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Der Schlüsselteil des Schlüssel-Wert-Paars.



| Schlüssel                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>CSDVersion</dt> </dl>                 | Eine Zeichenfolge, die die neueste Service Pack darstellt, die auf dem Gastsystem installiert ist. Beispiel: "Service Pack 2". Wenn keine Service Pack installiert wurde, ist diese Zeichenfolge leer.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>FullyQualifiedDomainName</dt> </dl>   | Eine Zeichenfolge, die den voll qualifizierten DNS-Namen darstellt, der den lokalen Computer eindeutig identifiziert. Dieser Name ist eine Kombination aus dem DNS-Hostnamen und dem DNS-Domänen Namen unter Verwendung des-Formats *Hostname*. *Domänen Name*. Wenn der lokale Computer ein Knoten in einem Cluster ist, ist dieser Wert der voll qualifizierte DNS-Name des virtuellen Cluster Servers. Dieser Wert entspricht dem Namen, der von der [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) -Funktion zurückgegeben wird, wenn der *nametype* -Parameter "computernamednsfullyqualified" ist.<br/> |
| <dl> <dt>"Integrationservicesversion"</dt> </dl> | Eine Zeichenfolge, die die Version der Integration Services darstellt, die derzeit auf dem virtuellen Gastcomputer installiert ist (z. b. "6.1.7000.0").<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>"NetworkAddressIPv4"</dt> </dl>         | Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der IPv4-Adressen enthält, die zurzeit dem virtuellen Gastcomputer zugewiesen sind. Die Liste wird automatisch aktualisiert, sobald eine TCP/IP-Konfigurationsänderung auf dem virtuellen Gastcomputer auftritt. Jede Adresse wird in Punkt-Dezimal Schreibweise dargestellt. <br/>                                                                                                                                                                                                                         |
| <dl> <dt>"NetworkAddressIPv6"</dt> </dl>         | Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der IPv6-Adressen enthält, die derzeit dem virtuellen Gastcomputer zugewiesen sind. Die Liste wird automatisch aktualisiert, sobald eine TCP/IP-Konfigurationsänderung auf dem virtuellen Gastcomputer auftritt. Jede Adresse wird in einer Doppelpunkt-hexadezimal Notation dargestellt. Es ist nicht garantiert, dass die IPv4-und IPv6-Listen immer synchronisiert werden.<br/>                                                                                                                                             |
| <dl> <dt>"Osbuildnumber"</dt> </dl>              | Eine Zeichenfolge, die die Buildnummer des Betriebssystems darstellt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"Oseditionid"</dt> </dl>                | Eine Zeichenfolge, die die Edition (SKU) des Gast Betriebssystems des virtuellen Computers darstellt. Eine Liste möglicher Werte finden Sie unter der [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) -Funktion.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>OSName</dt> </dl>                     | Eine Zeichenfolge, die den Namen des Betriebssystems darstellt. Dieser Wert stammt aus dem folgenden Registrierungs Eintrag: **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**<br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <dt>OSMajorVersion</dt> </dl>             | Eine Zeichenfolge, die die Hauptversionsnummer des Betriebssystems darstellt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>OSMinorVersion</dt> </dl>             | Eine Zeichenfolge, die die neben Versionsnummer des Betriebssystems darstellt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>"OSPlatformID"</dt> </dl>               | Eine Zeichenfolge, die die Betriebssystem Plattform darstellt. Mögliche Werte für die **Data** -Eigenschaft sind "1", um ein nicht unterstütztes Windows-System anzugeben, und "2", um ein unterstütztes Windows-System anzugeben.<br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>OSVersion</dt> </dl>                  | Eine Zeichenfolge, die die Betriebssystemversion darstellt. Das Format dieser Zeichenfolge ist *MajorVersion*. *MinorVersion*. *BuildNumber*. Beispiel: "5.2.3790" für Windows Server 2003.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>ProcessorArchitecture</dt> </dl>      | Eine Zeichenfolge, die die Prozessorarchitektur des Betriebssystems darstellt. Eine Liste der Werte finden Sie unter dem **wprocessorarchitecture** -Member der [**System \_ Info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) -Struktur.<br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>ProductType</dt> </dl>                | Eine Zeichenfolge, die den Produkttyp darstellt. Eine Liste der Werte finden Sie unter dem **wProductType** -Member der [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) -Struktur.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"RDPAddressIPv4"</dt> </dl>             | Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der IPv4-Adressen enthält, die der RDP-Stapel des virtuellen Gast Computers zurzeit überwacht. Wenn der RDP-Stapel aktuell nicht ausgeführt wird, ist die Zeichenfolge leer. Die Liste wird automatisch aktualisiert, wenn sich eine TCP/IP-Konfigurationsänderung auf den RDP-Stapel auf dem virtuellen Gastcomputer auswirkt. Jede Adresse wird in Punkt-Dezimal Schreibweise dargestellt.<br/>                                                                                                                   |
| <dl> <dt>"RDPAddressIPv6"</dt> </dl>             | Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der IPv6-Adressen enthält, die der RDP-Stapel des virtuellen Gast Computers zurzeit überwacht. Wenn der RDP-Stapel aktuell nicht ausgeführt wird, ist die Zeichenfolge leer. Die Liste wird automatisch aktualisiert, wenn sich eine TCP/IP-Konfigurationsänderung auf den RDP-Stapel auf dem virtuellen Gastcomputer auswirkt. Jede Adresse wird in einer Doppelpunkt-hexadezimal Notation dargestellt.<br/>                                                                                                             |
| <dl> <dt>"Servicepackmajor"</dt> </dl>           | Eine Zeichenfolge, die die Hauptversionsnummer des neuesten Service Pack darstellt, das auf dem System installiert ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"Servicepackminor"</dt> </dl>           | Eine Zeichenfolge, die die neben Versionsnummer des neuesten Service Pack darstellt, das auf dem System installiert ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"Suitemask"</dt> </dl>                  | Eine Zeichenfolge, die die im System verfügbaren Produkt Suites darstellt. Diese Zeichenfolge ist eine Kombination aus allen Werten des **wSuiteMask** -Members der [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) -Struktur.<br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Quelle**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Quelle der Daten.



| Wert                                                                        | Bedeutung                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | "Hostexchangeitems" beim Pushvorgang durch den Host.<br/>                                                                                                                                                                                      |
| <dl> <dt>1</dt> </dl> | "Guestexchangeitems" beim Pushvorgang durch den virtuellen Gastcomputer.<br/>                                                                                                                                                                    |
| <dl> <dt>2</dt> </dl> | "Guestintrinsicexchangeitems", wenn der virtuelle Gastcomputer automatisch aufgefüllt wird.<br/>                                                                                                                                          |
| <dl> <dt>4</dt> </dl> | Gibt an, dass das Element nur Host ist und nicht für den virtuellen Gastcomputer freigegeben ist. Wird mit der **hostonlyitems** -Eigenschaft der [**MSVM \_ kvpexchangecomponentsettingdata**](msvm-kvpexchangecomponentsettingdata.md) -Klasse verwendet. <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM-Klasse " \_ kvpexchangedataitem** " kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ managedelta**](cim-managedelement.md)
</dt> <dt>

[**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

