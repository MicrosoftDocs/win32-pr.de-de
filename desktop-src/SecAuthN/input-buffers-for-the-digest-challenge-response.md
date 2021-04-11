---
description: Die HTTP-Authentifizierung mit Microsoft Digest erfordert drei Eingabepuffer, um eine Abfrage Antwort zu generieren. In der folgenden Tabelle werden diese Puffer zusammengefasst.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Eingabepuffer für die digestaufforderungs-Antwort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128305"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a><span data-ttu-id="36b37-104">Eingabepuffer für die digestaufforderungs-Antwort</span><span class="sxs-lookup"><span data-stu-id="36b37-104">Input Buffers for the Digest Challenge Response</span></span>

<span data-ttu-id="36b37-105">Die HTTP-Authentifizierung mit Microsoft Digest erfordert drei Eingabepuffer, um eine Abfrage Antwort zu generieren.</span><span class="sxs-lookup"><span data-stu-id="36b37-105">HTTP authentication using Microsoft Digest requires three input buffers to generate a challenge response.</span></span> <span data-ttu-id="36b37-106">In der folgenden Tabelle werden diese Puffer zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="36b37-106">The following table summarizes these buffers.</span></span>



| <span data-ttu-id="36b37-107">Puffer Nummer</span><span class="sxs-lookup"><span data-stu-id="36b37-107">Buffer number</span></span> | <span data-ttu-id="36b37-108">Enthält</span><span class="sxs-lookup"><span data-stu-id="36b37-108">Contains</span></span>                                                                                                                                             | <span data-ttu-id="36b37-109">Puffertyp</span><span class="sxs-lookup"><span data-stu-id="36b37-109">Buffer type</span></span>                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36b37-110">0</span><span class="sxs-lookup"><span data-stu-id="36b37-110">0</span></span>             | <span data-ttu-id="36b37-111">Vom Server empfangene Abfrage</span><span class="sxs-lookup"><span data-stu-id="36b37-111">Challenge received from the Server</span></span>                                                                                                                   | <span data-ttu-id="36b37-112">secbuffer- \_ Token</span><span class="sxs-lookup"><span data-stu-id="36b37-112">SECBUFFER\_TOKEN</span></span>                                            |
| <span data-ttu-id="36b37-113">1</span><span class="sxs-lookup"><span data-stu-id="36b37-113">1</span></span>             | <span data-ttu-id="36b37-114">HTTP-Methode</span><span class="sxs-lookup"><span data-stu-id="36b37-114">HTTP Method</span></span>                                                                                                                                          | <span data-ttu-id="36b37-115">secbuffer \_ -Parameter</span><span class="sxs-lookup"><span data-stu-id="36b37-115">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="36b37-116">2</span><span class="sxs-lookup"><span data-stu-id="36b37-116">2</span></span>             | <span data-ttu-id="36b37-117">H (Entität)</span><span class="sxs-lookup"><span data-stu-id="36b37-117">H(Entity)</span></span>                                                                                                                                            | <span data-ttu-id="36b37-118">secbuffer \_ -Parameter</span><span class="sxs-lookup"><span data-stu-id="36b37-118">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="36b37-119">3</span><span class="sxs-lookup"><span data-stu-id="36b37-119">3</span></span>             | <span data-ttu-id="36b37-120">Der [*Dienst Prinzipal Name (Service Principal Name*](../secgloss/s-gly.md) , SPN) des Zielservers.</span><span class="sxs-lookup"><span data-stu-id="36b37-120">The [*service principal name*](../secgloss/s-gly.md) (SPN) of the target server.</span></span> | <span data-ttu-id="36b37-121">**Secbuffer \_ Schreib \_** Schutz für \| **secbuffer \_** des Zielhosts</span><span class="sxs-lookup"><span data-stu-id="36b37-121">**SECBUFFER\_TARGET\_HOST** \| **SECBUFFER\_READONLY**</span></span>      |
| <span data-ttu-id="36b37-122">4</span><span class="sxs-lookup"><span data-stu-id="36b37-122">4</span></span>             | <span data-ttu-id="36b37-123">Werte für Kanal Bindungs Token</span><span class="sxs-lookup"><span data-stu-id="36b37-123">Channel bindings token values</span></span>                                                                                                                        | <span data-ttu-id="36b37-124">**Secbuffer \_ Kanal \_ Bindungen** \| **secbuffer \_** schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36b37-124">**SECBUFFER\_CHANNEL\_BINDINGS** \| **SECBUFFER\_READONLY**</span></span> |



 

<span data-ttu-id="36b37-125">Der Puffer NULL enthält die vom Server empfangene digestfrage als Antwort auf die anfängliche Anforderung einer Zugriffs geschützten Ressource.</span><span class="sxs-lookup"><span data-stu-id="36b37-125">Buffer zero contains the Digest challenge received from the server in response to the initial request for an access-protected resource.</span></span>

<span data-ttu-id="36b37-126">Buffer 1 enthält die Zeichen folgen Darstellung der Methode, z. b. "Get" oder "Post".</span><span class="sxs-lookup"><span data-stu-id="36b37-126">Buffer 1 contains the string representation of the method, such as "GET" or "POST".</span></span> <span data-ttu-id="36b37-127">Die-Methode wird in der Berechnung von a2 verwendet, wie in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="36b37-127">The method is used in the calculation of A2, as described in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span></span>

<span data-ttu-id="36b37-128">Buffer 2 ist der [*MD5*](../secgloss/m-gly.md) -Hash des Entitäts Texts der Nachricht, wie in RFC 2617 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="36b37-128">Buffer 2 is the [*MD5*](../secgloss/m-gly.md) hash of the message's entity-body as described in RFC 2617.</span></span>

<span data-ttu-id="36b37-129">Buffer 3 enthält den SPN des Zielservers in UTF-8-Formatierung, wenn Digest mit Kanal Bindungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36b37-129">Buffer 3 contains the SPN of the target server in UTF-8 formatting when Digest is used with channel bindings.</span></span>

<span data-ttu-id="36b37-130">Puffer 4 enthält den channelbindungstokenwert, wenn Digest mit Kanal Bindungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36b37-130">Buffer 4 contains the channel binding token value when Digest is used with channel bindings.</span></span>

## <a name="input-buffers-for-sasl"></a><span data-ttu-id="36b37-131">Eingabepuffer für SASL</span><span class="sxs-lookup"><span data-stu-id="36b37-131">Input Buffers for SASL</span></span>

<span data-ttu-id="36b37-132">Stellen Sie nur Puffer NULL bereit.</span><span class="sxs-lookup"><span data-stu-id="36b37-132">Supply buffer zero only.</span></span> <span data-ttu-id="36b37-133">Aus Gründen der Kompatibilität mit anderen SSPs können Sie [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) ohne gültige Server Herausforderung abrufen.</span><span class="sxs-lookup"><span data-stu-id="36b37-133">For compatibility with other SSPs, you may call [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) without a valid server challenge.</span></span> <span data-ttu-id="36b37-134">In diesem Fall sollte der *pinput* -Parameter auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="36b37-134">In this case the *pInput* parameter should be set to **NULL**.</span></span>

 

 
