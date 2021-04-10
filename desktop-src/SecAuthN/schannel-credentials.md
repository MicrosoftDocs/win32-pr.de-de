---
description: SChannel-Protokolle erfordern Anmelde Informationen, um Server und optional Clients zu authentifizieren.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: SChannel-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959636"
---
# <a name="schannel-credentials"></a><span data-ttu-id="cfcba-103">SChannel-Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="cfcba-103">Schannel Credentials</span></span>

<span data-ttu-id="cfcba-104">SChannel-Protokolle erfordern Anmelde Informationen, um Server und optional Clients zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="cfcba-104">Schannel protocols require credentials to authenticate servers and optionally, clients.</span></span> <span data-ttu-id="cfcba-105">Die Server Authentifizierung, bei der der Server einen Nachweis seiner Identität für den Client bereitstellt, ist für die SChannel- [*Sicherheitsprotokolle*](../secgloss/s-gly.md)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cfcba-105">Server authentication, where the server provides proof of its identity to the client, is required by the Schannel [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="cfcba-106">Die Client Authentifizierung kann vom Server jederzeit angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="cfcba-106">Client authentication may be requested by the server at any time.</span></span>

<span data-ttu-id="cfcba-107">SChannel-Anmelde Informationen sind [*X. 509*](../secgloss/x-gly.md) -Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="cfcba-107">Schannel credentials are [*X.509*](../secgloss/x-gly.md) certificates.</span></span> <span data-ttu-id="cfcba-108">Informationen zu [*öffentlichen*](../secgloss/p-gly.md) und [*privaten Schlüsseln*](../secgloss/p-gly.md) von Zertifikaten werden verwendet, um den Server und optional den Client zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="cfcba-108">[*Public*](../secgloss/p-gly.md) and [*private key*](../secgloss/p-gly.md) information from certificates is used to authenticate the server and optionally, the client.</span></span> <span data-ttu-id="cfcba-109">Diese Schlüssel werden auch zum Bereitstellen der Nachrichten [*Integrität*](../secgloss/i-gly.md) verwendet, während der Client und der Server die zum Generieren und Austauschen von [*Sitzungs Schlüsseln*](../secgloss/s-gly.md)erforderlichen Informationen austauschen.</span><span class="sxs-lookup"><span data-stu-id="cfcba-109">These keys are also used to provide message [*integrity*](../secgloss/i-gly.md) while client and server exchange the information required to generate and exchange [*session keys*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="cfcba-110">Informationen zur Programmierung finden Sie unter [beschaffen von SChannel-Anmelde](obtaining-schannel-credentials.md)Informationen.</span><span class="sxs-lookup"><span data-stu-id="cfcba-110">For programming information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
