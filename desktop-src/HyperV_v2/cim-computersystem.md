---
description: Stellt eine Auflistung dar, die Computerfunktionen bereitstellt und aus CIM \_ ManagedSystemElement-Objekten besteht.
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: CIM_ComputerSystem-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00a53d0c514113175c3c6ffb7ea40f8ef4e730d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369078"
---
# <a name="cim_computersystem-class-hyper-v-management"></a><span data-ttu-id="300da-103">CIM_ComputerSystem-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="300da-103">CIM_ComputerSystem class (Hyper-V management)</span></span>

<span data-ttu-id="300da-104">Stellt eine Auflistung dar, die Computerfunktionen bereitstellt und aus [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekten besteht.</span><span class="sxs-lookup"><span data-stu-id="300da-104">Represents a collection that provides computing capabilities and consists of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="300da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="300da-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="300da-106">Member</span><span class="sxs-lookup"><span data-stu-id="300da-106">Members</span></span>

<span data-ttu-id="300da-107">Die **CIM \_ Computersystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="300da-107">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="300da-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="300da-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="300da-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="300da-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="300da-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="300da-110">Methods</span></span>

<span data-ttu-id="300da-111">Die **CIM \_ Computersystem** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="300da-111">The **CIM\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="300da-112">Methode</span><span class="sxs-lookup"><span data-stu-id="300da-112">Method</span></span>                                                    | <span data-ttu-id="300da-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="300da-113">Description</span></span>                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="300da-114">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="300da-114">**SetPowerState**</span></span>](cim-computersystem-setpowerstate.md) | <span data-ttu-id="300da-115">Diese Methode ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="300da-115">This method is deprecated.</span></span> <span data-ttu-id="300da-116">Verwenden Sie stattdessen die **requestpowerstatechange** -Methode in der **CIM- \_ powermanagementservice** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="300da-116">Instead, use the **RequestPowerStateChange** method in the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="300da-117">**Veraltete Beschreibung:** Legt den Energiezustand des Computers fest.</span><span class="sxs-lookup"><span data-stu-id="300da-117">**Deprecated description:** Sets the power state of the computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="300da-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="300da-118">Properties</span></span>

<span data-ttu-id="300da-119">Die **CIM \_ Computersystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="300da-119">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="300da-120">**Dediziert**</span><span class="sxs-lookup"><span data-stu-id="300da-120">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-121">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="300da-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="300da-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="300da-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="300da-123">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \|MIB-II.sysServices "," FC-GS. INCITS-T11 \| Platform \| PlatformType "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Computersystem**.**Otherdedialisiedbeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="300da-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.sysServices", "FC-GS.INCITS-T11 \| Platform \| PlatformType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**OtherDedicatedDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="300da-124">Der Zweck und die Features des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="300da-124">The purpose and features of the computer system.</span></span> <span data-ttu-id="300da-125">Beispielsweise könnte ein für das Drucken dediziertes System "11" (Print) angeben.</span><span class="sxs-lookup"><span data-stu-id="300da-125">For example, a system dedicated to printing could specify "11" (Print).</span></span> <span data-ttu-id="300da-126">Ein allgemeines System mit Druckfunktionen kann auf "0" (nicht dediziert) und "11" (Drucken) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="300da-126">A general purpose system with printing capabilities can be set to "0" (Not Dedicated) and "11" (Print).</span></span>

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span data-ttu-id="300da-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Nicht dediziert** (0)</span><span class="sxs-lookup"><span data-stu-id="300da-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Not Dedicated** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="300da-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (1)</span><span class="sxs-lookup"><span data-stu-id="300da-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="300da-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (2)</span><span class="sxs-lookup"><span data-stu-id="300da-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="300da-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Speicher** (3)</span><span class="sxs-lookup"><span data-stu-id="300da-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span data-ttu-id="300da-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)</span><span class="sxs-lookup"><span data-stu-id="300da-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="300da-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span><span class="sxs-lookup"><span data-stu-id="300da-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span data-ttu-id="300da-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Layer 3-Schalter** (6)</span><span class="sxs-lookup"><span data-stu-id="300da-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Layer 3 Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span data-ttu-id="300da-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Zentrale Niederlassung** (7)</span><span class="sxs-lookup"><span data-stu-id="300da-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Central Office Switch** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span data-ttu-id="300da-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span><span class="sxs-lookup"><span data-stu-id="300da-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span data-ttu-id="300da-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Zugriffs Server** (9)</span><span class="sxs-lookup"><span data-stu-id="300da-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Access Server** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span data-ttu-id="300da-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span><span class="sxs-lookup"><span data-stu-id="300da-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="300da-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Drucken** (11)</span><span class="sxs-lookup"><span data-stu-id="300da-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Print** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span data-ttu-id="300da-139"><span id="I_O"></span><span id="i_o"></span>E **/** a (12)</span><span class="sxs-lookup"><span data-stu-id="300da-139"><span id="I_O"></span><span id="i_o"></span>**I/O** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span data-ttu-id="300da-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Webcaching** (13)</span><span class="sxs-lookup"><span data-stu-id="300da-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Web Caching** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span data-ttu-id="300da-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Verwaltung** (14)</span><span class="sxs-lookup"><span data-stu-id="300da-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Management** (14)</span></span>


</dt> <dd>

<span data-ttu-id="300da-142">Diese Instanz ist für das Hosting der System Verwaltungssoftware vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="300da-142">This instance is dedicated to hosting system management software</span></span>

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span data-ttu-id="300da-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Block Server** (15)</span><span class="sxs-lookup"><span data-stu-id="300da-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Block Server** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span data-ttu-id="300da-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**Datei Server** (16)</span><span class="sxs-lookup"><span data-stu-id="300da-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**File Server** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span data-ttu-id="300da-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Mobiles Benutzergerät** (17)</span><span class="sxs-lookup"><span data-stu-id="300da-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Mobile User Device** (17)</span></span>


</dt> <dd>

<span data-ttu-id="300da-146">Ein Beispiel für ein dediziertes Benutzergerät ist ein Mobiltelefon oder ein Barcode Scanner in einem Geschäft, das über eine Radiofrequenz kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="300da-146">An example of a dedicated user device is a mobile phone or a barcode scanner in a store that communicates via radio frequency.</span></span> <span data-ttu-id="300da-147">Diese Systeme sind in der Funktionalität und Programmierbarkeit sehr eingeschränkt und werden nicht als "universell" eingestuft.</span><span class="sxs-lookup"><span data-stu-id="300da-147">These systems are quite limited in functionality and programmability, and are not considered 'general purpose' computing platforms.</span></span> <span data-ttu-id="300da-148">Alternativ ist ein Beispiel für ein mobiles System, das "universell" (d. h. nicht dediziert) ist, ein Hand gehalteter Computer.</span><span class="sxs-lookup"><span data-stu-id="300da-148">Alternately, an example of a mobile system that is 'general purpose' (i.e., is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="300da-149">Obwohl die Programmierbarkeit eingeschränkt ist, kann neue Software heruntergeladen und ihre Funktionalität vom Benutzer erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="300da-149">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span>

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span data-ttu-id="300da-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span><span class="sxs-lookup"><span data-stu-id="300da-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span data-ttu-id="300da-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)</span><span class="sxs-lookup"><span data-stu-id="300da-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span data-ttu-id="300da-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span><span class="sxs-lookup"><span data-stu-id="300da-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span data-ttu-id="300da-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Speichervirtualisierer** (21)</span><span class="sxs-lookup"><span data-stu-id="300da-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Storage Virtualizer** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span data-ttu-id="300da-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Medienbibliothek** (22)</span><span class="sxs-lookup"><span data-stu-id="300da-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Media Library** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span data-ttu-id="300da-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**Extendernode** (23)</span><span class="sxs-lookup"><span data-stu-id="300da-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span data-ttu-id="300da-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS-Head** (24)</span><span class="sxs-lookup"><span data-stu-id="300da-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS Head** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span data-ttu-id="300da-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Eigenständiges NAS** (25)</span><span class="sxs-lookup"><span data-stu-id="300da-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Self-contained NAS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span data-ttu-id="300da-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span><span class="sxs-lookup"><span data-stu-id="300da-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span data-ttu-id="300da-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP-Telefon** (27)</span><span class="sxs-lookup"><span data-stu-id="300da-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP Phone** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span data-ttu-id="300da-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Verwaltungs Controller** (28)</span><span class="sxs-lookup"><span data-stu-id="300da-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Management Controller** (28)</span></span>


</dt> <dd>

<span data-ttu-id="300da-161">Diese Instanz stellt spezielle Hardware dar, die für die Systemverwaltung vorgesehen ist (d. h. einen Baseboard-Verwaltungs Controller (BMC) oder einen Dienst Prozessor).</span><span class="sxs-lookup"><span data-stu-id="300da-161">This instance represents specialized hardware dedicated to systems management (i.e., a Baseboard Management Controller (BMC) or service processor).</span></span>

<span data-ttu-id="300da-162">Der Verwaltungsbereich eines Verwaltungs Controllers ist in der Regel ein einzelnes verwaltetes System, in dem es enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="300da-162">The management scope of a "Management Controller" is typically a single managed system in which it is contained.</span></span>

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span data-ttu-id="300da-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Chassis-Manager** (29)</span><span class="sxs-lookup"><span data-stu-id="300da-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Chassis Manager** (29)</span></span>


</dt> <dd>

<span data-ttu-id="300da-164">Diese Instanz stellt ein System dar, das für die Verwaltung eines Blade Chassis und der darin enthaltenen Geräte vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="300da-164">This instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="300da-165">Dieser Wert wird verwendet, um einen Regal Controller darzustellen.</span><span class="sxs-lookup"><span data-stu-id="300da-165">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="300da-166">Ein "Chassis-Manager" ist ein Aggregations Punkt für die Verwaltung und kann für die Verwaltung von Bestandteilen auf untergeordneten Verwaltungs Controllern beruhen.</span><span class="sxs-lookup"><span data-stu-id="300da-166">A "Chassis Manager" is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span>

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span data-ttu-id="300da-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Host basierter RAID-Controller** (30)</span><span class="sxs-lookup"><span data-stu-id="300da-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Host-based RAID controller** (30)</span></span>


</dt> <dd>

<span data-ttu-id="300da-168">Diese Instanz stellt einen RAID-Speichercontroller dar, der in einem Host Computer enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="300da-168">This instance represents a RAID storage controller contained within a host computer.</span></span>

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span data-ttu-id="300da-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Speichergeräte Gehäuse** (31)</span><span class="sxs-lookup"><span data-stu-id="300da-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Storage Device Enclosure** (31)</span></span>


</dt> <dd>

<span data-ttu-id="300da-170">Diese Instanz stellt ein Gehäuse dar, das Speichergeräte enthält.</span><span class="sxs-lookup"><span data-stu-id="300da-170">This instance represents an enclosure that contains storage devices.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="300da-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)</span><span class="sxs-lookup"><span data-stu-id="300da-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="300da-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)</span><span class="sxs-lookup"><span data-stu-id="300da-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span data-ttu-id="300da-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Bibliothek für virtuelle Bänder** (34)</span><span class="sxs-lookup"><span data-stu-id="300da-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Virtual Tape Library** (34)</span></span>


</dt> <dd>

<span data-ttu-id="300da-174">Die Emulation einer Band Bibliothek durch ein virtuelles Bibliotheks System.</span><span class="sxs-lookup"><span data-stu-id="300da-174">The emulation of a tape library by a Virtual Library System.</span></span>

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span data-ttu-id="300da-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Virtuelles Bibliotheks System** (35)</span><span class="sxs-lookup"><span data-stu-id="300da-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Virtual Library System** (35)</span></span>


</dt> <dd>

<span data-ttu-id="300da-176">Verwendung von Datenträger Speicher zum Emulieren von Bandbibliotheken</span><span class="sxs-lookup"><span data-stu-id="300da-176">Uses disk storage to emulate tape libraries</span></span>

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span data-ttu-id="300da-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Netzwerk-PC/Thin Client** (36)</span><span class="sxs-lookup"><span data-stu-id="300da-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Network PC/Thin Client** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span data-ttu-id="300da-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC-Schalter** (37)</span><span class="sxs-lookup"><span data-stu-id="300da-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC Switch** (37)</span></span>


</dt> <dd>

<span data-ttu-id="300da-179">Dediziert zum Wechseln von Fibre Channel-Frames der Ebene 2.</span><span class="sxs-lookup"><span data-stu-id="300da-179">Dedicated to switching layer 2 fibre channel frames.</span></span>

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span data-ttu-id="300da-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet-Switch** (38)</span><span class="sxs-lookup"><span data-stu-id="300da-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet Switch** (38)</span></span>


</dt> <dd>

<span data-ttu-id="300da-181">Dedizierter zum Wechseln von Layer 2-Ethernet-Frames</span><span class="sxs-lookup"><span data-stu-id="300da-181">Dedicated to switching layer 2 ethernet frames</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="300da-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="300da-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="300da-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32568.65535)</span><span class="sxs-lookup"><span data-stu-id="300da-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32568..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="300da-184">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="300da-184">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="300da-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="300da-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="300da-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="300da-187">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="300da-187">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="300da-188">Das Format des System namens des Computers.</span><span class="sxs-lookup"><span data-stu-id="300da-188">The format of the computer system name.</span></span>

<dt>



 <span data-ttu-id="300da-189">("Other")</span><span class="sxs-lookup"><span data-stu-id="300da-189">("Other")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-190">("IP")</span><span class="sxs-lookup"><span data-stu-id="300da-190">("IP")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-191">("Dial")</span><span class="sxs-lookup"><span data-stu-id="300da-191">("Dial")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-192">("HID")</span><span class="sxs-lookup"><span data-stu-id="300da-192">("HID")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-193">("NWA")</span><span class="sxs-lookup"><span data-stu-id="300da-193">("NWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-194">("Hwa")</span><span class="sxs-lookup"><span data-stu-id="300da-194">("HWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-195">("X25")</span><span class="sxs-lookup"><span data-stu-id="300da-195">("X25")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-196">("ISDN")</span><span class="sxs-lookup"><span data-stu-id="300da-196">("ISDN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-197">("IPX")</span><span class="sxs-lookup"><span data-stu-id="300da-197">("IPX")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-198">("DCC")</span><span class="sxs-lookup"><span data-stu-id="300da-198">("DCC")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-199">("ICD")</span><span class="sxs-lookup"><span data-stu-id="300da-199">("ICD")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-200">("E. 164")</span><span class="sxs-lookup"><span data-stu-id="300da-200">("E.164")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-201">("SNA")</span><span class="sxs-lookup"><span data-stu-id="300da-201">("SNA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-202">("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="300da-202">("OID/OSI")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-203">("WWN")</span><span class="sxs-lookup"><span data-stu-id="300da-203">("WWN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="300da-204">("Naa")</span><span class="sxs-lookup"><span data-stu-id="300da-204">("NAA")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="300da-205">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="300da-205">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-206">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="300da-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="300da-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="300da-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="300da-208">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Computersystem**".**Dediziert**")</span><span class="sxs-lookup"><span data-stu-id="300da-208">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**Dedicated**")</span></span>
</dt> </dl>

<span data-ttu-id="300da-209">Beschreibt, wie oder warum das System dediziert ist, wenn das **dedizierte** Array den Wert 2 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="300da-209">Describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="300da-210">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="300da-210">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-211">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="300da-211">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="300da-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="300da-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="300da-213">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ powermanagementfunktionalitäten. Power-Funktionen"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Energiesteuerung \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="300da-213">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="300da-214">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="300da-214">This property is deprecated.</span></span> <span data-ttu-id="300da-215">Verwenden Sie stattdessen die **powerchangefunktionalitäten** -Methode in der **CIM \_ powermanagementcapabilitiescim \_ powermanagementservice** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="300da-215">Instead, use the **PowerChangeCapabilities** method in the **CIM\_PowerManagementCapabilitiesCIM\_PowerManagementService** class.</span></span>

<span data-ttu-id="300da-216">**Veraltete Beschreibung:** Die Energie Verwaltungsfunktionen des Systems.</span><span class="sxs-lookup"><span data-stu-id="300da-216">**Deprecated description:** The power management capabilities of the system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="300da-217">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="300da-217">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="300da-218">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="300da-218">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="300da-219">**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="300da-219">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="300da-220">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="300da-220">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="300da-221">**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="300da-221">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="300da-222">**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="300da-222">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="300da-223">**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="300da-223">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="300da-224">**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="300da-224">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="300da-225">**Resetcapability**</span><span class="sxs-lookup"><span data-stu-id="300da-225">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-226">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="300da-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="300da-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="300da-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="300da-228">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| System Hardware Security \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="300da-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="300da-229">Gibt an, ob das System den Hardware Zurücksetzungs Vorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="300da-229">Indicates whether the system supports the hardware reset operation.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="300da-230">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="300da-230">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="300da-231">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="300da-231">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="300da-232">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="300da-232">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="300da-233">**Aktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="300da-233">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="300da-234">**Nicht implementiert** (5)</span><span class="sxs-lookup"><span data-stu-id="300da-234">**Not Implemented** (5)</span></span>


<span data-ttu-id="300da-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="300da-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="300da-236">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="300da-236">Requirements</span></span>



| <span data-ttu-id="300da-237">Anforderung</span><span class="sxs-lookup"><span data-stu-id="300da-237">Requirement</span></span> | <span data-ttu-id="300da-238">Wert</span><span class="sxs-lookup"><span data-stu-id="300da-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="300da-239">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="300da-239">Minimum supported client</span></span><br/> | <span data-ttu-id="300da-240">Windows 8</span><span class="sxs-lookup"><span data-stu-id="300da-240">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="300da-241">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="300da-241">Minimum supported server</span></span><br/> | <span data-ttu-id="300da-242">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="300da-242">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="300da-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="300da-243">Namespace</span></span><br/>                | <span data-ttu-id="300da-244">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="300da-244">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="300da-245">MOF</span><span class="sxs-lookup"><span data-stu-id="300da-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="300da-246"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="300da-246"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="300da-247">DLL</span><span class="sxs-lookup"><span data-stu-id="300da-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="300da-248"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="300da-248"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="300da-249">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="300da-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="300da-250">**CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="300da-250">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

