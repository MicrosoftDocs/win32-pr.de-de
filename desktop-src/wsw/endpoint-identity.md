---
title: Endpunktidentität
description: Die in diesem Abschnitt definierten Typen werden verwendet, um die Sicherheitsidentität einer Endpunkt Adresse zu definieren.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Endpunkt Identitäts-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388002"
---
# <a name="endpoint-identity"></a><span data-ttu-id="8179e-106">Endpunktidentität</span><span class="sxs-lookup"><span data-stu-id="8179e-106">Endpoint Identity</span></span>

<span data-ttu-id="8179e-107">Die in diesem Abschnitt definierten Typen werden verwendet, um die Sicherheitsidentität einer Endpunkt Adresse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8179e-107">The types defined in this section are used to define the security identity of an endpoint address.</span></span>

<span data-ttu-id="8179e-108">Die folgenden API-Elemente sind Teil der Endpunkt Indentity:</span><span class="sxs-lookup"><span data-stu-id="8179e-108">The following API elements are part of endpoint indentity:</span></span>



| <span data-ttu-id="8179e-109">Enumeration</span><span class="sxs-lookup"><span data-stu-id="8179e-109">Enumeration</span></span>                                                       | <span data-ttu-id="8179e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8179e-110">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8179e-111">**Identitäts Typ des WS- \_ Endpunkts \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8179e-111">**WS\_ENDPOINT\_IDENTITY\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | <span data-ttu-id="8179e-112">Der Typ der Endpunkt Identität, der als Selektor für die Untertypen der [**WS- \_ Endpunkt \_ Identität**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8179e-112">The type of the endpoint identity, used as a selector for subtypes of [**WS\_ENDPOINT\_IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span></span> |



 



| <span data-ttu-id="8179e-113">Struktur</span><span class="sxs-lookup"><span data-stu-id="8179e-113">Structure</span></span>                                                               | <span data-ttu-id="8179e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8179e-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8179e-115">**Identität des WS \_ CERT- \_ Endpunkts \_**</span><span class="sxs-lookup"><span data-stu-id="8179e-115">**WS\_CERT\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | <span data-ttu-id="8179e-116">Der Typ für die Zertifikat Endpunkt Identität.</span><span class="sxs-lookup"><span data-stu-id="8179e-116">The type for certificate endpoint identity .</span></span>                                                 |
| [<span data-ttu-id="8179e-117">**Identität des WS \_ DNS- \_ Endpunkts \_**</span><span class="sxs-lookup"><span data-stu-id="8179e-117">**WS\_DNS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | <span data-ttu-id="8179e-118">Der Typ zum Angeben einer Endpunkt Identität, die durch einen DNS-Namen dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8179e-118">The type for specifying an endpoint identity represented by a DNS name.</span></span>                      |
| [<span data-ttu-id="8179e-119">**WS- \_ Endpunkt \_ Identität**</span><span class="sxs-lookup"><span data-stu-id="8179e-119">**WS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | <span data-ttu-id="8179e-120">Der Basistyp für alle Endpunkt Identitäten.</span><span class="sxs-lookup"><span data-stu-id="8179e-120">The base type for all endpoint identities.</span></span>                                                   |
| [<span data-ttu-id="8179e-121">**Identität des WS \_ RSA- \_ Endpunkts \_**</span><span class="sxs-lookup"><span data-stu-id="8179e-121">**WS\_RSA\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | <span data-ttu-id="8179e-122">Geben Sie für die RSA-Endpunkt Identität ein.</span><span class="sxs-lookup"><span data-stu-id="8179e-122">Type for RSA endpoint identity.</span></span>                                                              |
| [<span data-ttu-id="8179e-123">**WS- \_ SPN- \_ Endpunkt \_ Identität**</span><span class="sxs-lookup"><span data-stu-id="8179e-123">**WS\_SPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | <span data-ttu-id="8179e-124">Der Typ zum Angeben einer Endpunkt Identität, die durch einen SPN (Dienst Prinzipal Name) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8179e-124">The type for specifying an endpoint identity represented by an SPN (service principal name).</span></span> |
| [<span data-ttu-id="8179e-125">**Identität des unbekannten WS- \_ \_ Endpunkts \_**</span><span class="sxs-lookup"><span data-stu-id="8179e-125">**WS\_UNKNOWN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | <span data-ttu-id="8179e-126">Der Typ für eine unbekannte Endpunkt Identität.</span><span class="sxs-lookup"><span data-stu-id="8179e-126">The type for an unknown endpoint identity.</span></span>                                                   |
| [<span data-ttu-id="8179e-127">**WS- \_ UPN- \_ Endpunkt \_ Identität**</span><span class="sxs-lookup"><span data-stu-id="8179e-127">**WS\_UPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | <span data-ttu-id="8179e-128">Der Typ zum Angeben einer Endpunkt Identität, die durch einen UPN (Benutzer Prinzipal Name) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8179e-128">The type for specifying an endpoint identity represented by a UPN (user principal name).</span></span>     |



 

 

 




