---
title: Übertragen von Daten zwischen den Supplicant-und EAP-Methoden
description: Weitere Informationen zum Übertragen von Daten zwischen den Supplicant-und EAP-Methoden. Das Übertragen von Daten zwischen Methoden erfolgt mithilfe von EAP-Attributen.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391026"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a><span data-ttu-id="b4b03-104">Übertragen von Daten zwischen den Supplicant-und EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="b4b03-104">Transferring Data Between the Supplicant and EAP Methods</span></span>

<span data-ttu-id="b4b03-105">Die Verwendung von EAP-Attributen ermöglicht das Austauschen von Daten zwischen Supplicants und EAP-Methoden.</span><span class="sxs-lookup"><span data-stu-id="b4b03-105">Using EAP attributes allows data to be exchanged between supplicants and EAP methods.</span></span>

## <a name="attribute-consumption"></a><span data-ttu-id="b4b03-106">Attribut Verbrauch</span><span class="sxs-lookup"><span data-stu-id="b4b03-106">Attribute Consumption</span></span>

<span data-ttu-id="b4b03-107">[**Eaphostpeerbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) verwendet EAP-Attribute, die direkt an die konfigurierte EAP-Methode übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="b4b03-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consumes EAP attributes that are passed directly to the configured EAP method.</span></span> <span data-ttu-id="b4b03-108">Ebenso können EAP-Methoden einen Aktions Code zurückgeben, der dem Supplicant angibt, dass Attribute verfügbar sind, und dass die Attribute mithilfe von [**eaphostpeergetresponseattribute**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes)erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4b03-108">Similarly, EAP methods are free to return an action code that indicates to the supplicant that attributes are available and that it should collect the attributes using [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span></span>

<span data-ttu-id="b4b03-109">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="b4b03-109">For more information, see the following topics.</span></span>

-   <span data-ttu-id="b4b03-110">Der [EAP-Peer-Supplicant-Aktions Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="b4b03-110">[EAP Peer Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="b4b03-111">[Grund Codes der EAP-Peer Supplicant](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span><span class="sxs-lookup"><span data-stu-id="b4b03-111">[EAP Peer Supplicant Reason Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span></span>
-   <span data-ttu-id="b4b03-112">[Aktions Codes der EAP-Authenticator-Methode](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span><span class="sxs-lookup"><span data-stu-id="b4b03-112">[EAP Authenticator Method Action Codes](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span></span>

<span data-ttu-id="b4b03-113">Supplicants wird erwartet, dass Attribute ignoriert werden, auf die Sie nicht reagieren oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b4b03-113">Supplicants are expected to ignore attributes that they do not recognize or cannot act upon.</span></span> <span data-ttu-id="b4b03-114">Bei Verwendung von [**eaphostpeerablattribute**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) werden diese ignorierten Attribute zurück an EAPHost und die EAP-Methode gesendet.</span><span class="sxs-lookup"><span data-stu-id="b4b03-114">Using [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) these ignored attributes are sent back to EAPHost and the EAP method.</span></span>

## <a name="vendor-specific-attributes"></a><span data-ttu-id="b4b03-115">Anbieterspezifische Attribute</span><span class="sxs-lookup"><span data-stu-id="b4b03-115">Vendor Specific Attributes</span></span>

<span data-ttu-id="b4b03-116">Durch die Verwendung des anbieterspezifischen EAP-Attributs können EAP-Methoden und Supplicants den Datenaustausch zu einem bestimmten Zweck einbinden.</span><span class="sxs-lookup"><span data-stu-id="b4b03-116">By using the vendor-specific EAP attribute, EAP methods and supplicants can engage in data exchange for a specific purpose.</span></span> <span data-ttu-id="b4b03-117">Anbieterspezifische Attribute werden von Supplicants und Methoden ignoriert, die das herstellerspezifische Attribut nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b4b03-117">Vendor-specific attributes are ignored by supplicants and methods that do not support the vendor-specific attribute.</span></span>

<span data-ttu-id="b4b03-118">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="b4b03-118">For more information, see the following topics.</span></span>

-   <span data-ttu-id="b4b03-119">[EAP-Attribute](about-eap-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b4b03-119">[EAP Attributes](about-eap-attributes.md).</span></span>
-   <span data-ttu-id="b4b03-120">[**EAP \_ \_Attributtyp**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span><span class="sxs-lookup"><span data-stu-id="b4b03-120">[**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4b03-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4b03-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4b03-122">Konfigurieren der Benutzeroberfläche der EAP-Methode</span><span class="sxs-lookup"><span data-stu-id="b4b03-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="b4b03-123">Aktivieren von Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b4b03-123">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="b4b03-124">Implementieren In-Band NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="b4b03-124">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="b4b03-125">Implementieren der NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="b4b03-125">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="b4b03-126">EAPHost-Supplicants</span><span class="sxs-lookup"><span data-stu-id="b4b03-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




