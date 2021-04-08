---
title: Implementieren In-Band NAP-Unterstützung für EAP-Methoden
description: Kann für EAPHost-EAP-Methoden aktiviert werden, die die Übertragung von Typ-Length-Value-Objekten (TLVS) unterstützen.
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734616"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a><span data-ttu-id="aaa8b-103">Implementieren In-Band NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="aaa8b-103">Implementing In-Band NAP Support for EAP Methods</span></span>

<span data-ttu-id="aaa8b-104">Die Unterstützung für den in-Band- [Netzwerk Zugriffsschutz (Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) , NAP) für eine EAP-Methode kann für EAPHost-EAP-Methoden aktiviert werden, die die Übertragung von TLVS (Type-Value Objects) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-104">In-band [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) support for an EAP method can be enabled for EAPHost EAP methods that support the transmission of type-length-value objects (TLVs).</span></span> <span data-ttu-id="aaa8b-105">Wenn die in-Band-NAP-Unterstützung aktiviert ist, werden NAP-Pakete in EAP-Methoden Paketen transportiert.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-105">When in-band NAP support is enabled, NAP packets are transported inside EAP method packets.</span></span>

<span data-ttu-id="aaa8b-106">Wenn die Out-of-Band-NAP-Unterstützung aktiviert ist, wird der NAP-Austausch ( [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) , SoH) im Gegensatz zu internen EAP-Methoden Paketen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-106">In contrast, when out-of-band NAP support is enabled, the NAP [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) exchange occurs through means other than internal to EAP method packets.</span></span>

<span data-ttu-id="aaa8b-107">Alle TLVS sind Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-107">All TLVs are vendor specific.</span></span>

## <a name="implementing-nap-support-on-eap-peer-methods"></a><span data-ttu-id="aaa8b-108">Implementieren der NAP-Unterstützung für EAP-Peer Methoden</span><span class="sxs-lookup"><span data-stu-id="aaa8b-108">Implementing NAP Support on EAP Peer Methods</span></span>

<span data-ttu-id="aaa8b-109">Die Implementierung der EAP-Peer Methode erhält ein TLV, das das [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH)-Anforderungs-TLV von einem EAP-Server enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-109">The EAP peer method implementation receives a TLV containing the [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) request TLV from an EAP server.</span></span>

