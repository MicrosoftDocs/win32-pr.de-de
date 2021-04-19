---
description: Stellt den Status der Komponente der Gast Dienst Schnittstelle dar, die einen Mechanismus zum interagieren mit der virtuellen Maschine über die Verwaltungs Schnittstellen auf dem Host System bereitstellt.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Msvm_GuestServiceInterfaceComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345764"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a><span data-ttu-id="08b1e-103">MSVM \_ guestserviczuterfacecomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="08b1e-103">Msvm\_GuestServiceInterfaceComponent class</span></span>

<span data-ttu-id="08b1e-104">Stellt den Status der Komponente der Gast Dienst Schnittstelle dar, die einen Mechanismus zum interagieren mit der virtuellen Maschine über die Verwaltungs Schnittstellen auf dem Host System bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-104">Represents the state of the guest service interface component, which provides a mechanism to interact with the virtual machine from the management interfaces on the host system.</span></span> <span data-ttu-id="08b1e-105">Diese Klasse wird von der [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="08b1e-105">This class derives from the [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) class.</span></span>

<span data-ttu-id="08b1e-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="08b1e-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b1e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="08b1e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="08b1e-108">Member</span><span class="sxs-lookup"><span data-stu-id="08b1e-108">Members</span></span>

<span data-ttu-id="08b1e-109">Die **MSVM \_ guestserviceinterfacecomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="08b1e-109">The **Msvm\_GuestServiceInterfaceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="08b1e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="08b1e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="08b1e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08b1e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08b1e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="08b1e-112">Methods</span></span>

<span data-ttu-id="08b1e-113">Die **MSVM \_ guestserviczuterfacecomponent** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-113">The **Msvm\_GuestServiceInterfaceComponent** class has these methods.</span></span>



