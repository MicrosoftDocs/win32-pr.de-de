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
# <a name="msvm_kvpexchangedataitem-class"></a><span data-ttu-id="b1194-103">MSVM- \_ kvpexchangedataitem-Klasse</span><span class="sxs-lookup"><span data-stu-id="b1194-103">Msvm\_KvpExchangeDataItem class</span></span>

<span data-ttu-id="b1194-104">Stellt ein Schlüssel-Wert-Paar dar.</span><span class="sxs-lookup"><span data-stu-id="b1194-104">Represents a key/value pair.</span></span>

<span data-ttu-id="b1194-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1194-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1194-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1194-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b1194-107">Member</span><span class="sxs-lookup"><span data-stu-id="b1194-107">Members</span></span>

<span data-ttu-id="b1194-108">Die **MSVM- \_ kvpexchangedataitem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b1194-108">The **Msvm\_KvpExchangeDataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="b1194-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1194-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1194-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1194-110">Properties</span></span>

<span data-ttu-id="b1194-111">Die **MSVM- \_ kvpexchangedataitem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1194-111">The **Msvm\_KvpExchangeDataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1194-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b1194-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1194-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1194-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1194-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1194-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1194-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b1194-115">A short description of the object.</span></span> <span data-ttu-id="b1194-116">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1194-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1194-117">**Daten**</span><span class="sxs-lookup"><span data-stu-id="b1194-117">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1194-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1194-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1194-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1194-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1194-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="b1194-120">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="b1194-121">Der Wertteil des Schlüssel-Wert-Paars.</span><span class="sxs-lookup"><span data-stu-id="b1194-121">The value portion of the key/value pair.</span></span>

</dd> <dt>

<span data-ttu-id="b1194-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1194-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1194-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1194-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1194-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1194-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1194-125">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b1194-125">A description of the object.</span></span> <span data-ttu-id="b1194-126">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1194-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1194-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b1194-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1194-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1194-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1194-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1194-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1194-130">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b1194-130">A display name for the object.</span></span> <span data-ttu-id="b1194-131">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1194-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1194-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b1194-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1194-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1194-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1194-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1194-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1194-135">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="b1194-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b1194-136">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b1194-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b1194-137">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1194-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1194-138">**Name**</span><span class="sxs-lookup"><span data-stu-id="b1194-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1194-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b1194-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1194-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1194-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1194-141">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="b1194-141">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="b1194-142">Der Schlüsselteil des Schlüssel-Wert-Paars.</span><span class="sxs-lookup"><span data-stu-id="b1194-142">The key portion of the key/value pair.</span></span>



