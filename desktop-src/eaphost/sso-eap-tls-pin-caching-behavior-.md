---
title: SSO-EAP-TLS-PIN-Zwischenspeicherungsverhalten
description: Bietet einen schrittweisen Ansatz zum Lösen von Problemen bei der Sitzungsaufbeendigung und erneuten Authentifizierung eines Roamingbenutzers in einer SSO-EAP-TLS-Umgebung.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bc8cb112a6def55085cbd0b94068407320e4116a4b0161d7d923319257258f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085884"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a>SSO-EAP-TLS-PIN-Zwischenspeicherungsverhalten

Dieses Thema bietet einen schrittweisen Ansatz zum Lösen von Problemen bei der Wiederaufnahme von Sitzungen und der erneuten Authentifizierung eines Roamingbenutzers in einer SSO-EAP-TLS-Umgebung.

## <a name="step-by-step-approach"></a>Schritt-für-Schritt-Vorgehensweise

Die folgende Liste stellt einen schrittweisen Ansatz zum Lösen von Problemen im Zusammenhang mit der Sitzungsaufbeendigung und erneuten Authentifizierung eines Roamingbenutzers in einer SSO-EAP-TLS-Umgebung dar.

-   Nach der ersten erfolgreichen Authentifizierung in einer SSO-Umgebung mit EAP-TLS behält die Unterstützung standardmäßig alle Benutzeranmeldeinformationen bei.
    > [!Note]  
    > Obwohl dies der jeweiligen suppliiellen Implementierung unterliegt, empfiehlt es sich, dass die Supplizierung die gesamte [**EAP \_ CONFIG \_ INPUT FIELD \_ ARRAY-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) beibehält, die zuletzt im [**EapHostPeerQueryUserBlobFromCredentialInputFields-Aufruf**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) von EAPHost verwendet wurde.

     

-   Wenn der Benutzer zum ersten Mal umgeht und die erneute Authentifizierung beginnt, ruft die Supplision [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) erneut mit der gleichen [**EAP \_ CONFIG \_ INPUT FIELD \_ ARRAY-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) auf. Die Unterstützung muss auch das gleiche Benutzer-BLOB übergeben, das nach der ersten erfolgreichen Authentifizierung beibehalten wurde.
-   EAPHost übergibt dann die Informationen im Benutzer-BLOB an die EAP-Methode.
-   Die EAP-Methode aktualisiert wiederum das Benutzer-BLOB mit Anmeldeinformationsfeldern , z. B. der PIN, die in *pEapConfigInputFieldArray* angegeben ist, und behält die verbleibenden Werte ( z. B. das Serverzertifikat ) wie im ursprünglichen Benutzer-BLOB bei.
-   Nach Abschluss dieser Schritte kann die Unterstützung die Authentifizierung normal fortsetzen, indem sie die [**Laufzeitfunktion EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) mit diesem Benutzer-BLOB aufruft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SSO EAPHost-Szenarien](why-eaphost-sso.md)
</dt> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




