---
description: Stellt SChannel-spezifische Informationen über einen Sicherheitskontext bereit.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Abfragen der Attribute eines SChannel-Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128284"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a><span data-ttu-id="76f26-103">Abfragen der Attribute eines SChannel-Kontexts</span><span class="sxs-lookup"><span data-stu-id="76f26-103">Querying the Attributes of an Schannel Context</span></span>

<span data-ttu-id="76f26-104">Die [**QueryContextAttributes-Funktion (SChannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) stellt SChannel-spezifische Informationen über einen [*Sicherheitskontext*](../secgloss/s-gly.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="76f26-104">The [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) function provides Schannel-specific information about a [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="76f26-105">Die meisten Informationen werden ursprünglich angegeben, wenn der Kontext mithilfe der Client [**InitializeSecurityContext-Funktion (SChannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) oder der Server [**Akzeptanz Context-Funktion (SChannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="76f26-105">Most of the information is originally specified when the context is created by using the client [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) or server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span> <span data-ttu-id="76f26-106">Beim Abrufen eines Handles für die Anmelde Informationen, die zum Erstellen des Kontexts verwendet werden, werden einige Informationen angegeben.</span><span class="sxs-lookup"><span data-stu-id="76f26-106">Some information is specified when obtaining a handle to the credential used to create the context.</span></span> <span data-ttu-id="76f26-107">Weitere Informationen finden Sie unter Abrufen von [SChannel-Anmelde](obtaining-schannel-credentials.md)Informationen.</span><span class="sxs-lookup"><span data-stu-id="76f26-107">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
