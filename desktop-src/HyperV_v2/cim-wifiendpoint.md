---
description: Stellt einen drahtlosen Kommunikations Endpunkt dar, der Datenrahmen senden und empfangen kann, wenn das zugehörige Schnittstellen Gerät mit einem IEEE 802,11-Drahtlos LAN verbunden ist.
ms.assetid: 61743402-f333-4501-ba17-e676d85f72f3
title: CIM_WiFiEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiEndpoint
- CIM_WiFiEndpoint.LANID
- CIM_WiFiEndpoint.ProtocolIFType
- CIM_WiFiEndpoint.EncryptionMethod
- CIM_WiFiEndpoint.OtherEncryptionMethod
- CIM_WiFiEndpoint.AuthenticationMethod
- CIM_WiFiEndpoint.OtherAuthenticationMethod
- CIM_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- CIM_WiFiEndpoint.AccessPointAddress
- CIM_WiFiEndpoint.BSSType
- CIM_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e09d040f9d4530bee4347528d704cfe2e9403b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366079"
---
# <a name="cim_wifiendpoint-class"></a><span data-ttu-id="21543-103">CIM- \_ wifendpoint-Klasse</span><span class="sxs-lookup"><span data-stu-id="21543-103">CIM\_WiFiEndpoint class</span></span>

<span data-ttu-id="21543-104">Stellt einen drahtlosen Kommunikations Endpunkt dar, der Datenrahmen senden und empfangen kann, wenn das zugehörige Schnittstellen Gerät mit einem IEEE 802,11-Drahtlos LAN verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="21543-104">Represents a wireless communication endpoint, which can send and receive data frames when its associated interface device is connected with an IEEE 802.11 wireless LAN.</span></span>

