---
description: Stellt die Konfiguration eines virtuellen Fibre Channel Schalters dar.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Msvm_VirtualFcSwitchSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525217"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a><span data-ttu-id="e6113-103">MSVM \_ virtualfcswitchsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="e6113-103">Msvm\_VirtualFcSwitchSettingData class</span></span>

<span data-ttu-id="e6113-104">Stellt die Konfiguration eines virtuellen Fibre Channel Schalters dar.</span><span class="sxs-lookup"><span data-stu-id="e6113-104">Represents the configuration of a virtual Fibre Channel switch.</span></span>

<span data-ttu-id="e6113-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e6113-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6113-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6113-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a><span data-ttu-id="e6113-107">Member</span><span class="sxs-lookup"><span data-stu-id="e6113-107">Members</span></span>

<span data-ttu-id="e6113-108">Die **MSVM \_ virtualfcswitchsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e6113-108">The **Msvm\_VirtualFcSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e6113-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e6113-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6113-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e6113-110">Properties</span></span>

<span data-ttu-id="e6113-111">Die **MSVM \_ virtualfcswitchsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e6113-111">The **Msvm\_VirtualFcSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6113-112">**Automatikrecoveryaction**</span><span class="sxs-lookup"><span data-stu-id="e6113-112">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6113-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-115">Die für den virtuellen Computer auszuführende Aktion, wenn die von der virtuellen Maschine ausgeführte Software ausfällt.</span><span class="sxs-lookup"><span data-stu-id="e6113-115">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="e6113-116">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6113-116">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6113-117">**Automaticshutdownaction**</span><span class="sxs-lookup"><span data-stu-id="e6113-117">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-118">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6113-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-120">Aktion, die beim Herunterfahren des Hosts für die virtuelle Maschine ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6113-120">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="e6113-121">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6113-121">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6113-122">**Automaticstartupaction**</span><span class="sxs-lookup"><span data-stu-id="e6113-122">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-123">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6113-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-125">Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn der Host gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e6113-125">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="e6113-126">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6113-126">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6113-127">**Automaticstartupactiondelay**</span><span class="sxs-lookup"><span data-stu-id="e6113-127">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-128">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6113-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-130">Die Verzögerungszeit, bevor der virtuelle Computer automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e6113-130">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="e6113-131">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6113-131">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6113-132">**Automaticstartupactionsequencenumschlag**</span><span class="sxs-lookup"><span data-stu-id="e6113-132">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6113-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-135">Eine Zahl, die die relative Sequenz der Aktivierung virtueller Maschinen angibt, wenn das Host System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e6113-135">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="e6113-136">Eine niedrigere Zahl deutet auf eine frühere Aktivierung hin.</span><span class="sxs-lookup"><span data-stu-id="e6113-136">A lower number indicates earlier activation.</span></span> <span data-ttu-id="e6113-137">Wenn eine oder mehrere Konfigurationen denselben Wert aufweisen, ist die Sequenz implementierungsabhängig.</span><span class="sxs-lookup"><span data-stu-id="e6113-137">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="e6113-138">Der Wert 0 gibt an, dass die Sequenz implementierungsabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="e6113-138">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="e6113-139">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6113-139">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6113-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e6113-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-143">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e6113-143">A short description of the object.</span></span> <span data-ttu-id="e6113-144">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-145">**Configurationdataroot**</span><span class="sxs-lookup"><span data-stu-id="e6113-145">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-148">Der Pfad eines Verzeichnisses, in dem Informationen zur Konfiguration der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e6113-148">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="e6113-149">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-149">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-150">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="e6113-150">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-153">Der relative Pfad und der Dateiname einer Datei, in der Informationen zur Konfiguration der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e6113-153">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="e6113-154">Dieser Pfad ist relativ zur **configurationdataroot** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e6113-154">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="e6113-155">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-155">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-156">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="e6113-156">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-159">Der eindeutige Bezeichner der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e6113-159">The unique identifier of the configuration.</span></span> <span data-ttu-id="e6113-160">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-160">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-161">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="e6113-161">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-162">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6113-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-164">Das Datum und die Uhrzeit der Erstellung der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="e6113-164">The date and time at which the settings were created.</span></span> <span data-ttu-id="e6113-165">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-165">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="e6113-166">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-166">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-167">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6113-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-170">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e6113-170">A description of the object.</span></span> <span data-ttu-id="e6113-171">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e6113-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-175">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e6113-175">A display name for the object.</span></span> <span data-ttu-id="e6113-176">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-176">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e6113-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6113-180">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="e6113-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e6113-181">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e6113-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e6113-182">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-183">**Logdataroot**</span><span class="sxs-lookup"><span data-stu-id="e6113-183">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-186">Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e6113-186">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="e6113-187">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6113-187">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6113-188">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="e6113-188">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-189">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="e6113-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e6113-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-191">Vom Benutzer bereitgestellte Hinweise zum virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e6113-191">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="e6113-192">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-192">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-193">**Wiederherstellbare Datei**</span><span class="sxs-lookup"><span data-stu-id="e6113-193">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-196">Der vollständige Pfad einer Datei, in der Wiederherstellungs bezogene Informationen für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e6113-196">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="e6113-197">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6113-197">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6113-198">**Snapshotdataroot**</span><span class="sxs-lookup"><span data-stu-id="e6113-198">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-201">Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e6113-201">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="e6113-202">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-203">**Suspenddataroot**</span><span class="sxs-lookup"><span data-stu-id="e6113-203">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-206">Der Pfad eines Verzeichnisses, in dem Informationen zu den Informationen zum Aussetzen der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e6113-206">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="e6113-207">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-208">**Austauschen von Daten**</span><span class="sxs-lookup"><span data-stu-id="e6113-208">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-211">Der Pfad eines Verzeichnisses, in dem die Auslagerungs Dateien für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e6113-211">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="e6113-212">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6113-212">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6113-213">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="e6113-213">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-216">Der Name des [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Objekts, zu dem diese Einstellungsdaten gehören.</span><span class="sxs-lookup"><span data-stu-id="e6113-216">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="e6113-217">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6113-218">**Virtualsystemtype**</span><span class="sxs-lookup"><span data-stu-id="e6113-218">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6113-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6113-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6113-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6113-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6113-221">Gibt den Typ der virtuellen Maschine an, die die Einstellungsdaten darstellen.</span><span class="sxs-lookup"><span data-stu-id="e6113-221">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="e6113-222">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e6113-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6113-223">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6113-223">Requirements</span></span>



| <span data-ttu-id="e6113-224">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6113-224">Requirement</span></span> | <span data-ttu-id="e6113-225">Wert</span><span class="sxs-lookup"><span data-stu-id="e6113-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6113-226">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6113-226">Minimum supported client</span></span><br/> | <span data-ttu-id="e6113-227">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6113-227">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e6113-228">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6113-228">Minimum supported server</span></span><br/> | <span data-ttu-id="e6113-229">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6113-229">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6113-230">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6113-230">Namespace</span></span><br/>                | <span data-ttu-id="e6113-231">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e6113-231">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6113-232">MOF</span><span class="sxs-lookup"><span data-stu-id="e6113-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6113-233"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e6113-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6113-234">DLL</span><span class="sxs-lookup"><span data-stu-id="e6113-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6113-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6113-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

