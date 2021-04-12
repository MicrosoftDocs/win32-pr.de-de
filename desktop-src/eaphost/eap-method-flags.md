---
title: EAP-methodenflags (eaptypes. h)
description: Die EAP-methodenflags werden innerhalb der Supplicant-, Authenticator-und Peer Funktionen verwendet, um das Verhalten einer EAP-Authentifizierungs Sitzung anzugeben.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475021"
---
# <a name="eap-method-flags"></a><span data-ttu-id="6b2ed-103">EAP-methodenflags</span><span class="sxs-lookup"><span data-stu-id="6b2ed-103">EAP Method Flags</span></span>

<span data-ttu-id="6b2ed-104">Die EAP-methodenflags werden innerhalb der Supplicant-, Authenticator-und Peer Funktionen verwendet, um das Verhalten einer EAP-Authentifizierungs Sitzung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-104">The EAP method flags are used within the supplicant, authenticator, and peer functions to specify behaviors of an EAP authentication session.</span></span>

<dl> <dt>

<span data-ttu-id="6b2ed-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP- \_ Flag \_ "reserved1"**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP\_FLAG\_Reserved1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6b2ed-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-107">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-107">Do not use.</span></span> <span data-ttu-id="6b2ed-108">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-108">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP- \_ Flag \_ nicht \_ interaktiv**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP\_FLAG\_NON\_INTERACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6b2ed-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-111">Zeigen Sie keine Benutzeroberfläche (UI) an.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-111">Do not display a user interface (UI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP- \_ Flag- \_ Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP\_FLAG\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-113">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6b2ed-113">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-114">Benutzerdaten wurden von der Windows-Anmeldung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-114">User data was obtained from Windows logon.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP- \_ Flag ( \_ Vorschau)**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP\_FLAG\_PREVIEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-116">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6b2ed-116">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-117">Anmelde Informationen-Benutzeroberfläche vor der Authentifizierung anzeigen, auch wenn zwischengespeicherte Anmelde Informationen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-117">Show credentials UI before authenticating, even if cached credentials are present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ Flag \_ "reserved2"**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span> **EAP\_FLAG\_Reserved2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b2ed-119">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-120">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-120">Do not use.</span></span> <span data-ttu-id="6b2ed-121">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-121">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP- \_ Flag für \_ Computer Authentifizierung \_**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP\_FLAG\_MACHINE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-123">0x00000020</span><span class="sxs-lookup"><span data-stu-id="6b2ed-123">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-124">Authentifizierung auf Computer Ebene verwenden; Wenn dieses Flag nicht festgelegt wird, wird die Authentifizierung auf Benutzerebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-124">Use machine level authentication; not setting this flag indicates user level authentication is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP- \_ Flag für \_ Gast \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP\_FLAG\_GUEST\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="6b2ed-126">0x00000040</span><span class="sxs-lookup"><span data-stu-id="6b2ed-126">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-127">Gibt eine Anforderung zum Bereitstellen des Gast Zugriffs an.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-127">Indicates a request to provide guest access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP- \_ Flag \_ "reserved3"**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP\_FLAG\_Reserved3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-129">0x00000080</span><span class="sxs-lookup"><span data-stu-id="6b2ed-129">0x00000080</span></span> 
</dt> <dt>



<span data-ttu-id="6b2ed-130">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-130">Do not use.</span></span> <span data-ttu-id="6b2ed-131">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-131">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ Flag \_ "reserved4"**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span> **EAP\_FLAG\_Reserved4**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-133">0x00000100</span><span class="sxs-lookup"><span data-stu-id="6b2ed-133">0x00000100</span></span> 
</dt> <dt>



<span data-ttu-id="6b2ed-134">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-134">Do not use.</span></span> <span data-ttu-id="6b2ed-135">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-135">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP-Flag fortsetzen \_ \_ \_ aus \_ Ruhezustand**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP\_FLAG\_RESUME\_FROM\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-137">0x00000200</span><span class="sxs-lookup"><span data-stu-id="6b2ed-137">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-138">Gibt an, dass dies der erste Rückruf ist, nachdem die Computeraktivität von einem Ruhezustand wieder aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-138">Indicates this is the first call after machine activity has resumed from a period of hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ Flag \_ Reserved5**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span> **EAP\_FLAG\_Reserved5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-140">0x00000400</span><span class="sxs-lookup"><span data-stu-id="6b2ed-140">0x00000400</span></span> 
</dt> <dt>



<span data-ttu-id="6b2ed-141">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-141">Do not use.</span></span> <span data-ttu-id="6b2ed-142">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-142">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP- \_ Flag \_ Reserved6**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP\_FLAG\_Reserved6**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-144">0x00000800</span><span class="sxs-lookup"><span data-stu-id="6b2ed-144">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-145">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-145">Do not use.</span></span> <span data-ttu-id="6b2ed-146">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-146">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP- \_ Flag für \_ vollständige \_ Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP\_FLAG\_FULL\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-148">0x00001000</span><span class="sxs-lookup"><span data-stu-id="6b2ed-148">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-149">Gibt an, dass Tunnel Methoden eine vollständige Authentifizierung anstelle einer abgekürzten Version durchführen sollen, z. b. eine [schnelle erneute Verbindungs Herstellung zwischen geschütztem EAP (PEAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6b2ed-149">Indicates that tunnel methods should perform a full authentication instead of an abbreviated version, such as [Protected EAP (PEAP) Fast Reconnect](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP- \_ Flag \_ bevorzugt alt- \_ \_ Anmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP\_FLAG\_PREFER\_ALT\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="6b2ed-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-152">Gibt an, dass an [**eappeerbeginsession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) weiter gegebene Anmelde Informationen allen anderen Formen des Abrufs von Anmelde Informationen bevorzugt werden, auch wenn Konfigurationsdaten, die an die aktuelle Funktion weitergegeben werden, einen anderen Modus zum Abrufen von Anmelde Informationen anfordern.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-152">Indicates credentials passed into [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) are preferred to all other forms of credential retrieval, even if configuration data passed into the current function requests a different mode of credential retrieval.</span></span>

> [!Note]  
> <span data-ttu-id="6b2ed-153">Dieses Flag wird nur von [**eappeerbeginsession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-153">This flag is only used by [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP- \_ Flag \_ Reserved7**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP\_FLAG\_Reserved7**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-155">0x00004000</span><span class="sxs-lookup"><span data-stu-id="6b2ed-155">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-156">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-156">Do not use.</span></span> <span data-ttu-id="6b2ed-157">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-157">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**Integritäts \_ \_ \_ \_ Status \_ Änderung des EAP-Peer Flags**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**EAP\_PEER\_FLAG\_HEALTH\_STATE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-159">0x00008000</span><span class="sxs-lookup"><span data-stu-id="6b2ed-159">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-160">Gibt an, dass die erneute Authentifizierung ein NAP-Rückruf ( [Network Access Protection, Netzwerk Zugriffsschutz](/windows/desktop/NAP/network-access-protection-start-page) ) ist. NAP hat die Authentifizierungs Sitzung initiiert, weil sich der Integritäts Status geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-160">Indicates the cause of re-authentication is a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) callback; NAP initiated the authentication session because the health state changed.</span></span> <span data-ttu-id="6b2ed-161">Dieses Flag muss nur gesendet werden, wenn diese Funktion von einem NAP-spezifischen [*notificationhandler*](/previous-versions/windows/desktop/api) -Rückruf aufgerufen wird, der von einem vorherigen Aufruf dieser Funktion bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-161">This flag must be sent only when this function is called by a NAP-specific [*NotificationHandler*](/previous-versions/windows/desktop/api) callback provided by a previous call to this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP- \_ Flag " \_ Supress" \_**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP\_FLAG\_SUPRESS\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-163">0x00010000</span><span class="sxs-lookup"><span data-stu-id="6b2ed-163">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-164">Setzen Sie die Authentifizierung mit verfügbaren Informationen fort.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-164">Continue authentication with available information.</span></span> <span data-ttu-id="6b2ed-165">Wenn die Authentifizierung nicht fortgesetzt werden kann, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-165">If the authentication cannot proceed then fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP- \_ Flag \_ vor der \_ Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP\_FLAG\_PRE\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-167">0x00020000</span><span class="sxs-lookup"><span data-stu-id="6b2ed-167">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-168">Gibt an, dass EAPHost einmaliges Anmelden (Single-Sign-on, SSO) bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-168">Indicates that EAPHost should provide Single-Sign-On (SSO).</span></span> <span data-ttu-id="6b2ed-169">Weitere Informationen finden Sie unter [SSO und PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="6b2ed-169">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP- \_ Flag \_ Benutzerauthentifizierung \_**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP\_FLAG\_USER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-171">0x00040000</span><span class="sxs-lookup"><span data-stu-id="6b2ed-171">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-172">Gibt die Authentifizierung auf Benutzerebene für Legacy Methoden an, die die Authentifizierung des **EAP- \_ Flag \_ \_** nicht festlegen können.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-172">Indicates user level authentication for legacy methods that cannot set **EAP\_FLAG\_MACHINE\_AUTH**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP- \_ Flag " \_ confg" (schreibgeschützt) \_**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP\_FLAG\_CONFG\_READONLY**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="6b2ed-174">0x00080000</span><span class="sxs-lookup"><span data-stu-id="6b2ed-174">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-175">Gibt an, dass die Konfiguration angezeigt, aber nicht aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-175">Indicates the configuration can be viewed but not updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b2ed-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP- \_ Flag \_ Reserved8**</span><span class="sxs-lookup"><span data-stu-id="6b2ed-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP\_FLAG\_Reserved8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2ed-177">0x00100000</span><span class="sxs-lookup"><span data-stu-id="6b2ed-177">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="6b2ed-178">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-178">Do not use.</span></span> <span data-ttu-id="6b2ed-179">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6b2ed-179">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b2ed-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b2ed-180">Requirements</span></span>



| <span data-ttu-id="6b2ed-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b2ed-181">Requirement</span></span> | <span data-ttu-id="6b2ed-182">Wert</span><span class="sxs-lookup"><span data-stu-id="6b2ed-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2ed-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b2ed-183">Minimum supported client</span></span><br/> | <span data-ttu-id="6b2ed-184">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b2ed-184">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b2ed-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b2ed-185">Minimum supported server</span></span><br/> | <span data-ttu-id="6b2ed-186">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b2ed-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b2ed-187">Header</span><span class="sxs-lookup"><span data-stu-id="6b2ed-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b2ed-188"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b2ed-188"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b2ed-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b2ed-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2ed-190">Allgemeine EAPHost-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6b2ed-190">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

