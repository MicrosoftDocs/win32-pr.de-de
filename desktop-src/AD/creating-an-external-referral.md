---
title: Erstellen eines externen Verweises
description: Wenn ein externes CrossRef-Objekt erstellt wird und ein Domänen Controller es zum Generieren eines Verweises verwendet, stellt das CrossRef-Objekt zwei wichtige Datenelemente in den folgenden Eigenschaften bereit.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- externe Verweise Active Directory
- Active Directory Beispiele Active Directory, Erstellen eines externen Verweises
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724592"
---
# <a name="creating-an-external-referral"></a><span data-ttu-id="ff2bc-105">Erstellen eines externen Verweises</span><span class="sxs-lookup"><span data-stu-id="ff2bc-105">Creating an External Referral</span></span>

<span data-ttu-id="ff2bc-106">Wenn ein externes [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt erstellt wird und ein Domänen Controller es zum Generieren eines Verweises verwendet, stellt das **CrossRef** -Objekt zwei wichtige Datenelemente in den folgenden Eigenschaften bereit.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-106">If an external [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is created and a domain controller uses it to generate a referral, the **crossRef** object provides two important data elements in the following properties.</span></span> <span data-ttu-id="ff2bc-107">Weitere Informationen zu Situationen, in denen dies auftreten kann, finden Sie im vorherigen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-107">For more information about situations where this can occur, see the previous section.</span></span>



| <span data-ttu-id="ff2bc-108">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff2bc-108">Property</span></span>                           | <span data-ttu-id="ff2bc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff2bc-109">Description</span></span>                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff2bc-110">**dnsRoot**</span><span class="sxs-lookup"><span data-stu-id="ff2bc-110">**dnsRoot**</span></span>](/windows/desktop/ADSchema/a-dnsroot) | <span data-ttu-id="ff2bc-111">Gibt den Server oder die Domäne an, der Daten aus dem namens Kontext bereitstellen kann, der in [**NCName**](/windows/desktop/ADSchema/a-ncname)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-111">Specifies the server or domain that can serve data from the naming context specified in [**nCName**](/windows/desktop/ADSchema/a-ncname).</span></span>                                           |
| [<span data-ttu-id="ff2bc-112">**NCName**</span><span class="sxs-lookup"><span data-stu-id="ff2bc-112">**nCName**</span></span>](/windows/desktop/ADSchema/a-ncname)   | <span data-ttu-id="ff2bc-113">Gibt den Distinguished Name für die Domäne, das Schema oder den Konfigurations Container an, die auf dem durch [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)angegebenen Server oder in der Domäne verankert ist.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-113">Specifies the distinguished name for the domain, schema, or configuration container rooted at the server or domain specified by [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot).</span></span> |



 

<span data-ttu-id="ff2bc-114">Wenn z. b. der Server mit der DNS-Adresse serv1.Northwest.fabrikam.com den namens Kontext für CN = MyContainer, ou = mydom, O = Fabrikam verwendet, legen [**Sie die DNS-Adresse des Servers**](/windows/desktop/ADSchema/a-dnsroot) auf die DNS-Adresse des Servers und [**NCName**](/windows/desktop/ADSchema/a-ncname) auf den Distinguished Name der Domäne, des Schemas oder des Konfigurations Containers fest.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-114">For example, if the server with DNS address of serv1.northwest.Fabrikam.com serves the naming context rooted at CN=MyContainer,OU=MyDOM,O=Fabrikam, set the [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) to that server's DNS address and the [**nCName**](/windows/desktop/ADSchema/a-ncname) to the distinguished name of the domain, schema, or configuration container.</span></span>

<span data-ttu-id="ff2bc-115">Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie einen externen Verweis erstellen, finden Sie unter [Beispielcode zum Erstellen eines externen CrossRef-Objekts](example-code-for-creating-an-external-crossref-object.md).</span><span class="sxs-lookup"><span data-stu-id="ff2bc-115">For more information and a code example that shows how to create an external referral, see [Example Code for Creating an External crossRef Object](example-code-for-creating-an-external-crossref-object.md).</span></span>

 

 