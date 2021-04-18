---
title: Verhalten von SSO-Kenn Wort Änderungen
description: Bietet eine Schritt-für-Schritt-Vorgehensweise zum Auflösen des Verhaltens von SSO-Kenn Wort Änderungen.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106340876"
---
# <a name="sso-password-change-behavior"></a>Verhalten von SSO-Kenn Wort Änderungen

Dieses Thema enthält eine Schritt-für-Schritt-Vorgehensweise zum Auflösen des Verhaltens von SSO-Kenn Wort Änderungen.

## <a name="step-by-step-approach"></a>Schritt-für-Schritt-Vorgehensweise

Die folgende Liste stellt eine schrittweise Vorgehensweise zum Auflösen des Verhaltens von SSO-Kenn Wort Änderungen dar.

-   Sobald die EAP-Methode über eine Kenn Wort Änderung benachrichtigt wird, benachrichtigt die Methode EAPHost; EAPHost benachrichtigt den Supplicant wiederum, indem er den Aktions Code [eaphostpeer-responseinvokeui](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)zurückgibt.
-   Nach dem Empfang des [eaphostpeerresponseinvokeui](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) -Aktionscodes von EAPHost erhält der Supplicant den UI-Kontext aus der EAP-Methode, indem er die [**eaphostpeergetuicontext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) -Funktion aufruft. EAPHost erhält dann den UI-Kontext aus der EAP-Methode, indem die entsprechende Methoden Funktion aufgerufen wird.
-   Der Supplicant übergibt den UI-Kontext an den UI-Prozess (mit einer Form Prozess übergreifender Kommunikation).
-   Der UI-Prozess ruft [**eaphostpeer-queryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) auf EAPHost auf.
-   EAPHost sammelt den UI-Kontext durch Aufrufen von [**eappeerqueryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) in der EAP-Methode.
-   Die EAP-Methode stellt alle notwendigen Benutzeroberflächen-Kontextinformationen in der [**interaktiven EAP- \_ \_ UI- \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) Struktur bereit, wobei *dwDataType* auf *eapkredexpiryreq* und *pbuidata* auf eine Struktur des Typs [**EAP- \_ \_ Erstellungs-req**](eap-cred-req.md)verweist.
-   Wenn Sie die [**interaktive EAP \_ - \_ UI- \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) Struktur auffüllen, füllt diese EAP-Methode nur den Parameter " *Curr| DS* " auf und legt nicht das Flag " [**\_ \_ \_ \_ \_ Read \_ only**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) " der EAP-Benutzeroberflächen-Eingabefeld Eigenschaften in der **Datenstruktur der EAP- \_ Konfigurations \_ Eingabe \_ \_** Felder fest.
    > [!Note]  
    > Das Flag für die schreibgeschützte [**EAP-Benutzeroberflächen- \_ \_ Eingabe \_ Feld \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) Eigenschaften ist für Mitglieds Felder, die geändert werden müssen.

     

-   Nachdem die Benutzeroberflächen-Kontextinformationen erfasst wurden, rendert der UI-Prozess eine Benutzeroberfläche, um die Informationen zum Ändern des Kennworts vom Benutzer zu erfassen Diese Informationen werden mit dem *newkreds* -Parameter der EAP-Funktion zum [**\_ \_ ablaufenden \_ req aufgefüllt**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .
-   Der UI-Prozess übergibt die [**EAP- \_ Kred- \_**](eap-cred-resp.md) /Struktur-Struktur über [**eaphostpeerqueryuiblobfrominteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)an EAPHost zurück.
-   Der UI-Prozess übergibt dieses benutzerblob an den Supplicant, und der Supplicant wird wie gewohnt mit den EAPHost-Lauf Zeitfunktionen fortgesetzt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SSO-EAPHost-Szenarios](why-eaphost-sso.md)
</dt> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




