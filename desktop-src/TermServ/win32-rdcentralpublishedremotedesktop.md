---
title: Win32_RDCentralPublishedRemoteDesktop-Klasse
description: Auf einem anderen Computer veröffentlichter Desktop für die Remote Verwendung durch Terminal Dienste.
ms.assetid: 2b28a2d3-048f-446f-9ce0-eb684b393eaa
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedRemoteDesktop-Klasse Remotedesktopdienste
- Win32_RDCentralPublishedRemoteDesktop Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteDesktop
- Win32_RDCentralPublishedRemoteDesktop.Caption
- Win32_RDCentralPublishedRemoteDesktop.Description
- Win32_RDCentralPublishedRemoteDesktop.InstallDate
- Win32_RDCentralPublishedRemoteDesktop.Name
- Win32_RDCentralPublishedRemoteDesktop.Status
- Win32_RDCentralPublishedRemoteDesktop.PublishingFarm
- Win32_RDCentralPublishedRemoteDesktop.Alias
- Win32_RDCentralPublishedRemoteDesktop.IconContents
- Win32_RDCentralPublishedRemoteDesktop.ShowInPortal
- Win32_RDCentralPublishedRemoteDesktop.RDPFileContents
- Win32_RDCentralPublishedRemoteDesktop.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04696331b7027b7cc65d2202c29e6ce95bb3f4b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476209"
---
# <a name="win32_rdcentralpublishedremotedesktop-class"></a><span data-ttu-id="0fe34-105">Win32 \_ rdcentralpublishedremotedesktop-Klasse</span><span class="sxs-lookup"><span data-stu-id="0fe34-105">Win32\_RDCentralPublishedRemoteDesktop class</span></span>

<span data-ttu-id="0fe34-106">Auf einem anderen Computer veröffentlichter Desktop für die Remote Verwendung durch Terminal Dienste</span><span class="sxs-lookup"><span data-stu-id="0fe34-106">Desktop published on another computer, for remote use through Terminal Services</span></span>

<span data-ttu-id="0fe34-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0fe34-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe34-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fe34-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="0fe34-109">Member</span><span class="sxs-lookup"><span data-stu-id="0fe34-109">Members</span></span>

<span data-ttu-id="0fe34-110">Die **Win32 \_ -Klasse rdcentralpublishedremotedesktop** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0fe34-110">The **Win32\_RDCentralPublishedRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="0fe34-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fe34-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fe34-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fe34-112">Properties</span></span>

<span data-ttu-id="0fe34-113">Die **Win32 \_ -Klasse rdcentralpublishedremotedesktop** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0fe34-113">The **Win32\_RDCentralPublishedRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fe34-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="0fe34-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0fe34-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0fe34-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-117">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0fe34-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-118">Alias des Desktops.</span><span class="sxs-lookup"><span data-stu-id="0fe34-118">Alias of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0fe34-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0fe34-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe34-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-122">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0fe34-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-123">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0fe34-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0fe34-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0fe34-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fe34-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0fe34-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe34-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-128">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0fe34-128">Description of the object.</span></span>

<span data-ttu-id="0fe34-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0fe34-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-130">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="0fe34-130">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-131">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0fe34-131">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0fe34-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-133">Liste der Ordner, in denen diese Ressource angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fe34-133">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-134">**Iconcontent**</span><span class="sxs-lookup"><span data-stu-id="0fe34-134">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-135">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="0fe34-135">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0fe34-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-137">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0fe34-137">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-138">Inhalt des Symbols, das der Anwendung entspricht.</span><span class="sxs-lookup"><span data-stu-id="0fe34-138">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0fe34-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-140">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0fe34-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe34-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-142">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0fe34-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-143">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0fe34-143">The date the object was installed.</span></span> <span data-ttu-id="0fe34-144">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0fe34-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0fe34-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0fe34-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="0fe34-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0fe34-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe34-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-149">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0fe34-149">The name of the object.</span></span>

<span data-ttu-id="0fe34-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0fe34-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-151">**Publishingfarm**</span><span class="sxs-lookup"><span data-stu-id="0fe34-151">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0fe34-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0fe34-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-154">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0fe34-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-155">Alias der Farm, die den Desktop veröffentlicht hat.</span><span class="sxs-lookup"><span data-stu-id="0fe34-155">Alias of the farm that published the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-156">**Rdpfilecontents**</span><span class="sxs-lookup"><span data-stu-id="0fe34-156">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0fe34-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe34-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-159">Inhalt der RDP-Datei, die dem Desktop entspricht.</span><span class="sxs-lookup"><span data-stu-id="0fe34-159">Contents of the RDP file corresponding to the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-160">**Showinportal**</span><span class="sxs-lookup"><span data-stu-id="0fe34-160">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-161">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0fe34-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-162">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0fe34-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-163">**true** , wenn diese Anwendung in der TS-Webzugriff angezeigt werden soll. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="0fe34-163">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="0fe34-164">**Status**</span><span class="sxs-lookup"><span data-stu-id="0fe34-164">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe34-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0fe34-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe34-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe34-167">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0fe34-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0fe34-168">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0fe34-168">Current status of the object.</span></span> <span data-ttu-id="0fe34-169">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0fe34-169">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0fe34-170">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="0fe34-170">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0fe34-171">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="0fe34-171">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0fe34-172">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fe34-172">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0fe34-173">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="0fe34-173">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0fe34-174">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0fe34-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0fe34-175">("OK")</span><span class="sxs-lookup"><span data-stu-id="0fe34-175">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe34-176">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="0fe34-176">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe34-177">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="0fe34-177">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe34-178">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="0fe34-178">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe34-179">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0fe34-179">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe34-180">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="0fe34-180">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe34-181">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="0fe34-181">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe34-182">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="0fe34-182">("Service")</span></span>


<span data-ttu-id="0fe34-183"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0fe34-183"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0fe34-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fe34-184">Requirements</span></span>



| <span data-ttu-id="0fe34-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fe34-185">Requirement</span></span> | <span data-ttu-id="0fe34-186">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe34-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe34-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fe34-187">Minimum supported client</span></span><br/> | <span data-ttu-id="0fe34-188">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0fe34-188">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0fe34-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fe34-189">Minimum supported server</span></span><br/> | <span data-ttu-id="0fe34-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0fe34-190">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="0fe34-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fe34-191">Namespace</span></span><br/>                | <span data-ttu-id="0fe34-192">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0fe34-192">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0fe34-193">MOF</span><span class="sxs-lookup"><span data-stu-id="0fe34-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fe34-194"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0fe34-194"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="0fe34-195">DLL</span><span class="sxs-lookup"><span data-stu-id="0fe34-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fe34-196"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fe34-196"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