| <span data-ttu-id="b1194-143">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b1194-143">Key</span></span>                                                                                                     | <span data-ttu-id="b1194-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1194-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1194-145"><dt>CSDVersion</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-145"><dt>"CSDVersion"</dt></span></span> </dl>                 | <span data-ttu-id="b1194-146">Eine Zeichenfolge, die die neueste Service Pack darstellt, die auf dem Gastsystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1194-146">A string that represents the latest service pack installed on the guest system.</span></span> <span data-ttu-id="b1194-147">Beispiel: "Service Pack 2".</span><span class="sxs-lookup"><span data-stu-id="b1194-147">For example, "Service Pack 2".</span></span> <span data-ttu-id="b1194-148">Wenn keine Service Pack installiert wurde, ist diese Zeichenfolge leer.</span><span class="sxs-lookup"><span data-stu-id="b1194-148">If no service pack has been installed, this string is empty.</span></span><br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b1194-149"><dt>FullyQualifiedDomainName</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-149"><dt>"FullyQualifiedDomainName"</dt></span></span> </dl>   | <span data-ttu-id="b1194-150">Eine Zeichenfolge, die den voll qualifizierten DNS-Namen darstellt, der den lokalen Computer eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b1194-150">A string that represents the fully qualified DNS name that uniquely identifies the local computer.</span></span> <span data-ttu-id="b1194-151">Dieser Name ist eine Kombination aus dem DNS-Hostnamen und dem DNS-Domänen Namen unter Verwendung des-Formats *Hostname*. *Domänen Name*.</span><span class="sxs-lookup"><span data-stu-id="b1194-151">This name is a combination of the DNS host name and the DNS domain name, using the format *HostName*.*DomainName*.</span></span> <span data-ttu-id="b1194-152">Wenn der lokale Computer ein Knoten in einem Cluster ist, ist dieser Wert der voll qualifizierte DNS-Name des virtuellen Cluster Servers.</span><span class="sxs-lookup"><span data-stu-id="b1194-152">If the local computer is a node in a cluster, this value is the fully qualified DNS name of the cluster virtual server.</span></span> <span data-ttu-id="b1194-153">Dieser Wert entspricht dem Namen, der von der [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) -Funktion zurückgegeben wird, wenn der *nametype* -Parameter "computernamednsfullyqualified" ist.</span><span class="sxs-lookup"><span data-stu-id="b1194-153">This value matches the name returned by the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function when the *NameType* parameter is "ComputerNameDnsFullyQualified".</span></span><br/> |
| <dl> <span data-ttu-id="b1194-154"><dt>"Integrationservicesversion"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-154"><dt>"IntegrationServicesVersion"</dt></span></span> </dl> | <span data-ttu-id="b1194-155">Eine Zeichenfolge, die die Version der Integration Services darstellt, die derzeit auf dem virtuellen Gastcomputer installiert ist (z. b. "6.1.7000.0").</span><span class="sxs-lookup"><span data-stu-id="b1194-155">A string representing the version of the Integration Services currently installed in the guest virtual machine (for example, "6.1.7000.0").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b1194-156"><dt>"NetworkAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-156"><dt>"NetworkAddressIPv4"</dt></span></span> </dl>         | <span data-ttu-id="b1194-157">Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der IPv4-Adressen enthält, die zurzeit dem virtuellen Gastcomputer zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b1194-157">A string that contains a semicolon-delimited list of the IPv4 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="b1194-158">Die Liste wird automatisch aktualisiert, sobald eine TCP/IP-Konfigurationsänderung auf dem virtuellen Gastcomputer auftritt.</span><span class="sxs-lookup"><span data-stu-id="b1194-158">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="b1194-159">Jede Adresse wird in Punkt-Dezimal Schreibweise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-159">Each address is represented in dot-decimal notation.</span></span> <br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="b1194-160"><dt>"NetworkAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-160"><dt>"NetworkAddressIPv6"</dt></span></span> </dl>         | <span data-ttu-id="b1194-161">Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der IPv6-Adressen enthält, die derzeit dem virtuellen Gastcomputer zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b1194-161">A string that contains a semicolon-delimited list of the IPv6 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="b1194-162">Die Liste wird automatisch aktualisiert, sobald eine TCP/IP-Konfigurationsänderung auf dem virtuellen Gastcomputer auftritt.</span><span class="sxs-lookup"><span data-stu-id="b1194-162">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="b1194-163">Jede Adresse wird in einer Doppelpunkt-hexadezimal Notation dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-163">Each address is represented in colon-hexadecimal notation.</span></span> <span data-ttu-id="b1194-164">Es ist nicht garantiert, dass die IPv4-und IPv6-Listen immer synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b1194-164">The IPv4 and IPv6 lists are not guaranteed to be in sync at all times.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="b1194-165"><dt>"Osbuildnumber"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-165"><dt>"OSBuildNumber"</dt></span></span> </dl>              | <span data-ttu-id="b1194-166">Eine Zeichenfolge, die die Buildnummer des Betriebssystems darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-166">A string that represents the build number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="b1194-167"><dt>"Oseditionid"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-167"><dt>"OSEditionId"</dt></span></span> </dl>                | <span data-ttu-id="b1194-168">Eine Zeichenfolge, die die Edition (SKU) des Gast Betriebssystems des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-168">A string representing the edition (SKU) of the guest virtual machine operating system.</span></span> <span data-ttu-id="b1194-169">Eine Liste möglicher Werte finden Sie unter der [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b1194-169">For a list of possible values, see the [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="b1194-170"><dt>OSName</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-170"><dt>"OSName"</dt></span></span> </dl>                     | <span data-ttu-id="b1194-171">Eine Zeichenfolge, die den Namen des Betriebssystems darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-171">A string that represents the name of the operating system.</span></span> <span data-ttu-id="b1194-172">Dieser Wert stammt aus dem folgenden Registrierungs Eintrag: **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**</span><span class="sxs-lookup"><span data-stu-id="b1194-172">This value comes from the following registry entry: **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ProductName**</span></span><br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="b1194-173"><dt>OSMajorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-173"><dt>"OSMajorVersion"</dt></span></span> </dl>             | <span data-ttu-id="b1194-174">Eine Zeichenfolge, die die Hauptversionsnummer des Betriebssystems darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-174">A string that represents the major version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="b1194-175"><dt>OSMinorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-175"><dt>"OSMinorVersion"</dt></span></span> </dl>             | <span data-ttu-id="b1194-176">Eine Zeichenfolge, die die neben Versionsnummer des Betriebssystems darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-176">A string that represents the minor version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="b1194-177"><dt>"OSPlatformID"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-177"><dt>"OSPlatformId"</dt></span></span> </dl>               | <span data-ttu-id="b1194-178">Eine Zeichenfolge, die die Betriebssystem Plattform darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-178">A string that represents the operating system platform.</span></span> <span data-ttu-id="b1194-179">Mögliche Werte für die **Data** -Eigenschaft sind "1", um ein nicht unterstütztes Windows-System anzugeben, und "2", um ein unterstütztes Windows-System anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b1194-179">The possible values of the **Data** property are "1" to indicate an unsupported Windows system and "2" to indicate a supported Windows system.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="b1194-180"><dt>OSVersion</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-180"><dt>"OSVersion"</dt></span></span> </dl>                  | <span data-ttu-id="b1194-181">Eine Zeichenfolge, die die Betriebssystemversion darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-181">A string that represents the operating system version.</span></span> <span data-ttu-id="b1194-182">Das Format dieser Zeichenfolge ist *MajorVersion*. *MinorVersion*. *BuildNumber*.</span><span class="sxs-lookup"><span data-stu-id="b1194-182">The format of this string is *MajorVersion*.*MinorVersion*.*BuildNumber*.</span></span> <span data-ttu-id="b1194-183">Beispiel: "5.2.3790" für Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b1194-183">For example, "5.2.3790" for Windows Server 2003.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="b1194-184"><dt>ProcessorArchitecture</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-184"><dt>"ProcessorArchitecture"</dt></span></span> </dl>      | <span data-ttu-id="b1194-185">Eine Zeichenfolge, die die Prozessorarchitektur des Betriebssystems darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-185">A string that represents the processor architecture of the operating system.</span></span> <span data-ttu-id="b1194-186">Eine Liste der Werte finden Sie unter dem **wprocessorarchitecture** -Member der [**System \_ Info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b1194-186">For a list of values, see the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="b1194-187"><dt>ProductType</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-187"><dt>"ProductType"</dt></span></span> </dl>                | <span data-ttu-id="b1194-188">Eine Zeichenfolge, die den Produkttyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-188">A string that represents the product type.</span></span> <span data-ttu-id="b1194-189">Eine Liste der Werte finden Sie unter dem **wProductType** -Member der [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b1194-189">For a list of values, see the **wProductType** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="b1194-190"><dt>"RDPAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-190"><dt>"RDPAddressIPv4"</dt></span></span> </dl>             | <span data-ttu-id="b1194-191">Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der IPv4-Adressen enthält, die der RDP-Stapel des virtuellen Gast Computers zurzeit überwacht.</span><span class="sxs-lookup"><span data-stu-id="b1194-191">A string that contains a semicolon-delimited list of the IPv4 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="b1194-192">Wenn der RDP-Stapel aktuell nicht ausgeführt wird, ist die Zeichenfolge leer.</span><span class="sxs-lookup"><span data-stu-id="b1194-192">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="b1194-193">Die Liste wird automatisch aktualisiert, wenn sich eine TCP/IP-Konfigurationsänderung auf den RDP-Stapel auf dem virtuellen Gastcomputer auswirkt.</span><span class="sxs-lookup"><span data-stu-id="b1194-193">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="b1194-194">Jede Adresse wird in Punkt-Dezimal Schreibweise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-194">Each address is represented in dot-decimal notation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="b1194-195"><dt>"RDPAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-195"><dt>"RDPAddressIPv6"</dt></span></span> </dl>             | <span data-ttu-id="b1194-196">Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der IPv6-Adressen enthält, die der RDP-Stapel des virtuellen Gast Computers zurzeit überwacht.</span><span class="sxs-lookup"><span data-stu-id="b1194-196">A string that contains a semicolon-delimited list of the IPv6 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="b1194-197">Wenn der RDP-Stapel aktuell nicht ausgeführt wird, ist die Zeichenfolge leer.</span><span class="sxs-lookup"><span data-stu-id="b1194-197">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="b1194-198">Die Liste wird automatisch aktualisiert, wenn sich eine TCP/IP-Konfigurationsänderung auf den RDP-Stapel auf dem virtuellen Gastcomputer auswirkt.</span><span class="sxs-lookup"><span data-stu-id="b1194-198">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="b1194-199">Jede Adresse wird in einer Doppelpunkt-hexadezimal Notation dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-199">Each address is represented in colon-hexadecimal notation.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="b1194-200"><dt>"Servicepackmajor"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-200"><dt>"ServicePackMajor"</dt></span></span> </dl>           | <span data-ttu-id="b1194-201">Eine Zeichenfolge, die die Hauptversionsnummer des neuesten Service Pack darstellt, das auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1194-201">A string that represents the major version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="b1194-202"><dt>"Servicepackminor"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-202"><dt>"ServicePackMinor"</dt></span></span> </dl>           | <span data-ttu-id="b1194-203">Eine Zeichenfolge, die die neben Versionsnummer des neuesten Service Pack darstellt, das auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1194-203">A string that represents the minor version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="b1194-204"><dt>"Suitemask"</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-204"><dt>"SuiteMask"</dt></span></span> </dl>                  | <span data-ttu-id="b1194-205">Eine Zeichenfolge, die die im System verfügbaren Produkt Suites darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1194-205">A string that represents the product suites available on the system.</span></span> <span data-ttu-id="b1194-206">Diese Zeichenfolge ist eine Kombination aus allen Werten des **wSuiteMask** -Members der [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b1194-206">This string is a combination of any of the values of the **wSuiteMask** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="b1194-207">**Quelle**</span><span class="sxs-lookup"><span data-stu-id="b1194-207">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1194-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1194-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1194-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1194-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1194-210">Die Quelle der Daten.</span><span class="sxs-lookup"><span data-stu-id="b1194-210">The source of the data.</span></span>



| <span data-ttu-id="b1194-211">Wert</span><span class="sxs-lookup"><span data-stu-id="b1194-211">Value</span></span>                                                                        | <span data-ttu-id="b1194-212">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b1194-212">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1194-213"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-213"><dt>0</dt></span></span> </dl> | <span data-ttu-id="b1194-214">"Hostexchangeitems" beim Pushvorgang durch den Host.</span><span class="sxs-lookup"><span data-stu-id="b1194-214">"HostExchangeItems" when pushed by the host.</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="b1194-215"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-215"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b1194-216">"Guestexchangeitems" beim Pushvorgang durch den virtuellen Gastcomputer.</span><span class="sxs-lookup"><span data-stu-id="b1194-216">"GuestExchangeItems" when pushed by the guest virtual machine.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="b1194-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b1194-218">"Guestintrinsicexchangeitems", wenn der virtuelle Gastcomputer automatisch aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="b1194-218">"GuestIntrinsicExchangeItems" when automatically populated by the guest virtual machine.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="b1194-219"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-219"><dt>4</dt></span></span> </dl> | <span data-ttu-id="b1194-220">Gibt an, dass das Element nur Host ist und nicht für den virtuellen Gastcomputer freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b1194-220">Indicates that the item is host-only and not shared with the guest virtual machine.</span></span> <span data-ttu-id="b1194-221">Wird mit der **hostonlyitems** -Eigenschaft der [**MSVM \_ kvpexchangecomponentsettingdata**](msvm-kvpexchangecomponentsettingdata.md) -Klasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1194-221">Used with the **HostOnlyItems** property of the [**Msvm\_KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) class.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1194-222">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1194-222">Remarks</span></span>

<span data-ttu-id="b1194-223">Der Zugriff auf die **MSVM-Klasse " \_ kvpexchangedataitem** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="b1194-223">Access to the **Msvm\_KvpExchangeDataItem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b1194-224">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b1194-224">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1194-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1194-225">Requirements</span></span>



| <span data-ttu-id="b1194-226">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1194-226">Requirement</span></span> | <span data-ttu-id="b1194-227">Wert</span><span class="sxs-lookup"><span data-stu-id="b1194-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1194-228">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1194-228">Minimum supported client</span></span><br/> | <span data-ttu-id="b1194-229">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b1194-229">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b1194-230">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1194-230">Minimum supported server</span></span><br/> | <span data-ttu-id="b1194-231">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1194-231">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1194-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1194-232">Namespace</span></span><br/>                | <span data-ttu-id="b1194-233">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b1194-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b1194-234">MOF</span><span class="sxs-lookup"><span data-stu-id="b1194-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1194-235"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1194-236">DLL</span><span class="sxs-lookup"><span data-stu-id="b1194-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1194-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b1194-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b1194-238">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1194-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1194-239">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="b1194-239">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> <dt>

[<span data-ttu-id="b1194-240">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="b1194-240">**CIM\_ManagedElement**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

