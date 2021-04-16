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
# <a name="msvm_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="e9c78-103">MSVM \_ virtualsystemmanagementfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="e9c78-103">Msvm\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="e9c78-104">Beschreibt die Funktionen des zugeordneten [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md).</span><span class="sxs-lookup"><span data-stu-id="e9c78-104">Describes the capabilities of the associated [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md).</span></span>

<span data-ttu-id="e9c78-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e9c78-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c78-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9c78-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="e9c78-107">Member</span><span class="sxs-lookup"><span data-stu-id="e9c78-107">Members</span></span>

<span data-ttu-id="e9c78-108">Die **MSVM \_ virtualsystemmanagementfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e9c78-108">The **Msvm\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="e9c78-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9c78-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9c78-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9c78-110">Properties</span></span>

<span data-ttu-id="e9c78-111">Die **MSVM \_ virtualsystemmanagementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e9c78-111">The **Msvm\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9c78-112">**Asynchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="e9c78-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-113">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e9c78-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ virtualsystemmanagementfunktionalitäten. asynchronousmethodssupported")</span><span class="sxs-lookup"><span data-stu-id="e9c78-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-116">Gibt die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Methoden an, die asynchron von der-Implementierung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e9c78-116">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e9c78-117">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e9c78-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="e9c78-118">**[**Validateplannedsystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="e9c78-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="e9c78-119">**[**Importsystemdefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="e9c78-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="e9c78-120">**[**Importsnapshotdefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="e9c78-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="e9c78-121">**[**Realizeplannedsystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="e9c78-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="e9c78-122">**[**Exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="e9c78-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="e9c78-123">**[**Addfeaturesettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="e9c78-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="e9c78-124">**[**Modifyfeaturesettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="e9c78-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="e9c78-125">**[**Removefeaturesettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="e9c78-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="e9c78-126">**[**Getvirtualsystemthumbnailimage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="e9c78-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="e9c78-127">**[**Modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="e9c78-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="e9c78-128">**[**Getsummaryinformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="e9c78-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="e9c78-129">**[**Addkvpitems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="e9c78-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="e9c78-130">**[**Modifykvpitems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="e9c78-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="e9c78-131">**[**Removekvpitems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="e9c78-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="e9c78-132">**[**Formaterror**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="e9c78-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="e9c78-133">**Requeststatechangesupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="e9c78-133">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="e9c78-134">**Startservicesupportiert** (32790)</span><span class="sxs-lookup"><span data-stu-id="e9c78-134">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="e9c78-135">**Stopservicesupportiert** (32791)</span><span class="sxs-lookup"><span data-stu-id="e9c78-135">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="e9c78-136">**[**Modifydiskmergesettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="e9c78-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="e9c78-137">**[**Generatewwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="e9c78-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="e9c78-138">**[**Addspbrechannelchap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="e9c78-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="e9c78-139">**[**Removefbrechannelchap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="e9c78-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="e9c78-140">**[**Setguestnetworkadapterconfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="e9c78-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="e9c78-141">**[**Getsizeofsystemfiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="e9c78-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="e9c78-142">**[**Getcurrentwwpnfromgenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="e9c78-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e9c78-143">**Anbieter reserviert** (32799.65535)</span><span class="sxs-lookup"><span data-stu-id="e9c78-143">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9c78-144">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e9c78-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e9c78-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-147">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e9c78-147">A short description of the object.</span></span> <span data-ttu-id="e9c78-148">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e9c78-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9c78-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e9c78-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e9c78-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-152">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e9c78-152">A description of the object.</span></span> <span data-ttu-id="e9c78-153">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e9c78-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9c78-154">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e9c78-154">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e9c78-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-157">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e9c78-157">A display name for the object.</span></span> <span data-ttu-id="e9c78-158">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e9c78-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9c78-159">**Elementnameeditsupported**</span><span class="sxs-lookup"><span data-stu-id="e9c78-159">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-160">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e9c78-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-162">Gibt an, ob die **ElementName** -Eigenschaft geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9c78-162">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="e9c78-163">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="e9c78-163">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="e9c78-164">**Elementnamemask**</span><span class="sxs-lookup"><span data-stu-id="e9c78-164">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e9c78-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-167">Gibt die Einschränkungen für **ElementName** an, ausgedrückt als regulärer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="e9c78-167">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="e9c78-168">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="e9c78-168">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="e9c78-169">**Unterstützt**</span><span class="sxs-lookup"><span data-stu-id="e9c78-169">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-170">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e9c78-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-172">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ virtualsystemmanagementfunktionalitäten. indicationssupported")</span><span class="sxs-lookup"><span data-stu-id="e9c78-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.IndicationsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-173">Gibt die von der-Implementierung unterstützten Hinweise an.</span><span class="sxs-lookup"><span data-stu-id="e9c78-173">Specifies the indications supported by the implementation.</span></span>

<span data-ttu-id="e9c78-174">Enumeration von Indikator Bezeichner, die jeweils einen von der-Implementierung unterstützten Hinweis identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e9c78-174">Enumeration of indication identifiers each identifying an indication that is supported by the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="e9c78-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**Virtualresourcestatus echanginditerationssupported** (2)</span><span class="sxs-lookup"><span data-stu-id="e9c78-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e9c78-176">Die-Implementierung unterstützt Benachrichtigungen über Zustandsänderungen von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Instanzen, die Ressourcen virtueller Systeme darstellen.</span><span class="sxs-lookup"><span data-stu-id="e9c78-176">The implementation supports notification of state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances representing resources of virtual systems.</span></span>

</dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="e9c78-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>" **Concretejobstatus echangein" unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="e9c78-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e9c78-178">Die-Implementierung unterstützt Benachrichtigungen über Zustandsänderungen von [**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85)) -Instanzen.</span><span class="sxs-lookup"><span data-stu-id="e9c78-178">The implementation supports notification of state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span>

</dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="e9c78-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**Virtualsystemstatus echangin-Unterstützung** (4)</span><span class="sxs-lookup"><span data-stu-id="e9c78-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e9c78-180">Die-Implementierung unterstützt Benachrichtigungen über Zustandsänderungen von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanzen, die virtuelle Systeme darstellen.</span><span class="sxs-lookup"><span data-stu-id="e9c78-180">The implementation supports notification of state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances representing virtual systems.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e9c78-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e9c78-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e9c78-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="e9c78-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9c78-183">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e9c78-183">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e9c78-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-186">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="e9c78-186">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-187">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e9c78-187">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e9c78-188">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e9c78-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9c78-189">**Maxelementnamelen**</span><span class="sxs-lookup"><span data-stu-id="e9c78-189">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-190">Datentyp: **unit16**</span><span class="sxs-lookup"><span data-stu-id="e9c78-190">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-192">Qualifizierer: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="e9c78-192">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-193">Gibt die maximal unterstützte Länge der **ElementName** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="e9c78-193">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="e9c78-194">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="e9c78-194">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="e9c78-195">**Requestedstaatunter stützt**</span><span class="sxs-lookup"><span data-stu-id="e9c78-195">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-196">Datentyp: **unit16** Array</span><span class="sxs-lookup"><span data-stu-id="e9c78-196">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-198">Gibt die möglichen Zustände an, die bei Verwendung der **requestStateChange** -Methode für das aktivierte logische Element angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="e9c78-198">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="e9c78-199">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="e9c78-199">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="e9c78-200">Wert</span><span class="sxs-lookup"><span data-stu-id="e9c78-200">Value</span></span>                                                                         | <span data-ttu-id="e9c78-201">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e9c78-201">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="e9c78-202"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-202"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="e9c78-203">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="e9c78-203">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="e9c78-204"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-204"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="e9c78-205">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="e9c78-205">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="e9c78-206"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-206"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="e9c78-207">Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="e9c78-207">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="e9c78-208"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-208"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="e9c78-209">Offline</span><span class="sxs-lookup"><span data-stu-id="e9c78-209">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="e9c78-210"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-210"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="e9c78-211">Test</span><span class="sxs-lookup"><span data-stu-id="e9c78-211">Test</span></span><br/>      |
| <dl> <span data-ttu-id="e9c78-212"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-212"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="e9c78-213">Wickeln</span><span class="sxs-lookup"><span data-stu-id="e9c78-213">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="e9c78-214"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-214"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="e9c78-215">Stilllegen</span><span class="sxs-lookup"><span data-stu-id="e9c78-215">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="e9c78-216"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-216"><dt>10</dt></span></span> </dl> | <span data-ttu-id="e9c78-217">Reboot</span><span class="sxs-lookup"><span data-stu-id="e9c78-217">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="e9c78-218"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-218"><dt>11</dt></span></span> </dl> | <span data-ttu-id="e9c78-219">Reset</span><span class="sxs-lookup"><span data-stu-id="e9c78-219">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="e9c78-220">**Synchronousmethodssupported**</span><span class="sxs-lookup"><span data-stu-id="e9c78-220">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-221">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e9c78-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-223">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ virtualsystemmanagementfunktionalitäten. synchronousmethodssupported")</span><span class="sxs-lookup"><span data-stu-id="e9c78-223">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.SynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-224">Gibt die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Methoden an, die von der-Implementierung synchron unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e9c78-224">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e9c78-225">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e9c78-225">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="e9c78-226">**[**Validateplannedsystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="e9c78-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="e9c78-227">**[**Importsystemdefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="e9c78-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="e9c78-228">**[**Importsnapshotdefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="e9c78-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="e9c78-229">**[**Realizeplannedsystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="e9c78-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="e9c78-230">**[**Exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="e9c78-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="e9c78-231">**[**Addfeaturesettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="e9c78-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="e9c78-232">**[**Modifyfeaturesettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="e9c78-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="e9c78-233">**[**Removefeaturesettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="e9c78-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="e9c78-234">**[**Getvirtualsystemthumbnailimage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="e9c78-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="e9c78-235">**[**Modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="e9c78-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="e9c78-236">**[**Getsummaryinformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="e9c78-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="e9c78-237">**[**Addkvpitems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="e9c78-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="e9c78-238">**[**Modifykvpitems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="e9c78-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="e9c78-239">**[**Removekvpitems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="e9c78-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="e9c78-240">**[**Formaterror**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="e9c78-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="e9c78-241">**Requeststatechangesupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="e9c78-241">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="e9c78-242">**Startservicesupportiert** (32790)</span><span class="sxs-lookup"><span data-stu-id="e9c78-242">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="e9c78-243">**Stopservicesupportiert** (32791)</span><span class="sxs-lookup"><span data-stu-id="e9c78-243">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="e9c78-244">**[**Modifydiskmergesettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="e9c78-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="e9c78-245">**[**Generatewwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="e9c78-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="e9c78-246">**[**Addspbrechannelchap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="e9c78-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="e9c78-247">**[**Removefbrechannelchap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="e9c78-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="e9c78-248">**[**Setguestnetworkadapterconfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="e9c78-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="e9c78-249">**[**Getsizeofsystemfiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="e9c78-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="e9c78-250">**[**Getcurrentwwpnfromgenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="e9c78-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e9c78-251">**Anbieter reserviert** (32799.65535)</span><span class="sxs-lookup"><span data-stu-id="e9c78-251">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9c78-252">**Virtualsystemtypessupported**</span><span class="sxs-lookup"><span data-stu-id="e9c78-252">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c78-253">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="e9c78-253">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9c78-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e9c78-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c78-255">Ein Array von Zeichen folgen, die jeweils einen Typ eines virtuellen Systems festlegen, das von der Implementierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c78-255">An array of strings each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="e9c78-256">Der Wert jedes Array Elements, das nicht **null** ist, muss den Zeichen folgen entsprechen, die für die Eigenschaft " [**MSVM \_ virtualsystemsettingdata. virtualsystemtype**](msvm-virtualsystemsettingdata.md) " definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e9c78-256">The value of each non-**NULL** array element must conform to the strings defined for the [**Msvm\_VirtualSystemSettingData.VirtualSystemType**](msvm-virtualsystemsettingdata.md) property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9c78-257">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9c78-257">Requirements</span></span>



| <span data-ttu-id="e9c78-258">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9c78-258">Requirement</span></span> | <span data-ttu-id="e9c78-259">Wert</span><span class="sxs-lookup"><span data-stu-id="e9c78-259">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c78-260">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9c78-260">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c78-261">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9c78-261">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e9c78-262">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9c78-262">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c78-263">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9c78-263">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9c78-264">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9c78-264">Namespace</span></span><br/>                | <span data-ttu-id="e9c78-265">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e9c78-265">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e9c78-266">MOF</span><span class="sxs-lookup"><span data-stu-id="e9c78-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9c78-267"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-267"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9c78-268">DLL</span><span class="sxs-lookup"><span data-stu-id="e9c78-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9c78-269"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9c78-269"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

