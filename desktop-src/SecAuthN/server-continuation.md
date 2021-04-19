---
description: Basierend auf dem Rückgabecode von einem vorherigen aufrufungskontext (allgemein) kann der Server auf eine Antwort vom Client warten und an zusätzlichen Austausch Vorgängen mit dem Client teilnehmen.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Server Fortsetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349195"
---
# <a name="server-continuation"></a><span data-ttu-id="c58e7-103">Server Fortsetzung</span><span class="sxs-lookup"><span data-stu-id="c58e7-103">Server Continuation</span></span>

<span data-ttu-id="c58e7-104">Basierend auf dem Rückgabecode von einem vorherigen [**aufrufungskontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)kann der Server auf eine Antwort vom Client warten und an zusätzlichen Austausch Vorgängen mit dem Client teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="c58e7-104">Based on the return code from a previous call to [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), the server can wait for a response from the client and can participate in additional exchanges with the client.</span></span> <span data-ttu-id="c58e7-105">Um das Authentifizierungsprotokoll fortzusetzen, wiederholt der Server Aufrufe von " **akzeptsecuritycontext (allgemein)**".</span><span class="sxs-lookup"><span data-stu-id="c58e7-105">To continue the authentication protocol, the server repeats calls to **AcceptSecurityContext (General)**.</span></span>

<span data-ttu-id="c58e7-106">Der von " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) " zurückgegebene Status wird geprüft, um festzustellen, ob der Server auf Weitere Nachrichten vom Client warten muss.</span><span class="sxs-lookup"><span data-stu-id="c58e7-106">The status returned by [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) is checked to see if the server needs to wait for additional messages from the client.</span></span> <span data-ttu-id="c58e7-107">In den meisten Authentifizierungs Protokollen gibt es eine maximale Anzahl von Austausch Vorgängen für die gegenseitige Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="c58e7-107">In most authentication protocols, there is a maximum number of exchanges even for mutual authentication.</span></span> <span data-ttu-id="c58e7-108">Derzeit führen sowohl die NTLM-als auch die [*Kerberos-Protokolle*](../secgloss/k-gly.md) gegenseitige Authentifizierung mit drei Austausch Vorgängen durch.</span><span class="sxs-lookup"><span data-stu-id="c58e7-108">Currently, both the NTLM and [*Kerberos protocols*](../secgloss/k-gly.md) do mutual authentication with three exchanges.</span></span>

 

 
