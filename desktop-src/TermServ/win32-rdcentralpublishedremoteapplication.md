---
title: Win32_RDCentralPublishedRemoteApplication-Klasse
description: Beschreibt eine auf einem anderen Computer veröffentlichte Anwendung für die Remote Verwendung durch Terminal Dienste.
ms.assetid: 8605bd1e-e825-4fd9-b14f-9d3bdac489f1
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedRemoteApplication-Klasse Remotedesktopdienste
- Win32_RDCentralPublishedRemoteApplication Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteApplication
- Win32_RDCentralPublishedRemoteApplication.Caption
- Win32_RDCentralPublishedRemoteApplication.Description
- Win32_RDCentralPublishedRemoteApplication.InstallDate
- Win32_RDCentralPublishedRemoteApplication.Name
- Win32_RDCentralPublishedRemoteApplication.Status
- Win32_RDCentralPublishedRemoteApplication.PublishingFarm
- Win32_RDCentralPublishedRemoteApplication.Alias
- Win32_RDCentralPublishedRemoteApplication.SecurityDescriptor
- Win32_RDCentralPublishedRemoteApplication.Path
- Win32_RDCentralPublishedRemoteApplication.VPath
- Win32_RDCentralPublishedRemoteApplication.IconContents
- Win32_RDCentralPublishedRemoteApplication.CommandLineSetting
- Win32_RDCentralPublishedRemoteApplication.RequiredCommandLine
- Win32_RDCentralPublishedRemoteApplication.ShowInPortal
- Win32_RDCentralPublishedRemoteApplication.AppID
- Win32_RDCentralPublishedRemoteApplication.RDPFileContents
- Win32_RDCentralPublishedRemoteApplication.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd837f62d8d0787d992e8eed7316ed1ef3f199ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949742"
---
# <a name="win32_rdcentralpublishedremoteapplication-class"></a><span data-ttu-id="c8ef0-105">Win32 \_ rdcentralpublishedremoteapplication-Klasse</span><span class="sxs-lookup"><span data-stu-id="c8ef0-105">Win32\_RDCentralPublishedRemoteApplication class</span></span>

<span data-ttu-id="c8ef0-106">Beschreibt eine auf einem anderen Computer veröffentlichte Anwendung für die Remote Verwendung durch Terminal Dienste.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-106">Describes an application published on another computer, for remote use through Terminal Services.</span></span>

<span data-ttu-id="c8ef0-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ef0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8ef0-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  string   VPath;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   AppID;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="c8ef0-109">Member</span><span class="sxs-lookup"><span data-stu-id="c8ef0-109">Members</span></span>

<span data-ttu-id="c8ef0-110">Die **Win32 \_ rdcentralpublishedremoteapplication** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c8ef0-110">The **Win32\_RDCentralPublishedRemoteApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="c8ef0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8ef0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8ef0-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8ef0-112">Properties</span></span>

<span data-ttu-id="c8ef0-113">Die **Win32 \_ rdcentralpublishedremoteapplication** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-113">The **Win32\_RDCentralPublishedRemoteApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8ef0-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-117">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-118">Alias der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-118">Alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-119">**AppID**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-119">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-122">AppID wird zum Fixieren auf den Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-122">AppID is used for pinning on the clients.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8ef0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-126">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-127">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-127">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c8ef0-128">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-129">**Commandlinesesetting**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-129">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-132">Gibt an, ob für diese Anwendung Befehlszeilenargumente erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-132">Whether command-line arguments are required for this application.</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="c8ef0-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**Donotallow** (0)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c8ef0-134">Nicht zulassen</span><span class="sxs-lookup"><span data-stu-id="c8ef0-134">Do not allow</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="c8ef0-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Zulassen** (1)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="c8ef0-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Erforderlich** (2)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8ef0-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8ef0-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-140">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-140">Description of the object.</span></span>

<span data-ttu-id="c8ef0-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-142">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-142">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-143">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c8ef0-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-145">Liste der Ordner, in denen diese Ressource angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-145">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-146">**Iconcontent**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-146">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-147">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="c8ef0-147">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-149">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-150">Inhalt des Symbols, das der Anwendung entspricht.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-150">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-152">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8ef0-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-154">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="c8ef0-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-155">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-155">The date the object was installed.</span></span> <span data-ttu-id="c8ef0-156">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-156">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c8ef0-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8ef0-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-161">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-161">The name of the object.</span></span>

<span data-ttu-id="c8ef0-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-163">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-163">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-166">Der Pfad zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-166">Path to the application</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-167">**Publishingfarm**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-167">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-170">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-171">Alias der Farm, die die Anwendung veröffentlicht hat.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-171">Alias of the farm that published the Application</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-172">**Rdpfilecontents**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-172">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8ef0-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-175">Inhalt der RDP-Datei, die der Anwendung entspricht.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-175">Contents of the RDP file corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-176">**"Requirements dcommandline"**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-176">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-179">Für diese Anwendung sind Befehlszeilenargumente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-179">Command-line arguments required for this application.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-180">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-180">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-182">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-183">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-183">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-184">Sicherheits Beschreibung, die den Zugriff auf die Anwendung im SDDL-Format steuert.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-184">Security Descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="c8ef0-185">Eine leere Zeichenfolge impliziert den gesamten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-185">Empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-186">**Showinportal**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-186">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-187">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c8ef0-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-188">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-189">**true** , wenn diese Anwendung in der TS-Webzugriff angezeigt werden soll. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-189">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef0-190">**Status**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8ef0-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-193">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-194">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-194">Current status of the object.</span></span> <span data-ttu-id="c8ef0-195">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-195">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c8ef0-196">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="c8ef0-196">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c8ef0-197">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="c8ef0-197">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c8ef0-198">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-198">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c8ef0-199">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-199">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c8ef0-200">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c8ef0-201">("OK")</span><span class="sxs-lookup"><span data-stu-id="c8ef0-201">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8ef0-202">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c8ef0-202">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8ef0-203">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c8ef0-203">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8ef0-204">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c8ef0-204">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8ef0-205">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c8ef0-205">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8ef0-206">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c8ef0-206">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8ef0-207">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="c8ef0-207">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8ef0-208">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c8ef0-208">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8ef0-209">**Vpath**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-209">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8ef0-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8ef0-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8ef0-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c8ef0-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8ef0-212">Der virtuelle Pfad zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8ef0-212">Virtual Path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8ef0-213">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8ef0-213">Requirements</span></span>



| <span data-ttu-id="c8ef0-214">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8ef0-214">Requirement</span></span> | <span data-ttu-id="c8ef0-215">Wert</span><span class="sxs-lookup"><span data-stu-id="c8ef0-215">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ef0-216">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-216">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ef0-217">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c8ef0-217">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c8ef0-218">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8ef0-218">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ef0-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8ef0-219">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="c8ef0-220">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8ef0-220">Namespace</span></span><br/>                | <span data-ttu-id="c8ef0-221">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c8ef0-221">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c8ef0-222">MOF</span><span class="sxs-lookup"><span data-stu-id="c8ef0-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8ef0-223"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c8ef0-223"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="c8ef0-224">DLL</span><span class="sxs-lookup"><span data-stu-id="c8ef0-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8ef0-225"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8ef0-225"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

