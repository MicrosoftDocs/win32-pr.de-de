---
description: Stellt SChannel-spezifische Informationen über Anmelde Informationen bereit.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Abfragen der Attribute von SChannel-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215881"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a><span data-ttu-id="92e4d-103">Abfragen der Attribute von SChannel-Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="92e4d-103">Querying the Attributes of an Schannel Credential</span></span>

<span data-ttu-id="92e4d-104">Die [**querykredentialsattributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) -Funktion stellt SChannel-spezifische Informationen über Anmelde Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="92e4d-104">The [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) function provides Schannel-specific information about a credential.</span></span> <span data-ttu-id="92e4d-105">Diese Informationen werden ursprünglich angegeben, wenn die Anmelde Informationen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="92e4d-105">This information is originally specified when the credential is created.</span></span> <span data-ttu-id="92e4d-106">Weitere Informationen finden Sie unter Abrufen von [SChannel-Anmelde](obtaining-schannel-credentials.md)Informationen.</span><span class="sxs-lookup"><span data-stu-id="92e4d-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span> <span data-ttu-id="92e4d-107">Die von dieser Funktion gemeldeten Informationen sind für alle Verbindungen ([*Sicherheits Kontexte*](../secgloss/s-gly.md)) gültig, die mit den angegebenen Anmelde Informationen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="92e4d-107">The information reported by this function is valid for any connections ([*security contexts*](../secgloss/s-gly.md)) created by using the specified credential.</span></span>

 

 
