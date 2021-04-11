---
description: Stellt den logischen Verbindungspunkt für einen Netzwerkadapter dar. Wenn der Wi-Fi-Endpunkt mit einem Switchport verbunden ist, verfügt der Netzwerkadapter, der mit dem Wi-Fi Endpunkt verbunden ist, über eine Netzwerkverbindung.
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Msvm_WiFiEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f4a0a287d85b7a229b0e8e50a10c402fca734429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958889"
---
# <a name="msvm_wifiendpoint-class"></a><span data-ttu-id="848bd-104">MSVM- \_ wifiendpoint-Klasse</span><span class="sxs-lookup"><span data-stu-id="848bd-104">Msvm\_WiFiEndpoint class</span></span>

<span data-ttu-id="848bd-105">Stellt den logischen Verbindungspunkt für einen Netzwerkadapter dar.</span><span class="sxs-lookup"><span data-stu-id="848bd-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="848bd-106">Wenn der Wi-Fi-Endpunkt mit einem Switchport verbunden ist, verfügt der Netzwerkadapter, der mit dem Wi-Fi Endpunkt verbunden ist, über eine Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="848bd-106">When the Wi-Fi endpoint is connected to a switch port, the network adapter connected to the Wi-Fi endpoint has network connectivity.</span></span>

<span data-ttu-id="848bd-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="848bd-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="848bd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="848bd-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a><span data-ttu-id="848bd-109">Member</span><span class="sxs-lookup"><span data-stu-id="848bd-109">Members</span></span>

<span data-ttu-id="848bd-110">Die **MSVM \_ wifiendpoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="848bd-110">The **Msvm\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="848bd-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="848bd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="848bd-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="848bd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="848bd-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="848bd-113">Methods</span></span>

<span data-ttu-id="848bd-114">Die **MSVM \_ wifiendpoint** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="848bd-114">The **Msvm\_WiFiEndpoint** class has these methods.</span></span>



| <span data-ttu-id="848bd-115">Methode</span><span class="sxs-lookup"><span data-stu-id="848bd-115">Method</span></span>                 | <span data-ttu-id="848bd-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="848bd-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="848bd-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="848bd-117">**RequestStateChange**</span></span> | <span data-ttu-id="848bd-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="848bd-118">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="848bd-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="848bd-119">Properties</span></span>

