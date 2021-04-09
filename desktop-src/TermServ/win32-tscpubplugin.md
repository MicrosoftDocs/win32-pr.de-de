---
title: Win32_TSCPubPlugin-Klasse
description: Stellt ein Plug-in dar, das für die Verwendung durch den RemoteApp-und Desktopverbindungsverwaltung-Dienst konfiguriert ist.
ms.assetid: 0eebdeea-4bfb-4032-a28b-870df7103473
ms.tgt_platform: multiple
keywords:
- Win32_TSCPubPlugin-Klasse Remotedesktopdienste
- Win32_TSCPubPlugin Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSCPubPlugin
- Win32_TSCPubPlugin.Caption
- Win32_TSCPubPlugin.Description
- Win32_TSCPubPlugin.InstallDate
- Win32_TSCPubPlugin.Name
- Win32_TSCPubPlugin.Status
- Win32_TSCPubPlugin.CLSID
- Win32_TSCPubPlugin.IsEnabled
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0b4fcff8cadae32d59fe45c61c506e768782d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858840"
---
# <a name="win32_tscpubplugin-class"></a><span data-ttu-id="5f1ae-105">Win32- \_ tscpubplugin-Klasse</span><span class="sxs-lookup"><span data-stu-id="5f1ae-105">Win32\_TSCPubPlugin class</span></span>

<span data-ttu-id="5f1ae-106">Stellt ein Plug-in dar, das für die Verwendung durch den RemoteApp-und Desktopverbindungsverwaltung-Dienst konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-106">Represents a plug-in that is configured to be used through the RemoteApp and Desktop Connection Management Service.</span></span>

<span data-ttu-id="5f1ae-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f1ae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f1ae-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSCPubPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CLSID;
  boolean  IsEnabled;
};
```

## <a name="members"></a><span data-ttu-id="5f1ae-109">Member</span><span class="sxs-lookup"><span data-stu-id="5f1ae-109">Members</span></span>

<span data-ttu-id="5f1ae-110">Die **Win32- \_ tscpubplugin** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5f1ae-110">The **Win32\_TSCPubPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="5f1ae-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f1ae-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f1ae-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f1ae-112">Properties</span></span>

<span data-ttu-id="5f1ae-113">Die **Win32 \_ tscpubplugin** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-113">The **Win32\_TSCPubPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f1ae-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1ae-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f1ae-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5f1ae-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5f1ae-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5f1ae-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f1ae-120">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-120">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1ae-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f1ae-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f1ae-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f1ae-124">Die CLSID des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-124">The CLSID of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ae-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1ae-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f1ae-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f1ae-128">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-128">Description of the object.</span></span>

<span data-ttu-id="5f1ae-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f1ae-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1ae-131">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f1ae-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-133">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5f1ae-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5f1ae-134">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-134">The date the object was installed.</span></span> <span data-ttu-id="5f1ae-135">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5f1ae-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f1ae-137">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-137">**IsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1ae-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5f1ae-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5f1ae-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5f1ae-140">Gibt an, ob das Plug-in aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-140">Specifies whether the plug-in is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ae-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1ae-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f1ae-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f1ae-144">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-144">The name of the object.</span></span>

<span data-ttu-id="5f1ae-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f1ae-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1ae-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f1ae-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f1ae-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f1ae-149">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5f1ae-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5f1ae-150">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-150">Current status of the object.</span></span> <span data-ttu-id="5f1ae-151">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5f1ae-152">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="5f1ae-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5f1ae-153">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="5f1ae-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5f1ae-154">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5f1ae-155">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5f1ae-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f1ae-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5f1ae-157">("OK")</span><span class="sxs-lookup"><span data-stu-id="5f1ae-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5f1ae-158">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="5f1ae-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5f1ae-159">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="5f1ae-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5f1ae-160">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="5f1ae-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5f1ae-161">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5f1ae-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5f1ae-162">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="5f1ae-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5f1ae-163">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="5f1ae-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5f1ae-164">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="5f1ae-164">("Service")</span></span>


<span data-ttu-id="5f1ae-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5f1ae-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5f1ae-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f1ae-166">Requirements</span></span>



| <span data-ttu-id="5f1ae-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f1ae-167">Requirement</span></span> | <span data-ttu-id="5f1ae-168">Wert</span><span class="sxs-lookup"><span data-stu-id="5f1ae-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1ae-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f1ae-169">Minimum supported client</span></span><br/> | <span data-ttu-id="5f1ae-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5f1ae-170">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5f1ae-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f1ae-171">Minimum supported server</span></span><br/> | <span data-ttu-id="5f1ae-172">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5f1ae-172">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="5f1ae-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f1ae-173">Namespace</span></span><br/>                | <span data-ttu-id="5f1ae-174">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5f1ae-174">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5f1ae-175">MOF</span><span class="sxs-lookup"><span data-stu-id="5f1ae-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f1ae-176"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5f1ae-176"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5f1ae-177">DLL</span><span class="sxs-lookup"><span data-stu-id="5f1ae-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f1ae-178"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f1ae-178"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

