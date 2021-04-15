---
title: Auswählen einer Authentifizierungs Ebene
description: Wenn Sie eine Authentifizierungs Ebene auswählen, verwenden Sie die folgende Richtlinie.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471149"
---
# <a name="choosing-an-authentication-level"></a><span data-ttu-id="7fff7-103">Auswählen einer Authentifizierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="7fff7-103">Choosing an Authentication Level</span></span>

<span data-ttu-id="7fff7-104">Wenn Sie eine Authentifizierungs Ebene auswählen, verwenden Sie die folgende Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="7fff7-104">When choosing an authentication level, use the following guideline.</span></span> <span data-ttu-id="7fff7-105">Wenn es keine Rolle spielt, ob die gesendeten Daten abgefangen und geändert werden können und die empfangenen Daten abgefangen oder geändert werden können, verwenden Sie RPC \_ C \_ authn \_ Level None ( \_ Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="7fff7-105">If it does not matter whether the data being sent can be intercepted and modified, and the data received can be intercepted or modified, use RPC\_C\_AUTHN\_LEVEL\_NONE, which is the default.</span></span> <span data-ttu-id="7fff7-106">Wenn die Daten nicht geändert werden sollen und private Daten nicht gesendet oder empfangen werden, verwenden Sie die Pkt-Integrität der RPC- \_ C- \_ authn- \_ Ebene \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7fff7-106">If the data should not be modified, and private data is not being sent or received, use RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY.</span></span> <span data-ttu-id="7fff7-107">Verwenden Sie in allen anderen Fällen die \_ Pkt-Datenschutz auf RPC-C- \_ authn- \_ Ebene \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7fff7-107">In all other cases, use RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

<span data-ttu-id="7fff7-108">Verwenden Sie nicht die Standardeinstellung RPC-c-authn- \_ \_ \_ Ebene \_ , RPC \_ c \_ authn \_ Level \_ Connect, RPC- \_ c- \_ authn- \_ Ebene \_ oder RPC- \_ c-authn-Ebene \_ \_ \_ Pkt.</span><span class="sxs-lookup"><span data-stu-id="7fff7-108">Do not use RPC\_C\_AUTHN\_LEVEL\_DEFAULT, RPC\_C\_AUTHN\_LEVEL\_CONNECT, RPC\_C\_AUTHN\_LEVEL\_CALL or RPC\_C\_AUTHN\_LEVEL\_PKT.</span></span> <span data-ttu-id="7fff7-109">Ein anspruchsvoller Angreifer kann diese Authentifizierungs Ebenen unterbrechen und Sie als unwirksam erweisen.</span><span class="sxs-lookup"><span data-stu-id="7fff7-109">A sophisticated attacker can break these authentication levels and render them ineffective.</span></span> <span data-ttu-id="7fff7-110">Auf jeder dieser Ebenen ist es für einen Angreifer etwas schwieriger, Daten abzufangen und zu ändern und einen Identitätswechsel vorzunehmen, aber die Sicherheit wird nicht wirklich erreicht.</span><span class="sxs-lookup"><span data-stu-id="7fff7-110">Each of these levels does make it slightly more difficult for an attacker to intercept and modify data, and to impersonate, but security is not really achieved.</span></span> <span data-ttu-id="7fff7-111">Da die Komplexität eines Angreifers selten bekannt ist, sind diese Optionen nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="7fff7-111">Since the sophistication level of an attacker is rarely known, these are not wise choices.</span></span>

 

 