## <a name="syntax"></a><span data-ttu-id="21543-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21543-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Network::Wireless"), AMENDMENT]
class CIM_WiFiEndpoint : CIM_LANEndpoint
{
  string  LANID;
  uint16  ProtocolIFType = 71;
  uint16  EncryptionMethod;
  string  OtherEncryptionMethod;
  uint16  AuthenticationMethod;
  string  OtherAuthenticationMethod;
  uint16  IEEE8021xAuthenticationProtocol;
  string  AccessPointAddress;
  uint16  BSSType;
  boolean Associated;
};
```

## <a name="members"></a><span data-ttu-id="21543-106">Member</span><span class="sxs-lookup"><span data-stu-id="21543-106">Members</span></span>

<span data-ttu-id="21543-107">Die **CIM- \_ wiatendpoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="21543-107">The **CIM\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="21543-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21543-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21543-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21543-109">Properties</span></span>

<span data-ttu-id="21543-110">Die **CIM \_ wifendpoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="21543-110">The **CIM\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21543-111">**Access spointaddress**</span><span class="sxs-lookup"><span data-stu-id="21543-111">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21543-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21543-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21543-114">Die Mac-Adresse des Zugriffs Punkts, der mit dem Wi-Fi Endpunkt verknüpft ist. andernfalls **null**.</span><span class="sxs-lookup"><span data-stu-id="21543-114">The MAC address of the access point that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="21543-115">**Zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="21543-115">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21543-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21543-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21543-118">**true** , wenn der WiFi-Endpunkt derzeit einem Zugriffspunkt oder einer Client Station zugeordnet ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="21543-118">**true** if the WiFi endpoint is currently associated with an access point or client station; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="21543-119">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="21543-119">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-120">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21543-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21543-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21543-122">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ wifendpoint**".**Verschlüsselungsmethod**","**CIM \_ wifendpoint**.**IEEE8021xAuthenticationProtocol**","**CIM \_ wifendpoint**.**Otherauthenticationmethod**")</span><span class="sxs-lookup"><span data-stu-id="21543-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**", "**CIM\_WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**", "**CIM\_WiFiEndpoint**.**OtherAuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="21543-123">Der Authentifizierungstyp, der zwischen dem Wi-Fi Endpunkt und dem Netzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21543-123">The authentication type used between the Wi-Fi endpoint and the network.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21543-124">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21543-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21543-125">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21543-125">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>

<span data-ttu-id="21543-126">**System öffnen** (2)</span><span class="sxs-lookup"><span data-stu-id="21543-126">**Open System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>

<span data-ttu-id="21543-127">**Gemeinsam** verwendeter Schlüssel (3)</span><span class="sxs-lookup"><span data-stu-id="21543-127">**Shared Key** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>

<span data-ttu-id="21543-128">**WPA-PSK** (4)</span><span class="sxs-lookup"><span data-stu-id="21543-128">**WPA PSK** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>

<span data-ttu-id="21543-129">**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="21543-129">**WPA IEEE 802.1x** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>

<span data-ttu-id="21543-130">**WPA2-PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="21543-130">**WPA2 PSK** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>

<span data-ttu-id="21543-131">**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="21543-131">**WPA2 IEEE 802.1x** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>

<span data-ttu-id="21543-132">**CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="21543-132">**CCKM IEEE 802.1x** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="21543-133">**DMTF reserviert** (9..)</span><span class="sxs-lookup"><span data-stu-id="21543-133">**DMTF Reserved** (9..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21543-134">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="21543-134">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21543-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21543-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21543-137">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3,16")</span><span class="sxs-lookup"><span data-stu-id="21543-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3.16")</span></span>
</dt> </dl>

<span data-ttu-id="21543-138">Der grundlegende Service Set-Typ (BSS) des Netzwerks, das der-Instanz entspricht.</span><span class="sxs-lookup"><span data-stu-id="21543-138">The basic service set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="21543-139">Ein BSS ist ein Satz von Stationen, die von einer einzelnen Koordinations Funktion gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="21543-139">A BSS is a set of stations controlled by a single coordination function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21543-140">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21543-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="21543-141">**Unabhängig** (2)</span><span class="sxs-lookup"><span data-stu-id="21543-141">**Independent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span>

<span data-ttu-id="21543-142">**Infrastruktur** (3)</span><span class="sxs-lookup"><span data-stu-id="21543-142">**Infrastructure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="21543-143">**DMTF reserviert** (4..)</span><span class="sxs-lookup"><span data-stu-id="21543-143">**DMTF Reserved** (4..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21543-144">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="21543-144">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-145">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21543-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21543-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21543-147">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ wifendpoint**".**AuthenticationMethod**","**CIM \_ wifendpoint**.**Otherverschlüsselungsmethod**")</span><span class="sxs-lookup"><span data-stu-id="21543-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**", "**CIM\_WiFiEndpoint**.**OtherEncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="21543-148">Der Verschlüsselungstyp, der beim Senden und empfangen von Daten über den Wi-Fi-Endpunkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21543-148">The encryption type used when sending and receiving data through the Wi-Fi endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21543-149">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="21543-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21543-150">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21543-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WEP"></span><span id="wep"></span>

<span data-ttu-id="21543-151">**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="21543-151">**WEP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TKIP"></span><span id="tkip"></span>

<span data-ttu-id="21543-152">**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="21543-152">**TKIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CCMP"></span><span id="ccmp"></span>

<span data-ttu-id="21543-153">**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="21543-153">**CCMP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="21543-154">**Keine** (5)</span><span class="sxs-lookup"><span data-stu-id="21543-154">**None** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="21543-155">**DMTF reserviert** (6..)</span><span class="sxs-lookup"><span data-stu-id="21543-155">**DMTF Reserved** (6..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21543-156">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="21543-156">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-157">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21543-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21543-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21543-159">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017. IETF "," RFC2716. IETF "," Draft-IETF-pppext-EAP-TTLS. IETF "," Draft-kamath-pppext-PEAPv0. IETF "," Draft-Josefsson-pppext-EAP-TLS-EAP "," RFC4851. IETF "," RFC3748. IETF "," RFC4764. IETF "," RFC4186. IETF "," RFC4187. IETF "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ wifendpoint**".**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="21543-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017.IETF", "RFC2716.IETF", "draft-ietf-pppext-eap-ttls.IETF", "draft-kamath-pppext-peapv0.IETF", "draft-josefsson-pppext-eap-tls-eap", "RFC4851.IETF", "RFC3748.IETF", "RFC4764.IETF", "RFC4186.IETF", "RFC4187.IETF"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="21543-160">Der EAP-Typ (Extensible Authentication Protocol) für den Wi-Fi-Endpunkt, wenn **AuthenticationMethod** "7" (WPA IEEE 802.1 x) oder "8" (CCKM IEEE 802.1 x) enthält.</span><span class="sxs-lookup"><span data-stu-id="21543-160">The EAP (Extensible Authentication Protocol) type for the Wi-Fi endpoint when **AuthenticationMethod** contains "7" (WPA IEEE 802.1x) or "8" (CCKM IEEE 802.1x).</span></span>

<dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>

<span data-ttu-id="21543-161">**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="21543-161">**EAP-TLS** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>

<span data-ttu-id="21543-162">**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="21543-162">**EAP-TTLS/MSCHAPv2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>

<span data-ttu-id="21543-163">**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="21543-163">**PEAPv0/EAP-MSCHAPv2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>

<span data-ttu-id="21543-164">**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="21543-164">**PEAPv1/EAP-GTC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>

<span data-ttu-id="21543-165">**EAP-fast/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="21543-165">**EAP-FAST/MSCHAPv2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>

<span data-ttu-id="21543-166">**EAP-fast/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="21543-166">**EAP-FAST/GTC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>

<span data-ttu-id="21543-167">**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="21543-167">**EAP-MD5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>

<span data-ttu-id="21543-168">**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="21543-168">**EAP-PSK** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>

<span data-ttu-id="21543-169">**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="21543-169">**EAP-SIM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>

<span data-ttu-id="21543-170">**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="21543-170">**EAP-AKA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>

<span data-ttu-id="21543-171">**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="21543-171">**EAP-FAST/TLS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="21543-172">**DMTF reserviert** (11..)</span><span class="sxs-lookup"><span data-stu-id="21543-172">**DMTF Reserved** (11..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21543-173">**Lanid**</span><span class="sxs-lookup"><span data-stu-id="21543-173">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21543-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21543-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21543-176">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("lanid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span><span class="sxs-lookup"><span data-stu-id="21543-176">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span></span>
</dt> </dl>

<span data-ttu-id="21543-177">Der Service Set Identifier (SSID) des Drahtlos-LANs, das mit dem Wi-Fi Endpunkt verknüpft ist. andernfalls **null**.</span><span class="sxs-lookup"><span data-stu-id="21543-177">The service set identifier (SSID) of the wireless LAN that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="21543-178">**Otherauthenticationmethod**</span><span class="sxs-lookup"><span data-stu-id="21543-178">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21543-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21543-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21543-181">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ wifendpoint**".**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="21543-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="21543-182">Der Authentifizierungstyp, der zwischen dem Wi-Fi Endpunkt und dem Netzwerk verwendet wird, wenn " **AuthenticationMethod** " "1" (sonstige) enthält.</span><span class="sxs-lookup"><span data-stu-id="21543-182">The authentication type used between the Wi-Fi endpoint and the network when **AuthenticationMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="21543-183">**Otherverschlüsselungsmethod**</span><span class="sxs-lookup"><span data-stu-id="21543-183">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21543-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21543-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21543-186">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ wifendpoint**".**Verschlüsselungsmethode**")</span><span class="sxs-lookup"><span data-stu-id="21543-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="21543-187">Beschreibt den Verschlüsselungstyp für den Wi-Fi Endpunkt, wenn " **verschlüsselungmethod** " "1" (sonstige) enthält.</span><span class="sxs-lookup"><span data-stu-id="21543-187">Describes the encryption type for the Wi-Fi endpoint when **EncryptionMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="21543-188">**Protocoliftype**</span><span class="sxs-lookup"><span data-stu-id="21543-188">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21543-189">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21543-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21543-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21543-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21543-191">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("protocoliftype")</span><span class="sxs-lookup"><span data-stu-id="21543-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span></span>
</dt> </dl>

<span data-ttu-id="21543-192">Die Kategorie oder Klassifizierung dieser Instanz.</span><span class="sxs-lookup"><span data-stu-id="21543-192">The category or classification of this instance.</span></span> <span data-ttu-id="21543-193">Die möglichen Werte sind auf die Wi-Fi und die reservierten Werte aus der DMTF-und [IANA iftype-MIB](https://www.iana.org/assignments/ianaiftype-mib)beschränkt.</span><span class="sxs-lookup"><span data-stu-id="21543-193">The possible values are limited to the Wi-Fi and reserved values from the DMTF and [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span>

<span data-ttu-id="21543-194">Wenn **protocoliftype** auf "1" (sonstige) festgelegt ist, sollten die Typinformationen in der **OtherTypeDescription** -Eigenschaft bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="21543-194">If the **ProtocolIFType** is set to "1" (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21543-195">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="21543-195">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

<span data-ttu-id="21543-196">**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="21543-196">**IEEE 802.11** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

<span data-ttu-id="21543-197">**IANA reserviert** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="21543-197">**IANA Reserved** (225..4095)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="21543-198">**DMTF reserviert** (4301.32767)</span><span class="sxs-lookup"><span data-stu-id="21543-198">**DMTF Reserved** (4301..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="21543-199">**Anbieter reserviert** (32768..)</span><span class="sxs-lookup"><span data-stu-id="21543-199">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="21543-200"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="21543-200"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="21543-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21543-201">Requirements</span></span>



| <span data-ttu-id="21543-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21543-202">Requirement</span></span> | <span data-ttu-id="21543-203">Wert</span><span class="sxs-lookup"><span data-stu-id="21543-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21543-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21543-204">Minimum supported client</span></span><br/> | <span data-ttu-id="21543-205">Windows 8</span><span class="sxs-lookup"><span data-stu-id="21543-205">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="21543-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21543-206">Minimum supported server</span></span><br/> | <span data-ttu-id="21543-207">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21543-207">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="21543-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="21543-208">Namespace</span></span><br/>                | <span data-ttu-id="21543-209">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="21543-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="21543-210">MOF</span><span class="sxs-lookup"><span data-stu-id="21543-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21543-211"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="21543-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="21543-212">DLL</span><span class="sxs-lookup"><span data-stu-id="21543-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21543-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="21543-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="21543-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21543-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21543-215">**CIM- \_ lanendpoint**</span><span class="sxs-lookup"><span data-stu-id="21543-215">**CIM\_LANEndpoint**</span></span>](cim-lanendpoint.md)
</dt> </dl>

 

