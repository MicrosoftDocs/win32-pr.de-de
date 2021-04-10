---
title: SSO EAP-TLS Pin Caching-Verhalten
description: Bietet eine Schritt-für-Schritt-Anleitung zur Behebung von Problemen bei der Sitzungs Wiederaufnahme und erneuten Authentifizierung eines Roamingbenutzers in einer SSO-EAP-TLS-Umgebung.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7c4e3058598f98327570fbcd0347cfb84e5825
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101122"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="eff2c-103">SSO EAP-TLS Pin Caching-Verhalten</span><span class="sxs-lookup"><span data-stu-id="eff2c-103">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="eff2c-104">Dieses Thema enthält eine schrittweise Anleitung zur Behebung von Problemen bei der Sitzungs Wiederaufnahme und erneuten Authentifizierung eines Roamingbenutzers in einer SSO-EAP-TLS-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="eff2c-104">This topic provides a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="eff2c-105">Schritt-für-Schritt-Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="eff2c-105">Step-By-Step Approach</span></span>

<span data-ttu-id="eff2c-106">Die folgende Liste enthält eine schrittweise Vorgehensweise zur Behebung von Problemen bei der Sitzungs Wiederaufnahme und erneuten Authentifizierung eines Roamingbenutzers in einer SSO-EAP-TLS-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="eff2c-106">The following list represents a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

-   <span data-ttu-id="eff2c-107">Nach der ersten erfolgreichen Authentifizierung in einer SSO-Umgebung mit EAP-TLS behält der Supplicant standardmäßig alle Benutzer Anmelde Informationen im Zusammenhang mit.</span><span class="sxs-lookup"><span data-stu-id="eff2c-107">After the first successful authentication in an SSO environment with EAP-TLS, the supplicant retains all user credential related information by default.</span></span>
    > [!Note]  
    > <span data-ttu-id="eff2c-108">Obwohl die jeweilige Supplicant-Implementierung unterliegt, empfiehlt es sich, die gesamte [**EAP- \_ config- \_ Eingabe \_ Feld Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur beizubehalten, die vom Supplicant zuletzt im [**eaphostpeerqueryuserblobfromdedentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) -aufrufeaphost verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="eff2c-108">Although subject to the particular supplicant implementation, it's advisable for the supplicant to retain the entire [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure that the supplicant last used in the [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) call to EAPHost.</span></span>

     

-   <span data-ttu-id="eff2c-109">Wenn der Benutzer zum ersten Mal wechselt und die erneute Authentifizierung beginnt, ruft der Supplicant [**eaphostpeerqueryuserblobfromkredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) erneut mit der gleichen [**EAP- \_ Konfigurations \_ Eingabefeld- \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) Struktur auf. der Supplicant muss auch denselben benutzerblob übergeben, der nach der ersten erfolgreichen Authentifizierung aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="eff2c-109">As the user first roams and the re-authentication begins, the supplicant calls [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) again with the same [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure; the supplicant must also pass in the same user BLOB retained after the first successful authentication.</span></span>
-   <span data-ttu-id="eff2c-110">EAPHost übergibt dann die Informationen im benutzerblob an die EAP-Methode.</span><span class="sxs-lookup"><span data-stu-id="eff2c-110">EAPHost then passes the information in the user BLOB to the EAP method.</span></span>
-   <span data-ttu-id="eff2c-111">Die EAP-Methode aktualisiert wiederum das benutzerblob mit Anmelde Informationsfeldern (z. b. in *peapconfiginputfieldarray*) und behält die restlichen Werte bei, z. b. das Serverzertifikat, wie es im ursprünglichen benutzerblob war.</span><span class="sxs-lookup"><span data-stu-id="eff2c-111">The EAP method in turn updates the user BLOB with credential fields - the PIN for example - provided in *pEapConfigInputFieldArray*, and keeps the remaining values - the server certificate for example - as it was in the original user BLOB.</span></span>
-   <span data-ttu-id="eff2c-112">Nachdem Sie diese Schritte ausgeführt haben, kann der Supplicant die Authentifizierung auf normale Weise fortsetzen, indem die [**eaphostpeer-BeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) -Lauf Zeitfunktion mit diesem benutzerblob aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="eff2c-112">After completing these steps, the supplicant can resume authentication in a normal way by calling the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) run-time function with this user BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eff2c-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eff2c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eff2c-114">SSO-EAPHost-Szenarios</span><span class="sxs-lookup"><span data-stu-id="eff2c-114">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="eff2c-115">SSO und PLAP</span><span class="sxs-lookup"><span data-stu-id="eff2c-115">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




