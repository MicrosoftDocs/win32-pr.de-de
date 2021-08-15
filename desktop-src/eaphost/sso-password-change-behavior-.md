---
title: SSO-Kennwortänderungsverhalten
description: Bietet einen schritt-für-Schritt-Ansatz zum Auflösen des SSO-Kennwortänderungsverhaltens.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d438dd41466809805f159fde4a2db698d11b1f7899e48e1f96ccce2c811111cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042798"
---
# <a name="sso-password-change-behavior"></a>SSO-Kennwortänderungsverhalten

Dieses Thema enthält eine schritt-für-Schritt-Vorgehensweise zum Auflösen des SSO-Kennwortänderungsverhaltens.

## <a name="step-by-step-approach"></a>Schritt-für-Schritt-Vorgehensweise

Die folgende Liste stellt einen schritt-für-Schritt-Ansatz zum Auflösen des SSO-Kennwortänderungsverhaltens dar.

-   Sobald die EAP-Methode über eine Kennwortänderung benachrichtigt wird, benachrichtigt die Methode EAPHost. EAPHost benachrichtigt wiederum den Supplicant, indem er den Aktionscode [EapHostPeerResponseInvokeUI zurücksendet.](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)
-   Nachdem der [EapHostPeerResponseInvokeUI-Aktionscode](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) von EAPHost empfangen wurde, ruft der Supplicant den Benutzeroberflächenkontext aus der EAP-Methode ab, indem er die [**EapHostPeerGetUIContext-Funktion**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) aufruft. EAPHost ruft dann den Benutzeroberflächenkontext aus der EAP-Methode ab, indem die entsprechende Methodenfunktion aufruft.
-   Der Supplicant übergibt den Benutzeroberflächenkontext an den Benutzeroberflächenprozess (mithilfe einer Form der prozessübergreifenden Kommunikation).
-   Der Benutzeroberflächenprozess ruft [**EapHostPeerQueryInteractiveUIInputFields auf**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) EAPHost auf.
-   EAPHost erfasst den Benutzeroberflächenkontext durch Aufrufen [**von EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) für die EAP-Methode.
-   Die EAP-Methode stellt alle erforderlichen Ui-Kontextinformationen in der [**EAP \_ INTERACTIVE UI \_ \_ DATA-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) zur Verfügung, wobei *dwDataType* auf *EapCredExpiryReq* festgelegt ist und *pbUiData* auf eine Struktur vom Typ [**EAP \_ CRED \_ REQ**](eap-cred-req.md)verweist.
-   Beim Auffüllen der [**EAP \_ INTERACTIVE UI \_ \_ DATA-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) füllt diese EAP-Methode nur den *curCreds-Parameter* aus und setzt nicht das [**EAP UI INPUT FIELD \_ \_ \_ \_ PROPS READ \_ \_ ONLY-Flag**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) in der **EAP \_ CONFIG INPUT FIELD \_ \_ \_ DATA-Struktur.**
    > [!Note]  
    > Das [**EAP \_ UI INPUT FIELD \_ \_ \_ PROPS READ \_ \_ ONLY-Flag**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) gilt für Memberfeld(e), die geändert werden müssen.

     

-   Nachdem die Benutzeroberflächenkontextinformationen erfasst wurden, rendert der Benutzeroberflächenprozess eine Benutzeroberfläche, um Änderungskennwortinformationen vom Benutzer zu sammeln. Diese Informationen werden im *NewCreds-Parameter* der [**EAP \_ CRED \_ EXPIRY \_ REQ-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) aufgefüllt.
-   Der Benutzeroberflächenprozess übergibt die [**EAP \_ CRED \_ RESP-Struktur**](eap-cred-resp.md) über [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)an EAPHost zurück.
-   Der Benutzeroberflächenprozess übergibt dieses BenutzerBLOB an den Supplicant, und der Supplicant wird wie gewohnt mit EAPHost-Laufzeitfunktionen fortgesetzt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SSO EAPHost-Szenarien](why-eaphost-sso.md)
</dt> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