<span data-ttu-id="aaa8b-110">Die Implementierung der EAP-Peer Methode übergibt dann den TLV mit der SoH-Anforderung TLV wie folgt an EAPHost.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-110">The EAP peer method implementation then passes the TLV containing the SoH request TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="aaa8b-111">Die EAP-Peer Methoden Implementierung gibt den Aktions Code [**eappeermethodresponseaction**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) Response bei Rückgabe von [**eappeerprocessrequestpacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)an EAPHost zurück.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-111">The EAP peer method implementation returns the action code [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) to EAPHost on return from [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span></span>
-   <span data-ttu-id="aaa8b-112">EAPHost ruft [**eappeergetresponlattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) aus der EAP-Peer Methoden Implementierung auf.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-112">EAPHost calls [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) from the EAP peer method implementation.</span></span> <span data-ttu-id="aaa8b-113">Die Attribute werden im Prozess übermittelt.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-113">The attributes are passed in the process.</span></span>
-   <span data-ttu-id="aaa8b-114">Die Implementierung der EAP-Peer Methode gibt das TLV mit dem SoH-Anforderungs-TLV in [**eappeergetresponmenattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)zurück.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-114">The EAP peer method implementation returns the TLV containing the SoH request TLV in [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes).</span></span> <span data-ttu-id="aaa8b-115">Die Attribute werden im Prozess empfangen.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-115">The attributes are received in the process.</span></span>

<span data-ttu-id="aaa8b-116">Die Implementierung der EAP-Peer Methode erhält wie folgt ein TLV mit einem SoH-TLV von EAPHost.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-116">The EAP peer method implementation receives a TLV containing an SoH TLV from EAPHost as follows.</span></span>

-   <span data-ttu-id="aaa8b-117">EAPHost ruft [**eappeersettresponmenattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) aus der Implementierung der EAP-Peer Methode auf.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-117">EAPHost calls [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) from the EAP peer method implementation.</span></span> <span data-ttu-id="aaa8b-118">**Eappeerltresponlattribute** enthält ein TLV, das ein SoH-TLV enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-118">**EapPeerSetResponseAttributes** contains a TLV that houses an SoH TLV.</span></span>
-   <span data-ttu-id="aaa8b-119">Die Implementierung der EAP-Peer Methode sendet den SoH-TLV an den EAP-Server.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-119">The EAP peer method implementation sends the SoH TLV to the EAP server.</span></span>
-   <span data-ttu-id="aaa8b-120">Die Implementierung der EAP-Peer Methode erhält einen TLV, der einen SoH-Antwort-TLV vom EAP-Server enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-120">The EAP peer method implementation receives a TLV containing an SoH response TLV from the EAP server.</span></span>

<span data-ttu-id="aaa8b-121">Die Implementierung der EAP-Peer Methode übergibt das TLV mit der SoH-Antwort TLV wie folgt an EAPHost.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-121">The EAP peer method implementation passes the TLV containing the SoH response TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="aaa8b-122">Die EAP-Peer Methoden Implementierung gibt den Aktions Code **eappeermethodresponseaction** Response bei Rückgabe von [**eappeerprocessrequestpacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)an EAPHost zurück.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-122">The EAP peer method implementation returns the action code **EapPeerMethodResponseActionRespond** to EAPHost on return from [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span></span>
-   <span data-ttu-id="aaa8b-123">EAPHost ruft [**eappeergetresponlattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) aus den Implementierungen der EAP-Peer Methode auf.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-123">EAPHost calls [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) from the EAP peer method implementations.</span></span> <span data-ttu-id="aaa8b-124">Die [**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) Struktur wird im Prozess übermittelt.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-124">The [**EAP\_ATTRIBUTES**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) structure is passed in the process.</span></span>
-   <span data-ttu-id="aaa8b-125">Die Implementierung der EAP-Peer Methode gibt das TLV zurück, das den SoH-Antwort-TLV in [**eappeerltresponmenattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-125">The EAP peer method implementation returns the TLV containing the SoH response TLV in [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).</span></span>

> [!Note]  
> <span data-ttu-id="aaa8b-126">Der **eaptype** -Member der [**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) Struktur wird immer auf **eateaptlv** festgelegt, und der **pValue** -Member verweist auf das erste Byte des TLV, das die SoH-Antwort TLV enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-126">The **eapType** member of the [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure will always be set to **eatEAPTLV** and the **pValue** member will point to the first byte of the TLV that contains the SoH response TLV.</span></span>

 

### <a name="implementing-nap-support-on-eap-server-methods"></a><span data-ttu-id="aaa8b-127">Implementieren der NAP-Unterstützung für EAP-Server Methoden</span><span class="sxs-lookup"><span data-stu-id="aaa8b-127">Implementing NAP Support on EAP Server Methods</span></span>

<span data-ttu-id="aaa8b-128">Die Implementierung der EAP-Server Methode erstellt ein TLV mit einem SoH-Anforderungs-TLV.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-128">The EAP server method implementation constructs a TLV containing an SoH request TLV.</span></span> <span data-ttu-id="aaa8b-129">Die Implementierung der EAP-Server Methode sendet dieses TLV mit der SoH-Anforderungs-TLV an den EAP-Peer.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-129">The EAP server method implementation sends this TLV containing the SoH Request TLV to the EAP peer.</span></span> <span data-ttu-id="aaa8b-130">Die Implementierung der EAP-Server Methode empfängt den TLV vom EAP-Peer.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-130">The EAP server method implementation receives the TLV from the EAP peer.</span></span>

<span data-ttu-id="aaa8b-131">Die Implementierung der EAP-Server Methode übergibt das TLV mit einem SoH-TLV wie folgt an EAPHost.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-131">The EAP server method implementation passes the TLV containing an SoH TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="aaa8b-132">Die EAP-Server Methoden Implementierung gibt den Aktions Code zurück, der die **EAP- \_ Methoden- \_ Authenticator- \_ Antwort \_** auf EAPHost bei Rückgabe von [**eapmethodauthenticatorreceivepacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)antwortet.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-132">The EAP server method implementation returns the action code **EAP\_METHOD\_AUTHENTICATOR\_RESPONSE\_RESPOND** to EAPHost on return from [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).</span></span>
-   <span data-ttu-id="aaa8b-133">EAPHost ruft [**eapmethodauthenticatorgetattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) aus der Implementierung der EAP-Server Methode auf.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-133">EAPHost calls [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) from the EAP server method implementation.</span></span>
-   <span data-ttu-id="aaa8b-134">Die Implementierung der EAP-Server Methode gibt das TLV mit dem SoH-TLV in [**eapmethodauthenticatorgetattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes)zurück.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-134">The EAP server method implementation returns the TLV containing the SoH TLV in [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).</span></span>

<span data-ttu-id="aaa8b-135">Die Implementierung der EAP-Server Methode erhält wie folgt ein TLV mit einem SoH-Antwort-TLV von EAPHost.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-135">The EAP server method implementation receives a TLV containing an SoH response TLV from EAPHost as follows.</span></span>

-   <span data-ttu-id="aaa8b-136">EAPHost ruft [**eapmethodauthenticatorstattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) aus der Implementierung der EAP-Server Methode auf.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-136">EAPHost calls [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) from the EAP server method implementation.</span></span>
-   <span data-ttu-id="aaa8b-137">Der TLV, der die SoH-Antwort "TLV" enthält, wird in [ **eapmethodauthentionor\tattributes** zurückgegeben.](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)</span><span class="sxs-lookup"><span data-stu-id="aaa8b-137">The TLV containing the SoH response TLV is returned in [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)</span></span>
-   <span data-ttu-id="aaa8b-138">Die Implementierung der EAP-Server Methode sendet den TLV, der die SoH-Antwort TLV enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-138">The EAP server method implementation sends the TLV containing the SoH response TLV.</span></span>

> [!Note]  
> <span data-ttu-id="aaa8b-139">Der **eaptype** -Member der [**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) Struktur wird immer auf **eateaptlv** festgelegt, und der **pValue** -Member verweist auf das erste Byte des TLV, das die SoH-Antwort TLV enthält.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-139">The **eapType** member of the [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure will always be set to **eatEAPTLV** and the **pValue** member will point to the first byte of the TLV that contains the SoH response TLV.</span></span>

 

### <a name="messages"></a><span data-ttu-id="aaa8b-140">Meldungen</span><span class="sxs-lookup"><span data-stu-id="aaa8b-140">Messages</span></span>

<span data-ttu-id="aaa8b-141">Der EAP SoH-TLV wird verwendet, um das SoH-Protokoll für die Übertragung über eine EAP-Methode zu kapseln.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-141">The EAP SoH TLV is used to encapsulate the SoH protocol for transmission via an EAP method.</span></span> <span data-ttu-id="aaa8b-142">Alle EAP SoH-TLVS haben dieselbe Struktur und unterscheiden sich nur hinsichtlich der Nachrichten-ID und des Daten Teils der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="aaa8b-142">All EAP SoH TLVs have the same structure, differing only on the message ID and data portion of the message.</span></span>

<span data-ttu-id="aaa8b-143">Weitere Informationen finden Sie unter [Network Access Protection (NAP)-SoH (Statement of Health)-Nachrichten](https://go.microsoft.com/fwlink/p/?linkid=83918).</span><span class="sxs-lookup"><span data-stu-id="aaa8b-143">For more information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaa8b-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aaa8b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaa8b-145">Konfigurieren der Benutzeroberfläche der EAP-Methode</span><span class="sxs-lookup"><span data-stu-id="aaa8b-145">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="aaa8b-146">Aktivieren von Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="aaa8b-146">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="aaa8b-147">Implementieren der NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="aaa8b-147">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="aaa8b-148">Übertragen von Daten zwischen den Supplicant-und EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="aaa8b-148">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="aaa8b-149">EAPHost-Supplicants</span><span class="sxs-lookup"><span data-stu-id="aaa8b-149">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 