| <span data-ttu-id="08b1e-114">Methode</span><span class="sxs-lookup"><span data-stu-id="08b1e-114">Method</span></span>                                                                               | <span data-ttu-id="08b1e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08b1e-115">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08b1e-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="08b1e-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestserviceinterfacecomponent.md) | <span data-ttu-id="08b1e-117">Fordert an, dass der Status der Komponente der Gast Dienst Schnittstelle in den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="08b1e-117">Requests that the state of the guest service interface component be changed to the specified value.</span></span><br/>                           |
| [<span data-ttu-id="08b1e-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="08b1e-118">**Reset**</span></span>](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | <span data-ttu-id="08b1e-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="08b1e-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="08b1e-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="08b1e-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="08b1e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="08b1e-121">**SetPowerState**</span></span>](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | <span data-ttu-id="08b1e-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08b1e-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="08b1e-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="08b1e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="08b1e-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08b1e-124">Properties</span></span>

<span data-ttu-id="08b1e-125">Die **MSVM \_ guestserviczuterfacecomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08b1e-125">The **Msvm\_GuestServiceInterfaceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08b1e-126">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="08b1e-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b1e-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-129">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="08b1e-129">Availability and status of the device.</span></span>



| <span data-ttu-id="08b1e-130">Wert</span><span class="sxs-lookup"><span data-stu-id="08b1e-130">Value</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="08b1e-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="08b1e-131">Meaning</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="08b1e-132"><dt>**Sonstige**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-132"><dt>**Other**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="08b1e-133"><dt>**Unbekannt**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-133"><dt>**Unknown**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <span data-ttu-id="08b1e-134">Wird <dt>**ausgeführt/Full Power**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-134"><dt>**Running/Full Power**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <span data-ttu-id="08b1e-135"><dt>**Warnung**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-135"><dt>**Warning**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="08b1e-136"><dt>**In Test**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-136"><dt>**In Test**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="08b1e-137"><dt>**Nicht zutreffend**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-137"><dt>**Not Applicable**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <span data-ttu-id="08b1e-138"><dt>**Ausschalten von**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-138"><dt>**Power Off**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <span data-ttu-id="08b1e-139"><dt>**Aus Zeile**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-139"><dt>**Off Line**</dt> <dt>8 (0x8)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <span data-ttu-id="08b1e-140"><dt>**Aus Duty**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-140"><dt>**Off Duty**</dt> <dt>9 (0x9)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="08b1e-141"><dt></dt> Heruntergestuft <dt>10 (0xa)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-141"><dt>**Degraded**</dt> <dt>10 (0xA)</dt></span></span> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <span data-ttu-id="08b1e-142"><dt>**Nicht installiert**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-142"><dt>**Not Installed**</dt> <dt>11 (0xB)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <span data-ttu-id="08b1e-143"><dt>**Installationsfehler**</dt> <dt>12 (0xc)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-143"><dt>**Install Error**</dt> <dt>12 (0xC)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <span data-ttu-id="08b1e-144"><dt>**Energie speichern-unbekannt**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-144"><dt>**Power Save - Unknown**</dt> <dt>13 (0xD)</dt></span></span> </dl>                             | <span data-ttu-id="08b1e-145">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span><br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <span data-ttu-id="08b1e-146"><dt>**Energiesparmodus-niedriger Energie Modus**</dt> <dt>14 (0xe)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-146"><dt>**Power Save - Low Power Mode**</dt> <dt>14 (0xE)</dt></span></span> </dl> | <span data-ttu-id="08b1e-147">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="08b1e-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span><br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <span data-ttu-id="08b1e-148"><dt>**Energiesparmodus-Standby**</dt> <dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-148"><dt>**Power Save - Standby**</dt> <dt>15 (0xF)</dt></span></span> </dl>                             | <span data-ttu-id="08b1e-149">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-149">The device is not functioning but could be brought to full power quickly.</span></span><br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <span data-ttu-id="08b1e-150"><dt>**Power Cycle**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-150"><dt>**Power Cycle**</dt> <dt>16 (0x10)</dt></span></span> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <span data-ttu-id="08b1e-151"><dt>**Energiespar Speicher-Warnung**</dt> <dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-151"><dt>**Power Save - Warning**</dt> <dt>17 (0x11)</dt></span></span> </dl>                            | <span data-ttu-id="08b1e-152">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="08b1e-152">The device is in a warning state, though also in a power save mode.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="08b1e-153">**Caption**</span><span class="sxs-lookup"><span data-stu-id="08b1e-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-156">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="08b1e-156">Short textual description of the object.</span></span> <span data-ttu-id="08b1e-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-158">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="08b1e-158">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08b1e-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-161">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="08b1e-161">Win32 Configuration Manager error code.</span></span>



| <span data-ttu-id="08b1e-162">Wert</span><span class="sxs-lookup"><span data-stu-id="08b1e-162">Value</span></span>                                                                                | <span data-ttu-id="08b1e-163">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="08b1e-163">Meaning</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08b1e-164"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-164"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-165">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="08b1e-165">Device is working properly.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="08b1e-166"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-166"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-167">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="08b1e-167">Device is not configured correctly.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="08b1e-168"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-168"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-169">Der Treiber für dieses Gerät kann nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-169">Windows cannot load the driver for this device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="08b1e-170"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-170"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-171">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="08b1e-171">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span><br/>                             |
| <dl> <span data-ttu-id="08b1e-172"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-172"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-173">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="08b1e-173">Device is not working properly.</span></span> <span data-ttu-id="08b1e-174">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-174">One of its drivers or the registry might be corrupted.</span></span><br/>                                        |
| <dl> <span data-ttu-id="08b1e-175"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-175"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-176">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="08b1e-176">Driver for the device requires a resource that Windows cannot manage.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="08b1e-177"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-177"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-178">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="08b1e-178">Boot configuration for the device conflicts with other devices.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="08b1e-179"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-179"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-180">Kann nicht gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-180">Cannot filter.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="08b1e-181"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-181"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-182">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-182">Driver loader for the device is missing.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="08b1e-183"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-183"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="08b1e-184">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="08b1e-184">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span><br/>               |
| <dl> <span data-ttu-id="08b1e-185"><dt>10 (0xa)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-185"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="08b1e-186">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-186">Device cannot start.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="08b1e-187"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-187"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="08b1e-188">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="08b1e-188">Device failed.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="08b1e-189"><dt>12 (0xc)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-189"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="08b1e-190">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-190">Device cannot find enough free resources to use.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="08b1e-191"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-191"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="08b1e-192">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-192">Windows cannot verify the device's resources.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="08b1e-193"><dt>14 (0xe)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-193"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="08b1e-194">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="08b1e-194">Device cannot work properly until the computer is restarted.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="08b1e-195"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-195"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="08b1e-196">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="08b1e-196">Device is not working properly due to a possible re-enumeration problem.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="08b1e-197"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-197"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="08b1e-198">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-198">Windows cannot identify all of the resources that the device uses.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="08b1e-199"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-199"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="08b1e-200">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="08b1e-200">Device is requesting an unknown resource type.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="08b1e-201"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-201"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="08b1e-202">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-202">Device drivers must be reinstalled.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="08b1e-203"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-203"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="08b1e-204">Fehler bei Verwendung des VXD-Lade Moduls.</span><span class="sxs-lookup"><span data-stu-id="08b1e-204">Failure using the VxD loader.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="08b1e-205"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-205"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="08b1e-206">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-206">Registry might be corrupted.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="08b1e-207"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-207"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="08b1e-208">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="08b1e-208">System failure.</span></span> <span data-ttu-id="08b1e-209">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="08b1e-209">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="08b1e-210">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-210">Windows is removing the device.</span></span><br/> |
| <dl> <span data-ttu-id="08b1e-211"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-211"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="08b1e-212">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="08b1e-212">Device is disabled.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="08b1e-213"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-213"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="08b1e-214">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="08b1e-214">System failure.</span></span> <span data-ttu-id="08b1e-215">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="08b1e-215">If changing the device driver is ineffective, see the hardware documentation.</span></span><br/>                                 |
| <dl> <span data-ttu-id="08b1e-216"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-216"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="08b1e-217">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="08b1e-217">Device is not present, not working properly, or does not have all of its drivers installed.</span></span><br/>                                   |
| <dl> <span data-ttu-id="08b1e-218"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-218"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="08b1e-219">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="08b1e-219">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="08b1e-220"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-220"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="08b1e-221">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="08b1e-221">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="08b1e-222"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-222"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="08b1e-223">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="08b1e-223">Device does not have valid log configuration.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="08b1e-224"><dt>28 (0x1C)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-224"><dt>28 (0x1C)</dt></span></span> </dl> | <span data-ttu-id="08b1e-225">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="08b1e-225">Device drivers are not installed.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="08b1e-226"><dt>29 (0x1D)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-226"><dt>29 (0x1D)</dt></span></span> </dl> | <span data-ttu-id="08b1e-227">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-227">Device is disabled; the device firmware did not provide the required resources.</span></span><br/>                                               |
| <dl> <span data-ttu-id="08b1e-228"><dt>30 (0x1E)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-228"><dt>30 (0x1E)</dt></span></span> </dl> | <span data-ttu-id="08b1e-229">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08b1e-229">Device is using an IRQ resource that another device is using.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="08b1e-230"><dt>31 (0x1F)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-230"><dt>31 (0x1F)</dt></span></span> </dl> | <span data-ttu-id="08b1e-231">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-231">Device is not working properly; Windows cannot load the required device drivers.</span></span><br/>                                              |



 

</dd> <dt>

<span data-ttu-id="08b1e-232">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="08b1e-232">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-233">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="08b1e-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-235">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="08b1e-235">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-236">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="08b1e-236">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-239">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08b1e-239">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="08b1e-240">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-240">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-241">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="08b1e-241">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-244">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="08b1e-244">Textual description of the object.</span></span> <span data-ttu-id="08b1e-245">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-246">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="08b1e-246">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-249">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="08b1e-249">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-250">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="08b1e-250">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-251">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="08b1e-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-253">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="08b1e-253">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-254">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="08b1e-254">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-257">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="08b1e-257">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-258">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="08b1e-258">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-259">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="08b1e-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-261">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="08b1e-261">Date and time the object was installed.</span></span> <span data-ttu-id="08b1e-262">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="08b1e-262">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="08b1e-263">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-264">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="08b1e-264">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-265">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08b1e-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-267">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="08b1e-267">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-268">**Name**</span><span class="sxs-lookup"><span data-stu-id="08b1e-268">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-269">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-271">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="08b1e-271">Label by which the object is known.</span></span> <span data-ttu-id="08b1e-272">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-272">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="08b1e-273">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-274">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="08b1e-274">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-275">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-277">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="08b1e-277">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="08b1e-278">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="08b1e-278">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-279">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="08b1e-279">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-280">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="08b1e-280">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-282">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="08b1e-282">Array of the specific power-related capabilities of a logical device.</span></span> <span data-ttu-id="08b1e-283">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-283">This property is inherited from **CIM\_LogicalDevice**.</span></span>



| <span data-ttu-id="08b1e-284">Wert</span><span class="sxs-lookup"><span data-stu-id="08b1e-284">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="08b1e-285">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="08b1e-285">Meaning</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="08b1e-286"><dt>**Unbekannt**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-286"><dt>**Unknown**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="08b1e-287"><dt>**Nicht unterstützt**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-287"><dt>**Not Supported**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="08b1e-288"><dt>**Deaktiviert**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-288"><dt>**Disabled**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="08b1e-289"><dt>**Aktiviert**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-289"><dt>**Enabled**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                                                                                                                     | <span data-ttu-id="08b1e-290">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08b1e-290">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span><br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <span data-ttu-id="08b1e-291">Der <dt>**Energiesparmodus wurde automatisch eingegeben**</dt> <dt>4 (0x4)</dt> .</span><span class="sxs-lookup"><span data-stu-id="08b1e-291"><dt>**Power Saving Modes Entered Automatically**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="08b1e-292">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="08b1e-292">The device can change its power state based on usage or other criteria.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <span data-ttu-id="08b1e-293"><dt>**Energiezustand feststellbar**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-293"><dt>**Power State Settable**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                 | <span data-ttu-id="08b1e-294">Die [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-294">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method is supported.</span></span> <span data-ttu-id="08b1e-295">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-295">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="08b1e-296">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="08b1e-296">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span><br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <span data-ttu-id="08b1e-297"><dt>**Unterstützung für Power Cycling**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-297"><dt>**Power Cycling Supported**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                                     | <span data-ttu-id="08b1e-298">Die [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="08b1e-298">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span><br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <span data-ttu-id="08b1e-299">Zeit <dt>**gesteuerte Stromversorgung unterstützt**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-299"><dt>**Timed Power On Supported**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                 | <span data-ttu-id="08b1e-300">Die [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) -Methode kann aufgerufen werden, wenn der *PowerState*-Parameter auf 5 festgelegt ist ("Power Cycle") und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="08b1e-300">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and *Time* set to a specific date and time, or interval, for power-on.</span></span><br/>                                                                                       |



 

</dd> <dt>

<span data-ttu-id="08b1e-301">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="08b1e-301">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-302">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="08b1e-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-304">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="08b1e-304">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="08b1e-305">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="08b1e-305">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="08b1e-306">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-306">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="08b1e-307">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="08b1e-307">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-308">**Status**</span><span class="sxs-lookup"><span data-stu-id="08b1e-308">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-311">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="08b1e-311">Current status of the object.</span></span> <span data-ttu-id="08b1e-312">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="08b1e-313">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="08b1e-313">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="08b1e-314">**Okay**</span><span class="sxs-lookup"><span data-stu-id="08b1e-314">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="08b1e-315">**Zeit**</span><span class="sxs-lookup"><span data-stu-id="08b1e-315">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="08b1e-316">**Zerstört**</span><span class="sxs-lookup"><span data-stu-id="08b1e-316">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="08b1e-317">**Unbekannter**</span><span class="sxs-lookup"><span data-stu-id="08b1e-317">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="08b1e-318">**"Pred Fail"**</span><span class="sxs-lookup"><span data-stu-id="08b1e-318">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="08b1e-319">**Fahren**</span><span class="sxs-lookup"><span data-stu-id="08b1e-319">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="08b1e-320">**Hindern**</span><span class="sxs-lookup"><span data-stu-id="08b1e-320">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="08b1e-321">**Leistungs**</span><span class="sxs-lookup"><span data-stu-id="08b1e-321">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="08b1e-322">**Gestresst**</span><span class="sxs-lookup"><span data-stu-id="08b1e-322">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="08b1e-323">**"Nicht wiederherstellen"**</span><span class="sxs-lookup"><span data-stu-id="08b1e-323">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="08b1e-324">**"Kein Kontakt"**</span><span class="sxs-lookup"><span data-stu-id="08b1e-324">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="08b1e-325">**"Verlorene comm"**</span><span class="sxs-lookup"><span data-stu-id="08b1e-325">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08b1e-326">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="08b1e-326">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-327">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b1e-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-329">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="08b1e-329">State of the logical device.</span></span> <span data-ttu-id="08b1e-330">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08b1e-330">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span> <span data-ttu-id="08b1e-331">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08b1e-331">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

<dl> <dt>

<span data-ttu-id="08b1e-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="08b1e-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="08b1e-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2 (0x2))</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="08b1e-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3 (0x3))</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="08b1e-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (4 (0x4))</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="08b1e-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5 (0x5))</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08b1e-337">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="08b1e-337">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-338">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-340">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="08b1e-340">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-341">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="08b1e-341">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b1e-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08b1e-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b1e-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08b1e-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b1e-344">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="08b1e-344">Scoping system's name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08b1e-345">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08b1e-345">Requirements</span></span>



| <span data-ttu-id="08b1e-346">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08b1e-346">Requirement</span></span> | <span data-ttu-id="08b1e-347">Wert</span><span class="sxs-lookup"><span data-stu-id="08b1e-347">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08b1e-348">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08b1e-348">Minimum supported client</span></span><br/> | <span data-ttu-id="08b1e-349">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="08b1e-349">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="08b1e-350">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08b1e-350">Minimum supported server</span></span><br/> | <span data-ttu-id="08b1e-351">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08b1e-351">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="08b1e-352">Namespace</span><span class="sxs-lookup"><span data-stu-id="08b1e-352">Namespace</span></span><br/>                | <span data-ttu-id="08b1e-353">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="08b1e-353">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="08b1e-354">MOF</span><span class="sxs-lookup"><span data-stu-id="08b1e-354">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08b1e-355"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-355"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08b1e-356">DLL</span><span class="sxs-lookup"><span data-stu-id="08b1e-356">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08b1e-357"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-357"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08b1e-358">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08b1e-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b1e-359">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="08b1e-359">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="08b1e-360">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="08b1e-360">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

