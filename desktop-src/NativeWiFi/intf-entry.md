---
description: Enthält ausführliche Informationen zu einer Schnittstelle, die für einen RPC-Client erforderlich ist.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: INTF_ENTRY Struktur (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527650"
---
# <a name="intf_entry-structure"></a><span data-ttu-id="3be83-103">INTF- \_ Eintrags Struktur</span><span class="sxs-lookup"><span data-stu-id="3be83-103">INTF\_ENTRY structure</span></span>

<span data-ttu-id="3be83-104">\[**INTF \_ Der Eintrag** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3be83-104">\[**INTF\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="3be83-105">Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet.</span><span class="sxs-lookup"><span data-stu-id="3be83-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="3be83-106">Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="3be83-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="3be83-107">Enthält ausführliche Informationen zu einer Schnittstelle, die für einen RPC-Client erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3be83-107">Contains detailed information about an interface that is required by an RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be83-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3be83-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a><span data-ttu-id="3be83-109">Member</span><span class="sxs-lookup"><span data-stu-id="3be83-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="3be83-110">**wszguid**</span><span class="sxs-lookup"><span data-stu-id="3be83-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-111">Ein Zeiger auf die GUID der Schnittstelle, die als Unicode-Zeichenfolge im folgenden Format dargestellt wird: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span><span class="sxs-lookup"><span data-stu-id="3be83-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> <dt>

<span data-ttu-id="3be83-112">**wszdescr**</span><span class="sxs-lookup"><span data-stu-id="3be83-112">**wszDescr**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-113">Ein Zeiger auf eine Zeichenfolge, die die Schnittstellen Beschreibung enthält, die vom drahtlos Konfigurations Dienst (wzcsvc) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-113">A pointer to a string that contains the interface description that is retrieved by the Wireless Zero Configuration service (WZCSVC).</span></span>

</dd> <dt>

<span data-ttu-id="3be83-114">**dwcontext**</span><span class="sxs-lookup"><span data-stu-id="3be83-114">**dwContext**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-115">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3be83-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-116">**ulmediastate**</span><span class="sxs-lookup"><span data-stu-id="3be83-116">**ulMediaState**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-117">Der aktuelle NDIS-Medien Verbindungsstatus für die Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3be83-117">The current NDIS media connect state for the interface.</span></span> <span data-ttu-id="3be83-118">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3be83-118">The following table shows the possible values.</span></span>



| <span data-ttu-id="3be83-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3be83-119">Value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="3be83-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3be83-120">Meaning</span></span>                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <span data-ttu-id="3be83-121"><dt> **Medien \_ Status \_ verbunden**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-121"><dt>**MEDIA\_STATE\_CONNECTED** </dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="3be83-122">Das Medium ist verbunden.</span><span class="sxs-lookup"><span data-stu-id="3be83-122">The media is connected.</span></span><br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <span data-ttu-id="3be83-123"><dt>**Medien \_ Status \_ getrennt**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-123"><dt>**MEDIA\_STATE\_DISCONNECTED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3be83-124">Die Medien werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="3be83-124">The media is disconnected.</span></span><br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <span data-ttu-id="3be83-125"><dt>**Medien \_ \_Unbekannter Status**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-125"><dt>**MEDIA\_STATE\_UNKNOWN**</dt> <dt>-1</dt></span></span> </dl>               | <span data-ttu-id="3be83-126">Der Medien Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="3be83-126">The media state is unknown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3be83-127">**ulmediatype**</span><span class="sxs-lookup"><span data-stu-id="3be83-127">**ulMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-128">Die NDIS-Medientypen, die derzeit von der NIC verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3be83-128">The NDIS media types that the NIC currently uses.</span></span> <span data-ttu-id="3be83-129">Beim Abfragen ist der Wert dieses Members **NdisMedium802 \_ 3** , wie in der *ndispnp. h* -Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="3be83-129">When queried, the value of this member is **NdisMedium802\_3** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-130">**ulphysicalmediatype**</span><span class="sxs-lookup"><span data-stu-id="3be83-130">**ulPhysicalMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-131">Der NDIS-Medientyp für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3be83-131">The NDIS media type for the interface.</span></span> <span data-ttu-id="3be83-132">Beim Abfragen lautet der Wert dieses Members **ndisphysicalmedienwirelesslan** , wie in der *ndispnp. h* -Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="3be83-132">When queried, the value of this member is **NdisPhysicalMediumWirelessLan** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-133">**ninframode**</span><span class="sxs-lookup"><span data-stu-id="3be83-133">**nInfraMode**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-134">Der aktuelle 802,11-Infrastrukturmodus für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3be83-134">The current 802.11 Infrastructure Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-135">**nauthmode**</span><span class="sxs-lookup"><span data-stu-id="3be83-135">**nAuthMode**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-136">Der aktuelle 802,11-Authentifizierungsmodus für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3be83-136">The current 802.11 Authentication Mode set on the interface.</span></span>

<span data-ttu-id="3be83-137">In der folgenden Tabelle werden die möglichen Werte für den-Parameter basierend auf der in der Header Datei *ntddndis. h* definierten Enumeration für den **NDIS \_ 802 \_ 11- \_ authentifizierungmodus \_** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3be83-137">The following table shows the possible values for the parameter based on the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration defined in the *NtDDNdis.h* header file.</span></span>



| <span data-ttu-id="3be83-138">Wert</span><span class="sxs-lookup"><span data-stu-id="3be83-138">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="3be83-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3be83-139">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <span data-ttu-id="3be83-140"><dt>**Ndis802 \_ 11authmodeopen**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-140"><dt>**Ndis802\_11AuthModeOpen**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="3be83-141">IEEE 802,11 öffnen Sie die System Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="3be83-141">IEEE 802.11 Open System authentication.</span></span><br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <span data-ttu-id="3be83-142"><dt>**Ndis802 \_ 11authmodeshared**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-142"><dt>**Ndis802\_11AuthModeShared**</dt> <dt>2</dt></span></span> </dl>                 | <span data-ttu-id="3be83-143">Die freigegebene IEEE 802,11-Authentifizierung, bei der ein vorinstaltzter WEP-Schlüssel (Wired Equivalent Privacy) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-143">IEEE 802.11 shared authentication that uses a pre-shared wired equivalent privacy (WEP) key.</span></span> <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <span data-ttu-id="3be83-144"><dt>**Ndis802 \_ 11authmodeautoswitch**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-144"><dt>**Ndis802\_11AuthModeAutoSwitch**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="3be83-145">Automatischer switchmodus.</span><span class="sxs-lookup"><span data-stu-id="3be83-145">Auto-switch mode.</span></span> <span data-ttu-id="3be83-146">Wenn Sie den Auto-Switch-Modus verwenden, versucht die drahtlos Netzwerkschnittstellenkarte (NIC) zuerst den freigegebenen Authentifizierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="3be83-146">When using auto-switch mode, the wireless network interface card (NIC) tries shared authentication mode first.</span></span> <span data-ttu-id="3be83-147">Wenn der Modus "freigegeben" fehlschlägt, versucht die NIC, den offenen Authentifizierungsmodus zu verwenden</span><span class="sxs-lookup"><span data-stu-id="3be83-147">If shared mode fails, the NIC attempts to use open authentication mode.</span></span> <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <span data-ttu-id="3be83-148"><dt>**Ndis802 \_ 11authmodewpa**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-148"><dt>**Ndis802\_11AuthModeWPA**</dt> <dt>4</dt></span></span> </dl>                             | <span data-ttu-id="3be83-149">Sicherheit des drahtlos geschützten Zugriffs (WPA).</span><span class="sxs-lookup"><span data-stu-id="3be83-149">Wireless Protected Access(WPA) security.</span></span> <span data-ttu-id="3be83-150">Die Authentifizierung erfolgt zwischen dem Supplicant-, Authenticator-und Authentifizierungsserver über IEEE 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3be83-150">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="3be83-151">Verschlüsselungsschlüssel sind dynamisch und werden durch den Authentifizierungsprozess abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3be83-151">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <span data-ttu-id="3be83-152"><dt>**Ndis802 \_ 11authmodewpapsk**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-152"><dt>**Ndis802\_11AuthModeWPAPSK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="3be83-153">WPA-Sicherheit mit einem vorinstallierten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3be83-153">WPA security using a pre-shared key.</span></span> <span data-ttu-id="3be83-154">Die Authentifizierung erfolgt zwischen dem Supplicant und Authentifikator über IEEE 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3be83-154">Authentication is performed between the supplicant and authenticator over IEEE 802.1X.</span></span> <span data-ttu-id="3be83-155">Verschlüsselungsschlüssel sind dynamisch und werden über den vorinstallierten Schlüssel abgeleitet, der vom Supplicant und Authentifikator verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-155">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <span data-ttu-id="3be83-156"><dt>**Ndis802 \_ 11authmodewpanone**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-156"><dt>**Ndis802\_11AuthModeWPANone**</dt> <dt>6</dt></span></span> </dl>             | <span data-ttu-id="3be83-157">WPA-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="3be83-157">WPA security.</span></span> <span data-ttu-id="3be83-158">Die Authentifizierung erfolgt mithilfe eines vorinstallierten Schlüssels ohne IEEE 802.1 x-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="3be83-158">Authentication is performed using a preshared key without IEEE 802.1X authentication.</span></span> <span data-ttu-id="3be83-159">Verschlüsselungsschlüssel sind statisch und werden über den vorinstallierten Schlüssel abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3be83-159">Encryption keys are static and are derived through the preshared key.</span></span> <span data-ttu-id="3be83-160">Dieser Modus gilt nur für Ad-hoc-Netzwerktypen.</span><span class="sxs-lookup"><span data-stu-id="3be83-160">This mode is applicable only to ad hoc network types.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <span data-ttu-id="3be83-161"><dt>**Ndis802 \_ 11authmodewpf2**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-161"><dt>**Ndis802\_11AuthModeWPA2**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="3be83-162">WPA2-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="3be83-162">WPA2 security.</span></span> <span data-ttu-id="3be83-163">Die Authentifizierung erfolgt zwischen dem Supplicant-, Authenticator-und Authentifizierungsserver über IEEE 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3be83-163">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="3be83-164">Verschlüsselungsschlüssel sind dynamisch und werden durch den Authentifizierungsprozess abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3be83-164">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <span data-ttu-id="3be83-165"><dt>**Ndis802 \_ 11authmodewpa2psk**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-165"><dt>**Ndis802\_11AuthModeWPA2PSK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="3be83-166">Gibt die WPA2-Sicherheit an.</span><span class="sxs-lookup"><span data-stu-id="3be83-166">Specifies WPA2 security.</span></span> <span data-ttu-id="3be83-167">Die Authentifizierung erfolgt zwischen dem Supplicant und Authentifikator über IEEE 802 1X.</span><span class="sxs-lookup"><span data-stu-id="3be83-167">Authentication is performed between the supplicant and authenticator over IEEE 802 1X.</span></span> <span data-ttu-id="3be83-168">Verschlüsselungsschlüssel sind dynamisch und werden über den vorinstallierten Schlüssel abgeleitet, der vom Supplicant und Authentifikator verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-168">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <span data-ttu-id="3be83-169"><dt>**Ndis802 \_ 11authmodemax**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-169"><dt>**Ndis802\_11AuthModeMax**</dt> <dt>9</dt></span></span> </dl>                             | <span data-ttu-id="3be83-170">Der maximal mögliche Wert für den Enumerationswert des **NDIS \_ 802 \_ 11- \_ Authentifizierungs \_ Modus** .</span><span class="sxs-lookup"><span data-stu-id="3be83-170">The maximum possible value for the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration value.</span></span> <span data-ttu-id="3be83-171">Dies ist kein gültiger Wert für den Authentifizierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="3be83-171">This is not a legal value for the authentication mode.</span></span> <br/>                                                                                        |



 

</dd> <dt>

<span data-ttu-id="3be83-172">**nwepstatus**</span><span class="sxs-lookup"><span data-stu-id="3be83-172">**nWepStatus**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-173">Der aktuelle 802,11-Verschlüsselungs Modus für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3be83-173">The current 802.11 Encryption Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-174">**dwctlflags**</span><span class="sxs-lookup"><span data-stu-id="3be83-174">**dwCtlFlags**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-175">Ein Bitmasken Wert von steuerungflags, die angeben, wie wzcsvc auf der Schnittstelle funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3be83-175">A bitmask value of control flags that indicate how WZCSVC is operating on the interface.</span></span>

<span data-ttu-id="3be83-176">In der folgenden Tabelle werden die möglichen Bitwerte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3be83-176">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="3be83-177">Wert</span><span class="sxs-lookup"><span data-stu-id="3be83-177">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="3be83-178">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3be83-178">Meaning</span></span>                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <span data-ttu-id="3be83-179"><dt>**Intfctl \_ CM- \_ Maske**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-179"><dt>**INTFCTL\_CM\_MASK**</dt> <dt>0x0007</dt></span></span> </dl>      | <span data-ttu-id="3be83-180">Eine Bitmaske für den Netzwerk Filter Modus.</span><span class="sxs-lookup"><span data-stu-id="3be83-180">A bitmask for the network filter mode.</span></span> <span data-ttu-id="3be83-181">Die intfctl \_ cm \_ Mask-& dwctlflags ergeben einen Wert vom Typ NDIS \_ 802 \_ 11 \_ Network \_ Infrastructure.</span><span class="sxs-lookup"><span data-stu-id="3be83-181">INTFCTL\_CM\_MASK & dwCtlFlags result in a value of the type NDIS\_802\_11\_NETWORK\_INFRASTRUCTURE.</span></span> <span data-ttu-id="3be83-182">Der resultierende Wert gibt an, ob wzcsvc nur mit Infrastruktur Netzwerken, Ad-hoc-Netzwerken oder mit beiden Arten von Netzwerken verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="3be83-182">The resulting value indicates whether WZCSVC connects only to infrastructure networks, adhoc networks, or to both types of networks.</span></span><br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <span data-ttu-id="3be83-183"><dt>**Intfctl \_**</dt> <dt>0X8000</dt> aktiviert</span><span class="sxs-lookup"><span data-stu-id="3be83-183"><dt>**INTFCTL\_ENABLED**</dt> <dt>0x8000</dt></span></span> </dl>       | <span data-ttu-id="3be83-184">Gibt an, ob die Schnittstelle von wzcsvc konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3be83-184">Indicates whether WZCSVC should configure the interface.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <span data-ttu-id="3be83-185"><dt>**Intfctl \_ Fallback**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-185"><dt>**INTFCTL\_FALLBACK**</dt> <dt>0x4000</dt></span></span> </dl>    | <span data-ttu-id="3be83-186">Wenn kein bevorzugtes Netzwerk verfügbar ist, gibt dieser Wert an, ob die NIC von wzcsvc automatisch so konfiguriert werden soll, dass Sie einem verfügbaren Netzwerk zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-186">If a preferred network is not available, this value indicates whether WZCSVC should automatically configure the NIC to associate to any available network.</span></span><br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <span data-ttu-id="3be83-187"><dt> **Intfctl \_ oidssupp**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-187"><dt>**INTFCTL\_OIDSSUPP** </dt> <dt>0x2000</dt></span></span> </dl> | <span data-ttu-id="3be83-188">Gibt an, ob der NIC-Treiber alle 802,11 OIDs unterstützt, die von wzcsvc benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="3be83-188">Indicates whether the NIC driver supports all the 802.11 OIDs required by WZCSVC to function.</span></span><br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <span data-ttu-id="3be83-189"><dt> **Intfctl \_ volatile**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-189"><dt>**INTFCTL\_VOLATILE** </dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="3be83-190">Gibt an, ob die Dienst Parameter für diese Schnittstelle in der Registrierung aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3be83-190">Indicates whether the service parameters for this interface should be retained in the registry.</span></span> <br/> <span data-ttu-id="3be83-191">Wenn dieser Wert festgelegt ist, sind diese Parameter flüchtig und sollten nicht in der Registrierung aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="3be83-191">If this value is set, then these parameters are volatile and should not be retained in the registry.</span></span><br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <span data-ttu-id="3be83-192"><dt> **Intfctl- \_ Richtlinie**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-192"><dt>**INTFCTL\_POLICY** </dt> <dt>0x0800</dt></span></span> </dl>       | <span data-ttu-id="3be83-193">Gibt an, ob die Dienst Parameter für diese Schnittstelle von einer Gruppenrichtlinie übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="3be83-193">Indicates whether the service parameters for this interface are pushed by a group policy.</span></span><br/> <span data-ttu-id="3be83-194">Wenn dieser Wert festgelegt ist, werden die Dienst Parameter über die Gruppenrichtlinie auf den lokalen Computer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="3be83-194">If this value is set, then the service parameters are pushed to the local computer by group policy.</span></span><br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <span data-ttu-id="3be83-195"><dt>**Intfctl \_ 8021xsupp**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-195"><dt>**INTFCTL\_8021XSUPP**</dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="3be83-196">Gibt an, ob 802.1 x-Unterstützung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3be83-196">Indicates whether 802.1X support is enabled.</span></span><br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="3be83-197">**dwdynflags**</span><span class="sxs-lookup"><span data-stu-id="3be83-197">**dwDynFlags**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-198">Eine Bitmaske dynamischer Flags, die das dynamische (nicht persistente und nicht statische) Verhalten für die Schnittstelle steuern.</span><span class="sxs-lookup"><span data-stu-id="3be83-198">A bitmask of dynamic flags that control the dynamic (non-persistent and non-static) behavior on the interface.</span></span>

<span data-ttu-id="3be83-199">Diese Bits sind nützlich, um dynamische, temporäre Änderungen in der Art und Weise zu initiieren, in der wzcsvc auf die Schnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-199">These bits are useful to trigger dynamic, temporary changes in the way the WZCSVC acts on the interface.</span></span> <span data-ttu-id="3be83-200">Keines dieser Bits wird in der Registrierung persistent gespeichert, sodass die Einstellungen einen Systemneustart oder eine Geräte-und Aktivierungs Sequenz nicht überstehen.</span><span class="sxs-lookup"><span data-stu-id="3be83-200">None of these bits are persisted in the registry, so the settings won't survive a system restart or a device disable and enable sequence.</span></span>

<span data-ttu-id="3be83-201">In der folgenden Tabelle werden die möglichen Bitwerte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3be83-201">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="3be83-202">Wert</span><span class="sxs-lookup"><span data-stu-id="3be83-202">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="3be83-203">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3be83-203">Meaning</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <span data-ttu-id="3be83-204"><dt>**Intfädyn \_ NOSCAN**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-204"><dt>**INTFDYN\_NOSCAN**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="3be83-205">Gibt an, dass wzcsvc nicht verlangen soll, dass die Schnittstelle eine aktive Überprüfung durchführt, sondern stattdessen die zwischengespeicherten Werte im NIC-Treiber verwendet.</span><span class="sxs-lookup"><span data-stu-id="3be83-205">Indicates that the WZCSVC should not request the interface conduct an active scan, but instead use the cached values in the NIC driver.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3be83-206">**DW-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="3be83-206">**dwCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-207">Gibt die Treiberfunktionen an.</span><span class="sxs-lookup"><span data-stu-id="3be83-207">Specifies the driver capabilities.</span></span>



| <span data-ttu-id="3be83-208">Wert</span><span class="sxs-lookup"><span data-stu-id="3be83-208">Value</span></span>                                                                                                                                                                                                                                                         | <span data-ttu-id="3be83-209">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3be83-209">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <span data-ttu-id="3be83-210"><dt>**Intfcap \_ Maximale Verschlüsselungs \_ \_ Maske**</dt> <dt>0x000000ff</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-210"><dt>**INTFCAP\_MAX\_CIPHER\_MASK**</dt> <dt>0x000000ff</dt></span></span> </dl> | <span data-ttu-id="3be83-211">Die unteren Reihenfolge dieser Member wird verwendet, um die maximale Verschlüsselung anzugeben, die unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-211">The lower order bits of this member are used to indicate the maximum encryption that is supported.</span></span> <span data-ttu-id="3be83-212">Mögliche Werte sind einige der Enumerationswerte, die in der **NDIS \_ 802 \_ 11- \_ WEP- \_ Status** Struktur in der Header Datei *ntddndis. h* definiert sind, die in der Windows SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3be83-212">The possible values are some of the enumeration values defined in the **NDIS\_802\_11\_WEP\_STATUS** structure in the *NtDDNdis.h* header file included in the Windows SDK.</span></span><br/> <span data-ttu-id="3be83-213">Der Ndis802 \_ 11verschlüsselungs1aktivierte Wert (2) gibt an, dass WEP unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-213">The Ndis802\_11Encryption1Enabled value (2) indicates that WEP is supported.</span></span> <span data-ttu-id="3be83-214">TKIP und AES werden nicht unterstützt, und ein Übertragungs Schlüssel ist möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3be83-214">TKIP and AES are not supported, and a transmit key may or may not be available.</span></span> <br/> <span data-ttu-id="3be83-215">Der Ndis802 \_ 11verschlüsselungs2aktivierte Wert (9) gibt an, dass TKIP und WEP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3be83-215">The Ndis802\_11Encryption2Enabled value (9) indicates that TKIP and WEP are supported.</span></span> <span data-ttu-id="3be83-216">AES wird nicht unterstützt, und es ist ein Übertragungs Schlüssel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3be83-216">AES is not supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="3be83-217">Der \_ Wert Ndis802 11verschlüsselungs3aktivierte (11) gibt an, dass AES, TKIP und WEP unterstützt werden und ein Übertragungs Schlüssel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3be83-217">The Ndis802\_11Encryption3Enabled value (11) indicates that AES, TKIP, and WEP are supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="3be83-218">"Ndis802 \_ 11verschlüsselungnotsupported (8)" gibt an, dass der WEP-Schlüssel nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-218">The Ndis802\_11EncryptionNotSupported (8) indicates Indicates that the WEP key is not supported.</span></span> <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <span data-ttu-id="3be83-219"><dt>**Intfcap \_ SSN**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-219"><dt>**INTFCAP\_SSN**</dt> <dt>0x00000100</dt></span></span> </dl>                                       | <span data-ttu-id="3be83-220">Gibt die Unterstützung für Simple Secure Network (SSN) an, bei dem es sich um eine Teilmenge von 802.11 i handelt.</span><span class="sxs-lookup"><span data-stu-id="3be83-220">Indicates support for Simple Secure Network (SSN) which is a subset of 802.11i.</span></span> <br/> <span data-ttu-id="3be83-221">Der Verschlüsselungsschlüssel wird von SSN regelmäßig geändert (im Gegensatz zum WEP-Standard (verkabelte äquivalente Datenschutz), in dem ein statischer Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-221">SSN changes the encryption key periodically, as opposed to the WEP (Wired Equivalent Privacy) standard, which uses a static key.</span></span> <span data-ttu-id="3be83-222">Damit SSN funktioniert, sollte die maximal unterstützte Verschlüsselung mindestens TKIP betragen.</span><span class="sxs-lookup"><span data-stu-id="3be83-222">In order for SSN to work, the maximum supported cipher should be at least TKIP.</span></span> <span data-ttu-id="3be83-223">SSN wurde von einem Konsortium von Lieferanten in 2002 als Interims Ansatz entwickelt, um die drahtlose LAN-Sicherheit zu verbessern, während der IEEE 802.11 i-Standard abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3be83-223">SSN was developed by a consortium of vendors in 2002 as an interim approach to improve wireless LAN security while the IEEE 802.11i standard was being completed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <span data-ttu-id="3be83-224"><dt>**Intfcap \_ 80211i**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-224"><dt>**INTFCAP\_80211I**</dt> <dt>0x00000200</dt></span></span> </dl>                              | <span data-ttu-id="3be83-225">Gibt die Unterstützung für den IEEE 802.11 i-Standard an.</span><span class="sxs-lookup"><span data-stu-id="3be83-225">Indicates support for the IEEE 802.11i standard.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="3be83-226">**rdniccapabilitäten**</span><span class="sxs-lookup"><span data-stu-id="3be83-226">**rdNicCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-227">Eine Reihe von Funktionen für 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="3be83-227">A set of capabilities for 802.11i.</span></span>

<span data-ttu-id="3be83-228">Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdniccapabili-** Daten zurück, wenn Sie mit dem INTF Functions-Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird. **\_**</span><span class="sxs-lookup"><span data-stu-id="3be83-228">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdNicCapabilities** data when called with the **INTF\_CAPABILITIES** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="3be83-229">Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **pData** -Member der **\_ rohdatenstruktur** eine **INTF \_ 80211 \_** -Funktionsstruktur.</span><span class="sxs-lookup"><span data-stu-id="3be83-229">If the function call is successful, the **pData** member of the **RAW\_DATA** structure contains an **INTF\_80211\_CAPABILITY** structure.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-230">**rdssid**</span><span class="sxs-lookup"><span data-stu-id="3be83-230">**rdSSID**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-231">Binärdaten, die die derzeit für die Schnittstelle konfigurierte 802,11 SSID enthalten.</span><span class="sxs-lookup"><span data-stu-id="3be83-231">Binary data containing the 802.11 SSID currently configured on the interface.</span></span>

<span data-ttu-id="3be83-232">Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdssid-** Daten zurück, wenn Sie mit dem **INTF \_ SSID** -Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-232">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdSSID** data when called with the **INTF\_SSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="3be83-233">Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **dwdatalen** -Member der **\_ rohdatenstruktur** den **ssidlength** -Member einer **NDIS \_ 802 \_ 11 \_ SSID** -Struktur, und der **pData** -Member der **\_ rohdatenstruktur** enthält den **SSID-** Member einer **NDIS \_ 802 \_ 11 \_ SSID** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3be83-233">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the **SsidLength** member of a **NDIS\_802\_11\_SSID** structure and the **pData** member of the **RAW\_DATA** structure contains the **Ssid** member of a **NDIS\_802\_11\_SSID** structure.</span></span>

<span data-ttu-id="3be83-234">Die Struktur **NDIS \_ 802 \_ 11 \_ SSID** ist in der Header Datei *ntddndis. h* definiert.</span><span class="sxs-lookup"><span data-stu-id="3be83-234">The **NDIS\_802\_11\_SSID** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-235">**rdbssid**</span><span class="sxs-lookup"><span data-stu-id="3be83-235">**rdBSSID**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-236">Binärdaten, die die in der Schnittstelle konfigurierte 802,11 BSSID enthalten.</span><span class="sxs-lookup"><span data-stu-id="3be83-236">Binary data containing the 802.11 BSSID configured on the interface.</span></span>

<span data-ttu-id="3be83-237">Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdbssid-** Daten zurück, wenn Sie mit dem **INTF \_ -BSSID-** Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-237">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSID** data when called with the **INTF\_BSSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="3be83-238">Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **dwdatalen** -Member der **\_ rohdatenstruktur** die Größe einer **NDIS \_ 802 \_ 11-Mac- \_ \_ Adress** Struktur, und der **pData** -Member der **\_ rohdatenstruktur** enthält die **NDIS \_ 802 \_ 11 Mac- \_ \_ Adress** Struktur.</span><span class="sxs-lookup"><span data-stu-id="3be83-238">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the size of an **NDIS\_802\_11\_MAC\_ADDRESS** structure and the **pData** member of the **RAW\_DATA** structure contains the **NDIS\_802\_11\_MAC\_ADDRESS** structure.</span></span>

<span data-ttu-id="3be83-239">Die **Mac- \_ \_ \_ \_ Adressstruktur von NDIS 802 11** ist in der Header Datei *ntddndis. h* definiert.</span><span class="sxs-lookup"><span data-stu-id="3be83-239">The **NDIS\_802\_11\_MAC\_ADDRESS** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-240">**rdbssidlist**</span><span class="sxs-lookup"><span data-stu-id="3be83-240">**rdBSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-241">Binärdaten, die die Liste der BSSIDs enthalten, die zuletzt von wzcsvc abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="3be83-241">Binary data that contains the list of BSSIDs that was last retrieved by WZCSVC.</span></span>

<span data-ttu-id="3be83-242">Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdbssidlist** -Daten zurück, wenn Sie mit dem **INTF \_ bssidlist** -Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-242">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSIDList** data when called with the **INTF\_BSSIDLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="3be83-243">Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **dwdatalen** -Member der **\_ rohdatenstruktur** die Länge des Puffers mit den zurückgegebenen Daten, und der **pData** -Member der **\_ rohdatenstruktur** enthält die **WZC \_ 802 \_ 11- \_ Konfigurations \_ Listen** Struktur.</span><span class="sxs-lookup"><span data-stu-id="3be83-243">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-244">**rdstssidlist**</span><span class="sxs-lookup"><span data-stu-id="3be83-244">**rdStSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-245">Binärdaten, die die Liste der für diese Schnittstelle konfigurierten bevorzugten Netzwerke enthalten.</span><span class="sxs-lookup"><span data-stu-id="3be83-245">Binary data that contains the list of preferred networks configured for this interface.</span></span>

<span data-ttu-id="3be83-246">Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdstssidlist** -Daten zurück, wenn Sie mit dem **INTF \_ preflist** -Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3be83-246">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdStSSIDList** data when called with the **INTF\_PREFLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="3be83-247">Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **dwdatalen** -Member der **\_ rohdatenstruktur** die Länge des Puffers mit den zurückgegebenen Daten, und der **pData** -Member der **\_ rohdatenstruktur** enthält die **WZC \_ 802 \_ 11- \_ Konfigurations \_ Listen** Struktur.</span><span class="sxs-lookup"><span data-stu-id="3be83-247">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

<span data-ttu-id="3be83-248">Wenn eines der bevorzugten Netzwerke zurzeit verbunden ist, wird für den **dwctlflags** -Member der **WZC- \_ WLAN- \_ Konfigurations** Struktur für das Netzwerk das **wzcctl \_ Media \_ Connected** (0x0400) Bit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3be83-248">If one of the preferred networks is currently connected, the **dwCtlFlags** member of the **WZC\_WLAN\_CONFIG** structure for the network will have the **WZCCTL\_MEDIA\_CONNECTED** (0x0400) bit set.</span></span>

</dd> <dt>

<span data-ttu-id="3be83-249">**rdctrldata**</span><span class="sxs-lookup"><span data-stu-id="3be83-249">**rdCtrlData**</span></span>
</dt> <dd>

<span data-ttu-id="3be83-250">Binäre Daten, die mit anderen steuerungflags verwendet werden, wenn zusätzliche Parameter für die Schnittstelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3be83-250">Binary data used with other control flags, when setting additional parameters on the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3be83-251">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3be83-251">Remarks</span></span>

<span data-ttu-id="3be83-252">Die **INTF- \_ Eintrags** Struktur wird von den [**wzcqueryinterface**](wzcqueryinterface.md) -und [**wzkrefreshinterface**](wzcrefreshinterface.md) -Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3be83-252">The **INTF\_ENTRY** structure is used by the [**WZCQueryInterface**](wzcqueryinterface.md) and [**WZCRefreshInterface**](wzcrefreshinterface.md) functions.</span></span>

<span data-ttu-id="3be83-253">Die **\_ Rohdaten** Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3be83-253">The **RAW\_DATA** structure is defined as follows:</span></span>


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



<span data-ttu-id="3be83-254">Der *pData* -Member verweist auf Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="3be83-254">The *pData* member points to binary data.</span></span> <span data-ttu-id="3be83-255">*Dwdatalen* gibt die Anzahl der Bytes an, auf die *pData* verweist.</span><span class="sxs-lookup"><span data-stu-id="3be83-255">The *dwDataLen* indicates the number of bytes pointed by *pData*.</span></span>

> [!Note]  
> <span data-ttu-id="3be83-256">Die Header Datei " *wzcsapi. h* " ist im Windows SDK nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3be83-256">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3be83-257">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3be83-257">Requirements</span></span>



| <span data-ttu-id="3be83-258">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3be83-258">Requirement</span></span> | <span data-ttu-id="3be83-259">Wert</span><span class="sxs-lookup"><span data-stu-id="3be83-259">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3be83-260">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3be83-260">Minimum supported client</span></span><br/> | <span data-ttu-id="3be83-261">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3be83-261">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3be83-262">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3be83-262">Minimum supported server</span></span><br/> | <span data-ttu-id="3be83-263">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3be83-263">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3be83-264">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3be83-264">End of client support</span></span><br/>    | <span data-ttu-id="3be83-265">Windows XP mit SP3</span><span class="sxs-lookup"><span data-stu-id="3be83-265">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="3be83-266">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3be83-266">End of server support</span></span><br/>    | <span data-ttu-id="3be83-267">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3be83-267">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="3be83-268">Header</span><span class="sxs-lookup"><span data-stu-id="3be83-268">Header</span></span><br/>                   | <dl> <span data-ttu-id="3be83-269"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3be83-269"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be83-270">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3be83-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be83-271">**Wzcenumschlag-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="3be83-271">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="3be83-272">**Wzcqueryinterface**</span><span class="sxs-lookup"><span data-stu-id="3be83-272">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="3be83-273">**Wzkrefreshinterface**</span><span class="sxs-lookup"><span data-stu-id="3be83-273">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 




