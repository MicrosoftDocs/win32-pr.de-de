---
description: Enthält Informationen zum 802.1 x-Verbindungsprofil, das zurzeit für die 802.1 x-Authentifizierung verwendet wird.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: ONEX_CONNECTION_PROFILE Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356709"
---
# <a name="onex_connection_profile-structure"></a><span data-ttu-id="c4c96-103">Onex- \_ Verbindungs \_ Profil Struktur</span><span class="sxs-lookup"><span data-stu-id="c4c96-103">ONEX\_CONNECTION\_PROFILE structure</span></span>

<span data-ttu-id="c4c96-104">Die **Onex- \_ Verbindungs \_ Profil** Struktur enthält Informationen zum 802.1 x-Verbindungsprofil, das zurzeit für die 802.1 x-Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4c96-104">The **ONEX\_CONNECTION\_PROFILE** structure contains information on the 802.1X connection profile currently used for 802.1X authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4c96-105">Syntax</span></span>


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a><span data-ttu-id="c4c96-106">Member</span><span class="sxs-lookup"><span data-stu-id="c4c96-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4c96-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="c4c96-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-108">Die Version dieser **Onex- \_ Verbindungs \_ Profil** Struktur.</span><span class="sxs-lookup"><span data-stu-id="c4c96-108">The version of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-109">**dwtotallen**</span><span class="sxs-lookup"><span data-stu-id="c4c96-109">**dwTotalLen**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-110">Die Länge dieser **Onex- \_ Verbindungs \_ Profil** Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c4c96-110">The length, in bytes, of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-111">**fonexsupplicantflags**</span><span class="sxs-lookup"><span data-stu-id="c4c96-111">**fOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-112">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwonexsupplicantflags** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-112">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwOneXSupplicantFlags** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-113">**"losupplicantmode"**</span><span class="sxs-lookup"><span data-stu-id="c4c96-113">**fsupplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-114">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **supplicantmode** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-114">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **supplicantMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-115">**"f"**</span><span class="sxs-lookup"><span data-stu-id="c4c96-115">**fauthMode**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-116">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **authmode** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-116">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **authMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-117">**"Gültigkeitsdauer"**</span><span class="sxs-lookup"><span data-stu-id="c4c96-117">**fHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-118">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwheldperiod** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-118">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwHeldPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-119">**Gültigkeitsdauer**</span><span class="sxs-lookup"><span data-stu-id="c4c96-119">**fAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-120">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwauthperiod** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-120">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwAuthPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-121">**Start Zeitraum**</span><span class="sxs-lookup"><span data-stu-id="c4c96-121">**fStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-122">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwstartperiod** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-122">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwStartPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-123">**"f" starten**</span><span class="sxs-lookup"><span data-stu-id="c4c96-123">**fMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-124">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwmaxstart** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-124">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxStart** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-125">**Fehler bei "f"**</span><span class="sxs-lookup"><span data-stu-id="c4c96-125">**fMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-126">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwmaxauthfailure** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-126">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxAuthFailures** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-127">**"f"**</span><span class="sxs-lookup"><span data-stu-id="c4c96-127">**fNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-128">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwnetworkauthtimeout** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-128">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthTimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-129">**"f"-logondialoge**</span><span class="sxs-lookup"><span data-stu-id="c4c96-129">**fAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-130">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **ballowlogondialogs** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-130">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bAllowLogonDialogs** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-131">**"f"**</span><span class="sxs-lookup"><span data-stu-id="c4c96-131">**fNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-132">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwnetworkauthwithuitimeout** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-132">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthWithUITimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-133">**fuserbasedvlan**</span><span class="sxs-lookup"><span data-stu-id="c4c96-133">**fUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-134">Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **buserbasedvlan** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-134">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bUserBasedVLan** member.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-135">**dwonexsupplicantflags**</span><span class="sxs-lookup"><span data-stu-id="c4c96-135">**dwOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-136">Ein Satz von 802.1 x-Flags, die im Profil vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="c4c96-136">A set of 802.1X flags that can be present in the profile.</span></span> <span data-ttu-id="c4c96-137">Diese Flags sind für die interne Verwendung durch das 802.1 x-Authentifizierungs Modul reserviert.</span><span class="sxs-lookup"><span data-stu-id="c4c96-137">These flags are reserved for internal use by the 802.1X authentication module.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-138">**supplicantmode**</span><span class="sxs-lookup"><span data-stu-id="c4c96-138">**supplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-139">Das supplicantmode-Element im 802.1 x-Schema, das die Übertragungsmethode angibt, die für EAPOL-Start Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4c96-139">The supplicantMode element in the 802.1X schema that specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="c4c96-140">Weitere Informationen finden Sie unter dem [**supplicantmode (Onex)-Element**](onexschema-supplicantmode-onex-element.md) im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-140">For more information, see the [**supplicantMode (OneX) Element**](onexschema-supplicantmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="c4c96-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c4c96-141">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="c4c96-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4c96-142">Meaning</span></span>                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <span data-ttu-id="c4c96-143"><dt>**Onexsupplicantmodeinhibittransmission**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c4c96-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="c4c96-144">EAPOL-Start-Nachrichten werden nicht übertragen.</span><span class="sxs-lookup"><span data-stu-id="c4c96-144">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="c4c96-145">Nur für kabelgebundene LAN-profile gültig.</span><span class="sxs-lookup"><span data-stu-id="c4c96-145">Valid for wired LAN profiles only.</span></span><br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <span data-ttu-id="c4c96-146"><dt>**Onexsupplicantmodelearn**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c4c96-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="c4c96-147">Der Client legt fest, wann EAPOL-Start Pakete auf der Grundlage der Netzwerkfunktion gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c4c96-147">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="c4c96-148">EAPOL-Start Meldungen werden nur bei Bedarf gesendet.</span><span class="sxs-lookup"><span data-stu-id="c4c96-148">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="c4c96-149">Nur für kabelgebundene LAN-profile gültig.</span><span class="sxs-lookup"><span data-stu-id="c4c96-149">Valid for wired LAN profiles only.</span></span><br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <span data-ttu-id="c4c96-150"><dt>**Onexsupplicantmodecompliance**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c4c96-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="c4c96-151">EAPOL-Start-Nachrichten werden gemäß 802.1 x übertragen.</span><span class="sxs-lookup"><span data-stu-id="c4c96-151">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="c4c96-152">Gültig für Kabel-und Drahtlos-LAN-Profile.</span><span class="sxs-lookup"><span data-stu-id="c4c96-152">Valid for both wired and wireless LAN profiles.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="c4c96-153">**authmode**</span><span class="sxs-lookup"><span data-stu-id="c4c96-153">**authMode**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-154">Das authmode-Element im 802.1 x-Schema, das den Typ der Anmelde Informationen angibt, die für die 802.1 x-Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4c96-154">The authMode element in the 802.1X schema that specifies the type of credentials used for 802.1X authentication.</span></span> <span data-ttu-id="c4c96-155">Weitere Informationen finden Sie unter dem [**authmode-Element (Onex)**](onexschema-authmode-onex-element.md) im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-155">For more information, see the [**authMode (OneX) Element**](onexschema-authmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="c4c96-156">Wert</span><span class="sxs-lookup"><span data-stu-id="c4c96-156">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="c4c96-157">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4c96-157">Meaning</span></span>                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <span data-ttu-id="c4c96-158"><dt>**Onexauthmodemachineoruser**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c4c96-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="c4c96-159">Verwenden Sie Computer-oder Benutzer Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="c4c96-159">Use machine or user credentials.</span></span> <span data-ttu-id="c4c96-160">Wenn ein Benutzer angemeldet ist, werden die Anmelde Informationen des Benutzers zur Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4c96-160">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="c4c96-161">Wenn kein Benutzer angemeldet ist, werden Computer Anmelde Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4c96-161">When no user is logged on, machine credentials are used.</span></span><br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <span data-ttu-id="c4c96-162"><dt>**Onexauthmodemachineonly**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c4c96-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="c4c96-163">Verwenden Sie nur Computer Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="c4c96-163">Use machine credentials only.</span></span><br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <span data-ttu-id="c4c96-164"><dt>**Onexauthmudeuseronly**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c4c96-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="c4c96-165">Nur Benutzer Anmelde Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4c96-165">Use user credentials only.</span></span><br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <span data-ttu-id="c4c96-166"><dt>**Onexauthmodeguest**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c4c96-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span></span> </dl>                                 | <span data-ttu-id="c4c96-167">Nur Gast Anmelde Informationen (leer) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4c96-167">Use guest (empty) credentials only.</span></span><br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <span data-ttu-id="c4c96-168"><dt>**Onexauthmodeunspezifiziert**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c4c96-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="c4c96-169">Die zu verwendenden Anmelde Informationen wurden nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="c4c96-169">Credentials to use are not specified.</span></span><br/>                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="c4c96-170">**dwheldperiod**</span><span class="sxs-lookup"><span data-stu-id="c4c96-170">**dwHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-171">Das heldperiod-Element im 802.1 x-Schema, das die Zeitdauer in Sekunden angibt, in der ein Client die Authentifizierung nach einem fehlgeschlagenen Authentifizierungs Versuch nicht erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="c4c96-171">The heldPeriod element in the 802.1X schema that specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span> <span data-ttu-id="c4c96-172">Weitere Informationen finden Sie unter dem [**heldperiod-Element (Onex)**](onexschema-heldperiod-onex-element.md) im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-172">For more information, see the [**heldPeriod (OneX) Element**](onexschema-heldperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-173">**dwauthperiod**</span><span class="sxs-lookup"><span data-stu-id="c4c96-173">**dwAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-174">Das authperiod-Element im 802.1 x-Schema, das die maximale Zeitspanne (in Sekunden) angibt, in der ein Client auf eine Antwort vom Authentifikator wartet.</span><span class="sxs-lookup"><span data-stu-id="c4c96-174">The authPeriod element in the 802.1X schema that specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="c4c96-175">Wenn innerhalb des angegebenen Zeitraums keine Antwort empfangen wird, geht der Client davon aus, dass im Netzwerk kein Authentifikator vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c4c96-175">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="c4c96-176">Weitere Informationen finden Sie unter dem [**authperiod-Element (Onex)**](onexschema-authperiod-onex-element.md) im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-176">For more information, see the [**authPeriod (OneX) Element**](onexschema-authperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-177">**dwstartperiod**</span><span class="sxs-lookup"><span data-stu-id="c4c96-177">**dwStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-178">Das startperiod-Element im 802.1 x-Schema, das angibt, wie lange (in Sekunden) gewartet werden soll, bevor eine EAPOL-Start gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4c96-178">The startPeriod element in the 802.1X schema that specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="c4c96-179">Eine EAPOL-Start Nachricht wird gesendet, um den 802.1 x-Authentifizierungsprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="c4c96-179">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span> <span data-ttu-id="c4c96-180">Weitere Informationen finden Sie unter dem [**startperiod-Element (Onex)**](onexschema-startperiod-onex-element.md) im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-180">For more information, see the [**startPeriod (OneX) Element**](onexschema-startperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-181">**dwmaxstart**</span><span class="sxs-lookup"><span data-stu-id="c4c96-181">**dwMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-182">Das maxstart-Element im 802.1 x-Schema, das die maximale Anzahl von EAPOL-Start gesendeten Nachrichten angibt.</span><span class="sxs-lookup"><span data-stu-id="c4c96-182">The maxStart element in the 802.1X schema that specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="c4c96-183">Nachdem die maximale Anzahl von EAPOL-Start-Nachrichten gesendet wurde, nimmt der Client an, dass im Netzwerk kein Authentifikator vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c4c96-183">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="c4c96-184">Weitere Informationen finden Sie unter dem [**maxstart (Onex)-Element**](onexschema-maxstart-onex-element.md) im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-184">For more information, see the [**maxStart (OneX) Element**](onexschema-maxstart-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-185">**dwmaxauthfailure**</span><span class="sxs-lookup"><span data-stu-id="c4c96-185">**dwMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-186">Das maxauthfailure-Element im 802.1 x-Schema, das die maximale Anzahl von Authentifizierungs Fehlern angibt, die für einen Satz von Anmelde Informationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c4c96-186">The maxAuthFailures element in the 802.1X schema that specifies the maximum number of authentication failures allowed for a set of credentials.</span></span> <span data-ttu-id="c4c96-187">Weitere Informationen finden Sie unter dem [**maxauthfailure (Onex)**](onexschema-maxauthfailures-onex-element.md) -Element im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-187">For more information, see the [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-188">**dwnetworkauthtimeout**</span><span class="sxs-lookup"><span data-stu-id="c4c96-188">**dwNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-189">Die Zeit in Sekunden, für die auf den Abschluss der 802.1 x-Authentifizierung gewartet werden soll, bevor die normale Anmeldung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c4c96-189">The time, in seconds, to wait for 802.1X authentication completion before normal logon proceeds.</span></span> <span data-ttu-id="c4c96-190">Dieser Wert wird in Szenarien mit einmaligem Anmelden (Single Sign-on, SSO) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4c96-190">This value is used in single signon (SSO) scenarios.</span></span> <span data-ttu-id="c4c96-191">Der Standardwert ist 10 Sekunden in einem 802.1 x-Profil.</span><span class="sxs-lookup"><span data-stu-id="c4c96-191">This value defaults to 10 seconds in an 802.1X profile.</span></span> <span data-ttu-id="c4c96-192">Weitere Informationen finden Sie unter dem [**MaxDelay-Element (SingleSignOn)**](onexschema-maxdelay-singlesignon-element.md) im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-192">For more information, see the [**maxDelay (singleSignOn) Element**](onexschema-maxdelay-singlesignon-element.md) in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-193">**dwnetworkauthwithuitimeout**</span><span class="sxs-lookup"><span data-stu-id="c4c96-193">**dwNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-194">Die maximale Dauer (in Sekunden), die auf eine Verbindung gewartet werden soll, falls ein Benutzeroberflächen Dialogfeld, das eine Benutzereingabe erfordert, während des einmaligen Anmeldens pro Anmeldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4c96-194">The maximum duration time, in seconds, to wait for a connection in case a user interface dialog box that requires user input is displayed during the per-logon SSO.</span></span>

<span data-ttu-id="c4c96-195">Unter Windows Vista mit SP1 und höher ist dieser Wert in 10 Minuten hart codiert und kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c4c96-195">On Windows Vista with SP1 and later, this value is hardcoded to 10 minutes and is not configurable.</span></span> <span data-ttu-id="c4c96-196">In Windows Vista Release to Manufacturing ist dieser Wert standardmäßig auf 60 Sekunden in einem 802.1 x-Profil festgelegt und wurde vom Element **maxdelaywithadditionaldialoge** im Schema gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c4c96-196">On Windows Vista Release to Manufacturing, this value defaults to 60 seconds in an 802.1X profile and was controlled by the **maxDelayWithAdditionalDialogs** element in the schema.</span></span>

<span data-ttu-id="c4c96-197">Unter Windows Vista mit SP1 und höher wird das **maxdelaywithadditionaldialogs** -Element im 802.1 x-Schema ignoriert und als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="c4c96-197">On Windows Vista with SP1 and later, the **maxDelayWithAdditionalDialogs** element in the 802.1X schema is ignored and deprecated.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-198">**ballowlogondialogfelder**</span><span class="sxs-lookup"><span data-stu-id="c4c96-198">**bAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-199">Ein-Wert, der angibt, ob EAP-Dialoge bei Verwendung des einmaligen Anmeldens von SSO angezeigt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="c4c96-199">A value that specifies whether to allow EAP dialogs to be displayed when using pre-logon SSO.</span></span> <span data-ttu-id="c4c96-200">Weitere Informationen finden Sie unter dem **allowadditionaldialogs** -Element im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-200">For more information, see the **allowAdditionalDialogs** element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="c4c96-201">**buserbasedvlan**</span><span class="sxs-lookup"><span data-stu-id="c4c96-201">**bUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="c4c96-202">Das userbasedvirtuallan-Element im 802.1 x-Schema, das angibt, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c4c96-202">The userBasedVirtualLan element in the 802.1X schema that specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="c4c96-203">Einige Netzwerk Zugriffs Server-Geräte (NAS) ändern das VLAN, nachdem sich ein Benutzer authentifiziert hat.</span><span class="sxs-lookup"><span data-stu-id="c4c96-203">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="c4c96-204">Wenn userbasedvirtuallan den Wert true hat, kann der NAS das VLAN eines Geräts ändern, nachdem sich ein Benutzer authentifiziert hat.</span><span class="sxs-lookup"><span data-stu-id="c4c96-204">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span> <span data-ttu-id="c4c96-205">Weitere Informationen finden Sie unter dem [**userbasedvirtuallan (SingleSignOn)-Element**](onexschema-userbasedvirtuallan-singlesignon-element.md) im 802.1 x-Schema.</span><span class="sxs-lookup"><span data-stu-id="c4c96-205">For more information, see the [**userBasedVirtualLan (singleSignOn) Element**](onexschema-userbasedvirtuallan-singlesignon-element.md) in the 802.1X scheme.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4c96-206">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4c96-206">Remarks</span></span>

<span data-ttu-id="c4c96-207">Die **Onex- \_ Verbindungs \_ Profil** Struktur wird vom 802.1 x-Modul verwendet, eine neue drahtlos Konfigurationskomponente, die unter Windows Vista und höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c4c96-207">The **ONEX\_CONNECTION\_PROFILE** structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and later.</span></span>

<span data-ttu-id="c4c96-208">Die [**Onex- \_ Ergebnis \_ Aktualisierungs \_ Daten**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) enthalten Informationen zu einer Statusänderung in der 802.1 x-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="c4c96-208">The [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contains information on a status change to 802.1X authentication.</span></span> <span data-ttu-id="c4c96-209">Die **Datenstruktur der Onex- \_ Ergebnis \_ \_ Aktualisierung** wird zurückgegeben, wenn der **notificationsource** -Member der [**WLAN- \_ Benachrichtigungs \_ Daten**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) Struktur die **WLAN- \_ Benachrichtigungs \_ Quelle \_ Onex** und der **notificationcode** -Member der **WLAN- \_ Benachrichtigungs \_ Daten** Struktur für die empfangene Benachrichtigung **onexnotificationtyperesultupdate** ist.</span><span class="sxs-lookup"><span data-stu-id="c4c96-209">The **ONEX\_RESULT\_UPDATE\_DATA** structure is returned when the **NotificationSource** member of the [**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) structure is **WLAN\_NOTIFICATION\_SOURCE\_ONEX** and the **NotificationCode** member of the **WLAN\_NOTIFICATION\_DATA** structure for received notification is **OneXNotificationTypeResultUpdate**.</span></span> <span data-ttu-id="c4c96-210">Für diese Benachrichtigung verweist der **pData** -Member der **WLAN- \_ Benachrichtigungs \_ Daten** Struktur auf eine Datenstruktur des **Onex- \_ Ergebnis \_ Updates \_** , die Informationen über die 802.1 x-Authentifizierungs Statusänderung enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c96-210">For this notification, the **pData** member of the **WLAN\_NOTIFICATION\_DATA** structure points to an **ONEX\_RESULT\_UPDATE\_DATA** structure that contains information on the 802.1X authentication status change.</span></span>

<span data-ttu-id="c4c96-211">Wenn das Element " **fonexauthparser** " in der Datenstruktur der [**Onex- \_ Ergebnis \_ Aktualisierung \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) festgelegt ist, enthält das **authparameams** -Element der Datenstruktur des **Onex- \_ Ergebnis \_ \_ Updates** eine [**Onex-Variablen- \_ \_ BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) -Struktur mit einer eingebetteten [**Onex \_ auth \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) -Parameter Struktur, beginnend beim **dwOffset** -Member des **Onex- \_ Variablen- \_ BLOB**.</span><span class="sxs-lookup"><span data-stu-id="c4c96-211">If the **fOneXAuthParams** member in the [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) structure is set, then the **authParams** member of the **ONEX\_RESULT\_UPDATE\_DATA** structure contains an [**ONEX\_VARIABLE\_BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) structure with an [**ONEX\_AUTH\_PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span> <span data-ttu-id="c4c96-212">Der **onexconfiguration profile** -Member der **Onex \_ auth \_** -Parameter Struktur enthält eine **Onex- \_ Variablen- \_ BLOB** -Struktur mit einer eingebetteten **Onex- \_ Verbindungs \_ Profil** Struktur, beginnend beim **dwOffset** -Member des **Onex- \_ \_ variablenblobs**.</span><span class="sxs-lookup"><span data-stu-id="c4c96-212">The **oneXConnProfile** member of the **ONEX\_AUTH\_PARAMS** structure contains an **ONEX\_VARIABLE\_BLOB** structure with an **ONEX\_CONNECTION\_PROFILE** structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span>

<span data-ttu-id="c4c96-213">Die **Onex- \_ Verbindungs \_ Profil** Struktur ist nicht in einer öffentlichen Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="c4c96-213">The **ONEX\_CONNECTION\_PROFILE** structure is not defined in a public header file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c96-214">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4c96-214">Requirements</span></span>



| <span data-ttu-id="c4c96-215">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4c96-215">Requirement</span></span> | <span data-ttu-id="c4c96-216">Wert</span><span class="sxs-lookup"><span data-stu-id="c4c96-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c4c96-217">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4c96-217">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c96-218">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4c96-218">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c4c96-219">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4c96-219">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c96-220">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4c96-220">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4c96-221">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4c96-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c96-222">Informationen zur ACM-Architektur</span><span class="sxs-lookup"><span data-stu-id="c4c96-222">About the ACM Architecture</span></span>](about-the-acm-architecture.md)
</dt> <dt>

[<span data-ttu-id="c4c96-223">Onex-Schema</span><span class="sxs-lookup"><span data-stu-id="c4c96-223">OneX Schema</span></span>](onexschema-schema.md)
</dt> <dt>

[<span data-ttu-id="c4c96-224">**authmode-Element (Onex)**</span><span class="sxs-lookup"><span data-stu-id="c4c96-224">**authMode (OneX) Element**</span></span>](onexschema-authmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="c4c96-225">**authperiod-Element (Onex)**</span><span class="sxs-lookup"><span data-stu-id="c4c96-225">**authPeriod (OneX) Element**</span></span>](onexschema-authperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="c4c96-226">**heldperiod-Element (Onex)**</span><span class="sxs-lookup"><span data-stu-id="c4c96-226">**heldPeriod (OneX) Element**</span></span>](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="c4c96-227">**maxauthfailure (Onex)**</span><span class="sxs-lookup"><span data-stu-id="c4c96-227">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[<span data-ttu-id="c4c96-228">**maxstart (Onex)-Element**</span><span class="sxs-lookup"><span data-stu-id="c4c96-228">**maxStart (OneX) Element**</span></span>](onexschema-maxstart-onex-element.md)
</dt> <dt>

[<span data-ttu-id="c4c96-229">**startperiod (Onex)-Element**</span><span class="sxs-lookup"><span data-stu-id="c4c96-229">**startPeriod (OneX) Element**</span></span>](onexschema-startperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="c4c96-230">**supplicantmode-Element (Onex)**</span><span class="sxs-lookup"><span data-stu-id="c4c96-230">**supplicantMode (OneX) Element**</span></span>](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="c4c96-231">**userbasedvirtuallan (SingleSignOn)-Element**</span><span class="sxs-lookup"><span data-stu-id="c4c96-231">**userBasedVirtualLan (singleSignOn) Element**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[<span data-ttu-id="c4c96-232">**Onex \_ auth-Parameter \_**</span><span class="sxs-lookup"><span data-stu-id="c4c96-232">**ONEX\_AUTH\_PARAMS**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[<span data-ttu-id="c4c96-233">**Onex \_ - \_ Benachrichtigungstyp**</span><span class="sxs-lookup"><span data-stu-id="c4c96-233">**ONEX\_NOTIFICATION\_TYPE**</span></span>](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[<span data-ttu-id="c4c96-234">**Onex- \_ Ergebnis \_ Aktualisierungs \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="c4c96-234">**ONEX\_RESULT\_UPDATE\_DATA**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[<span data-ttu-id="c4c96-235">**Onex-Schema Element**</span><span class="sxs-lookup"><span data-stu-id="c4c96-235">**OneX Schema Element**</span></span>](onexschema-onex-element.md)
</dt> <dt>

[<span data-ttu-id="c4c96-236">**Onex \_ - \_ variablenblob**</span><span class="sxs-lookup"><span data-stu-id="c4c96-236">**ONEX\_VARIABLE\_BLOB**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

<span data-ttu-id="c4c96-237">[**WLAN- \_ Benachrichtigungs \_ Daten**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4c96-237">[**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c4c96-238">**Wlanregisternotification**</span><span class="sxs-lookup"><span data-stu-id="c4c96-238">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
