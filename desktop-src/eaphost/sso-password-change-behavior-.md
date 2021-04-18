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
# <a name="sso-password-change-behavior"></a><span data-ttu-id="3f3b4-103">Verhalten von SSO-Kenn Wort Änderungen</span><span class="sxs-lookup"><span data-stu-id="3f3b4-103">SSO Password Change Behavior</span></span>

<span data-ttu-id="3f3b4-104">Dieses Thema enthält eine Schritt-für-Schritt-Vorgehensweise zum Auflösen des Verhaltens von SSO-Kenn Wort Änderungen.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-104">This topic provides a step-by-step approach for resolving SSO password change behavior.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="3f3b4-105">Schritt-für-Schritt-Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="3f3b4-105">Step-By-Step Approach</span></span>

<span data-ttu-id="3f3b4-106">Die folgende Liste stellt eine schrittweise Vorgehensweise zum Auflösen des Verhaltens von SSO-Kenn Wort Änderungen dar.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-106">The following list represents a step-by-step approach for resolving SSO password change behavior.</span></span>

-   <span data-ttu-id="3f3b4-107">Sobald die EAP-Methode über eine Kenn Wort Änderung benachrichtigt wird, benachrichtigt die Methode EAPHost; EAPHost benachrichtigt den Supplicant wiederum, indem er den Aktions Code [eaphostpeer-responseinvokeui](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-107">Once the EAP method is notified about a password change, the method notifies EAPHost; EAPHost in turn notifies the supplicant by returning the action code, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="3f3b4-108">Nach dem Empfang des [eaphostpeerresponseinvokeui](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) -Aktionscodes von EAPHost erhält der Supplicant den UI-Kontext aus der EAP-Methode, indem er die [**eaphostpeergetuicontext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) -Funktion aufruft. EAPHost erhält dann den UI-Kontext aus der EAP-Methode, indem die entsprechende Methoden Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-108">After receiving the [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) action code from EAPHost, the supplicant obtains the UI context from the EAP method by calling the [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) function; EAPHost then obtains the UI context from the EAP method by calling the corresponding method function</span></span>
-   <span data-ttu-id="3f3b4-109">Der Supplicant übergibt den UI-Kontext an den UI-Prozess (mit einer Form Prozess übergreifender Kommunikation).</span><span class="sxs-lookup"><span data-stu-id="3f3b4-109">The supplicant passes the UI context to the UI process (using some form of inter-process communication).</span></span>
-   <span data-ttu-id="3f3b4-110">Der UI-Prozess ruft [**eaphostpeer-queryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) auf EAPHost auf.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-110">The UI process calls [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) on EAPHost.</span></span>
-   <span data-ttu-id="3f3b4-111">EAPHost sammelt den UI-Kontext durch Aufrufen von [**eappeerqueryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) in der EAP-Methode.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-111">EAPHost collects the UI context by calling [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) on the EAP method.</span></span>
-   <span data-ttu-id="3f3b4-112">Die EAP-Methode stellt alle notwendigen Benutzeroberflächen-Kontextinformationen in der [**interaktiven EAP- \_ \_ UI- \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) Struktur bereit, wobei *dwDataType* auf *eapkredexpiryreq* und *pbuidata* auf eine Struktur des Typs [**EAP- \_ \_ Erstellungs-req**](eap-cred-req.md)verweist.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-112">The EAP method provides any necessary UI context information in the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, where *dwDataType* is set to *EapCredExpiryReq* and *pbUiData* points to a structure of type [**EAP\_CRED\_REQ**](eap-cred-req.md).</span></span>
-   <span data-ttu-id="3f3b4-113">Wenn Sie die [**interaktive EAP \_ - \_ UI- \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) Struktur auffüllen, füllt diese EAP-Methode nur den Parameter " *Curr| DS* " auf und legt nicht das Flag " [**\_ \_ \_ \_ \_ Read \_ only**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) " der EAP-Benutzeroberflächen-Eingabefeld Eigenschaften in der **Datenstruktur der EAP- \_ Konfigurations \_ Eingabe \_ \_** Felder fest.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-113">While populating the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, this EAP method will only fill in the *curCreds* parameter, and not set the [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag in the **EAP\_CONFIG\_INPUT\_FIELD\_DATA** structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="3f3b4-114">Das Flag für die schreibgeschützte [**EAP-Benutzeroberflächen- \_ \_ Eingabe \_ Feld \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) Eigenschaften ist für Mitglieds Felder, die geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-114">The [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag is for member field(s) which need to be changed.</span></span>

     

-   <span data-ttu-id="3f3b4-115">Nachdem die Benutzeroberflächen-Kontextinformationen erfasst wurden, rendert der UI-Prozess eine Benutzeroberfläche, um die Informationen zum Ändern des Kennworts vom Benutzer zu erfassen</span><span class="sxs-lookup"><span data-stu-id="3f3b4-115">Having collected the UI context informtion, the UI process renders a UI to collect change password information from the user.</span></span> <span data-ttu-id="3f3b4-116">Diese Informationen werden mit dem *newkreds* -Parameter der EAP-Funktion zum [**\_ \_ ablaufenden \_ req aufgefüllt**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .</span><span class="sxs-lookup"><span data-stu-id="3f3b4-116">This information is populated in the *NewCreds* parameter of the [**EAP\_CRED\_EXPIRY\_REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) structure.</span></span>
-   <span data-ttu-id="3f3b4-117">Der UI-Prozess übergibt die [**EAP- \_ Kred- \_**](eap-cred-resp.md) /Struktur-Struktur über [**eaphostpeerqueryuiblobfrominteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)an EAPHost zurück.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-117">The UI process passes the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure back to EAPHost via [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span></span>
-   <span data-ttu-id="3f3b4-118">Der UI-Prozess übergibt dieses benutzerblob an den Supplicant, und der Supplicant wird wie gewohnt mit den EAPHost-Lauf Zeitfunktionen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-118">The UI process passes this user BLOB to the supplicant, and the supplicant continues with EAPHost run-time functions as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f3b4-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f3b4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f3b4-120">SSO-EAPHost-Szenarios</span><span class="sxs-lookup"><span data-stu-id="3f3b4-120">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="3f3b4-121">SSO und PLAP</span><span class="sxs-lookup"><span data-stu-id="3f3b4-121">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




