---
title: EAPHost-Peer Methoden Strukturen
description: Erfahren Sie mehr über EAPHost-Peer Methoden-API-Strukturen wie eapcertifikatecredential und eapsimcredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339099"
---
# <a name="eaphost-peer-method-structures"></a><span data-ttu-id="51282-103">EAPHost-Peer Methoden Strukturen</span><span class="sxs-lookup"><span data-stu-id="51282-103">EAPHost Peer Method Structures</span></span>

<span data-ttu-id="51282-104">Die API-Strukturen der EAPHost-Peer Methode lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="51282-104">The EAPHost Peer Method API structures are as follows.</span></span>



| <span data-ttu-id="51282-105">Struktur</span><span class="sxs-lookup"><span data-stu-id="51282-105">Structure</span></span>                                                              | <span data-ttu-id="51282-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51282-106">Description</span></span>                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51282-107">**Eapcertifialisiecredential**</span><span class="sxs-lookup"><span data-stu-id="51282-107">**EapCertificateCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | <span data-ttu-id="51282-108">Enthält Informationen über das Zertifikat, das von der EAP-Methode für die Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51282-108">Contains information about the certificate that the EAP method uses for authentication.</span></span>                                                                                                            |
| [<span data-ttu-id="51282-109">**Eapcredential**</span><span class="sxs-lookup"><span data-stu-id="51282-109">**EapCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | <span data-ttu-id="51282-110">Enthält Informationen zum Typ der Anmelde Informationen und den entsprechenden Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="51282-110">Contains information about the credentials type and the appropriate credentials.</span></span> <span data-ttu-id="51282-111">Dies wird als Eingabe an die [**eappeergetconfigblobanduserblob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) -API übermittelt.</span><span class="sxs-lookup"><span data-stu-id="51282-111">This is passed as an input to the [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) API.</span></span> |
| [<span data-ttu-id="51282-112">**EAP- \_ Peer \_ Methoden \_ Routinen**</span><span class="sxs-lookup"><span data-stu-id="51282-112">**EAP\_PEER\_METHOD\_ROUTINES**</span></span>](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | <span data-ttu-id="51282-113">Enthält einen Satz von Funktions Zeigern für die EAPHost-Peer Methoden-APIs.</span><span class="sxs-lookup"><span data-stu-id="51282-113">Contains a set of function pointers to the EAPHost Peer Method APIs.</span></span>                                                                                                                               |
| [<span data-ttu-id="51282-114">**Eappeermethodoutput**</span><span class="sxs-lookup"><span data-stu-id="51282-114">**EapPeerMethodOutput**</span></span>](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | <span data-ttu-id="51282-115">Enthält die Aktions Informationen, die von einer EAP-Peer Methode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51282-115">Contains the action information returned by an EAP peer method.</span></span>                                                                                                                                    |
| [<span data-ttu-id="51282-116">**Eappeermethodresult**</span><span class="sxs-lookup"><span data-stu-id="51282-116">**EapPeerMethodResult**</span></span>](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | <span data-ttu-id="51282-117">Enthält Ergebnisdaten, die während der Authentifizierung von einer EAP-Methode generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="51282-117">Contains result data generated by an EAP method during authentication.</span></span>                                                                                                                             |
| [<span data-ttu-id="51282-118">**Eapsimcredential**</span><span class="sxs-lookup"><span data-stu-id="51282-118">**EapSimCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | <span data-ttu-id="51282-119">Enthält Informationen über die SIM-Daten, die von der EAP-Methode für die Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51282-119">Contains information about the SIM that is used by the EAP method for authentication.</span></span>                                                                                                              |
| [<span data-ttu-id="51282-120">**Eapusernamepasswordcredential**</span><span class="sxs-lookup"><span data-stu-id="51282-120">**EapUsernamePasswordCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | <span data-ttu-id="51282-121">Enthält den Benutzernamen und das Kennwort, die von der EAP-Methode zum Authentifizieren des Benutzers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51282-121">Contains the username and password that is used by the EAP method for authenticating the user.</span></span>                                                                                                     |



 

 

 