<span data-ttu-id="848bd-120">Die **MSVM \_ wifiendpoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="848bd-120">The **Msvm\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="848bd-121">**Access spointaddress**</span><span class="sxs-lookup"><span data-stu-id="848bd-121">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-124">Enthält die Mac-Adresse des Zugriffs Punkts, dem der Wi-Fi-Endpunkt derzeit zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-124">Contains the MAC address of the access point with which the Wi-Fi endpoint is currently associated.</span></span> <span data-ttu-id="848bd-125">Wenn der Wi-Fi Endpunkt derzeit nicht zugeordnet ist, sollte **accesspointaddress** **null** sein.</span><span class="sxs-lookup"><span data-stu-id="848bd-125">If the Wi-Fi endpoint is not currently associated, then **AccessPointAddress** should be **Null**.</span></span> <span data-ttu-id="848bd-126">Die Mac-Adresse muss als zwölf hexadezimal Ziffern formatiert werden (z. b. "010203040506"), wobei jedes Paar eines der sechs Oktette der Mac-Adresse in kanonischer bidirektionale darstellt (z. b. befindet sich das Gruppen Adress Bit im unteren Bit des ersten Zeichens der Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="848bd-126">The MAC address should be formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (for example, the Group address bit is found in the low order bit of the first character of the string).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-127">**Aliasadressen**</span><span class="sxs-lookup"><span data-stu-id="848bd-127">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-128">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="848bd-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="848bd-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-130">Andere Unicastadressen, die für die Kommunikation mit dem LAN-Endpunkt verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="848bd-130">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="848bd-131">Diese Eigenschaft wird von [**CIM \_ lanendpoint**](/previous-versions//cc136865(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-131">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-132">**Zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="848bd-132">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-133">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="848bd-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-135">Gibt an, ob der Wi-Fi Endpunkt derzeit einem Zugriffspunkt oder einer Client Station zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-135">Indicates whether the Wi-Fi endpoint is currently associated to an access point or client station.</span></span>

<span data-ttu-id="848bd-136">Enthält **true** , wenn der Wi-Fi Endpunkt einem Zugriffspunkt oder einer Client Station zugeordnet ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="848bd-136">Contains **True** if the Wi-Fi endpoint is associated to an access point or client station; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="848bd-137">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="848bd-137">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-138">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-140">Gibt die Methode an, die verwendet wird, um den Wi-Fi Endpunkt und das Netzwerk untereinander zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="848bd-140">Specifies the method used to authenticate the Wi-Fi endpoint and the network to one another.</span></span>

<dl> <dt>

<span data-ttu-id="848bd-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="848bd-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="848bd-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**System öffnen** (2)</span><span class="sxs-lookup"><span data-stu-id="848bd-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Open System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Gemeinsam** verwendeter Schlüssel (3)</span><span class="sxs-lookup"><span data-stu-id="848bd-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Shared Key** (3)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA-PSK** (4)</span><span class="sxs-lookup"><span data-stu-id="848bd-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="848bd-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1x** (5)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2-PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="848bd-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="848bd-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1x** (7)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="848bd-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1x** (8)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (9...</span><span class="sxs-lookup"><span data-stu-id="848bd-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (9..</span></span> <span data-ttu-id="848bd-151">)</span><span class="sxs-lookup"><span data-stu-id="848bd-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="848bd-152">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="848bd-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-153">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="848bd-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="848bd-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-155">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="848bd-155">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="848bd-156">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind.</span><span class="sxs-lookup"><span data-stu-id="848bd-156">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="848bd-157">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="848bd-157">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="848bd-158">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="848bd-158">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="848bd-159">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="848bd-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="848bd-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="848bd-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="848bd-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="848bd-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="848bd-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="848bd-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="848bd-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="848bd-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="848bd-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="848bd-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="848bd-170">)</span><span class="sxs-lookup"><span data-stu-id="848bd-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="848bd-171">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="848bd-171">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-172">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-174">Gibt den grundlegenden Service Set (BSS)-Typ des Netzwerks an, das der-Instanz entspricht.</span><span class="sxs-lookup"><span data-stu-id="848bd-174">Indicates the Basic Service Set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="848bd-175">Ein grundlegender Service Satz ist eine Gruppe von Stationen, die von einer einzelnen Koordinations Funktion gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="848bd-175">A Basic Service Set is a set of stations controlled by a single coordination function.</span></span>



| <span data-ttu-id="848bd-176">Wert</span><span class="sxs-lookup"><span data-stu-id="848bd-176">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="848bd-177">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="848bd-177">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="848bd-178"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="848bd-178"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <span data-ttu-id="848bd-179"><dt>**Unabhängig**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="848bd-179"><dt>**Independent**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="848bd-180">Der Wi-Fi-Endpunkt wird direkt einer anderen Client Station zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="848bd-180">The Wi-Fi endpoint is associated directly to another client station.</span></span><br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <span data-ttu-id="848bd-181"><dt>**Infrastruktur**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="848bd-181"><dt>**Infrastructure**</dt> <dt>3</dt></span></span> </dl>    | <span data-ttu-id="848bd-182">Der Wi-Fi-Endpunkt wird einem Netzwerk mithilfe eines Zugriffs Punkts zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="848bd-182">The Wi-Fi endpoint is associated to a network by using an access point.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="848bd-183"><dt> **DMTF reserviert**</dt> <dt>4..</dt></span><span class="sxs-lookup"><span data-stu-id="848bd-183"><dt>**DMTF Reserved** </dt> <dt>4.. </dt></span></span> </dl> |                                                                                    |



 

</dd> <dt>

<span data-ttu-id="848bd-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="848bd-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-187">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="848bd-187">A short description of the object.</span></span> <span data-ttu-id="848bd-188">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-189">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="848bd-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-190">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-192">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="848bd-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="848bd-193">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="848bd-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-195">**Verbunden**</span><span class="sxs-lookup"><span data-stu-id="848bd-195">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-196">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="848bd-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-198">Diese Eigenschaft wird auf **true** festgelegt, wenn der Wi-Fi Endpunkt mit einem Switchport verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-198">This property is set to **True** if the Wi-Fi endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="848bd-199">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="848bd-199">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="848bd-202">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="848bd-202">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="848bd-203">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="848bd-203">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="848bd-204">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-204">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-205">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="848bd-205">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-208">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="848bd-208">A description of the object.</span></span> <span data-ttu-id="848bd-209">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-210">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="848bd-210">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-211">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-213">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="848bd-213">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="848bd-214">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-214">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="848bd-215">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="848bd-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-219">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="848bd-219">A display name for the object.</span></span> <span data-ttu-id="848bd-220">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-221">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="848bd-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-222">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-224">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="848bd-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="848bd-225">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="848bd-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="848bd-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="848bd-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="848bd-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="848bd-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="848bd-229">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="848bd-229">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-230">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-232">Gibt den aktivierten Zustand des geplanten Systems an.</span><span class="sxs-lookup"><span data-stu-id="848bd-232">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="848bd-233">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="848bd-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="848bd-234">Wert</span><span class="sxs-lookup"><span data-stu-id="848bd-234">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="848bd-235">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="848bd-235">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="848bd-236"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="848bd-236"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="848bd-237">Das System ist ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="848bd-237">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="848bd-238"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="848bd-238"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="848bd-239">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="848bd-239">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="848bd-240"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="848bd-240"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="848bd-241">Das System ist aktiviert, aber offline.</span><span class="sxs-lookup"><span data-stu-id="848bd-241">The system is enabled, but offline.</span></span> <span data-ttu-id="848bd-242">Alle neuen Anforderungen werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="848bd-242">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="848bd-243">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="848bd-243">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-244">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-246">Gibt die verwendete Verschlüsselungsmethode zum Schutz der Vertraulichkeit von Daten an, die vom Wi-Fi Endpunkt gesendet und empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="848bd-246">Specifies the encryption method in use to protect the confidentiality of data sent and received by the Wi-Fi endpoint.</span></span>

<dl> <dt>

<span data-ttu-id="848bd-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="848bd-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="848bd-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="848bd-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="848bd-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="848bd-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (5)</span><span class="sxs-lookup"><span data-stu-id="848bd-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (5)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (6...</span><span class="sxs-lookup"><span data-stu-id="848bd-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (6..</span></span> <span data-ttu-id="848bd-254">)</span><span class="sxs-lookup"><span data-stu-id="848bd-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="848bd-255">**Groupadressen**</span><span class="sxs-lookup"><span data-stu-id="848bd-255">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-256">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="848bd-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="848bd-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-258">Multicast Adressen, auf die der LAN-Endpunkt lauscht.</span><span class="sxs-lookup"><span data-stu-id="848bd-258">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="848bd-259">Diese Eigenschaft wird von [**CIM \_ lanendpoint**](/previous-versions//cc136865(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-259">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-260">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="848bd-260">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-261">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-263">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="848bd-263">The current health of the element.</span></span> <span data-ttu-id="848bd-264">Diese Eigenschaft drückt die Integrität dieses Elements aus, aber nicht notwendigerweise die seiner unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="848bd-264">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="848bd-265">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-265">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="848bd-266">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-267">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="848bd-267">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-268">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-270">Enthält den EAP-Typ (Extensible Authentication Protocol) nur dann, wenn **AuthenticationMethod** 5 (WPA IEEE 802.1 x), 7 (WPA2 IEEE 802.1 x) oder 8 (CCKM IEEE 802.1 x) enthält.</span><span class="sxs-lookup"><span data-stu-id="848bd-270">Contains the Extensible Authentication Protocol (EAP) type if and only if **AuthenticationMethod** contains 5 (WPA IEEE 802.1x), 7 (WPA2 IEEE 802.1x), or 8 (CCKM IEEE 802.1x).</span></span>

<dl> <dt>

<span data-ttu-id="848bd-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="848bd-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="848bd-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="848bd-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="848bd-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-fast/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="848bd-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-fast/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="848bd-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="848bd-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="848bd-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="848bd-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="848bd-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="848bd-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (11...</span><span class="sxs-lookup"><span data-stu-id="848bd-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (11..</span></span> <span data-ttu-id="848bd-283">)</span><span class="sxs-lookup"><span data-stu-id="848bd-283">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="848bd-284">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="848bd-284">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-285">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="848bd-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-287">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="848bd-287">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="848bd-288">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-289">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="848bd-289">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-290">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="848bd-292">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="848bd-292">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="848bd-293">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="848bd-293">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="848bd-294">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-294">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-295">**Lanid**</span><span class="sxs-lookup"><span data-stu-id="848bd-295">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-296">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-298">Eine Bezeichnung oder ein Bezeichner für das LAN-Segment, mit dem der Endpunkt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-298">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="848bd-299">Wenn der Endpunkt derzeit nicht aktiv/verbunden ist oder diese Informationen nicht bekannt sind, ist diese Eigenschaft **null**.</span><span class="sxs-lookup"><span data-stu-id="848bd-299">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="848bd-300">Diese Eigenschaft wird von [**CIM \_ lanendpoint**](/previous-versions//cc136865(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-300">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-301">**Lantype**</span><span class="sxs-lookup"><span data-stu-id="848bd-301">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-302">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-304">Diese Eigenschaft wird anstelle der **ProtocolType** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="848bd-304">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="848bd-305">Diese Eigenschaft wird von [**CIM \_ lanendpoint**](/previous-versions//cc136865(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-305">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-306">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="848bd-306">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="848bd-309">Qualifizierer: **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="848bd-309">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="848bd-310">Die bei der Kommunikation mit dem LAN-Endpunkt verwendete MAC-Adresse.</span><span class="sxs-lookup"><span data-stu-id="848bd-310">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="848bd-311">Die Mac-Adresse ist als zwölf hexadezimal Ziffern (z. b. "010203040506") formatiert, wobei jedes Paar eines der sechs Oktette der Mac-Adresse in kanonischer bitreihenfolge gemäß RFC 2469 darstellt.</span><span class="sxs-lookup"><span data-stu-id="848bd-311">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="848bd-312">Diese Eigenschaft wird von [**CIM \_ lanendpoint**](/previous-versions//cc136865(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-312">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-313">**Maxdatasize**</span><span class="sxs-lookup"><span data-stu-id="848bd-313">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-314">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="848bd-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="848bd-316">Qualifizierer: **Einheiten** ("Bits")</span><span class="sxs-lookup"><span data-stu-id="848bd-316">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="848bd-317">Die größte Größe (in Bits) des Informations Felds, das vom LAN-Endpunkt gesendet oder empfangen werden kann.</span><span class="sxs-lookup"><span data-stu-id="848bd-317">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="848bd-318">Diese Eigenschaft wird von [**CIM \_ lanendpoint**](/previous-versions//cc136865(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-318">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-319">**Name**</span><span class="sxs-lookup"><span data-stu-id="848bd-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-320">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-322">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-322">The label by which the object is known.</span></span> <span data-ttu-id="848bd-323">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-324">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="848bd-324">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="848bd-327">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="848bd-327">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="848bd-328">Enthält die Namensheuristik, die ausgewählt wird, um sicherzustellen, dass der Wert der **Name** -Eigenschaft eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-328">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="848bd-329">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-329">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-330">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="848bd-330">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-331">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-333">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="848bd-333">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="848bd-334">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-334">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="848bd-335">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-335">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="848bd-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-337">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="848bd-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="848bd-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-339">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="848bd-339">The current statuses of the object.</span></span> <span data-ttu-id="848bd-340">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-341">**Otherauthenticationmethod**</span><span class="sxs-lookup"><span data-stu-id="848bd-341">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-344">Gibt die 802,11-Authentifizierungsmethode nur dann an, wenn **AuthenticationMethod** 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="848bd-344">Specifies the 802.11 authentication method if and only if **AuthenticationMethod** contains 1 (Other).</span></span> <span data-ttu-id="848bd-345">Das Format dieser Zeichenfolge ist Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="848bd-345">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="848bd-346">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="848bd-346">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-347">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-349">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-349">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="848bd-350">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-350">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="848bd-351">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-351">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-352">**Otherverschlüsselungsmethod**</span><span class="sxs-lookup"><span data-stu-id="848bd-352">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-355">Gibt die 802,11-Verschlüsselungsmethode nur dann an, wenn " **verschlüsselungsmethod** " 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="848bd-355">Specifies the 802.11 encryption method if and only if **EncryptionMethod** contains 1 (Other).</span></span> <span data-ttu-id="848bd-356">Das Format dieser Zeichenfolge ist Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="848bd-356">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="848bd-357">**Otherlantype**</span><span class="sxs-lookup"><span data-stu-id="848bd-357">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-360">Diese Eigenschaft wird anstelle der **OtherTypeDescription** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="848bd-360">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="848bd-361">Diese Eigenschaft wird von [**CIM \_ lanendpoint**](/previous-versions//cc136865(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-361">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-362">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="848bd-362">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-363">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="848bd-365">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="848bd-365">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="848bd-366">Eine Zeichenfolge, die den Typ des Protokoll Endpunkts beschreibt, wenn die **protocoliftype** -Eigenschaft dieser Klasse (oder eine ihrer Unterklassen) auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-366">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="848bd-367">Diese Eigenschaft sollte auf **null** festgelegt werden, wenn die **protocoliftype** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="848bd-367">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="848bd-368">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-368">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-369">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="848bd-369">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-370">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-372">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="848bd-372">Provides high level status information.</span></span> <span data-ttu-id="848bd-373">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="848bd-373">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="848bd-374">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="848bd-374">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="848bd-375">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-376">**Protocoliftype**</span><span class="sxs-lookup"><span data-stu-id="848bd-376">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-377">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-379">Die-Eigenschaft wird verwendet, um Instanzen dieser Klasse zu kategorisieren und zu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="848bd-379">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="848bd-380">Wenn **protocoliftype** auf 1 (Sonstiges) festgelegt ist, sollten die Typinformationen in der **OtherTypeDescription** -Eigenschaft bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="848bd-380">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="848bd-381">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-381">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="848bd-382">**Protocoliftype** ist eine Enumeration, die mit der [IANA iftype-MIB](https://www.iana.org/assignments/ianaiftype-mib)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="848bd-382">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="848bd-383">Weitere Werte, die von der DMTF definiert werden, sind ebenfalls enthalten.</span><span class="sxs-lookup"><span data-stu-id="848bd-383">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="848bd-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="848bd-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="848bd-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA reserviert** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="848bd-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (4301.32767)</span><span class="sxs-lookup"><span data-stu-id="848bd-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (4301..32767)</span></span>
</dt> <dt>

<span data-ttu-id="848bd-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (32768...</span><span class="sxs-lookup"><span data-stu-id="848bd-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="848bd-389">)</span><span class="sxs-lookup"><span data-stu-id="848bd-389">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="848bd-390">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="848bd-390">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-391">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-393">Diese Eigenschaft wird anstelle der **protocoliftype** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="848bd-393">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="848bd-394">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-394">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="848bd-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-396">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-398">Der zuletzt angeforderte oder gewünschte Status für den Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="848bd-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="848bd-399">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-400">**Status**</span><span class="sxs-lookup"><span data-stu-id="848bd-400">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-401">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-403">Beschreibt den Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="848bd-403">Describes the status of the element.</span></span> <span data-ttu-id="848bd-404">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-404">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="848bd-405">Okay</span><span class="sxs-lookup"><span data-stu-id="848bd-405">"OK"</span></span>

<span data-ttu-id="848bd-406">Zeit</span><span class="sxs-lookup"><span data-stu-id="848bd-406">"Error"</span></span>

<span data-ttu-id="848bd-407">Zerstört</span><span class="sxs-lookup"><span data-stu-id="848bd-407">"Degraded"</span></span>

<span data-ttu-id="848bd-408">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="848bd-408">"Unknown"</span></span>

<span data-ttu-id="848bd-409">"Pred Fail"</span><span class="sxs-lookup"><span data-stu-id="848bd-409">"Pred Fail"</span></span>

<span data-ttu-id="848bd-410">Fahren</span><span class="sxs-lookup"><span data-stu-id="848bd-410">"Starting"</span></span>

<span data-ttu-id="848bd-411">Hindern</span><span class="sxs-lookup"><span data-stu-id="848bd-411">"Stopping"</span></span>

<span data-ttu-id="848bd-412">Leistungs</span><span class="sxs-lookup"><span data-stu-id="848bd-412">"Service"</span></span>

<span data-ttu-id="848bd-413">Gestresst</span><span class="sxs-lookup"><span data-stu-id="848bd-413">"Stressed"</span></span>

<span data-ttu-id="848bd-414">"Nicht wiederherstellen"</span><span class="sxs-lookup"><span data-stu-id="848bd-414">"NonRecover"</span></span>

<span data-ttu-id="848bd-415">"Kein Kontakt"</span><span class="sxs-lookup"><span data-stu-id="848bd-415">"No Contact"</span></span>

<span data-ttu-id="848bd-416">"Verlorene comm"</span><span class="sxs-lookup"><span data-stu-id="848bd-416">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="848bd-417">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="848bd-417">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-418">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="848bd-418">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="848bd-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-420">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="848bd-420">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="848bd-421">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-421">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-422">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="848bd-422">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-423">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-425">Der Name der Erstellungs Klasse des hostingsystems.</span><span class="sxs-lookup"><span data-stu-id="848bd-425">The hosting system's creation class name.</span></span> <span data-ttu-id="848bd-426">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-426">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-427">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="848bd-427">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-428">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="848bd-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="848bd-430">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="848bd-430">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="848bd-431">Der Name des hostingsystems.</span><span class="sxs-lookup"><span data-stu-id="848bd-431">The name of the hosting system.</span></span> <span data-ttu-id="848bd-432">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-432">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-433">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="848bd-433">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-434">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="848bd-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-436">Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements.</span><span class="sxs-lookup"><span data-stu-id="848bd-436">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="848bd-437">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-437">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="848bd-438">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="848bd-438">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="848bd-439">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="848bd-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="848bd-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="848bd-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="848bd-441">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="848bd-441">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="848bd-442">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="848bd-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="848bd-443">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="848bd-443">Requirements</span></span>



| <span data-ttu-id="848bd-444">Anforderung</span><span class="sxs-lookup"><span data-stu-id="848bd-444">Requirement</span></span> | <span data-ttu-id="848bd-445">Wert</span><span class="sxs-lookup"><span data-stu-id="848bd-445">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="848bd-446">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="848bd-446">Minimum supported client</span></span><br/> | <span data-ttu-id="848bd-447">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="848bd-447">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="848bd-448">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="848bd-448">Minimum supported server</span></span><br/> | <span data-ttu-id="848bd-449">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="848bd-449">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="848bd-450">Namespace</span><span class="sxs-lookup"><span data-stu-id="848bd-450">Namespace</span></span><br/>                | <span data-ttu-id="848bd-451">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="848bd-451">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="848bd-452">MOF</span><span class="sxs-lookup"><span data-stu-id="848bd-452">MOF</span></span><br/>                      | <dl> <span data-ttu-id="848bd-453"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="848bd-453"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="848bd-454">DLL</span><span class="sxs-lookup"><span data-stu-id="848bd-454">DLL</span></span><br/>                      | <dl> <span data-ttu-id="848bd-455"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="848bd-455"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

