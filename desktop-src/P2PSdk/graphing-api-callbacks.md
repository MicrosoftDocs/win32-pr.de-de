---
description: 'Die graphende-API verwendet die folgenden Rückrufe:'
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Grafisch darzulegende API-Rückrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042266"
---
# <a name="graphing-api-callbacks"></a><span data-ttu-id="efdac-103">Grafisch darzulegende API-Rückrufe</span><span class="sxs-lookup"><span data-stu-id="efdac-103">Graphing API Callbacks</span></span>

<span data-ttu-id="efdac-104">Die graphende-API verwendet die folgenden Rückrufe:</span><span class="sxs-lookup"><span data-stu-id="efdac-104">The Graphing API uses the following callbacks:</span></span>



| <span data-ttu-id="efdac-105">Rückruf</span><span class="sxs-lookup"><span data-stu-id="efdac-105">Callback</span></span>                                                          | <span data-ttu-id="efdac-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efdac-106">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efdac-107">*Kostenlose pfnpeer- \_ \_ Sicherheits \_ Daten*</span><span class="sxs-lookup"><span data-stu-id="efdac-107">*PFNPEER\_FREE\_SECURITY\_DATA*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | <span data-ttu-id="efdac-108">Gibt die Funktion an, die von der Peer Diagramm Infrastruktur aufgerufen wird, um Daten freizugeben, die von [*pfnpeer \_ Secure \_ Record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) zurückgegeben werden, und [*pfnpeer-Daten \_ \_ Satz*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) Rückrufe</span><span class="sxs-lookup"><span data-stu-id="efdac-108">Specifies the function that the Peer Graphing Infrastructure calls to free data returned by [*PFNPEER\_SECURE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) and [*PFNPEER\_VALIDATE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) callbacks.</span></span> |
| [<span data-ttu-id="efdac-109">*sicherer pfnpeer- \_ \_ Datensatz*</span><span class="sxs-lookup"><span data-stu-id="efdac-109">*PFNPEER\_SECURE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | <span data-ttu-id="efdac-110">Gibt die Funktion an, die die Peer-graphinginfrastruktur zum Sichern von Datensätzen aufruft.</span><span class="sxs-lookup"><span data-stu-id="efdac-110">Specifies the function that the Peer Graphing Infrastructure calls to secure records.</span></span>                                                                                                                                        |
| [<span data-ttu-id="efdac-111">*pfnpeer-Überprüfungs \_ \_ Daten Satz*</span><span class="sxs-lookup"><span data-stu-id="efdac-111">*PFNPEER\_VALIDATE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | <span data-ttu-id="efdac-112">Gibt die Funktion an, die von der Peer Diagramm Infrastruktur zum Validieren von Datensätzen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="efdac-112">Specifies the function that the Peer Graphing Infrastructure calls to validate records.</span></span>                                                                                                                                      |



 

 

 



