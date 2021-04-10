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
# <a name="sso-eap-tls-pin-caching-behavior"></a>SSO EAP-TLS Pin Caching-Verhalten

Dieses Thema enthält eine schrittweise Anleitung zur Behebung von Problemen bei der Sitzungs Wiederaufnahme und erneuten Authentifizierung eines Roamingbenutzers in einer SSO-EAP-TLS-Umgebung.

## <a name="step-by-step-approach"></a>Schritt-für-Schritt-Vorgehensweise

Die folgende Liste enthält eine schrittweise Vorgehensweise zur Behebung von Problemen bei der Sitzungs Wiederaufnahme und erneuten Authentifizierung eines Roamingbenutzers in einer SSO-EAP-TLS-Umgebung.

-   Nach der ersten erfolgreichen Authentifizierung in einer SSO-Umgebung mit EAP-TLS behält der Supplicant standardmäßig alle Benutzer Anmelde Informationen im Zusammenhang mit.
    > [!Note]  
    > Obwohl die jeweilige Supplicant-Implementierung unterliegt, empfiehlt es sich, die gesamte [**EAP- \_ config- \_ Eingabe \_ Feld Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur beizubehalten, die vom Supplicant zuletzt im [**eaphostpeerqueryuserblobfromdedentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) -aufrufeaphost verwendet wurde.

     

-   Wenn der Benutzer zum ersten Mal wechselt und die erneute Authentifizierung beginnt, ruft der Supplicant [**eaphostpeerqueryuserblobfromkredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) erneut mit der gleichen [**EAP- \_ Konfigurations \_ Eingabefeld- \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) Struktur auf. der Supplicant muss auch denselben benutzerblob übergeben, der nach der ersten erfolgreichen Authentifizierung aufbewahrt wird.
-   EAPHost übergibt dann die Informationen im benutzerblob an die EAP-Methode.
-   Die EAP-Methode aktualisiert wiederum das benutzerblob mit Anmelde Informationsfeldern (z. b. in *peapconfiginputfieldarray*) und behält die restlichen Werte bei, z. b. das Serverzertifikat, wie es im ursprünglichen benutzerblob war.
-   Nachdem Sie diese Schritte ausgeführt haben, kann der Supplicant die Authentifizierung auf normale Weise fortsetzen, indem die [**eaphostpeer-BeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) -Lauf Zeitfunktion mit diesem benutzerblob aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SSO-EAPHost-Szenarios](why-eaphost-sso.md)
</dt> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




