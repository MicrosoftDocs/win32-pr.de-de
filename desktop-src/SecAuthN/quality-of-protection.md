---
description: Die von der QoP-Direktive identifizierte Qualität des Schutzes wird zuerst vom Server in der digestfrage angegeben und dann vom Client in der Challenge-Antwort bestätigt.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualität des Schutzes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050318"
---
# <a name="quality-of-protection"></a><span data-ttu-id="0b572-103">Qualität des Schutzes</span><span class="sxs-lookup"><span data-stu-id="0b572-103">Quality of Protection</span></span>

<span data-ttu-id="0b572-104">Die von der QoP-Direktive identifizierte Qualität des Schutzes wird zuerst vom Server in der digestfrage angegeben und dann vom Client in der Challenge-Antwort bestätigt.</span><span class="sxs-lookup"><span data-stu-id="0b572-104">The quality of protection, identified by the qop directive, is first specified by the server in the Digest challenge, and then confirmed by the client in the challenge response.</span></span> <span data-ttu-id="0b572-105">Wenn der Client eine Quality of Protection erfordert, die vom Server nicht unterstützt wird, muss der Client die Authentifizierung beenden.</span><span class="sxs-lookup"><span data-stu-id="0b572-105">If the client requires a quality of protection that the server does not support, the client must terminate the authentication.</span></span>

<span data-ttu-id="0b572-106">Die möglichen Werte für die QoP-Direktive werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0b572-106">The possible values for the qop directive are described in the following table.</span></span>



| <span data-ttu-id="0b572-107">Wert</span><span class="sxs-lookup"><span data-stu-id="0b572-107">Value</span></span>                   | <span data-ttu-id="0b572-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b572-108">Description</span></span>                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b572-109">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="0b572-109">"auth"</span></span>                  | <span data-ttu-id="0b572-110">Nur Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="0b572-110">Authentication only.</span></span>                                                                                                                         |
| <span data-ttu-id="0b572-111">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="0b572-111">"auth-int"</span></span>              | <span data-ttu-id="0b572-112">Authentifizierungs-und [*Integritäts*](../secgloss/i-gly.md) Überprüfung mithilfe von Signaturen.</span><span class="sxs-lookup"><span data-stu-id="0b572-112">Authentication and [*integrity*](../secgloss/i-gly.md) checking using signatures.</span></span>                  |
| <span data-ttu-id="0b572-113">(Nur SASL) "auth-conf"</span><span class="sxs-lookup"><span data-stu-id="0b572-113">(SASL only) "auth-conf"</span></span> | <span data-ttu-id="0b572-114">Authentifizierung, Integrität und Vertraulichkeits Überprüfung mithilfe von Signaturen und Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="0b572-114">Authentication, integrity and confidentiality checking by using signatures and encryption.</span></span> <span data-ttu-id="0b572-115">Weitere Informationen finden Sie unter [Chiffren](ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="0b572-115">For more information, see [Ciphers](ciphers.md).</span></span> |



 

<span data-ttu-id="0b572-116">Die Qualität des Schutzes wird durch die an die Microsoft Digest SSP übergebenen anforderungsflags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0b572-116">Quality of protection is determined by context requirement flags passed to the Microsoft Digest SSP.</span></span> <span data-ttu-id="0b572-117">In der folgenden Tabelle werden die Flags im Zusammenhang mit der Qualität des Schutzes und der resultierende Wert der QoP-Direktive aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0b572-117">The following table lists the flags related to quality of protection, and the resulting value of the qop directive.</span></span>



| <span data-ttu-id="0b572-118">Flag</span><span class="sxs-lookup"><span data-stu-id="0b572-118">Flag</span></span>                         | <span data-ttu-id="0b572-119">QoP-Wert</span><span class="sxs-lookup"><span data-stu-id="0b572-119">qop value</span></span>               |
|------------------------------|-------------------------|
| <span data-ttu-id="0b572-120">*Xxx* \_ req- \_ Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="0b572-120">*XXX*\_REQ\_CONFIDENTIALITY</span></span>  | <span data-ttu-id="0b572-121">"auth-conf" (nur SASL)</span><span class="sxs-lookup"><span data-stu-id="0b572-121">"auth-conf" (SASL only)</span></span> |
| <span data-ttu-id="0b572-122">*Xxx* \_ req \_ Replay \_ Detect</span><span class="sxs-lookup"><span data-stu-id="0b572-122">*XXX*\_REQ\_REPLAY\_DETECT</span></span>   | <span data-ttu-id="0b572-123">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="0b572-123">"auth-int"</span></span>              |
| <span data-ttu-id="0b572-124">*Xxx* \_ req- \_ Sequenz \_ Erkennung</span><span class="sxs-lookup"><span data-stu-id="0b572-124">*XXX*\_REQ\_SEQUENCE\_DETECT</span></span> | <span data-ttu-id="0b572-125">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="0b572-125">"auth-int"</span></span>              |
| <span data-ttu-id="0b572-126">*Xxx* \_ req- \_ Integrität</span><span class="sxs-lookup"><span data-stu-id="0b572-126">*XXX*\_REQ\_INTEGRITY</span></span>        | <span data-ttu-id="0b572-127">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="0b572-127">"auth-int"</span></span>              |
| <span data-ttu-id="0b572-128">(none)</span><span class="sxs-lookup"><span data-stu-id="0b572-128">(none)</span></span>                       | <span data-ttu-id="0b572-129">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="0b572-129">"auth"</span></span>                  |



 

> [!Note]  
> <span data-ttu-id="0b572-130">Von Server Anwendungen angegebene kontoanforderungsflags haben das Präfix ASC, und den Clients, die von Clients angegeben werden, wird das Präfix ISC bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="0b572-130">Context requirement flags specified by server applications have a prefix of ASC, and those specified by clients are prefixed with ISC.</span></span> <span data-ttu-id="0b572-131">Um die von der Anwendung verwendeten Flagwerte zu ermitteln, ersetzen Sie eines dieser Präfixe für *xxx*.</span><span class="sxs-lookup"><span data-stu-id="0b572-131">To determine the flag values used by your application, substitute one of these prefixes for *XXX*.</span></span>

 

<span data-ttu-id="0b572-132">Weitere Server bezogene Informationen finden Sie unter [Erstellen der Digest-Challenge](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="0b572-132">For additional server-related information, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

<span data-ttu-id="0b572-133">Weitere Client bezogene Informationen finden Sie unter [Erstellen der Digest](generating-the-digest-challenge-response.md)-Abfrage Antwort.</span><span class="sxs-lookup"><span data-stu-id="0b572-133">For additional client-related information, see [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).</span></span>

 

 
